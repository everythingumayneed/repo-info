## `gradle:jdk9`

```console
$ docker pull gradle@sha256:13006789fa1923c13fa6d64e0957172efe654d7eb6c8181bc52ac55569b5489c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gradle:jdk9` - linux; amd64

```console
$ docker pull gradle@sha256:ece012491c830fae2553fbfd3336f9353c9bdd5dae3df69a595491b0fa0f9660
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.7 MB (464718598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55aab7ecec6306abfcc1aa677d9e9be8e7fd9857a044ce047b203513593581fe`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 09 Oct 2017 21:32:24 GMT
ADD file:d558b03d3d859cf66504349fc540b4c9ea26365896e7cc64fa87a79ca21bcf78 in / 
# Mon, 09 Oct 2017 21:32:24 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:33:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 22:33:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 09 Oct 2017 22:33:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:51:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:52:00 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 00:52:01 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 00:52:01 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 00:52:02 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 00:52:02 GMT
ENV JAVA_VERSION=9-b181
# Tue, 10 Oct 2017 00:52:02 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Tue, 10 Oct 2017 00:52:53 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 10 Oct 2017 00:52:53 GMT
CMD ["jshell"]
# Tue, 10 Oct 2017 04:05:04 GMT
CMD ["gradle"]
# Tue, 10 Oct 2017 04:05:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 10 Oct 2017 04:05:04 GMT
ENV GRADLE_VERSION=4.2.1
# Tue, 10 Oct 2017 04:05:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=b551cc04f2ca51c78dd14edb060621f0e5439bdfafa6fd167032a09ac708fbc0
# Tue, 10 Oct 2017 04:05:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b551cc04f2ca51c78dd14edb060621f0e5439bdfafa6fd167032a09ac708fbc0
RUN set -o errexit -o nounset 	&& echo "Downloading Gradle" 	&& wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip" 		&& echo "Checking download hash" 	&& echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check - 		&& echo "Installing Gradle" 	&& unzip gradle.zip 	&& rm gradle.zip 	&& mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/" 	&& ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle 		&& echo "Adding gradle user and group" 	&& groupadd --system --gid 1000 gradle 	&& useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle 	&& mkdir /home/gradle/.gradle 	&& chown --recursive gradle:gradle /home/gradle 		&& echo "Symlinking root Gradle cache to gradle Gradle cache" 	&& ln -s /home/gradle/.gradle /root/.gradle
# Tue, 10 Oct 2017 04:05:09 GMT
USER [gradle]
# Tue, 10 Oct 2017 04:05:10 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 10 Oct 2017 04:05:10 GMT
WORKDIR /home/gradle
# Tue, 10 Oct 2017 04:05:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b551cc04f2ca51c78dd14edb060621f0e5439bdfafa6fd167032a09ac708fbc0
RUN set -o errexit -o nounset 	&& echo "Testing Gradle installation" 	&& gradle --version
```

-	Layers:
	-	`sha256:3a8649ffa174245c68120e05b22db9c8a8f781cc4d9c24816fb562ecf8ab9652`  
		Last Modified: Mon, 09 Oct 2017 21:39:55 GMT  
		Size: 47.6 MB (47561948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b58c0540eee85afd65d984ed9680210a9e8740b186454a9c5411b9b3862140e`  
		Last Modified: Mon, 09 Oct 2017 22:59:35 GMT  
		Size: 8.6 MB (8552413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c55f19db116c2c49c508d0625d83267697fdac44eba96a9510109088f88fc40`  
		Last Modified: Mon, 09 Oct 2017 22:59:34 GMT  
		Size: 9.3 MB (9274450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf7e2e8b82f67b215add075a7fcc9ca4d027d7f375ddcb3a5d09f0eb6c3afca`  
		Last Modified: Mon, 09 Oct 2017 23:00:03 GMT  
		Size: 48.2 MB (48207160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32822f5e747ae22da3c35acc657e511a8168f628458e42877ed0ec9cd42dcdbf`  
		Last Modified: Tue, 10 Oct 2017 01:27:15 GMT  
		Size: 893.8 KB (893756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68eab7eb0322f04354ca240de0d8e9eace1d6dcc89d779fbbcd264ef137025ea`  
		Last Modified: Tue, 10 Oct 2017 01:27:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e345a4b7188b7ca6b86546091bc61ecca78d94ecee591b281a1a73687b155c3d`  
		Last Modified: Tue, 10 Oct 2017 01:27:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46af528a88a933a783d0a32ab91877c8fa43e708efc3527cc5f78c6251f1497`  
		Last Modified: Tue, 10 Oct 2017 01:27:58 GMT  
		Size: 279.2 MB (279152519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc7f3f52e334daf969e252448f630cc4601e29c493ad3c8a54e0dd432250882`  
		Last Modified: Tue, 10 Oct 2017 04:09:49 GMT  
		Size: 71.1 MB (71075835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c23f48e7b42154a75190efd0a0c8e6ad5ba26018c16bfac172fa9fcbd9eeb0`  
		Last Modified: Tue, 10 Oct 2017 04:09:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
