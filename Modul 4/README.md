No 1.
```CREATE DATABASE db_akademik;```

No 2.

```Java
CREATE TABLE dosen(
Id_Dosen VARCHAR(6) PRIMARY KEY,
Nama_Dosen VARCHAR(20),
JK CHAR(1),
NoHP VARCHAR(20),
Gaji INT(11),
TunjanganJabatan INT(11),
Id_Produ VARCHAR(4)
);
```

No 3.

```java
INSERT INTO dosen VALUES
('D101', 'Kuncoro', 'L', '08123', '5000000', '5000000', 'P021'),
('D102', 'Mustika', 'P', '08125', '3750000', '0', 'P022'),
('D103', 'Safitri', 'P', '08126', '4550000', '5300000', 'P024'),
('D104', 'Prasetiadi', 'L', '08128', '5500000', '7500000', 'P021');
```

No 4.
```java
SELECT * FROM dosen;
```

No 5.
```java
SELECT Id_Dosen, Nama_dosen, Gaji FROM dosen;
```

No 6.

```java
SELECT Id_Dosen, Nama_dosen, Gaji, TunjanganJabatan, SUM(TunjanganJabatan + Gaji) FROM dosen;
```

```java
SELECT Id_Dosen, Nama_dosen, Gaji, TunjanganJabatan, (TunjanganJabatan + Gaji) AS total FROM dosen;
```

No 7.

```java
UPDATE dosen SET TunjanganJabatan = null WHERE Id_Dosen = 'D104';
```

No. 8

```
SELECT Id_Produ, COUNT(Id_Produ) FROM dosen GROUP BY Id_Produ;
```

