#WRITING AND PRESENTATION WEEK 3
##SAMUEL MISKAN HANOCK - FRONT END DEVELOPMENT


###ARRAY
*Array* adalah variabel yang berisi banyak nilai (item). Sintaks array pada JavaScript mirip dengan variabel biasa. Array pada JavaScript digunakan untuk menyimpan daftar item (nama, judul, dan lain sebagainya). Array pada JavaScript adalah variabel yang dapat berisi lebih dari satu objek. array pada javascript memiliki beberapa ciri yaitu:
- Array pada Javascript adalah variabel yang berisi banyak nilai (item).
- Sintaks array pada JavaScript mirip dengan variabel biasa.
- Array pada JavaScript digunakan untuk menyimpan daftar item (nama, judul, dan lain sebagainya).
- Array pada JavaScript adalah variabel yang dapat berisi lebih dari satu objek.
- Ada dua cara untuk mendefinisikan sebuah array dalam JavaScript, tetapi ini dianggap sebagai praktik yang lebih baik untuk menggunakan metode literal array.
- Array pada JavaScript dapat menyimpan fungsi, objek, dan array lainnya.
- Array memiliki berbagai metode dan properti yang berguna.

**Mengapa menggunakan Array**
karena Array adalah kumpulan data bertipe sama yang menggunakan nama sama. dan juga ketika kita menggunakan array list dengan mudah, contoh kita ingin membuat list dari sebuah mobil
```javascript
let car1 = "Saab";
let car2 = "Volvo";
let car3 = "BMW"; 
```
Namun, bagaimana jika Anda ingin menelusuri mobil dan menemukan yang spesifik? Dan bagaimana jika Anda tidak memiliki 3 mobil, tetapi 300? Solusinya adalah array! Array dapat menampung banyak nilai di bawah satu nama, dan Anda dapat mengakses nilai dengan merujuk ke nomor indeks.

**Bagaimana membuat array**
Menggunakan literal array adalah cara termudah untuk membuat Array JavaScript.
contoh syntax nya:
```javascript
const array_name = [item1, item2, ...];    
```
contoh:
```javascript
const cars = ["Saab", "Volvo", "BMW"];
```
**Mengakses element array**
Kita bisa mengakses elemen array dengan melihat pada nomor indeks:
```javascript
const cars = ["Saab", "Volvo", "BMW"];
let car = cars[0];
```
yang dimana telah kita ketahui bahwa array dimulai dari index ke 0 bukan ke 1
**Mengubah element array**
kita juga dapat mengubah element dari suatu array dengan cara berikut:
```javascript
const cars = ["Saab", "Volvo", "BMW"];
cars[0] = "Opel";
```

**Mengakses full array**
Dengan JavaScript, array lengkap dapat diakses dengan mengacu pada nama dari suatu array:
```javascript
const cars = ["Saab", "Volvo", "BMW"];
document.getElementById("demo").innerHTML = cars;
```

**Array adalah object**
*Array* adalah jenis objek khusus. Operator typeof dalam JavaScript mengembalikan "objek" untuk array. Tapi, array JavaScript paling baik digambarkan sebagai array. Array menggunakan angka untuk mengakses "elemen" -nya. contoh: 
```javascript
//array
const person = ["John", "Doe", 46];

//object
const person = {firstName:"John", lastName:"Doe", age:46};
```

**Array bisa menjadi object**
Variabel JavaScript dapat berupa objek. Array adalah jenis objek khusus. Karena itu, kita dapat memiliki variabel dengan tipe berbeda dalam Array yang sama. kita dapat memiliki objek dalam Array. Anda dapat memiliki fungsi dalam Array. kita dapat memiliki array dalam Array:
```javascript
myArray[0] = Date.now;
myArray[1] = myFunction;
myArray[2] = myCars;
```


