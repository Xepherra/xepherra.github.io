FROM mcr.microsoft.com/devcontainers/ruby:3

# Basic tools + Node for assets (Sass)
RUN apt-get update && \
    apt-get install -y --no-install-recommends nodejs npm build-essential curl git && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

# Global gems used for local testing
RUN gem install jekyll bundler

# Create workspace dir (Codespaces mounts your repo here)
WORKDIR /workspaces

# Keep image small; actual gem/npm installs happen in postCreateCommand
