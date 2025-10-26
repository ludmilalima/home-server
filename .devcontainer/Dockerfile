FROM arm64v8/ubuntu:24.04

# Set the environment variables
ENV DEBIAN_FRONTEND=noninteractive

# Update and install necessary packages
RUN apt-get update && \
    apt-get install -y \
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

# Set the working directory
WORKDIR /workspace

# Default command
CMD ["bash"]