# Ide Solusi 
Membuat sistem terintegrasi antara informasi hasil lab dan dokter .

# Deskripsi 
Sistem ini dibuat untuk mempermudah integrasi informasi anatara hasil lab 
pasien dengan sistem yang di kelola oleh dokter yang manangani pasien tersebut Dengan Fitur-Fitur:
1. Menyimpan Hasil Lab
2. Mengirimkan Hasil Lab
3. Mengunduh dan Mengunggah Hasil Lab

# Entitas dan Atribut
## Dokter
1. Id
2. Nama dokter
3. Jenis kelamin 
4. Jenis penyakit (Spesialisasi)
5. Nama Pasien
6. Alamat 

## Pasien
1. Id
2. Nama pasien
3. Jenis kelamin
4. Alamat
5. Jenis penyakit (spesialisasi)
6. Nama dokter

## Admin lab
1. Id
2. Nama adm
3. Alamat
4. Nama dokter
5. Jenis penyakit (Spesialisasi) 
6. Jenis kelamin


## Laboratorium
1. Id
2. Waktu 
3. Jenis pemeriksaan

## Pemeriksaan
1. ID Pasien
2. ID Lab
3. ID Admin lab
4. Waktu
5. Kategori
6. Hasil
7. Status pengiriman hasil
8. Waktu pengiriman hasil
