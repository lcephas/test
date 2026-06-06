FROM fedora:40

# Non-apt distro chosen to exercise the dnf → pip-venv rung of the az install ladder.
# Provide the standard devcontainer prerequisites (sudo, git, ssh) since this is a
# bare distro image, not an MS devcontainers base.
RUN dnf install -y openssh-server openssh-clients sudo git ca-certificates which \
    && ssh-keygen -A \
    && mkdir -p /var/run/sshd \
    && useradd -m -s /bin/bash -G wheel vscode \
    && echo 'vscode ALL=(ALL) NOPASSWD: ALL' > /etc/sudoers.d/vscode

EXPOSE 22
