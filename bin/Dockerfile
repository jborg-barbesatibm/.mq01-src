# Source image to build from
# Use free version to simplify initial install
FROM icr.io/ibm-messaging/mq:latest

# Add some tools to ensure a new version of the image is created:
RUN microdnf upgrade && microdnf --disableplugin=subscription-manager install lsof bc ca-certificates file findutils gawk util-linux which
RUN microdnf --disableplugin=subscription-manager clean all
