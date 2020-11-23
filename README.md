# nginx-docker
nginx-docker镜像


#win镜像启动
docker pull nuiiqk/nginx

[保持重启启动]
docker run --restart=always --name nginx  -d  -p 80:80 -v F:\nginx\conf\nginx.conf:/etc/nginx/nginx.conf -v F:\nginx\html:/usr/share/nginx/html -v F:\nginx\logs:/var/log/nginx nuiiqk/nginx:latest

#nginx默认目录  html logs conf
/etc/nginx/nginx.conf
/usr/share/nginx/html
/var/log/nginx