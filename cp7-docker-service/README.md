# Docker Service

__Create Service__

> docker pull httpd:2.4

> docker service create --name test-docker-service -p 80:80 httpd:2.4

__List Service__

> docker service ls


__Log Service__

> docker service logs test-docker-service