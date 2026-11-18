
# Lightweight Nginx container
# Infrastructure Automation Portfolio

FROM nginx:1.27-alpine

LABEL org.opencontainers.image.title="Infrastructure Automation Demo"
LABEL org.opencontainers.image.description="Sample Nginx container for CI/CD demonstrations"

COPY docker/index.html /usr/share/nginx/html/index.html

EXPOSE 80

HEALTHCHECK --interval=30s --timeout=5s \
  --start-period=10s --retries=3 \
  CMD wget -q -O /dev/null http://127.0.0.1/ || exit 1
