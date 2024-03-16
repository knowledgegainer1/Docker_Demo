FROM almalinux/8-base
RUN yum install nginx -y
LABEL person="sadashiva" \
      working="yes" \
      orzn="TCS"
CMD ["nginx", "-g", "daemon off;"]  