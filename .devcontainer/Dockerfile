FROM arm64v8/ubuntu:24.04

# Set the environment variables
ENV DEBIAN_FRONTEND=noninteractive

# Update and install necessary packages
RUN apt-get update && \
    apt-get install -y \
    sudo \
    build-essential \
    curl \
    git \
    vim \
    bc \
    bison \
    flex \
    libssl-dev \
    make \
    libc6-dev \
    libncurses-dev \
    && apt-get clean

# Create a new user
RUN useradd -m -s /bin/bash home-server-builder && \
    echo "home-server-builder ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

# Switch to the new user
USER home-server-builder

# Set the working directory for the new user
WORKDIR /home/home-server

# Default command
CMD ["bash"]