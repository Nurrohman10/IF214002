# Tabel Normalisasi

## Tabel Dokter
|🔑ID_Dokter|Nama_Dokter|Nama_Pasien|Jenis_Kelamin|alamat|Jenis_Penyakit(spesialisasi)|Jenis_Pemeriksaan|
|---|-------|------|--|---|---|---|
|1. dr1|dr. Meliana, Sp. A|Mahran Rangga|L|Purwakarta|Anak|Tes Uji Protein C - Reaktif|
|2. Drg1| Drg. Wiena Manggala Putri|Maylan Nada|P|Cirebon|Gigi Dan Mulut|Sondasi|
|3. dr2| Dr. Alvin Nursalim, SpPD|Athalia Adzani|P|Yogyakarta|Penyakit Dalam|Magnetic Resonance Imaging (MRI)|


## Tabel Pasien
|🔑ID_Pasien|Nama_Dokter|Nama_Pasien|Jenis_Kelamin|alamat|Jenis_Penyakit(spesialisasi)|Jenis_Pemeriksaan|
|---|-------|------|--|---|---|---|
|1. Mahran-1|dr. Meliana, Sp. A|Mahran Rangga|L|Purwakarta|Anak|Tes Uji Protein C - Reaktif|
|2. Maylan-1| Drg. Wiena Manggala Putri|Maylan Nada|P|Cirebon|Gigi Dan Mulut|Sondasi|
|3. Athalia-1| Dr. Alvin Nursalim, SpPD|Athalia Adzani|P|Yogyakarta|Penyakit Dalam|Magnetic Resonance Imaging (MRI)|


## Tabel Admin Lab
|🔑ID_Admin_Lab|Nama_Dokter|Nama_Pasien|Jenis_Kelamin|alamat|Jenis_Penyakit(spesialisasi)|Jenis_Pemeriksaan|
|---|-------|------|--|---|---|---|
|1. LUSD-1|dr. Meliana, Sp. A|Mahran Rangga|L|Purwakarta|Anak|Tes Uji Protein C - Reaktif|
|2. LUGM-1|Drg. Wiena Manggala Putri|Maylan Nada|P|Cirebon|Gigi Dan Mulut|Sondasi|
|3. LUPD-1|RD-1|Dr. Alvin Nursalim, SpPD|Athalia Adzani|P|Yogyakarta|Penyakit Dalam|Magnetic Resonance Imaging (MRI)|


## Tabel Pemeriksaan
|🔑ID_Pasien|ID_Admin_Lab|ID_Lab|Waktu|Kategori|Hasil|Status_Pengriman_Hasil|Waktu_Pengriman_Hasil|
|---|---|---|---|---|---|---|---|
|1.  Mahran-1|LUSD-1|UP-1|10:15|D|Negative (-)|B|12:45|
|2.  Maylan-1|LUGM-1|PG-1|09:30|G|O|P|O|
|3.  Athalia-1|LUPD-1|RD-1|09:15|PG|Negative (-)|B|17:55|


## Tabel Laboratorium
|🔑ID_Pasien|ID_Admin_Lab|ID_Lab| 
|---|---|---| 
|1|LUSD-1|UP-1|  
|2|LUGM-1|PG-1| 
|3|LUPD-1|RD-1| 
