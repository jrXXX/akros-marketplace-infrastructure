## Rest-Services

- This command runs the preconfigured PostgreSQL database as described in the **database_only** section.
- This is primary useful for frontend developers testing the frontend to Rest-Service-End-Point communication.

### Rest-Service-End-Point Configuration
- **host** : localhost
- **port** : 8080

### Swagger End Point
- **End Point** : http://localhost:8080

### Start/Stop
- **start**: docker-compose up
- **stop**: docker-compose down

### Reinitialize Rest-Service

If the Docker image **data-service-backend:latest** exists when a container of the image is just started.
The Rest-Service is only build when the Docker image **data-service-backend:latest** does not exists.

To force rebuild procede the following steps
- **show images**: docker images
- **remove image**: docker image rm data-service-backend:latest

