FROM alpine:3
LABEL author="valentin.marlier@ynov.com"

RUN apk update && apk add curl unzip
RUN curl -o terraform.zip https://releases.hashicorp.com/terraform/0.14.3/terraform_0.14.3_linux_amd64.zip && \
    curl -o /usr/local/bin/scw -L "https://github.com/scaleway/scaleway-cli/releases/download/v2.2.3/scw-2.2.3-linux-x86_64" && \
    curl -o /usr/local/bin/kubectl -L "https://storage.googleapis.com/kubernetes-release/release/v1.20.0/bin/linux/amd64/kubectl"

RUN unzip terraform.zip && mv terraform /bin/terraform && \
    chmod +x /usr/local/bin/scw && \
    chmod +x /usr/local/bin/kubectl

WORKDIR /opt/
