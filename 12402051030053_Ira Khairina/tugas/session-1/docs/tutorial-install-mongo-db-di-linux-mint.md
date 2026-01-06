# Tutorial Menginstal MongoDB di Linux Mint
## Step 1: Buka Situs MongoDB
Buka situs [MongoDB](www.mongodb.com) di Firefox. 
## Step 2: Navigasi ke Dokumentasi Server MongoDB
Kemudian klik "Resources", pilih "Server Documentation", lanjutkan ke "MongoDB Community", dan klik "Install on Linux". 
<img width="546" height="417" alt="Screenshot from 2025-09-22 13-03-39" src="https://github.com/user-attachments/assets/a090a978-ecf0-4568-9fc2-8c2552bb5437" />
<img width="860" height="589" alt="Screenshot from 2025-09-22 13-05-07" src="https://github.com/user-attachments/assets/2f5ad684-6cc2-40e8-8975-1b6b2b7ee4cb" />

## Step 3: Import Public Key dan Public GPG Key pada Terminal Linux Mint
Karena menggunakan Linux Mint, pilih opsi "Install on Ubuntu" karena paling mendekati. Copy import the public key gnupg dan curl; `sudo apt-get install gnupg curl` dan `curl -fsSL https://www.mongodb.org/static/pgp/server-8.0.asc |    sudo gpg -o /usr/share/keyrings/mongodb-server-8.0.gpg    --dearmor`, lalu paste di terminal dan tekan Enter. 
<img width="829" height="316" alt="Screenshot from 2025-09-22 13-06-53" src="https://github.com/user-attachments/assets/ccd0c610-d6fb-4317-995d-3875fe0cc9bd" />

## Step 4: Mengupdate Repository dan Menginstall MongoDB
Setelah itu, copy `sudo apt-get update`, paste di dalam terminal, dan tekan Enter. Lakukan hal yang sama dengan `sudo apt-get install -y mongodb-org`, lalu tekan Enter. Dengan begitu, proses pengunduhan MongoDB selesai.
<img width="794" height="437" alt="Screenshot from 2025-09-22 12-44-58" src="https://github.com/user-attachments/assets/10883f1e-6907-44fc-b481-c85059fe56f0" />
