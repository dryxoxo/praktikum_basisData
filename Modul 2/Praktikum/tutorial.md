**no 1**
```sql
CREATE DATABASE db_perpustakaan;
```

**no 2**
```sql
CREATE TABLE master_buku(
kode_buku int(11),
nama_buku varchar(30),
pengarang varchar(10),
penerbit varchar(20),
tahun_terbit year,
jumlah_buku int(11)
);
```

**no 3**
```sql
INSERT INTO master_buku VALUES
('1', 'Kado untuk Sahabat', 'Izzatul Jannah', 'Eureka', '2003', '2'),
('2', 'Ice Breaker', 'Adi Soenarno', 'Penerbit Andi', '1997', '1'),
('3', 'Seni Berbicara', 'Larry King', 'Gramedia', '2010', '3'),
('4', 'Crayon Shinchan 46', 'Yoshito Usui', 'Gramedia', '2000', '2'),
('5', 'SPSS 13.0 Terapan Riset Parametrik', 'Triton', 'Penerbit Andi', '2015', '1'),
('6', 'Quantum Learning', 'Bobbi de Porter', 'Kaifa for Teens', '2005', '2'),
('7', '7 Habits of Highly Effective Teens', 'Sean Covey', 'Binarupa Aksara', '2009', '2'),
('8', 'Kepemimpinan dan Seni Berbicara', 'Kim H. Krisco', 'Professional Books', '2014', '2'),
('9', 'Pengantar Psikologi Klinis', 'Suprapti Slamet', 'UIP', '2011', '3'),
('10', 'How to Think Like a Computer Scientist – Learning Python 3th Edition', 'Peter Wentworth, Jeffery Elkner, Allen B. Downey, Chris Meyers', 'Free Software Foundation', '2012', '3');
```

**no 4**
```sql
ALTER TABLE master_buku ADD jumlah_halaman int(11) AFTER penerbit;
```

**No 5**
```sql
ALTER TABLE master_buku ADD isbn int(11) AFTER jumlah_halaman;
```

**No 6**
```sql
ALTER TABLE master_buku CHANGE nama_buku judul_buku varchar(30);
```

**No 7**
```sql
ALTER TABLE master_buku MODIFY pengarang varchar(30);
```

**No 8**
```sql
ALTER TABLE master_buku DROP jumlah_halaman;
```

**No 9**
```sql
ALTER TABLE master_buku DROP jumlah_buku;
```

**No 10**
```sql
ALTER TABLE master_buku ADD PRIMARY KEY(kode_buku);
```