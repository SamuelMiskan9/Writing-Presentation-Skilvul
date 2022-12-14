# WRITING AND PRESENTATION WEEK 6
## SAMUEL MISKAN HANOCK - FRONT END DEVELOPMENT


## **React Js - Introduction**
**React JS**
React JS adalah library Javascript yang dimanfaatkan untuk membuat desain interface website. yang dimana bisa menyimpan code dari JavaScript, React juga di perkenalkan oleh Facebook pada tahun 2011 dan dirilis pada tahun 2013

**How To Install React**
Berikut merupakan cara untuk menginstall react
```md
    1. Kita harus menginstall node JS terlebih dahulu, karena node JS merupakan salah satu komponen ketika kita ingin menggunakan react
    2. Membuat folder yang nantinya dijadikan tempat untuk di bash dan membuat folder react didalamnya
```
 selanjutnya kita bisa mengunjungi situs resmi react untuk melakukan penginstalan, tetapi disini saya memilih Vite + React karena lebih terbiasa (OPSIONAL)
 
 **Membuat Folder**
 ```js
 npm create vite@latest learn-react -- --react
 ```
![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/vite/1.PNG)

ketika kita sudah menjalankan perintah nya akan keluar seperti itu, kemudian kita tinggal masuk kedalam folder yang telah kita buat, dan menjalankannya
```js
cd install-react
```
```js
npm install
```
lalu untuk menjalankannya kita melakukan
```js
npm run dev
```

kemudian untuk shortcut masuk kedalam Visual code kita tinggal menjalankan perintah
```md
code .
```

**Vite + React**
Setelah kita sudah melakukan penginstalan, sekarang kita masuk ke dalam VScode untuk melihat struktur dari React itu sendiri
![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/vite/2.PNG)
berikut merupakan struktur dari react, dimana terdapat file node_modules, public, src. untuk format file dari react adalah js, tetapi disini saya memakai jsx. jsx dan js tidak ada perbedaaan, fungsi dan sifat nya tetap sama dan dapat digunakan

untuk membuat isi didalam suatu komponen kita harus menggunakan tag <div> atau dengan menggunakan fragment <></>
```js
Menggunakan 
<div> </div>

atau

//Fragment
<> </>
```
Berikut merupakan tampilan function didalam suatu komponen
    
![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/3.PNG)
```md
Ketika kita menggunakan suatu function, dianjurkan untuk menulis huruf depan dengan huruf kapital agar fungsi yang kita buat dapat berfungsi dengan baik.
```

**Komponen Didalam React JS**
Komponen adalah bagian terpenting dari aplikasi React, karena aplikasi react sendiri terusun dari komponen-komponen. Komponen di Reactjs ada berbapa macam, Ada yang disebut dengan stateful component dan stateless component. Ada juga function components dan class components. Ada Dumb Components dan Smart Components. tetapi disini saya akan menjelaskan mengenai komponen dasar dari react

**Cara Membuat Komponen**
- untuk membuat suatu komponen kita bisa create folder baru, dan folder tersebut harus diletakkan didalam src, agar lebih teratur dan rapi
- kemudian kita membuat file component dengan huruf kapital diawal dengan format JSX

**Cara Menggunakan Komponen**
- pertama kita harus membuat struktur dari komponen yang telah kita buat, contohnya
```js
import React from 'react'

const Header = () => {
  return (
    <div>Header</div>
  )
}

export default Header
```
- disini saya membuat file component dengan nama Header, jangan lupa setiap komponen yang kita buat harus disertakan export agar nantinya bisa dipanggil kedalam komponen parent nya (app.jsx)

**Memanggil File Komponen**
untuk memanggil file komponen sangatlah mudah kita harus melakukan pemanggilan pada app.jsx dengan cara import file komponen nya, contohnya
```js
import Header from "./components/Header";
```
setelah dipanggil, didalam function App.jsx kita harus meletakkan sebuah tag, yang dimana tag tersebut adalah nama dari komponen yang telah kita buat,
```js
import { useState } from "react";
import ListDigimon from "./components/ListDigimon";
import "./App.css";
import Header from "./components/Header";

function App() {
  return (
    <div>
      <ListDigimon />
      <Header />
    </div>
  );
}

export default App;
```
**OUTPUT**
    
![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/vite/4.PNG)
   
### **Styling di React**
Untuk styling css di react tidak jauh berbeda dengan HTML dan CSS pada umumnya yang membedakan hanyalah nama class nya saja
```md
untuk HTML dan CSS menggunakan class="" saja
tetapi untuk react kita harus menulis dengan berbeda yaitu className=""
```
Seperti:

![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/vite/5.PNG)

![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/vite/6.PNG)

untuk melakukan styling seperti diatas kita yaitu seperti ini:
```css
.image-pfp {
  width: 150px;
  height: 150px;
  overflow: hidden;
  border-radius: 100%;
  object-fit: cover;
}

.profile-info {
  margin-left: 20px;
}

.profile-container {
  margin-left: 100px;
  display: flex;
  margin-top: 20px;
}
```
```md
catatan untuk pemanggilan CSS hanya dilakukan didalam file App.jsx saja
```


### **Prop and State**
**Props** adalah properti yang berbentuk parameter dari suatu function, cara kerja props adalah mengirimkan data properti dari child ke parent contonya kita membuat file child seperti:
```js
//Component Child
import React from "react";

const Header = ({ name, age, info, imgUrl }) => {
  return (
    <div>
      <div className="profile-container">
        <img src={imgUrl} alt="" className="image-pfp" />
        <div className="profile-info">
          <h2>My name is {name}</h2>
          <h3>I am {age} years old</h3>
          <p>{info}</p>
        </div>
      </div>
    </div>
  );
};
export default Header;
```
```js
//Component Parent
import { useState } from "react";
import "./App.css";
import Header from "./components/Header";

function App() {
  return (
    <div>
      <Header
        name={"Miskan"}
        age={"20"}
        info={"Halo batam"}
        imgUrl={
          "https://i.pinimg.com/236x/85/9a/f7/859af748d1eed0d67d5801a6df188a89.jpg"
        }
      />
      <Header
        name={"Arifian"}
        age={"20"}
        info={"Halo Pinang"}
        imgUrl={
          "https://divedigital.id/wp-content/uploads/2022/07/Anya-Forger-PFP-PROFILE-PICTURE.jpg"
        }
      />
    </div>
  );
}
export default App;
```
```js
const Header = ({ name, age, info, imgUrl })
```
berikut merupakan props yang berbentuk parameter yang berisikan nama age info dan img url yang nantinya akan dipanggil oleh komponen parent, contohnya seperti:
```js
return (
    <div>
      <div className="profile-container">
        <img src={imgUrl} alt="" className="image-pfp" />
        <div className="profile-info">
          <h2>My name is {name}</h2>
          <h3>I am {age} years old</h3>
          <p>{info}</p>
        </div>
      </div>
    </div>
  );
```
kalau kita lihat diatas pada tag h2, itu merupakan pemanggilan props dari komponent child, yang berisikan data properti yang telah kita buat tadi, ketika sudah dipanggil props nya maka akan muncul output seperti ini:

![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/vite/6.PNG)

properti diatas merupakan hasil dari penggunaan props

**State**
```md
sedangkan State adalah data yang tersimpan dalam sebuah component. State bersifat private dan hanya relevan terhadap component itu sendiri. Berbeda dengan props yang valuenya dilempar dari component lain, state justru dapat menyimpan dan mengubah datanya sendiri dari dalam.
```

untuk pengguaan useState seperti ini
```js
import { useState } from "react";

const [nama, getName] = useState("Munir");
const [umur, getAge] = useState(20);
```

## Perbedaan Statefull  dan Stateless
```md
Statefull:
Stateful components adalah komponen yang menggunakan state. 

Stateless:
Sedangkan Stateless adalah komponen yang tidak menggunakan state.
```
## **React Bootstrap**
Untuk menggunakan bootstrap didalam react, pertama yang harus kita lakukan adalah menginstall package bootstrap itu terlebih dahulu seperti:
```md
npm i bootstrap
```
lakukan penginstalan hingga selesai, setelah siap menginstal, kita membuat komponen baru dengan nama Navbar. perlu diingat jangan lupa untuk copy CDN dari bootstrap ke HTML di react agar bootstrap dapat digunakan.

setelah selesai kita membuat komponen baru dengan nama Navbar dan lakukan export import untuk memanggil navbarnya di dalam App.jsx
```js
import React from "react";

const Navbar = () => {
  return <div>
    <nav class="navbar bg-light">
  <div class="container-fluid">
    <a class="navbar-brand">Navbar</a>
    <form class="d-flex" role="search">
      <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search" />
      <button class="btn btn-outline-success" type="submit">Search</button>
    </form>
  </div>
</nav>
  </div>;
};

export default Navbar;
```
setelah kita membuat komponen dari Navbar, kita memanggil komponen kedalam App,jsx nya

![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/vite/7.PNG)

ketika sudah selesai memanggil komponennya maka OUTPUT nya akan seperti ini, navbar nya akan muncul:

![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/vite/9.PNG)

### **Penggunaan useState Untuk Button Increment dan Decrement**
berikut cara membuat tombol increment dan decrement menggunakan eventHandler dengan memasukkan fungsi useState
- pertama kita membuat komponen baru, seperti biasa. kemudian kita menambahkan fungsi decrement dan increment didalam nya:
```js
import React from "react";
import { useEffect } from "react";
import { useState } from "react";

const Count = () => {
  useEffect(() => {});

  const [count, setCount] = useState(0);
  const hitung = () => {
    setCount(count + 1);
  };
  const kurangi = () => {
    setCount(count - 1);
  };
  //   console.log("count", count);

  const [isLoading, setIsLoading] = useState(true);
  console.log("isLoading", isLoading);
  return (
    <div>
      <h1>Hallow</h1>
      <button onClick={hitung}>+</button>
      <span>{count}</span>
      <button onClick={kurangi}>-</button>

      <button onClick={() => setIsLoading(!isLoading)}>Ubah Loading</button>
      <span>{isLoading}</span>
    </div>
  );
};

export default Count;
```
contoh nya seperti diatas.
```js
//Function Increment
const [count, setCount] = useState(0);
  const hitung = () => {
    setCount(count + 1);
  };
```
```js
//Function Decrement
const kurangi = () => {
    setCount(count - 1);
  };
```
```js
return (
    <div>
      <h1>Hallow</h1>
      <button onClick={hitung}>+</button>
      <span>{count}</span>
      <button onClick={kurangi}>-</button>

      <button onClick={() => setIsLoading(!isLoading)}>Ubah Loading</button>
      <span>{isLoading}</span>
    </div>
  );
};
```
berikut adalah eventHandler berupa onclick yang dimana akan work ketika kita menekan tombol + dan -. maka hasilnya akan seperti ini

![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/vite/10.PNG)

kemudian ketika kita menekan tomboh +/- nya akan ada console log yang memberi tahu bahwa tombol tersebut bekerja

![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/vite/12.PNG)

### Penggunaan useState array of object untuk mengisi suatu data
untuk itu, kita harus membuatnya dalam bentuk useState ketika ingin menambahkan data contohnya seperti:
```js
import React from "react";
import { useState } from "react";

export const ListUser = () => {
  const [users, setUsers] = useState([
    {name: "John", umur: 20},
    {name: "David", umur: 21},
    {name: "Josh", umur: 22},
    {name: "Bayu", umur: 23},
  ]);
  return <div>ListUser</div>;
};
```

### **Login With ListMember**
```js
import { useState } from "react";
import Card from "./components/Card";
import Counter from "./components/Counter";
import ListUser from "./components/ListUser";

function App() {
  const [isLogin, setIsLogin] = useState(false);

  return (
    <div>
      {!isLogin && <button onClick={() => setIsLogin(true)}>Login</button>}

      <br />

      {isLogin ? <Counter /> : <span>login dulu cuuuy...</span>}

      {isLogin && <ListUser />}
    </div>
  );
}

export default App;
```

### React Hooks
Hooks merupakan fungsi yang memungkinkan Anda untuk ???mengaitkan??? state dan fitur-fitur lifecycle React dari function component. intinya hooks mempermudah penggunaan functional components, agar bisa menggunakan state dan lifecyle lainnya

Hooks yang sering digunakan adalah
- UseState
- useEffect

### **useEffect**
React hooks useEffect digunakan untuk menambahkan side effect ke function komponen. Penggunaan useEffect mirip dengan lifecycle method seperti componentDidMount, componentDidUpdate, dan componentWillMount di class component.
```js
import { useState, useEffect } from "react";
import ReactDOM from "react-dom/client";

function Timer() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    setTimeout(() => {
      setCount((count) => count + 1);
    }, 1000);
  });

  return <h1>I've rendered {count} times!</h1>;
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Timer />);
```

### LifeCycle
React Lifecycle terbagi kedalam 3 komponen yaitu
- Mounting
Fase dimana component dibuat dan mulai ditambahkan ke DOM.
- Updating
Fase dimana component di-render ulang karena perubahan props dan state.
- Unmounting
Fase dimana sebuah component dihapus dari DOM.

### Struktur Lifecycle
![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/vite/13.PNG)

contoh simple nya seperti ini:
```js
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  render() {
    return (
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
    );
  }
}
ReactDOM.render(<Header />, document.getElementById('root'));
```
