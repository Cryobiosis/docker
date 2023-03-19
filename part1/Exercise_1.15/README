
## Debian Bullseye + Yle-dl

https://github.com/aajanki/yle-dl

## Usage

```mkdir download
docker run --rm -v "$(pwd)"/download:/opt/dl:rw yle-dl https://areena.yle.fi/1-3395140
```

Or
```
docker volume create download
chmod a+rw /var/lib/docker/volumes/download/_data/
docker run --mount source=download,target=/opt/dl yle-dl https://areena.yle.fi/podcastit/1-65057445
ls -la /var/lib/docker/volumes/download/_data/
```