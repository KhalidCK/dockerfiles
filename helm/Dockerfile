FROM ubuntu:focal
RUN apt update && apt install -y curl
RUN curl -LO https://dl.k8s.io/release/v1.20.4/bin/linux/amd64/kubectl
RUN install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
RUN curl https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3 | bash