# Wireguard + Grafana + Loki + Prometheus
---
> #### **⚠️ Этот playbook предназначен исключительно для образовательных целей и автоматизации настройки Wireguard в рамках легального использования (например, для безопасного удалённого доступа в корпоративных или личных сетях).**
> #### **Автор не призывает к использованию в целях обхода блокировок или нарушению законодательства страны.**
---
> #### **⚠️ This playbook is intended for educational purposes only and for automating the setup of Wireguard for legal use cases (e.g., secure remote access to corporate or personal networks).**
> #### **The author does not encourage or endorse using it to bypass restrictions or violate any applicable laws.**
---
#### Monitoring & Logging Stack with Prometheus, Loki, and Grafana

    This version is not completely secure.

A complete stack for container metrics monitoring and log aggregation based on Docker Compose. 

---
### Stack Components

- **Prometheus** — collects and stores metrics
    
- **Loki** — log aggregation system
    
- **Promtail** — log collector agent
    
- **Grafana** — visualization for metrics and logs
    

---
### Quick Start

1. Clone the repository:
    
    bash
    
    КопироватьРедактировать
    
    `git clone https://github.com/your-user/your-repo.git cd your-repo`
    
2. Start the stack:
    
    bash
    
    КопироватьРедактировать
    
    `docker-compose up -d`
    
3. Open Grafana: [http://localhost:3000](http://localhost:3000)  
    Default login: `admin` / `admin`
    

---
### Configuration

- `docker-compose.yaml` — launches all services
    
- `prometheus.yml` — metrics target configuration
    
- `loki-config.yaml` — log storage configuration
    
- `promtail-config.yaml` — collects logs from containers
    
- `datasources.yaml` — preconfigures Grafana data sources
    

---
### Dashboards

Once running, you can:

- View metrics in Prometheus
    
- Explore logs via Loki
    
- Build dashboards in Grafana
    

---
### Shutdown

bash

КопироватьРедактировать

`docker-compose down`

---
### Notes

- By default, Promtail collects logs from all Docker containers.
    
- Default ports: Grafana `3000`, Prometheus `9090`, Loki `3100`.

---
### Improve
- Reverse Proxy setup (напр., NGINX или Traefik)
