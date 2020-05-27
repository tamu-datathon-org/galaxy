FROM nginx:1.18.0
COPY routes.conf /etc/nginx/conf.d/default.conf.template
ARG GATEKEEPER_URL
CMD /bin/bash -c "envsubst '\$PORT,\$GATEKEEPER_URL' < /etc/nginx/conf.d/default.conf.template > /etc/nginx/conf.d/default.conf" && nginx -g 'daemon off;'