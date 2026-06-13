# pacskage

A tiny package manager for [Skript](https://github.com/SkriptLang/Skript). Requires skript-reflect.

## Install

```
curl -o plugins/Skript/scripts/package.sk https://raw.githubusercontent.com/miberss/pacskage/HEAD/package.sk
```

## Use

```
/package install <git url>[@version]
/package (update|remove|enable|disable|info) <name>
/package (list|check|outdated|awesome)
```

Packages are installed into `scripts/packages/`. Browse available packages at
[awesome-pacskage](https://github.com/miberss/awesome-pacskage).

Append `@version` to an install url to pin a specific tag, branch, or commit
instead of the default branch.

## Manifest

A package may include a `package.txt` describing it:

```
name: my-package
version: 1.0.0
description: what it does
requires: skript >= 2.15, skript-reflect >= 2.6
packages: https://github.com/someone/other-package
```

All fields are optional:

- `name` sets the package name (otherwise taken from the install url).
- `version` is compared on `update`.
- `description` is shown by `info`.
- `requires` lists plugins, comma-separated, each `name` or `name >= version`.
- `packages` lists dependencies, comma-separated. A git url is installed for
  you, a bare name is only checked.

`origin` is added automatically on install, so don't set it yourself. See
[pacskage-example](https://github.com/miberss/pacskage-example) for a full
example.

## License

[Unlicense](LICENSE) (public domain).
