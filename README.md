# Kafka Pub/Sub with Python and Docker Compose

This repository demonstrates how to set up a Kafka Pub/Sub system using Docker Compose and Python. It includes Docker Compose configurations for running Kafka and Kafka UI locally, along with Python scripts for a simple publisher and subscriber implementation.

---

## Prerequisites

Before starting, ensure you have the following installed:

1. **Docker**
2. **Docker Compose**
3. **Python** (version 3.7 or higher)
4. **pip** (Python package manager)

---

### 1. Set Up Kafka and Kafka UI Using Docker Compose

Refer to the `docker-compose.yml` file in this repository to run Kafka and Kafka UI locally. 

- Start Kafka and Kafka UI:

```bash
docker-compose up -d
```

- Kafka will be accessible at `localhost:9092`.
- Kafka UI will be accessible at `http://localhost:8080`.

---

### 2. Install Required Python Libraries

Install the `kafka-python` library for interacting with Kafka:

```bash
pip install kafka-python
```

---

### 3. Publisher and Subscriber Scripts

Refer to the `publisher.py` and `subscriber.py` scripts in this repository to implement a simple Pub/Sub system. 

---

### 4. Test the Publisher and Subscriber

1. Run the **subscriber** script to start listening to the topic:
   ```bash
   python subscriber.py
   ```

2. In a separate terminal, run the **publisher** script to send messages:
   ```bash
   python publisher.py
   ```

3. Observe the messages being sent by the publisher and received by the subscriber.

---

### Architecture Diagram

![image](https://github.com/user-attachments/assets/f1b32317-5879-49aa-ad09-bda16fc4d1be)


- **Publisher** sends serialized messages to Kafka topics.
- **Kafka Broker** stores messages in the specified topic (`test-topic`).
- **Subscriber** reads and processes messages from the topic.

---

### Notes

- Use `Kafka UI` at `http://localhost:8080` to monitor topics, messages, and consumer groups.
- Modify the topic name and message format as needed for your use case.
- Use `docker-compose down` to stop and remove containers when done.

---

![kafka_1](https://github.com/user-attachments/assets/469b2bc2-9243-433f-8e0a-3e2a6bc7aad7)
![kafka_2](https://github.com/user-attachments/assets/9b94c85d-3dea-43fb-bfa8-d3601267747b)
![kafka_3](https://github.com/user-attachments/assets/19e8c576-cb47-43a9-9cc9-fedc899f6965)
![kafka_4](https://github.com/user-attachments/assets/bc1c6043-8f46-455c-a329-2f24cc7efe9e)
![kafka_5](https://github.com/user-attachments/assets/1f41af16-5016-4ea3-993e-fd81eeb633eb)
