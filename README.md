# RR-Team-46-distributed-logging-system
# **Distributed Monitoring and Microservices Framework**

This project is a distributed system framework designed to monitor and manage services efficiently. It uses **Kafka**, **Fluentd**, **Elasticsearch**, and **Kibana** for data streaming, logging, storage, and visualization. All components are containerized using Docker to ensure seamless deployment and scalability.

---

## **Features**
- **Kafka**: For real-time log and event streaming between components.
- **Fluentd**: To aggregate and forward logs from various services to Elasticsearch.
- **Elasticsearch & Kibana**: For log storage, searching, and visualization.
- **Microservices**: Includes sample services for inventory, order, and payment management.
- **Monitoring**: Tracks heartbeat and logs to detect anomalies and trigger alerts.

---

## **Requirements**
- Docker and Docker Compose installed on your system.
- Python 3.10 or later (for development purposes).

---

## **Setup and Usage**

### **1. Install Dependencies**
Install Python dependencies if needed (for local testing):  
```bash
pip install -r requirements.txt
```

### **2. Start Docker Containers**
Use the provided `docker-compose.yml` file to start all services:  
```bash
docker-compose up -d
```

This will set up:
- **Kafka**
- **Fluentd**
- **Elasticsearch**
- **Kibana**

---

### **3. Run Monitoring System**
Run the monitoring system to handle heartbeat checks and log accumulation:  
```bash
python run_monitoring.py
```

---

### **4. Run a Microservice**
Start a specific microservice by passing its name:  
```bash
python run_service.py <service_name>
```

Replace `<service_name>` with the name of the service you want to run, such as:
- `inventory_service`
- `order_service`
- `payment_service`

---

## **File Structure**
```
├── README.md                  # Documentation
├── config/                    # Configuration for Kafka and Elasticsearch
├── core/                      # Core logic for alerting, monitoring, and log storage
├── microservices/             # Microservices: Inventory, Order, Payment
├── fluentd/                   # Fluentd configuration and Dockerfile
├── docker-compose.yml         # Orchestrates services in Docker
├── requirements.txt           # Python dependencies
├── run_monitoring.py          # Starts the monitoring system
├── run_service.py             # Starts a specific microservice
├── utils/                     # Utility scripts (e.g., logger)
```

---

## **Visualization**
- Access **Kibana** to visualize logs and system metrics:  
  Open [http://localhost:5601](http://localhost:5601) in your browser.

---

## **Extending the System**
To add a new service:
1. Create a new file in the `microservices` directory (e.g., `new_service.py`).
2. Implement the logic using the provided `base_service.py` as a template.
3. Run the new service with:  
   ```bash
   python run_service.py new_service
   ```

---

## **Troubleshooting**
- Ensure all Docker containers are running:  
  ```bash
  docker ps
  ```
- Check logs for errors using Docker or Kibana.

---

## **Contributors**
- **Aniruddh Suresh Guttikar**: PES1UG22CS089
- **Arunkumar R**: PES1UG22CS108
- **Amruth R**: PES1UG22CS078
- **Aditya P**: PES1UG22CS040

---

## **License**
This project is licensed under the MIT License.
