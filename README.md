# Attic for docker

This is a lightweight image for running [attic](https://attic-backup.org/). This image is based on the lightweight [Alpine Linux](https://alpinelinux.org/).

## Usage

### Initialize a repository
```
docker run -v /:/os xori/attic init /os/var/repo
```

### Create a backup
```
docker run -v /:/os xori/attic create /os/var/repo::`date -Iseconds` /os/home/me
```

### Extract a backup
```
docker run -v /:/os xori/attic extract /os/var/repo::2016-02-19T16:44:10+00:00 /os/home/me
```
