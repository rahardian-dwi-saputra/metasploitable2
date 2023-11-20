# Hacking Metasploitable2
Metasploitable2 adalah mesin virtual (VM) Linux yang vulnerable. VM ini dapat digunakan untuk melakukan pelatihan cyber security, menguji tools keamanan jaringan, dan mempraktikkan teknik penetration testing.

## Requirement
- [Virtual Box](https://www.virtualbox.org/)
- [Metasploitable2](https://sourceforge.net/projects/metasploitable/)
- [Kali linux](https://www.kali.org/get-kali/#kali-virtual-machines)
- [OPNsense](https://opnsense.org/) (optional)

## Arsitektur Sistem

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/arsitektur%20sistem.png)

## Recognition
- Lakukan konfigurasi routing pada kali linux
```sh
ip route add 192.168.1.0/24 via <IP OPNsense>
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/recognition/recognition%201.png)

- Temukan IP Metasploitable2 dengan tool `nmap`
```sh
nmap -sn 192.168.1.0/24
```

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/recognition/recognition%202.JPG)

- Temukan IP Metasploitable2 dengan tool `nbtscan`

![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/assets/recognition/recognition%203.JPG)

- Hasil scanning port dengan nmap bisa dilihat [disini](nmap%20report.txt)

## Exploitation
- [Port 21 FTP](Exploit%20Port%2021%20FTP.md)
- [Port 22 SSH](Exploit%20Port%2022%20SSH.md)
- [Port 23 Telnet](Exploit%20Port%2023%20Telnet.md)
- [Port 25 SMTP](Exploit%20Port%2025%20SMTP.md)
- [Port 80 HTTP](Exploit%20Port%2080%20HTTP.md)
- [Port 139 dan 445 SMB](Exploit%20Port%20139%20dan%20445%20SMB.md)
- [Port 1099 Java RMI](Exploit%20Port%201099%20Java%20RMI.md)

## Peringatan
Semua materi yang disajikan disini hanya digunakan sebagai media pembelajaran. Penulis tidak bertanggung jawab atas penyalahgunaan dari materi tersebut