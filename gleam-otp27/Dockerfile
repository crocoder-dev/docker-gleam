FROM rust:1.81.0 AS build

ENV GLEAM_VERSION="v1.5.1"

RUN git clone https://github.com/gleam-lang/gleam.git --branch ${GLEAM_VERSION} \
	&& cd gleam \
	&& make install

RUN gleam --version

FROM erlang:27.1

COPY --from=build /usr/local/cargo/bin/gleam /bin

CMD ["gleam"]
