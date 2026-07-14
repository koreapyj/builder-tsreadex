# builder-tsreadex

Unofficial, automated Debian/Ubuntu package builds of
[xtne6f/tsreadex](https://github.com/xtne6f/tsreadex).

A scheduled GitHub Actions workflow checks upstream's latest GitHub release
daily. When a new tag appears that hasn't been packaged here yet, it builds
`.deb` packages for:

| Distro | Codename | Version suffix |
|---|---|---|
| Debian 11 | bullseye | `~deb11` |
| Debian 12 | bookworm | `~deb12` |
| Debian 13 | trixie | `~deb13` |
| Ubuntu 22.04 | jammy | `~ubuntu22.04` |
| Ubuntu 24.04 | noble | `~ubuntu24.04` |
| Ubuntu 26.04 | resolute | `~ubuntu26.04` |

on **amd64** and **arm64**, and publishes them as a GitHub release here under
the same tag name as upstream
(e.g. `master-260428`).

## Installing

Download the `.deb` for your distro/arch from the Releases page, then:

```sh
sudo dpkg -i tsreadex_<version>_<arch>.deb
```

Not affiliated with upstream. MIT-licensed — see `debian/copyright`.
