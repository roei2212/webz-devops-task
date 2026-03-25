FROM ubuntu:18.04

# Install system packages
RUN apt update && \
    apt install -y systemd systemd-sysv iputils-ping curl apache2 && \
    apt clean

# Enable systemd
STOPSIGNAL SIGRTMIN+3

# Expose Apache port
EXPOSE 80

CMD ["/sbin/init"]
