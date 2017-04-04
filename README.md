# parity-wasm

## Rust WebAssembly format serializing/deserializing

```rust

extern crate parity_wasm;

let module = parity-wasm::deserialize_file("./res/cases/v1/hello.wasm");
assert_eq!(module.code_section().is_some());

let code_section = module.code_section().unwrap(); // Part of the module with functions code

println!("Function count in wasm file: {}", code_section.bodies().len());
```
