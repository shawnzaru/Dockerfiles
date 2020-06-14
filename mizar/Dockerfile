# > docker run --rm -it -v ${PWD}:/dir mizar mizf /dir/hello.miz

FROM ubuntu
WORKDIR /mizar
COPY . .
RUN ./install.sh --default
ARG mizfiles=/usr/local/share/mizar
ENV MIZFILES=$mizfiles
CMD echo "Usage: mizf /<container_fs_dir>/[filename]"
