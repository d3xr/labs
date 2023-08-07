
# Docker Container Management

## List Containers
- **Command used to list Docker containers:** `docker ps -a`
- **Output:** 
```
IskanderVafin@DevOpsLabs % docker ps -a
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```

## Pull Latest Ubuntu Image
- **Command used to pull the latest Ubuntu image:** `docker pull ubuntu:latest`
- **Output:** 
```
IskanderVafin@DevOpsLabs % docker pull ubuntu:latest
latest: Pulling from library/ubuntu
3153aa388d02: Pull complete 
Digest: sha256:0bced47fffa3361afa981854fcabcd4577cd43cebbb808cea2b1f33a3dd7f508
Status: Downloaded newer image for ubuntu:latest
docker.io/library/ubuntu:latest
```

## Run Container
- **Command used to run a container using the Ubuntu image:** `docker run -it ubuntu`
- **Output:** 
```
IskanderVafin@DevOpsLabs % docker run -it ubuntu                      
root@631a563360e9:/# whoami
root
root@631a563360e9:/# ps -a
  PID TTY          TIME CMD
   10 pts/0    00:00:00 ps
root@631a563360e9:/# 
```

## Remove Image
- **Command used to remove the Ubuntu image:** `docker rmi ubuntu:latest`
- **Outcome:** 
```
IskanderVafin@DevOpsLabs % docker rmi ubuntu                                                         
Untagged: ubuntu:latest
Untagged: ubuntu@sha256:0bced47fffa3361afa981854fcabcd4577cd43cebbb808cea2b1f33a3dd7f508
Deleted: sha256:5a81c4b8502e4979e75bd8f91343b95b0d695ab67f241dbed0d1530a35bde1eb
Deleted: sha256:59c56aee1fb4dbaeb334aef06088b49902105d1ea0c15a9e5a2a9ce560fa4c5d
```
