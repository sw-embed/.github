## sw-embed — software for embedded targets

Operating systems, language ports and toolchains for small hardware, target by
target. **47 repositories** of my own here, and one fork.

COR24 — MakerLisp's 24-bit RISC for FPGAs — is the first target and most of
what is here today. It set the pattern the rest will follow: an ISA model, an
emulator, an assembler, a debugger, a monitor, an operating system, and then a
dozen languages ported onto it, each implemented in a *different* host language
on purpose, most with a browser demo you can run from a link.

The pattern is meant to repeat. [risc-v-rs](https://github.com/sw-embed/risc-v-rs)
is the second target already here, and ESP32-xx, the Lychee boards and ARM are
next — each in time with its own operating system and its own ports of the same
languages, so the same program can be compared across machines.

### Run something first

| | |
|---|---|
| [web-sw-cor24-demos](https://github.com/sw-embed/web-sw-cor24-demos) | The demo landing page: every live browser demo in one place. |
| [cor24-rs](https://github.com/sw-embed/cor24-rs) | The COR24 emulator itself, Yew/Rust/WASM. Start here to see a machine run. |
| [risc-v-rs](https://github.com/sw-embed/risc-v-rs) | A RISC-V emulator, same approach, different target. |
| [web-sw-tos](https://github.com/sw-embed/web-sw-tos) | Tiny O/S, TUI and all, in a browser tab. |
| [web-sw-cor24-assembler](https://github.com/sw-embed/web-sw-cor24-assembler) | A browser-based COR24 assembly IDE and emulator. |

### Then read the code

| | |
|---|---|
| [sw-cor24-isa](https://github.com/sw-embed/sw-cor24-isa) | The ISA itself: opcodes, encoding, registers. Everything else agrees with this. |
| [sw-tos](https://github.com/sw-embed/sw-tos) | Tiny O/S. The first of what will be several operating systems, one per target family. |
| [sw-cor24-forth](https://github.com/sw-embed/sw-cor24-forth) · [sw-cor24-macrolisp](https://github.com/sw-embed/sw-cor24-macrolisp) · [sw-cor24-plsw](https://github.com/sw-embed/sw-cor24-plsw) | Forth in assembler, a Lisp-1 with closures and GC, and my own PL/I-inspired systems language. |
| [sw-cor24-apl](https://github.com/sw-embed/sw-cor24-apl) · [sw-cor24-prolog](https://github.com/sw-embed/sw-cor24-prolog) · [sw-cor24-smalltalk](https://github.com/sw-embed/sw-cor24-smalltalk) · [sw-cor24-snobol4](https://github.com/sw-embed/sw-cor24-snobol4) | APL, a WAM-like Prolog, a Smalltalk written in Tiny BASIC, and SNOBOL4 built on PL/SW. |

39 more are here — the full list is under
[Repositories](https://github.com/orgs/sw-embed/repositories), and grouped by
subject in [the index](https://github.com/softwarewrighter/softwarewrighter).

### How the names work

A repository named `web-<something>` is the browser front end for the thing
after it. `sw-<target>-<part>` is one target taken apart into the same pieces —
`sw-cor24-isa`, `sw-cor24-asm`, `sw-cor24-emulator` — which is what makes a
second target a matter of filling in the same slots. A name like `tf24a` decodes
as *Tiny Forth for COR24, in Assembler*: the host language is the last letter,
and swapping it is the exercise.

### What makes retargeting cheap

- [sw-langtools](https://github.com/sw-langtools) holds the shared machinery: a
  target-independent SSA representation, and ISA, codegen and target cores.
- [gen-isa](https://github.com/sw-vibe-coding/gen-isa) generates the emulator,
  assembler and tooling for a *new* target ISA.
- [hardwarewrighter](https://github.com/hardwarewrighter) is the hardware these
  run on: the FPGA boards, the ESP32 carrier, the bench instruments.

### Where the rest is

- [sw-cor24-project](https://github.com/sw-embed/sw-cor24-project) — the
  umbrella repository for COR24: docs, and links to every part.
- [**The index**](https://github.com/softwarewrighter/softwarewrighter) — all
  251 public repositories across all 15 accounts, including the historic
  machines, the compiler machinery and the machine-learning work.
- [The blog](https://blog.softwarewrighter.com) — most of this was written up
  while it was being built.
