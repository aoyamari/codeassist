# CodeAssist

• System Requirements
• 12 GB RAM minimum (32 GB recommended)
• Stable internet connection
• At least 10 GB of available storage (for overhead)
• Modern multi-core CPU (Intel, AMD, or Apple Silicon)

# Installation

## 1. Update System
```bash
sudo apt update && sudo apt upgrade -y
```

## 2. Install General Utilities and Tools
```bash
sudo apt install screen curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev  -y
```

## 3. Docker

```bash
sudo apt update -y && sudo apt upgrade -y
```

```bash
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove -y $pkg; done
```

```bash
sudo apt-get update
```

```bash
sudo apt-get install ca-certificates curl gnupg
```

```bash
sudo install -m 0755 -d /etc/apt/keyrings
```

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

``` bash
sudo chmod a+r /etc/apt/keyrings/docker.gpg
```

```bash
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```bash
sudo apt update -y && sudo apt upgrade -y
```

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

Then Enter `Y`

#### Test Docker
```bash
sudo docker run hello-world
```
## 4. Python

```bash
sudo apt install python3 python3-pip python3-venv python3-dev -y
```

## 5. UV

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

```bash
source $HOME/.local/bin/env
```

# Download CodeAssist

```bash
git clone https://github.com/gensyn-ai/codeassist.git
```

# Running

```bash
cd codeassist
```

```bash
uv run run.py
```

# Get HuggingFace Access token

1- Create account in [HuggingFace](https://huggingface.co/)

2- Create an Access Token with `Write` permissions [here](https://huggingface.co/settings/tokens) and save it

# Access CodeAssist Web UI

I have 3 ways to do this 

### 1. Ngrok

> Install Ngrok

```bash
wget https://bin.equinox.io/c/bNyj1mQVY4c/ngrok-v3-stable-linux-amd64.tgz && tar -xvzf ngrok-v3-stable-linux-amd64.tgz && sudo mv ngrok /usr/local/bin/
```

- Regist [ngrok](ngrok.com)
- Get your Authtoken [here](https://dashboard.ngrok.com/get-started/your-authtoken)
- Paste on your terminal

> Get URL

```bash
ngrok http 3000
```

### 2. Localtunnel

> Install Localtunnel

```bash
sudo npm install -g localtunnel
```
> Get Password

```bash
curl https://loca.lt/mytunnelpassword
```

The password is actually your VPS IP

> Get URL

```bash
lt --port 3000
```

### 3. CloudFlare

> Install CloudFlare

```bash
curl -fsSL https://pkg.cloudflare.com/cloudflare-main.gpg | sudo gpg --dearmor -o /usr/share/keyrings/cloudflare-main.gpg
```

```bash
echo "deb [signed-by=/usr/share/keyrings/cloudflare-main.gpg] https://pkg.cloudflare.com/ $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/cloudflare.list
```

```bash
sudo apt update
```

```bash
sudo apt install cloudflared
```

> Get URL

```bash
cloudflared tunnel --url http://localhost:3000
```

# Last
After solved the codeassist problem, `CTRL+C` your log and wait the training done
🙏🙏🙏
