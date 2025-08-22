
# Nexus CLI Node - Run via UserLAnd (Fully Working Guide)

This guide explains how to run the Nexus CLI Node on an Android device using **UserLAnd** (ARM64 architecture).  
Follow the steps carefully to set up your node successfully.

---

## ✅ Requirements
- Android Device (ARM64)
- UserLAnd App installed
- Stable Internet Connection
- At least **6GB Storage** and **2GB RAM**
- Basic knowledge of Linux commands

---

## ✅ Install Ubuntu in UserLAnd
1. Download **UserLAnd** from Google Play Store.
2. Create a new Ubuntu session and start it.
3. Update your system:
    ```bash
    sudo apt update && sudo apt upgrade -y
    ```

---

## ✅ Install Required Packages
Install essential dependencies:
```bash
sudo apt install -y build-essential curl wget git unzip nano
```

---

## ✅ Install Node.js (LTS)
```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install -y nodejs
node -v
npm -v
```

---

## ✅ Install Latest Go (ARM64)
```bash
wget https://go.dev/dl/go1.23.1.linux-arm64.tar.gz
sudo tar -C /usr/local -xzf go1.23.1.linux-arm64.tar.gz
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
source ~/.bashrc
go version
```

---

## ✅ Install Latest Rust (ARM64)
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
rustc --version
```

---

## ✅ Install Python
```bash
sudo apt install -y python3 python3-pip
python3 --version
pip3 --version
```

---

## ✅ Download Nexus CLI
Run the official script:
```bash
curl https://cli.nexus.xyz/ | sh
```

---

## ✅ Register and Start Node
Register with your wallet:
```bash
nexus-network register-user --wallet-address <your-wallet-address>
nexus-network register-node
```

Start your node with Node ID:
```bash
nexus-network start --node-id <your-node-id>
```

---

## ✅ Join Our Community
📢 **Telegram Channel**: [Crypto Income Free](https://t.me/cryptoincomefree)

---

### ✅ Tips:
- Keep your UserLAnd session running in the background.
- Use `tmux` or `screen` to keep the node alive.

---

## ✅ License
MIT License
