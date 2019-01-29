Dockerfile:
```
FROM microsoft/iis

RUN powershell -NoProfile -Command Remove-Item -Recurse C:\inetpub\wwwroot\*

WORKDIR /inetpub/wwwroot

COPY content/ .
```

Run commands:
```
$ docker build -t iis-site .
$ docker run -d -p 8000:80 --name my-running-site iis-site
```
Result:
```
Step 1/4 : FROM microsoft/iis
latest: Pulling from microsoft/iis
no matching manifest for unknown in the manifest list entries
```