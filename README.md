# Homelab services

In this repository, you will find all the services that I run on my Raspberry Pi 5 (8Gb RAM).

I use AdGuard Home as my local DNS to resolve custom domain names to the IP addresses of my local services, and I use Nginx Proxy Manager as a reverse proxy to route HTTPS requests to the correct service based on the domain name.

All the services are on the same network as Nginx Proxy Manager (network name: proxy) so I can avoid exposing ports to the outside for each application.

## Diagram architecture

<img width="641" height="691" alt="image" src="https://github.com/user-attachments/assets/f5d8f9cd-9db3-4515-80bc-ce9f8d890364" />

## Getting started

1. Install Docker and Docker Compose on your homelab server.
2. Clone this repository.
3. Start AdGuardHome and configure it to add your own DNS in DNS Rewrite.
4. Start Nginx Proxy Manager and configure it.
5. Start all others services and enjoy!

## Notes 

- All services are isolated in the `proxy` network for internal routing.
- You can expand this setup by adding new services on your own.
