# Use an official Python slim image as the base
FROM python:3.11-slim

# Update packages and install dependencies (e.g., openssh-client for SSH connectivity)
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    openssh-client \ 
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Install Ansible via pip
RUN pip install --no-cache-dir ansible

# Set the working directory (optional)
WORKDIR /ansible