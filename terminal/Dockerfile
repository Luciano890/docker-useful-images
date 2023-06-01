FROM alpine:latest

RUN apk update && apk add --no-cache neovim openssh-client openssh -f

RUN sh -c "$(wget -O- https://github.com/deluan/zsh-in-docker/releases/download/v1.1.5/zsh-in-docker.sh)" -- \
    -p git -p copyfile \
    -p https://github.com/zsh-users/zsh-autosuggestions \
    -p https://github.com/zsh-users/zsh-syntax-highlighting

WORKDIR /root

CMD [ "zsh" ]
