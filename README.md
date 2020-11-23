# nginx-docker
* nginx-docker镜像

# CentOS镜像启动
* 批量创建文件夹
> mkdir -p  {/home/nginx/html,/home/nginx/conf,/home/nginx/logs}[跟需要的文件夹]

* 将 config中的nginx默认配置文件拷贝到 /home/nginx/conf 目录下

* [保持重启启动]
> docker run --restart=always --name nginx  -d  -p 80:80 -v /home/nginx/conf/nginx.conf:/etc/nginx/nginx.conf -v /home/nginx/html:/usr/share/nginx/html -v /home/nginx/logs:/var/log/nginx nuiiqk/nginx:latest

# win镜像启动
> docker pull nuiiqk/nginx

* [保持重启启动]
> docker run --restart=always --name nginx  -d  -p 80:80 -v F:\nginx\conf\nginx.conf:/etc/nginx/nginx.conf -v F:\nginx\html:/usr/share/nginx/html -v F:\nginx\logs:/var/log/nginx nuiiqk/nginx:latest

# nginx默认目录  html logs conf
/etc/nginx/nginx.conf
/usr/share/nginx/html
/var/log/nginx
