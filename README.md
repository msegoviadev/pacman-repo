# pacman-repo

Personal, GPG-signed [pacman repository](https://wiki.archlinux.org/title/Pacman/Tips_and_tricks#Custom_local_repository) hosting binary packages for x86_64 and aarch64, published on GitHub Pages from the `gh-pages` branch.

## Use this repository

One-time setup:

```bash
# Trust the signing key
curl -fsSL https://msegovia.dev/pacman-repo/msegoviadev.asc | sudo pacman-key --add -
sudo pacman-key --lsign-key ABD517389B8A1447971AE05F7A1E0EC939A79CBC

# Add the repository to /etc/pacman.conf
[msegoviadev]
Server = https://msegovia.dev/pacman-repo/$arch

# Refresh and install
sudo pacman -Sy
sudo pacman -S <package>
```

## Packages

| Package | Description | Source |
|---------|-------------|--------|
| `termurl` | Terminal client for Hurl collections with an agent-friendly headless CLI | [msegoviadev/termurl](https://github.com/msegoviadev/termurl) |

## Key

- Fingerprint: `ABD517389B8A1447971AE05F7A1E0EC939A79CBC`
- UID: `msegoviadev (pacman repo) <contact@msegovia.dev>`
- Public key: [`msegoviadev.asc`](msegoviadev.asc)
