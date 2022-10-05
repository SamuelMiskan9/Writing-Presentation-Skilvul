# Samuel Miskan Hanock - Learning Track - Front End 
## Writing and Presentation 
# **Unix Command Line**
* ### **CLI**
    Command line Interface adalah antarmuka pengguna berbasis teks ( UI ) yang digunakan untuk menjalankan program, mengelola file komputer, dan berinteraksi dengan komputer. Command Line Interface juga disebut antarmuka pengguna baris perintah , antarmuka pengguna konsol , dan antarmuka pengguna karakter.

* ### **SHELL**
    Shell adalah program yang digunakan untuk berkomunikasi atau memerintah sistem, atau arti secara lain sebagai penerjemah agar bisa terhubung dengan komputer

* ### **TERMINAL**
    Sebuah aplikasi yang dapat digunakan untuk mengakses CLI, ketika terminal dijalankan kita membutuhkan shell untuk memberi/mengetik perintah untuk menjalankannya.

* ### **FILE SYSTEM**
    mengatur bagaimana data disimpan di dalam sebuah system Sistem operasi Windows & Unix-like menyusun file dan direktori menggunakan struktur yang bentuknya mirip tree. bisa kita lihat contoh nya seperti gambar dibawah.
    
![tree](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/tree.JPG)

* ### **COMMAND**
    Beberapa contoh COMMAND yang bisa kita lakukan
    - pwd (print working directory), untuk melihat current working directory
    - dir (directory), untuk melihat directory
    - cd (change directory), untuk pindah directory
    - ls (list), untuk melihat isi file di dalam directory
    - touch, untuk membuat file directory
    - cp (copy), untuk menyalin file directory
    - mv (move), untuk memindahkan file directory
    - rm (remove), untuk menghapus file directory

* **

# **GIT & GITHUB**
* **Apa itu GIT dan GITHUB**
    - Git
    Merupakan aplikasi yang dapat melacaks suatu perubahan yang terjadi di suatu folder ataupun file, yang biasanya digunakan oleh programmer sebagai tempat untuk menyimpan file programan mereka karena lebih efektif. 
    - Github
    Merupakan vendor penyedia layanan git yang dimiliki oleh microsoft atau secara definisi merupakan layanan hosting berbasis web sebagai repositori git. 

        **Mengapa Wajib Menggunakan Github**
        Alasan utamanya adalah sepandai apapun programmer, tidak akan mampu untuk mengerjakan semuanya sendiri selamanya. Maka dari itu dengan menggunakan Git & Github akan memudahkan programmer untuk bisa bekerja sama dalam sebuah tim. Tujuan besarnya adalah programmer bisa berkolaborasi dengan programmer lainnya dengan mengerjakan proyek yang sama tanpa harus repot copy paste folder aplikasi yang terupdate. 
        
* **Command di dalam Git & Github**
    - *Git init* <nama proyek kamu>, ini command untuk membuat repositori baru
    ![init](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/repo.PNG)
    - *git commit*, untuk melakukan commit atau menyimpan perubahan pada version control pada git. Dan kita bisa menambahkan pesan untuk membeikan checkout pada setiap perbuahan. contohnya git commit "Commit Pertama"
    ![commit](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/commit.PNG)
    - *Git Push Origin* untuk mempublish file atau aplikasi ke github
    ![origin](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/origin.PNG)
    - *Git clone* merupakan sebuah perintah yang digunakan untuk membuat salinan repository lokal
    ![clone](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/clone.PNG)

* **

# **HTML**
* **Definisi HTML**
    HyperTextMarkupLanguage adalah adalah bahasa standar pemrogaman yang digunakan untuk membuat halaman website, yang diakses melalui internet.
* **Kerangka HTML**
    berikut merupakan kerangka dari HTML:
    ![html](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/htmlkerangka.PNG)
    diatas merupakan contoh kerangka awal dari suatu html, terdapat head dan body. pada bagian head kita bisa menuliskan judul dari html kita, dan pada bagian body itu     digunakan untuk membuat sebuah isi dari sebuah konten
* **Tag HTML**
    - Tag untuk membuat heading pada isi konten
    
    ![h1](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/heading.PNG)
    
    untuk heading sendiri terdapat 6 heading yaitu ,h1 ,h2, h3, h4, h5, h6
    - Tag untuk membuat sebuah paragraph
    
    ![p](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/paragraph.PNG)
    - Tag untuk membuat suatu link
    
    ![link](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/linkhtml.PNG)
    - Tag untuk membuat sebuah daftar/list
        * Ordered List
    
        ![ol](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/ol%20list.PNG)
        * Unordered List
    
        ![ul](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/ul%20list.PNG)
    - Tag untuk menampilkan sebuah gambar
    
    ![img](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/imghtml.PNG)

* **Deploy Html**
    Deploy adalah sebuah proses untuk menyebarkan aplikasi yang sudah kita kerjakan supaya bisa digunakan oleh orang-orang. Jika aplikasi kita HTML atau Web App kita perlu mendeploy ke server. Untuk melakukan hal tersebut kita bisa menggunakan layanan yang bernama Netlify

* **

# **CSS**

* **Definisi CSS**
    CSS adalah Cascading Style Sheet yang merupakan kumpulan dari perintah dimana digunakan untuk dapat menjelaskan tampilan dari sebuah laman website dalam mark up language. 
* **Langkah Menggunakan CSS**
    - *Inline CSS*
    Inline CSS digunakan untuk tag HTML tertentu. Atribut <style> digunakan untuk memberikan style ke tag HTML tertentu.
    
    ![inline](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/inline.PNG)
    
    - *Eksternal CSS*
    Kita akan menyisipkan kode CSS dengan cara membuat file CSS terpisah, dan lalu menyambungkannya dengan file HTML dengan menggunakan element.
    
    ![eksternal](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/eksternal1.PNG)
    
    ![eksternal](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/eksternal2.PNG)
    
    - *Internal CSS*
    Kode CSS internal diletakkan di dalam bagian <head> pada halaman. Class dan ID bisa digunakan untuk merujuk pada kode CSS, namun hanya akan aktif pada halaman tersebut.
    
    ![internal](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/internal.PNG)

* Syntax CSS
    CSS Syntax adalah syntax yang digunakan untuk menunjuk atau memilih HTML element mana yang ingin diberi style (dihias). CSS syntax terdiri dari selector, property, dan value. contohnya
    
    ![eksternal](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/eksternal2.PNG)
    
    - Body adalah selector yang akan diubah elementnya
    - background-color Adalah sebuah properti berupa bagian mana dari element HTML yang akan diubah. Contoh diatas kita akan mengubah background color dari element body.
    - blue adalah value yang diterapkan kedalam background-color.
    
* **Flexbox CSS**
    flexbox digunakan untuk membuat tampilan responsive dari halaman suatu web, dan cara membuatnya sebagai berikut:
    - membuat div baru dengan class wrapper untuk membuat lapisan kotaknya
    
    ![flexbox](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/wrapper.PNG)
    
    - kemudian kita styling css nya agar menyerupai dengan flexbox
    
    ![flexbox](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/csswrapper.PNG)
    
    - Hasilnya sebagai berikut
    
    ![hasilflexbox](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/hasilflexbox.PNG)
    

* **Deploy Netlify**
    - pertama kita harus login menggunakan GitHub
    - membuat project baru
    - hubungkan ke GitHub kita (atau memilih tool version kontrol yang tersedia)
    - otorisasi netlify
    - Pilih Repository yang akan di Deploy
    - Melakukan Konfigurasi
    - deploy website
* **

# **Algoritma dan Struktur Data**
* **Perbeedaan Algoritma dan Struktur Data**
    - **Algoritma** adalah proses atau serangkaian aturan yang harus diikuti dalam perhitungan atau operasi pemecahan masalah lainnya, terutama oleh komputer. Dengan kata lain, semua susunan logis yang diurutkan berdasarkan sistematika tertentu dan digunakan untuk memecahkan suatu masalah.
    - **Struktur Data** adalah cara penyimpanan , pengorganisasian , dan pengaturan data di dalam media penyimpanan komputer sehingga data tersebut dapat digunakan secara efisien. 
    
* **Manfaat Algoritma dan Struktur Data**
* **Algoritma**
    - Agar bisa membantu menyederhanakan suatu program yang rumit dan juga besar
    - Agar bisa mempermudah membuat program yang dapat menyelesaikan masalah tertentu
    - Agar memudahkan pembuatan program yang lebih rapi dan juga terstruktur
* **Struktur Data**
    - Memberikan kemudahan dalam proses pemrograman
    - Memudahkan dalam menggunakan konsep algoritma
    - Efisiensi memori yang dipakai
    - Memudahkan dalam pengaturan data

* **Penggunaan Algoritma**
    - **Menghitung Luas Segitiga**
    - *analisis*
        - Input: a (alas) dan t (tinggi)
        - Luas Segitiga = a*t/2
    - algoritma
        - Masukan nilai alas (a) dan nilai tinggi segitiga (t)
        - Maka untuk menghitung luas digunakan rumus alas dengan tinggi yang sudah ditentukan
        - Rumus untuk menghitung Luas Segitiga yaitu L = 1/2*a*t
        - Nilai L (Luas) akan dicetak sebagai output ke perangkat output (keluaran)
        
* **Penerapan Algoritma Kedalam Bahasa Pemrograman**
    - Algoritma Pemrograman Tarif Parkir
    
    ![JS](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/algoritmajs.PNG)
    

* **Pseudocode**
    Pseudocode adalah menuliskan algoritma sebelum kita implementasikan ke bahasa pemograman tertentu. contoh Pseudocode
    
    ![JS](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/pseudo.PNG)
    


* **

# **JavaScript**
* **Apa itu JavaScript**
    Javascript adalah bahasa pemograman yang sangat powerful yang digunakan untuk logic pada sebuah website dan Javascript juga dapat membuat website menjadi interaktif dan dinamis
* **Cara menjalankan Javascript**
    Menjalankan JavaScript Sangatlah mudah, tinggal melalui browser, Chrome dan Mozilla adalah browser yang mendukung semua fitur JavaScript
* **Syntax dan Statement**
    - alert()
    ![alert](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/alert().PNG)
    Dialog alert() biasanya digunakan untuk menampilkan sebuah pesan peringatan atau informasi.
    
    - prompt()
    ![prompt](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/prompt.PNG)
    Dialog prompt() berfungsi untuk mengambil sebuah inputan dari pengguna.
    
    - confirm()
    ![prompt](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/confirm().PNG)
    Dialog confirm() digunakan untuk melakukan konfirmasi dalam melakukan tindakan tertentu.
    
* **Tipe Data JavaScript**
Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming. ada 6 tipe data fundamental di dalam JavaScript yaitu:
    - **number**
    Tipe data number adalah tipe data yang mengandung semua angka termasuk angka desimal.

    - **string**
    Tipe data string adalah grup karakter yang ada pada keyboard laptop/PC kita yaitu letters (huruf), number (angka), spaces (spasi), symbol, dan lainnya.

    - **boolean**
    Tipe data boolean adalah tipe data yang hanya mempunyai 2 buah nilai. 2 buah nilai tersebu adalah TRUE (benar) or FALSE (salah). Analoginya adalah seperti tombol/button ON/OFF dan juga seperti sebuah jawaban antara YES/NO.

    - **null**
    Tipe data null adalah tipe data yang diartikan bahwa sebuah variable/data tidak memiliki nilai. Null berbeda dengan string kosong. String kosong masih memiliki tipe data string.

    - **undefined**
    Tipe data undefined adalah tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai. Undefined berbeda dengan null. Undefined didapat dari hasil berikut:
        - Nilai dari pemanggilan variabel yang belum didefinisikan
        - Nilai dari pemanggilan element array yang tidak ada
        - Nilai dari pemanggilan property objek yang tidak ada
        - Nilai dari pemanggilan fungsi yang tidak mengembalikan nilai (return)
        - Nilai dari parameter fungsi yang tidak memiliki argumen
        
    - **object**
    Tipe data object adalah koleksi data yang saling berhubungan (related). Tipe data pbject dapat menyimpan data dengan tipe data apapun (number, string, boolean, dan lainnya). Tipe data object mempunyai key dan value.
* **JavaScript Conditional**
Conditional merupakan statement percabangan yang menggambarkan suatu kondisi. Conditional statement akan mengecek kondisi spesifik dan menjalankan perintah berdasarkan kondisi tersebut. Yang dicek adalah apakah kondisi tersebut TRUE (benar). Jika TRUE maka code didalam kondisi tersebut dijalankan.
* **Contoh Conditional**
    - **if Statement**
    *contohnya*
    if (true){
        console.log('Pesan ini akan ditampilkan ketika kondisinya true')
    }
    - **if else statement**
     Else akan mengeksekusi sebuah statement/code jika suatu kondisi bernilai FALSE
    *contohnya*
    let haus = true;
    if (haus){
        console.log('Harus minum')
    }else{
        console.log('Tidak minum')
    }
    - **if else if statement**
    Else … If statement dapat kita gunakan jika kita mempunyai berbagai kondisi.
    - **Switch Case Conditional**
    Gunakan switch case jika kondisi dan percabangan terlalu banyak
* **Truthy and Falsy**
Truthy and falsy digunakan untuk mengecek apakah variabel telah terisi namun tidak mementingkan nilainya.

* **Operator Dalam JavaScript**
    - Operator Aritmatika
    terdapat 7 jenis operator aritmatika yaitu
        - Penjumlahan (+)
        - Pengurangan (-)
        - Perkalian (*)
        - Pembagian (/)
        - Modulus (%)
        - Increment (++)
        - Decrement (--)
    - Operator Pembandingan
        - Equal (=)
        - Not Equal(!=)
        - Identical(===)
        - Not Identical(!==)
        - Lebih Besar(>) 
        - Lebih Kecil(<)
        - Lebih Besar sama dengan(>=)
        - 	Lebih Kecil sama dengan(>=)
    - Operator Logika Javascript
        - and(&&)
        - or(||)
        - not(!)
    - Operator Penugasan(Assignment)
        - = 
        - +=
        - -=
        - *=
        - /=
        - %=

* **Looping**
Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.

* **Contoh Looping**
    - **For Loop**
    FOR LOOP merupakan instruksi pengulangan yang dapat kita berikan pada program yang kita kembangkan.
    
    ![for loop](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/fo%20loop.PNG)
    
    - **While Loop**
    WHILE LOOP akan menjalankan instruksi pengulangan kondisi bernilai TRUE.
    
    ![while loop](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/while%20loop.PNG)
    
    - **Do While**
    jika kita ingin setidaknya menjalankan pengulangan 1 kali sebelum dilakukan pengecekan kondisi kita membutuhkan Do While
    
    ![do while](https://raw.githubusercontent.com/SamuelMiskan9/image1/main/do%20while.PNG)
    
    - **Nested Loop**
    Jika kita membuat looping didalam looping. Maka ini dinamakan Nested Loop. Looping pertama dianalogikan sebagai baris. Looping kedua dianalogikan sebagai kolom.
