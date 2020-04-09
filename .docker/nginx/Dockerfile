FROM nginx:1.15.0-alpine

ENV DOCKERIZE_VERSION v0.6.1
RUN wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /usr/local/bin -xzvf dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && rm dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz

#remover o arquivo de configuração padrão do nginx o index.html
RUN rm /etc/nginx/conf.d/default.conf

#Copiar os arquivos de configuração criado por nos em outro arquivo.
COPY ./nginx.conf /etc/nginx/conf.d