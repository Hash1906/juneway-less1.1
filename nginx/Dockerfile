FROM nginx:1.23.4

COPY ./config/nginx/django.conf /etc/nginx/conf.d/django.conf

CMD ["nginx", "-g", "daemon off;"]
