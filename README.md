# Birun Agents

`birun-agents` is the public signed package repository for agents that run on
BirunOS. Release bundles currently provide the repository metadata and package
artifacts used to install PicoClaw and upstream Hermes Agent through the BirunOS
repository, lifecycle, runtime, model, MCP, and state authority boundaries.

## Boundary

- Packages declare their runtime, state, model, MCP, network, UI, and permission
  requirements; they do not grant themselves authority.
- BirunOS verifies repository metadata and package digests before installation.
- Agent package rootfs and durable owner state are separate lifecycle domains.
- Repository releases contain no provider credentials, owner data, or production
  secrets.
- Hosted commercial cloud agents, if added later, belong to a separate product
  boundary and are not the purpose of this repository.

The active package/runtime contracts and end-to-end acceptance stories live in
the [`birunos`](https://github.com/birunos/birunos) repository.
