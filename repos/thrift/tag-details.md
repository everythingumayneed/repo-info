<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `thrift`

-	[`thrift:0.10`](#thrift010)
-	[`thrift:0.10.0`](#thrift0100)
-	[`thrift:0.9`](#thrift09)
-	[`thrift:0.9.3`](#thrift093)
-	[`thrift:latest`](#thriftlatest)

## `thrift:0.10`

```console
$ docker pull thrift@sha256:6cfff8d58d440226a31cb17bb3a9d7b35dd00ede88a066684d08c2bff6b9dd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `thrift:0.10` - linux; amd64

```console
$ docker pull thrift@sha256:2aa008aa88c46bba4275eb6d00bb497b12e1f4a36ce0d3b4c21b025a267024de
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51257075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d03e48a8adab43060fdd42a61f88fbfdf002f6040fdb6e1b8b8477c99e7a781`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 09 Oct 2017 21:34:51 GMT
ADD file:4a0b4ab0f637224302bf3f7a7eedc5b75a404bc1188499ef2f98edb7ce44d0ed in / 
# Mon, 09 Oct 2017 21:34:51 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:16 GMT
MAINTAINER Adam Hawkins <hi@ahawkins.me>
# Mon, 09 Oct 2017 22:15:16 GMT
ENV THRIFT_VERSION=0.10.0
# Mon, 09 Oct 2017 22:18:02 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Mon, 09 Oct 2017 22:18:03 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:39e552a2b1f74a9985244528219d26fc1c27f1447a3d04e64b63bd70a4e68e2c`  
		Last Modified: Mon, 09 Oct 2017 21:44:19 GMT  
		Size: 38.1 MB (38103127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98039a56a27a312c2c10df1d0bc390784bf3b2d90ad8f0dda43e4be012a09c8b`  
		Last Modified: Mon, 09 Oct 2017 22:18:54 GMT  
		Size: 13.2 MB (13153948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.10.0`

```console
$ docker pull thrift@sha256:6cfff8d58d440226a31cb17bb3a9d7b35dd00ede88a066684d08c2bff6b9dd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `thrift:0.10.0` - linux; amd64

```console
$ docker pull thrift@sha256:2aa008aa88c46bba4275eb6d00bb497b12e1f4a36ce0d3b4c21b025a267024de
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51257075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d03e48a8adab43060fdd42a61f88fbfdf002f6040fdb6e1b8b8477c99e7a781`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 09 Oct 2017 21:34:51 GMT
ADD file:4a0b4ab0f637224302bf3f7a7eedc5b75a404bc1188499ef2f98edb7ce44d0ed in / 
# Mon, 09 Oct 2017 21:34:51 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:16 GMT
MAINTAINER Adam Hawkins <hi@ahawkins.me>
# Mon, 09 Oct 2017 22:15:16 GMT
ENV THRIFT_VERSION=0.10.0
# Mon, 09 Oct 2017 22:18:02 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Mon, 09 Oct 2017 22:18:03 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:39e552a2b1f74a9985244528219d26fc1c27f1447a3d04e64b63bd70a4e68e2c`  
		Last Modified: Mon, 09 Oct 2017 21:44:19 GMT  
		Size: 38.1 MB (38103127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98039a56a27a312c2c10df1d0bc390784bf3b2d90ad8f0dda43e4be012a09c8b`  
		Last Modified: Mon, 09 Oct 2017 22:18:54 GMT  
		Size: 13.2 MB (13153948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.9`

```console
$ docker pull thrift@sha256:fc54e24baf8fffed06c6b47b1470fb922741077602e7f7f09371c9a27270994b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `thrift:0.9` - linux; amd64

```console
$ docker pull thrift@sha256:a0047bbff032ddde580845574ea3d938b92da9373ee6fbc942ae2c1491f084a2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50199464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2af6443c4a42e57d101bae43641f80d48fbbb94ec18a759e175bfed70822aa`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 09 Oct 2017 21:34:51 GMT
ADD file:4a0b4ab0f637224302bf3f7a7eedc5b75a404bc1188499ef2f98edb7ce44d0ed in / 
# Mon, 09 Oct 2017 21:34:51 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:12:04 GMT
MAINTAINER Adam Hawkins <adam@hawkins.io>
# Mon, 09 Oct 2017 22:12:04 GMT
ENV THRIFT_VERSION=0.9.3
# Mon, 09 Oct 2017 22:14:56 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Mon, 09 Oct 2017 22:14:57 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:39e552a2b1f74a9985244528219d26fc1c27f1447a3d04e64b63bd70a4e68e2c`  
		Last Modified: Mon, 09 Oct 2017 21:44:19 GMT  
		Size: 38.1 MB (38103127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9810b49729fafd4421e9f400da75b30a972acae09130ab7a791a038c6de05ec0`  
		Last Modified: Mon, 09 Oct 2017 22:18:31 GMT  
		Size: 12.1 MB (12096337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.9.3`

```console
$ docker pull thrift@sha256:fc54e24baf8fffed06c6b47b1470fb922741077602e7f7f09371c9a27270994b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `thrift:0.9.3` - linux; amd64

```console
$ docker pull thrift@sha256:a0047bbff032ddde580845574ea3d938b92da9373ee6fbc942ae2c1491f084a2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50199464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2af6443c4a42e57d101bae43641f80d48fbbb94ec18a759e175bfed70822aa`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 09 Oct 2017 21:34:51 GMT
ADD file:4a0b4ab0f637224302bf3f7a7eedc5b75a404bc1188499ef2f98edb7ce44d0ed in / 
# Mon, 09 Oct 2017 21:34:51 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:12:04 GMT
MAINTAINER Adam Hawkins <adam@hawkins.io>
# Mon, 09 Oct 2017 22:12:04 GMT
ENV THRIFT_VERSION=0.9.3
# Mon, 09 Oct 2017 22:14:56 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Mon, 09 Oct 2017 22:14:57 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:39e552a2b1f74a9985244528219d26fc1c27f1447a3d04e64b63bd70a4e68e2c`  
		Last Modified: Mon, 09 Oct 2017 21:44:19 GMT  
		Size: 38.1 MB (38103127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9810b49729fafd4421e9f400da75b30a972acae09130ab7a791a038c6de05ec0`  
		Last Modified: Mon, 09 Oct 2017 22:18:31 GMT  
		Size: 12.1 MB (12096337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:latest`

```console
$ docker pull thrift@sha256:6cfff8d58d440226a31cb17bb3a9d7b35dd00ede88a066684d08c2bff6b9dd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `thrift:latest` - linux; amd64

```console
$ docker pull thrift@sha256:2aa008aa88c46bba4275eb6d00bb497b12e1f4a36ce0d3b4c21b025a267024de
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51257075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d03e48a8adab43060fdd42a61f88fbfdf002f6040fdb6e1b8b8477c99e7a781`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 09 Oct 2017 21:34:51 GMT
ADD file:4a0b4ab0f637224302bf3f7a7eedc5b75a404bc1188499ef2f98edb7ce44d0ed in / 
# Mon, 09 Oct 2017 21:34:51 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:16 GMT
MAINTAINER Adam Hawkins <hi@ahawkins.me>
# Mon, 09 Oct 2017 22:15:16 GMT
ENV THRIFT_VERSION=0.10.0
# Mon, 09 Oct 2017 22:18:02 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Mon, 09 Oct 2017 22:18:03 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:39e552a2b1f74a9985244528219d26fc1c27f1447a3d04e64b63bd70a4e68e2c`  
		Last Modified: Mon, 09 Oct 2017 21:44:19 GMT  
		Size: 38.1 MB (38103127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98039a56a27a312c2c10df1d0bc390784bf3b2d90ad8f0dda43e4be012a09c8b`  
		Last Modified: Mon, 09 Oct 2017 22:18:54 GMT  
		Size: 13.2 MB (13153948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
