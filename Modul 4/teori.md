# 1. 
```JAVA
 SELECT JK as Jenis_Kelamin FROM dosen;
 ```

 # 2.
 ```JAVA
SELECT d.Nama_Dosen, m.nama FROM mahasiswa AS m, dosen AS d
 ```

 # 3.
 ```JAVA
SELECT * From dosen, mahasiswa;
 ```

# 4.
``` JAVA
SELECT * FROM dosen WHERE Id_Produ = 'P021' AND GAJI > 3000000;
```

# 5.
``` JAVA
SELECT * FROM dosen WHERE Nama_Dosen LIKE 'F%';
```

# 6.
``` JAVA
SELECT DISTINCT Id_Produ FROM dosen;
```

# 7.
``` JAVA
SELECT * FROM dosen LIMIT 2;
```

# 8.
``` JAVA
SELECT * FROM dosen GROUP BY Id_Produ;
```

# 9.
```JAVA
SELECT Id_Produ, COUNT(*) FROM dosen GROUP BY Id_Produ;
```

# 10.
```JAVA
SELECT Nama_Dosen, Gaji + TunjanganJabatan AS TotalGaji FROM dosen HAVING TotalGaji >5000000;
```

# 11.
```JAVA
SELECT Nama_Dosen, Gaji + TunjanganJabatan AS TotalGaji FROM dosen HAVING TotalGaji >5000000 ORDER BY Nama_Dosen;

SELECT Nama_Dosen, Gaji + TunjanganJabatan AS TotalGaji FROM dosen HAVING TotalGaji >5000000 ORDER BY Nama_Dosen DESC;
```

# 12.
```JAVA
SELECT Nama_Dosen, Id_Produ,  Gaji + TunjanganJabatan AS TotalGaji FROM dosen HAVING TotalGaji >5000000 ORDER BY Nama_Dosen, Id_Produ;
```

# 13.
```JAVA
SELECT * FROM dosen WHERE Gaji BETWEEN 3000000 AND 4000000;
```

# 14.
```JAVA
SELECT * FROM dosen WHERE Gaji > ALL (SELECT Gaji FROM dosen WHERE Gaji = 3000000);

SELECT * FROM dosen WHERE Gaji > ALL (SELECT Gaji FROM dosen WHERE Id_Produ = 'P021');
```

# 15.

```JAVA
SELECT * FROM dosen WHERE Gaji > ANY (SELECT Gaji FROM dosen WHERE Id_Produ = 'P021');
```

# 16.

```JAVA
SELECT * FROM dosen WHERE Gaji IN (5000000, 5500000);
```

# 17.

```JAVA
SELECT * FROM dosen WHERE Gaji > EXISTS (SELECT Gaji FROM dosen WHERE Id_Produ = 'P021');
```