## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:44e7290845fda27cfcdf542f2920cb1c9558c0efae06d7e742ceadd35bffe7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1770; amd64

### `mongo:windowsservercore` - windows version 10.0.14393.1770; amd64

```console
$ docker pull mongo@sha256:43cc6a51bbcf88d85734082a93d25d42790ff6624a615420d400e707c4bf8f9a
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5413628453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb35c1d8bb5f1e90b844d023f2efc423d6dbd15031c6a7dcfc1bc10a894d374`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 09 Oct 2017 19:23:50 GMT
RUN Install update 10.0.14393.1770
# Wed, 11 Oct 2017 01:37:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2017 01:40:27 GMT
ENV MONGO_VERSION=3.4.9
# Wed, 11 Oct 2017 01:40:30 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.9-signed.msi
# Wed, 11 Oct 2017 01:40:33 GMT
ENV MONGO_DOWNLOAD_SHA256=68e911de302ddd42e6fe4dda71193c8873f469c59c790fffdd645660e8a5b49a
# Wed, 11 Oct 2017 01:41:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Oct 2017 01:41:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Oct 2017 01:41:46 GMT
EXPOSE 27017/tcp
# Wed, 11 Oct 2017 01:41:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8df8e568af76c1c311a1251f6f7402e2a09d14629840c97091beb9ba55419464`  
		Size: 1.3 GB (1280521235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8db45a9c1883baa808fc2bd5b53ea6c18ad7b55eba3d8ad132f5a38d689b3bdf`  
		Last Modified: Wed, 11 Oct 2017 01:43:58 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337316175d43fb774500873af1a5af250210da650adb72ca3b46ec90470aba1b`  
		Last Modified: Wed, 11 Oct 2017 01:44:44 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8577496c933902bdf89e8159b9b61b8c5106f098c3f18fce7eb3c64100548051`  
		Last Modified: Wed, 11 Oct 2017 01:44:42 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f350b8e0567f3d61ce8dfc290c2c361be89e2ef1faf7123542c49d1a8257cd`  
		Last Modified: Wed, 11 Oct 2017 01:44:35 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec21414b3605a123a92668caab41a717487e145ef190eae91f970be17c8fb1d`  
		Last Modified: Wed, 11 Oct 2017 01:44:48 GMT  
		Size: 63.1 MB (63112788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d66ad002cbdedf6ed25912d4def0ad10b2c433cdf00c35fd3422537176aee63`  
		Last Modified: Wed, 11 Oct 2017 01:44:36 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46715773679d9c781cfc8c4556dc66ab854a30034e4f11d14c96bcb38e43079`  
		Last Modified: Wed, 11 Oct 2017 01:44:35 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf2b484f66b16aa9d7577a9766022320a81c9c8ba63bd95b92ff7c94ed123fe`  
		Last Modified: Wed, 11 Oct 2017 01:44:38 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
