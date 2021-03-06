## `plone:latest`

```console
$ docker pull plone@sha256:d87ffb7506b251a49bb8b2db4fa132d0c5b95df49eca58f42fae1f3d04430b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `plone:latest` - linux; amd64

```console
$ docker pull plone@sha256:79747819e84ba95ae2e9705cc6aaba4f0ea1fa5313ffe10cdb865c2835df8970
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269385331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bf26423262f8a73ad7f7ba4491399b5c627128cd6c550e3d3f0b71616d536e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["start"]`

```dockerfile
# Mon, 09 Oct 2017 21:30:05 GMT
ADD file:55b071e2cfc3ea2f4bbf048d7d676e3c06a77a9a98d63f7af291f3decb495ec8 in / 
# Mon, 09 Oct 2017 21:30:05 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 02:30:35 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2017 02:30:36 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 02:51:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 02:51:37 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Tue, 10 Oct 2017 02:51:37 GMT
ENV PYTHON_VERSION=2.7.14
# Tue, 10 Oct 2017 02:54:10 GMT
RUN set -ex 	&& buildDeps=' 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& apt-get purge -y --auto-remove $buildDeps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python
# Tue, 10 Oct 2017 02:54:10 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 10 Oct 2017 02:54:39 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py 'https://bootstrap.pypa.io/get-pip.py'; 		apt-get purge -y --auto-remove wget; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 10 Oct 2017 02:54:40 GMT
CMD ["python2"]
# Tue, 10 Oct 2017 11:50:37 GMT
RUN useradd --system -m -d /plone -U -u 500 plone  && mkdir -p /data/filestorage /data/blobstorage  && chown -R plone:plone /data
# Tue, 10 Oct 2017 11:50:38 GMT
ENV PLONE_MAJOR=5.0
# Tue, 10 Oct 2017 11:50:38 GMT
ENV PLONE_VERSION=5.0.8
# Tue, 10 Oct 2017 11:50:38 GMT
ENV PLONE_MD5=246788240851f48bc2f84289a3dc6480
# Tue, 10 Oct 2017 11:50:39 GMT
LABEL plone=5.0.8 os=debian os.version=8 name=Plone 5 description=Plone image, based on Unified Installer maintainer=Plone Community
# Tue, 10 Oct 2017 11:54:41 GMT
RUN buildDeps="wget sudo python-setuptools python-dev build-essential libssl-dev libxml2-dev libxslt1-dev libbz2-dev libjpeg62-turbo-dev libtiff5-dev libopenjp2-7-dev"  && runDeps="libxml2 libxslt1.1 libjpeg62 rsync lynx wv libtiff5 libopenjp2-7 poppler-utils"  && apt-get update  && apt-get install -y --no-install-recommends $buildDeps  && wget -O Plone.tgz https://launchpad.net/plone/$PLONE_MAJOR/$PLONE_VERSION/+download/Plone-$PLONE_VERSION-UnifiedInstaller.tgz  && echo "$PLONE_MD5 Plone.tgz" | md5sum -c -  && tar -xzf Plone.tgz  && ./Plone-$PLONE_VERSION-UnifiedInstaller/install.sh       --password=admin       --daemon-user=plone       --owner=plone       --group=plone       --target=/plone       --instance=instance       --var=/data       none  && cd /plone/instance  && sed -i 's/parts =/parts =\n    zeoserver/g' buildout.cfg  && echo '\n[zeoserver]\n<= zeoserver_base\nrecipe = plone.recipe.zeoserver' >> buildout.cfg  && sudo -u plone bin/buildout  && chown -R plone:plone /plone /data  && rm -rf /Plone*  && SUDO_FORCE_REMOVE=yes apt-get remove --purge -y $buildDeps && apt-get install -y --no-install-recommends $runDeps  && apt-get clean  && rm -rf /var/lib/apt/lists/*  && rm -rf /plone/buildout-cache/downloads/*  && rm -rf /plone/Plone-docs  && find /plone \( -type f -a -name '*.pyc' -o -name '*.pyo' \) -exec rm -rf '{}' +
# Tue, 10 Oct 2017 11:58:25 GMT
VOLUME [/data]
# Tue, 10 Oct 2017 11:58:25 GMT
COPY multi:df870708d456e9785c9b887f2caba9a08a7b0644a7384dc8873e8ff7b1eed3b4 in / 
# Tue, 10 Oct 2017 11:58:25 GMT
EXPOSE 8080/tcp
# Tue, 10 Oct 2017 11:58:26 GMT
USER [plone]
# Tue, 10 Oct 2017 11:58:26 GMT
WORKDIR /plone/instance
# Tue, 10 Oct 2017 11:58:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Oct 2017 11:58:26 GMT
CMD ["start"]
```

-	Layers:
	-	`sha256:85b1f47fba49da65256f07c8790542a3880e9216f9c491965040f35ce2c6ca7a`  
		Last Modified: Mon, 09 Oct 2017 21:36:40 GMT  
		Size: 52.6 MB (52595124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e401c4a903e3c61630c231fd5fac9fa4ef987b45cf4b05a58372fd1d1ff186`  
		Last Modified: Tue, 10 Oct 2017 03:04:31 GMT  
		Size: 3.5 MB (3472886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f744658dd6263a62f11a68118afb190a447390734d8a00bbf9537247672cdba`  
		Last Modified: Tue, 10 Oct 2017 03:04:35 GMT  
		Size: 15.0 MB (15045225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562843cc69f8952a960e4d0b5f2c4a827e6c3c620345cdcf41fd933a463cf957`  
		Last Modified: Tue, 10 Oct 2017 03:04:31 GMT  
		Size: 2.0 MB (1966074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821242a33ae7e29081e0fd2d81b9d9e2aadf511dadea4e2fbc79f6d1c2d7bc97`  
		Last Modified: Tue, 10 Oct 2017 12:03:21 GMT  
		Size: 4.2 KB (4198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c64e4d564c8b2e111a505c77a94cf213df94c332e4261c62eef886529e773c`  
		Last Modified: Tue, 10 Oct 2017 12:04:13 GMT  
		Size: 196.3 MB (196299594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13244b3fea4aab24e050c17b91ec0ece308d45f006cb1cc54e4ee15cf9c93c2`  
		Last Modified: Tue, 10 Oct 2017 12:03:21 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
