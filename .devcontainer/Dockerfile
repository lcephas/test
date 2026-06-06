FROM mcr.microsoft.com/devcontainers/base:fedora

# devcontainers/features/sshd:1 is Debian-only (uses apt-get); install via dnf instead.
RUN dnf install -y openssh-server openssh-clients sudo \
    && ssh-keygen -A \
    && mkdir -p /var/run/sshd

EXPOSE 22
