# gruen/homebrew-tap

Homebrew tap for [tailport](https://github.com/gruen/tailport) — a TUI to
expose local ports across your tailnet via `tailscale serve`.

```sh
brew install gruen/tap/tailport
```

## Notes

- **Source build.** The formula compiles from the release tarball rather than
  shipping a bottle, so it works on both Apple Silicon and Intel Macs (and
  Linuxbrew). tailport's release CI publishes no `darwin/amd64` binary, so a
  prebuilt formula would strand Intel Macs; building from source sidesteps that.
- **`tailscale` is a runtime dependency** — tailport shells out to the
  `tailscale` CLI for `serve`/`funnel`.
- The canonical copy of this formula lives in the tailport repo under
  [`packaging/brew/`](https://github.com/gruen/tailport/tree/main/packaging/brew),
  alongside the AUR PKGBUILDs. Changes should be made there and copied here.
