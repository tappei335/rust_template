FROM ubuntu:22.04

RUN apt-get update && \
    apt-get install -y \
    curl \
    git \
    gnupg2 \
    jq \
    sudo \
    zsh \
    vim \
    build-essential \
    pkg-config \
    libssl-dev

ENV PATH="/root/.cargo/bin:${PATH}"
RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- --default-toolchain none -y && \
    rustup toolchain install nightly --allow-downgrade --profile minimal --component clippy && \
    cargo install cargo-edit

