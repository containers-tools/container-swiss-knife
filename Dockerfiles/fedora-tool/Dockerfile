FROM fedora/tools
MAINTAINER David Becvarik <dbecvari@redhat.com>

RUN dnf install 9pfs -y && dnf clean all
#FIXME do not run this as root
RUN useradd -m tools
USER tools 
ENV HOME /home/tools
CMD ["9pfs", "-p", "6000"]

