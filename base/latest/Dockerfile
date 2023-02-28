FROM registry.fedoraproject.org/fedora-minimal:34

LABEL maintainer="Debezium Community"

COPY ZscalerRootCertificate-2048-SHA256.pem /etc/pki/ca-trust/source/anchors/
RUN update-ca-trust

USER root
RUN microdnf update -y &&\
    microdnf install -y java-11-openjdk tar gzip iproute findutils zip &&\
    microdnf clean all
