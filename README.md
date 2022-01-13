# Installing and Running the Infrastructure

## Database only

For Java-Backend-Developers start only the PostGreSQL database to develop the Rest Services.

Use 'database_only' folder configuration.

## Rest-Services

For Frontend-Developers start the the PostGreSQL database and the Rest Services to develop the frontend functionality.

Use 'restservice' folder configuration.


### Rest-Service-End-Point Configuration
- **host** : localhost
- **port** : 8080

### Reinitialze Rest-Service

If the Docker image **akros-marketplace-infrastructure_data-service-backend:latest** exists when a container of the image is just started.
The Rest-Service is only build when the Docker image **akros-marketplace-infrastructure_data-service-backend:latest** does not exists.

To force rebuild procede the following steps
- **show images**: docker images
- **remove image**: docker image rm akros-marketplace-infrastructure_data-service-backend:latest

### Start/Stop
- **start**: docker-compose -f docker-compose_rest_service_end_points_and_database.yml up
- **stop**: docker-compose -f docker-compose_rest_service_end_points_and_database.yml down

