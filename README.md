# Installing and Running Infrastructure

## Database only : docker-compose_database_only.yml

- This command runs a preconfigured PostgreSQL database.
- This is primary used for backend developers using a database to test there Rest-Service.

### Database Configuration
- **user** : am
- **passsword** : am
- **database_name** : am
- **host** : localhost
- **port** : 5432

### PostgreSQL Data Files / Reinitialize Database

The data files are stored in sub directory ./pg_data. This directory is once created on first run and installs the required tables, views and initializes the data.

To rebuild the database, shut the database down and delete the ./pg_data directory. On next start the database will be reinitialized again.

### Start/Stop
- **start**: docker-compose -f docker-compose_database_only.yml up
- **stop**: docker-compose -f docker-compose_database_only.yml down




## Rest-Services : docker-compose_rest_service_end_points_and_database.yml

- This command runs the preconfigured PostgreSQL database described in previous section.
- This is primary used for frontend developers testing frontend to Rest-Service-End-Point communication.

### Rest-Service-End-Point Configuration
- **host** : localhost
- **port** : 8080

### Reinitialze Rest-Service

If the Docker image **akros-marketplace-infrastructure_data-service-backend:latest** exists when a container of the image is just started.
The Rest-Service is only build when the Docker image **akros-marketplace-infrastructure_data-service-backend:latest** does not exists.

To force rebuild procede the following steps
- **show images**: docker images
- **remove image**: docker image rm akros-marketplace-infrastructure_data-service-backend:latest

## Start/Stop
- **start**: docker-compose -f docker-compose_rest_service_end_points_and_database.yml up
- **stop**: docker-compose -f docker-compose_rest_service_end_points_and_database.yml down

