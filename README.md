# Octra-testnet step by step on Windows WSL or Codespase
Join discord Join Discord [Join Discord](https://discord.gg/octra)

Requirements
- Windows: Install Linux Ubuntu using WSL by following this guide from @Oxmoei https://github.com/0xmoei/Install-Linux-on-Windows
- Codespace: Or you can use Github Codespace, create a blank template and run your codes.


Install dependecies :
Install & Update Packages: 
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install screen curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev  -y

Create wallet: 
1. Clone the Repostitory
 ```bash git clone https://github.com/0xmoei/wallet-gen.git cd wallet-gen

2. Run the wallet generator webserver
  ```bash chmod +x ./start.sh ./start.sh

3. Open your browser
   - Navigate to http://localhost:8888 on browser
  
4. . Generate wallet
Click "GENERATE NEW WALLET" and watch the real-time progress
Save all the details of your Wallet

5. Get Faucet
Visit Faucet page
Enter your address starting with oct... to get faucet


      
   
   
