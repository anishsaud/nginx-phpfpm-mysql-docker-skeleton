FROM nginx:alpine

### IF SSL is needed
# RUN apk upgrade --update-cache --available && \
#     apk add openssl && \
#     rm -rf /var/cache/apk/*

# RUN openssl req -x509 -nodes -days 365 \
#     -newkey rsa:2048 \
#     -out /etc/ssl/certs/localhost.crt \
#     -keyout /etc/ssl/private/localhost.key \
#     -subj "/CN=localhost" \
#     -addext "subjectAltName=DNS:localhost" \
#     -addext "keyUsage=digitalSignature" ;


# Entry point
ENTRYPOINT ["/usr/sbin/nginx", "-g", "daemon off;"]

