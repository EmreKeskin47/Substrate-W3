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
--port 30333

## 2nd Node

./target/release/polkadot \
--bob \
--validator \
--base-path /tmp/relay-bob \
--chain /tmp/raw-local-chainspec.json \
--port 30334

https://github.com/paritytech/polkadot/tree/master/node/service/chain-specs

https://raw.githubusercontent.com/paritytech/polkadot/master/node/service/chain-specs/polkadot.json

https://paritytech.github.io/substrate/master/sc_service/struct.GenericChainSpec.html
