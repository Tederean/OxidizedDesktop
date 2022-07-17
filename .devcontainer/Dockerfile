FROM rust:latest

RUN apt-get update -y
RUN apt-get upgrade -y

RUN apt-get install -y wget

RUN rustup component add rustfmt

RUN groupadd --gid 1000 vscode
RUN useradd --system --gid 1000 --uid 1000 --shell /bin/bash vscode

RUN mkdir /home/vscode
RUN chown -R 1000:1000 /home/vscode

RUN chown -R 1000:1000 /usr/local/cargo

USER vscode