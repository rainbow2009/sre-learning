FROM nginx:alpine

# Metadata
LABEL maintainer="rainbow2009"
LABEL version="1.0"


COPY index.html /usr/share/nginx/html/index.html


EXPOSE 80

HEALTHCHECK --interval=30s --timeout=3s \
  CMD wget -q --spider http://localhost/ || exit 1
