# Evenmate

An event planner app for **Software Engineering and Information Technologies** course at **Faculty of Technical Sciences**, Novi Sad, Serbia, 2024.

## Requirements

- [Docker](https://docs.docker.com/engine/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## How to run

Rename, or create a copy of **.env.example** called **.env**

- `docker compose up -d` to start all containers
- `docker compose down` to remove all containers
  - use the `-v` flag to remove the volumes(data) as well

## Routes

- **Frontend** at **http://localhost:4200**
- **Backend** at **http://localhost:8080**
- **pgAdmin** at **http://localhost:5050**
