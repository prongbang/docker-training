# Docker Stack

ตองโจทย์ความต้องการเอา Service ขึ้นหลายๆตัวในครั้งเดียว

__Create Network with Overlay Driver__

> docker network create -d overlay training-overlay-network

__Deploy Service as Stack__

```
docker stack deploy -c docker-compose.yml (ชื่อ stack)
```

> docker stack deploy -c docker-compose.yml training-stack

__Remove Every Service in Stack__

> docker stack rm training-stack

__Scale Service

```
docker scale service
```