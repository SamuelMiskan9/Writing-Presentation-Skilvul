# WRITING AND PRESENTATION WEEK 7
## SAMUEL MISKAN HANOCK - FRONT END DEVELOPMENT


## **Props Types**
**Props Types**
PropTypes merupakan library untuk menvalidasi props. Ini sangat membantu dalam meminimalkan bugs saat mengembangkan App besar. Jika props tidak benar type nya maka akan muncul warning.

**How To Install Props Types**
Berikut merupakan cara untuk menginstall react
```md
    npm install --save prop-types
```
setelah kita melakukan penginstalan terhadap prop types kita harus melakukan import terlebih dahulu agar props types nya dapat digunakan

```js
import { PropTypes } from "prop-types";
```
untuk melakukan pengujian terhadap props types kita harus membuat komponen beserta isinya, disini saya membuat satu komponen member yang berisikan
```js
import React from "react";
import { PropTypes } from "prop-types";

const Member = ({ name, age, data, info }) => {
  return (
    <div>
      <h2>{name}</h2>
      <h2>{age + 4}</h2>
    </div>
  );
};
```

setelah membuat file komponen, saatnya kita menggunakan fungsi yang terdapat didalam props types
 **Using Props-Types**
```js
Member.propTypes = {
    name: PropTypes.string,
}
```
fungsi diatas adalah, kondisi dimana ketika tipe data kita bertipe string, props types akan mengecek apakah tipe data yang kita gunakan benar atau tidak
```js
age: PropTypes.number
```
Kalau yang ini merupakan pengecekan tipe data yang berbentuk number oleh props-types
```js
data: PropTypes.array
```
Pengecekan tipe data berupa array
```js
age: PropTypes.oneOfType([PropTypes.string, PropTypes.number])
```
sedangkan ini merupakan fungsi dari props types yang melakukan pengecekan apabila tipe data yang kita gunakan terdapat dialam fungsi tersebut, yaitu tipe data string dan number
```js
age: PropTypes.any.isRequired,
```
kalau isRequired merupakan fungsi propstypes yang dimana kondisinya diharuskan kita harus/wajib mengisi tipe data jenis apa pun, jika tidak maka akan terjadi error
```js
data: PropTypes.arrayOf(PropTypes.number),
```
Kondisi jika tipe data didalam array bertipe number
```js
data: PropTypes.arrayOf(
    PropTypes.oneOfType([PropTypes.string, PropTypes.number])
    )
```
Kondisi jika tipe data didalam terdapat tipe data berupa string ataupun number
```js
info: PropTypes.object
```
ini tentang object
```js
info: PropTypes.shape({
  hoby: PropTypes.string,
  class: PropTypes.number,
  })
```
kondisi diatas adalah pengecekan tipe data yang terdapat didalam object

**Nilai dan Key**
```js
cek nilai dan key
   info: PropTypes.exact({
     hoby: PropTypes.string,
     class: PropTypes.number,
     address: PropTypes.string,
   }),
```

**Display Console Log Ketika Error**

![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/error.PNG)

jika tipe data yang kita berikan tidak sesuai dengan ketentuan props-types, maka akan timbul error seperti gambar diatas. terdapat error di console log yang berisi pesan, bahwa data yang kita input didalam Age tidaak sesuai, harus berbentuk number atau string. karena pada kasus ini saya memakai ketentuan dari props types yaitu oneOfTypes.

## **React Router**
Routing adalah proses di mana pengguna diarahkan ke halaman yang berbeda berdasarkan tindakan atau permintaan mereka. sedangkan React Router adalah suatu sistem library standar yang dibangun di atas React dan digunakan untuk membuat perutean di aplikasi React menggunakan Paket React Router. Ini menyediakan URL sinkron di browser dengan data yang akan ditampilkan di halaman web. Ini memelihara struktur standar dan perilaku aplikasi dan terutama digunakan untuk mengembangkan aplikasi web satu halaman.

**How To Install React Router**
```md
npm install react-router-dom@6
```

setelah diinstal kemudian kita import kedalam file main.jsx
```js
import { BrowserRouter as Router } from "react-router-dom";
```

```js
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";
import "./index.css";
import { BrowserRouter as Router } from "react-router-dom";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <Router>
      <App />
    </Router>
  </React.StrictMode>
);
```
kemudian setelah kita import kedalam file main.jsx kita, jangan lupa untuk membungkus <App /> dengan router atau BrowserRouter, agar ketika kita jalankan tidak terjadi error.

**Simple Routing***
```js
import "./App.css";
import { Link, Route, Routes } from "react-router-dom";
import Home from "./pages/Home";
import { About } from "./pages/About";
import Navbar from "./pages/Navbar";
import Projects from "./pages/Projects";
import Contact from "./pages/Contact";
import AOS from "aos";

AOS.init();

function App() {
  return (
    <>
      <Navbar />
      <Routes>
        <Route exact path="/" element={<Home />} />
        <Route path="/About" element={<About />} />
        <Route path="/Projects" element={<Projects />} />
        <Route path="/Contact" element={<Contact />} />
      </Routes>
    </>
  );
}
export default App;
```
berikut diatas merupakan contoh untuk routing dasar, dimaana kita menggunakan route kemudian dengan path sebagai alamat component yang ingin kita tuju. pada dasarnya sama saja dengan menggunakan a href.

**Dynamic Route**
```js
<BrowserRouter>
  /* Links */
  {heroes.map(hero => (<Link to={'heroes/' + hero.id} />)}

  /* Component */
  <Route path="heroes/:id" component={Hero} />
</BrowserRouter>

class Hero extends Component {
  render() {
    return (
      <div>
        {this.props.match.params.id}
      </div>
    );
  }
}
```
cara menggunakan Dynamic Route sebagi berikut
- Gunakan Tautan untuk membuat daftar rute secara dinamis.
- Gunakan titik dua (:) untuk mengindikasikan parameter dari url di dalam kondisi tertentu
- Gunakan objek serupa yang diteruskan sebagai props ke komponen route yang dirender untuk mengakses params url **this.props.match.params.id** .

**Nested Route**
```js
export default function App() {
    return (
        <Router>
            <Routes>
                <Route path='/' element={<Home />} />
                <Route path='about' element={<About />} />
                <Route path='posts' element={<Posts />}>
                    <Route path='new' element={<NewPost />} /> {/*A nested route!*/}
                    <Route path=':postId' element={<Post />} /> {/*A nested route!*/}
                </Route>
            </Routes>
        </Router>
    )
}
```
di antara  route komponen kita dapat menyematkan Route lain seperti
```md
<Route>{/* Children routes go here*/}</Route>
```
Nested route ini dapat menyampaikan informasi satu sama lain dan memastikan mereka ditampilkan dengan Nested  yang tepat.

## **State Management**
**Redux**
Redux adalah pustaka JavaScript sumber terbuka untuk mengelola dan memusatkan status aplikasi. redux juga merupakan salah satu state management

**How To Install Redux**
```md
npm install redux react-redux
```
kita harus membuat sebuah folder baru di dalam src dan memberi nama redux pada file itu
kemudian kita membuat file dengan nama store js dengan code seperti ini
```js
import { createStore } from "redux";
import { composeWithDevTools } from "redux-devtools-extension";
import rootReducer from "./reducers"; const store = createStore(
rootReducer,
composeWithDevTools()
)
export default store;
```
Setelah itu kita akan membuat reducer untuk todo listnya di src/store/reducers/todoReducer.js.
```js
const initialState = {
  todos: [
    {
      id: 1,
      title: "title one",
      completed: false
    },
    {
      id: 1,
      title: "title one",
      completed: false
    }
  ]
}const todoReducer = (state = initialState, action) => {
  const { type, payload} = action;
  switch(type){
    default:
      return {
        ...state
      }
  }
}export default todoReducer;
```
Gabungkan reducer — reducer di dalam file src/store/reducers/index.js dan sekarang kita hanya memiliki satu reducer yaitu todoReducer.
```js
import { combineReducers} from "redux";
import todoReducer from "./todoReducer";export default combineReducers({
  todoReducer
})
```

file app.jsx
```js
import React from "react";
import { Provider} from "react-redux";
import store from "./store"const App= () => {
  return(
    <Provider store={store}>
      <div>
        <TodoApp/>
      </div>
    </Provider>
  )
}export default App;
```
karena kita sudah terhuhung dengan store yang telah kita buat, maka Kita sudah bisa mengambil data dari store dan menampilkannya di UI. Di komponent TodoApp.js kita akan mengambil state dari store. Untuk itu kita membutuhkan function connect dari react-redux untuk menghubungkan komponent dan store.

Setelah itu buat sebuah fungsi untuk mengambil state dari store.


redux terdapat beberapa struktur yaitu
- **Store**
Seluruh status aplikasi terdaftar di tempat bernama Store. Ini bertindak sebagai otak dan mengelola status aplikasi. Ini juga memiliki fungsi pengiriman (Action).

- **Action**
objek murni yang dikirim atau dikirim dari tampilan. Ini dibuat untuk menyimpan informasi tentang acara pengguna seperti info tentang jenis tindakan, waktu terjadinya, lokasi kejadian, info tentang koordinatnya, dan info tentang keadaan yang ingin diubah.

- **Reducer**
Reducer adalah fungsi murni yang digunakan untuk mengembalikan keadaan baru dari keadaan awal. Ia membaca muatan dari tindakan. Peredam kemudian memperbarui toko melalui status yang sesuai.

**Redux Thunk**
Thunk merupakan Middleware untuk redux, thunk akan mengizinkan untuk menulis sebuah fungsi dengan logika didalamnya yang dimana bisa berinteraksi dengan Redux store dispatch dan getState methods.

**How To Install**
install dengan toolkit
```js
mport { configureStore } from '@reduxjs/toolkit'

import todosReducer from './features/todos/todosSlice'
import filtersReducer from './features/filters/filtersSlice'

const store = configureStore({
  reducer: {
    todos: todosReducer,
    filters: filtersReducer
  }
})
```
dengan cara diatas otomatis redux thunk sudah ter install
**Cara Manual**
```js
npm install redux-thunk
//atau
yarn add redux-thunk
```

Untuk Redux Toolkit, callback getDefaultMiddleware di dalam configureStore memungkinkan kita untuk meneruskan argumen ekstra khusus:
```js
import { configureStore } from '@reduxjs/toolkit'
import rootReducer from './reducer'
import { myCustomApiService } from './api'

const store = configureStore({
  reducer: rootReducer,
  middleware: getDefaultMiddleware =>
    getDefaultMiddleware({
      thunk: {
        extraArgument: myCustomApiService
      }
    })
})

// later
function fetchUser(id) {
  // The `extraArgument` is the third arg for thunk functions
  return (dispatch, getState, api) => {
    // kita bisa menggunakan api disini
  }
}
```

ketika kita ingin memberi multiple values kita bisa menggabungkannya untuk membuatnya menjadi single objek
```js
const store = configureStore({
  reducer: rootReducer,
  middleware: getDefaultMiddleware =>
    getDefaultMiddleware({
      thunk: {
        extraArgument: {
          api: myCustomApiService,
          otherValue: 42
        }
      }
    })
})

function fetchUser(id) {
  return (dispatch, getState, { api, otherValue }) => {

  }
}
```
ketika kita  menyiapkan Store secara manual, ekspor thunk default memiliki fungsi thunk.withExtraArgument() terlampir yang harus digunakan untuk menghasilkan middleware thunk yang benar:
```js
const store = createStore(
  reducer,
  applyMiddleware(thunk.withExtraArgument(api))
)
```
