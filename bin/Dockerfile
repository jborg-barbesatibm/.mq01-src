# Source image to build from
# Use free version to simplify initial install
FROM icr.io/ibm-messaging/mq:latest



USER 0

# Check out the flavour of Linux:
# RUN uname
RUN cat /etc/os-release
RUN cat /etc/issue


# Add some tools to ensure a new version of the image is created:
# RUN apt-get update && apt-get upgrade -y
# RUN apt-get install libssl-dev
#                     openssl-devel.
# RUN apk-get update && apk-get upgrade -y

RUN dnf upgrade && dnf --disableplugin=subscription-manager install openssl-devel

# RUN microdnf upgrade && microdnf --disableplugin=subscription-manager install lsof bc ca-certificates file findutils gawk util-linux which
# RUN microdnf --disableplugin=subscription-manager clean all


USER 1001

RUN echo "all utilities now added"
