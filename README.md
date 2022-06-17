## Rust for i586 architecture (x86 without SSE2) for Linux.

Following example configuration `config.toml` and patch `rustc-X.YY.Z-i586.patch`
should be applied before Rust compiler compilation from sources. A patch just fixes some
linker error due to lacks of simple declaration.

The `patch` command can be used to apply patch into source of Rust compiler:

```
patch -p1 < rustc-X.YY.Z-i586.patch
```

A `config.toml` file can be used as configuration. Some parameters can be changed (like
installation prefix). Unfortunately, this configuration needs a machine
with SSE2 instructions to build Rust compiler for i586 architecture :(.
