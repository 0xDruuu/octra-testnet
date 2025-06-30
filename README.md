# 🔥 Tutorial Octra Testnet: Jadi Ninja Blockchain di Windows/WSL/Codespaces 🚀

Selamat datang di panduan paling asik buat setup **Octra Testnet**! Ikutin langkah ini, dijamin lo bakal jago ngerjain testnet, entah pake WSL di Windows atau Codespaces. Siap? Gaskeun, bro! 😎

## 📢 Join Komunitas Dulu, Bro!
Mampir ke Discord Octra biar ga ketinggalan update dan bisa nanya-nanya:
👉 **[Join Discord](https://discord.gg/octra)**

---

## 🛠 Persiapan: Apa yang Lo Butuhin
- **Windows (pake WSL)**:
  - Pasang Ubuntu di WSL. Ikutin panduan kece dari bro **[0xmoei](https://github.com/0xmoei/Install-Linux-on-Windows)**.
  - Ga punya WSL? Buka PowerShell, ketik:
    ```bash
    wsl --install
    ```
    Tunggu sampe selesai, trus buka terminal Ubuntu.
- **GitHub Codespaces**:
  - Males setup lokal? Bikin template kosong di [GitHub Codespaces](https://github.com/codespaces) dan jalanin kode di sana. Tinggal gas!

---

## 🚀 Langkah 1: Pasang Dependencies, Biar Sistem Lo Gahar
Pertama, update sistem dan pasang alat-alat tempur biar ga lemot kayak keong. Klik ikon **copy** di kanan atas kode biar ga kebawa ```bash, njir!

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y screen curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev
