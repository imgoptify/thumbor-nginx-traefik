# Thumbor + Nginx + Traefik

All-in-one solution to build your own image optimisation service with Thumbor, Nginx for cache and Traefik for SSL.

So the plan is

- You create or use existing integration with Thumbor API from your application
- Requests from your application come to this API
  - Traefik generate free and automatically renewed SSL ( to make your connection secure)
  - Nginx redirect traffic to Thumbor 
  - Thumbor optimize and convert your image to WebP (if you want)
  - Nginx cache optimised and converted images, so next request for this image will come through Nginx cache and your syetem will get optimised image without optimisation routine for second time.
 
## Getting Started

- Clone repo to your server like `git clone https://github.com/imgoptify/thumbor-nginx-traefik.git`
- Make necessary changes in `.env` file
- Run `docker compose up -d`
