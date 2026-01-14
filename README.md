# Postgres with pgvector (Docker)

This repository provides a Docker Compose configuration to run a stock PostgreSQL instance with the `pgvector` extension pre-installed.

It is specifically designed to provide a vector database backend for the [post-pgvector-mcp](https://github.com/design-rules/post-pgvector-mcp) server (or any other application requiring pgvector).

## Connection Details

*   **Host:** `localhost`
*   **Port:** `5432`
*   **Username:** `postgres`
*   **Password:** `password`
*   **Database:** `postgres`

## Quick Start

1.  **Start the container:**
    ```bash
    docker compose up -d
    ```

2.  **Verify status:**
    ```bash
    docker ps
    ```

3.  **Stop the container:**
    ```bash
    docker compose down
    ```

## Features

*   **Base Image:** Uses the official `pgvector/pgvector:pg16` image.
*   **Persistence:** Data is persisted in a Docker volume named `pgdata`.
*   **Auto-Restart:** Configured to always restart unless stopped manually.
