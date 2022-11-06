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




