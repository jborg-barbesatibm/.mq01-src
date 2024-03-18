# Source image to build from
# Use free version to simplify initial install
FROM icr.io/ibm-messaging/mq:latest

# Add some tools to ensure a new version of the image is created:

USER 0

RUN uname

RUN cat /etc/os-release

RUN cat /etc/issue


# RUN apt-get update && apt-get upgrade -y
# RUN apt-get install libssl-dev
RUN apk-get update && apk-get upgrade -y


RUN microdnf upgrade && microdnf --disableplugin=subscription-manager install lsof bc ca-certificates file findutils gawk util-linux which
RUN microdnf --disableplugin=subscription-manager clean all


USER 1001

RUN echo "all utilities now added"
