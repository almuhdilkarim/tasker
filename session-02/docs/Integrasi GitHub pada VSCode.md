# Integrasi GitHub dengan Visual Studio Code

## Prasyarat
Akun GitHub · VS Code · Git  
Cek Git: `git --version`

## Konfigurasi Git (sekali)
`git config --global user.name "NamaKamu"`  
`git config --global user.email "emailkamu@gmail.com"`

## Login GitHub di VS Code
Accounts (👤) → Sign in with GitHub → Authorize di browser

## Clone Repository
VS Code: Ctrl+Shift+P → Git: Clone → paste URL repo → pilih folder  
Terminal: `git clone https://github.com/username/nama-repo.git`

## Workflow Harian
`git add .` → `git commit -m "pesan commit"` → `git push origin main`

## Ambil Update
`git pull origin main`

## Branch (opsional)
`git checkout -b nama-branch` → `git push origin nama-branch`

## Catatan
Jangan clone di dalam repo · Jangan upload folder `.git` · Pakai `.gitignore`

**Alur:** Edit → Commit → Push
