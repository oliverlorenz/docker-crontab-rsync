![Docker Cloud Automated build](https://img.shields.io/docker/cloud/automated/oliverlorenz/crontab-rsync) ![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/oliverlorenz/crontab-rsync)
# docker-crontab-rsync

This is a image is based on [oliverlorenz/docker-crontab](https://hub.docker.com/r/oliverlorenz/crontab). It adds the rsync package which can be used in a cronjob.

## usage

```
docker run -d \
  -v /path/to/crontab:/crontab
  -v /path/to/files:/volume
  oliverlorenz/crontab-rsync:latest-alpine
```

### example crontab
```
* * * * * /usr/bin/rsync /volume/* user@host:/path/
```

## see also

* base image: [oliverlorenz/docker-crontab](https://hub.docker.com/r/oliverlorenz/crontab)
