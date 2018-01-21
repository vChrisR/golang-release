# golang

This is an ARMv7 (and v6) bosh-release of Golang.

Note: requires bosh-cli version `v2.0.36` to `vendor-package` and `create-release`.

To vendor golang package into your release, run:

```
$ git clone https://github.com/bosh-packages/golang-release
$ cd ~/workspace/your-release
$ bosh vendor-package golang-1.9-linux ~/workspace/golang-release
```

Included packages:

- golang-1.9-armv7-linux

To use `golang-*` package for compilation in your packaging script:

```bash
#!/bin/bash -eu
source /var/vcap/packages/golang-1.9-armv7-linux/bosh/compile.env
go build ...
```

[advanced use] To use `golang-*` package at runtime in your job scripts:

```bash
#!/bin/bash -eu
source /var/vcap/packages/golang-1.9-armv7-linux/bosh/runtime.env
go run ...
```
