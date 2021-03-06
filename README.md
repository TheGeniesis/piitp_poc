# Metric application

![PHP 7.4](https://img.shields.io/badge/PHP-7.4-green)
![SYMFONY 4,4](https://img.shields.io/badge/SYMFONY-4.4-green)

This application was created to show an example integration [Prometheus](http://prometheus.io) with [Symfony](https://symfony.com/) 4 Framework

The Application logic is created to add some scenarios like many database queries, slow endpoints, etc.

The application has 5 endpoints:

| Method | Routing         | Description                |
|--------|-----------------|----------------------------|
| GET    | /example        | Endpoint to count          |
| POST   | /example        | Endpoint to count          |
| GET    | /second/example | Endpoint to count          |
| POST   | /second/example | Endpoint to count          |
| GET    | /slow/example   | Endpoint to count          |
| POST   | /slow/example   | Endpoint to count          |
| PUT    | /slow/example   | Endpoint to count          |
| DELETE | /slow/example   | Endpoint to count          |
| GET    | /metrics        | Get metrics for Prometheus |

## Pre-requirements

- [Docker](https://www.docker.com/)
- [Docker-compose](https://docs.docker.com/compose/)
- [Task](https://taskfile.dev)

> The application wasn't tested on Windows

## Setup

- Run `task init`
- Run `task start`
- [Setup kubernetes environment](devops/README.md)
- Open `http://localhost` to check if it works
- If you get `502 Bad Gateway`, please wait a little longer. The application needs a moment to wake up
- To generate an example traffic use [prepared stress tests project](tests/README.md)
