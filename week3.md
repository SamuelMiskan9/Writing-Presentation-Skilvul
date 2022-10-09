# WRITING AND PRESENTATION WEEK 3
## SAMUEL MISKAN HANOCK - FRONT END DEVELOPMENT


### ARRAY
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
Namun, bagaimana jika Kita ingin menelusuri mobil dan menemukan yang spesifik? Dan bagaimana jika kita tidak memiliki 3 mobil, tetapi 300? Solusinya adalah array! Array dapat menampung banyak nilai di bawah satu nama, dan kita dapat mengakses nilai dengan merujuk ke nomor indeks.

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
// array
const person = ["John", "Doe", 46];

// object
const person = {firstName:"John", lastName:"Doe", age:46};
```

**Array bisa menjadi object**
Variabel JavaScript dapat berupa objek. Array adalah jenis objek khusus. Karena itu, kita dapat memiliki variabel dengan tipe berbeda dalam Array yang sama. kita dapat memiliki objek dalam Array. Anda dapat memiliki fungsi dalam Array. kita dapat memiliki array dalam Array:
```javascript
myArray[0] = Date.now;
myArray[1] = myFunction;
myArray[2] = myCars;
```

**Array properti dan method**
Dengan array kita bisa mem-build sebuah property maupun method contohnya:
```javascript
cars.length   // Returns the number of elements
cars.sort()   // Sorts the array 
```
**Array length **
Kita dapat menghitung banyak array dengan menggunakan fungsi length contohnya:
```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let length = fruits.length;
```

**Mengakses array pertama dan terakhir dalam suatu element**
```javascript
// Mengakses first array
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits[0];

// Mengakses last array
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits[fruits.length - 1];
```

**Menggunakan looping dengan array**
kita dapat menggunakan loop didalam suatu array, yaitu dengan cara menggunakan loop **for loop** , contohnya:
```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fLen = fruits.length;

let text = "<ul>";
for (let i = 0; i < fLen; i++) {
  text += "<li>" + fruits[i] + "</li>";
}
text += "</ul>";
```
**array For Each**
merupakan method array di JavaScript yang mengeksekusi fungsi yang disediakan sekali untuk setiap elemen array. Method ini mengembalikan nilai undefined dan tidak mengubah array asli, tapi jika dibutuhkan kita bisa memodifikasi array sumber di dalam badan fungsi.
```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];

let text = "<ul>";
fruits.forEach(myFunction);
text += "</ul>";

function myFunction(value) {
  text += "<li>" + value + "</li>";
} 
```
**Menambah array didalam element**
Kita bisa menambah value atau array baru di dalam suatau element menggunakan push() method, contohnya:
```javascript
 const fruits = ["Banana", "Orange", "Apple"];
fruits.push("Lemon");  // Menambah array baru yaitu (Lemon)

// Juga bisa menambahkan array menggunakan length = "Lemon"
 const fruits = ["Banana", "Orange", "Apple"];
fruits[fruits.length] = "Lemon";  // Menambah "Lemon" kedalam fruits

// Menambahkan array dengan index yang tinggi akan terjadi Undifined
const fruits = ["Banana", "Orange", "Apple"];
fruits[6] = "Lemon";  // Membuat array undifined didalam fruits
```

### OBJECT
Objek  adalah sebuah variabel yang menyimpan nilai (properti) dan fungsi (method). contoh object didalam javascript itu seperti:
```javascript
// Terdapat variable car dengan value Bmw
let car = "Bmw";

// Terdapat variable car dengan berbagai object didalamnya, seperti type, model dan warna
const car = {type:"Fiat", model:"500", color:"white"};
```
**Mendefiniskan Objek**
kita bisa define dan membuat sebuah object menggunakan objek literal contohnya:
```javascript
const person = {firstName:"Samuel", lastName:"Miskan", age:20, eyeColor:"Brown"};

// atau kita bisa sejajarkan object didalam variable person nya sebagai berikut
const person = {
  firstName: "Samuel",
  lastName: "Miskan",
  age: 21,
  eyeColor: "Brown"
};
```
**Objek Properti**
terdapat sebuah properti ketika kita membuat suatu objek yaitu:
```javascript
// Contoh object sebagai berikut, objek tersebut memiliki properti yaitu
// firstName Samuel
// lastName Miskan
// age 21
// eyeColor Brown
const person = {
  firstName: "Samuel",
  lastName: "Miskan",
  age: 21,
  eyeColor: "Brown"
};
```
**Mengakses Properti Objek**
Kita dapat mengakses properti dari sebuah object dengan cara:
```javascript
objectName.propertyName
// atau
objectName["propertyName"]

// contohnya
const person = {
  firstName: "Samuel",
  lastName: "Miskan",
  age: 21,
  eyeColor: "Brown"
};
person.lastName;
person["lastName"];
```
**Object Method**
*Objek* juga memiliki sebuah method, Metode adalah tindakan yang dapat dilakukan pada objek. Metode disimpan dalam properti sebagai definisi fungsi. contohnya:
```javascript
// Metode adalah fungsi yang disimpan sebagai properti.

const person = {
  firstName: "Samuel",
  lastName : "Miskan",
  id       : 4411,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```
