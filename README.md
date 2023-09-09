# isec6000-assignment1-task2
This repository contains the development and running of the Saleor application as a part of the ISEC6000 Secure DevOps assignment.

### What is Saleor Platform?

Saleor Platform is the easiest way to start local development with all the major Saleor services:

## Requirements
1. [Docker](https://docs.docker.com/install/)

## How to clone the repository?

To clone the repository, run the following command

```
git clone https://github.com/dahalapaar/isec6000-assignment1-task2.git
```

## How to run it?

1. Go to the cloned directory:
```shell
cd saleor-platform
```

3. Build the application:
```shell
docker compose build
```

4. Apply Django migrations:
```shell
docker compose run --rm api python3 manage.py migrate
```

5. Populate the database with example data and create the admin user:
```shell
docker compose run --rm api python3 manage.py populatedb --createsuperuser
```
*Note that `--createsuperuser` argument creates an admin account for `admin@example.com` with the password set to `admin`.*

6. Run the application:
```shell
docker compose up
```

## Where is the application running?
- Saleor Dashboard - http://localhost:9003
