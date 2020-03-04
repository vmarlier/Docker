FROM debian:10.3

LABEL author="valentin.marlier@d2si.io"

RUN apt update -y
RUN apt install -y python-pip unzip
RUN pip install --upgrade pip
RUN pip install awscli

RUN apt install -y curl
RUN curl https://releases.hashicorp.com/terraform/0.12.21/terraform_0.12.21_linux_amd64.zip -o terraform.zip
RUN unzip ./terraform.zip
RUN mv ./terraform /bin/terraform
RUN terraform version

WORKDIR /opt/
