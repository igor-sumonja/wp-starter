# WordPress Docker Xdebug Setup

Welcome to the WordPress Docker Xdebug Setup repository! This project provides a quick and easy way to set up a WordPress development environment with Docker, complete with Xdebug for debugging your PHP code. Ideal for developers looking to streamline their WordPress development workflow, this setup saves time and ensures a consistent environment across multiple machines.

## Features

- **WordPress Latest Version**: Stay up-to-date with the latest WordPress release for your development needs.
- **Docker Compose**: Easy setup and teardown with Docker Compose, making it simple to manage your development environment.
- **Xdebug Integration**: Built-in Xdebug support for in-depth debugging of your WordPress themes and plugins.
- **Customizable**: Easy to customize Docker configurations to suit your project's specific requirements.

## Prerequisites

Before you begin, ensure you have the following installed on your system:
- Docker
- Docker Compose

## Installation

**Clone the Repository**

```bash
   git clone https://github.com/igor-sumonja/wordpress-docker-xdebug.git
```

**Navigate to the Project Directory**

```bash
cd wordpress-docker-xdebug
```

**Start Docker Containers**

Use Docker Compose to build and start the containers:

```bash
docker-compose up -d
```

**Access WordPress**

Once the containers are up and running, access your WordPress site at http://localhost:8000.


## Configuring Xdebug
To configure Xdebug for your development needs, follow these steps:

Update php.ini if needed 
Edit the x-debug.ini file in the `files-to-copy/usr/local/etc/php
/conf.d` directory to adjust Xdebug settings. An example working configuration is provided in the repository.

**Restart Docker Containers**

After making changes, restart your Docker containers to apply the new configuration:
```bash
docker-compose down
docker-compose up -d
```

## Using Xdebug with Your IDE

To integrate Xdebug with your IDE (e.g., VSCode, PHPStorm), refer to your IDE's documentation for setting up PHP debugging with Xdebug. You may need to adjust IDE settings and xdebug.ini to ensure smooth integration.

## Using WP-CLI

To use WP-CLI you need to use command `docker-compose run --rm wp-cli` following the rest of WP-CLI command you want, it is rather long command so you can set up alias on your system like 
```
alias wpc="docker-compose run --rm wp-cli"
```
which would shorten it to simply `wpc`

