<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `zookeeper`

-	[`zookeeper:3.3`](#zookeeper33)
-	[`zookeeper:3.3.6`](#zookeeper336)
-	[`zookeeper:3.4`](#zookeeper34)
-	[`zookeeper:3.4.10`](#zookeeper3410)
-	[`zookeeper:latest`](#zookeeperlatest)

## `zookeeper:3.3`

```console
$ docker pull zookeeper@sha256:43693e22efb17a3626bddeb5d3f6a661956cc828e063c7090bbab63f088c85b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `zookeeper:3.3` - linux; amd64

```console
$ docker pull zookeeper@sha256:014cde3f9ec2c9399acb3d73c87f4081b772b3fc6dd06b9332790986895d4344
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69292463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08c1c22dae391012da865c7824aa9ad219db6e03d27402a59567919f201a42c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2017 04:13:40 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 04:13:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Thu, 14 Sep 2017 04:25:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_VERSION=8u131
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_ALPINE_VERSION=8.131.11-r2
# Thu, 14 Sep 2017 04:25:42 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 14 Sep 2017 07:50:01 GMT
MAINTAINER Elisey Zanko <elisey.zanko@gmail.com>
# Thu, 14 Sep 2017 07:50:05 GMT
RUN apk add --no-cache     bash     su-exec
# Thu, 14 Sep 2017 07:50:05 GMT
ENV ZOO_USER=zookeeper ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_PORT=2181 ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_MAX_CLIENT_CNXNS=60
# Thu, 14 Sep 2017 07:50:05 GMT
RUN set -ex;     adduser -D "$ZOO_USER";     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR";     chown "$ZOO_USER:$ZOO_USER" "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR"
# Thu, 14 Sep 2017 07:50:06 GMT
ARG GPG_KEY=D0BC8D8A4E90A40AFDFC43B3E22A746A68E327C1
# Thu, 14 Sep 2017 07:50:06 GMT
ARG DISTRO_NAME=zookeeper-3.3.6
# Thu, 14 Sep 2017 07:50:22 GMT
# ARGS: DISTRO_NAME=zookeeper-3.3.6 GPG_KEY=D0BC8D8A4E90A40AFDFC43B3E22A746A68E327C1
RUN set -ex;     apk add --no-cache --virtual .build-deps         gnupg;     wget -q "http://www.apache.org/dist/zookeeper/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     wget -q "http://www.apache.org/dist/zookeeper/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY" ||     gpg --keyserver pgp.mit.edu --recv-keys "$GPG_KEY" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     apk del .build-deps
# Thu, 14 Sep 2017 07:50:22 GMT
WORKDIR /zookeeper-3.3.6
# Thu, 14 Sep 2017 07:50:22 GMT
VOLUME [/data /datalog]
# Thu, 14 Sep 2017 07:50:23 GMT
EXPOSE 2181/tcp 2888/tcp 3888/tcp
# Thu, 14 Sep 2017 07:50:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin:/zookeeper-3.3.6/bin ZOOCFGDIR=/conf
# Thu, 14 Sep 2017 07:50:23 GMT
COPY file:dab1f2991c403145ae0277be86810aa6ab4838363663db6dfbedba997dfd4bcf in / 
# Thu, 14 Sep 2017 07:50:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 07:50:23 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720349d0916a74fb5124be4a8a2bf898de431927e1caec15cc956c8a7fb33d14`  
		Last Modified: Thu, 14 Sep 2017 04:50:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9431a0557160e1ec384a6cfe37d1225528bd236e486010ffc0b75ce7fe1c1465`  
		Last Modified: Thu, 14 Sep 2017 05:01:46 GMT  
		Size: 54.3 MB (54282902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86da735556fee6dc9935895751e31482618d74b42a06c6cadc45cad518d52ca3`  
		Last Modified: Thu, 14 Sep 2017 07:50:57 GMT  
		Size: 1.1 MB (1124440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186b5d47e92c3972a32fb820ffda6c9c2185f9cdb61dcaac31527a2ac1b4a16d`  
		Last Modified: Thu, 14 Sep 2017 07:50:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548b816d0de5af186c9e6bcee10d81de80b0505732ff872f4bb0aa197c1f9a00`  
		Last Modified: Thu, 14 Sep 2017 07:50:58 GMT  
		Size: 11.9 MB (11892637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85504f3b3c6052919a58bed7ceb4bb275f6344c8def56c67de236ecf52f993b`  
		Last Modified: Thu, 14 Sep 2017 07:50:56 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.3.6`

```console
$ docker pull zookeeper@sha256:43693e22efb17a3626bddeb5d3f6a661956cc828e063c7090bbab63f088c85b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `zookeeper:3.3.6` - linux; amd64

```console
$ docker pull zookeeper@sha256:014cde3f9ec2c9399acb3d73c87f4081b772b3fc6dd06b9332790986895d4344
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69292463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08c1c22dae391012da865c7824aa9ad219db6e03d27402a59567919f201a42c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2017 04:13:40 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 04:13:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Thu, 14 Sep 2017 04:25:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_VERSION=8u131
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_ALPINE_VERSION=8.131.11-r2
# Thu, 14 Sep 2017 04:25:42 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 14 Sep 2017 07:50:01 GMT
MAINTAINER Elisey Zanko <elisey.zanko@gmail.com>
# Thu, 14 Sep 2017 07:50:05 GMT
RUN apk add --no-cache     bash     su-exec
# Thu, 14 Sep 2017 07:50:05 GMT
ENV ZOO_USER=zookeeper ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_PORT=2181 ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_MAX_CLIENT_CNXNS=60
# Thu, 14 Sep 2017 07:50:05 GMT
RUN set -ex;     adduser -D "$ZOO_USER";     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR";     chown "$ZOO_USER:$ZOO_USER" "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR"
# Thu, 14 Sep 2017 07:50:06 GMT
ARG GPG_KEY=D0BC8D8A4E90A40AFDFC43B3E22A746A68E327C1
# Thu, 14 Sep 2017 07:50:06 GMT
ARG DISTRO_NAME=zookeeper-3.3.6
# Thu, 14 Sep 2017 07:50:22 GMT
# ARGS: DISTRO_NAME=zookeeper-3.3.6 GPG_KEY=D0BC8D8A4E90A40AFDFC43B3E22A746A68E327C1
RUN set -ex;     apk add --no-cache --virtual .build-deps         gnupg;     wget -q "http://www.apache.org/dist/zookeeper/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     wget -q "http://www.apache.org/dist/zookeeper/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY" ||     gpg --keyserver pgp.mit.edu --recv-keys "$GPG_KEY" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     apk del .build-deps
# Thu, 14 Sep 2017 07:50:22 GMT
WORKDIR /zookeeper-3.3.6
# Thu, 14 Sep 2017 07:50:22 GMT
VOLUME [/data /datalog]
# Thu, 14 Sep 2017 07:50:23 GMT
EXPOSE 2181/tcp 2888/tcp 3888/tcp
# Thu, 14 Sep 2017 07:50:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin:/zookeeper-3.3.6/bin ZOOCFGDIR=/conf
# Thu, 14 Sep 2017 07:50:23 GMT
COPY file:dab1f2991c403145ae0277be86810aa6ab4838363663db6dfbedba997dfd4bcf in / 
# Thu, 14 Sep 2017 07:50:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 07:50:23 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720349d0916a74fb5124be4a8a2bf898de431927e1caec15cc956c8a7fb33d14`  
		Last Modified: Thu, 14 Sep 2017 04:50:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9431a0557160e1ec384a6cfe37d1225528bd236e486010ffc0b75ce7fe1c1465`  
		Last Modified: Thu, 14 Sep 2017 05:01:46 GMT  
		Size: 54.3 MB (54282902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86da735556fee6dc9935895751e31482618d74b42a06c6cadc45cad518d52ca3`  
		Last Modified: Thu, 14 Sep 2017 07:50:57 GMT  
		Size: 1.1 MB (1124440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186b5d47e92c3972a32fb820ffda6c9c2185f9cdb61dcaac31527a2ac1b4a16d`  
		Last Modified: Thu, 14 Sep 2017 07:50:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548b816d0de5af186c9e6bcee10d81de80b0505732ff872f4bb0aa197c1f9a00`  
		Last Modified: Thu, 14 Sep 2017 07:50:58 GMT  
		Size: 11.9 MB (11892637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85504f3b3c6052919a58bed7ceb4bb275f6344c8def56c67de236ecf52f993b`  
		Last Modified: Thu, 14 Sep 2017 07:50:56 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.4`

```console
$ docker pull zookeeper@sha256:c9d677c4d859462e86fa663d1986f5ce1d19032fa12165ecb9f8eb01e80befab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `zookeeper:3.4` - linux; amd64

```console
$ docker pull zookeeper@sha256:8cd51da85f15a703f8fae0150cbddf0e09abe8d26af353749d5720ba86018ef3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92559587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2249a75c5d00931f32779e5593ac02700e07f1648e95137c3acab820575c701`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2017 04:13:40 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 04:13:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Thu, 14 Sep 2017 04:25:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_VERSION=8u131
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_ALPINE_VERSION=8.131.11-r2
# Thu, 14 Sep 2017 04:25:42 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 14 Sep 2017 07:50:01 GMT
MAINTAINER Elisey Zanko <elisey.zanko@gmail.com>
# Thu, 14 Sep 2017 07:50:05 GMT
RUN apk add --no-cache     bash     su-exec
# Thu, 14 Sep 2017 07:50:05 GMT
ENV ZOO_USER=zookeeper ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_PORT=2181 ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_MAX_CLIENT_CNXNS=60
# Thu, 14 Sep 2017 07:50:05 GMT
RUN set -ex;     adduser -D "$ZOO_USER";     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR";     chown "$ZOO_USER:$ZOO_USER" "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR"
# Thu, 14 Sep 2017 07:50:26 GMT
ARG GPG_KEY=C823E3E5B12AF29C67F81976F5CECB3CB5E9BD2D
# Thu, 14 Sep 2017 07:50:27 GMT
ARG DISTRO_NAME=zookeeper-3.4.10
# Thu, 14 Sep 2017 07:50:46 GMT
# ARGS: DISTRO_NAME=zookeeper-3.4.10 GPG_KEY=C823E3E5B12AF29C67F81976F5CECB3CB5E9BD2D
RUN set -ex;     apk add --no-cache --virtual .build-deps         gnupg;     wget -q "http://www.apache.org/dist/zookeeper/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     wget -q "http://www.apache.org/dist/zookeeper/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY" ||     gpg --keyserver pgp.mit.edu --recv-keys "$GPG_KEY" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     apk del .build-deps
# Thu, 14 Sep 2017 07:50:47 GMT
WORKDIR /zookeeper-3.4.10
# Thu, 14 Sep 2017 07:50:47 GMT
VOLUME [/data /datalog]
# Thu, 14 Sep 2017 07:50:47 GMT
EXPOSE 2181/tcp 2888/tcp 3888/tcp
# Thu, 14 Sep 2017 07:50:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin:/zookeeper-3.4.10/bin ZOOCFGDIR=/conf
# Thu, 14 Sep 2017 07:50:47 GMT
COPY file:dab1f2991c403145ae0277be86810aa6ab4838363663db6dfbedba997dfd4bcf in / 
# Thu, 14 Sep 2017 07:50:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 07:50:48 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720349d0916a74fb5124be4a8a2bf898de431927e1caec15cc956c8a7fb33d14`  
		Last Modified: Thu, 14 Sep 2017 04:50:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9431a0557160e1ec384a6cfe37d1225528bd236e486010ffc0b75ce7fe1c1465`  
		Last Modified: Thu, 14 Sep 2017 05:01:46 GMT  
		Size: 54.3 MB (54282902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86da735556fee6dc9935895751e31482618d74b42a06c6cadc45cad518d52ca3`  
		Last Modified: Thu, 14 Sep 2017 07:50:57 GMT  
		Size: 1.1 MB (1124440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186b5d47e92c3972a32fb820ffda6c9c2185f9cdb61dcaac31527a2ac1b4a16d`  
		Last Modified: Thu, 14 Sep 2017 07:50:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac726347bf47c59115dc09926565e9c6e6bfe4abfd630bb70d3f10aa4168e71`  
		Last Modified: Thu, 14 Sep 2017 07:51:17 GMT  
		Size: 35.2 MB (35159761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23175ccbbeb7028f0019e8b098f23c06b0767d7299e09ba251a6af39c75c01a`  
		Last Modified: Thu, 14 Sep 2017 07:51:13 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.4.10`

```console
$ docker pull zookeeper@sha256:c9d677c4d859462e86fa663d1986f5ce1d19032fa12165ecb9f8eb01e80befab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `zookeeper:3.4.10` - linux; amd64

```console
$ docker pull zookeeper@sha256:8cd51da85f15a703f8fae0150cbddf0e09abe8d26af353749d5720ba86018ef3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92559587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2249a75c5d00931f32779e5593ac02700e07f1648e95137c3acab820575c701`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2017 04:13:40 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 04:13:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Thu, 14 Sep 2017 04:25:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_VERSION=8u131
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_ALPINE_VERSION=8.131.11-r2
# Thu, 14 Sep 2017 04:25:42 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 14 Sep 2017 07:50:01 GMT
MAINTAINER Elisey Zanko <elisey.zanko@gmail.com>
# Thu, 14 Sep 2017 07:50:05 GMT
RUN apk add --no-cache     bash     su-exec
# Thu, 14 Sep 2017 07:50:05 GMT
ENV ZOO_USER=zookeeper ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_PORT=2181 ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_MAX_CLIENT_CNXNS=60
# Thu, 14 Sep 2017 07:50:05 GMT
RUN set -ex;     adduser -D "$ZOO_USER";     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR";     chown "$ZOO_USER:$ZOO_USER" "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR"
# Thu, 14 Sep 2017 07:50:26 GMT
ARG GPG_KEY=C823E3E5B12AF29C67F81976F5CECB3CB5E9BD2D
# Thu, 14 Sep 2017 07:50:27 GMT
ARG DISTRO_NAME=zookeeper-3.4.10
# Thu, 14 Sep 2017 07:50:46 GMT
# ARGS: DISTRO_NAME=zookeeper-3.4.10 GPG_KEY=C823E3E5B12AF29C67F81976F5CECB3CB5E9BD2D
RUN set -ex;     apk add --no-cache --virtual .build-deps         gnupg;     wget -q "http://www.apache.org/dist/zookeeper/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     wget -q "http://www.apache.org/dist/zookeeper/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY" ||     gpg --keyserver pgp.mit.edu --recv-keys "$GPG_KEY" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     apk del .build-deps
# Thu, 14 Sep 2017 07:50:47 GMT
WORKDIR /zookeeper-3.4.10
# Thu, 14 Sep 2017 07:50:47 GMT
VOLUME [/data /datalog]
# Thu, 14 Sep 2017 07:50:47 GMT
EXPOSE 2181/tcp 2888/tcp 3888/tcp
# Thu, 14 Sep 2017 07:50:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin:/zookeeper-3.4.10/bin ZOOCFGDIR=/conf
# Thu, 14 Sep 2017 07:50:47 GMT
COPY file:dab1f2991c403145ae0277be86810aa6ab4838363663db6dfbedba997dfd4bcf in / 
# Thu, 14 Sep 2017 07:50:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 07:50:48 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720349d0916a74fb5124be4a8a2bf898de431927e1caec15cc956c8a7fb33d14`  
		Last Modified: Thu, 14 Sep 2017 04:50:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9431a0557160e1ec384a6cfe37d1225528bd236e486010ffc0b75ce7fe1c1465`  
		Last Modified: Thu, 14 Sep 2017 05:01:46 GMT  
		Size: 54.3 MB (54282902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86da735556fee6dc9935895751e31482618d74b42a06c6cadc45cad518d52ca3`  
		Last Modified: Thu, 14 Sep 2017 07:50:57 GMT  
		Size: 1.1 MB (1124440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186b5d47e92c3972a32fb820ffda6c9c2185f9cdb61dcaac31527a2ac1b4a16d`  
		Last Modified: Thu, 14 Sep 2017 07:50:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac726347bf47c59115dc09926565e9c6e6bfe4abfd630bb70d3f10aa4168e71`  
		Last Modified: Thu, 14 Sep 2017 07:51:17 GMT  
		Size: 35.2 MB (35159761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23175ccbbeb7028f0019e8b098f23c06b0767d7299e09ba251a6af39c75c01a`  
		Last Modified: Thu, 14 Sep 2017 07:51:13 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:latest`

```console
$ docker pull zookeeper@sha256:c9d677c4d859462e86fa663d1986f5ce1d19032fa12165ecb9f8eb01e80befab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `zookeeper:latest` - linux; amd64

```console
$ docker pull zookeeper@sha256:8cd51da85f15a703f8fae0150cbddf0e09abe8d26af353749d5720ba86018ef3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92559587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2249a75c5d00931f32779e5593ac02700e07f1648e95137c3acab820575c701`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2017 04:13:40 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 04:13:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Thu, 14 Sep 2017 04:25:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_VERSION=8u131
# Thu, 14 Sep 2017 04:25:34 GMT
ENV JAVA_ALPINE_VERSION=8.131.11-r2
# Thu, 14 Sep 2017 04:25:42 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 14 Sep 2017 07:50:01 GMT
MAINTAINER Elisey Zanko <elisey.zanko@gmail.com>
# Thu, 14 Sep 2017 07:50:05 GMT
RUN apk add --no-cache     bash     su-exec
# Thu, 14 Sep 2017 07:50:05 GMT
ENV ZOO_USER=zookeeper ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_PORT=2181 ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_MAX_CLIENT_CNXNS=60
# Thu, 14 Sep 2017 07:50:05 GMT
RUN set -ex;     adduser -D "$ZOO_USER";     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR";     chown "$ZOO_USER:$ZOO_USER" "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR"
# Thu, 14 Sep 2017 07:50:26 GMT
ARG GPG_KEY=C823E3E5B12AF29C67F81976F5CECB3CB5E9BD2D
# Thu, 14 Sep 2017 07:50:27 GMT
ARG DISTRO_NAME=zookeeper-3.4.10
# Thu, 14 Sep 2017 07:50:46 GMT
# ARGS: DISTRO_NAME=zookeeper-3.4.10 GPG_KEY=C823E3E5B12AF29C67F81976F5CECB3CB5E9BD2D
RUN set -ex;     apk add --no-cache --virtual .build-deps         gnupg;     wget -q "http://www.apache.org/dist/zookeeper/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     wget -q "http://www.apache.org/dist/zookeeper/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY" ||     gpg --keyserver pgp.mit.edu --recv-keys "$GPG_KEY" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     apk del .build-deps
# Thu, 14 Sep 2017 07:50:47 GMT
WORKDIR /zookeeper-3.4.10
# Thu, 14 Sep 2017 07:50:47 GMT
VOLUME [/data /datalog]
# Thu, 14 Sep 2017 07:50:47 GMT
EXPOSE 2181/tcp 2888/tcp 3888/tcp
# Thu, 14 Sep 2017 07:50:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin:/zookeeper-3.4.10/bin ZOOCFGDIR=/conf
# Thu, 14 Sep 2017 07:50:47 GMT
COPY file:dab1f2991c403145ae0277be86810aa6ab4838363663db6dfbedba997dfd4bcf in / 
# Thu, 14 Sep 2017 07:50:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 07:50:48 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720349d0916a74fb5124be4a8a2bf898de431927e1caec15cc956c8a7fb33d14`  
		Last Modified: Thu, 14 Sep 2017 04:50:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9431a0557160e1ec384a6cfe37d1225528bd236e486010ffc0b75ce7fe1c1465`  
		Last Modified: Thu, 14 Sep 2017 05:01:46 GMT  
		Size: 54.3 MB (54282902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86da735556fee6dc9935895751e31482618d74b42a06c6cadc45cad518d52ca3`  
		Last Modified: Thu, 14 Sep 2017 07:50:57 GMT  
		Size: 1.1 MB (1124440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186b5d47e92c3972a32fb820ffda6c9c2185f9cdb61dcaac31527a2ac1b4a16d`  
		Last Modified: Thu, 14 Sep 2017 07:50:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac726347bf47c59115dc09926565e9c6e6bfe4abfd630bb70d3f10aa4168e71`  
		Last Modified: Thu, 14 Sep 2017 07:51:17 GMT  
		Size: 35.2 MB (35159761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23175ccbbeb7028f0019e8b098f23c06b0767d7299e09ba251a6af39c75c01a`  
		Last Modified: Thu, 14 Sep 2017 07:51:13 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
