# Tutorial Insatal Mongodb
## step 1 update
pastikan sistem di arch linux sudah ter update ke versi terbaru dengan comannd keterminal
`sudo pacman -Syu`


## step 2 mengistall yay
setelah terupdate di arch linux, agar mempermudah kita kita bisa menggunakan yay jika kalian belum mengistal yay kalian dapat menginstal dengan comand
`sudo pakman -S yay`

## step 3 menginstall mongodb
setelah itu karena kita sudah mngistall yay maka kita hanya tinggal mengetik comand
`yay -S mongodb-bin`

## step 4 menjalankan mongodb
Untuk memulai MongoDB, gunakan comand berikut:
`sudo systemctl start mongodb`
setelah itu kalian bisa periksa status mongodb dengan
`sudo systemctl status mongodb`

## step 5 menggunakan mongodb
setelah mongodb berjalan kalian dapat mengguakan dengan comand `mongosh` dan setiap ingin membeuka mongodb kalian bisa mengunakan comand `sudo systemctl start mongodb`
selamat mencoba

