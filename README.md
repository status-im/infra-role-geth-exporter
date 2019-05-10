# Description

This role configures [`geth_exporter`](https://github.com/status-im/geth_exporter), a metrics exporter for ([go-ethereum](https://github.com/ethereum/go-ethereum)).

The image used by default is [statusteam/geth_exporter:latest](https://hub.docker.com/r/statusteam/geth_exporter).

# Configuration

```yaml
```

# Known Issues

Currently only connecting via an IPC socket is supported by `geth_exporter`, RPC HTTP is not supported.
