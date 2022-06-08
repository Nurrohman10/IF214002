
DDL
```python
CREATE TABLE IF NOT EXISTS public."Admin Lab"
(
    id_admin_lab character varying(30) COLLATE pg_catalog."default" NOT NULL,
    nama_dokter character(50) COLLATE pg_catalog."default",
    nama_pasien character(50) COLLATE pg_catalog."default",
    jenis_kelamin character varying(15) COLLATE pg_catalog."default",
    alamat character varying(75) COLLATE pg_catalog."default",
    jenis_penyakit_spesialisasi character(50) COLLATE pg_catalog."default",
    jenis_pemeriksaan character varying(50) COLLATE pg_catalog."default",
    CONSTRAINT "Admin Lab_pkey" PRIMARY KEY (id_admin_lab)
)

TABLESPACE pg_default;

CREATE TABLE IF NOT EXISTS public."Dokter"
(
    id_dokter character varying(20) COLLATE pg_catalog."default" NOT NULL,
    nama_dokter character(50) COLLATE pg_catalog."default",
    nama_pasien character(30) COLLATE pg_catalog."default",
    jenis_kelamin character(15) COLLATE pg_catalog."default",
    alamat character varying(75) COLLATE pg_catalog."default",
    jenis_penyakit_spesialisasi character(50) COLLATE pg_catalog."default",
    jenis_pemeriksaan character varying(50) COLLATE pg_catalog."default",
    CONSTRAINT "Dokter_pkey" PRIMARY KEY (id_dokter)
)

TABLESPACE pg_default;

CREATE TABLE IF NOT EXISTS public."Laboratorium"
(
    id_pasien character varying(30) COLLATE pg_catalog."default" NOT NULL,
    id_admin_lab character varying(30) COLLATE pg_catalog."default",
    id_lab character varying(30) COLLATE pg_catalog."default",
    CONSTRAINT "Laboratorium_pkey" PRIMARY KEY (id_pasien)
)

TABLESPACE pg_default;


CREATE TABLE IF NOT EXISTS public."Pasien"
(
    id_pasien character varying(30) COLLATE pg_catalog."default" NOT NULL,
    nama_dokter character(50) COLLATE pg_catalog."default",
    nama_pasien character(30) COLLATE pg_catalog."default",
    jenis_kelamin character(15) COLLATE pg_catalog."default",
    alamat character varying(75) COLLATE pg_catalog."default",
    jenis_penyakit_spesialisasi character(50) COLLATE pg_catalog."default",
    jenis_pemeriksaan character varying(75) COLLATE pg_catalog."default",
    CONSTRAINT "Pasien_pkey" PRIMARY KEY (id_pasien)
)

TABLESPACE pg_default;


CREATE TABLE IF NOT EXISTS public."Pemeriksaan"
(
    id_pasien character varying(30) COLLATE pg_catalog."default" NOT NULL,
    id_admin_lab character varying(30) COLLATE pg_catalog."default",
    id_lab character varying(30) COLLATE pg_catalog."default",
    kategori character varying(30) COLLATE pg_catalog."default",
    hasil character(30) COLLATE pg_catalog."default",
    status_pengriman_hasil character(15) COLLATE pg_catalog."default",
    waktu_pengriman_hasil timestamp(6) with time zone,
    waktu timestamp(6) with time zone,
    CONSTRAINT "Pemeriksaan_pkey" PRIMARY KEY (id_pasien)
)

TABLESPACE pg_default;


```
DML

```python
INSERT INTO "Admin Lab" (id_admin_lab,nama_dokter,nama_pasien,jenis_kelamin,alamat,jenis_penyakit_spesialisasi,jenis_pemeriksaan) VALUES (
  'adm2',
  'terawan',
  'rayhan',
  'male',
  'garut',
  'dalam',
  'ctscan'
); SELECT * FROM "Admin Lab";
INSERT INTO "Admin Lab" (id_admin_lab,nama_dokter,nama_pasien,jenis_kelamin,alamat,jenis_penyakit_spesialisasi,jenis_pemeriksaan) VALUES (
  'adm3',
  'devya',
  'nenti',
  'female',
  'indramayu',
  'gigi',
  'medical care '
); SELECT * FROM "Admin Lab";
INSERT INTO "Admin Lab" (id_admin_lab,nama_dokter,nama_pasien,jenis_kelamin,alamat,jenis_penyakit_spesialisasi,jenis_pemeriksaan) VALUES (
  'adm4',
  'sadewa',
  'norma',
  'female',
  'bekasi',
  'kulit',
  'laser'
); SELECT * FROM "Admin Lab";
INSERT INTO "Admin Lab" (id_admin_lab,nama_dokter,nama_pasien,jenis_kelamin,alamat,jenis_penyakit_spesialisasi,jenis_pemeriksaan) VALUES (
  'adm5',
  'calista',
  'dila',
  'female',
  'bandung',
  'kulit',
  'botox'
); SELECT * FROM "Admin Lab";

INSERT INTO "Dokter" (id_dokter,nama_dokter,nama_pasien,jenis_kelamin,alamat,jenis_penyakit_spesialisasi,jenis_pemeriksaan) VALUES (
  'dr2',
  'terawan',
  'rayhan',
  'male',
  'garut',
  'dalam',
  'ctscan'
); SELECT * FROM "Dokter";
INSERT INTO "Dokter" (id_dokter,nama_dokter,nama_pasien,jenis_kelamin,alamat,jenis_penyakit_spesialisasi,jenis_pemeriksaan) VALUES (
  'dr3',
  'devya',
  'nenti',
  'female',
  'indramayu',
  'gigi&mulut',
  'medical care'
); SELECT * FROM "Dokter";
INSERT INTO "Dokter" (id_dokter,nama_dokter,nama_pasien,jenis_kelamin,alamat,jenis_penyakit_spesialisasi,jenis_pemeriksaan) VALUES (
  'adm4',
  'sadewa',
  'norma',
  'female',
  'bekasi',
  'kulit',
  'laser'
); SELECT * FROM "Dokter";
INSERT INTO "Dokter" (id_dokter,nama_dokter,nama_pasien,jenis_kelamin,alamat,jenis_penyakit_spesialisasi,jenis_pemeriksaan) VALUES (
  'dr5',
  'calista',
  'dila',
  'female',
  'bandung',
  'kulit',
  'botox'
); SELECT * FROM "Dokter";

INSERT INTO "Laboratorium" (id_pasien,id_admin_lab,id_lab) VALUES (
  'c2',
  'adm2',
  'lab2'
); SELECT * FROM "Laboratorium";
INSERT INTO "Laboratorium" (id_pasien,id_admin_lab,id_lab) VALUES (
  'c3',
  'adm3',
  'lab3'
); SELECT * FROM "Laboratorium";
INSERT INTO "Laboratorium" (id_pasien,id_admin_lab,id_lab) VALUES (
  'c4',
  'adm4',
  'lab4'
); SELECT * FROM "Laboratorium";
INSERT INTO "Laboratorium" (id_pasien,id_admin_lab,id_lab) VALUES (
  'c5',
  'adm5',
  'lab5'
); SELECT * FROM "Laboratorium";

INSERT INTO "Pasien" (id_pasien,nama_dokter,nama_pasien,jenis_kelamin,alamat,jenis_penyakit_spesialisasi,jenis_pemeriksaan) VALUES (
  'c3',
  'terawan',
  'rayhan',
  'male',
  'garut',
  'dalam',
  'ctscan'
); SELECT * FROM "Pasien";
INSERT INTO "Pasien" (id_pasien,nama_dokter,nama_pasien,jenis_kelamin,alamat,jenis_penyakit_spesialisasi,jenis_pemeriksaan) VALUES (
  'c4',
  'devya',
  'nenti',
  'female',
  'indramayu',
  'gigi',
  'medical care '
); SELECT * FROM "Pasien";
INSERT INTO "Pasien" (id_pasien,nama_dokter,nama_pasien,jenis_kelamin,alamat,jenis_penyakit_spesialisasi,jenis_pemeriksaan) VALUES (
  'c5',
  'sadewa',
  'norma',
  'female',
  'bekasi',
  'kulit',
  'laser'
); SELECT * FROM "Pasien";
INSERT INTO "Pasien" (id_pasien,nama_dokter,nama_pasien,jenis_kelamin,alamat,jenis_penyakit_spesialisasi,jenis_pemeriksaan) VALUES (
  'c6',
  'calista ',
  'dila',
  'female',
  'bandung',
  'kulit',
  'botox'
); SELECT * FROM "Pasien";

INSERT INTO "Pemeriksaan" (id_pasien,id_admin_lab,id_lab,kategori,hasil,status_pengriman_hasil,waktu_pengriman_hasil,waktu) VALUES (
  'c1',
  'adm1',
  'lab1',
  'cancer',
  'negative ',
  'berhasil',
  '2017-08-09 07:00:00 -7:00',
  '2017-08-09 07:00:00 -8:00'
); SELECT * FROM "Pemeriksaan";
INSERT INTO "Pemeriksaan" (id_pasien,id_admin_lab,id_lab,kategori,hasil,status_pengriman_hasil,waktu_pengriman_hasil,waktu) VALUES (
  'c2',
  'adm2',
  'lab2',
  'continue ',
  'negative',
  'pending',
  '2017-08-09 07:00:00 -7:00',
  '2017-08-09 07:00:00 -7:10'
); SELECT * FROM "Pemeriksaan";
INSERT INTO "Pemeriksaan" (id_pasien,id_admin_lab,id_lab,kategori,hasil,status_pengriman_hasil,waktu_pengriman_hasil,waktu) VALUES (
  'c6',
  'adm3',
  'lab3',
  'continue ',
  'positive ',
  'berhasil',
  '2017-08-09 07:00:00 -5:00',
  '2017-08-09 07:00:00 -7:05'
); SELECT * FROM "Pemeriksaan";
INSERT INTO "Pemeriksaan" (id_pasien,id_admin_lab,id_lab,kategori,hasil,status_pengriman_hasil,waktu_pengriman_hasil,waktu) VALUES (
  'c5',
  'adm4',
  'lab4',
  'low',
  'negative ',
  'berhasil',
  '2017-08-09 07:00:00 -7:07',
  '2017-08-09 07:00:00 -7:11'
); SELECT * FROM "Pemeriksaan";
```

