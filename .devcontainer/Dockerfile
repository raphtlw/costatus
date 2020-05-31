FROM alpine:latest

# Install packages
RUN apk add git curl bash nodejs npm

# Setup shell
RUN curl -fsSL https://starship.rs/install.sh | bash -s -- --yes
RUN printf 'eval "$(starship init bash)"' >> '/root/.bashrc'