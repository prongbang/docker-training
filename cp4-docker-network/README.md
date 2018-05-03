# Docker Network

ทำให้ container เชื่อมต่อกัน โดย 1 container มีได้หลาย network ถ้าอยู่คนละเครื่องจะใช้ IP แทน

__Create Network__

> docker network create training-network

__Show__

> docker network ls

__Remove Network__

> docker network rm training-network

__Docker run with network__
กรณีอยู่ภายในเครื่องเดียวกันจะใช้ชื่อ container แทน IP

> docker run --network training-network --name test-network1 --detach ping-image

> docker run --network training-network --name test-network2 --env TARGET=test-network1 --detach ping-image

__Loga__

docker logs -f test-network(ชื่อ container)