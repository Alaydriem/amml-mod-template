<div align="center">

<img src="./assets/readme.png" alt="__TITLE__" width="256">

# Alaydriem's __TITLE__

[![Release](https://img.shields.io/github/v/release/alaydriem/amml-__MOD__?include_prereleases)](https://github.com/alaydriem/amml-__MOD__/releases)
[![Build](https://img.shields.io/github/actions/workflow/status/alaydriem/amml-__MOD__/build.yml?branch=master&label=build)](https://github.com/alaydriem/amml-__MOD__/actions/workflows/build.yml)
[![License](https://img.shields.io/github/license/alaydriem/amml-__MOD__)](./LICENSE)
![Minecraft Bedrock](https://img.shields.io/badge/Minecraft_Bedrock-__MC_VERSION__-62B47A)
[![AMML](https://img.shields.io/badge/AMML-mod-4A90D9)](https://github.com/alaydriem/amml)

</div>

<!-- init:begin -->
> **This is the AMML mod template.** To start a new mod: click "Use this template" on GitHub, clone the new repo, then run:
>
> ```powershell
> mise trust
> mise run init --name <kebab-name> --title "<Title>" --namespace <amml|alaydriem> [--mc-version 1.26.63]
> ```
>
> `--namespace` is required: `amml` for the core mods, `alaydriem` for every other mod. `init` fills in every placeholder, removes this note, and deletes itself.
<!-- init:end -->

TODO: one-line summary of the mod.

## Features

TODO

## Installation

Install it with the [AMML launcher](https://github.com/alaydriem/amml/releases/latest). The launcher also installs the AMML loader and Alaydriem's Mod Manager, which this mod needs.

## Configuration

Settings are in the mod manager panel and saved to `mods/amml/@__NAMESPACE__/__MOD__/config/config.hcl`.

TODO

## Building

Requires Windows x64, [mise](https://mise.jdx.dev), rustup and [cargo-nextest](https://nexte.st). The AMML SDK and the mod manager crates are git dependencies on their public release tags (`Cargo.toml`); cargo fetches them.

```powershell
mise trust
mise run preflight
mise run package
mise run test
```

`mise run package` writes `dist/@__NAMESPACE__/__MOD__/` (`__NAMESPACE_____MOD_SNAKE__.dll` and `amml.hcl`). `mise run install --instance <name>` runs `package`, then copies it into `%LOCALAPPDATA%\amml\instances\<name>\mods\amml\@__NAMESPACE__\__MOD__\`. Close the game first.

Commit `Cargo.lock`. The release workflow updates it and fails if git does not track it.

## License

BSD 3-Clause. Copyright (c) 2026 Charles R. Portwood II. See [LICENSE](./LICENSE).
