# WRITING AND PRESENTATION WEEK 4
## SAMUEL MISKAN HANOCK - FRONT END DEVELOPMENT


## **Git Dan Github**
**Git**
Git adalah salah satu sistem pengontrol versi (Version Control System) pada proyek perangkat lunak

**Github**
Github adalah platform atau layanan web host yang memungkinkan tim developer untuk bekerja bersama secara online. Maksudnya bagaimana? Jadi, melalui Github, developer tidak hanya bisa menyimpan dan mengelola kode, tapi juga dapat mengajak timnya mengecek kode di waktu dan satu tempat yang sama.

**Perbedaan Git dengan Github**
Perbedaan utama dari Git dengan GitHub terletak pada fungsinya. Persamaan keduanya diantaranya terletak pada penyediaan Source Code Management (SCM) serta sama-sama memudahkan penggabungan dan pembagian kode. Bedanya, Git merupakan open-source software yang dirancang untuk merangkum riwayat sumber dari pengkodean. Tools ini mampu membalikkan perubahan hingga memberikan kesempatan pada seorang developer untuk membagikan kode kepada sesama developer. Kamu harus melakukan instalasi lokal untuk berkolaborasi menggunakan Git. Selain itu, Git punya peran sebagai tools terbaik dan banyak digunakan saat ini.

Di sisi lain, GitHub merupakan layanan hosting berbasis web sebagai repositori Git. GitHub menawarkan seluruh DVCS SCM dan diperkaya dengan beberapa fitur tambahan. Beberapa diantaranya berupa kolaborasi manajemen tiket, manajemen proyek, hingga pelacakan bug. Melalui GitHub, developer dapat membagikan, mengakses, serta menyimpan salinan repositori secara jarak jauh.

**Cara Kerja Git dan Github**
- Instalasi Git
- Atur Git dengan cara mengisi username dan email:
   ```md
       git config --global user.name = "(miskan?)"
       git config --global user.email = "(miskan@gmail.com)"
   ```
   
- Apabila ingin memeriksa instalasi berhasil atau tidak, maka ketikan:
   ```md
       git --version
   ```
- Setiap repository hanya berisi 1 direktori saja.
- Terdapat 3 fase yaitu working directory (modified), staging area (staged), dan commit (committed)
      - Fase working directory (modified) merupakan kondisi perubahan sudah dilakukan, tetapi belum ditandai (untracked) dan belum disimpan di version control.
      - Fase staging area (stagged) merupakan kondisi perubahan telah ditandai (tracked) dan belum disimpan di version control.
      - fase commit (committed) merupakan kondisi perubahan telah disimpan pada version control.  
- Pembuatan folder repository di GitHub bertujuan untuk menyediakan ruangan terhadap file yang siap di upload di GitHub dengan remote repository

- Masukan (push) file pada fase commit ke dalam gitHub
   
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




