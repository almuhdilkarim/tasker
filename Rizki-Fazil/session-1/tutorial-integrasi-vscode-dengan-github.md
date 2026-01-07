# tutorial mengintegrasikan aplikasi Vscode dengan Github

## setp 1 : buka aplikasi vscode di laptop
![WhatsApp Image 2025-09-22 at 14 40 52](https://github.com/user-attachments/assets/9c947bad-23dd-4411-895d-ac3a89283121)
## step 2 : klik ikon terminal yang berada di barisan kanan atas
![WhatsApp Image 2025-09-22 at 14 40 53](https://github.com/user-attachments/assets/b52cc72c-e3c2-4b21-9040-405bcc6f7f22)
## step 3 : buat file ssh
untuk membuat file ssh, tambahkan text
```
ssh-keygen -t ed25519 -C "your email"
```
![WhatsApp Image 2025-09-22 at 14 41 30](https://github.com/user-attachments/assets/4c1e90fe-84ef-4744-9575-3eddf5cef086)
## step 4 : masukkan nama file
![WhatsApp Image 2025-09-22 at 14 41 31](https://github.com/user-attachments/assets/c58cbb6a-f69f-4de4-9cc1-e31c280ce0ca)
## step 5 : masukkan password 
jika file yang ingin kita integrasikan bersifat rahasia, jika tidak, maka kosongkan saja dengan menekan tombol **enter**
![WhatsApp Image 2025-09-22 at 14 41 32](https://github.com/user-attachments/assets/dda0b7f8-c34f-4e35-9ca4-5c43873d28bc)
## step 6 : verifikasi password 
isi verifikasi password jika file yang ingin di integrasikan memiliki password
![WhatsApp Image 2025-09-22 at 14 41 33](https://github.com/user-attachments/assets/b180d68d-22b2-4530-8ae3-9afa603e9fa7)
## step 7 : buat folder
untuk membuat file, tambahkan text
```
mkdir .ssh
```
![WhatsApp Image 2025-09-22 at 14 41 33 (1)](https://github.com/user-attachments/assets/4706087b-5f7b-4b3e-9744-d277eb3f3504)
## step 8 : buka dokumen di terminal
untuk membuka dokumen di terminal, tambahkan text
```
cd
```
![WhatsApp Image 2025-09-22 at 14 41 34](https://github.com/user-attachments/assets/7c373fe6-8493-4009-ad27-945e8cde7ce1)
## step 9 : lihat list dokumen yang ada
untuk melihat list dokumen yang ada, tambahkan text
```
ls
```
![WhatsApp Image 2025-09-22 at 14 41 36](https://github.com/user-attachments/assets/408bdf5a-55d8-478f-aa95-95bbc6525eda)
## step 10 : pindahkan file ke folder ssh
untuk memindahkan file ke dalam folder ssh, tambahkan text
```
cat .ssh/"nama file"
```
![WhatsApp Image 2025-09-22 at 14 41 37](https://github.com/user-attachments/assets/b8ac8f9d-5dd0-4f5c-8d09-aa7ceea403c0)
## step 11 : copy link yang telah muncul
![WhatsApp Image 2025-09-22 at 14 41 38 (1)](https://github.com/user-attachments/assets/dceefc82-4e75-438f-bd78-8920e8c1dcac)
## step 12 : buka github
untuk membuka website github, bisa menggunakan link
```
https://github.com/.
```
## step 13 : klik ikon profile di pojok kanan atas
![WhatsApp Image 2025-09-22 at 14 41 39](https://github.com/user-attachments/assets/ea70a737-016c-43ac-a1bb-6345cf737588)
## step 14 : klik ikon settings
![WhatsApp Image 2025-09-22 at 14 41 39 (1)](https://github.com/user-attachments/assets/e41e2598-3c9b-41b9-a22e-e713d518a357)
## step 15 : klik ikon ssh and gpg keys yang ada di barisan kanan
![WhatsApp Image 2025-09-22 at 14 41 40](https://github.com/user-attachments/assets/aa363ecb-3d66-458b-8042-e4a7ae827977)
## step 16 : klik ikon new ssh key yang berwarna hijau
![WhatsApp Image 2025-09-22 at 14 41 42](https://github.com/user-attachments/assets/2384afb3-8fa4-48c7-95a3-b0de5ffec2a0)
## step 17 : tambahkan judul pada bagian tittle
![WhatsApp Image 2025-09-22 at 14 41 42 (1)](https://github.com/user-attachments/assets/12743888-7e1b-46e6-9d97-6e21fa803e91)
## step 18 : isi authentication key 
jika file yang ingin kita integrasikan bersifat rahasia
## step 19 : masukkan link yang telah di copy kedalam bagian key
![WhatsApp Image 2025-09-22 at 14 41 43](https://github.com/user-attachments/assets/3b6e6608-ce73-42ac-a937-95ffee29fbb0)
## step 20 : klik ikon add ssh key yang berwarna hijau
![WhatsApp Image 2025-09-22 at 14 41 44](https://github.com/user-attachments/assets/168724d9-0453-4902-8b4d-39d0fc3b5ded)
# maka file telah di integrasikan
![WhatsApp Image 2025-09-22 at 14 41 44 (1)](https://github.com/user-attachments/assets/072177f0-6f96-4f24-b6ab-f3e35c587e96)
