## `openjdk:9-slim`

```console
$ docker pull openjdk@sha256:c1bac838dc63a270629ac3fad8a335b6a55d9b9c4f5658fcdddba5934be6262a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `openjdk:9-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:6c6438a0cfbac1a83f09aebef3dc3fbe39652e299428550639ed7e7275f56b7c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181789253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dca67f4790e7b45e42f0daba715983a8da2f2f6e9762515e0dd2be5c805fc84`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Oct 2017 21:32:38 GMT
ADD file:4f5c99023af857b40a8bb5ef610e4fc8a4ab4bcec326fcffddd3c18162eb5a90 in / 
# Mon, 09 Oct 2017 21:32:38 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 00:53:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:53:13 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 00:53:14 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 00:53:14 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 00:53:14 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 00:53:15 GMT
ENV JAVA_VERSION=9-b181
# Tue, 10 Oct 2017 00:53:15 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Tue, 10 Oct 2017 00:53:56 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 10 Oct 2017 00:53:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f84388a33351f025313af89e330691da0d2d0f7309fa0d0f6cbb15e0160473d`  
		Last Modified: Mon, 09 Oct 2017 21:40:21 GMT  
		Size: 24.9 MB (24897397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af7807a0ec32711dd39dcdd82043f6ae89e4b101f7105e75f29c0a6ecd9b132`  
		Last Modified: Tue, 10 Oct 2017 01:28:41 GMT  
		Size: 460.4 KB (460389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d580f15c0bb3bdb994dfaefd68e8459d5901df7fc39b4bd6a4b758786f8225`  
		Last Modified: Tue, 10 Oct 2017 01:28:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a3b03fc984224fd6836153e97c1a8d632351cacc82689281efaf1a82b3ca5e`  
		Last Modified: Tue, 10 Oct 2017 01:28:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08022c1872b4ef17d20fe930d6f53e90993fd1ab2c2b1a28e9c22605b1a74337`  
		Last Modified: Tue, 10 Oct 2017 01:29:07 GMT  
		Size: 156.4 MB (156431089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-slim` - linux; arm variant v5

```console
$ docker pull openjdk@sha256:22693b453dc06976eca7bfefe98e4111ae4710f46a6c52955ea71b22fd41cea2
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155077259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048c789d3cce7dde28c4d64ca4a3740a66b2b385dd0c515ba91543aad1f105d0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Oct 2017 21:43:49 GMT
ADD file:53515d12c277346acef474e8405d99646f72a11380a3b75d1dad8756510e6870 in / 
# Mon, 09 Oct 2017 21:43:49 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 22:30:35 GMT
ENV LANG=C.UTF-8
# Mon, 09 Oct 2017 22:30:36 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 09 Oct 2017 22:30:37 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 09 Oct 2017 22:30:38 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 09 Oct 2017 22:30:38 GMT
ENV JAVA_VERSION=9-b181
# Mon, 09 Oct 2017 22:30:38 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Mon, 09 Oct 2017 22:31:33 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Mon, 09 Oct 2017 22:31:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea37965471e13f9e6050ef152f0f00007063aed293f9ab9254f7ae0062caffe9`  
		Last Modified: Mon, 09 Oct 2017 21:49:34 GMT  
		Size: 23.3 MB (23348454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec082c0f8a485cb2fc949ff337b67626da849d056263c1e0248f98c847b5c21`  
		Last Modified: Mon, 09 Oct 2017 22:35:30 GMT  
		Size: 453.8 KB (453840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f6cc6201a4bb264d660ccd911867d17fbe817ca21b715fc9434b49ebed1a78`  
		Last Modified: Mon, 09 Oct 2017 22:35:30 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a147ee1897b6272956335a08816ffbef1187d77ddafd822f9312e36e7034eb1d`  
		Last Modified: Mon, 09 Oct 2017 22:35:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c0faf86df96a8f4f87910900514ca42689c39e74b95d049f1bda3685e8e3c4`  
		Last Modified: Mon, 09 Oct 2017 22:35:55 GMT  
		Size: 131.3 MB (131274586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-slim` - linux; arm variant v7

```console
$ docker pull openjdk@sha256:11f4453e8bb2c67d9377ef28cdf1c9b789654e4eadae66c185fc700088fdf853
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158703285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e15a83f00d695bb8ffe16fd43dde795ba7178489ae5823da36a25f60e531f0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:28 GMT
ADD file:5d5c4a7233c6c9a2682e39e732a1f23db741e074dbc5b6f16309bb53d0bdaf18 in / 
# Mon, 09 Oct 2017 21:44:29 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:10:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 23:10:27 GMT
ENV LANG=C.UTF-8
# Mon, 09 Oct 2017 23:10:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 09 Oct 2017 23:10:30 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 09 Oct 2017 23:10:30 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 09 Oct 2017 23:10:30 GMT
ENV JAVA_VERSION=9-b181
# Mon, 09 Oct 2017 23:10:31 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Mon, 09 Oct 2017 23:11:16 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Mon, 09 Oct 2017 23:11:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d96a59f9a30fc164a930c5f4118584e683bec40d1797f9d9bca30f65f3a647af`  
		Last Modified: Mon, 09 Oct 2017 21:51:14 GMT  
		Size: 21.6 MB (21639073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c164bdc72bb7e7c356d01b6f09f139b666b9b352a4ddc54537fdaa48e8a0ad6`  
		Last Modified: Mon, 09 Oct 2017 23:27:15 GMT  
		Size: 436.4 KB (436444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40759634bf5c1bbde4c10d3cb802e1d71d31216cf2c389d566820272f1239ca`  
		Last Modified: Mon, 09 Oct 2017 23:27:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaabb110ae529eef899672bd02ae789a08f5b8093187fded0073a6352a26493d`  
		Last Modified: Mon, 09 Oct 2017 23:27:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d844640aaa94a99f4ee621f2f4ad3006eb33dee4e1e745776431b3733b7f7a50`  
		Last Modified: Mon, 09 Oct 2017 23:27:38 GMT  
		Size: 136.6 MB (136627390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b19b1e210ac842019e98484c2aa591ea81cc0b056eff5242c280ad9e74036f07
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161684689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92d3f7629f2cbf0c74368b78b5bd168a1ac32fbf4ecc607543402eb62ba67cb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Oct 2017 21:45:50 GMT
ADD file:7734ca257bd7327a8da07cdcc881d2054c6cf50201f5bb0aeda8637c7e40cc06 in / 
# Mon, 09 Oct 2017 21:45:51 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 01:49:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 01:49:51 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 01:49:53 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 01:49:55 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 01:49:55 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 01:49:56 GMT
ENV JAVA_VERSION=9-b181
# Tue, 10 Oct 2017 01:49:57 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Tue, 10 Oct 2017 01:52:07 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 10 Oct 2017 01:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9dc315cd342ed5fdb1c77afafbe657c1c29de0747c81d85f1f9ae06ad1d01fa4`  
		Last Modified: Mon, 09 Oct 2017 21:59:06 GMT  
		Size: 22.7 MB (22709128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f96b1ccf72714886ea440013736b3705900f6f9751ec2664a26a9cb3042e3f0`  
		Last Modified: Tue, 10 Oct 2017 02:22:06 GMT  
		Size: 445.3 KB (445252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d7984bd0489b39fe260c46dcb9772e8656599426233067ad9af68b557e2d73`  
		Last Modified: Tue, 10 Oct 2017 02:22:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3682b3ee64dc20e447d8a52e66fd89da4f08cb2341fc1836b460609fc12eb0d`  
		Last Modified: Tue, 10 Oct 2017 02:22:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42934029f8dcbcb579e040f9cc84c49b8d40a6de13bc36079b0679c7d253c18`  
		Last Modified: Tue, 10 Oct 2017 02:23:39 GMT  
		Size: 138.5 MB (138529932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-slim` - linux; 386

```console
$ docker pull openjdk@sha256:fd09a9b0d3d676e6c263dbaf315d86d53ff622ee67592fd7c70f0bba666169b5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185191140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e5a2b3b8db12f9cfe210a0fb3e97b9055a1e8f9f2597b0b2d914d02787e4a6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:42 GMT
ADD file:19c55eeae4bfb6e75c713222705ba8d4849604df30a58a50860ac7bd205dfda4 in / 
# Mon, 09 Oct 2017 21:44:42 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 01:28:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 01:28:08 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 01:28:09 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 01:28:10 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 01:28:10 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 01:28:10 GMT
ENV JAVA_VERSION=9-b181
# Tue, 10 Oct 2017 01:28:11 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Tue, 10 Oct 2017 01:28:53 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 10 Oct 2017 01:28:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8dbd94837ca8315beb351e1b4a4633d7694cecb75bd76e51339f9fc3d1362ea4`  
		Last Modified: Mon, 09 Oct 2017 21:51:23 GMT  
		Size: 25.7 MB (25658987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4541ed9bcc08c4b1df4164753e37f6503b3dc167e45d1ee73bae5df2235d4bd5`  
		Last Modified: Tue, 10 Oct 2017 02:03:41 GMT  
		Size: 469.1 KB (469054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dc19ed4e40f01efc0a9b7e8728b3a714e8988d9988c655294a7cd0557e4fd4`  
		Last Modified: Tue, 10 Oct 2017 02:03:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6adbd212b15cf15807ba58d5148c502ce8708f3fb6e4b929f35ab3e2806ba9c`  
		Last Modified: Tue, 10 Oct 2017 02:03:40 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dfdebfbd5da818c309ceda0c9dabf3d7d263a14fd8b3a00c80043bd961f9f4`  
		Last Modified: Tue, 10 Oct 2017 02:04:01 GMT  
		Size: 159.1 MB (159062721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-slim` - linux; ppc64le

```console
$ docker pull openjdk@sha256:5e907834d8839274d9eceb6e7766844ef942562ead1bdcf8b86656fe38449b43
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166212609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9960ce04daa4fb3ce61fc3ab3d9a1b974b657f8710eafc4b271f8d3379d8e0a0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:35 GMT
ADD file:975af260e7927569ddcee28239226e9deaf2ba539f038b467169340d69bc7072 in / 
# Mon, 09 Oct 2017 21:44:37 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 04:37:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 04:37:48 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 04:37:54 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 04:38:01 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 04:38:05 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 04:38:08 GMT
ENV JAVA_VERSION=9-b181
# Tue, 10 Oct 2017 04:38:10 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Tue, 10 Oct 2017 04:43:15 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 10 Oct 2017 04:43:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:58316d9a92e4d6154c1ca7f3d20c3fe96a2931387507b6226b9bcb094ebf13a1`  
		Last Modified: Mon, 09 Oct 2017 21:51:05 GMT  
		Size: 25.9 MB (25935856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cb131ef3a79b457ff98e269a64ece4b6e5a2b846dfeffe8d816ad700c89eb1`  
		Last Modified: Tue, 10 Oct 2017 05:22:45 GMT  
		Size: 455.2 KB (455170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af6ed7bad84f73f72309cd6fd34c5f02d380a962d70be083f47f50011e29f8b`  
		Last Modified: Tue, 10 Oct 2017 05:22:46 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c81bf7c16727685616c16f67bbedf2377b69b2b65856f76e421844e15d28208`  
		Last Modified: Tue, 10 Oct 2017 05:22:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad353dc067f2f356dd58bf08db15a7176aac0c93e90ca265147cc5b4e93e39f`  
		Last Modified: Tue, 10 Oct 2017 05:23:29 GMT  
		Size: 139.8 MB (139821203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-slim` - linux; s390x

```console
$ docker pull openjdk@sha256:76de555895ed83fd710696e1ed8569b31d1a36dd3ea5705bacd56443a1115f1c
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165655425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b79db22d69ba8889cbd4267a540de385b5742b188262e5b7c26d3b8c972d3f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Oct 2017 21:43:37 GMT
ADD file:b4deb6fb528f8c816ba7db3484f7590bf072a683b2d2bf4b616ac44850e10494 in / 
# Mon, 09 Oct 2017 21:43:38 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:56:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 22:56:38 GMT
ENV LANG=C.UTF-8
# Mon, 09 Oct 2017 22:56:38 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 09 Oct 2017 22:56:41 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 09 Oct 2017 22:56:44 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 09 Oct 2017 22:56:46 GMT
ENV JAVA_VERSION=9-b181
# Mon, 09 Oct 2017 22:56:48 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Mon, 09 Oct 2017 22:57:23 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Mon, 09 Oct 2017 22:57:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:044c9ae4e8107afdcd4e6b93a76f7d598ae117778f3cf7dacd9d6087e3ac4f3b`  
		Last Modified: Mon, 09 Oct 2017 21:47:55 GMT  
		Size: 24.6 MB (24643207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9070e5b963f9d96e62e6d5bd2a1e800f7745293b6bf97e423d883ad4cb6a280d`  
		Last Modified: Mon, 09 Oct 2017 23:04:14 GMT  
		Size: 471.4 KB (471352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624213d4686ead64a27d4dac297ad322ddab0cf41272465a4cd53620bcbd47b`  
		Last Modified: Mon, 09 Oct 2017 23:04:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c076a1ba6889dcaf5124d6f37956b4265b3b023a96bbdd23780ad89cb3cf18`  
		Last Modified: Mon, 09 Oct 2017 23:04:15 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9290ac191bab6543ec6d236fdebfdb6b2e677a1a1651ca5e3026a61539d83a`  
		Last Modified: Mon, 09 Oct 2017 23:04:30 GMT  
		Size: 140.5 MB (140540487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
