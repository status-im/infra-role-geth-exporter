# Description

This role configures [`geth_exporter`](https://github.com/status-im/geth_exporter), a metrics exporter for [go-ethereum](https://github.com/ethereum/go-ethereum).

The image used by default is [statusteam/geth_exporter:latest](https://hub.docker.com/r/statusteam/geth_exporter).

# Installation

```yaml
- name: infra-role-geth-exporter
  src: git+git@github.com:status-im/infra-role-geth-exporter.git
  scm: git
```

# Configuration

The main thing to change is name of container to connect to and IPC path:
```yaml
geth_source_cont_name: 'my-geth-container'
```

The rest of the defaults should be fine, but if you want to change anything change those:
```yaml
geth_expo_cont_name: 'metrics-geth-01'
geth_expo_cont_port: 9300
```

# Known Issues

Currently only connecting via an IPC socket is supported by `geth_exporter`, RPC HTTP is not supported.
