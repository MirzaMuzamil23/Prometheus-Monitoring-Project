# Docker Monitoring Stack - Prometheus + Grafana + Node Exporter

🚀 A simple and clean Docker Compose based monitoring setup to track your host machine's CPU, memory, disk, and system metrics in real-time.

This project helps you quickly spin up a complete observability stack using **Prometheus**, **Grafana**, and **Node Exporter** — perfect for learning DevOps monitoring or running it on your personal server/home lab.

## Features

- **Node Exporter**: Collects detailed Linux host metrics (CPU, RAM, Disk, Network, etc.)
- **Prometheus**: Scrapes and stores metrics every 15 seconds
- **Grafana**: Beautiful dashboards to visualize all your metrics
- Fully containerized with Docker Compose
- Easy to start, stop, and customize
- Persistent data storage for Prometheus and Grafana

## Project Structure
.
├── docker-compose.yml
├── prometheus.yml
└── README.md


## How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/docker-monitoring-stack.git
   cd docker-monitoring-stack
   docker compose up -d

Access the tools
Grafana: http://localhost:3000
(Default login: admin / 12345 — change this immediately!)
Prometheus: http://localhost:9091
Node Exporter: http://localhost:9100 (metrics only)

## What I Learned

How Prometheus scrapes metrics from exporters
Role of Node Exporter in exposing host-level metrics
Setting up persistent volumes in Docker Compose
Basic Grafana dashboard creation and Prometheus data source configuration
Importance of proper networking and service dependencies in monitoring stacks

## Important Notes

Change the default Grafana password (12345) right after starting the stack for security.
Prometheus is exposed on port 9091 (instead of default 9090) to avoid conflicts.
This setup is ideal for learning and small-scale monitoring. Not recommended for large production environments without further hardening.

## Future Improvements

Add cAdvisor for Docker container metrics
Configure alerting with Alertmanager
Add more pre-built Grafana dashboards
Secure Grafana with proper authentication

Feel free to fork, improve, or use this as a starting point for your own monitoring journey!
Made with ❤️ for learning DevOps and observability.

## Technologies Used

Docker & Docker Compose
Prometheus
Grafana
Node Exporter (Prometheus)
