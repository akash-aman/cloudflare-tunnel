# Cloudflare Docker Compose Setup

This repository contains a Docker Compose setup for running a Cloudflare tunnel.

## Services

- `cloudflared`: This service runs the latest version of the `cloudflared` image from Cloudflare. It starts a Cloudflare tunnel with a specified token.

## Usage

1. Set your tunnel token as an environment variable named `TOKEN`. You can do this in your shell:

    ```bash
    export TOKEN=your-token-here
    ```

    Or you can set it in an `.env` file in the same directory as your `docker-compose.yml`:

    ```env
    TOKEN=your-token-here
    ```

2. Run Docker Compose:

    ```bash
    docker-compose up
    ```

This will start the `cloudflared` service and create a Cloudflare tunnel with your specified token. The service will restart automatically unless it is explicitly stopped.