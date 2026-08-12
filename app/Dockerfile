FROM nginx:alpine

# Metadata
LABEL maintainer="rainbow2009"
LABEL version="1.0"

# Копируем страницу
COPY index.html /usr/share/nginx/html/index.html

# Nginx слушает 80
EXPOSE 80

# Healthcheck — CI и K8s используют для проверки
HEALTHCHECK --interval=30s --timeout=3s \
  CMD wget -q --spider http://localhost/ || exit 1