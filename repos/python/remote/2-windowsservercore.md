## `python:2-windowsservercore`

```console
$ docker pull python@sha256:a8dd17cae48614272f499623fd6a5c7e68360b28f49d5586105af05b1efcf56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1770; amd64

### `python:2-windowsservercore` - windows version 10.0.14393.1770; amd64

```console
$ docker pull python@sha256:9f45696be32cf25704b75567cd4acb75397434404eaae9f43b8ba36d23b8955b
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5404613527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678838e5d9495aaa4f2315e9ba27c05244f804034cb773ecd283c6e89528e4f2`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 09 Oct 2017 19:23:50 GMT
RUN Install update 10.0.14393.1770
# Wed, 11 Oct 2017 02:13:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2017 16:33:00 GMT
ENV PYTHON_VERSION=2.7.14
# Wed, 11 Oct 2017 16:33:03 GMT
ENV PYTHON_RELEASE=2.7.14
# Wed, 11 Oct 2017 16:34:11 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Oct 2017 16:34:13 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Wed, 11 Oct 2017 16:35:00 GMT
RUN Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri 'https://bootstrap.pypa.io/get-pip.py' -OutFile 'get-pip.py'; 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2017 16:35:26 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 11 Oct 2017 16:35:30 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8df8e568af76c1c311a1251f6f7402e2a09d14629840c97091beb9ba55419464`  
		Size: 1.3 GB (1280521235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9604659e3e8da6b99c25a393035f4f0c389c2dfe4d4935d6d2c5c3f14bb34019`  
		Last Modified: Wed, 11 Oct 2017 02:29:33 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f8dc9cf57fed89dbbbf274be22f9b6f4fea8343a71055c9db4b24dbfdbaa9c`  
		Last Modified: Wed, 11 Oct 2017 16:37:03 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53384d383001e23167101bd5973fbe9a9c06722db143639095f01d991d9d6224`  
		Last Modified: Wed, 11 Oct 2017 16:37:03 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6060bf3165d338be8de7764e6b5951d3081f286deee91ed20c72e736463c975`  
		Last Modified: Wed, 11 Oct 2017 16:37:09 GMT  
		Size: 38.3 MB (38343007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d9212ba07131ac6f47c18e7ec00c94e665309a904805a2d31bfc1e7ecf583f`  
		Last Modified: Wed, 11 Oct 2017 16:36:59 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96bac13a91b7f52e5107a6399a7ec8bf67927ace3844867cb4e469745dcbd800`  
		Last Modified: Wed, 11 Oct 2017 16:37:05 GMT  
		Size: 9.0 MB (9013931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da208ae6262517b65bdec9bcc6e8949781d91e862e857b02bb37a0f82eff982c`  
		Last Modified: Wed, 11 Oct 2017 16:37:03 GMT  
		Size: 6.7 MB (6743349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8ece3fe44799d1affb3d64d4ec49c43a07b89ead2d4fc08fea2ca410783ee8`  
		Last Modified: Wed, 11 Oct 2017 16:37:00 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
