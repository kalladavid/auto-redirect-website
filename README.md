# DevOps Portfolio Project

This is a simple static portfolio website deployed using Docker and NGINX.

## Tech Stack

HTML
Docker
NGINX
GitHub
AWS EC2

## Free Domain Options

### Option 1: Use EC2 Public DNS (Immediate & Free)
Your EC2 instance comes with a free public DNS:
```
http://ec2-XX-XX-XX-XX.compute-1.amazonaws.com
```
Find it in AWS Console → EC2 → Your Instance → Public IPv4 DNS

### Option 2: Freenom Free Domain (.tk, .ml, .ga, .cf, .gq)
1. Visit https://www.freenom.com
2. Search for available domain (e.g., daveedu.tk, daveedu.ml)
3. Register for free (12 months, renewable)
4. Configure DNS A record to point to your EC2 IP

**Note:** Freenom domains may have reliability issues and are not recommended for professional use.

### Option 3: Free Subdomain Services
- **EU.org** - Free .eu.org subdomain (e.g., daveedu.eu.org)
  - Visit: https://nic.eu.org
  - Professional, reliable, permanent
  - Approval takes 1-2 weeks

- **Afraid.org** - Free DNS with subdomains
  - Visit: https://freedns.afraid.org
  - Instant setup, multiple TLD options

### Option 4: GitHub Pages (Alternative Deployment)
Deploy your site to GitHub Pages for free:
```
https://YOUR-USERNAME.github.io/portfolio
```

## Deploy to EC2

### 1. SSH to your EC2 instance
```bash
ssh -i your-key.pem ec2-user@YOUR_EC2_IP
```

### 2. Run Docker Container
```bash
docker-compose up -d
```

### 3. Access Your Site
- Via IP: `http://YOUR_EC2_IP`
- Via EC2 DNS: `http://ec2-XX-XX-XX-XX.compute-1.amazonaws.com`
- Via Custom Domain (after DNS setup): `http://yourdomain.tk`

## Run Locally

docker build -t portfolio-app .
docker run -d -p 8080:80 portfolio-app

Access:
http://localhost:8080
