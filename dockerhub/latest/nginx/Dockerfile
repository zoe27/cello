FROM hyperledger/cello-baseimage:x86_64-latest

COPY nginx/ /tmp/

RUN cp /tmp/nginx.default.conf /etc/nginx/nginx.default.conf

RUN ln -sf /dev/stdout /var/log/nginx/access.log \
	&& ln -sf /dev/stderr /var/log/nginx/error.log

CMD ["/bin/bash", "/tmp/docker-entrypoint.sh"]
