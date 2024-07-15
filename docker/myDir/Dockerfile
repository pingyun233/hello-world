# 使用 Ubuntu 作为基础镜像
FROM ubuntu:20.04

# 安装必要的包
RUN apt-get update && apt-get install -y nginx

# 删除默认的 Nginx 配置文件
RUN rm /etc/nginx/sites-enabled/default

# 复制自定义的 Nginx 配置文件到镜像中
COPY nginx.conf /etc/nginx/nginx.conf

# 复制项目中的文件到 Nginx 的 web 根目录
COPY public /var/www/html

# 暴露 Nginx 端口
EXPOSE 80

# 启动 Nginx
CMD ["nginx", "-g", "daemon off;"]
