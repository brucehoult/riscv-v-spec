# riscv-v-spec
RISC-V V vector extension 1.0.

[Version 1.0](https://github.com/riscv/riscv-v-spec/releases/tag/v1.0)
has been frozen and ratified. At present it is available only in Spike and QEMU and
the Kendryte K230 SoC found in the CanMV-K230 board. A number of other SoCs and boards
using them have been announced to be available later in 2024, including Sophgo SG2380, SG2044,
SpacemiT K1.

[Draft Version 0.7.1](https://github.com/brucehoult/riscv-v-spec/tree/0.7.1) has been
implemented by THead in their C906 and C910/C920 cores and widely sold in SoCs including
the AllWinner D1, Bouffalo BL808, Cvitek CV1800B, Sophgo SG2002 and SG2042, THead TH1520.

Other stable releases are
[v1.0-rc2](https://github.com/riscv/riscv-v-spec/releases/tag/v1.0-rc2),
[v1.0-rc1](https://github.com/riscv/riscv-v-spec/releases/tag/v1.0-rc1),
[v0.10](https://github.com/riscv/riscv-v-spec/releases/tag/v0.10),
[v0.9](https://github.com/riscv/riscv-v-spec/releases/tag/0.9), and
[v0.8](https://github.com/riscv/riscv-v-spec/releases/tag/0.8).
Note, these previous releases were for experimental development purposes only and are not standard versions suitable for production use. Significant incompatible changes were made from these earlier versions prior to freezing.

The top level file is [v-spec.adoc](./v-spec.adoc)

Simply clicking on the file in the github repo viewer will render a usable
version as markdown.

For a better rendering, use the documentation build process described
below.

This work is licensed under a Creative Commons Attribution 4.0
International License. See the LICENSE file for details.

### Additional Resources

- The [Spike simulator](https://github.com/riscv/riscv-isa-sim) supports v1.0.
- The [RISC-V Proxy Kernel](https://github.com/riscv/riscv-pk)
  (to be used with e.g. Spike) supports v1.0 binaries.
- The [Binutils port for v0.8](https://github.com/riscv/riscv-binutils-gdb/tree/rvv-0.8.x)
- The [GNU toolchain port for v0.8](https://github.com/riscv/riscv-gnu-toolchain/tree/rvv-0.8.x)
- [riscvOVPsim](https://github.com/riscv/riscv-ovpsim) is a free
  RISC-V reference simulator that has support for v0.9, v0.8 and
  v0.7.1 (simulator is under a proprietary license, models are
  open source)

### Documentation generator

Requirements

`node v6+`

**Linux**: install using [nvm](https://github.com/creationix/nvm)

**macOS Homebrew**: `brew install node`

**macOS Macports**: `sudo port install npm6`

**Windows**: [nodejs.org](https://nodejs.org/en/download/)

Install documentation generator

`npm i`

Build HTML/PDF documents

`npm run build`

Resulted files

`public/*`
