## install docker dan docker compose
```
sudo pacman -S docker docker-compose
```

## cloning docker images untuk eprints
``
git clone https://github.com/DTLudlow/eprints-3.4.4-docker.git`
``

## masuk ke direktori docker
```
cd eprints-3.4.4-docker-main
```

## membuat docker container
```
sudo docker compose up --build -d
```

## memberi akses file penuh ke user eprints
```
chown -R -c eprints:eprints /usr/share/eprints/
```

## masuk ke user eprints
```
su eprints
```

## pastikan tidak ada link yang berantakan
```
/usr/share/eprints/bin/generate_static pub
```

## memastikan user admin sudah ditambahkan ke database
```
/usr/share/eprints/bin/epadmin update pub
```

## memastikan konfigurasi arsip
```
/usr/share/eprints/bin/epadmin reload pub
```

## kembali ke user root
```
exit
```

## restart webserver
```
httpd -k restart
```

## jalankan eprints
masuk ke docker images eprints lalu jalankan
```
docker compose up -d
```

## masuk ke eprints
```
http://localhost
```
## tampilan
![tampilan eprints](tampilan.png)
