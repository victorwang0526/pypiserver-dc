# pypiserver-dc

ref https://pypiserver.readthedocs.io

### start pypi server

> docker-compose up -d

then access url http://localhost:18080/


### upload package to server


#### Client Config

On client-side, edit or create a ~/.pypirc file with a similar content:

```
[distutils]
index-servers =
  pypi
  internal

[internal]
repository: http://localhost:18080
username: sottop
password: sottop

[pypi]
repository: https://upload.pypi.org/legacy/
username: your_username
password: your_password
```


#### install pypiuploader

> pip install pypi-uploader2

#### upload to pypi server

> pypiupload requirements requirements.txt -i internal