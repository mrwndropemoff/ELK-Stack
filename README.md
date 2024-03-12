# ELK Stack Setup with Docker Compose

This repository contains a Docker Compose setup for deploying an ELK (Elasticsearch, Logstash, Kibana) Stack for log management and analysis.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- **Docker**: Make sure you have Docker installed on your machine. You can download it [here](https://www.docker.com/get-started).
- **Docker Compose**: Ensure you have Docker Compose installed. You can find installation instructions [here](https://docs.docker.com/compose/install/).

## Getting Started

1. Clone this repository to your local machine:

    ```bash
    git clone https://github.com/mrwndropemoff/ELK-Stack.git
    ```

2. Navigate to the project directory:

    ```bash
    cd ELK-Stack
    ```

3. Start the ELK Stack containers using Docker Compose:

    ```bash
    docker-compose up -d
    ```

4. Access Kibana in your web browser:

    Open [http://localhost:5601](http://localhost:5601) in your web browser to access the Kibana dashboard.

## Configuration

- **Elasticsearch**: The Elasticsearch configuration can be found in `./elk-config/elasticsearch/`.
  
- **Logstash**: Logstash configurations are located in `./elk-config/logstash`.

- **Kibana**: Kibana configuration files are available in `./elk-config/kibana`.

- **Filebeat**: Filebeat configuration file is located in `./elk-config/filebeat`.

## Usage

1. Once the ELK Stack is running, you can start sending logs to Elasticsearch using Filebeat (put log in the /logs file).

2. Configure Filebeat to monitor log files or locations according to your requirements. Update `filebeat.yml` accordingly.

3. Run Filebeat:

    ```bash
    docker-compose restart filebeat
    ```

4. Explore, analyze, and visualize your logs using Kibana.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, feel free to open an issue or create a pull request.

