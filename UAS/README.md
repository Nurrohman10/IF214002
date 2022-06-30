# Jawaban
1. 
a. Ide Solusi 
Membuat sistem terintegrasi antara informasi hasil lab dan dokter .

b. Fitur Utama 
Sistem ini dibuat untuk mempermudah integrasi informasi anatara hasil lab 
pasien dengan sistem yang di kelola oleh dokter yang manangani pasien tersebut Dengan Fitur-Fitur:
1. Menyimpan Hasil Lab
2. Mengirimkan Hasil Lab

c.
# ![image](https://user-images.githubusercontent.com/100698149/176569181-4a9a0f75-2eba-41f4-b8de-2cfcca47ac4e.png)

d. DDL
```python
CREATE TABLE IF NOT EXISTS public.adminlab
(
    id_admin_lab integer NOT NULL,
    jenis_kelamin character varying(15) COLLATE pg_catalog."default",
    alamat character varying(75) COLLATE pg_catalog."default",
    nama_admin character(50) COLLATE pg_catalog."default",
    CONSTRAINT adminlab_pkey PRIMARY KEY (id_admin_lab)
)

TABLESPACE pg_default;

CREATE TABLE IF NOT EXISTS public.dokter
(
    id_dokter integer NOT NULL,
    nama_dokter character(50) COLLATE pg_catalog."default",
    jenis_kelamin character(15) COLLATE pg_catalog."default",
    alamat character varying(75) COLLATE pg_catalog."default",
    jenis_penyakit_spesialisasi character(50) COLLATE pg_catalog."default",
    jenis_pemeriksaan character varying(50) COLLATE pg_catalog."default",
    CONSTRAINT dokter_pkey PRIMARY KEY (id_dokter)
)

TABLESPACE pg_default;

CREATE TABLE IF NOT EXISTS public.laboratorium
(
    id_lab integer NOT NULL,
    id_admin_lab integer,
    id_pasien integer NOT NULL,
    CONSTRAINT laboratorium_pkey PRIMARY KEY (id_lab)
)


TABLESPACE pg_default;


CREATE TABLE IF NOT EXISTS public.pasien
(
    id_pasien integer NOT NULL,
    nama_pasien character(30) COLLATE pg_catalog."default",
    jenis_kelamin character(15) COLLATE pg_catalog."default",
    alamat character varying(75) COLLATE pg_catalog."default",
    jenis_penyakit_spesialisasi character(50) COLLATE pg_catalog."default",
    CONSTRAINT pasien_pkey PRIMARY KEY (id_pasien)
)

TABLESPACE pg_default;


CREATE TABLE IF NOT EXISTS public.pemeriksaan
(
    id_pasien integer NOT NULL,
    id_admin_lab character varying(30) COLLATE pg_catalog."default",
    id_lab character varying(30) COLLATE pg_catalog."default",
    kategori character varying(30) COLLATE pg_catalog."default",
    hasil character(30) COLLATE pg_catalog."default",
    status_pengriman_hasil character(15) COLLATE pg_catalog."default",
    waktu_pengriman_hasil timestamp(6) with time zone,
    waktu timestamp(6) with time zone,
    jenis_pemeriksaan character varying(75) COLLATE pg_catalog."default",
    CONSTRAINT pemeriksaan_pkey PRIMARY KEY (id_pasien)
)


TABLESPACE pg_default;


```
DML

Admin Lab
```python
INSERT INTO public.adminlab (id_admin_lab,jenis_kelamin,alamat,nama_admin) VALUES
	 (1,'male','garut','rifqi'),
	 (2,'male','sumedang','rifky'),
	 (3,'male','bandung','nugraha'),
	 (4,'male','rijki','majalengka');
```
Dokter
```python
INSERT INTO public.dokter (id_dokter,nama_dokter,jenis_kelamin,alamat,jenis_penyakit_spesialisasi,jenis_pemeriksaan) VALUES
	 (1,'terawan','male','garut','dalam','ctscan'),
	 (2,'devya','female','indramayu','gigi','medicalcare'),
	 (3,'sadewa','female','bekasi','kulit','laser'),
	 (4,'calista','female','bandung','kulit','botox');
```
Laboratorium
```python
INSERT INTO public.laboratorium (id_lab,id_admin_lab,id_pasien) VALUES
	 (1,1,1),
	 (2,2,2),
	 (3,3,3),
	 (4,4,4);
```
Pasien
```python
INSERT INTO public.pasien (id_pasien,nama_pasien,jenis_kelamin,alamat,jenis_penyakit_spesialisasi) VALUES
	 (1,'rayhan','male','garut','dalam'),
	 (2,'nenti','female','indramayu','gigi'),
	 (3,'norma','female','bekasi','kulit'),
	 (4,'dila','female','bandung','kulit');
```
Pemeriksaan
```python
INSERT INTO public.pemeriksaan (id_pasien,id_admin_lab,id_lab,kategori,hasil,status_pengriman_hasil,waktu_pengriman_hasil,waktu,jenis_pemeriksaan) VALUES
	 (1,'1','1','cancer','negative','berhasil','2017-08-09 21:00:00+07','2017-08-09 22:00:00+07','ctscan'),
	 (2,'2','2','continue ','negative','pending','2017-08-09 21:00:00+07','2017-08-09 21:10:00+07','mri'),
	 (3,'3','3','continue ','positive','berhasil','2017-08-09 19:00:00+07','2017-08-09 21:05:00+07','usg'),
	 (4,'4','4','low','negative','berhasil','2017-08-09 21:07:00+07','2017-08-09 21:11:00+07','mri');
```


DQL
```python
SELECT
	adminlab.nama_admin,
    laboratorium.id_admin_lab
FROM
	adminlab
INNER JOIN laboratorium
    ON laboratorium.id_admin_lab = adminlab.id_admin_lab
order by id_lab

SELECT jenis_pemeriksaan, COUNT(*) AS jumlah from pemeriksaan group by jenis_pemeriksaan order by jenis_pemeriksaan; ") or exit("Error with quering database
```
