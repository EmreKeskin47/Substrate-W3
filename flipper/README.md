rustup component add rust-src

rustup target add wasm32-unknown-unknown --toolchain nightly

cargo install --force --locked cargo-contract --version 2.0.0-rc
