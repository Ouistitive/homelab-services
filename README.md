# Homelab services

In this repository, you will find all the services that I run on my Raspberry Pi 5 (8Gb RAM).

I use AdGuard Home as my local DNS to resolve custom domain names to the IP addresses of my local services, and I use Nginx Proxy Manager as a reverse proxy to route HTTPS requests to the correct service based on the domain name.

All the services are on the same network as Nginx Proxy Manager (network name: proxy) so I can avoid exposing ports to the outside for each application.

## Diagram architecture

![Diagram network architecture]([https://private-user-images.githubusercontent.com/91791407/590641607-3e49a05e-1b01-479a-a1ba-941c17615a3e.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Nzg1MjU0MzEsIm5iZiI6MTc3ODUyNTEzMSwicGF0aCI6Ii85MTc5MTQwNy81OTA2NDE2MDctM2U0OWEwNWUtMWIwMS00NzlhLWExYmEtOTQxYzE3NjE1YTNlLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA1MTElMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwNTExVDE4NDUzMVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWE4Y2I4N2I0ZjJjODQyMzk3OTUxZDY1NGM3OTFmNGFmOGEzODQ4NjE3NGRjNGVkOGE0ODVmMDU5MzBhN2Y3YjgmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRnBuZyJ9.UAwsP7vVQY2Mpeuw2Ld2TJeYokDxpQNuRSDZytBdzy4](https://private-user-images.githubusercontent.com/91791407/590641607-3e49a05e-1b01-479a-a1ba-941c17615a3e.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Nzk3MDg3MDMsIm5iZiI6MTc3OTcwODQwMywicGF0aCI6Ii85MTc5MTQwNy81OTA2NDE2MDctM2U0OWEwNWUtMWIwMS00NzlhLWExYmEtOTQxYzE3NjE1YTNlLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA1MjUlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwNTI1VDExMjY0M1omWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWRhODgzNzY2OTA0NzUzOWZjOTFmMDZhODZmZTk4N2FlM2Q3ZDdiMDdiNDQ4M2RhMWEzZGE4NWYxMDA0YjQ0MjQmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRnBuZyJ9.6LN-PkDeunsi6uOG24thy1rFA8plmWsNdwvtxc5IhkQ))

## Getting started

1. Install Docker and Docker Compose on your homelab server.
2. Clone this repository.
3. Start AdGuardHome and configure it to add your own DNS in DNS Rewrite.
4. Start Nginx Proxy Manager and configure it.
5. Start all others services and enjoy!

## Notes 

- All services are isolated in the `proxy` network for internal routing.
- You can expand this setup by adding new services on your own.
