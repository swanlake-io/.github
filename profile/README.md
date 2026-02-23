# SwanLake

[![CI](https://github.com/swanlake-io/swanlake/actions/workflows/ci.yml/badge.svg)](https://github.com/swanlake-io/swanlake/actions/workflows/ci.yml)
[![codecov](https://codecov.io/github/swanlake-io/swanlake/graph/badge.svg?token=BPEVOE3Z8Y)](https://codecov.io/github/swanlake-io/swanlake)

SwanLake is an Arrow Flight SQL server backed by DuckDB, designed for fast analytics and ingestion with DuckLake data lake support.

- Website: <https://swanlake.io>
- Main repository: <https://github.com/swanlake-io/swanlake>
- Container image: <https://github.com/swanlake-io/swanlake/pkgs/container/swanlake>

## Quick Start

Run the server:

```bash
# from source
RUST_LOG=info cargo run --bin swanlake

# or with Docker
docker run --rm -p 4214:4214 -p 4215:4215 ghcr.io/swanlake-io/swanlake:latest
```

Connect with the CLI:

```bash
cargo run --bin swanlake-cli --features="cli"
```

By default:
- Flight SQL endpoint: `grpc://127.0.0.1:4214`
- Status page: `http://127.0.0.1:4215`

## Why SwanLake

- Arrow Flight SQL over gRPC for efficient SQL query and ingestion flows
- DuckDB execution engine with optional DuckLake integrations
- Session-aware architecture with Rust client pooling for parallelism
- Built-in status page with latency percentiles, slow queries, and recent errors
- Environment-variable driven runtime configuration

## Docs and Examples

- Overview: <https://swanlake.io/docs/overview/>
- Quick Start guide: <https://swanlake.io/docs/getting-started/quickstart/>
- Configuration reference: <https://github.com/swanlake-io/swanlake/blob/main/CONFIGURATION.md>
- Benchmark report: <https://github.com/swanlake-io/swanlake/blob/main/BENCHMARK.md>
- Go example: <https://github.com/swanlake-io/swanlake/tree/main/examples/go-adbc>
- Rust example: <https://github.com/swanlake-io/swanlake/tree/main/examples/rust-adbc>
- Python example: <https://github.com/swanlake-io/swanlake/tree/main/examples/python-adbc>

## Repositories

- `swanlake`: Flight SQL server, Rust client, and examples
- `swanlake.github.io`: project website and docs source
