| Nama  | Division        | Sub-Division  |
| ----- | ---------- | ---------- |
| Febri Firmansyah   | ELC | Component Management |

# Cara Menggunakan Git & GitHub

## A. Instalasi dan Konfigurasi Awal
### 1. Instal Git di PC/Laptop
    (https://git-scm.com/downloads)

### 2. Buat akun GitHub
    (https://github.com/join)
### 3. Konfigurasi Git di Git Bash atau Terminal

    git config --global user.name "FEBRIFIRNANSYAH"
    git config --global user.email "febrifirmansyah332@gmail.com"

### 4. Buat SSH Keys di GitHub
### a. Buka GitHub, lalu pergi ke Settings -> SSH and GPG keys -> New SSH Key
### b. Buat SSH key dengan membuka Git Bash dan menjalankan perintah berikut
    ssh-keygen -t ed25519 -C "febrifirmansyah332@gmail.com"
    
### c. Salin SSH key yang telah dibuat dengan perintah berikut
 
    clip.exe < ~/.ssh/id_ed25519.pub
   
### d. Tempelkan (Ctrl+V) key tersebut ke bagian key di setting New SSH Key di GitHub

## B. Membuat Repository
### 1. Buka halaman GitHub
    https://github.com/new
### 2. Masukkan nama repository dan pilih tipe (private atau public), lalu klik create repository
### 3. Buka repository yang telah dibuat
### 4. Klik Code -> SSH -> klik tombol berbentuk 2 kotak untuk menyalin link SSH
### 5. Hubungkan dengan file lokal menggunakan dua cara berikut:
### a. Manual 
### i. Buat folder di File Explorer dengan nama yang sama seperti repository
### ii. Klik kanan dan buka Git Bash
### iii. Masukkan perintah berikut di Git Bash

    git init
    git remote add origin (link SSH yang telah disalin)
    git branch -M main
  
### iv. Sinkronkan folder lokal dengan repository di GitHub
 
    git pull origin (branch yang ingin diunduh)
    
### b. Git Clone
### i. Buka Git Bash di folder parent yang diinginkan dan masukkan perintah berikut

    git clone git@github.com:FEBRIFIRMANSYAH/barunastra.git

### ii. Folder/Repository akan muncul di File Explorer / folder parent yang dipilih
### iii. Buka folder tersebut
### iv. Klik kanan dan buka Git Bash
### v. Masukkan perintah berikut di Git Bash

    git branch -M main


## C. Mengunggah File Lokal ke GitHub
### 1. Isi folder yang telah dibuat dengan file yang diinginkan
### 2. Buka folder lokal yang telah diisi
### 3. Klik kanan dan buka Git Bash
### 4. Masukkan perintah berikut di Git Bash

    git add .
    git commit -m "Test 1"
    git push origin barunastra


## D. Membuat Branch Baru di GitHub
### 1. Branch adalah versi lain dari repository di GitHub, memungkinkan perubahan tanpa mengganggu branch utama
### 2. Buka folder yang terhubung dengan GitHub
### 3. Klik kanan dan buka Git Bash
### 4. Masukkan perintah berikut di Git Bash

    git checkout -b barun

### 5. Pindah ke branch yang telah dibuat dengan perintah berikut

    git checkout barun


## E. Menghapus Branch di GitHub
### 1. Pindah ke branch lain yang tidak akan dihapus dengan perintah berikut
  
    git checkout barun_2

### 2. Hapus branch yang dipilih dengan perintah berikut

    git branch -d barun


## F. Menggabungkan Branch di GitHub
### 1. Pindah ke branch utama yang akan digabungkan dengan perintah berikut
  
    git checkout barun_3
  
### 2. Gabungkan branch dengan perintah berikut
   
    git merge barun_3
  