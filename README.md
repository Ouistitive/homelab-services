# Homelab services

In this repository, you will find all the services that I run on my Raspberry Pi 5 (8Gb RAM).

I use AdGuard Home as my local DNS to resolve custom domain names to the IP addresses of my local services, and I use Nginx Proxy Manager as a reverse proxy to route HTTPS requests to the correct service based on the domain name.

All the services are on the same network as Nginx Proxy Manager (network name: proxy) so I can avoid exposing ports to the outside for each application.

## Diagram architecture

![Diagram network architecture](https://private-user-images.githubusercontent.com/91791407/590641607-3e49a05e-1b01-479a-a1ba-941c17615a3e.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3ODAwNzE4NzIsIm5iZiI6MTc4MDA3MTU3MiwicGF0aCI6Ii85MTc5MTQwNy81OTA2NDE2MDctM2U0OWEwNWUtMWIwMS00NzlhLWExYmEtOTQxYzE3NjE1YTNlLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA1MjklMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwNTI5VDE2MTkzMlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWYyYmQxYzIyN2E2ZGI1OTE0MTQ5OWRhNjlkZjVjYzQ3ZjlmNjM1ZDM3YzE1ZWQxMjAwYTQwZmYwM2M4YjM4YzEmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRnBuZyJ9.-_rT2D26uqFUvrwmJglBCWrdxhqdZl24lEawyqFgMLU)

## Getting started

1. Install Docker and Docker Compose on your homelab server.
2. Clone this repository.
3. Start AdGuardHome and configure it to add your own DNS in DNS Rewrite.
4. Start Nginx Proxy Manager and configure it.
5. Start all others services and enjoy!

## Notes 

- All services are isolated in the `proxy` network for internal routing.
- You can expand this setup by adding new services on your own.
