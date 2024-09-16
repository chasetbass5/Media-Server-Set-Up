# Media Server with Docker VPN Setup

This project provides a fully automated media server setup that runs all necessary services through a Docker VPN setup called Gluetun. With a single setup file, you can easily start all services, including Plex, qBittorrent, Sonarr, Radarr, Overseerr, and Prowlarr.

## Features

- **Easy Setup**: Run a single setup file to start all services.
- **VPN Integration**: All services are routed through a secure VPN connection provided by Gluetun.
- **Media Management**: Includes popular tools like Plex for media streaming, qBittorrent for downloading, and Sonarr, Radarr, Overseerr, and Prowlarr for managing and organizing your media library.
- **Dockerized Services**: All components run as Docker containers, making it easy to deploy, manage, and update.

## Requirements

- Docker and Docker Compose installed on your system.
- A VPN provider compatible with Gluetun (e.g., NordVPN, PIA, etc.).
- Basic knowledge of Docker and networking.

## Installation

# 1) Download the `docker-compose.yml` file from the repository to your server:
        curl -O https://raw.githubusercontent.com/your-username/media-server-docker/main/docker-compose.yml

# 2) Open the docker-compose.yml file with a text editor and update the necessary configuration settings for your setup:
        nano docker-compose.yml

- VPN Settings: Update the Gluetun environment variables such as VPN_PROVIDER, VPN_USER, VPN_PASSWORD, and VPN_COUNTRY.
- For more information about all their service providers and ways to use gluetun refer to: https://github.com/qdm12/gluetun
- Service Settings: Customize the settings for Plex, qBittorrent, Sonarr, Radarr, Overseerr, and Prowlarr as needed.
- Update paths to where you will download the media and where you will save it.


# 3) Start the services using Docker Compose:
        docker-compose up -d

## Usage

- **Start the Media Server**: After running the `docker-compose.yaml` file, all services will start automatically.
- **Access the Services**:
  - **Plex**: `http://localhost:32400/web`
  - **qBittorrent**: `http://localhost:8085`
  - **Sonarr**: `http://localhost:8989`
  - **Radarr**: `http://localhost:7878`
  - **Overseerr**: `http://localhost:5055`
  - **Prowlarr**: `http://localhost:9696`

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your improvements.

---

Feel free to modify the content to better fit your project's specifics or add any additional details.
