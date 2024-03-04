ARG VARIANT=0.204.0-18
FROM mcr.microsoft.com/vscode/devcontainers/javascript-node:${VARIANT}

# install homebrew
ENV BREW_PREFIX=/home/linuxbrew/.linuxbrew
ENV PATH=${BREW_PREFIX}/sbin:${BREW_PREFIX}/bin:${PATH}
COPY docker-based/library-scripts/homebrew-debian.sh /tmp/library-scripts/
RUN apt-get update && bash /tmp/library-scripts/homebrew-debian.sh

#
RUN brew install hugo