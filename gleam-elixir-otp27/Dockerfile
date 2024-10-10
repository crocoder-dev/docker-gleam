FROM rust:1.81.0 AS build

ENV GLEAM_VERSION="v1.5.1"

RUN git clone https://github.com/gleam-lang/gleam.git --branch ${GLEAM_VERSION} \
	&& cd gleam \
	&& make install

RUN gleam --version

FROM elixir:1.17.3-otp-27

COPY --from=build /usr/local/cargo/bin/gleam /bin

CMD ["gleam"]
