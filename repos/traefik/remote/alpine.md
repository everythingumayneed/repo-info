## `traefik:alpine`

```console
$ docker pull traefik@sha256:14b4cf8ada48a1eeb5c7024a35766d0c319710625079b90cb91da7a77166d5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `traefik:alpine` - linux; amd64

```console
$ docker pull traefik@sha256:0acd867a486e0589fa6e600db4c0869fecfb9d777db7dc4e7c98098f10e393b4
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15545601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9542d0c874d180048f4da582010e76ded226d1c878d4e77681440560107e6d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2017 19:35:45 GMT
RUN apk --no-cache add ca-certificates
# Mon, 16 Oct 2017 18:48:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	apk add --no-cache --virtual .fetch-deps libressl; 	wget -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.4.0/traefik_linux-$arch"; 	apk del .fetch-deps; 	chmod +x /usr/local/bin/traefik
# Mon, 16 Oct 2017 18:48:47 GMT
COPY file:41f5bd1ea0a61e819b7d8c5489c305d4f2798046917dd6b6695318f555981727 in / 
# Mon, 16 Oct 2017 18:48:47 GMT
EXPOSE 80/tcp
# Mon, 16 Oct 2017 18:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Oct 2017 18:48:47 GMT
CMD ["traefik"]
# Mon, 16 Oct 2017 18:48:47 GMT
LABEL org.label-schema.vendor=Containous org.label-schema.url=https://traefik.io org.label-schema.name=Traefik org.label-schema.description=A modern reverse-proxy org.label-schema.version=v1.4.0 org.label-schema.docker.schema-version=1.0
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690da7be984deafe90a6af23d8afd106994491a9c83c7914b48b31d056b063ca`  
		Last Modified: Mon, 18 Sep 2017 19:37:01 GMT  
		Size: 351.4 KB (351350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd0fb074fafa62a96dbc669ef41607a47945b5f01f18e52c5bb32d2c36812f2`  
		Last Modified: Mon, 16 Oct 2017 18:49:57 GMT  
		Size: 13.2 MB (13203510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee8516667533c370cacd2074f3b1725a991f47c37b7c8a086a0e33f9662faa1`  
		Last Modified: Mon, 16 Oct 2017 18:49:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
