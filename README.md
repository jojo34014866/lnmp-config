# LNMP 服务器配置

本项目用于管理和备份 LNMP (Linux + Nginx + MySQL + PHP) 服务器的 Nginx 配置文件，方便部署和维护。

## 📌 目录结构
```
etc/
├── nginx.conf                  # Nginx 主配置文件
├── sites-available/            # 可用站点配置
│   ├── default
│   ├── gettop.vip
├── sites-enabled/              # 启用站点配置
│   ├── default
│   ├── gettop.vip
├── snippets/                   # 片段配置（如 FastCGI）
│   ├── fastcgi-php.conf
│   ├── snakeoil.conf
└── 其他配置文件...
```

## 🚀 快速开始

### 1️⃣ 克隆仓库
```bash
git clone git@github.com:jojo34014866/lnmp-config.git
cd lnmp-config
```

### 2️⃣ 备份并替换现有配置
```bash
sudo mv /etc/nginx /etc/nginx.bak
sudo cp -r etc/nginx /etc/
```

### 3️⃣ 测试 Nginx 配置
```bash
sudo nginx -t
```

### 4️⃣ 重启 Nginx 使配置生效
```bash
sudo systemctl restart nginx
```

## ⚡ 证书管理（Let's Encrypt）
如果你使用了 HTTPS 证书，你可以使用以下命令手动更新：
```bash
sudo certbot renew --dry-run
```

## 🛠 贡献指南
1. **Fork** 这个仓库
2. 提交 **Pull Request**
3. 提前测试你的修改

