# mkb79/homebrew-tap

Homebrew formulae for [mkb79](https://github.com/mkb79)'s projects.

```sh
brew install mkb79/tap/audible-rs
```

## Formulae

| Formula | What it installs |
| --- | --- |
| `audible-rs` | The `audible` command — a command-line client for your Audible library ([mkb79/audible-rs](https://github.com/mkb79/audible-rs)) |

## Notes

**`audible-rs` installs a prebuilt binary**, not a source build: the project publishes one archive per target and the formula verifies it against the release's checksums. On Linux the binary is statically linked against musl, so it does not depend on the host's glibc.

**The formula is generated.** The `audible-rs` release workflow rewrites version and checksums on every release and pushes the result here — so `brew upgrade` follows releases without anyone remembering to bump anything. Do not edit `Formula/audible-rs.rb` by hand; the next release overwrites it.

**Pre-1.0.** `audible-rs` currently ships pre-releases only, and the formula tracks them. Expect breaking changes between versions, and read the release notes before upgrading — some of them change the local database.

**Careful with a second installation.** If you also installed `audible` via `install.sh` (into `~/.local/bin`), you now have two binaries and `PATH` order decides which one runs — Homebrew usually puts itself first. Pick one.
