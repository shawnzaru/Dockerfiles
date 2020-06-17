# usage:
# > docker run --rm -it -v ${PWD}:/problems shawnzaru/prover9 /problems/ex25.in
#
# N.B. in provers.src/Makefile, move all '-lm' to the end of the line

FROM alpine:latest
WORKDIR /LADR-2009-11A
COPY . .
RUN apk add --no-cache gcc libc-dev make
RUN make all
ENTRYPOINT ["bin/prover9", "-f"]
