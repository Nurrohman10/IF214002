## Sourcecode posgreSQL

- CREATE TABLE IF NOT EXISTS public."Admin Lab"
- (
   - "ID_Admin_Lab" character varying(30) COLLATE pg_catalog."default" NOT NULL,
   - "Nama_Dokter" character(50) COLLATE pg_catalog."default",
   - "Nama_Pasien" character(50) COLLATE pg_catalog."default",
   - "Jenis_Kelamin" character(15) COLLATE pg_catalog."default",
   - "Alamat" character varying(75) COLLATE pg_catalog."default",
   - "Jenis_Penyakit(spesialisasi)" character(50) COLLATE pg_catalog."default",
   - "Jenis_Pemeriksaan" character varying(50) COLLATE pg_catalog."default",
   - CONSTRAINT "Admin Lab_pkey" PRIMARY KEY ("ID_Admin_Lab")
- )

- TABLESPACE pg_default;

- CREATE TABLE IF NOT EXISTS public."Dokter"
- (
    - "ID_Dokter" character varying(20) COLLATE pg_catalog."default" NOT NULL,
    - "Nama_Dokter" character(50) COLLATE pg_catalog."default",
    - "Nama_Pasien" character(30) COLLATE pg_catalog."default",
    - "Jenis_Kelamin" character(15) COLLATE pg_catalog."default",
    - "Alamat" character varying(75) COLLATE pg_catalog."default",
    - "Jenis_Penyakit(spesialisasi)" character(50) COLLATE pg_catalog."default",
    - "Jenis_Pemeriksaan" character varying(50) COLLATE pg_catalog."default",
    - CONSTRAINT "Dokter_pkey" PRIMARY KEY ("ID_Dokter")
- )

- CREATE TABLE IF NOT EXISTS public."Laboratorium"
- (
   - "ID_Pasien" character varying(30) COLLATE pg_catalog."default" NOT NULL,
   - "ID_Admin_Lab" character varying(30) COLLATE pg_catalog."default",
   - "ID_Lab" character varying(30) COLLATE pg_catalog."default",
   - CONSTRAINT "Laboratorium_pkey" PRIMARY KEY ("ID_Pasien")
- )

- TABLESPACE pg_default;

- CREATE TABLE IF NOT EXISTS public."Pasien"
- (
    - "ID_Pasien" character varying(30) COLLATE pg_catalog."default" NOT NULL,
    - "Nama_Dokter" character(50) COLLATE pg_catalog."default",
    - "Nama_Pasien" character(30) COLLATE pg_catalog."default",
    - "Jenis_Kelamin" character(15) COLLATE pg_catalog."default",
    - "Alamat" char acter varying(75) COLLATE pg_catalog."default",
    - "Jenis_Penyakit(spesialisasi)" character(50) COLLATE pg_catalog."default",
    - "Jenis_Pemeriksaan" character varying(75) COLLATE pg_catalog."default",
    - CONSTRAINT "Pasien_pkey" PRIMARY KEY ("ID_Pasien")
- )

- TABLESPACE pg_default;

- CREATE TABLE IF NOT EXISTS public."Pemeriksaan"
- (
    - "ID_Pasien" character varying(30) COLLATE pg_catalog."default" NOT NULL,
    - "ID_Admin_Lab" character varying(30) COLLATE pg_catalog."default",
    - "ID_Lab" character varying(30) COLLATE pg_catalog."default",
    - "Kategori" character varying(30) COLLATE pg_catalog."default",
    - "Hasil" character(30) COLLATE pg_catalog."default",
    - "Status_Pengriman_Hasil" character(15) COLLATE pg_catalog."default",
    - "Waktu_Pengriman_Hasil" timestamp(6) with time zone,
    - "Waktu" timestamp(6) with time zone,
    - CONSTRAINT "Pemeriksaan_pkey" PRIMARY KEY ("ID_Pasien")
- )

- TABLESPACE pg_default;
