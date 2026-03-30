# Fixes Applied

## Issue 1: Target group unhealthy

### Root cause
Health check path was incorrect (/health did not exist)

### Fix
Updated health check path to: /

---

## Issue 2: Web server not running

### Root cause
Nginx was not installed or stopped on one instance

### Fix
Installed and started nginx:
```bash
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx

---

## Issue 3: Security group blocking traffic

### Root cause
Port 80 (HTTP) was not allowed in the security group, preventing the load balancer from reaching the EC2 instances.

### Fix
Updated the security group inbound rules to allow:
- Port 80 (HTTP)
- Source: 0.0.0.0/0

---

## Issue 4: High CPU usage

### Root cause
A process was consuming CPU resources continuously:
   bash
yes > /dev/null

### Fix
Identified and stopped the process:
   bash
killall yes
