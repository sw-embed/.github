## sw-embed — COR24, and everything written for it

COR24 is MakerLisp's 24-bit RISC for FPGAs. I did not design it; I adopted it
and then built the world around it, and this organisation is that world:
**47 repositories** of emulator, assembler, monitor, debugger, operating
system, FPGA target — and a dozen languages hosted on the same machine, each
implemented in a different host language on purpose.

### Run something first

| | |
|---|---|
| [web-sw-cor24-demos](https://github.com/sw-embed/web-sw-cor24-demos) | The demo landing page: every live browser demo in one place. |
| [cor24-rs](https://github.com/sw-embed/cor24-rs) | The emulator itself, Yew/Rust/WASM. Start here to see the machine run. |
| [web-sw-tos](https://github.com/sw-embed/web-sw-tos) | Tiny O/S, TUI and all, in a browser tab. |
| [web-sw-cor24-assembler](https://github.com/sw-embed/web-sw-cor24-assembler) | A browser-based COR24 assembly IDE and emulator. |

### Then read the code

| | |
|---|---|
| [sw-cor24-isa](https://github.com/sw-embed/sw-cor24-isa) | The ISA itself: opcodes, encoding, registers. Everything else agrees with this. |
| [sw-tos](https://github.com/sw-embed/sw-tos) | The operating system. |
| [sw-cor24-forth](https://github.com/sw-embed/sw-cor24-forth) · [sw-cor24-macrolisp](https://github.com/sw-embed/sw-cor24-macrolisp) · [sw-cor24-plsw](https://github.com/sw-embed/sw-cor24-plsw) | Forth in assembler, a Lisp-1 with closures and GC, and my own PL/I-inspired systems language. |
| [sw-cor24-apl](https://github.com/sw-embed/sw-cor24-apl) · [sw-cor24-prolog](https://github.com/sw-embed/sw-cor24-prolog) · [sw-cor24-smalltalk](https://github.com/sw-embed/sw-cor24-smalltalk) · [sw-cor24-snobol4](https://github.com/sw-embed/sw-cor24-snobol4) | APL, a WAM-like Prolog, a Smalltalk written in Tiny BASIC, and SNOBOL4 built on PL/SW. |

A repository named `web-<something>` is the browser front end for the thing
after it. A name like `tf24a` decodes as *Tiny Forth for COR24, in
Assembler* — the host language is the last letter, and swapping it is the
exercise.

### Where the rest is

- [sw-cor24-project](https://github.com/sw-embed/sw-cor24-project) — the
  umbrella repository for COR24: docs, and links to every part.
- [**The index**](https://github.com/softwarewrighter/softwarewrighter) — the index
  to all 251 public repositories across all 15 organisations, including the
  historic machines, the compiler machinery these toolchains share, and the
  machine-learning work.
- [The blog](https://blog.softwarewrighter.com) — most of this was written up
  while it was being built.
