# Source image to build from
# Use free version to simplify initial install
FROM icr.io/ibm-messaging/mq:latest


USER 0

# Check out the flavour of Linux:
# RUN uname
RUN cat /etc/os-release
RUN cat /etc/issue
RUN echo "Architecture is: " && arch

RUN rpm -qa


RUN microdnf upgrade \
  --refresh \
  --best \
  --nodocs \
  --noplugins \
  --setopt=install_weak_deps=0

RUN microdnf --disableplugin=subscription-manager install openssl-devel
RUN microdnf --disableplugin=subscription-manager clean all


USER 1001

RUN echo "all utilities now added"
