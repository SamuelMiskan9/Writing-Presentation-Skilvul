# Samuel Miskan Hanock - Learning Track - Front End 
## Writing and Presentation - WEEK 2
# **SCOPE AND FUNCTION**
* **SCOPE**
    **SCOPE** adalah sebuah konsep dalam flow data variabel. scope menentukan, apakah variabel x dapat diakses pada titik tertentu atau tidak, atau manakah variable yang dapat diakses?, Scope ditentukan oleh block, block adalah {} yang sebelumnya ada di for, while, if.
    * Jenis-Jenis scope
        - *GLOBAL SCOPE*
        - *LOCAL SCOPE*
        
* **GLOBAL SCOPE**
    variabel yang bisa dideklarasikan secara global dan dapat digunakan di dalam file apa pun.  contohnya:
    ![global](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/image2/scope.PNG)
    
    penggunaan variabel diatas valid semua karena deklarasi variabel global
* **LOCAL SCOPE**
    variabel yang dideklarasikan secara local hanya bisa diakses pada scope tersebut contohnya:
    ![local](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/image2/local.PNG)

* **FUNCTION**
Fungsi adalah sebuah blok kode yang digunakan untuk membungkus suatu proses dengan tujuan agar penulisan kode atau proses yang sama tidak ditulis secara berulang kali.
    
- Cara Mendeklarasikan Suatu Fungsi

![function](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/image2/function.PNG)

- Cara Memanggil Fungsi
```js
	function here(param1, param2){
	return console.log(param1 + param2);
	}
	
	function done(){
	console.log("Hellow World");
	}
	
	here(1,2);
	done();
```

* **PARAMETER DAN ARGUMENT**
    * **PARAMETER** merupakan sebuah sebutan nilai untuk inputan fungsi pada saat fungsi tersebut di definisikan
    * **ARGUMENT** adalah sebutan untuk nilai inputan fungsi pada saat fungsi tersebut di panggil.
    
* **CONTOH ARGUMENT DAN PARAMETER**
- Argumen dan Parameter

![Argupara](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/image2/paramargument.PNG)

- Default Parameter

![default](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/image2/defaultparameter.PNG)

- Helper Function

    helper function adalah sifat fungsi yang dapat dipanggil didalam fungsi lainnya.
![Argupara](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/image2/helper.PNG)

## Data Types
data types adalah tipe data

data types garis besar dibagi menjadi 2 kategori primitive dan objects, tipe daya dijavascript tidak memiliki fondasi yang kuat contohnya kita bisa merubah-ubah tipe data.
```js
let myVar = "s" // tipe string
myVar = 1 // tipe number
myVar = {x:1} // tipe object
myVar = Undefined // tipe Undefined
myVar = NaN // tipe NaN (not a number)
```

### Primitive Data Types
primitive hanya memiliki 1 sifat.
primitive data types terdiri dari:
- Boolean: mendeskripsikan nilai true/false atau 1/0
```js
let bool = true;
```
- Null: menandakan sebuah variabel tidak ada isi
```js
let nullExample = null;
```
- Undefined: menandakan sebuah variabel belum terdefinisi suatu nilai atau "undefined"
```js
let x;
```
- Numeric
  - Number: menandakan variabel sebagai angka
  - BigInt: dapat menyimpan variabel diluar jangkauan aman number
  - NaN: menandakan variabel bukanlah angka
```js
let num = 10;
// sebuah variabel angka

let bigNum = BigInt(1000000000000000000000000000000);
console.log(Number.MAX_SAFE_INTEGER == Number.MAX_SAFE_INTEGER + 100 ? "sama" : "beda");
let nanExample = 0/0;
```
- String: menandakan variabel sebuah huruf, dan string memiliki sifat yang tidak dapat dimutasikan.
```js
let str = "abcd";
```


### Object Data Types
Properti dari object:
- value: Nilai yang diambil oleh akses dengan properti.
- writable: boolan yang menandakan apakah nilai dapat dirubah dengan perintah. `obj.name = "envyx"`
- enumerable: object dapat diiterasikan dengan menggunakan `for in...`
- configurable: sebuah boolean yang mengindikasikan apakah nilai/properti dari object dapat dirubah seperti di detele atau tambah.

## Built in Methods
### Math
Math adalah sebuah fungsi yang ada di javascript dan dapat diakses menggunakan `Math.`
```js
Math.method()
// atau
Math.property
```

beberapa method yang sering digunakan adalah sebagai berikut
- Math.PI, menampilkan nilai PI `3.14...`
```js
console.log(Math.PI);
```
- Math.abs(), membuat seluruh nilai positif
```js
console.log(Math.abs(-1));
// mencetak 1
```
- Math.ceil(), membulatkan keatas
```js
console.log(Math.ceil(Math.PI));
// mencetak 4
```
- Math.floor(), membulatkan kebawah
```js
console.log(Math.floor(Math.PI));
// mencetak 3
```
- Math.round(), membulatkan ke nilai terdekat jika 5.1 kebawah menjadi 5, 5.5 keatas menjadi 6s
```js
console.log(Math.round(Math.PI));
// mencetak 3
```
- Math.random(), memberikan angka acak dari dari 0 sampai 1
```js
console.log(Math.random());
// mencetak angka acak dari 0 sampai 1
```

### Prototype functions
prototype function adalah method atau properti yang ada pada sebuah variabel, contohnya jika kita memiliki variable 

integer memiliki beberapa prototype function

```js
let x = 1.129391208347;
let me = x.toFixed(3);
console.log(me);
```
string juga memiliki prototype function 

```js
let str = "   Hello mate!      ";
console.log(str.toUpperCase());

console.log(str.toLowerCase())

console.log(str.trim());

console.log(str.trim().toUpperCase());
```

selain itu kita dapat membuat prototype function dengan cara seperti ini
```js
String.prototype.read = function() {
	newStr = "";
	str = String(this);
	for(let i = 0; i < str.length; i++) {
		if(i % 2) {
			newStr += str[i].toLowerCase();
		} else {
			newStr += str[i].toUpperCase();
		}
	}
	return newStr;
}
```
prototype function akan merubah string dari `"saya suka makan atau tidak"` menjadi `"SaYa sUkA MaKaN AtAu tIdAk"`

fungsi tersebut berada di String.prototype.methods sehingga seluruh tipe data string dapat mengakses method tersebut.

## JavaScript Dasar - DOM Manipulation

- ### Memanipulasi HTML dan DOM
  <div align="justify">DOM (Document Object Model) merupakan cara untuk memanipulasi style, konten, dan element pada website. Setelah website dimuat, maka akan ada DOM yang terbentuk menjadi sebuah pohon dan terdiri dari parent & child.</div> <br/>
  
  <img src="https://raw.githubusercontent.com/SamuelMiskan9/image1/main/image2/dom.PNG" width="400" />
  <br/>
  
  DOM juga merupakan objek yang terdiri dari properties dan method. Lalu, cara untuk mendapatkan element HTML : <br/>
  
  ```md
    a) document.getElementById(id) // mendapatkan element berdasarkan id. Akan mendapatkan 1 element spesifik
    b) document.getElementsByTagName(name) // mendapatkan banyak element (collections) berdasarkan tag name
    c) document.getElementsByClassName(name) // mendapatkan banyak element (collections) berdasarkan class name
    d) document.querySelector(css selector) //mendapatkan satu element berdasarkan CSS selector
    e) document.querySelectorAll(css selector) // mendapatkan banyak element (collections) berdasarkan CSS selector
    f) parentElement // digunakan untuk menyeleksi parent dari suatu elemen 
    g) nextElementSibling // digunakan untuk menyeleksi elemen setelahnya dalam 1 parent
    h) previousElementSibling // digunakan untuk menyeleksi elemen sebelumnya dalam 1 parent
  ```
  
  <br/>
  Contohnya:
  
  `<html>`
  
  ```html
    <html>
      <head>
        <title>Website</title>
      </head>
      <body>
        <p id="para1">Hai</p> <!-- berdasarkan id -->
        
        <h1>Halo</h1> <!-- berdasarkan tag name -->
        <h1>Keren</h1>
        
        <ul>
          <li class="item">1</li> <!-- berdasarkan class nname -->
          <li class="item">2</li>
          <li class="item">3</li>
          <li class="item">4</li>
        </ul>
        
        <div class="box"></div> <!-- berdasarkan css selector -->
        
        <p class="orang">Samuel Miskan Hanock</p>
        <p class="orang">Arifian Saputra</p>
        <p class="orang">Syahri Rahmadhan</p>
        
      </body>
    </html>
  ```
  
  <br/>
  
  `<script>`
  
  ```js
    let a = document.getElementById("para1") // berdasarkan id
    
    let b = document.getElementsByTagName("h1") //berdasarkan tag name
    
    let c = document.getElementsByClassName("item") //berdasarkan class name
    
    let d = document.querySelector("div.box") // berdasarkan css selector (hanya mendapatkan 1 element HTML)
    
    let d = document.querySelectorAll("p.orang") // berdasarkan css selector (mendapatkan banyak element HTML)
  ```
  
  <br/>
  Cara merubah konten HTML: <br/>
  
  `<html>`
  
  <br/>
  
  ```html
    <html>
      <head>
        <title>Website</title>
      </head>
      <body>
        <div id="para1">Hai</div>
      </body>
    </html>
  ```
  
  <br/>
  
  `<script>`
  
  ```js
    document.getElementById("para1").innerHTML  = "<h1>teks baru</h1>"
  ```
  
  <br/>
  Catatan: merubah konten dengan `innerHTML` tidak hanya merubah teks, melainkan bisa saja merubah element HTML. <br/>
  
  Cara merubah nilai pada atribut HTML : <br/>
  
  `<html>`
  
  <br/>
  
  ```html
    <html>
      <head>
        <title>Website</title>
      </head>
      <body>
        <img src="pony1.png" id="img1"/>
      </body>
    </html>
  ```
  
  <br/>
  
  `<script>`
  
  ```js
    document.getElementById("img1").src  = "pony2.png"
    
    // struktur
    // document.getElementById("img1").attribute   = nilai
  ```
  
  <br/>
  Cara menambah langsung element pada HTML dengan JavaScript : <br/>
  
  ```html
    <html>
      <head>
        <title>Website</title>
      </head>
      <body>
        <p>Hai</p>
          <script>
            document.write("Hafi Ihza Farhana")
          </script>
        <p>Selamat tinggal</p>
      </body>
    </html>
  ```
  
  <br/>
  Cara memanipulasi element HTML : <br/>
  
  ```md
    a) document.createElement(e) // membuat element HTML
    b) document.removeChild(e) // menghapus element HTML
    c) document.appendChild(e) // menggabungkan element HTML
    d) document.replaceChild  // mengganti atau mengubah sebuah element HTML yang lama menjadi element baru
  ```
  
  Contohnya seperti berikut:
  <br/>
  
  `<html>`
  
  ```html
           <!DOCTYPE html>
      <html lang="en">
      <head>
          <meta charset="UTF-8">
          <meta http-equiv="X-UA-Compatible" content="IE=edge">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>Document</title>
      </head>
      <body>
          <div class="kontainer">
              <form action="">
                  <input type="text" id="nama" placeholder="isi nama">
                  <button type="submit" id="add">Tambah</button>
              </form>
              <ul class="todo" id="todo">
                  <li>Item</li>
              </ul>
          </div>
          <script src="script.js"></script>
      </body>
      </html>
  ```
  
  ```js
    let tambahButton = document.getElementById("add")
      let inputNama = document.getElementById("nama")

      tambahButton.addEventListener("click", (e) => {
          e.preventDefault()
          let valueInputNama = inputNama.value
          if(valueInputNama){
              tambahData(valueInputNama)
          }
      })

      let tambahData = (data) => {
          let list = document.getElementById("todo")
          // create li
          let item = document.createElement('li')
          item.innerText = data
          console.log(list.childNodes)
          list.insertBefore(item, list.childNodes[0])
      }
  ```
  
  <br/>
  Pada contoh di atas merupakan langkah untuk melakukan set data denga JavaScript.
  
 <br/>

  Memanipulasi Atribut : <br/>
  
  ```md
  1) setAttribute //untuk menetapkan atribut dengan nilai tertentu
  2) getAttribute //untuk mendapatkan nilai sebuah atribut
  3) removeAttribute //untuk menghapus atribut
  4) hasAttribute // memeriksa element tersebut memilik atribut atau tidak
  ```
  
  <br/>
  Memanipulasi element styling : <br/>
  
  ```md
  1) style.property // untuk mengatur element styling tertentu
  2) getComputedStyle // untuk mendapatkan style
  ```
  
  <br/>
  Events merupakan sebuah kejadian yang dilakukan berdasarkan interaksi pengguna pada webiste. Ada beberapa event, dan ini merupakan yang populer : <br/>
  
  ```md
  1) onchange // Terpicu ketika element dirubah
  2) onclick // Terpic ketika element di klik
  3) ondblclick // Terpicu ketika element di double click
  4) ondrag // Terpicu ketika element di seret
  5) onkeyup // Terpicu ketika key-up ditekan
  6) onload // Terpicu ketika website di load
  ```
  
  <br/>
