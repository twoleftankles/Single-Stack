# Single-Stack
Traefik | Authentik | Crowdsec | Netbird

The Traefik/Authentik/Crowdsec should be configured first.
Traefik config includes cloudflare plugin for real IP and crowdsec bouncer so you can proxy DNS through cloudflare with with correct client IP in logs.

Before proceeding with Netbird, make sure to have provider/application with proper config created in authentik.

Netbird folder contains modified docker-compose.yml, management.json, setup.env(Original template included), and configure.sh file to only expose netbird on port 443 for TCP traffic (Including relay service). All other UDP traffic will still need to be available externally.
