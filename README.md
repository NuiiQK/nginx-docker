# nginx-docker
* nginx-docker镜像

# CentOS镜像启动
* 批量创建文件夹
> mkdir -p  {/app/docker/data/nginx/html,/app/docker/data/nginx/conf,/app/docker/data/nginx/logs}[跟需要的文件夹]

* 将 config中的nginx默认配置文件拷贝到 /app/docker/nginx/conf 目录下

* [保持重启启动]
> docker run --restart=always --privileged=true --name nginx  -d  -p 80:80 -v /app/docker/data/nginx/conf/nginx.conf:/etc/nginx/nginx.conf -v /app/docker/data/nginx/html:/usr/share/nginx/html -v /app/docker/data/nginx/logs:/var/log/nginx nuiiqk/nginx:latest

# win镜像启动
> docker pull nuiiqk/nginx

* [保持重启启动]
> docker run --restart=always --privileged=true --name nginx  -d  -p 80:80 -v F:\app\docker\data\nginx\conf:/etc/nginx -v F:\app\docker\data\nginx\html:/usr/share/nginx/html -v F:\app\docker\data\nginx\logs:/var/log/nginx nuiiqk/nginx:latest

# nginx默认目录  html logs conf
/etc/nginx/nginx.conf
/usr/share/nginx/html
/var/log/nginx

/user/local/nginx
