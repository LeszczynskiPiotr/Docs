## Linux setup running for running kafka inside docker

###Install docker

```bash
apt update && apt upgrade -y
apt install -y ca-certificates curl gnupg
install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | gpg --dearmor -o /etc/apt/keyrings/docker.gpg
chmod a+r /etc/apt/keyrings/docker.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
```

`apt update`

`apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`

```bash
mkdir -p /opt/kafka
cd /opt/kafka
```

## Setup docker compose

`nano docker-compose.yml`

#### Paste the content from the docker compose

`docker compose up -d`
