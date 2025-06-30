markdown

# 🔥 Tutorial Octra Testnet: Bikin Wallet & Kirim Transaksi di Windows/WSL atau Codespaces 🚀

Yo bro, mau ikutan **Octra Testnet** tapi bingung? Tenang, panduan ini bakal bikin lo jadi ninja blockchain dalam hitungan menit! Khusus buat Windows (pake WSL) atau GitHub Codespaces, ga pake ribet VPS. Ikutin langkah ini, dijamin lo ngegas kayak coder Hollywood! 😎

## 📢 Gabung Komunitas Octra
Mampir ke Discord buat nanya-nanya, pamer wallet, atau curhat kalo error:
👉 **[Join Discord](https://discord.gg/octra)**

---

## 🛠 Persiapan: Apa yang Lo Butuhin
Sebelum gas, pastiin lo udah siap:
1. **Windows (pake WSL)**:
   - Pasang Ubuntu di WSL. Cek panduan kece dari bro **[0xmoei](https://github.com/0xmoei/Install-Linux-on-Windows)**.
   - Belum punya WSL? Buka PowerShell (Run as Administrator), ketik:
     ```bash
     wsl --install
     ```
     Tunggu sampe selesai, trus buka terminal Ubuntu (ketik `wsl` di PowerShell).
2. **GitHub Codespaces**:
   - Pengen simpel? Bikin template kosong di [GitHub Codespaces](https://github.com/codespaces), trus jalanin kode di sana. No setup, no drama!

---

## 💸 Langkah 1: Bikin Wallet Octra
Sekarang lo bikin wallet buat flexing di testnet. Semua dependencies dan setup digabung di sini, bro, biar ga ribet. Ikutin langkah ini, jangan lupa backup!

### 1. Pasang Dependencies
Update sistem dan pasang alat-alat tempur biar ga lemot. **Klik ikon copy** di kanan atas kode biar ga kebawa ```bash, njir!

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y screen curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip

Catatan: Internet harus kenceng. Kalo pake WiFi tetangga, mending sembunyi dulu!  Kalo error (misalnya, “Permission denied”), pastiin lo pake sudo.
2. Clone Repository
Ambil kode wallet generator dari 0xmoei:
bash

git clone https://github.com/0xmoei/wallet-gen.git
cd wallet-gen

Cek: Kalo git clone ga jalan, pastiin git udah terinstall:
bash

git --version
sudo apt install -y git

3. Jalanin Webserver Wallet
Kasih izin ke script, trus gas:
bash

chmod +x ./start.sh
./start.sh

Cek: Kalo ./start.sh ga jalan, ketik ls buat pastiin file start.sh ada. Kalo ga ada, cek ulang clone repo-nya.
4. Buka Browser
Buka browser lo (Chrome, Firefox, jangan IE, bro!), trus masuk ke:

http://localhost:8888

Cek: Kalo ga kebuka, pastiin webserver udah jalan (liat output di terminal). Sabun colek dulu kalo error! 
5. Generate Wallet
Di web, klik tombol "GENERATE NEW WALLET".

Pantau progress-nya kayak lagi nonton loading bar game.

PENTING: Simpen detail wallet (private key, address, dll.) di tempat aman. Jangan di Notepad atau status WA, njir! Tulis di kertas atau file terenkripsi.

6. Ambil Faucet
Buka halaman Faucet (cek link di Discord Octra).

Masukin address wallet lo yang mulai dengan oct....

Tunggu token testnet masuk. Kalo lama, ngopi dulu, bro!

 Langkah 2: Kirim Transaksi
Udah punya wallet? Saatnya kirim transaksi biar lo keliatan pro! Ikutin langkah ini:
1. Pasang Python
Install Python dan temen-temennya:
bash

sudo apt install -y python3 python3-pip python3-venv python3-dev

Cek: Kalo error, ulang sudo apt update. Masih error? Tanya di Discord.
2. Install CLI
Ambil kode CLI dari Octra Labs:
bash

git clone https://github.com/octra-labs/octra_pre_client.git
cd octra_pre_client

Setup virtual environment dan install dependensi:
bash

python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

Copy file contoh wallet:
bash

cp wallet.json.example wallet.json

3. Tambah Wallet ke CLI
Edit file wallet.json pake nano:
bash

nano wallet.json

Ganti nilai berikut:
private-key-here: Masukin private key lo dalam format B64.

octxxxxxxxx...: Masukin address Octra lo yang mulai dengan oct....

Simpen file (tekan Ctrl+O, Enter, trus Ctrl+X).
4. Jalanin CLI
Jalanin CLI buat buka Testnet UI:
bash

python3 -m venv venv
source venv/bin/activate
python3 cli.py

Cek: Kalo UI ga muncul, pastiin lo udah di folder octra_pre_client dan virtual environment aktif (liat (venv) di prompt).
5. Kirim Transaksi
Kirim transaksi ke address ini:

octBvPDeFCaAZtfr3SBr7Jn6nnWnUuCfAZfgCmaqswV8YR5

Cari address Octra lain pake Octra Explorer (ganti link kalo punya yang resmi).
6. Pakai Script Alternatif (Opsional)
Kalo script resmi bikin pusing, coba script kece dari 0xmoei:
bash

curl -o cli.py https://raw.githubusercontent.com/0xmoei/octra/refs/heads/main/cli.py

Jalanin ulang CLI:
bash

python3 cli.py

