# integrasi akun github dan vscode

## buat ssh key
langkah pertama adalah membuat key github [keygithub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)


## buat folder untuk generate key

```
mkdir .ssh
```

```
cd .ssh
```

lalu masukkan code di bawah ke dalam folder .ssh

```
ssh-keygen -t ed25519 -C "your_email@example.com"
```

## membaca isi file

```
cat id_ed25519.pub
```

lalu salin isi file ke dalam github

## generate key to github
buka settings, lalu pilih gpg and ssh key, add new ssh


## integrasi github ke vscode
pilih repo pada github
lalu klik tombol code
salin link ssh

## cloning repository
```
git clone (link codenya)
```
