# luauc-toolkit

Pure-luau library providing utilities for assembling, dissecting and executing
luau bytecode.

This library is work in progress and most features aren't implemented properly.

## Todo

- [x] An intermediate table format ("IR")
    - [X] Encoder
    - [X] Decoder
- [ ] A Luau Bytecode Assembler ("LASM") for creating custom bytecode chunks
    - [ ] `P` Formal Grammar
    - [ ] `P` VSC Textmate Grammar
    - [ ] `P` Lexer
    - [ ] `P` Parser
    - [ ] Analyser (to convert AST to IR)
    - [ ] `??` a very basic LSP
- [ ] `P` Disassembler (emits LASM source from a given bytecode chunk/ir)
- [ ] `?` A bytecode interpeter?
- [ ] Optimisations
    - [ ] `P` Strip debug info
    - [ ] `?` Inlining
    - [ ] `?` Unrolling
- [ ] `??` Decompiler
- [ ] Come up with a decent name

||Meaning|
|-|-|
||planned|
|`?`|most likely|
|`??`|maybe|
|`???`|probably not|
|`P`|prototype already completed|

## Notes

- For performance reasons, the IR encoder will not attempt to validate the
passed data and makes no guarantees that a successful emits bytecode that can
be ran by a luau interpreter. It is the callers responsibility to ensure the
data is valid. No runtime checks will be performed by either the encoder or
decoder, except for those implemented in dependencies and the luau standard
library.
