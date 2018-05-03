# Docker Volume

mount ไฟล์ที่อยู่ข้างในให้ออกมาอยู่ข้่างนอก เวลา container ตายข้อมูลจะได้ไม่หายไปด้วย

__Create Volume__

> docker volume create train-volume

__Remove Volume__

> docker volume rm train-volume

__Docker run with volume__

_Run new container with existing volume_

```
docker run --volume train-volume(นอก docker):(folder/file ใน docker)/data --name test-volume1 --detach ping-image
```

> docker run --volume train-volume:/data --name test-volume1 --detach ping-image

_Test 1_

> docker exec -it test-volume1 /bin/bash

> ls /data

> echo "test message" > /data/test-volume1.txt

_Stop and remove test-volume1_

> docker stop test-volume1

> docker rm test-volume1

_Run new container with existing volume_

> Create and volume

```
docker run --volume train-volume:/data --name test-volume2 --detach ping-image
```

_Test 2_

> docker exec -it test-volume2 /bin/bash

> ls /data

_Stop and remove test-volume2_

> docker stop test-volume2

> docker rm test-volume2