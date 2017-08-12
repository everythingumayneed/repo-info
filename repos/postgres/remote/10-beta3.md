## `postgres:10-beta3`

```console
$ docker pull postgres@sha256:802521458c79ded89f718d6f0b0a0856b9468b3aaf4ca3ecd6942129a50188c2
```

-	Platforms:
	-	linux; amd64

### `postgres:10-beta3` - linux; amd64

-	Docker Version: 17.03.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117572263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b10a469cf2c69c0aa537f2111084d3f0b1046299a259aa5accb4f93ab1c43d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 24 Jul 2017 16:52:54 GMT
ADD file:ebba725fb97cea45d0b1b35ccc8144e766fcfc9a78530465c23b0c4674b14042 in / 
# Mon, 24 Jul 2017 16:52:55 GMT
CMD ["bash"]
# Wed, 26 Jul 2017 08:44:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jul 2017 08:44:00 GMT
RUN groupadd -r postgres --gid=999 && useradd -r -g postgres --uid=999 postgres
# Wed, 26 Jul 2017 08:44:01 GMT
ENV GOSU_VERSION=1.7
# Wed, 26 Jul 2017 08:44:14 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 26 Jul 2017 08:44:19 GMT
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* 	&& localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 26 Jul 2017 08:44:19 GMT
ENV LANG=en_US.utf8
# Wed, 26 Jul 2017 08:44:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Jul 2017 08:44:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 26 Jul 2017 08:44:23 GMT
ENV PG_MAJOR=10
# Thu, 10 Aug 2017 22:39:31 GMT
ENV PG_VERSION=10~beta3-1.pgdg90+1
# Thu, 10 Aug 2017 22:39:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' $PG_MAJOR > /etc/apt/sources.list.d/pgdg.list
# Thu, 10 Aug 2017 22:39:57 GMT
RUN apt-get update 	&& apt-get install -y postgresql-common 	&& sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf 	&& apt-get install -y 		postgresql-$PG_MAJOR=$PG_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Aug 2017 22:39:57 GMT
RUN mv -v /usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample /usr/share/postgresql/ 	&& ln -sv ../postgresql.conf.sample /usr/share/postgresql/$PG_MAJOR/ 	&& sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample
# Thu, 10 Aug 2017 22:39:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 10 Aug 2017 22:39:58 GMT
ENV PATH=/usr/lib/postgresql/10/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Aug 2017 22:39:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2017 22:39:59 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # this 777 will be replaced by 700 at runtime (allows semi-arbitrary "--user" values)
# Thu, 10 Aug 2017 22:40:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2017 22:40:00 GMT
COPY file:643bb6306366c6990a8d7cc47297e0080cc2a18a48a305868c51739e9416a044 in /usr/local/bin/ 
# Thu, 10 Aug 2017 22:40:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 10 Aug 2017 22:40:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2017 22:40:01 GMT
EXPOSE 5432/tcp
# Thu, 10 Aug 2017 22:40:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:06b22ddb19134ec8c42aaabd3e2e9f5b378e4e53da4a8960eaaaa86351190af3`  
		Last Modified: Mon, 24 Jul 2017 16:59:30 GMT  
		Size: 45.1 MB (45142935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a89e9890c383465015499306a27143688020b186d8efa289d9e97670b8c60dc`  
		Last Modified: Wed, 26 Jul 2017 08:50:39 GMT  
		Size: 7.0 MB (7029499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ec871acfa2d70642e3044907f4c793fbb34bba761548a6557dcce41e72453c`  
		Last Modified: Wed, 26 Jul 2017 08:50:38 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9332a355d3d73c1cfbc811504d3ed1cf2c5660ea8736467140cf3c4538c135e6`  
		Last Modified: Wed, 26 Jul 2017 08:50:36 GMT  
		Size: 1.3 MB (1275160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6675a5cbbf42cffc312e240b1a8286b4cadbe7057c730c81df3e4ae90fc2d13`  
		Last Modified: Wed, 26 Jul 2017 08:50:37 GMT  
		Size: 6.6 MB (6577473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d0e64f9fe2ba9d7ff0aa91cfddadb79abfdc05a9523ac365496f35914b13c9`  
		Last Modified: Wed, 26 Jul 2017 08:50:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6df1120c4fd91d1cb826ee3406ebf7a0f03e3277756848e8bd4732271c5ee69`  
		Last Modified: Wed, 26 Jul 2017 08:50:37 GMT  
		Size: 4.5 KB (4470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e581a65df7daf7bed27ffa7515665184bf0b6cb742d15555ebcba9ee102ea46`  
		Last Modified: Thu, 10 Aug 2017 23:11:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6772b737b12431e82ef5e0bae3f12ded2d85ffcab47835afe700cf4decc80e3f`  
		Last Modified: Thu, 10 Aug 2017 23:11:44 GMT  
		Size: 57.5 MB (57531169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b7472db95a21e1808ba829707ea85a8cc7fd2fd2b66cf7a3adf80b3a11bdec`  
		Last Modified: Thu, 10 Aug 2017 23:11:23 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2110c1905b871d894a32a6ad7cc4806458a59050a589d6b8a06497d10deeab`  
		Last Modified: Thu, 10 Aug 2017 23:11:23 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d25a5dfa071effa2bba88c04df316bc279807c1975ab32e8842dcb85468535f`  
		Last Modified: Thu, 10 Aug 2017 23:11:23 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6628b5fe794ab39afef7294055ec5b0860df591a64112db828f3e68783147192`  
		Last Modified: Thu, 10 Aug 2017 23:11:28 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50967d96fb4766f78fcd9fc0be0afeb8dd728e39ed9b483a5ce09f757f38a1a`  
		Last Modified: Thu, 10 Aug 2017 23:11:23 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip