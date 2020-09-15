FROM elixir:1.10-alpine
ENV MIX_ENV=prod
ENV REPLACE_OS_VARS=true
ENV RUSTFLAGS="-C target-feature=-crt-static"
RUN apk add --no-cache cargo rust git

RUN mix local.hex --force
RUN mix local.rebar --force
WORKDIR /app

