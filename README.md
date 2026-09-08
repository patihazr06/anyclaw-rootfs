# anyclaw-rootfs

Public host for the Codex Enterprise Mobile Ubuntu runtime.

- Release asset `rootfs.tar.zst` (+ `.sha256`) is the Ubuntu `noble` `arm64` rootfs with Node 22, Codex CLI, OpenCode, OpenClaw, and Hermes preinstalled.
- Built by `build-rootfs` in the private app repo from the frozen `enterprise/rootfs.manifest.json`.
- Consumers:
  - `build-apk` stages it into `app/src/main/assets/rootfs/` (bundled first-run install).
  - The app falls back to downloading it from here on first setup when no bundled asset exists.

Verify: `sha256sum -c rootfs.tar.zst.sha256`
