# Docker Swarm

กรณีที่มี container มากกว่า 1 เครื่อง จึงจะต้องใช้ docker swarm เพื่อเชื่อมต่อไปทุกเครื่อง เวลาเราสร้าง service หรืออะไรก้แล้วแต่ ในเครื่องเดียว ผ่าน proxy

__1. Initial Docker Swarm Cluster__

> docker swarm init --advertise-addr [comunicate ip ที่ต้องการให้ แต่ละเครื่องมาคุยกันที่นี่]

> docker swarm join-token (managerหรือmaster|worker)

managerหรือmaster สามารถจัดการได้

__2. Join Docker Swarm Cluster__

> docker swarm join --token (swarm-token) (advertise-ip):2377

__3. Check Node Status__

> docker node ls

__4. Inspect Each Node__

> docker node inspect (hostname|node id)

#### การทำให้ swarm3 เป็น master

> docker promote swarm3