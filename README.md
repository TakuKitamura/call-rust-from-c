# Call Rust-Code from C-Code

## Dependencies
- rust
- cbindgen

## Run
```bash
$ make build
cargo build --release && cbindgen --config cbindgen.toml --lang c --crate rust --output rust.h && gcc main.c target/release/librust.a
    Finished release [optimized] target(s) in 0.00s
$ make run
./a.out
Hello, world!
```
