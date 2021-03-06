## `php:rc-fpm-alpine`

```console
$ docker pull php@sha256:4d300d5e5343a4117bbded2d6e4d1cf069acef318690a016934f098fa7fddcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php:rc-fpm-alpine` - linux; amd64

```console
$ docker pull php@sha256:895a179bfc75cd96f0e83d731c459b92e0d1033c66e84679b9b6a077f6aa6010
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31999655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb2dbb760ad969d3d7e18050ee54ba8b0a6574720458c43db33d49c05862780`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2017 23:34:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pcre-dev 		pkgconf 		re2c
# Wed, 27 Sep 2017 21:03:47 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz 		libressl
# Wed, 27 Sep 2017 21:03:48 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Wed, 27 Sep 2017 21:03:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 27 Sep 2017 21:03:48 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Wed, 27 Sep 2017 21:12:14 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Wed, 27 Sep 2017 21:12:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Wed, 27 Sep 2017 21:12:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Wed, 27 Sep 2017 21:12:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Wed, 27 Sep 2017 21:12:14 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 12 Oct 2017 22:47:39 GMT
ENV PHP_VERSION=7.2.0RC4
# Thu, 12 Oct 2017 22:47:39 GMT
ENV PHP_URL=https://downloads.php.net/~remi/php-7.2.0RC4.tar.xz PHP_ASC_URL=https://downloads.php.net/~remi/php-7.2.0RC4.tar.xz.asc
# Thu, 12 Oct 2017 22:47:39 GMT
ENV PHP_SHA256=08ee9e764891224d73f157e01594605fc85c63ffc9d4773d9ac29b0e3160c68f PHP_MD5=
# Thu, 12 Oct 2017 22:48:02 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Thu, 12 Oct 2017 22:48:02 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Thu, 12 Oct 2017 22:52:20 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		coreutils 		curl-dev 		libedit-dev 		libressl-dev 		libxml2-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Thu, 12 Oct 2017 22:52:21 GMT
COPY multi:3a3ce8aa3891c64454909e9f8257446a1817abe660b49a7baaa26f28bfdc444d in /usr/local/bin/ 
# Thu, 12 Oct 2017 22:52:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Oct 2017 22:52:21 GMT
WORKDIR /var/www/html
# Thu, 12 Oct 2017 22:52:22 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 12 Oct 2017 22:52:22 GMT
EXPOSE 9000/tcp
# Thu, 12 Oct 2017 22:52:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc619ec5037e3de315afe796d462dcc277556bf72975ee0efa11e858b6849d3`  
		Last Modified: Wed, 27 Sep 2017 22:24:09 GMT  
		Size: 1.4 MB (1370282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e276a47a1d7d82fda6eb7fd4b5dbab50f2d148cb15248c28bf90c84bcf740f`  
		Last Modified: Wed, 27 Sep 2017 22:24:06 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c812c22857bd26153e34274d91009c5c196fa09a445bd6437ec80f5d792c7b77`  
		Last Modified: Wed, 27 Sep 2017 22:24:04 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4174b0aa439d76f79e4dfff95d846450c905fd5260aa49c60f66d29b18a0941`  
		Last Modified: Thu, 12 Oct 2017 23:14:22 GMT  
		Size: 12.0 MB (11999952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f13ac699d81fbedab032a837dc47cdf029f26af0f3a8cb76ca3ecba71f34df1`  
		Last Modified: Thu, 12 Oct 2017 23:14:19 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e19a04f86da39ca8f2d91e3efb0d7a3404f2cb0b17b7888f966c64c85708b1`  
		Last Modified: Thu, 12 Oct 2017 23:14:26 GMT  
		Size: 16.6 MB (16627117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c567f4bcc318949416b4a7cdc31e9c6dc6bb670c9dd756f404bc4a0429f7eb`  
		Last Modified: Thu, 12 Oct 2017 23:14:20 GMT  
		Size: 2.2 KB (2162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539fb21bf103ad29daad634fce1dc4d5f8649e7868cff52cff7c8dcb683334d0`  
		Last Modified: Thu, 12 Oct 2017 23:14:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6555840aa284a0166cb3abe9bcd853b08a8662c20676e4cd8a9feb2bcd5330`  
		Last Modified: Thu, 12 Oct 2017 23:14:19 GMT  
		Size: 7.7 KB (7698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
