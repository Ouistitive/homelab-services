# Homelab services

In this repository, you will find all the services that I run on my Raspberry Pi 5 (8Gb RAM).

I use AdGuard Home as my local DNS to resolve custom domain names to the IP addresses of my local services, and I use Nginx Proxy Manager as a reverse proxy to route HTTPS requests to the correct service based on the domain name.

All the services are on the same network as Nginx Proxy Manager (network name: proxy) so I can avoid exposing ports to the outside for each application.

## Diagram architecture

![Diagram network architecture](https://private-user-images.githubusercontent.com/91791407/590635393-a067927f-c7b0-49c0-9fbf-12501d4e9319.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Nzg1MjQ5MjcsIm5iZiI6MTc3ODUyNDYyNywicGF0aCI6Ii85MTc5MTQwNy81OTA2MzUzOTMtYTA2NzkyN2YtYzdiMC00OWMwLTlmYmYtMTI1MDFkNGU5MzE5LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA1MTElMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwNTExVDE4MzcwN1omWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTYyZDM5ZmM1NjRiZTRlMzY5YzhhOWFiOTBlMjVmMmJkZWVmMWEwNTY3NTY5MGU0ZjI5Y2M2OGI4Mjc3NjUxMzAmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRnBuZyJ9.kgFXtxAY6Lhq2Hodg_BO-OtjUYwjBXupCWbbsNgug38)

## Getting started

1. Install Docker and Docker Compose on your homelab server.
2. Clone this repository.
3. Start AdGuardHome and configure it to add your own DNS in DNS Rewrite.
4. Start Nginx Proxy Manager and configure it.
5. Start all others services and enjoy!

## Notes 

- All services are isolated in the `proxy` network for internal routing.
- You can expand this setup by adding new services on your own.
