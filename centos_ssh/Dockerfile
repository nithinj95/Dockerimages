FROM centos
RUN mkdir -p /var/run/sshd
RUN dnf install  openssh-server openssh openssh-clients  -y
RUN ssh-keygen -A
 
ADD ./sshd_config /etc/ssh/sshd_config
RUN  echo 'root:root@123' | chpasswd
RUN rm -rf /var/run/nologin

CMD ["/usr/sbin/sshd","-D"]
