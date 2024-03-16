FROM almalinux/8-base
RUN yum install nginx -y
EXPOSE 80/tcp
ENV greeting="hello" value="tem"
LABEL person="sadashiva"
CMD ["nginx", "-g", "daemon off;"]      