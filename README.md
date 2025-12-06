# CodeAssist
# Installation

## 1. Docker

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
## 2. Python

```bash
sudo apt install python3 python3-pip python3-venv python3-dev -y
```

## 3. UV

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
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
