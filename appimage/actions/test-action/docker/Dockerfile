FROM debian:10 AS builder
LABEL maintainer="Great Scott Gadgets <dev@greatscottgadgets.com>"
LABEL stage="builder"

# - setup base system ---------------------------------------------------------

USER root

# add user
RUN useradd -ms /bin/bash runner

# - squish --------------------------------------------------------------------

FROM debian:10
COPY --from=builder / /

ENV HOME="/home/runner"

USER runner
WORKDIR $HOME
