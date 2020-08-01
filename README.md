# Docker openSUSE Leap Systemd

[![build status](https://img.shields.io/docker/cloud/build/maodevops/opensuse-systemd)](https://hub.docker.com/repository/docker/maodevops/opensuse-systemd)

openSUSE Leap image that has systemd enabled.

## Branches

Each branch in the repository is used for building a specific version.

| Branch | openSUSE Leap Version | FROM Docker image tag |
| ------ | --------------------- | --------------------- |
| master | latest (15.2)         | latest                |
| 15.2   | 15.2                  | 15.2                  |
| 15.1   | 15.1                  | 15.1                  |

### Run it

```bash
docker run -d \
  --tty \
  --privileged \
  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro \
  --name maodevops-opensuse15.2-systemd \
  maodevops/opensuse-systemd:15.2
```

### Enter it

```bash
docker exec -it maodevops-opensuse15.2-systemd /bin/bash
```

### Remove it

```bash
docker rm -f maodevops-opensuse15.2-systemd
```
