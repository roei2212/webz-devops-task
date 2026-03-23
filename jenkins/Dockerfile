FROM ubuntu:18.04

# Install dependencies
RUN apt update && \
    apt install -y openjdk-11-jdk wget gnupg curl && \
    apt clean

# Install Jenkins
RUN wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | apt-key add - && \
    echo "deb https://pkg.jenkins.io/debian binary/" > /etc/apt/sources.list.d/jenkins.list && \
    apt update && \
    apt install -y jenkins && \
    apt clean

# Expose Jenkins port
EXPOSE 8080

# Create logs directory inside container
RUN mkdir -p /logs

CMD ["bash", "-c", "service jenkins start && tail -f /var/log/jenkins/jenkins.log"]
