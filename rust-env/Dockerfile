FROM base-env:latest

USER dev-user

RUN curl https://sh.rustup.rs -sSf | sh -s -- -y
ENV PATH="/home/dev-user/.cargo/bin:${PATH}"
