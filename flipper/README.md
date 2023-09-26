rustup component add rust-src

rustup target add wasm32-unknown-unknown --toolchain nightly

cargo install --force --locked cargo-contract --version 2.0.0-rc

rustup update stable
rustup install 1.69
rustup default 1.69
rustup component add rust-src --toolchain 1.69
rustup target add wasm32-unknown-unknown --toolchain 1.69
cargo contract build

# Run node in seperate terminal

substrate-contracts-node --log info,runtime::contracts=debug 2>&1

# Build

cargo contract build --release

# Instantiate

cargo contract instantiate --constructor new --args "false" --suri //Alice --salt $(date +%s)

# Instantiate Output

Contract 5HSyM96UqvHUGU9PaNAAyUuXqt9hiFptFShAdbDArnvJVyB5

# get() message

cargo contract call --contract $INSTANTIATED_CONTRACT_ADDRESS --message get --suri //Alice --dry-run

# flip() message

cargo contract call --contract $INSTANTIATED_CONTRACT_ADDRESS --message flip --suri //Alice
