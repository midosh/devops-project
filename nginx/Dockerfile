FROM nginx

RUN mkdir /etc/nginx/private /etc/nginx/certs
COPY static-website/index.html /etc/nginx/html/
COPY static-website/index.css /etc/nginx/html/
COPY static-website/nginx.conf /etc/nginx/nginx.conf

RUN openssl req -x509 -nodes -days 365 \
-subj "/C=US/ST=FL/O=Parlor Design, LLC/CN=nginx.midolab.local" \
-newkey rsa:2048 -keyout /etc/nginx/private/nginx-selfsigned.key \
-out /etc/nginx/certs/nginx-selfsigned.crt;
