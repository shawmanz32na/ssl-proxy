FROM httpd:alpine

WORKDIR /www/

COPY ./conf/extra/dhparams.pem /usr/local/apache2/conf/extra/

COPY ./entrypoint.sh ./

EXPOSE 80 443

# RUN apt-get update && apt-get install apache2-utils openssl -y
# RUN apk --update add bash apache2-utils openssl-dev

ENTRYPOINT /www/entrypoint.sh

# Re-specify the httpd:alpine CMD, since it gets overridden when we specify an entrypoint
CMD ["httpd-foreground"]
