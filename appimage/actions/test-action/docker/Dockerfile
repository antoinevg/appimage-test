FROM debian:10 AS builder
LABEL maintainer="Great Scott Gadgets <dev@greatscottgadgets.com>"
LABEL stage="builder"


# - squish --------------------------------------------------------------------

FROM debian:10
COPY --from=builder / /

ENV HOME="/home/runner"

USER runner
WORKDIR $HOME
