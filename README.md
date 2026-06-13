# pacskage

A tiny package manager for [Skript](https://github.com/SkriptLang/Skript). Requires skript-reflect.

## Install

```
curl -o plugins/Skript/scripts/package.sk https://raw.githubusercontent.com/miberss/pacskage/HEAD/package.sk
```

## Use

```
/package install <git url>
/package (update|remove|enable|disable|info) <name>
/package (list|check)
```

Packages are installed into `scripts/packages/`. See
[pacskage-example](https://github.com/miberss/pacskage-example) for the
`package.txt` manifest format.
