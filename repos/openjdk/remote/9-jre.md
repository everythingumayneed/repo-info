## `openjdk:9-jre`

```console
$ docker pull openjdk@sha256:8b1c7bfdb98e18552fb3aae8a739d12c69b81f079d83219c8ced9de48d9a6913
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

### `openjdk:9-jre` - linux; amd64

```console
$ docker pull openjdk@sha256:7976bf2d432d1901144cfedeec48d71cfb7280490926e66c239b5e2a67f9b00f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339628531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57decab795a3cc5a420ad79ee767cf7fa0e67f5c18df76962d59dec41e75eff7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 09 Oct 2017 21:32:24 GMT
ADD file:d558b03d3d859cf66504349fc540b4c9ea26365896e7cc64fa87a79ca21bcf78 in / 
# Mon, 09 Oct 2017 21:32:24 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:33:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 22:33:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 10 Oct 2017 00:56:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:56:52 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 00:56:53 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 00:56:54 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 00:56:54 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 00:56:54 GMT
ENV JAVA_VERSION=9-b181
# Tue, 10 Oct 2017 00:56:54 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Tue, 10 Oct 2017 00:57:45 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
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
	-	`sha256:82778428e07641125327971168285129e3ba441ecd842001243dc101ebf61e64`  
		Last Modified: Tue, 10 Oct 2017 01:35:17 GMT  
		Size: 855.6 KB (855569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1d7ba119a5b30a05594bd8c5aa001f2dcff735bd4def7e8af140770babb49a`  
		Last Modified: Tue, 10 Oct 2017 01:35:17 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45bc206640a65ef432a7d450250a37f91263abbf64efb51bb0a839651f6c82e`  
		Last Modified: Tue, 10 Oct 2017 01:35:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49626e0ac053b36ffcbae3b40934b4c7586de14f0fb87fe21d775eb9d432dc3`  
		Last Modified: Tue, 10 Oct 2017 01:36:01 GMT  
		Size: 273.4 MB (273383771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-jre` - linux; arm variant v5

```console
$ docker pull openjdk@sha256:b9d1203a1fa424b481e23e905ee0da99026ed8aa1ba6d8b454740ad80a6c5e80
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308227901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a0d8086ad9749f4a0b8c00b87b419e77fb323c4891ca2e900477a2936f50fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 09 Oct 2017 21:43:38 GMT
ADD file:ed4faefd58667ec248b15ae9b227fc04967695ab4002e9f3a65e8e53b3f73cc6 in / 
# Mon, 09 Oct 2017 21:43:39 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:16:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 22:16:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 10 Oct 2017 08:15:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 08:15:58 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 08:15:58 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 08:15:59 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 08:15:59 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 08:15:59 GMT
ENV JAVA_VERSION=9-b181
# Tue, 10 Oct 2017 08:16:00 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Tue, 10 Oct 2017 08:17:13 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:45a6221cafba09e06352fbe396f5863616e79d7ab2b9481c3016ee02a2fc322d`  
		Last Modified: Mon, 09 Oct 2017 21:49:19 GMT  
		Size: 46.0 MB (46010091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a71f239a0573ab2b5a38f8e4787b24e0ed366e436a7165e9ff81a4ea2645db`  
		Last Modified: Mon, 09 Oct 2017 22:25:10 GMT  
		Size: 7.7 MB (7735486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ce7be1041ce6e58e87ad6afb19bf18a87d2165de44e26e939f089cc710b651`  
		Last Modified: Mon, 09 Oct 2017 22:25:10 GMT  
		Size: 9.0 MB (9016383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a6be5d0733e2c6defa57b5b9af32dc534c7c9977c98a4b85816b10a2aeb7ae`  
		Last Modified: Tue, 10 Oct 2017 08:23:00 GMT  
		Size: 848.7 KB (848706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba348bd1838af9ae734307029a0e037cea63147412e0932ca60e90ed06cc4894`  
		Last Modified: Tue, 10 Oct 2017 08:23:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac88ec578ba543983b7eb5b39b7c83c86c5c103aab5f0ca49ea7ee2ac444b1c`  
		Last Modified: Tue, 10 Oct 2017 08:23:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:face4aefd716b182bd412c7e6e0301b15f5f58888a8a654ce35203dc74ff53a5`  
		Last Modified: Tue, 10 Oct 2017 08:23:52 GMT  
		Size: 244.6 MB (244616857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-jre` - linux; arm variant v7

```console
$ docker pull openjdk@sha256:846e23e81bcc3f998530910eefdc5f72848b5bc6fe9b27ea255321e9a45d53e3
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308144996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa0190e0c414c2edbf308c2967ddc5b896d6c8985cff9347d78c3f073da598a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:14 GMT
ADD file:8310e9969f49ad8da22c8531636a505f796ae2e5ab255104280bbe27bd312eb2 in / 
# Mon, 09 Oct 2017 21:44:15 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:21:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 22:21:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 09 Oct 2017 23:11:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 23:11:32 GMT
ENV LANG=C.UTF-8
# Mon, 09 Oct 2017 23:11:33 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 09 Oct 2017 23:11:34 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 09 Oct 2017 23:11:35 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 09 Oct 2017 23:11:35 GMT
ENV JAVA_VERSION=9-b181
# Mon, 09 Oct 2017 23:11:35 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Mon, 09 Oct 2017 23:12:42 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:c73d8f8e11b2d23be25158f1c637fa52a156601fa88a99dae20e4e90c9f8094e`  
		Last Modified: Mon, 09 Oct 2017 21:50:57 GMT  
		Size: 44.2 MB (44221149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f095d6eb4fb7112eed5df1d4ec6df80dba73c8cf89cb23d2b882b20b26a990db`  
		Last Modified: Mon, 09 Oct 2017 22:32:26 GMT  
		Size: 7.6 MB (7565479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bc97a5447d52b18ed72c0f57ee0282eabc3a90a66debb1556b65434b85175c`  
		Last Modified: Mon, 09 Oct 2017 22:32:26 GMT  
		Size: 8.8 MB (8801265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2636a8169c3c67390fa8bdcb26557a8c48ccac495c940edc899b57350918cf6`  
		Last Modified: Mon, 09 Oct 2017 23:28:01 GMT  
		Size: 832.6 KB (832564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ff7588e673a640f851fe8f5b43dac3fa01c7bd4b4649a73c76a7cd4a8d2ace`  
		Last Modified: Mon, 09 Oct 2017 23:28:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3cde4a48f59d004d065421764406a6771f7149975ce32ba61cfbc4458b5ad0`  
		Last Modified: Mon, 09 Oct 2017 23:28:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acaa13084c9d9e2b777880c8553973724d60676af70e23cba8af38e83335781`  
		Last Modified: Mon, 09 Oct 2017 23:28:50 GMT  
		Size: 246.7 MB (246724160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-jre` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0a7f54ad27f3a4c221f897771ecbd9d4d9f55777b8beb8b9c6dc85ab4a4b6117
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313459621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6860dd1c314c9669a282e95e56445c2a84ff48c920f378155eb4ccf23945d22d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 09 Oct 2017 21:45:25 GMT
ADD file:2dbe9971a07bebac37e2e609659f04c039921d9ece341799444660b1c747e595 in / 
# Mon, 09 Oct 2017 21:45:26 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:52:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 22:52:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 10 Oct 2017 01:52:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 01:53:00 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 01:53:04 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 01:53:09 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 01:53:12 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 01:53:15 GMT
ENV JAVA_VERSION=9-b181
# Tue, 10 Oct 2017 01:53:18 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Tue, 10 Oct 2017 02:00:27 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:e81325a6af85f75a75f466627b0f3e722d22ef0a99868726a293425fa3678d30`  
		Last Modified: Mon, 09 Oct 2017 21:57:27 GMT  
		Size: 45.3 MB (45334165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6b15acc099095e5b3dae6d84d900fe23c7d7fdf62fa46ad2bf73cd1939322b`  
		Last Modified: Mon, 09 Oct 2017 23:29:57 GMT  
		Size: 7.7 MB (7719898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749e8c0209ca35b7d2c6836c10ca36a971cf8c58f53b1654c5c8e675f11470d`  
		Last Modified: Mon, 09 Oct 2017 23:29:57 GMT  
		Size: 9.0 MB (9013384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9539825b98dea89c05f8640df46fda40dbd8afe7179835552e9b4b5dd5da5199`  
		Last Modified: Tue, 10 Oct 2017 02:24:36 GMT  
		Size: 841.9 KB (841946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1987b137da415ab1814a5e31d1d8fdfb59cc30cbfada63227639e267288fb1dd`  
		Last Modified: Tue, 10 Oct 2017 02:24:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4bf6805a69066d90b1a3be0e9c6afc4d9f0e7d44c149b0b230d0944a385fb2`  
		Last Modified: Tue, 10 Oct 2017 02:24:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fcd93d3aa146da2a81d347b7f94e9f70950c3cba0f1915859abd8e48a7a016`  
		Last Modified: Tue, 10 Oct 2017 02:25:42 GMT  
		Size: 250.5 MB (250549850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-jre` - linux; 386

```console
$ docker pull openjdk@sha256:b9f487d76a0bcd8342930d25c12a29c369259bb5969218e3831013ec1c7dea21
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347503170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e851571f9fe2da3cdcb2ab21520b4c0c24e3546ec68131bec5622f35f871d3fd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:31 GMT
ADD file:7151fc1811302d898848668f8be530bdc1d6b0832da7b159b54c108f9b9f39ef in / 
# Mon, 09 Oct 2017 21:44:32 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:07:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 23:08:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 10 Oct 2017 01:29:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 01:29:06 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 01:29:07 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 01:29:08 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 01:29:09 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 01:29:09 GMT
ENV JAVA_VERSION=9-b181
# Tue, 10 Oct 2017 01:29:09 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Tue, 10 Oct 2017 01:31:00 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:c4f0ba6c109e4a20a92a03d7e3ed54b584598a77c79e7891221658b1b505c8d3`  
		Last Modified: Mon, 09 Oct 2017 21:50:58 GMT  
		Size: 48.4 MB (48397299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b294cfff7eb8dcc3dafb8c0e7697c3a7d4be20ea1cffb502417ad7ef4a81c`  
		Last Modified: Mon, 09 Oct 2017 23:38:45 GMT  
		Size: 8.5 MB (8522414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c3b53a9e9d87dd74dc2a2c6f2f180cfbde0232334af5b23318831fd50a3151`  
		Last Modified: Mon, 09 Oct 2017 23:38:45 GMT  
		Size: 9.6 MB (9553600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34471774ffb32d47dbe4a6b2fc725c7e83d7f3859b8995d539ff08d9c6053aa`  
		Last Modified: Tue, 10 Oct 2017 02:04:44 GMT  
		Size: 864.4 KB (864400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355a54ba729fee99200347e7e1d367ce6f45232cd881751130b21e6f33ce324b`  
		Last Modified: Tue, 10 Oct 2017 02:04:44 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a3f98dcb3cc127801bce30b4b6c174aad6e6b3a1d76f00f693e942561f263c`  
		Last Modified: Tue, 10 Oct 2017 02:04:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbcd52ad2e554b27eba79d80de2a33670e7a69931227f8a1db9863a1bccea58`  
		Last Modified: Tue, 10 Oct 2017 02:05:31 GMT  
		Size: 280.2 MB (280165078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-jre` - linux; ppc64le

```console
$ docker pull openjdk@sha256:b5fd2cadddde78eac479cf5dd926e64cbf1e63b5c36624a5475f4957d7ad045c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322867301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52985250269b12f9ebc9d7d664ac94d81bd8cc7a12893aff9bdd70c0be806a1b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:18 GMT
ADD file:c095ec4581fd0b74d04b5c60602abfc26045b0c8018b11e233ff33678663b4bc in / 
# Mon, 09 Oct 2017 21:44:21 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 23:34:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 10 Oct 2017 04:44:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 04:44:07 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 04:44:15 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 04:44:24 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 04:44:27 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Oct 2017 04:44:29 GMT
ENV JAVA_VERSION=9-b181
# Tue, 10 Oct 2017 04:44:31 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Tue, 10 Oct 2017 05:01:58 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:11a0304e8c893e4d955264c2d8a8a0c4dd84908eba9876476623a4a364a7c48e`  
		Last Modified: Mon, 09 Oct 2017 21:50:45 GMT  
		Size: 48.7 MB (48723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ee00dbe27034f9638c9023274ecf0166a5b554572eb473a7ffc2b3c764737c`  
		Last Modified: Tue, 10 Oct 2017 00:56:04 GMT  
		Size: 8.0 MB (7978865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61e6c60857c077b60e6f1bed65fd0305a4f2dd5780a6e42953e68147c6141a1`  
		Last Modified: Tue, 10 Oct 2017 00:56:04 GMT  
		Size: 9.5 MB (9498659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d177e5090def4650ff7f3da9582777ceb4f3c74e43a714179a0889c9f7f9e4`  
		Last Modified: Tue, 10 Oct 2017 05:23:53 GMT  
		Size: 852.0 KB (851969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb33c327c1bd4f09349ee6f16949ec92588f10d0eea0738d1c691a2138593f71`  
		Last Modified: Tue, 10 Oct 2017 05:23:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbfc20af0a90b4595c791869027ef1df77e303a5c3c344d565e78b3abd7e439`  
		Last Modified: Tue, 10 Oct 2017 05:23:52 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3339534c486332d9c0ab374c41e40f8893b96cadafbc236ca66d59fde2088c42`  
		Last Modified: Tue, 10 Oct 2017 05:25:16 GMT  
		Size: 255.8 MB (255813835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-jre` - linux; s390x

```console
$ docker pull openjdk@sha256:b05d32d3f22710f543d565f2af3ace2523c0ed9aee230c239998f991c2a5e1ec
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.9 MB (299912195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767effd149a024419f777a1f85e4d5bd56b84b811e797ad816fdb19075f8cda3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 09 Oct 2017 21:43:27 GMT
ADD file:51898e1a12f3bbc77c696e9156d7bb51579dc530148ca78c00142c511a349de6 in / 
# Mon, 09 Oct 2017 21:43:27 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:13:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 22:13:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 09 Oct 2017 22:57:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 22:57:34 GMT
ENV LANG=C.UTF-8
# Mon, 09 Oct 2017 22:57:35 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 09 Oct 2017 22:57:36 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 09 Oct 2017 22:57:36 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 09 Oct 2017 22:57:36 GMT
ENV JAVA_VERSION=9-b181
# Mon, 09 Oct 2017 22:57:36 GMT
ENV JAVA_DEBIAN_VERSION=9~b181-4
# Mon, 09 Oct 2017 22:58:27 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:387500139c6151d781fe62dbc679af96a9ac79dc2049d4b57d00beb6515f3617`  
		Last Modified: Mon, 09 Oct 2017 21:47:41 GMT  
		Size: 47.3 MB (47292875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2bf7517ce1b767b32d484c45cdbde2774795f97aa23cbd2ca4f9aa57e0907e`  
		Last Modified: Mon, 09 Oct 2017 22:20:45 GMT  
		Size: 8.1 MB (8093416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74288a4e0c7163fd8f413c3f39aea05d13784a92020bf38c86348ef9d2b76b67`  
		Last Modified: Mon, 09 Oct 2017 22:20:45 GMT  
		Size: 9.2 MB (9248587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa44fa0b81de0ef5c29dc509af5a864f43ba0f662d5afccfa81439cd34334a6`  
		Last Modified: Mon, 09 Oct 2017 23:04:46 GMT  
		Size: 866.2 KB (866155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf893cbe656c7cb73341c7fb1109880471355435c0977c89c18efe715e35a10`  
		Last Modified: Mon, 09 Oct 2017 23:04:46 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cad695beb707fb317d3305b6cec83212dc0e76be56cc1d7720c441c4257120`  
		Last Modified: Mon, 09 Oct 2017 23:04:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0631f0630da1193561d2b3813a1fec9e5eb9b28d5550270945efe54e4cb99346`  
		Last Modified: Mon, 09 Oct 2017 23:05:17 GMT  
		Size: 234.4 MB (234410784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
