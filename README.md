# Gleam Docker Images with Erlang/OTP 27

This repository provides Docker images for the [Gleam programming language](https://gleam.run/). These images are ready-to-use environments for developing and running Gleam applications.

## Table of Contents

- [Overview](#overview)
- [Images](#images)
- [Installation](#installation)
- [Usage](#usage)
- [Building Locally](#building-locally)
- [License](#license)

## Overview

Gleam is a type-safe, functional programming language for building scalable systems and applications. By providing Docker images with Gleam, Erlang/OTP 27, and Elixir, we aim to simplify the setup process and help you get started quickly.

## Images

We offer two Docker images:

- **Gleam with Erlang/OTP 27**: Contains Gleam and Erlang/OTP 27.
- **Gleam with Elixir and Erlang/OTP 27**: Contains Gleam, Elixir, and Erlang/OTP 27.

## Installation

You can pull the images from the GitHub Container Registry:

### Pull Gleam with Erlang/OTP 27

```bash
docker pull ghcr.io/crocoder-dev/gleam:latest
```

### Pull Gleam with Elixir and Erlang/OTP 27

```bash
docker pull ghcr.io/crocoder-dev/gleam-elixir:latest
```

## Usage

### Running the Container

Run the container interactively to access Gleam commands:

#### Gleam with Erlang/OTP 27

```bash
docker run -it ghcr.io/crocoder-dev/gleam:latest gleam --help
```

#### Gleam with Elixir and Erlang/OTP 27

```bash
docker run -it ghcr.io/crocoder-dev/gleam-elixir:latest gleam --help
```

### Using with a Project

Mount your project directory into the container:

```bash
docker run -it -v $(pwd):/app -w /app ghcr.io/crocoder-dev/gleam:latest gleam build
```

## Building Locally

If you prefer to build the images yourself, use the provided Dockerfiles.

### Build Gleam with Erlang/OTP 27

```bash
cd gleam-otp27
docker build -t gleam:local .
```

### Build Gleam with Elixir and Erlang/OTP 27

```bash
cd gleam-elixir-otp27
docker build -t gleam-elixir:local .
```

## License

This project is licensed under the MIT License.
