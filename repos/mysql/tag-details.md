<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.5`](#mysql55)
-	[`mysql:5.5.58`](#mysql5558)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.38`](#mysql5638)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.20`](#mysql5720)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.3`](#mysql803)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:eb9a3bca059ee178b5a69a2443462d156ff5b3d3f739c516b62d9d902ba49132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:11dfb1316b5fa189470b5eba2d3031e4ee702fd97912a3d1fc4dadafa6c90731
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144191752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fac85ee2c688e850040d38719a152ae3d290711441f60fd36f4fc29e799d0ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 09 Oct 2017 21:30:05 GMT
ADD file:55b071e2cfc3ea2f4bbf048d7d676e3c06a77a9a98d63f7af291f3decb495ec8 in / 
# Mon, 09 Oct 2017 21:30:05 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:41:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 09 Oct 2017 23:41:34 GMT
ENV GOSU_VERSION=1.7
# Mon, 09 Oct 2017 23:42:02 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Mon, 09 Oct 2017 23:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 10 Oct 2017 00:22:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:22:17 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 10 Oct 2017 00:22:54 GMT
ENV MYSQL_MAJOR=5.7
# Mon, 16 Oct 2017 19:10:27 GMT
ENV MYSQL_VERSION=5.7.20-1debian8
# Mon, 16 Oct 2017 19:10:28 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Mon, 16 Oct 2017 19:10:59 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Mon, 16 Oct 2017 19:10:59 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/mysql.conf.d/mysqld.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Mon, 16 Oct 2017 19:11:00 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Oct 2017 19:11:00 GMT
COPY file:5453fdbdb142b28e9aa4df64d5e1f42a740f018457cb1c65d113b947858ae314 in /usr/local/bin/ 
# Mon, 16 Oct 2017 19:11:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 16 Oct 2017 19:11:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2017 19:11:01 GMT
EXPOSE 3306/tcp
# Mon, 16 Oct 2017 19:11:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:85b1f47fba49da65256f07c8790542a3880e9216f9c491965040f35ce2c6ca7a`  
		Last Modified: Mon, 09 Oct 2017 21:36:40 GMT  
		Size: 52.6 MB (52595124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dc53f13a11bdd5a8c0406231db61e3bbcc80abd383c8d2aa025de18bc854f1`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095c8ae4182d531daaaab1ba53752c6ced9fe2b285e113c8f6ace3482fe35e14`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 1.3 MB (1302935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972f6b9a7de1ee8ae02473a098d3794336153353cf8cbbaf563ed6be7735a5f`  
		Last Modified: Mon, 09 Oct 2017 23:50:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b199048e1dac21056ab6d1bcc4ff6777aa744394e028220fe5a7f3969b2556d`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 10.7 MB (10711007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159de3cf101e0a10be9c44f65c56d4d6736cf0df58e6da23644a8c5807abdacb`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 19.8 KB (19791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff639f4e6d90459976593914c5ae23a5d3a3b4268c77a7dce16b05ace12dff7`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d7a93157e8ed7c1bf354b7719b84dae0155a54966c45ad827604ce621966a`  
		Last Modified: Mon, 16 Oct 2017 19:17:44 GMT  
		Size: 79.6 MB (79556668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5afe5b139c57a2fd6956d728f02bcfed357755f955adfd105dbf778570c841`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c916ff94d5c0d2a773f95650e78095417845db669525f396f93cfdb8e11622`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 2.7 KB (2736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e934932d4d2512ea0fceb79e43baec06d6eb9e552053da5837a01fbc3a4c1186`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.5`

```console
$ docker pull mysql@sha256:041ca744802be04119d31813cd7f26072a70451f321d3fe74c12458e3fdae580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.5` - linux; amd64

```console
$ docker pull mysql@sha256:1a58414c8127865a1be548a414934a889053ada95906919e949b64d630f01fef
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90190500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8539f89064c27dfb723eb2a7972b78b293243a635dea00cf4089a20a7ea92a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 09 Oct 2017 21:30:05 GMT
ADD file:55b071e2cfc3ea2f4bbf048d7d676e3c06a77a9a98d63f7af291f3decb495ec8 in / 
# Mon, 09 Oct 2017 21:30:05 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:41:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 09 Oct 2017 23:41:34 GMT
ENV GOSU_VERSION=1.7
# Mon, 09 Oct 2017 23:42:02 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Mon, 09 Oct 2017 23:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 10 Oct 2017 00:24:57 GMT
RUN apt-get update && apt-get install -y perl --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:25:12 GMT
RUN apt-get update && apt-get install -y libaio1 pwgen && rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:25:14 GMT
ENV MYSQL_MAJOR=5.5
# Mon, 16 Oct 2017 19:12:07 GMT
ENV MYSQL_VERSION=5.5.58
# Mon, 16 Oct 2017 19:13:11 GMT
RUN apt-get update && apt-get install -y ca-certificates wget --no-install-recommends && rm -rf /var/lib/apt/lists/* 	&& wget "https://cdn.mysql.com/Downloads/MySQL-$MYSQL_MAJOR/mysql-$MYSQL_VERSION-linux-glibc2.12-x86_64.tar.gz" -O mysql.tar.gz 	&& wget "https://cdn.mysql.com/Downloads/MySQL-$MYSQL_MAJOR/mysql-$MYSQL_VERSION-linux-glibc2.12-x86_64.tar.gz.asc" -O mysql.tar.gz.asc 	&& apt-get purge -y --auto-remove ca-certificates wget 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5 	&& gpg --batch --verify mysql.tar.gz.asc mysql.tar.gz 	&& rm -r "$GNUPGHOME" mysql.tar.gz.asc 	&& mkdir /usr/local/mysql 	&& tar -xzf mysql.tar.gz -C /usr/local/mysql --strip-components=1 	&& rm mysql.tar.gz 	&& rm -rf /usr/local/mysql/mysql-test /usr/local/mysql/sql-bench 	&& rm -rf /usr/local/mysql/bin/*-debug /usr/local/mysql/bin/*_embedded 	&& find /usr/local/mysql -type f -name "*.a" -delete 	&& apt-get update && apt-get install -y binutils && rm -rf /var/lib/apt/lists/* 	&& { find /usr/local/mysql -type f -executable -exec strip --strip-all '{}' + || true; } 	&& apt-get purge -y --auto-remove binutils
# Mon, 16 Oct 2017 19:13:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/mysql/bin:/usr/local/mysql/scripts
# Mon, 16 Oct 2017 19:13:11 GMT
RUN mkdir -p /etc/mysql/conf.d 	&& { 		echo '[mysqld]'; 		echo 'skip-host-cache'; 		echo 'skip-name-resolve'; 		echo 'datadir = /var/lib/mysql'; 		echo '!includedir /etc/mysql/conf.d/'; 	} > /etc/mysql/my.cnf
# Mon, 16 Oct 2017 19:13:12 GMT
RUN mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Mon, 16 Oct 2017 19:13:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Oct 2017 19:13:13 GMT
COPY file:0dfb1be3ff2b71842e1c4ae21d0e9f4b9a103296130d270c5072557604f5ca73 in /usr/local/bin/ 
# Mon, 16 Oct 2017 19:13:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 16 Oct 2017 19:13:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2017 19:13:14 GMT
EXPOSE 3306/tcp
# Mon, 16 Oct 2017 19:13:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:85b1f47fba49da65256f07c8790542a3880e9216f9c491965040f35ce2c6ca7a`  
		Last Modified: Mon, 09 Oct 2017 21:36:40 GMT  
		Size: 52.6 MB (52595124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dc53f13a11bdd5a8c0406231db61e3bbcc80abd383c8d2aa025de18bc854f1`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095c8ae4182d531daaaab1ba53752c6ced9fe2b285e113c8f6ace3482fe35e14`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 1.3 MB (1302935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972f6b9a7de1ee8ae02473a098d3794336153353cf8cbbaf563ed6be7735a5f`  
		Last Modified: Mon, 09 Oct 2017 23:50:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ae57f3d01d8aad375cdfed9c4f45fb563f392badd89afb25b97882ad082471`  
		Last Modified: Tue, 10 Oct 2017 00:29:30 GMT  
		Size: 8.4 MB (8441038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72384e4507532cfa1cb685002ed60449f3fb73835de041860a268b1126ee39e`  
		Last Modified: Tue, 10 Oct 2017 00:29:28 GMT  
		Size: 301.9 KB (301943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf214e4570f06cad552ef6106b1d44c839e3cf16fa38b2dad3f66ba1d2d889c`  
		Last Modified: Mon, 16 Oct 2017 19:18:51 GMT  
		Size: 27.5 MB (27544085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19d2b4b74fe16a64af60e3673674c6cd7c6b3b3b49a17c06bb31563c5dfc16b`  
		Last Modified: Mon, 16 Oct 2017 19:18:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81272c77039d6105af989e412e4c5fc7d197f4d627faf09cda77aebef3a5793f`  
		Last Modified: Mon, 16 Oct 2017 19:18:48 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deab12c58eae25bc045d3144492db01230b9c212f412a098eeaf569884de38cc`  
		Last Modified: Mon, 16 Oct 2017 19:18:48 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0830a21cf3537dcf7bb5db8340e7e5ea61f5ce20228d820d65439e336b5bff3`  
		Last Modified: Mon, 16 Oct 2017 19:18:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.5.58`

```console
$ docker pull mysql@sha256:041ca744802be04119d31813cd7f26072a70451f321d3fe74c12458e3fdae580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.5.58` - linux; amd64

```console
$ docker pull mysql@sha256:1a58414c8127865a1be548a414934a889053ada95906919e949b64d630f01fef
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90190500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8539f89064c27dfb723eb2a7972b78b293243a635dea00cf4089a20a7ea92a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 09 Oct 2017 21:30:05 GMT
ADD file:55b071e2cfc3ea2f4bbf048d7d676e3c06a77a9a98d63f7af291f3decb495ec8 in / 
# Mon, 09 Oct 2017 21:30:05 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:41:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 09 Oct 2017 23:41:34 GMT
ENV GOSU_VERSION=1.7
# Mon, 09 Oct 2017 23:42:02 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Mon, 09 Oct 2017 23:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 10 Oct 2017 00:24:57 GMT
RUN apt-get update && apt-get install -y perl --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:25:12 GMT
RUN apt-get update && apt-get install -y libaio1 pwgen && rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:25:14 GMT
ENV MYSQL_MAJOR=5.5
# Mon, 16 Oct 2017 19:12:07 GMT
ENV MYSQL_VERSION=5.5.58
# Mon, 16 Oct 2017 19:13:11 GMT
RUN apt-get update && apt-get install -y ca-certificates wget --no-install-recommends && rm -rf /var/lib/apt/lists/* 	&& wget "https://cdn.mysql.com/Downloads/MySQL-$MYSQL_MAJOR/mysql-$MYSQL_VERSION-linux-glibc2.12-x86_64.tar.gz" -O mysql.tar.gz 	&& wget "https://cdn.mysql.com/Downloads/MySQL-$MYSQL_MAJOR/mysql-$MYSQL_VERSION-linux-glibc2.12-x86_64.tar.gz.asc" -O mysql.tar.gz.asc 	&& apt-get purge -y --auto-remove ca-certificates wget 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5 	&& gpg --batch --verify mysql.tar.gz.asc mysql.tar.gz 	&& rm -r "$GNUPGHOME" mysql.tar.gz.asc 	&& mkdir /usr/local/mysql 	&& tar -xzf mysql.tar.gz -C /usr/local/mysql --strip-components=1 	&& rm mysql.tar.gz 	&& rm -rf /usr/local/mysql/mysql-test /usr/local/mysql/sql-bench 	&& rm -rf /usr/local/mysql/bin/*-debug /usr/local/mysql/bin/*_embedded 	&& find /usr/local/mysql -type f -name "*.a" -delete 	&& apt-get update && apt-get install -y binutils && rm -rf /var/lib/apt/lists/* 	&& { find /usr/local/mysql -type f -executable -exec strip --strip-all '{}' + || true; } 	&& apt-get purge -y --auto-remove binutils
# Mon, 16 Oct 2017 19:13:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/mysql/bin:/usr/local/mysql/scripts
# Mon, 16 Oct 2017 19:13:11 GMT
RUN mkdir -p /etc/mysql/conf.d 	&& { 		echo '[mysqld]'; 		echo 'skip-host-cache'; 		echo 'skip-name-resolve'; 		echo 'datadir = /var/lib/mysql'; 		echo '!includedir /etc/mysql/conf.d/'; 	} > /etc/mysql/my.cnf
# Mon, 16 Oct 2017 19:13:12 GMT
RUN mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Mon, 16 Oct 2017 19:13:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Oct 2017 19:13:13 GMT
COPY file:0dfb1be3ff2b71842e1c4ae21d0e9f4b9a103296130d270c5072557604f5ca73 in /usr/local/bin/ 
# Mon, 16 Oct 2017 19:13:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 16 Oct 2017 19:13:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2017 19:13:14 GMT
EXPOSE 3306/tcp
# Mon, 16 Oct 2017 19:13:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:85b1f47fba49da65256f07c8790542a3880e9216f9c491965040f35ce2c6ca7a`  
		Last Modified: Mon, 09 Oct 2017 21:36:40 GMT  
		Size: 52.6 MB (52595124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dc53f13a11bdd5a8c0406231db61e3bbcc80abd383c8d2aa025de18bc854f1`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095c8ae4182d531daaaab1ba53752c6ced9fe2b285e113c8f6ace3482fe35e14`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 1.3 MB (1302935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972f6b9a7de1ee8ae02473a098d3794336153353cf8cbbaf563ed6be7735a5f`  
		Last Modified: Mon, 09 Oct 2017 23:50:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ae57f3d01d8aad375cdfed9c4f45fb563f392badd89afb25b97882ad082471`  
		Last Modified: Tue, 10 Oct 2017 00:29:30 GMT  
		Size: 8.4 MB (8441038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72384e4507532cfa1cb685002ed60449f3fb73835de041860a268b1126ee39e`  
		Last Modified: Tue, 10 Oct 2017 00:29:28 GMT  
		Size: 301.9 KB (301943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf214e4570f06cad552ef6106b1d44c839e3cf16fa38b2dad3f66ba1d2d889c`  
		Last Modified: Mon, 16 Oct 2017 19:18:51 GMT  
		Size: 27.5 MB (27544085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19d2b4b74fe16a64af60e3673674c6cd7c6b3b3b49a17c06bb31563c5dfc16b`  
		Last Modified: Mon, 16 Oct 2017 19:18:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81272c77039d6105af989e412e4c5fc7d197f4d627faf09cda77aebef3a5793f`  
		Last Modified: Mon, 16 Oct 2017 19:18:48 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deab12c58eae25bc045d3144492db01230b9c212f412a098eeaf569884de38cc`  
		Last Modified: Mon, 16 Oct 2017 19:18:48 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0830a21cf3537dcf7bb5db8340e7e5ea61f5ce20228d820d65439e336b5bff3`  
		Last Modified: Mon, 16 Oct 2017 19:18:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:8d69af5de8ad5a0a598a0632ebc930b42721eb7af0bff0239a566f5ff8edb9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:230c93744ed86f68535db7a3cf971ca92862679dc6b837ff3601e7a524fb45b7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105052696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0b301e2e86b40d4906e38c7a5948648d96a844c6ceb398c73a9f525eea53a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 09 Oct 2017 21:30:05 GMT
ADD file:55b071e2cfc3ea2f4bbf048d7d676e3c06a77a9a98d63f7af291f3decb495ec8 in / 
# Mon, 09 Oct 2017 21:30:05 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:41:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 09 Oct 2017 23:41:34 GMT
ENV GOSU_VERSION=1.7
# Mon, 09 Oct 2017 23:42:02 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Mon, 09 Oct 2017 23:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 10 Oct 2017 00:23:55 GMT
RUN apt-get update && apt-get install -y perl pwgen --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:24:01 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 10 Oct 2017 00:24:04 GMT
ENV MYSQL_MAJOR=5.6
# Mon, 16 Oct 2017 19:11:13 GMT
ENV MYSQL_VERSION=5.6.38-1debian8
# Mon, 16 Oct 2017 19:11:14 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Mon, 16 Oct 2017 19:11:39 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Mon, 16 Oct 2017 19:11:42 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/my.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Mon, 16 Oct 2017 19:11:42 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Oct 2017 19:11:43 GMT
COPY file:b4e423a0d95974d5269d37431aafc0c69cb304dc09ab3f496dbcfdfbc2dbd818 in /usr/local/bin/ 
# Mon, 16 Oct 2017 19:11:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 16 Oct 2017 19:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2017 19:11:49 GMT
EXPOSE 3306/tcp
# Mon, 16 Oct 2017 19:11:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:85b1f47fba49da65256f07c8790542a3880e9216f9c491965040f35ce2c6ca7a`  
		Last Modified: Mon, 09 Oct 2017 21:36:40 GMT  
		Size: 52.6 MB (52595124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dc53f13a11bdd5a8c0406231db61e3bbcc80abd383c8d2aa025de18bc854f1`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095c8ae4182d531daaaab1ba53752c6ced9fe2b285e113c8f6ace3482fe35e14`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 1.3 MB (1302935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972f6b9a7de1ee8ae02473a098d3794336153353cf8cbbaf563ed6be7735a5f`  
		Last Modified: Mon, 09 Oct 2017 23:50:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11a67190c24ce790deba7c2bc760c74f69f26ed50d88992fd80ce9c52a1825b`  
		Last Modified: Tue, 10 Oct 2017 00:28:43 GMT  
		Size: 8.5 MB (8460816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908252bea0ceac590d3aafbc1d2618fc3dc5536d25863d731a560411d0e40076`  
		Last Modified: Tue, 10 Oct 2017 00:28:40 GMT  
		Size: 19.8 KB (19791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870c4f4d5e5c2da375b1a02f31bdce9027b45b7eda2e1aa4ce2af98156619d89`  
		Last Modified: Mon, 16 Oct 2017 19:18:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cecf05ad8c7516833aaa3b557514fdbfda3f298d736e5db9741f3bd0bda928`  
		Last Modified: Mon, 16 Oct 2017 19:18:27 GMT  
		Size: 42.7 MB (42668026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39efa0847de2f31c7f480cb1e6c1226702412b06d7fdcd036c5437a4992913a`  
		Last Modified: Mon, 16 Oct 2017 19:18:22 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c87208d7a4c83c520429f30755d1fcfdba45a3c8c1fd48e57b2ad967070da8`  
		Last Modified: Mon, 16 Oct 2017 19:18:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d34f0a09719df514630f4cb7566264894bac888e8dbf523aa2bf11e973a444f`  
		Last Modified: Mon, 16 Oct 2017 19:18:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.38`

```console
$ docker pull mysql@sha256:8d69af5de8ad5a0a598a0632ebc930b42721eb7af0bff0239a566f5ff8edb9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.38` - linux; amd64

```console
$ docker pull mysql@sha256:230c93744ed86f68535db7a3cf971ca92862679dc6b837ff3601e7a524fb45b7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105052696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0b301e2e86b40d4906e38c7a5948648d96a844c6ceb398c73a9f525eea53a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 09 Oct 2017 21:30:05 GMT
ADD file:55b071e2cfc3ea2f4bbf048d7d676e3c06a77a9a98d63f7af291f3decb495ec8 in / 
# Mon, 09 Oct 2017 21:30:05 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:41:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 09 Oct 2017 23:41:34 GMT
ENV GOSU_VERSION=1.7
# Mon, 09 Oct 2017 23:42:02 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Mon, 09 Oct 2017 23:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 10 Oct 2017 00:23:55 GMT
RUN apt-get update && apt-get install -y perl pwgen --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:24:01 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 10 Oct 2017 00:24:04 GMT
ENV MYSQL_MAJOR=5.6
# Mon, 16 Oct 2017 19:11:13 GMT
ENV MYSQL_VERSION=5.6.38-1debian8
# Mon, 16 Oct 2017 19:11:14 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Mon, 16 Oct 2017 19:11:39 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Mon, 16 Oct 2017 19:11:42 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/my.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Mon, 16 Oct 2017 19:11:42 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Oct 2017 19:11:43 GMT
COPY file:b4e423a0d95974d5269d37431aafc0c69cb304dc09ab3f496dbcfdfbc2dbd818 in /usr/local/bin/ 
# Mon, 16 Oct 2017 19:11:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 16 Oct 2017 19:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2017 19:11:49 GMT
EXPOSE 3306/tcp
# Mon, 16 Oct 2017 19:11:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:85b1f47fba49da65256f07c8790542a3880e9216f9c491965040f35ce2c6ca7a`  
		Last Modified: Mon, 09 Oct 2017 21:36:40 GMT  
		Size: 52.6 MB (52595124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dc53f13a11bdd5a8c0406231db61e3bbcc80abd383c8d2aa025de18bc854f1`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095c8ae4182d531daaaab1ba53752c6ced9fe2b285e113c8f6ace3482fe35e14`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 1.3 MB (1302935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972f6b9a7de1ee8ae02473a098d3794336153353cf8cbbaf563ed6be7735a5f`  
		Last Modified: Mon, 09 Oct 2017 23:50:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11a67190c24ce790deba7c2bc760c74f69f26ed50d88992fd80ce9c52a1825b`  
		Last Modified: Tue, 10 Oct 2017 00:28:43 GMT  
		Size: 8.5 MB (8460816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908252bea0ceac590d3aafbc1d2618fc3dc5536d25863d731a560411d0e40076`  
		Last Modified: Tue, 10 Oct 2017 00:28:40 GMT  
		Size: 19.8 KB (19791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870c4f4d5e5c2da375b1a02f31bdce9027b45b7eda2e1aa4ce2af98156619d89`  
		Last Modified: Mon, 16 Oct 2017 19:18:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cecf05ad8c7516833aaa3b557514fdbfda3f298d736e5db9741f3bd0bda928`  
		Last Modified: Mon, 16 Oct 2017 19:18:27 GMT  
		Size: 42.7 MB (42668026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39efa0847de2f31c7f480cb1e6c1226702412b06d7fdcd036c5437a4992913a`  
		Last Modified: Mon, 16 Oct 2017 19:18:22 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c87208d7a4c83c520429f30755d1fcfdba45a3c8c1fd48e57b2ad967070da8`  
		Last Modified: Mon, 16 Oct 2017 19:18:22 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d34f0a09719df514630f4cb7566264894bac888e8dbf523aa2bf11e973a444f`  
		Last Modified: Mon, 16 Oct 2017 19:18:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:eb9a3bca059ee178b5a69a2443462d156ff5b3d3f739c516b62d9d902ba49132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:11dfb1316b5fa189470b5eba2d3031e4ee702fd97912a3d1fc4dadafa6c90731
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144191752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fac85ee2c688e850040d38719a152ae3d290711441f60fd36f4fc29e799d0ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 09 Oct 2017 21:30:05 GMT
ADD file:55b071e2cfc3ea2f4bbf048d7d676e3c06a77a9a98d63f7af291f3decb495ec8 in / 
# Mon, 09 Oct 2017 21:30:05 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:41:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 09 Oct 2017 23:41:34 GMT
ENV GOSU_VERSION=1.7
# Mon, 09 Oct 2017 23:42:02 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Mon, 09 Oct 2017 23:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 10 Oct 2017 00:22:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:22:17 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 10 Oct 2017 00:22:54 GMT
ENV MYSQL_MAJOR=5.7
# Mon, 16 Oct 2017 19:10:27 GMT
ENV MYSQL_VERSION=5.7.20-1debian8
# Mon, 16 Oct 2017 19:10:28 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Mon, 16 Oct 2017 19:10:59 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Mon, 16 Oct 2017 19:10:59 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/mysql.conf.d/mysqld.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Mon, 16 Oct 2017 19:11:00 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Oct 2017 19:11:00 GMT
COPY file:5453fdbdb142b28e9aa4df64d5e1f42a740f018457cb1c65d113b947858ae314 in /usr/local/bin/ 
# Mon, 16 Oct 2017 19:11:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 16 Oct 2017 19:11:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2017 19:11:01 GMT
EXPOSE 3306/tcp
# Mon, 16 Oct 2017 19:11:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:85b1f47fba49da65256f07c8790542a3880e9216f9c491965040f35ce2c6ca7a`  
		Last Modified: Mon, 09 Oct 2017 21:36:40 GMT  
		Size: 52.6 MB (52595124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dc53f13a11bdd5a8c0406231db61e3bbcc80abd383c8d2aa025de18bc854f1`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095c8ae4182d531daaaab1ba53752c6ced9fe2b285e113c8f6ace3482fe35e14`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 1.3 MB (1302935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972f6b9a7de1ee8ae02473a098d3794336153353cf8cbbaf563ed6be7735a5f`  
		Last Modified: Mon, 09 Oct 2017 23:50:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b199048e1dac21056ab6d1bcc4ff6777aa744394e028220fe5a7f3969b2556d`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 10.7 MB (10711007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159de3cf101e0a10be9c44f65c56d4d6736cf0df58e6da23644a8c5807abdacb`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 19.8 KB (19791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff639f4e6d90459976593914c5ae23a5d3a3b4268c77a7dce16b05ace12dff7`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d7a93157e8ed7c1bf354b7719b84dae0155a54966c45ad827604ce621966a`  
		Last Modified: Mon, 16 Oct 2017 19:17:44 GMT  
		Size: 79.6 MB (79556668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5afe5b139c57a2fd6956d728f02bcfed357755f955adfd105dbf778570c841`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c916ff94d5c0d2a773f95650e78095417845db669525f396f93cfdb8e11622`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 2.7 KB (2736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e934932d4d2512ea0fceb79e43baec06d6eb9e552053da5837a01fbc3a4c1186`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.20`

```console
$ docker pull mysql@sha256:eb9a3bca059ee178b5a69a2443462d156ff5b3d3f739c516b62d9d902ba49132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.20` - linux; amd64

```console
$ docker pull mysql@sha256:11dfb1316b5fa189470b5eba2d3031e4ee702fd97912a3d1fc4dadafa6c90731
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144191752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fac85ee2c688e850040d38719a152ae3d290711441f60fd36f4fc29e799d0ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 09 Oct 2017 21:30:05 GMT
ADD file:55b071e2cfc3ea2f4bbf048d7d676e3c06a77a9a98d63f7af291f3decb495ec8 in / 
# Mon, 09 Oct 2017 21:30:05 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:41:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 09 Oct 2017 23:41:34 GMT
ENV GOSU_VERSION=1.7
# Mon, 09 Oct 2017 23:42:02 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Mon, 09 Oct 2017 23:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 10 Oct 2017 00:22:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:22:17 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 10 Oct 2017 00:22:54 GMT
ENV MYSQL_MAJOR=5.7
# Mon, 16 Oct 2017 19:10:27 GMT
ENV MYSQL_VERSION=5.7.20-1debian8
# Mon, 16 Oct 2017 19:10:28 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Mon, 16 Oct 2017 19:10:59 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Mon, 16 Oct 2017 19:10:59 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/mysql.conf.d/mysqld.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Mon, 16 Oct 2017 19:11:00 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Oct 2017 19:11:00 GMT
COPY file:5453fdbdb142b28e9aa4df64d5e1f42a740f018457cb1c65d113b947858ae314 in /usr/local/bin/ 
# Mon, 16 Oct 2017 19:11:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 16 Oct 2017 19:11:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2017 19:11:01 GMT
EXPOSE 3306/tcp
# Mon, 16 Oct 2017 19:11:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:85b1f47fba49da65256f07c8790542a3880e9216f9c491965040f35ce2c6ca7a`  
		Last Modified: Mon, 09 Oct 2017 21:36:40 GMT  
		Size: 52.6 MB (52595124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dc53f13a11bdd5a8c0406231db61e3bbcc80abd383c8d2aa025de18bc854f1`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095c8ae4182d531daaaab1ba53752c6ced9fe2b285e113c8f6ace3482fe35e14`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 1.3 MB (1302935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972f6b9a7de1ee8ae02473a098d3794336153353cf8cbbaf563ed6be7735a5f`  
		Last Modified: Mon, 09 Oct 2017 23:50:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b199048e1dac21056ab6d1bcc4ff6777aa744394e028220fe5a7f3969b2556d`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 10.7 MB (10711007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159de3cf101e0a10be9c44f65c56d4d6736cf0df58e6da23644a8c5807abdacb`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 19.8 KB (19791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff639f4e6d90459976593914c5ae23a5d3a3b4268c77a7dce16b05ace12dff7`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d7a93157e8ed7c1bf354b7719b84dae0155a54966c45ad827604ce621966a`  
		Last Modified: Mon, 16 Oct 2017 19:17:44 GMT  
		Size: 79.6 MB (79556668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5afe5b139c57a2fd6956d728f02bcfed357755f955adfd105dbf778570c841`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c916ff94d5c0d2a773f95650e78095417845db669525f396f93cfdb8e11622`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 2.7 KB (2736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e934932d4d2512ea0fceb79e43baec06d6eb9e552053da5837a01fbc3a4c1186`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:bc8c4b1dc9b7033253b5b5b8f7ac30af46a6ba49a362c84e01f86349ba68a093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:8a86b5aa1439de4e28bc17e3e7758c2d5e7504c9fbd0e46049f241422470c387
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112861436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f4698df813756da1fa14e08b17a1cde31e26087d6dd686d4159d59350d98cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 09 Oct 2017 21:30:05 GMT
ADD file:55b071e2cfc3ea2f4bbf048d7d676e3c06a77a9a98d63f7af291f3decb495ec8 in / 
# Mon, 09 Oct 2017 21:30:05 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:41:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 09 Oct 2017 23:41:34 GMT
ENV GOSU_VERSION=1.7
# Mon, 09 Oct 2017 23:42:02 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Mon, 09 Oct 2017 23:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 10 Oct 2017 00:22:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:22:17 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 10 Oct 2017 00:22:19 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 10 Oct 2017 00:22:19 GMT
ENV MYSQL_VERSION=8.0.3-rc-1debian8
# Tue, 10 Oct 2017 00:22:20 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 10 Oct 2017 00:22:40 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client-core="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 10 Oct 2017 00:22:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 10 Oct 2017 00:22:41 GMT
COPY dir:110dcf1221c1f9432c68c32a2465ef0b40994f401d5fae0b0de80025bcf839a5 in /etc/mysql/ 
# Tue, 10 Oct 2017 00:22:41 GMT
COPY file:5453fdbdb142b28e9aa4df64d5e1f42a740f018457cb1c65d113b947858ae314 in /usr/local/bin/ 
# Tue, 10 Oct 2017 00:22:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 10 Oct 2017 00:22:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Oct 2017 00:22:42 GMT
EXPOSE 3306/tcp
# Tue, 10 Oct 2017 00:22:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:85b1f47fba49da65256f07c8790542a3880e9216f9c491965040f35ce2c6ca7a`  
		Last Modified: Mon, 09 Oct 2017 21:36:40 GMT  
		Size: 52.6 MB (52595124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dc53f13a11bdd5a8c0406231db61e3bbcc80abd383c8d2aa025de18bc854f1`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095c8ae4182d531daaaab1ba53752c6ced9fe2b285e113c8f6ace3482fe35e14`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 1.3 MB (1302935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972f6b9a7de1ee8ae02473a098d3794336153353cf8cbbaf563ed6be7735a5f`  
		Last Modified: Mon, 09 Oct 2017 23:50:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b199048e1dac21056ab6d1bcc4ff6777aa744394e028220fe5a7f3969b2556d`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 10.7 MB (10711007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159de3cf101e0a10be9c44f65c56d4d6736cf0df58e6da23644a8c5807abdacb`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 19.8 KB (19791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f475e9e4797484105a6f6f3385da586a50ccf4aed1fef0dcac1319f7a135d0`  
		Last Modified: Tue, 10 Oct 2017 00:26:43 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441312cc0ec5c9566f72ae82ac7ea07ddfb84c0539abfc5860e052b30463ac28`  
		Last Modified: Tue, 10 Oct 2017 00:26:52 GMT  
		Size: 48.2 MB (48226410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cf4618860df66ef55d9bae898cf329fb4e362d230b841fe68bc77d252de19d`  
		Last Modified: Tue, 10 Oct 2017 00:26:44 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70412d5bf27077eb8825b0b59b3c3f370b09ac08d3e4a404531f3a495e4aaf7d`  
		Last Modified: Tue, 10 Oct 2017 00:26:43 GMT  
		Size: 2.7 KB (2733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6972ae417158b9d16d9c41b868540ec3c8741e5f9bca6d21f31eeefced4f05ad`  
		Last Modified: Tue, 10 Oct 2017 00:26:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:bc8c4b1dc9b7033253b5b5b8f7ac30af46a6ba49a362c84e01f86349ba68a093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:8a86b5aa1439de4e28bc17e3e7758c2d5e7504c9fbd0e46049f241422470c387
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112861436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f4698df813756da1fa14e08b17a1cde31e26087d6dd686d4159d59350d98cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 09 Oct 2017 21:30:05 GMT
ADD file:55b071e2cfc3ea2f4bbf048d7d676e3c06a77a9a98d63f7af291f3decb495ec8 in / 
# Mon, 09 Oct 2017 21:30:05 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:41:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 09 Oct 2017 23:41:34 GMT
ENV GOSU_VERSION=1.7
# Mon, 09 Oct 2017 23:42:02 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Mon, 09 Oct 2017 23:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 10 Oct 2017 00:22:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:22:17 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 10 Oct 2017 00:22:19 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 10 Oct 2017 00:22:19 GMT
ENV MYSQL_VERSION=8.0.3-rc-1debian8
# Tue, 10 Oct 2017 00:22:20 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 10 Oct 2017 00:22:40 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client-core="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 10 Oct 2017 00:22:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 10 Oct 2017 00:22:41 GMT
COPY dir:110dcf1221c1f9432c68c32a2465ef0b40994f401d5fae0b0de80025bcf839a5 in /etc/mysql/ 
# Tue, 10 Oct 2017 00:22:41 GMT
COPY file:5453fdbdb142b28e9aa4df64d5e1f42a740f018457cb1c65d113b947858ae314 in /usr/local/bin/ 
# Tue, 10 Oct 2017 00:22:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 10 Oct 2017 00:22:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Oct 2017 00:22:42 GMT
EXPOSE 3306/tcp
# Tue, 10 Oct 2017 00:22:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:85b1f47fba49da65256f07c8790542a3880e9216f9c491965040f35ce2c6ca7a`  
		Last Modified: Mon, 09 Oct 2017 21:36:40 GMT  
		Size: 52.6 MB (52595124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dc53f13a11bdd5a8c0406231db61e3bbcc80abd383c8d2aa025de18bc854f1`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095c8ae4182d531daaaab1ba53752c6ced9fe2b285e113c8f6ace3482fe35e14`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 1.3 MB (1302935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972f6b9a7de1ee8ae02473a098d3794336153353cf8cbbaf563ed6be7735a5f`  
		Last Modified: Mon, 09 Oct 2017 23:50:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b199048e1dac21056ab6d1bcc4ff6777aa744394e028220fe5a7f3969b2556d`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 10.7 MB (10711007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159de3cf101e0a10be9c44f65c56d4d6736cf0df58e6da23644a8c5807abdacb`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 19.8 KB (19791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f475e9e4797484105a6f6f3385da586a50ccf4aed1fef0dcac1319f7a135d0`  
		Last Modified: Tue, 10 Oct 2017 00:26:43 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441312cc0ec5c9566f72ae82ac7ea07ddfb84c0539abfc5860e052b30463ac28`  
		Last Modified: Tue, 10 Oct 2017 00:26:52 GMT  
		Size: 48.2 MB (48226410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cf4618860df66ef55d9bae898cf329fb4e362d230b841fe68bc77d252de19d`  
		Last Modified: Tue, 10 Oct 2017 00:26:44 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70412d5bf27077eb8825b0b59b3c3f370b09ac08d3e4a404531f3a495e4aaf7d`  
		Last Modified: Tue, 10 Oct 2017 00:26:43 GMT  
		Size: 2.7 KB (2733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6972ae417158b9d16d9c41b868540ec3c8741e5f9bca6d21f31eeefced4f05ad`  
		Last Modified: Tue, 10 Oct 2017 00:26:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.3`

```console
$ docker pull mysql@sha256:bc8c4b1dc9b7033253b5b5b8f7ac30af46a6ba49a362c84e01f86349ba68a093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.3` - linux; amd64

```console
$ docker pull mysql@sha256:8a86b5aa1439de4e28bc17e3e7758c2d5e7504c9fbd0e46049f241422470c387
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112861436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f4698df813756da1fa14e08b17a1cde31e26087d6dd686d4159d59350d98cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 09 Oct 2017 21:30:05 GMT
ADD file:55b071e2cfc3ea2f4bbf048d7d676e3c06a77a9a98d63f7af291f3decb495ec8 in / 
# Mon, 09 Oct 2017 21:30:05 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:41:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 09 Oct 2017 23:41:34 GMT
ENV GOSU_VERSION=1.7
# Mon, 09 Oct 2017 23:42:02 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Mon, 09 Oct 2017 23:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 10 Oct 2017 00:22:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:22:17 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 10 Oct 2017 00:22:19 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 10 Oct 2017 00:22:19 GMT
ENV MYSQL_VERSION=8.0.3-rc-1debian8
# Tue, 10 Oct 2017 00:22:20 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 10 Oct 2017 00:22:40 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client-core="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 10 Oct 2017 00:22:40 GMT
VOLUME [/var/lib/mysql]
# Tue, 10 Oct 2017 00:22:41 GMT
COPY dir:110dcf1221c1f9432c68c32a2465ef0b40994f401d5fae0b0de80025bcf839a5 in /etc/mysql/ 
# Tue, 10 Oct 2017 00:22:41 GMT
COPY file:5453fdbdb142b28e9aa4df64d5e1f42a740f018457cb1c65d113b947858ae314 in /usr/local/bin/ 
# Tue, 10 Oct 2017 00:22:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 10 Oct 2017 00:22:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Oct 2017 00:22:42 GMT
EXPOSE 3306/tcp
# Tue, 10 Oct 2017 00:22:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:85b1f47fba49da65256f07c8790542a3880e9216f9c491965040f35ce2c6ca7a`  
		Last Modified: Mon, 09 Oct 2017 21:36:40 GMT  
		Size: 52.6 MB (52595124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dc53f13a11bdd5a8c0406231db61e3bbcc80abd383c8d2aa025de18bc854f1`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095c8ae4182d531daaaab1ba53752c6ced9fe2b285e113c8f6ace3482fe35e14`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 1.3 MB (1302935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972f6b9a7de1ee8ae02473a098d3794336153353cf8cbbaf563ed6be7735a5f`  
		Last Modified: Mon, 09 Oct 2017 23:50:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b199048e1dac21056ab6d1bcc4ff6777aa744394e028220fe5a7f3969b2556d`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 10.7 MB (10711007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159de3cf101e0a10be9c44f65c56d4d6736cf0df58e6da23644a8c5807abdacb`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 19.8 KB (19791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f475e9e4797484105a6f6f3385da586a50ccf4aed1fef0dcac1319f7a135d0`  
		Last Modified: Tue, 10 Oct 2017 00:26:43 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441312cc0ec5c9566f72ae82ac7ea07ddfb84c0539abfc5860e052b30463ac28`  
		Last Modified: Tue, 10 Oct 2017 00:26:52 GMT  
		Size: 48.2 MB (48226410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cf4618860df66ef55d9bae898cf329fb4e362d230b841fe68bc77d252de19d`  
		Last Modified: Tue, 10 Oct 2017 00:26:44 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70412d5bf27077eb8825b0b59b3c3f370b09ac08d3e4a404531f3a495e4aaf7d`  
		Last Modified: Tue, 10 Oct 2017 00:26:43 GMT  
		Size: 2.7 KB (2733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6972ae417158b9d16d9c41b868540ec3c8741e5f9bca6d21f31eeefced4f05ad`  
		Last Modified: Tue, 10 Oct 2017 00:26:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:eb9a3bca059ee178b5a69a2443462d156ff5b3d3f739c516b62d9d902ba49132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:11dfb1316b5fa189470b5eba2d3031e4ee702fd97912a3d1fc4dadafa6c90731
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144191752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fac85ee2c688e850040d38719a152ae3d290711441f60fd36f4fc29e799d0ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 09 Oct 2017 21:30:05 GMT
ADD file:55b071e2cfc3ea2f4bbf048d7d676e3c06a77a9a98d63f7af291f3decb495ec8 in / 
# Mon, 09 Oct 2017 21:30:05 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:41:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 09 Oct 2017 23:41:34 GMT
ENV GOSU_VERSION=1.7
# Mon, 09 Oct 2017 23:42:02 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Mon, 09 Oct 2017 23:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 10 Oct 2017 00:22:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 00:22:17 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 10 Oct 2017 00:22:54 GMT
ENV MYSQL_MAJOR=5.7
# Mon, 16 Oct 2017 19:10:27 GMT
ENV MYSQL_VERSION=5.7.20-1debian8
# Mon, 16 Oct 2017 19:10:28 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Mon, 16 Oct 2017 19:10:59 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Mon, 16 Oct 2017 19:10:59 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/mysql.conf.d/mysqld.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Mon, 16 Oct 2017 19:11:00 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Oct 2017 19:11:00 GMT
COPY file:5453fdbdb142b28e9aa4df64d5e1f42a740f018457cb1c65d113b947858ae314 in /usr/local/bin/ 
# Mon, 16 Oct 2017 19:11:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 16 Oct 2017 19:11:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Oct 2017 19:11:01 GMT
EXPOSE 3306/tcp
# Mon, 16 Oct 2017 19:11:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:85b1f47fba49da65256f07c8790542a3880e9216f9c491965040f35ce2c6ca7a`  
		Last Modified: Mon, 09 Oct 2017 21:36:40 GMT  
		Size: 52.6 MB (52595124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dc53f13a11bdd5a8c0406231db61e3bbcc80abd383c8d2aa025de18bc854f1`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095c8ae4182d531daaaab1ba53752c6ced9fe2b285e113c8f6ace3482fe35e14`  
		Last Modified: Mon, 09 Oct 2017 23:50:44 GMT  
		Size: 1.3 MB (1302935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972f6b9a7de1ee8ae02473a098d3794336153353cf8cbbaf563ed6be7735a5f`  
		Last Modified: Mon, 09 Oct 2017 23:50:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b199048e1dac21056ab6d1bcc4ff6777aa744394e028220fe5a7f3969b2556d`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 10.7 MB (10711007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159de3cf101e0a10be9c44f65c56d4d6736cf0df58e6da23644a8c5807abdacb`  
		Last Modified: Tue, 10 Oct 2017 00:26:50 GMT  
		Size: 19.8 KB (19791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff639f4e6d90459976593914c5ae23a5d3a3b4268c77a7dce16b05ace12dff7`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d7a93157e8ed7c1bf354b7719b84dae0155a54966c45ad827604ce621966a`  
		Last Modified: Mon, 16 Oct 2017 19:17:44 GMT  
		Size: 79.6 MB (79556668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5afe5b139c57a2fd6956d728f02bcfed357755f955adfd105dbf778570c841`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c916ff94d5c0d2a773f95650e78095417845db669525f396f93cfdb8e11622`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 2.7 KB (2736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e934932d4d2512ea0fceb79e43baec06d6eb9e552053da5837a01fbc3a4c1186`  
		Last Modified: Mon, 16 Oct 2017 19:17:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
