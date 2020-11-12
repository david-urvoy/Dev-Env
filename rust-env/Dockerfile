FROM david-urvoy/base-env:latest

USER dev-user
RUN mkdir -p /home/dev-user/.cargo
#VOLUME [ "/home/dev-user/.cargo" ]

RUN curl https://sh.rustup.rs -sSf | sh -s -- -y
ENV PATH="/home/dev-user/.cargo/bin:${PATH}"
