# Local Parachain

## Clone Polkadot

git clone --branch release-v0.9.37 https://github.com/paritytech/polkadot.git

## Run Polkadot

cd polkadot
cargo build --release
./target/release/polkadot --help

## 1st Node

./target/release/polkadot \
--alice \
--validator \
--base-path /tmp/relay/alice \
--chain /tmp/raw-local-chainspec.json \
--port 30333 \
--ws-port 9944

## 2nd Node

./target/release/polkadot \
--bob \
--validator \
--base-path /tmp/relay-bob \
--chain /tmp/raw-local-chainspec.json \
--port 30334 \
--ws-port 9945
