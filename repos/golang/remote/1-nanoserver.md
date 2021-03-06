## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:2ac4be02f2761dc7fddbbe5ffd81ec66650533e1771e868bd40773146b3cae6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1770; amd64

### `golang:1-nanoserver` - windows version 10.0.14393.1770; amd64

```console
$ docker pull golang@sha256:ed90906834123a0b67c7b0d004ec930afec5258bfa5435253a666e84bb9d476e
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.2 MB (505217194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3ffa63368698e5305defd9ab6411fffb234deb51ac12d4f8ec8bbed11ed6d5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:47:17 GMT
RUN Apply image 10.0.14393.0
# Mon, 09 Oct 2017 19:23:15 GMT
RUN Install update 10.0.14393.1770
# Wed, 11 Oct 2017 02:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2017 02:18:44 GMT
ENV GOPATH=C:\gopath
# Wed, 11 Oct 2017 02:19:07 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath;
# Wed, 11 Oct 2017 02:19:10 GMT
ENV GOLANG_VERSION=1.9.1
# Wed, 11 Oct 2017 02:22:18 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8dc72a3881388e4e560c2e45f6be59860b623ad418e7da94e80fee012221cc81'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Complete.';
# Wed, 11 Oct 2017 02:22:21 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:bce2fbc256ea437a87dadac2f69aabd25bed4f56255549090056c1131fad0277`  
		Size: 252.7 MB (252691002 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b0b5e40cb939a7befa4e01212d6f65f30022bbd04b5f15985b45ce9cfd3fcabc`  
		Size: 141.8 MB (141758132 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:357b0f27c7da8f9e64125f39f5d19f42647c49dadd423259e05be758449b1cd8`  
		Last Modified: Wed, 11 Oct 2017 02:30:23 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9f048f62baf5e9fa1a0167d343b349326cc36680d42bef15983c9e4fb01ce8`  
		Last Modified: Wed, 11 Oct 2017 02:30:20 GMT  
		Size: 953.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bedc99243ee3bba8dd6ec1143526f84c1ee3b37fc8fcb99c30cd2fe4a61bde8`  
		Last Modified: Wed, 11 Oct 2017 02:30:20 GMT  
		Size: 891.6 KB (891590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc3eba636fdea6641f4ca121a4bab1b7782ff6e56d8ae4a403f98c9c1c604bf`  
		Last Modified: Wed, 11 Oct 2017 02:30:20 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b71a60dc1f6cdbf40c57190b07b3229a2342958a9c0f4b4133b47cffebc2e9`  
		Last Modified: Wed, 11 Oct 2017 02:30:46 GMT  
		Size: 109.9 MB (109872440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5e28bdc4112f5116a8da6af0f08018e185e366238bd50045cdfe98c762da38`  
		Last Modified: Wed, 11 Oct 2017 02:30:20 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
