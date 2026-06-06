FROM mcr.microsoft.com/devcontainers/base:alpine

# devcontainers/features/sshd:1 is Debian-only (uses apt-get); install via apk.
RUN apk add --no-cache openssh-server openssh-client sudo \
    && ssh-keygen -A \
    && mkdir -p /var/run/sshd

EXPOSE 22
