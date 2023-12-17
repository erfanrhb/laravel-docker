

---

# Laravel Docker Compose Configuration

This repository contains a Docker Compose configuration for setting up a Laravel development environment with MySQL, Nginx, PHPMyAdmin using Docker containers.

## Getting Started

To get started with this setup, ensure that you have Docker and Docker Compose installed on your machine.

### Prerequisites

- Docker installed on your system ([Get Docker](https://docs.docker.com/get-docker/))
- Docker Compose installed on your system ([Install Docker Compose](https://docs.docker.com/compose/install/))

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/erfanrhb/laravel-docker.git
   ```

2. Navigate to the cloned repository:
   ```bash
   cd laravel-docker
   ```

3. Create a `.env` file based on the provided `.env.example` and configure necessary environment variables.
   ```bash
   cp .env.example .env
   ```

4. Start the Docker containers:
   ```bash
   docker-compose up -d --build
   ```

5. Access your Laravel application at [http://localhost:8005](http://localhost:8005)
    - PHPMyAdmin can be accessed at [http://localhost:8085](http://localhost:8085)

### Docker Compose Services

- **walletnginx**: Nginx service configured for the Laravel application.
- **walletweb**: PHP service running Laravel application.
- **walletdb**: MySQL service for the database.
- **walletphpmyadmin**: PHPMyAdmin service for managing the MySQL database.

### Custom Configurations

- **Nginx Configuration**: Check `.docker/nginx/default.conf` for the Nginx server configuration.
- **PHP Configuration**: PHP configuration is defined in `.docker/php/Dockerfile`.

## Configuration Details

### Docker Compose

The `docker-compose.yml` file contains the configuration for all services required for this setup.

```yaml
# docker-compose.yml
version: "3.7"

services:
  walletnginx:
    # ... (Nginx service configuration)

  walletweb:
    # ... (PHP service configuration)

  walletdb:
    # ... (MySQL service configuration)

  walletphpmyadmin:
    # ... (PHPMyAdmin service configuration)
```

### Nginx Configuration

The Nginx server configuration is located at `.docker/nginx/default.conf`.

```nginx
# .docker/nginx/default.conf
# ... (Nginx server configuration details)
```

### PHP Configuration

The PHP configuration is defined in `.docker/php/Dockerfile`.

```Dockerfile
# .docker/php/Dockerfile
# ... (PHP Dockerfile configuration details)
```

## Notes

- Ensure proper configuration of environment variables in `.env` for your Laravel application.
- Adjust PHP and Nginx configurations as needed for your specific requirements.

## Contributing

Feel free to contribute to this repository by opening issues or pull requests.

## License

This project is licensed under the [MIT License](LICENSE).

---

Feel free to adjust the content based on your specific project details and requirements. If you need further clarifications or additions, feel free to ask!
