# Zen Browser – Unofficial apt repository

A signed Debian repository for **Zen Browser**, automatically built daily from the [official build script](https://github.com/sh4r10/zen-browser-debian).  
Install Zen Browser with `apt` and receive automatic updates.

## Adding the repository

Run these commands in a terminal:

```bash
# 1. Import the repository's GPG key
curl -fsSL https://tiagocasalribeiro.github.io/zen-browser-apt/KEY.gpg \
  | sudo tee /etc/apt/trusted.gpg.d/zen-browser.asc

# 2. Add the apt source
echo "deb [arch=amd64 signed-by=/etc/apt/trusted.gpg.d/zen-browser.asc] \
  https://tiagocasalribeiro.github.io/zen-browser-apt stable main" \
  | sudo tee /etc/apt/sources.list.d/zen-browser.list

# 3. Update package lists and install
sudo apt update
sudo apt install zen-browser
