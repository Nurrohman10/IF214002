# Pemodelan Data Historis

# Quiz

## contoh pemanfaatan data Historis
Archive Transaksi Lampau
## Perusahaan
## PT Halodoc


||Karyawan|
|---|---|
|PK|ID|
||Nama|
||Gaji Bulanan|
||Tanggal Mulai Gaji|
||Tanggal Mulai Kerja|
||Jabatan|
||Alamat|






||Histori Gaji|
|---|---|
|PK|Tanggal Mulai Gaji|
|PK|ID Karyawan|
||Tanggal Mulai Kerja|
||Gaji Bulanan|
||Jabatan|


```sql
CREATE TABLE
```
```python

databasekaryawan_ tbl(
   karyawan_id INT NOT NULL AUTO_INCREMENT,
   nama_karyawan VARCHAR(100) NOT NULL,
   gaji bulanan INT NOT NULL,
   tanggal_mulai_gaji_DATETIME,
   tanggal_masuk_date DATETIME,
   alamat_sekarang VARCHAR(100)
   Jabatan_sekarang CHAR(20)
   PRIMARY KEY ( karyawan_id )
);
datahistorigaji_ tbl(
   karyawan_id INT NOT NULL AUTO_INCREMENT,
   gaji bulanan INT NOT NULL,
   tanggal_mulai_gaji_DATETIME,
   PRIMARY KEY ( tanggal_mulai_gaji )
);
datahistorialamat_ tbl(
   karyawan_id INT NOT NULL AUTO_INCREMENT,
   tanggal_masuk_date DATETIME,
   alamat_sekarang VARCHA…
