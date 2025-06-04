FROM gcc:14 AS compilation
WORKDIR /projet
COPY prog.c .
RUN  gcc -o prog prog.c

FROM debian:12
COPY --from=compilation /projet/prog /bin
CMD  ["/bin/prog"]
