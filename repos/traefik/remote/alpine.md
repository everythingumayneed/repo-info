## `traefik:alpine`

```console
$ docker pull traefik@sha256:95ce155376b02d4c0cda38da1d45ef25146dd38efa015c4feba274bacffeea3c
```

-	Platforms:
	-	linux; amd64

### `traefik:alpine` - linux; amd64

-	Docker Version: 17.03.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15335576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab58e39bdb4ae61ff0a97809ea579546c876e32b31c64000074b8c1960dea5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 27 Jun 2017 18:41:51 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Tue, 27 Jun 2017 18:42:16 GMT
CMD ["/bin/sh"]
# Fri, 08 Sep 2017 22:27:22 GMT
RUN apk --no-cache add ca-certificates
# Fri, 08 Sep 2017 22:28:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	apk add --no-cache --virtual .fetch-deps libressl; 	wget -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.3.8/traefik_linux-$arch"; 	apk del .fetch-deps; 	chmod +x /usr/local/bin/traefik
# Fri, 08 Sep 2017 22:28:07 GMT
COPY file:41f5bd1ea0a61e819b7d8c5489c305d4f2798046917dd6b6695318f555981727 in / 
# Fri, 08 Sep 2017 22:28:07 GMT
EXPOSE 80/tcp
# Fri, 08 Sep 2017 22:28:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Sep 2017 22:28:08 GMT
CMD ["traefik"]
# Fri, 08 Sep 2017 22:28:08 GMT
LABEL org.label-schema.vendor=Containous org.label-schema.url=https://traefik.io org.label-schema.name=Traefik org.label-schema.description=A modern reverse-proxy org.label-schema.version=v1.3.8 org.label-schema.docker.schema-version=1.0
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba34ec7734d5df4b40906b9bce73ea49921678ea9eb9bfbc06bda5e5e2c43ef8`  
		Last Modified: Fri, 08 Sep 2017 22:29:03 GMT  
		Size: 351.3 KB (351289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abaab4123b8e2c27e40a7b1409d79dac369d4f7c2060e521eb0366090c7e661`  
		Last Modified: Fri, 08 Sep 2017 22:30:42 GMT  
		Size: 13.0 MB (12993543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987692e948ff8c9d8684b3773e7dabbc4abf9051b5842411dab03d5e5be735ae`  
		Last Modified: Fri, 08 Sep 2017 22:30:40 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip