# Stream Server for Home Assistant

Home Assistant app repository for running the open-source [`perpetus/stream-server`](https://github.com/perpetus/stream-server) server locally on Home Assistant OS or Supervised installations.

The app exposes a Stremio-compatible HTTP API on port `11470` for use with the separate [`Stremio Stream Bridge`](https://github.com/diegocesaretti/stremio-stream-bridge) custom integration.

## Installation

Add this repository in the Home Assistant app store:

```text
https://github.com/diegocesaretti/stream-server-home-assistant
```

Then install **Stream Server for Home Assistant**, start it, and configure Stremio Stream Bridge to use:

```text
http://HOME_ASSISTANT_IP:11470
```

Use the Raspberry Pi or Home Assistant host LAN address rather than `localhost`, because Cast receivers must reach the stream URL directly.

Version `0.3.0` and later use prebuilt multi-architecture images from GitHub Container Registry. Home Assistant downloads the correct `aarch64` or `amd64` image instead of compiling Rust on the host.

### Prototype migration

Version `0.2.0` changed the app slug from `stremio_stream_engine` to `stream_server_home_assistant`. Home Assistant treats it as a different app. Remove the old prototype before installing the current version.

## Supported architectures

- `aarch64` — Raspberry Pi 5 and other 64-bit ARM hosts
- `amd64` — x86-64 hosts

## Upstream

The published images are built from the pinned `perpetus/stream-server` v0.1.8 release with the upstream-supported `libtorrent` backend.
