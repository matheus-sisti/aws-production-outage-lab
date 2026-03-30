#  AWS Production Outage Lab

##  Purpose
This project simulates a real-world cloud support incident involving intermittent downtime in a multi-tier AWS architecture.

---

##  Architecture
- Application Load Balancer (ALB)
- EC2 instances (Auto Scaling)
- RDS database
- CloudWatch monitoring

![Architecture](architecture/architecture-lab-1.drawio.png)

---

##  Issues Simulated
- Broken health check path
- One EC2 instance misconfigured
- Security group blocking HTTP traffic
- High CPU usage causing instability

---

##  Troubleshooting Approach
- Checked ALB target group health
- Tested instances using curl
- Verified nginx service status
- Analyzed CloudWatch metrics

 Full troubleshooting steps: [troubleshooting.md](troubleshooting.md)

---

##  Fixes Applied
- Fixed health check configuration
- Restarted and configured nginx
- Updated security group rules
- Resolved high CPU usage

 Detailed fixes: [fixes.md](fixes.md)

---

##  Scripts
- Nginx setup: scripts/install_nginx.sh
- CPU stress simulation: scripts/stress_cpu.sh

---

##  Skills Demonstrated
- AWS troubleshooting
- Incident analysis
- Root cause identification
- Infrastructure debugging

---

##  Real-world relevance
This lab reflects common production issues handled by Cloud Support Engineers.
