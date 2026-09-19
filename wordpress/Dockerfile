FROM wordpress:7.1-fpm-alpine@sha256:c3d995d24a9ba8e8e271c00d108057d1af2b7d04ce98314391d28512f4cbdfce

WORKDIR /var/www/html/

RUN apk update && \
    apk add zip curl --no-cache

RUN curl -o wpgraphql.zip -fL https://downloads.wordpress.org/plugin/wp-graphql.1.13.7.zip && \
    unzip -q wpgraphql.zip -d wp-content/plugins/ && \
    rm wpgraphql.zip

COPY themes wp-content/themes