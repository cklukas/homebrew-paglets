# Homebrew tap for paglets

```sh
brew install cklukas/paglets/paglets
```

Installs the C++ edition of [paglets](https://github.com/cklukas/paglets/tree/cpp):
mobile agents as WebAssembly modules that move between hosts with their state.

- `paglets-host`: runs paglets, hosts of a mesh, the mesh ledger and the
  `remote` commands for live hosts;
- `paglets-worker`: runs paglet instances in a sandbox for `paglets-host`;
- `paglets-web`: a local web UI for a mesh, with the matching shell commands;
- the guest SDK and CMake package (`find_package(paglets)`) for building your
  own paglets (with `brew install llvm lld wasi-libc wasi-runtimes`).

Documentation: https://cklukas.github.io/paglets/cpp/

The formula is built from the source archive of each `cpp-v*` release. The
release workflow of the paglets repository
([`cpp-release.yml`](https://github.com/cklukas/paglets/blob/cpp/.github/workflows/cpp-release.yml))
updates `Formula/paglets.rb`; its source is
[`cpp/packaging/homebrew/paglets.rb`](https://github.com/cklukas/paglets/blob/cpp/cpp/packaging/homebrew/paglets.rb).

To update: `brew update` then `brew upgrade paglets`.
