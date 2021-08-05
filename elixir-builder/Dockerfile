FROM bitwalker/alpine-elixir:1.12.2
ENV MIX_ENV=prod
ENV REPLACE_OS_VARS=true
ENV RUSTFLAGS="-C target-feature=-crt-static"
RUN apk add --no-cache cargo rust git alpine-sdk

RUN mix local.hex --force
RUN mix local.rebar --force
WORKDIR /app

