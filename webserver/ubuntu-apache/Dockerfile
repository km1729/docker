FROM ubuntu:latest

# Set the timezone to Melbourne
RUN ln -sf /usr/share/zoneinfo/Australia/Melbourne /etc/localtime

# Install sudo and Apache
RUN apt-get update && apt-get install -y sudo apache2
RUN apt upgrade -y

# Set up a non-root user with sudo privileges
RUN useradd -ms /bin/bash myuser && echo "myuser ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

# Switch to the non-root user
USER myuser

CMD ["/bin/bash"]
