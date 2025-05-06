FROM alpine:latest

# Install Ansible, SSH client, and dependencies
RUN apk add --no-cache ansible openssh-client python3 sshpass

WORKDIR /ansible

# Disable host key checking for Ansible
ENV ANSIBLE_HOST_KEY_CHECKING=False

CMD ["sh"]
