ARG NGINX_VERSION=1.17

FROM nginx:${NGINX_VERSION}-alpine AS api_platform_nginx

EXPOSE 80 443

COPY ./api/public /srv/api/public

WORKDIR /srv/api/public

COPY ./api/docker/nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf

CMD ["nginx", "-g", "daemon off;"]






#FROM varnish:${VARNISH_VERSION} AS api_platform_varnish
#
#COPY docker/varnish/conf/default.vcl /etc/varnish/default.vcl
#
#CMD ["varnishd", "-F", "-f", "/etc/varnish/default.vcl", "-p", "http_resp_hdr_len=65536", "-p", "http_resp_size=98304"]
