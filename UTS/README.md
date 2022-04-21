# 1. ERD 
### Adalah model atau rancangan untuk membuat database, supaya lebih mudah dalam menggambarkan data yang memiliki hubungan atau relasi dalam bentuk sebuah desain. Dengan adanya ER diagram, maka sistem database yang terbentuk dapat digambarkan dengan lebih terstruktur dan terlihat rapi. Untuk menyusun sistem database yang tepat, maka kita harus menentukan terlebih dahulu mengenai jenis model data yang akan digunakan. Yang mana, hal tersebut akan sangat berpengaruh nantinya pada pengembangan aplikasi sesuai dengan kebutuhan proyek bisnis. Model ER konseptual sangat berguna untuk mendokumentasikan segala bentuk arsitektur data pada sebuah organisasi. Model ini dapat digunakan untuk satu atau lebih jenis model data logis. Tujuan dari pengembangannya adalah untuk membangun struktur metadata untuk data master entitas dan set ER model logis.

## A. Data Logis
### Jenis yang pertama adalah model data logis, dimana untuk proses pembuatannya tidak membutuhkan model data konseptual. Komponen dalam model data logis antara lain, entitas data master, operasional, dan transaksional yang telah terdefinisi sebelumnya. Model ini juga dapat dikembangkan secara independen mulai dari yang lebih spesifik, hingga sistem manajemen basis data yang dapat diimplementasikan langsung.

## B. Data Fisik
### Model data fisik memungkinkan untuk dikembangkan dari model data logis. Model ini yang digunakan sebagai database. Model data fisik dipakai dalam menentukan metadata struktural dalam sistem manajemen database sebagai objek penyimpanan data yang bersifat relasional, contohnya tabel, indeks dan trigger pada database.
# 2. Mentransformasikan proses bisnis sebuah organisasi menjadi struktur data di basis data
### Langkah pertama kita harus memahami dulu proses bisnis dari suatu organisasi itu, sebagai contoh, misalkan kita akan mentrasnformasikan proses bisnis yaitu sistem aplikasi yang mengatur suatu perusahaan. Nah Langkah pertama kita harus menelusuri atau mengumpulkan informasi apa saja bagian atau role dari suatu karyawan, berapa gaji dari karyawan berdasarkan bidangnya dll. Setelah mengetahui alur dari proses bisnis suatu perusahaan tersebut kita bisa merancangnya , Tentukan entitas dan atribut. buat folwchart nya, buat diagram ERD nya. lalu normalisasikan data nya. setelah itu bisa langsung dibuat sqlnya. untuk menghindari kesalahan dalam proses pembuatan suatu aplikasi tersebut.
# 3. Ide solusi 
### Membuat sistem terintegrasi antara informasi laboratorium dan Dokter
## A. Deskripsi
### Sistem ini dibuat untuk mempermudah integrasi informasi anatara laboratorium dan dokter, dimana nantinya ketika ada keperluan untuk medical chek-up yang membutuhkan hasil laboratorium pasien tidak harus datang ke ruang administrasi laboratorium tersebut untuk mengambilnya, karena hal tersebut bisa dilakukan dengan sistem yang telah dirancang untuk mempermudah dokter dan pasien tersebut.
## B. Fitur - Fitur
### Menyimpan Hasil Lab
### Mengirimkan Hasil Lab
## C. ERD notasi Chen 
### ![image](https://user-images.githubusercontent.com/100698149/164351880-c852f8db-73b0-4055-9ed5-d3fe306076bb.png)
## D. ERD notasi Crow Foot
### ![image](https://user-images.githubusercontent.com/100698149/164354504-d2b1dbb9-9952-46bc-8df4-7763ed01af09.png)
