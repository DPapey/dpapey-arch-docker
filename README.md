# Local SQL Environment with MariaDB and PostgreSQL

This repository contains Docker Compose configurations to quickly spin up scalable and deployable local SQL environments using MariaDB and PostgreSQL, along with their web-based admin tools (phpMyAdmin and pgAdmin).

---

## Features

- MariaDB with persistent data volume
- phpMyAdmin for easy database management
- PostgreSQL with persistent data volume and initialization scripts
- pgAdmin for PostgreSQL management
- Configured to use environment variables for secure credentials
- Restart policies for resilience

---

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/) installed
- [Docker Compose](https://docs.docker.com/compose/install/) installed

---

## Setup

1. Create a `.env` file in the root of the repo with the following variables:

```env
# MariaDB
MYSQL_ROOT_PASSWORD=your_root_password
MYSQL_USER=your_user
MYSQL_PASS=your_password
DB_PORT=port_of_choice

# PostgreSQL
POSTGRES_USER=your_pg_user
POSTGRES_PASSWORD=your_pg_password
PG_PORT=port_of_choice


# phpMyAdmin
PMA_PORT=port_of_choice

# pgAdmin
PGADMIN_EMAIL=your_email@example.com
PGADMIN_PASSWORD=your_pgadmin_password
PGA_PORT=port_of_choice
``` 

> **Important:** Use strong, unique passwords. Do **not** commit your `.env` file to any public repository.

## 2. Run the containers:

```bash
docker-compose up -d 

3. Access the admin tools:

- phpMyAdmin: http://localhost:${PMA_PORT}
- pgAdmin: http://localhost:${PGA_PORT}
```

