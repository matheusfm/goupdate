# goupdate

A small Bash script to check for and install the latest Go release on Linux.

It manages the official tarball installation in `/usr/local/go`, as described in the [Go install docs](https://go.dev/doc/install).

## Install

```bash
curl -fsSL -o ~/.local/bin/goupdate https://raw.githubusercontent.com/matheusfm/goupdate/main/goupdate
chmod +x ~/.local/bin/goupdate
```

Make sure `~/.local/bin` is in your `PATH`.

## Usage

```bash
goupdate check     # is the installed Go the latest version?
goupdate install   # download and install the latest version
```

`check` exits with code `1` when an update is available, so it can be used in scripts.

`install` downloads the release for your architecture, verifies its SHA-256 checksum and replaces `/usr/local/go` (requires `sudo`).

## Requirements

`bash`, `curl`, `tar`, `sha256sum` and `sudo`.

## License

[MIT](LICENSE)
