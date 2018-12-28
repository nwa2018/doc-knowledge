# 本地开发环境配置Nginx

### 安装
```
brew install nginx
```
```
安装目录：/usr/local/Cellar/nginx/

配置文件路径：/usr/local/etc/nginx

日志位置：
/usr/local/var/log/nginx/access.log
/usr/local/var/log/nginx/error.log
```

### 查看nginx配置文件：
`/usr/local/etc/nginx/`
``` nginx
worker_processes  1;
events {
    worker_connections  1024;
}
http {
    include       mime.types;
    default_type  application/octet-stream;
    sendfile        on;
    keepalive_timeout  65;
    server {
        listen       8080;
        server_name  localhost;
        location / {
            root   html;
            index  index.html index.htm;
        }
        error_page   500 502 503 504  /50x.html;
        location = /50x.html {
            root   html;
        }
    }
    include /usr/local/etc/nginx/conf.d/*.conf;
}
```
### 在/usr/local/etc/nginx/conf.d/目录下新建一个配置文件kdrp.conf：
```
server {
    listen 80;
    server_name localhost;
    charset     utf-8;
    client_max_body_size 75M;

    location ^~ /api/ {
        proxy_set_header X-Real-IP $remote_addr;
        proxy_pass http://***.com/api/;
    }

    location / {
        proxy_pass http://localhost:8000/;
    }
}
```
### 测试Nginx配置文件是否正确：
```
nginx - t
```
### 启动或者重启nginx服务
```
> nginx
或
> nginx -s reload
```

