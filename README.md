## 👋 Welcome to composecraft 🚀

Docker Compose management and visualization tool

## 📋 Description

Docker Compose management and visualization tool

## 🚀 Services

- **app**: composecraft/composecraft:latest

### Infrastructure Components

- **db**: Mongo database


## 📦 Installation

### Option 1: Quick Install
```bash
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/composecraft/main/docker-compose.yaml" -o compose.yml
```

### Option 2: Git Clone
```bash
git clone "https://github.com/composemgr/composecraft" ~/.local/srv/docker/composecraft
cd ~/.local/srv/docker/composecraft
docker compose up -d
```

### Option 3: Using composemgr
```bash
composemgr install composecraft
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
APP_JWT_TOKEN=changeme_secret_key_min_32_chars
DB_ADMIN_PASS=LaV0m2OH4AJNwFJHpCaua1o9tCTktCDS
```

See `docker-compose.yaml` for complete list of configurable options.

## 🌐 Access

- **Web Interface**: http://172.17.0.1:58003

## 📂 Volumes

- `./rootfs/data/db/mongodb/composecraft` - Data storage

## 🔐 Security

- Change all default passwords before deploying to production
- Use strong secrets for all authentication tokens
- Configure HTTPS using a reverse proxy (nginx, traefik, caddy)
- Regularly update Docker images for security patches
- Backup your data regularly

## 🔍 Logging

```shell
docker compose logs -f app
```

## 🛠️ Management

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# Update to latest images
docker compose pull && docker compose up -d

# View logs
docker compose logs -f

# Restart services
docker compose restart
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
