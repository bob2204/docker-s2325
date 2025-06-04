FROM gcc:14 AS compilation
WORKDIR /projet
COPY prog.c .
RUN  gcc -o prog -static prog.c

FROM scratch
COPY --from=compilation /projet/prog /prog
CMD  ["/prog"]
