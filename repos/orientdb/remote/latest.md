## `orientdb:latest`

```console
$ docker pull orientdb@sha256:e2caf64d8448c82331e9c84c703a72e9a109a98166a8ac786251f87756543fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:38ed7982b3f29f0c7cdf2d785f5f607d8402b22a8b7ff26323946ca51ec03022
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116970225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a4e1ff2dc8d37b9746746c95338d6aa64d60c0771a786872133a3f003c6ff1`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2017 04:13:40 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 04:13:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 04:21:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Thu, 14 Sep 2017 04:21:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 14 Sep 2017 04:21:31 GMT
ENV JAVA_VERSION=8u131
# Thu, 14 Sep 2017 04:21:31 GMT
ENV JAVA_ALPINE_VERSION=8.131.11-r2
# Thu, 14 Sep 2017 04:21:39 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 14 Sep 2017 06:40:32 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 14 Sep 2017 06:40:43 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 06 Oct 2017 18:37:31 GMT
ENV ORIENTDB_VERSION=2.2.29
# Fri, 06 Oct 2017 18:37:31 GMT
ENV ORIENTDB_DOWNLOAD_MD5=f20dc9a571e3b361bf115f1a5b9b82cb
# Fri, 06 Oct 2017 18:37:31 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=051f68bdc70642744def2c85d7136673a6bf24c1
# Fri, 06 Oct 2017 18:37:32 GMT
ENV ORIENTDB_DOWNLOAD_URL=http://central.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.29/orientdb-community-2.2.29.tar.gz
# Fri, 06 Oct 2017 18:37:35 GMT
RUN apk add --update tar curl     && rm -rf /var/cache/apk/*
# Fri, 06 Oct 2017 18:37:41 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 06 Oct 2017 18:37:41 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Fri, 06 Oct 2017 18:37:42 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 06 Oct 2017 18:37:42 GMT
WORKDIR /orientdb
# Fri, 06 Oct 2017 18:37:42 GMT
EXPOSE 2424/tcp
# Fri, 06 Oct 2017 18:37:42 GMT
EXPOSE 2480/tcp
# Fri, 06 Oct 2017 18:37:43 GMT
CMD ["server.sh"]
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
	-	`sha256:42a4b3080d3cc157970baf6edf6194df12fa0a9dc61d2c1525781ae4af65213c`  
		Last Modified: Thu, 14 Sep 2017 04:59:04 GMT  
		Size: 70.1 MB (70051361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df238cfb90639443a84c7dfe64eed41845a2968b365a63e13da766c6aea136a2`  
		Last Modified: Fri, 06 Oct 2017 18:38:01 GMT  
		Size: 662.5 KB (662481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72210388770339e73eebf9534c49eb04bad63f20cf2516213f0a7dd226728c4c`  
		Last Modified: Fri, 06 Oct 2017 18:38:04 GMT  
		Size: 44.3 MB (44265741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
