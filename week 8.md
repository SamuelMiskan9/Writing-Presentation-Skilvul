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
adalah seperangkat helpers yang memungkinkan Anda mengetes komponen pada React tanpa bergantung pada detail implementasinya. Pendekatan ini membuat refactoring menjadi mudah dan juga mendorong Anda untuk menerapkan best practices untuk aksesbilitas. Mungkin tidak memberikan cara untuk me-render secara “dangkal” pada sebuah komponen tanpa anak, test runner seperti Jest yang memungkinkan Anda melakukan mocking.



