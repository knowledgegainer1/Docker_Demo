FROM almalinux:8
# RUN yum install nginx -y
# CMD [  "google.com" ]
# ENTRYPOINT [ "ping" ]
RUN adduser sada
USER sada
WORKDIR /tmp
RUN echo "hello you are in temp foldr now" > hellp.txt
CMD [ "sleep", "10" ]
