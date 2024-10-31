# Use Debian Slim as the base image
FROM debian:bullseye-slim

# Set maintainer label
LABEL maintainer="konas13@gmail.com"

# Install neccesery software
 RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
     && apt-get -y install --no-install-recommends lolcat \
     git \
# Install R and system dependencies
    r-base \
    libcurl4-openssl-dev \
    libssl-dev \
    libxml2-dev \
    && apt-get clean

# Install R packages
RUN Rscript -e "install.packages(c('dplyr', 'ggplot2', 'tidyr'), repos='https://cloud.r-project.org')"

    
#FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu

# use this Dockerfile to install additional tools you might need, e.g.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>
