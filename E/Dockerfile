# Put this Dockerfile at the root directory of E. Build docker image by
# > docker build -t eprover .
#
# At the root of E, run this image as an executable container by
# > docker run --rm -it -v ${PWD}/PROVER:/problems eprover /problems/LUSK6.lop
#
# The host PROVER directory of E is now mounted as /problems in the container.
#
# If you don't want to build your own image, you can pull mine from DockerHub
# > docker pull shawnzaru/eprover
#
# And run like above
# > docker run --rm -it -v ${PWD}/PROVER:/problems shawnzaru/eprover /problems/LUSK6.lop
#
# You can also test run a container problem copy by
# > docker run --rm -it shawnzaru/eprover PROVER/LUSK6.lop
#
# TODO: minimize image size by basing on alpine linux.

FROM ubuntu
WORKDIR /E
COPY . .
RUN apt-get update && apt-get install -y build-essential
RUN ./configure
RUN make rebuild
ENTRYPOINT ["PROVER/eprover"]
CMD ["-h"]
