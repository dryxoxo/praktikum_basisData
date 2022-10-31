## No 1
```sql
CREATE DATABASE akademik_19102005;
```

### a. Tabel Mahasiswa
```sql
CREATE TABLE mahasiswa(
NIM int(10) NOT NULL PRIMARY KEY AUTO_INCREMENT,
nama varchar(30),
jenis_kelamin char(1),
tempat_lahir varchar(10),
tanggal_lahir date,
telepon varchar(13),
pembimbing_akademik varchar(30)
);
```

### b. Tabel Dosen
```sql
CREATE TABLE dosen(
NIDN int(12) NOT NULL PRIMARY KEY AUTO_INCREMENT,
nama varchar(30),
jenis_kelamin char(1),
jabatan varchar(10),
Kelompok_keahlian VARCHAR(20),
telepon varchar(13)
);
```

### c. mata_kuliah
```sql
CREATE TABLE mata_kuliah(
kode_mataKuliah int(12) NOT NULL PRIMARY KEY AUTO_INCREMENT,
nama_mataKuliah varchar(30),
sks char(1),
dosen_pengampu varchar(30),
hari VARCHAR(10),
jam varchar(6),
kode_ruang varchar(5)
);
```

### d. KRS
```sql
CREATE TABLE krs(
id_krs int(12) NOT NULL PRIMARY KEY AUTO_INCREMENT,
kode_mataKuliah int(12),
NIM int(10),
tahun year,
semester char(2),
nilai int(2)
);
```


## No 2
```sql
INSERT INTO mahasiswa VALUES
('19102005', 'Ibrohim Huzaimi', 'L', 'Banyumas', '29-03-2001', '082241626872', 'Yoso Adi Setyoko'),
('19102004', 'Imada Ramadhanti', 'P', 'Tegal', '28-01-2001', '088114422621', 'Yoso Adi Setyoko');
```

```sql
INSERT INTO dosen VALUES
('0617098802', 'Agi Prasetiadi', 'L', 'Dosen', 'Rekayasa Data', '08881111222'),
('0606019201', 'Amalia Beladinna Arifa', 'P', 'Dosen', 'Rekayasa Data', '08881111222');

```

```sql
INSERT INTO mata_kuliah VALUES
('21436', 'ETIKA PROFESI', '3', 'Amalia Julianudin', 'Kamis', '09:30:00', 'IO-103'),
('21437', 'Tugas Akhir 1', '3', 'Hiro Santoso', 'Kamis', '11:30:00', 'IOT-02');
```

```sql
INSERT INTO krs VALUES
('112233', '21436', '19102005', '2020', '3', '80'),
('112234', '21437', '19102004', '2020', '3', '82');
```

## No 3

```sql
SELECT * FROM mahasiswa;
```

```sql
SELECT * FROM dosen;
```

```sql
SELECT * FROM mata_kuliah;
```

```sql
SELECT * FROM krs;
```

## No 4

```sql
DESCRIBE mahasiswa;
```

```sql
DESCRIBE dosen;
```

```sql
DESCRIBE mata_kuliah;
```

```sql
DESCRIBE krs;
```


## No 5
### a. Hapus keterangan Primary Key pada ‘NIDN’

```sql
alter table dosen DROP PRIMARY KEY, change NIDN NIDN INT(12);
```

### b. Tambahkan kembali Primary Key pada ‘NIDN’

```sql
ALTER TABLE dosen
ADD PRIMARY KEY (NIDN);
```

### c. Tambahkan atribut alamat_domisili setelah atribut ‘tanggal_lahir’ pada tabel ‘mahasiswa’

```sql
ALTER TABLE mahasiswa ADD alamat_domisili varchar(30) AFTER tanggal_lahir;
```

### d. Tambahkan atribut program_studi setelah atribut ‘jenis_kelamin’ hapada tabel ‘dosen’

```sql
ALTER TABLE dosen ADD program_studi varchar(30) AFTER jenis_kelamin;
```

### e. Ubah nama tabel ‘dosen’ menjadi tabel_dosen

```sql
ALTER TABLE dosen RENAME TO tabel_dosen;
```

### f. Ubah nama atribut ‘nama’ pada tabel dosen menjadi nama_dosen

```sql
ALTER TABLE tabel_dosen CHANGE nama nama_dosen varchar(30);
```

### g. Ubah tipe data ‘jenis kelamin’ menjadi enum {‘pria’, ‘wanita’}

```sql
ALTER TABLE tabel_dosen MODIFY jenis_kelamin ENUM('pria', 'wanita');
```

### h. Ubah tipe data ‘telepon’ menjadi int

```sql
ALTER TABLE tabel_dosen MODIFY telepon int(13);
```

### i. Hapus atribut ‘jam’ pada tabel ‘mata_kuliah’

```sql
ALTER TABLE mata_kuliah DROP jam;
```

### j. Hapus atribut ‘nilai’ pada tabel ‘KRS’

```sql
ALTER TABLE krs DROP nilai;
```