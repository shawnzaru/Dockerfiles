# Put this Dockerfile into the root directory of E. Build the docker image by
# > docker build -t eprover .
#
# At the root directory of E, run this container as an executable by
# > docker run --rm -it -v ${PWD}/PROVER:/problems eprover /problems/LUSK6.lop
#
# Or you can just pull my own image
# > docker pull shawnzaru/eprover
#
# And run as above.

FROM ubuntu
WORKDIR /E
COPY . .
RUN apt-get update && apt-get install -y build-essential
RUN ./configure
RUN make rebuild
ENTRYPOINT ["PROVER/eprover"]
CMD ["-h"]
