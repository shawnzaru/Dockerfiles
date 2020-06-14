# Download the recent mizar linux tarball and put it into a clean directory.
# Put this Dockerfile into that directory too.
#
# Build image
# > docker build -t mizar .
#
# Run
# > docker run --rm -it -v ${PWD}:/dir mizar mizf /dir/<path-to-local-miz-file>

FROM ubuntu
WORKDIR /mizar
COPY README               /mizar
COPY install.sh           /mizar
COPY mizbin.tar.gz        /mizar
COPY mizdoc.tar.gz        /mizar
COPY mizshare.tar.gz      /mizar
RUN ./install.sh --default
ARG mizfiles=/usr/local/share/mizar
ENV MIZFILES=$mizfiles
CMD echo "Usage: mizf /<mount_dir>/<path-to-file>"
