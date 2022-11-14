# WRITING AND PRESENTATION WEEK 8
## SAMUEL MISKAN HANOCK - FRONT END DEVELOPMENT


## **React Context**
**React Context**
Context merupakan Context provides a way to pass data through the component tree without having to pass props down manually at every level. Singkat saja, Context itu seperti variable global yang bisa kamu akses dimana saja tanpa kiyta harus memparsing props ke setiap komponen.

**Kapan Harus Menggunakan Context**
ketika kita menggunakan React, kita harus menggunakan context ini segera. Tapi, kita harus menganalisis aplikasimu terlebih dahulu. Aplikasimu bakal besar atau tidak? Jika tidak, maka sangat direkomendasikan untun menggunakan context ini.
Jika kita mempunyai aplikasi yang besar, kamu tidak disarankan untuk menggunkan context ini. Karena jika kamu mempunyai aplikasi yang besar, mungkin Kita harus segera menggunakan redux.  
Jadi maksudnya adalah, kita di rekomendasikan menggunakan context ini jika kita mempunyai aplikasi dengan skala kecil ke menengah untuk membuat aplikasimu mudah di kembangkan dan mudah di mengerti oleh orang-orang.

**Membuat Context**
```js
import { createContext } from "react"

export default createContext()
```
 **Membuat Provider**
```js
import MyContext from './myContext';

export default class Parent extends React.PureComponent {

  state = {
    xyz: 0
  }

  // ... dst

  render() {
    return (
      <MyContext.Provider value={this.state}>
        <div>
          <ChildA />
        </div>
      </MyContext.Provider>
    );
  }
}
```
**Komponen Child B**
```js
import React from "react";
import MyContext from "./myContext";

export default props => {
  return (
    <MyContext.Consumer>
      {value => {
        return <div>{value.xyz}</div>;
      }}
    </MyContext.Consumer>
  );
};
```

**Menggunakan Context.Consumer**
```js
import React from "react";
import CounterContext from "./counterContext";

export default props => {
  return (
    <CounterContext.Consumer>
      {value => {
        console.log("PrevDisplay: context value", value);
        return <div>Previous: {value.previousCount}</div>;
      }}
    </CounterContext.Consumer>
  );
};

```

**Pake contextType (life-cycle)**
```js
import React from "react";
import CounterContext from "./counterContext";

export default class PrevDisplay extends React.PureComponent {
  static contextType = CounterContext;
  // context bisa dipake di life-cycle API
  componentDidMount() {
    console.log("[PrevDisplay componentDidMount] context", this.context);
  }
  render() {
    return <div>Previous: {this.context.previousCount}</div>;
  }
}

```

## **React Testing**
adalah seperangkat helpers yang memungkinkan Anda mengetes komponen pada React tanpa bergantung pada detail implementasinya. Pendekatan ini membuat refactoring menjadi mudah dan juga mendorong Anda untuk menerapkan best practices untuk aksesbilitas. Mungkin tidak memberikan cara untuk me-render secara “dangkal” pada sebuah komponen tanpa anak, test runner seperti Jest yang memungkinkan Anda melakukan mocking. contohnya
```js
import React from 'react'
import {rest} from 'msw'
import {setupServer} from 'msw/node'
import {render, fireEvent, waitFor, screen} from '@testing-library/react'
import '@testing-library/jest-dom'
import Fetch from '../fetch'

const server = setupServer(
  rest.get('/greeting', (req, res, ctx) => {
    return res(ctx.json({greeting: 'hello there'}))
  }),
)

beforeAll(() => server.listen())
afterEach(() => server.resetHandlers())
afterAll(() => server.close())

test('loads and displays greeting', async () => {
  render(<Fetch url="/greeting" />)

  fireEvent.click(screen.getByText('Load Greeting'))

  await waitFor(() => screen.getByRole('heading'))

  expect(screen.getByRole('heading')).toHaveTextContent('hello there')
  expect(screen.getByRole('button')).toBeDisabled()
})

test('handles server error', async () => {
  server.use(
    rest.get('/greeting', (req, res, ctx) => {
      return res(ctx.status(500))
    }),
  )

  render(<Fetch url="/greeting" />)

  fireEvent.click(screen.getByText('Load Greeting'))

  await waitFor(() => screen.getByRole('alert'))

  expect(screen.getByRole('alert')).toHaveTextContent('Oops, failed to fetch!')
  expect(screen.getByRole('button')).not.toBeDisabled()
})
```

**Import**
```js
// import dependencies
import React from 'react'

// import API mocking utilities from Mock Service Worker
import {rest} from 'msw'
import {setupServer} from 'msw/node'

// import react-testing methods
import {render, fireEvent, waitFor, screen} from '@testing-library/react'

// add custom jest matchers from jest-dom
import '@testing-library/jest-dom'
// the component to test
import Fetch from '../fetch'
```

**Implementasi Dengan mockAPI**
```js
// declare which API requests to mock
const server = setupServer(
  // capture "GET /greeting" requests
  rest.get('/greeting', (req, res, ctx) => {
    // respond using a mocked JSON body
    return res(ctx.json({greeting: 'hello there'}))
  }),
)

// establish API mocking before all tests
beforeAll(() => server.listen())
// reset any request handlers that are declared as a part of our tests
// (i.e. for testing one-time error scenarios)
afterEach(() => server.resetHandlers())
// clean up once the tests are done
afterAll(() => server.close())

// ...

test('handles server error', async () => {
  server.use(
    // override the initial "GET /greeting" request handler
    // to return a 500 Server Error
    rest.get('/greeting', (req, res, ctx) => {
      return res(ctx.status(500))
    }),
  )

  // ...
})
```



