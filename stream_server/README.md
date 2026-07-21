# Stream Server for Home Assistant

Home Assistant app that runs `perpetus/stream-server` and exposes its Stremio-compatible API on port `11470`.

Use it with the **Stremio Stream Bridge** custom integration.

Home Assistant downloads a prebuilt image for the host architecture: Raspberry Pi 5 uses `aarch64` and PCs use `amd64`. Rust is not compiled on the Home Assistant host.
