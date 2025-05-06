FROM ubuntu:latest

# Install SSH server and sudo
RUN apt-get update && apt-get install -y openssh-server sudo && \
    rm -rf /var/lib/apt/lists/*

# Create ansible user with password and sudo access
RUN useradd -m -s /bin/bash ansible && \
    echo "ansible:password" | chpasswd && \
    echo 'ansible ALL=(ALL) NOPASSWD: ALL' > /etc/sudoers.d/ansible

# Configure SSH
RUN mkdir /var/run/sshd && \
    sed -i 's/#PasswordAuthentication yes/PasswordAuthentication yes/' /etc/ssh/sshd_config && \
    sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin no/' /etc/ssh/sshd_config

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
