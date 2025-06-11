# A dockerfile for 42 School's minishell project.

# Clone the minishell repo and move into the project directory.

# Pull the docker image. And then build it with:

# `docker build -t minishell .`

# Run the Minishell via:

# `docker run -it --rm minishell`

FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
 && apt-get install -y --no-install-recommends \
      build-essential \
      libreadline-dev \
      pkg-config \
 && rm -rf /var/lib/apt/lists/*

WORKDIR /usr/src/minishell

COPY . .

RUN make

ENTRYPOINT ["./minishell"]