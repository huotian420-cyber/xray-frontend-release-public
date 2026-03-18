# Xray Frontend Release Package

This repository hosts the public release archive for the frontend-enabled Xray panel package.

## Ubuntu Download

```bash
wget -O xray-backend-release.tar.gz https://github.com/huotian420-cyber/xray-frontend-release-public/raw/main/xray-backend-release.tar.gz
wget -O SHA256SUMS.txt https://raw.githubusercontent.com/huotian420-cyber/xray-frontend-release-public/main/SHA256SUMS.txt
sha256sum -c SHA256SUMS.txt --ignore-missing
mkdir -p xray-backend
tar -xzf xray-backend-release.tar.gz -C xray-backend
cd xray-backend
sudo bash install.sh
```

## Files

- `xray-backend-release.tar.gz`: frontend-enabled deployment package
- `SHA256SUMS.txt`: SHA256 checksums for the package
