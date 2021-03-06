## `maven:3-jdk-8-slim`

```console
$ docker pull maven@sha256:a6782eb9084d78ba6aedab86497220c9d8adc69035ffe068707dc43a0694ae8b
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

### `maven:3-jdk-8-slim` - linux; amd64

```console
$ docker pull maven@sha256:6cb3a8e4bb5c90bd0437007bcc76a293f225930dc7bdc52e506f56047028847e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103880569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c4173bcfc5761a2ad170b87e0ca452669d3ca7011ef7cdd479af358f8a73ec`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 09 Oct 2017 21:33:42 GMT
ADD file:45233d6b5c9b91e9437065d3e7c332d1c4eb4bce8e1079a4c1af342c450abe67 in / 
# Mon, 09 Oct 2017 21:33:43 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 00:49:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:49:52 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 00:49:53 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 00:49:53 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 00:49:53 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 00:49:54 GMT
ENV JAVA_VERSION=8u141
# Tue, 10 Oct 2017 00:49:54 GMT
ENV JAVA_DEBIAN_VERSION=8u141-b15-1~deb9u1
# Tue, 10 Oct 2017 00:49:54 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 10 Oct 2017 00:50:13 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 10 Oct 2017 00:50:14 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 10 Oct 2017 09:58:23 GMT
ARG MAVEN_VERSION=3.5.0
# Tue, 10 Oct 2017 09:58:23 GMT
ARG USER_HOME_DIR=/root
# Tue, 10 Oct 2017 09:58:24 GMT
ARG SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034
# Tue, 10 Oct 2017 09:58:24 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries
# Tue, 10 Oct 2017 09:58:33 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl   && rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 09:58:35 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 10 Oct 2017 09:58:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 10 Oct 2017 09:58:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 10 Oct 2017 09:58:36 GMT
COPY file:e4099db07053a2301f4263d416cab324c1f89ee74c752bebec511d8b59464cb6 in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 10 Oct 2017 09:58:36 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Tue, 10 Oct 2017 09:58:37 GMT
VOLUME [/root/.m2]
# Tue, 10 Oct 2017 09:58:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 10 Oct 2017 09:58:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bc95e04b23c06ba1b9bf092d07d1493177b218e0340bd2ed49dac351c1e34313`  
		Last Modified: Mon, 09 Oct 2017 21:42:28 GMT  
		Size: 22.5 MB (22492350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9244331a890e4aec0df6e10bce14d07eaa1bde905780d45fc41f12fd615d732c`  
		Last Modified: Tue, 10 Oct 2017 01:22:35 GMT  
		Size: 454.8 KB (454783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f111692a5874ce9859050b16b85e181a6ccadf449e850fa65a2a49a72b0d77c`  
		Last Modified: Tue, 10 Oct 2017 01:22:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838df694d9c3f97ab5439d7a43ad258fd52186bb900ccb303cabb1e04246953b`  
		Last Modified: Tue, 10 Oct 2017 01:22:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e28e4f90e03290c2a0417b0aa708fa3b838e9405592370a49feb22ed2d84d5`  
		Last Modified: Tue, 10 Oct 2017 01:22:48 GMT  
		Size: 68.5 MB (68455512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc233c0a95c1214fb9aeb4a724cdc41914d89f910f7352351de93f8d798d7dd2`  
		Last Modified: Tue, 10 Oct 2017 01:22:35 GMT  
		Size: 272.0 KB (272030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001fbda5019ee0bb6892ca8f60c2822d4b8b7682126f6269ed1a7421fe4bdd0`  
		Last Modified: Tue, 10 Oct 2017 10:01:53 GMT  
		Size: 3.5 MB (3531625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623b056430215a1a88dfa89a4eae6ecd6104a41edf4a558cd9183c4ed0e3d145`  
		Last Modified: Tue, 10 Oct 2017 10:01:54 GMT  
		Size: 8.7 MB (8672796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a150b7693b08f9eeef93f90b715277a0005e05e2ac44a7ae998c2dd9d169d6`  
		Last Modified: Tue, 10 Oct 2017 10:01:51 GMT  
		Size: 735.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b95a6838ae8414b358e2e505747b25a9e24cfa3912a0eacfa9b5e9a526f061`  
		Last Modified: Tue, 10 Oct 2017 10:01:51 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-jdk-8-slim` - linux; arm variant v5

```console
$ docker pull maven@sha256:b0ed569ebb1e6e09b9e253be9713e41ce4eb9ee178fafe47d80814a56881939d
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90120651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06866f6c669a1416d5ba7b53d9dffc10c2b5cb5db90394613c8745bb93bfa04`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:48 GMT
ADD file:ff9945b48b1ac236dcec24eb9dfaf52b7c151a3b11c8502391f0866dfb4e3ac3 in / 
# Mon, 09 Oct 2017 21:44:48 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 22:28:40 GMT
ENV LANG=C.UTF-8
# Mon, 09 Oct 2017 22:28:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 09 Oct 2017 22:28:42 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 09 Oct 2017 22:28:42 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 09 Oct 2017 22:28:43 GMT
ENV JAVA_VERSION=8u141
# Mon, 09 Oct 2017 22:28:43 GMT
ENV JAVA_DEBIAN_VERSION=8u141-b15-1~deb9u1
# Mon, 09 Oct 2017 22:28:43 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Mon, 09 Oct 2017 22:29:22 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Mon, 09 Oct 2017 22:29:27 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 10 Oct 2017 01:31:01 GMT
ARG MAVEN_VERSION=3.5.0
# Tue, 10 Oct 2017 01:31:02 GMT
ARG USER_HOME_DIR=/root
# Tue, 10 Oct 2017 01:31:02 GMT
ARG SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034
# Tue, 10 Oct 2017 01:31:03 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries
# Tue, 10 Oct 2017 01:31:14 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl   && rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 01:31:17 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 10 Oct 2017 01:31:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 10 Oct 2017 01:31:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 10 Oct 2017 01:31:18 GMT
COPY file:e4099db07053a2301f4263d416cab324c1f89ee74c752bebec511d8b59464cb6 in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 10 Oct 2017 01:31:19 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Tue, 10 Oct 2017 01:31:19 GMT
VOLUME [/root/.m2]
# Tue, 10 Oct 2017 01:31:19 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 10 Oct 2017 01:31:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:836d5b6056a9815be79c76480a90299267f60201bd1e3396817003e6c14819cc`  
		Last Modified: Mon, 09 Oct 2017 21:50:56 GMT  
		Size: 21.2 MB (21166251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5157015f0bd49750479bdb4a232fc207026b23874b5511f0c27a1036727e350`  
		Last Modified: Mon, 09 Oct 2017 22:34:32 GMT  
		Size: 447.6 KB (447638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbbd094d7ff14181d978a21b9b418571f16a4ed689f7f43cc92bad967710265`  
		Last Modified: Mon, 09 Oct 2017 22:34:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b426de7c4048293b8f750a1a91fb8046e1a1f7374ebcd47a78ec8177ed43b1ef`  
		Last Modified: Mon, 09 Oct 2017 22:34:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f306bc3b64c5283be70f0fba7a87dd9a307f3abae8d6681ea951a5bba9a6f7a`  
		Last Modified: Mon, 09 Oct 2017 22:34:47 GMT  
		Size: 56.5 MB (56536016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982392af1508a542f3c6f876092e251f05477cc0b4faa4ce8571be0075a44477`  
		Last Modified: Mon, 09 Oct 2017 22:34:32 GMT  
		Size: 272.2 KB (272178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35e1348c17364d971303551d3af0f3aedcd846659406e9f94fd807dcffd8424`  
		Last Modified: Tue, 10 Oct 2017 01:32:17 GMT  
		Size: 3.0 MB (3024242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d776802012797a67a436816aec3ea98ce158fea13a77d62b4ee97a75da996649`  
		Last Modified: Tue, 10 Oct 2017 01:32:18 GMT  
		Size: 8.7 MB (8672856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0775f510f5c9a0b8b86d4a1439a48716636972372df4f452411873e261dea9da`  
		Last Modified: Tue, 10 Oct 2017 01:32:15 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b0956608b9ed9c9bdbb8919b822284e4b1bc132376e40755b7e0194b31bb0b`  
		Last Modified: Tue, 10 Oct 2017 01:32:15 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-jdk-8-slim` - linux; arm variant v7

```console
$ docker pull maven@sha256:1c609e97861eb2f5455d7ba4c097e0124f947bd9395fff294e5d6ef57bcbb923
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87032552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb03f1227472f6a42e172c78651b33ac455b3f09a4c18602020b093a231befc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 09 Oct 2017 21:45:43 GMT
ADD file:b758c6c3ff989778bd740dde35c86b953fa09be913a7e02711b2881de6b8911d in / 
# Mon, 09 Oct 2017 21:45:44 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:05:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 23:05:30 GMT
ENV LANG=C.UTF-8
# Mon, 09 Oct 2017 23:05:32 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 09 Oct 2017 23:05:33 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 09 Oct 2017 23:05:33 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 09 Oct 2017 23:05:34 GMT
ENV JAVA_VERSION=8u141
# Mon, 09 Oct 2017 23:05:34 GMT
ENV JAVA_DEBIAN_VERSION=8u141-b15-1~deb9u1
# Mon, 09 Oct 2017 23:05:35 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Mon, 09 Oct 2017 23:06:08 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Mon, 09 Oct 2017 23:06:14 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 10 Oct 2017 01:19:34 GMT
ARG MAVEN_VERSION=3.5.0
# Tue, 10 Oct 2017 01:19:34 GMT
ARG USER_HOME_DIR=/root
# Tue, 10 Oct 2017 01:19:35 GMT
ARG SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034
# Tue, 10 Oct 2017 01:19:35 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries
# Tue, 10 Oct 2017 01:19:45 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl   && rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 01:19:57 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 10 Oct 2017 01:19:58 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 10 Oct 2017 01:19:58 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 10 Oct 2017 01:19:58 GMT
COPY file:e4099db07053a2301f4263d416cab324c1f89ee74c752bebec511d8b59464cb6 in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 10 Oct 2017 01:19:59 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Tue, 10 Oct 2017 01:19:59 GMT
VOLUME [/root/.m2]
# Tue, 10 Oct 2017 01:20:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 10 Oct 2017 01:20:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:59e81a3fde58ec8d4b8f2f58b98ef2f4d951d37dd9b99b016fd294a8e07d7796`  
		Last Modified: Mon, 09 Oct 2017 21:52:49 GMT  
		Size: 19.3 MB (19277135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6226915187b9d61d290e04413a4ccdf021b5e0fc267ba8129cc0126cab1f1a93`  
		Last Modified: Mon, 09 Oct 2017 23:24:02 GMT  
		Size: 430.6 KB (430580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98b9b3c90ff2ee65efc9f88b2383f6f1760df78bcd965fa0b22e001977eaf96`  
		Last Modified: Mon, 09 Oct 2017 23:24:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377cafaae0c7321b0549f3949d78826675109fe908cb8521f39fe433ccfced7c`  
		Last Modified: Mon, 09 Oct 2017 23:24:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b54cd082813272ec0eee997651297edb9bab1e57b36937aeb96ef819318ed1e`  
		Last Modified: Mon, 09 Oct 2017 23:24:18 GMT  
		Size: 55.5 MB (55499788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc34b3797b251df09cbf29653d3faf2fabcdf80cb0f026c5bd5a61c741cea657`  
		Last Modified: Mon, 09 Oct 2017 23:24:02 GMT  
		Size: 272.2 KB (272179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4b310c781088b01ce1cc7543d7be259be5b45f9e5f710d9736a2e830586c2`  
		Last Modified: Tue, 10 Oct 2017 01:22:53 GMT  
		Size: 2.9 MB (2878542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e425e25cfaacf5eeeef3d725c4f3ed685462747cf9ac8ffee5a219024b6e1b`  
		Last Modified: Tue, 10 Oct 2017 01:22:54 GMT  
		Size: 8.7 MB (8672855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c342c81ef437676bd5f31006ca236d019b177f83c312a1e04a579d534a80ce02`  
		Last Modified: Tue, 10 Oct 2017 01:22:52 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7e28268a2ee8bf5991966bcbdf711e0d72e39fe9018c6d9ee9a1080629fae6`  
		Last Modified: Tue, 10 Oct 2017 01:22:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-jdk-8-slim` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:affb9756c60e51cb2b9aca76447f1b5f8357a90486cdad0564d916b40d4ab48e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90972701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea9f3d876d4806e20d2b2dfb3df06c0673a5cbea9185341850dcd49903fba79`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 09 Oct 2017 21:47:55 GMT
ADD file:3a528355cfc75437716aff3b517ef99ae602918d84d26dbafff0ed142248fb93 in / 
# Mon, 09 Oct 2017 21:47:56 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 01:28:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 01:28:29 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 01:28:30 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 01:28:40 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 01:28:40 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 01:28:50 GMT
ENV JAVA_VERSION=8u141
# Tue, 10 Oct 2017 01:28:58 GMT
ENV JAVA_DEBIAN_VERSION=8u141-b15-1~deb9u1
# Tue, 10 Oct 2017 01:28:59 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 10 Oct 2017 01:30:13 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 10 Oct 2017 01:30:19 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 10 Oct 2017 12:51:46 GMT
ARG MAVEN_VERSION=3.5.0
# Tue, 10 Oct 2017 12:51:46 GMT
ARG USER_HOME_DIR=/root
# Tue, 10 Oct 2017 12:51:47 GMT
ARG SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034
# Tue, 10 Oct 2017 12:51:48 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries
# Tue, 10 Oct 2017 12:52:11 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl   && rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 12:52:17 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 10 Oct 2017 12:52:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 10 Oct 2017 12:52:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 10 Oct 2017 12:52:19 GMT
COPY file:e4099db07053a2301f4263d416cab324c1f89ee74c752bebec511d8b59464cb6 in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 10 Oct 2017 12:52:19 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Tue, 10 Oct 2017 12:52:20 GMT
VOLUME [/root/.m2]
# Tue, 10 Oct 2017 12:52:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 10 Oct 2017 12:52:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e907afd6e25615a4d3eb554d930cef57b87e79ec82413889c2eac38beb4eb8f7`  
		Last Modified: Mon, 09 Oct 2017 22:03:08 GMT  
		Size: 20.3 MB (20337143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a727a90fab15cbfc5f05ababc5c02416ee800f138c5c7a5439eb1b2e323a3e`  
		Last Modified: Tue, 10 Oct 2017 02:15:52 GMT  
		Size: 440.8 KB (440793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5692da35bab82003fb0cc285002d5c2cf8a001ac800c9e3e14fd5026f41bc7ed`  
		Last Modified: Tue, 10 Oct 2017 02:15:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc3ffc0cbcf7695d1498de6039806f2bf5a6cb7d2862b331372f29c402c382f`  
		Last Modified: Tue, 10 Oct 2017 02:15:52 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df63a56890e45b20a4610ec6523295d5bdb9412389c065b50e660e99f6b46b57`  
		Last Modified: Tue, 10 Oct 2017 02:16:25 GMT  
		Size: 58.3 MB (58251080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238e5c9b4f5366fbfd8f99bad5b6594a4f73bb67b014c07ef0b9cde90ea8b7b4`  
		Last Modified: Tue, 10 Oct 2017 02:15:52 GMT  
		Size: 272.1 KB (272095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741ba5002141e80faa23d7816eeb92a1bf92150dd774c40bad5ade5d34ba66a6`  
		Last Modified: Tue, 10 Oct 2017 12:58:13 GMT  
		Size: 3.0 MB (2997343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8720449b402a4f82c2ac4876647e1618b7004b3b2868415ca94dd52126974c6`  
		Last Modified: Tue, 10 Oct 2017 12:58:14 GMT  
		Size: 8.7 MB (8672772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d10a3079eb806414c4a4049b749dee992043a57745588beb7291eadb275e9d4`  
		Last Modified: Tue, 10 Oct 2017 12:58:12 GMT  
		Size: 735.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc5479a0c94f12a537ca156c5507f73e17c442b37361e869d1b551bd53c922d`  
		Last Modified: Tue, 10 Oct 2017 12:58:12 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-jdk-8-slim` - linux; 386

```console
$ docker pull maven@sha256:fb53f96b39b5f75019cb7bd9767ceca6146ee0b21048d017336178d0f202a63a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103682365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef13b2306917e3aaa4d7daaee2aa06ff270666fbe74f0d1c3ffa3db2035579be`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 09 Oct 2017 21:45:36 GMT
ADD file:6582536277127947668f7bfdc1471a4e36170915b91a4cb841e7e1bfa1de6535 in / 
# Mon, 09 Oct 2017 21:45:36 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 01:12:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 01:12:56 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 01:12:58 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 01:12:58 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 01:12:59 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 01:12:59 GMT
ENV JAVA_VERSION=8u141
# Tue, 10 Oct 2017 01:12:59 GMT
ENV JAVA_DEBIAN_VERSION=8u141-b15-1~deb9u1
# Tue, 10 Oct 2017 01:12:59 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 10 Oct 2017 01:13:30 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 10 Oct 2017 01:13:32 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 10 Oct 2017 04:21:33 GMT
ARG MAVEN_VERSION=3.5.0
# Tue, 10 Oct 2017 04:21:34 GMT
ARG USER_HOME_DIR=/root
# Tue, 10 Oct 2017 04:21:34 GMT
ARG SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034
# Tue, 10 Oct 2017 04:21:34 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries
# Tue, 10 Oct 2017 04:21:41 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl   && rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 04:21:43 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 10 Oct 2017 04:21:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 10 Oct 2017 04:21:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 10 Oct 2017 04:21:43 GMT
COPY file:e4099db07053a2301f4263d416cab324c1f89ee74c752bebec511d8b59464cb6 in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 10 Oct 2017 04:21:44 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Tue, 10 Oct 2017 04:21:44 GMT
VOLUME [/root/.m2]
# Tue, 10 Oct 2017 04:21:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 10 Oct 2017 04:21:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b2b52fe46b29fe5d0689f26449c2114e40f0731d4ce3eb8c3941397b74205432`  
		Last Modified: Mon, 09 Oct 2017 21:53:42 GMT  
		Size: 23.1 MB (23128678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7853b0a86faa843cda410f263a64ed5ba757a019c60eecb5902c191e41d5e1eb`  
		Last Modified: Tue, 10 Oct 2017 01:53:30 GMT  
		Size: 463.5 KB (463454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca21864f4b88fad8ba103bfc79ee0908fd694c165ef5a0b46919f203e822188a`  
		Last Modified: Tue, 10 Oct 2017 01:53:30 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18652bc80c9f29e1dcf29225e3e5e82bdbcde149fe8b95219bd5c0f808b5211c`  
		Last Modified: Tue, 10 Oct 2017 01:53:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b09cbe459d2d6e66b4a6e57c52702ef821cf730cbca002bf20fa3cc0dd55ec6`  
		Last Modified: Tue, 10 Oct 2017 01:53:44 GMT  
		Size: 67.7 MB (67700322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7565a346cded999c65118b00d6c89a56a19eca1746f9e7440cac91e2db0df326`  
		Last Modified: Tue, 10 Oct 2017 01:53:30 GMT  
		Size: 272.1 KB (272146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aafb7bb3fdb128d5baa3d4cf67ebfe4afc34000f4451423d9cfde67c3f77942`  
		Last Modified: Tue, 10 Oct 2017 04:24:25 GMT  
		Size: 3.4 MB (3443472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5281cbf8e1e1aefdb32a0133b2c5aac07f861c69030672384a548fedaef65f`  
		Last Modified: Tue, 10 Oct 2017 04:24:26 GMT  
		Size: 8.7 MB (8672822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73765b9807fb617d6e8b4c890301aa1d9be944dbc3d79190615c9e4a93f6c9ab`  
		Last Modified: Tue, 10 Oct 2017 04:24:25 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbe0281cb6fdb4471917b085e707edd8025f32808ccb90806261f25a295f569`  
		Last Modified: Tue, 10 Oct 2017 04:24:23 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-jdk-8-slim` - linux; ppc64le

```console
$ docker pull maven@sha256:38b1e4607a4e27e4fb32c3243925a8f787942b74c12ce077f0f40d7a81f3533c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93990228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f021b0b9f781633bf186ddb6334e81cf2d86984dc103e36ea5a3e13b9d74318`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 09 Oct 2017 21:45:56 GMT
ADD file:7edf73437495be24244c16841b563be06c15452963f41ac940fb5e105ed96027 in / 
# Mon, 09 Oct 2017 21:45:58 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 03:38:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 03:38:37 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 03:38:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 03:38:57 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 03:39:02 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 03:39:06 GMT
ENV JAVA_VERSION=8u141
# Tue, 10 Oct 2017 03:39:10 GMT
ENV JAVA_DEBIAN_VERSION=8u141-b15-1~deb9u1
# Tue, 10 Oct 2017 03:39:14 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 10 Oct 2017 03:46:16 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 10 Oct 2017 03:46:22 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 10 Oct 2017 09:50:33 GMT
ARG MAVEN_VERSION=3.5.0
# Tue, 10 Oct 2017 09:50:38 GMT
ARG USER_HOME_DIR=/root
# Tue, 10 Oct 2017 09:50:40 GMT
ARG SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034
# Tue, 10 Oct 2017 09:50:43 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries
# Tue, 10 Oct 2017 09:51:53 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl   && rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 09:52:10 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 10 Oct 2017 09:52:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 10 Oct 2017 09:52:16 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 10 Oct 2017 09:52:20 GMT
COPY file:e4099db07053a2301f4263d416cab324c1f89ee74c752bebec511d8b59464cb6 in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 10 Oct 2017 09:52:32 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Tue, 10 Oct 2017 09:52:45 GMT
VOLUME [/root/.m2]
# Tue, 10 Oct 2017 09:52:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 10 Oct 2017 09:52:54 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c4860466fa1e6824151f4fa3a51ef0e9d7d3c3ba860e21d94e69988b65601260`  
		Last Modified: Mon, 09 Oct 2017 21:52:59 GMT  
		Size: 22.7 MB (22746217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73df072fb69cadf906dd2f3522f93ee911666af83ba9ab5f97bfe839d32822c5`  
		Last Modified: Tue, 10 Oct 2017 05:12:41 GMT  
		Size: 449.8 KB (449799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d776a3d19316e343e85e29960b7bb8553c71cac10990b3fa919e5c4fa4338f5`  
		Last Modified: Tue, 10 Oct 2017 05:12:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a45b43bf439e946d85916a7ecd48ef55110070ba9ce3c85651345d07aaa08f2`  
		Last Modified: Tue, 10 Oct 2017 05:12:40 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eea08692df95d904d7400cb9c97c9489586e6e53f1d43aa25f1fcc1d7badd45`  
		Last Modified: Tue, 10 Oct 2017 05:13:03 GMT  
		Size: 58.6 MB (58637166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b00316d28023ece407adba774e7077cd98d2e14b1c938d3d0db584cde298ab`  
		Last Modified: Tue, 10 Oct 2017 05:12:41 GMT  
		Size: 272.0 KB (272044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97211a965a7ce06f701e0088dc0f2b52ed639b6471e438f301212984580bfcf4`  
		Last Modified: Tue, 10 Oct 2017 09:58:49 GMT  
		Size: 3.2 MB (3210675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2ce96b28b6cdba71dd844857a3132be3baebebbef55ceccd9a2a95b7da2cc8`  
		Last Modified: Tue, 10 Oct 2017 09:58:49 GMT  
		Size: 8.7 MB (8672851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6b465a8bccbb5e23a36da74a509fe7f6c4ced01ec50395d2d12ee9b8d51ddc`  
		Last Modified: Tue, 10 Oct 2017 09:58:49 GMT  
		Size: 736.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fee8e292c21e63389b13bf073aeb95d70a32394074c49a1de3cbb0cbdeea6fe`  
		Last Modified: Tue, 10 Oct 2017 09:58:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-jdk-8-slim` - linux; s390x

```console
$ docker pull maven@sha256:2f10144574711e5b1025380450582dd0f71e997ce32636bc433d288f92ad14cb
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92668061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d74d3c7d6b4e4b9f43b27cbeadc299135e295b294184acd0951e62ee1324942`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:35 GMT
ADD file:ae4aaa6affe22f36ab5478771d5c84917f72de7a8dac16345a035709a1a5edf4 in / 
# Mon, 09 Oct 2017 21:44:36 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:52:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 22:52:36 GMT
ENV LANG=C.UTF-8
# Mon, 09 Oct 2017 22:52:37 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 09 Oct 2017 22:52:37 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 09 Oct 2017 22:52:37 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 09 Oct 2017 22:52:38 GMT
ENV JAVA_VERSION=8u141
# Mon, 09 Oct 2017 22:52:38 GMT
ENV JAVA_DEBIAN_VERSION=8u141-b15-1~deb9u1
# Mon, 09 Oct 2017 22:52:38 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Mon, 09 Oct 2017 22:53:10 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Mon, 09 Oct 2017 22:53:12 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 10 Oct 2017 01:20:46 GMT
ARG MAVEN_VERSION=3.5.0
# Tue, 10 Oct 2017 01:20:46 GMT
ARG USER_HOME_DIR=/root
# Tue, 10 Oct 2017 01:20:46 GMT
ARG SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034
# Tue, 10 Oct 2017 01:20:46 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries
# Tue, 10 Oct 2017 01:20:53 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl   && rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 01:20:59 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.5.0/binaries MAVEN_VERSION=3.5.0 SHA=beb91419245395bd69a4a6edad5ca3ec1a8b64e41457672dc687c173a495f034 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha256sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 10 Oct 2017 01:20:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 10 Oct 2017 01:21:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 10 Oct 2017 01:21:00 GMT
COPY file:e4099db07053a2301f4263d416cab324c1f89ee74c752bebec511d8b59464cb6 in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 10 Oct 2017 01:21:00 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Tue, 10 Oct 2017 01:21:00 GMT
VOLUME [/root/.m2]
# Tue, 10 Oct 2017 01:21:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 10 Oct 2017 01:21:01 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:671716cc49517eef5f430c695ce344d63e390cb65f58d30939f2ba615c953686`  
		Last Modified: Mon, 09 Oct 2017 21:49:09 GMT  
		Size: 22.3 MB (22339951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b68a7778da3a2e44964f508fbd3bc92882c4ad1dbd961716e950115a17786c`  
		Last Modified: Mon, 09 Oct 2017 23:02:01 GMT  
		Size: 465.7 KB (465695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cbedee24083ce9a877823999b311c5211df0a60c7d39f0f1a7ffc40e5d3d98`  
		Last Modified: Mon, 09 Oct 2017 23:02:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b4c73c20e2fb65e204d4f0e9530411503632baa0c81a5cd04aa4258ad9c478`  
		Last Modified: Mon, 09 Oct 2017 23:02:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff107e8605f877b67a64c0bea37d46ff610f742062cfbd1ad4cec4e2d4338982`  
		Last Modified: Mon, 09 Oct 2017 23:02:13 GMT  
		Size: 57.6 MB (57597680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36553e27252d10ca7d945672d977007dc866b9a6cd833eb6f236c242394dbccd`  
		Last Modified: Mon, 09 Oct 2017 23:02:01 GMT  
		Size: 272.2 KB (272160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0c299ba1a7d1a9ea79d2867b8a3679ef4570389a9b5619174654ab84a1592c`  
		Last Modified: Tue, 10 Oct 2017 01:22:58 GMT  
		Size: 3.3 MB (3318301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae17c60ae99bf38336de36df5a324cecaeb1276a6d6f3c32de42526fc30f59c`  
		Last Modified: Tue, 10 Oct 2017 01:22:58 GMT  
		Size: 8.7 MB (8672802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47a1044d52db8d2a68e0aa60668264bded663e0f7680cd789ee493b01817420`  
		Last Modified: Tue, 10 Oct 2017 01:22:57 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef1526c5d4aff1a7dfe980adfd57a8a068d1ddd71e67ccd67400a98e6d638a6`  
		Last Modified: Tue, 10 Oct 2017 01:22:57 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
