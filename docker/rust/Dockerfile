FROM rust:1.66

RUN apt-get update && \
    apt-get -y install git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rustup component add rust-analyzer rust-src rustfmt clippy && \
    rustup target add x86_64-unknown-linux-musl && \
    rustup toolchain add 1.42.0 && \
    cargo install cargo-atcoder && \
    mkdir ~/.config

COPY cargo-atcoder.toml /root/.config/cargo-atcoder.toml
