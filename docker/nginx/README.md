确保app下面有portal所有的前端代码
确保data/conf/nginx.conf文件的正确性

启动nginx，执行下面命令
docker run --name portal-nginx -d -p 80:80 -v $PWD/app:/usr/share/nginx/html -v $PWD/conf/nginx.conf:/etc/nginx/nginx.conf -v $PWD/logs:/etc/nginx/logs nginx

