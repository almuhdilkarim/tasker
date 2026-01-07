# Tutorial Integrasi VSCode dengan GitHub di Arch Linux

## Step 1 Masuk ke Dalam Terminal
pertama tama masuk ke dalam terminal 

## Step 2
Buat file ssh dari GitHub dengan menggunakan command

`ssh-keygen -t ed25519 -C "email GitHub"`
 
setelah itu kalian bisa memberinama kepada file tersebut kalian juga bisa menambahkan password jika file itu rahasia


## Step 3 Membuat Folder SSH
Lalu membuat folder untuk menyimpan file ssh dengan command

`mkdir .ssh`

lalu masuk ke document menggunakan command

`cd .ssh` 

kemudian untuk mengetahui file tersebut ada atau tidak, menggunakan command 

`ls`
setelah itu kita bisa pindahkan file dengan comand

`mv "nama file" "nama folder" .ssh/`

## Step 4
setelah itu kita harus mendapatkan link untuk mengitregasiakan vscode dengan git hub dengan comand

`cat .ssh/"nama file yang ada.pub"`

setelah itu copy link yang muncul 

## Step 5 Memasukan link ke SSH Keys
Buka browser dan masuk ke web [github.com] (https://github.com/)
Klik profile lalu masuk ke opsi "settings"

Lalu pilih ke "SSH and GPG keys" di bagian kiri layar tentang "Access"
Pilih ke New SSH key pada bagian kanan layar 


setealh itu isi "Add new SSH Key" dengan masukkan link yang sudah di copy tadi ke opsi "Key"


setelah itu pilih opsi "Add SSH key"


## Step 6 konfigurasi Git
Masuk ke terminal lagi lalu masukkan command 

`git config --global user.email "email git"`

`git config --global user.name "user git"`