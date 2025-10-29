# Manual AWS EC2 Deployment Project

A simple project demonstrating the manual deployment of a web application on an AWS EC2 instance using Nginx. This project serves as a practical guide for deploying static web content using AWS infrastructure.

## 📋 Project Overview

This project consists of a web application built with:
- HTML (19.9%)
- CSS (70.4%)
- JavaScript (9.7%)

The application is configured to be deployed on an AWS EC2 instance using Nginx as the web server.

## 🚀 Features

- Step-by-step demonstration of manual EC2 deployment
- Nginx server configuration
- Static web application showcase
- AWS infrastructure setup guidelines

## 🛠️ Prerequisites

Before you begin, ensure you have:
- An AWS account
- Basic understanding of AWS EC2
- Familiarity with Nginx
- Basic knowledge of HTML, CSS, and JavaScript

## 📦 Installation & Deployment Steps

1. **AWS EC2 Setup**
   ```bash
   # Clone this repository
   git clone https://github.com/Bunny0311/manual-aws-ec2-deployment-
   ```

2. **Launch EC2 Instance**
   - Launch an EC2 instance in your AWS Console
   - Choose an appropriate AMI (e.g., Amazon Linux 2 or Ubuntu)
   - Configure security groups to allow HTTP (port 80) and SSH (port 22)

3. **Install Nginx**
   ```bash
   # For Ubuntu
   sudo apt update
   sudo apt install nginx

   # For Amazon Linux
   sudo amazon-linux-extras install nginx1
   ```

4. **Deploy Application**
   - Copy the web application files to your EC2 instance
   - Configure Nginx to serve your application

## ⚙️ Configuration

### Nginx Configuration Example
```nginx
server {
    listen 80;
    server_name your_domain.com;

    root /path/to/your/application;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}
```

## 🔒 Security Considerations

- Keep your EC2 instance updated
- Use secure SSH keys for instance access
- Configure AWS security groups properly
- Implement HTTPS using SSL/TLS certificates

## 🚦 Usage

1. Access your application through your EC2 instance's public IP or domain
2. Navigate through the web interface
3. Monitor server logs for any issues:
   ```bash
   sudo tail -f /var/log/nginx/error.log
   ```

## 👥 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 📧 Contact

- GitHub: [@Bunny0311](https://github.com/Bunny0311)

## 🙏 Acknowledgments

- AWS Documentation
- Nginx Documentation
- The web development community
