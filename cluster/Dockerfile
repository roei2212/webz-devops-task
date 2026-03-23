FROM ubuntu:18.04

RUN apt update && \
    apt install -y systemd systemd-sysv iputils-ping curl apache2 \
                   pacemaker corosync pcs && \
    apt clean

CMD ["/sbin/init"]
