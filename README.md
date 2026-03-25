# Vaultwarden Docker app

Local instance of [Vaultwarden](https://github.com/dani-garcia/vaultwarden), an unofficial Bitwarden compatible server written in Rust.

<https://www.vaultwarden.net/>

## Features

- **Vaultwarden server**: Running securely behind Caddy on <https://localhost:8446>
- **File Attachments**: Enabled by default
- **Persistent Data**: Stored locally in the ./data directory

## Getting Started

### Prerequisites

- Docker and Docker Compose installed on your system.
- Windows (as the provided scripts are .bat files).

### Managing the Server

You can easily manage the server using the provided batch scripts:

- **Start the server**: Run start.bat
- **Stop the server**: Run stop.bat
- **Update Vaultwarden**: Run update to latest version.bat to pull the latest image and recreate the container.

## Configuration Details

- **Caddy Reverse Proxy**: Handles HTTPS locally using a self-signed certificate to ensure secure communication.
- **Port:** HTTPS access is provided on port 8446 (`https://localhost:8446`).
- **Start Script:** The `start.bat` script automatically waits for the service to be ready and launches Chrome while ignoring the self-signed certificate warnings.
- **Volumes:** All user data, databases, attachments, and Caddy configurations are persisted in `./data`.
