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
   
### Command didalam Github
- **Membuat Repositori Baru**. Ini digunakan untuk membuat repository baru. Yaitu folder yang akan dipantau oleh git.
```md
git init folder-baru
```

- **Melihat status dari git kita** perintah dari git status ini adalah menampilkan status yang terdapat didalam giat kita
```md
git status
```

- **Membuat atau menambahkan sebuah file kedalam git** kita bisa menggunakan git add, tetapi Dalam git itu ada 3 area dalam proses pengerjaanya mengerjakan.
- Working area - area yang belum di add
- Staging area - area yang sudah di add dan siap di commit
- Repository area - area yang sudah  di commit
Misalnya kita ingin membuat suatu file baru dalam repository kalian nah file baru tersebut akan masuk ke working area dahulu sebelum kalian melakukan git add
```md
git add [nama_file]
```
jika ingin memindahkan semua yang ada di working area ke staging area kita bisa memasukan perintah
```md
git add .
```
- **Git Checkout**
jika kita ingin membuat sebuah branch baru kita bisa memanggil perintah ini
```md
git branch [branch-baru]
```
jika kita ingin melepas branch yang sedang kita gunakan lalu membuat sebuah branch baru kita bisa menggunakan perintah yaitu
```md
git branch -b [branch-baru]
```
- **Git Merge**
Ini digunakan untuk menggabungkan branch ke branch yang aktif biasa ke branch master perintahnya!
```md
git merge [nama branch]
```
- **Git Commit**
digunakan untuk menyimpan perubahan yang sudah dilakukan, namun tidak ada perubahan yang terjadi pada remote repository.
```md
git commit -m "Pesan Kamu"
```
- **Git Log**
Untuk menampilkan daftar commit yang sudah dibuat perintahnya!
```md
git log
```

### Perintah Git Untuk Github
- **Git Clone** digunakan untuk mengcopy repository orang lain melalui URL
```md
git clone [url repository
```
- **Git Push** Biasa digunakan untuk mengupdate project yang ada di github dari git. Untuk melakukan push bisa diawali dengan mengclone terlebih dahulu lalu jika project kita yang sudah diubah dan kita bisa mengubahnya juga di github dengan printah!
```md
git push
```
- untuk push remote dari local ke server
```md
git push origin master
```
- **Git Pull** untuk mengupdate project kita yang ada di local yang sudah di clone dan ternyata project di github diupdate oleh kita di beda perangkat misalnya lalu kita ingin mengupdate suatu project yang ada di local lewat github tanpa melakukan clone
```md
git pull
```
- **Git Remote** Fungsinya untuk menghubungkan repository yang ada di local ke github kita. Jadi kita tidak perlu clone dahulu repo yang ada di github. Kelebihan remote itu Nama Repository yang dibuat git dilocal dan nama repository di github bisa beda. 
```md
git remote add origin https://github.com/username/nama_repo.git
```

### Langkah Langkah Untuk Melakukan Colaborasi Git
```md
    1.Salah satu buat github organisasi (auto leader)
    2.leader buat repository
    3.leader jadi first person yang bakal push lokal ke repository.
    4.leader invite siapa aja yang ada di repository tersebut
    5.anggota melakukan clone
    6. lakukan push dengan branch yang sesuai dengan fitur apa yang dibuat seperti 
    : Samuel-login
    7.leader buat pull request untuk penggabungan dari "hafi-login ke dev" dulu
    8.leader checking & merge
    9."git pull" sama kayak ngeclone, tapi tanpa link
```

## **Responsive Web Design**
**Responsive Web** design adalah tampilan website yang bisa menyesuaikan dengan device pengguna. Tampilan dari website akan menyesuaikan sesuai dengan ukuran layar pengguna, bisa jadi tampilan satu device dengan device lainnya akan berbeda. Semuanya aspek dari desain website mulai dari user interface, image, font, video akan menyesuaikan dengan resolusi device pengguna.

- **Mengatur ViewPort** untuk membuat suatu web yang responsive kita harus membutuhkan tag Viewport <meta> di seluruh halaman html kita
```html
 <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
 ```
 - **Menggunakan width Property**
 Ketika kita menstyling css menggunakan width property dengan value 100%, gambar yang kita pakai akan menjadi responsive dengan skala yang keatas dan kebawah, contohnya
```html
 <img src="ur_foto.jpg" style="width:100%;"> 
 ```
 - **Menggunakan max-width Property** ketika kita mengatur max-width menjadi 100%, maka gambar yang kita pakai akan menscalling kebawah ketika dibutuhkan, tetapi tidak akan pernah scalling keatas atau lebih besar dari size original nya
 ```html
  <img src="ur_foto.jpg" style="max-width:100%;height:auto;"> 
  ```
- **Media Query** sangat berguna untuk membuat layout kita responsive dengan menyesuaikan tampilan berdasarkan ukuran layar perangkat.Misalnya, media query berikut ini menguji untuk melihat apakah halaman web saat ini sedang ditampilkan sebagai media layar dan lebar area pandang setidaknya 800 px. CSS untuk pemilih .container hanya akan diterapkan jika kedua hal ini benar.
```css
@media screen and (min-width: 800px) {
  .container {
    margin: 1em 2em;
  }
}
```
 Media query dapat digunakan untuk memeriksa :
     a) Tinggi dan lebar viewport
     b) Tinggi dan lebar device
     c) Resolusi 
     d) Orientasi (landscape atau potrait)
     
     Namun, pada umumnya yang sering digunakan adalah melihat lebar dan tinggi device (screen).
- kita dapat menambahkan beberapa media query di dalam stylesheet, mengubah seluruh tata letak atau bagiannya agar sesuai dengan berbagai ukuran layar.

- **Flexible Grids**
Situs responsif tidak hanya mengubah tata letaknya di antara titik henti sementara, tetapi juga dibangun di atas grid yang fleksibel. Grids yang fleksibel berarti kita tidak harus menargetkan setiap kemungkinan ukuran perangkat yang ada, dan membangun tata letak piksel yang sempurna untuknya. Pendekatan itu tidak mungkin dilakukan mengingat banyaknya perangkat dengan ukuran berbeda yang ada, dan fakta bahwa setidaknya di desktop, orang tidak selalu memaksimalkan browser window mereka.
```css
.col {
  width: 6.12%; /* 60 / 980 = 0.0612 */
}
```
- #### Ordering dan orientation
```md
    `flex-direction` digunakan untuk mengatur letak child item. Ada 4 jenis:
    1.row untuk membentuk sebuah baris dari kiri ke kanan.
    2.row-reverse untuk membentuk baris dari kanan ke kiri.
    3.column untuk membentuk baris dari atas ke bawah.
    4.column-reverse untuk membentuk baris dari bawah ke atas.
```
```md
    `flex-wrap` digunakan untuk membuat tatal letak item <i>children</i> dalam satu tata letak saja. Ada 3 jenis
    1.no-wrap artinya tidak menggunakan flex-wrap.
    2.wrap artinya memiliki beberapa line dari atas ke bawah  jika space dalam 1 line sudah full width.
    3.wrap-reverse artinya memiliki beberapa line dari bawah ke atas  jika space dalam 1 line sudah full width.
```
- **`flex-flow`** merupakan gabungan dari `flex-wrap` dan `flex-direction`
- **`order`** digunakan untuk memposisikan yang akan diatur berdasarkan urutan order. Apabila semakin kecil, maka akan diposisikan paling awal. Namun, apabila `order` bernilai 0 tidak akan berubah karena merupakan value
 - #### Alignment:
```md
    `justify-content` digunakan untuk mengatur tata letak dan jarak antar item child secara horizontal dan vertikal. Ada 6 jenis:
    1.flex-start untuk memposisikan item di awal kontainer.
    2.flex-end untuk memposisikan item di akhir kontainer.
    3.center untuk memposisikan item di tengah kontainer.
    4.space-between untuk memposisikan antar ruang di setiap item.
    5.space-around memiliki jarak sebelum, setelah, dan setelah di tiap item.
    6.space-evenly memiliki posisi yang sama dengan `space-around` 
```
```md
    `align-self` digunakan untuk mengatur align. Ada 5 jenis:
    1.flex-start untuk memposisikan item di awal kontainer.
    2.flex-end untuk memposisikan item di akhir kontainer.
    3.center untuk memposisikan item di tengah kontainer.
    4.baseline memiliki kesamaan dengan flex-start .
    5.stretch untuk memposisikan item dengan full kontainer.
```
- **Align Content** `align-content` memiliki kesamaan dengan `justify-content` . Hanya saja yang membedakan pada `align-content` terdapat value
```md
    `align-items` digunakan untuk mengatur align dari item child secara vertikal. 
    Ada 5 jenis:
    1.flex-start untuk memposisikan item di awal kontainer.
    2.flex-end untuk memposisikan item di akhir kontainer.
    3.center untuk memposisikan item di tengah kontainer.
    4.baseline memiliki kesamaan dengan flex-start
    5.stretch untuk memposisikan item dengan full kontainer.
```
- #### Flexibility:
- `flex-grow` digunakan untuk mengatur ukuran suatu <i>item child</id> pada flexbox. Nilai harus angka dan tidak boleh minus.
         
- `flex-shrink` digunakan untuk membuat ukuran suatu <i>item child</i> mengecil secara relatif terhadap <i>item child</i> lainya. Nilai harus angka          dan tidak boleh minus. Semakin besar nilainya, maka semakin kecil ukuran dari suatu <i>item child</i>.
         
- `flex-basis` digunakan untuk menentukan lebar dari <i>item child</i>. Flexbox tidak bisa menggunakan properti `min-width` dan `max-width`. Ada 4 nilai dari `flex basis` :
```md
    1.auto akan menyesuaikan dengan kontenya
    2.angka (bisa menggunakan satuan)
    3.initial adalah bentuk default
    4.inherit akan diturunkan dari <i>parent</i>
```

## **BOOTSTRAP**
- **Pengertian**
Pengertian dari Bootstrap adalah kerangka kerja CSS yang bersifat open source dan digunakan untuk kebutuhan pembuatan tampilan desain visual dari aplikasi web atau situs website. Kerangka kerja yang digunakan berbentuk template desain berbasis HTML dan CSS untuk kebutuhan pengembangan navigasi, tombol, tipografi, formulir, dan komponen antarmuka yang lainnya.

- **Cara Menginstall Bootstrap**
cara menginstall bootstrap dengan cara mengintegrasikannya ke dalam format kode program kerangka HTML dan CSS, yaitu dengan cara manual atau online.
- **HTML**
```html
<script src=”https://maxcdn.bootstrapcdn.com/bootstrap/3.4.0/js/bootstrap.min.js”></script>

<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
```
- **Contoh Bootstrap**
```html
 <div class="jumbotron text-center">
  <h1>My First Bootstrap Page</h1>
  <p>Resize this responsive page to see the effect!</p>
</div>

<div class="container">
  <div class="row">
    <div class="col-sm-4">
      <h3>Column 1</h3>
      <p>Lorem ipsum dolor..</p>
    </div>
    <div class="col-sm-4">
      <h3>Column 2</h3>
      <p>Lorem ipsum dolor..</p>
    </div>
    <div class="col-sm-4">
      <h3>Column 3</h3>
      <p>Lorem ipsum dolor..</p>
    </div>
  </div>
</div> 
```

- **Kelebihan dan Kekurangan Bootstrap**
    - **Kelebihan**
    ```md
    1.Bootstrap dilengkapi dengan komponen antarmuka yang lengkap. Seperti bilah navigasi, sistem grid, serta carousel gambar
    
    2.Mudah dipelajari, karena memiliki banyak tutorial di forum daring, serta popularitasnya optimal
    
    3.Struktur file lebih sederhana
    
    4.Mempertahankan konsistensi di seluruh sintaks antara pengembang dan situs web
    
    5.Sistem grid telah ditentukan, menyelamatkan dari membuatnya di awal
    
    6.Sistem kisinya sudah ada, sehingga tidak perlu memasukkan kueri media ke file CSS
    ```
    - **Kekurangan**
    ```md
    1.Perlu penyesuaian yang berat untuk membuat satu proyek yang berbeda dari yang lain
    
    2.Jika tidak sesuai, semua situs web akan memiliki kerangka, komponen, serta desain yang sama, sehingga tidak terlihat profesional
    
    3.File Bootstrap berukuran besar, sehingga bisa memperlambat loading. Hal ini juga berkesempatan membebani server jika tidak hati-hati
    
    4.Untuk versi terbaru, Bootstrap memang kompatibel dengan berbagai peramban, akan tetapi tidak berlaku untuk versi yang lebih lama
    
    5.Gaya Bootstrap relatif besar, hal ini akan membuat keluaran HTML yang tidak perlu
    ```
