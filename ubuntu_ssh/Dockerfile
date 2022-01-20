FROM ubuntu
RUN mkdir -p /var/run/sshd
RUN apt-get update && apt-get install  openssh-server  -y
RUN ssh-keygen -A
 
ADD ./sshd_config /etc/ssh/sshd_config
RUN  echo 'root:root@123' | chpasswd
RUN rm -rf /var/run/nologin

CMD ["/usr/sbin/sshd","-D"]
