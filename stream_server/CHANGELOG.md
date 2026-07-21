# Changelog

## 0.3.0

- Publishes native `aarch64` and `amd64` container images to GitHub Container Registry.
- Publishes a generic multi-architecture image manifest.
- Configures Home Assistant to download the versioned prebuilt image instead of compiling Rust locally.
- Keeps native build validation and the `/heartbeat` smoke test before publishing.

## 0.2.0

- Renames the Home Assistant app to **Stream Server for Home Assistant**.
- Changes the app slug from `stremio_stream_engine` to `stream_server_home_assistant`.
- Aligns container metadata, CI image names and documentation with the repository name.
- This slug change creates a new Home Assistant app identity; an installed `stremio_stream_engine` prototype must be removed before installing the renamed app.

## 0.1.0

- Initial Home Assistant app package.
- Published from its own dedicated Home Assistant app repository.
- Builds `perpetus/stream-server` v0.1.8 for `aarch64` and `amd64`.
- Uses the upstream-supported `libtorrent` torrent backend.
- Exposes the Stremio-compatible API on TCP port 11470.
- Persists configuration and cache under `/data`.
- Adds health monitoring through the `/heartbeat` endpoint.
