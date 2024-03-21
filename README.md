# riscv-v-spec
Working draft 0.7.1 of the proposed RISC-V V vector extension.

The top level file is [v-spec.adoc](./v-spec.adoc)

---

This draft version of RVV has been implemented by THead in their C906 and C910/C920
cores and widely sold in SoCs including the AllWinner D1, Bouffalo BL808, Cvitek CV1800B,
Sophgo SG2002 and SG2042, THead TH1520.

The only divergence I'm aware of from this spec is the addition of the `vlenb` CSR (0xC22,
same as in 1.0) returning VLEN/8 the vector register length in bytes i.e. 16 for all THead
implementations to date.

The optional EDIV extension is not implemented.

There is a [GCC 9.4 toolchain](https://github.com/brucehoult/riscv-gnu-toolchain) snapshot supporting this spec as written,
as the "v" extension e.g. `-march=rv64gcv`. The support is primarily in binutils, with gcc knowing how to pass the
correct flags through, thus allowing the `gcc` driver to assemble `.s` files using RVV 0.7.1, or to use  inline asm in C.

THead have upstreamed this spec (plus `vlenb`, minus `EDIV`) as `_XTheadVector` in GCC 14 and later. The functionality is as in
this spec but all instruction and CSR mnemonics are prefixed with `th.`.

THead have also added some pseudo instructions to enable the use of RVV 1.0 instruction mnemonics where they differ. See their
[documentation](https://github.com/T-head-Semi/thead-extension-spec/blob/master/xtheadvector.adoc) for details.

C intrinsics for RVV can generate either 1.0 or 0.7.1 instructions, depending on whether `v` or `_xtheadvector` is included
in the ISA specification.

---

Simply clicking on the file in the github repo viewer will render a usable
version as markdown.

For a better rendering, use "asciidoctor v-spec.adoc".

This work is licensed under a Creative Commons Attribution 4.0
International License. See the LICENSE file for details.

[[HTML](https://riscv.github.io/documents/riscv-v-spec/)] [[PDF](https://riscv.github.io/documents/riscv-v-spec/riscv-v-spec.pdf)]

### Documentation generator

Requirements

`node v6+`

**Linux**: install using [nvm](https://github.com/creationix/nvm)

**OSX**: `brew install node`

**Windows**: [nodejs.org](https://nodejs.org/en/download/)

Install documentation generator

`npm i`

Build HTML/PDF documents

`npm run build`

Resulted files

`public/*`
