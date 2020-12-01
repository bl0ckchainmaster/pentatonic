# How to build Pentatonic on Ubuntu 20.xx ?

## Update Packages
Update the  `/etc/apt/sources.list` to remove prefix "such as au." from there repository and then run apt update if you get timeout.

```bash
apt update
apt upgrade -y
```

## Build Requirements
```bash
apt install libclang-dev llvm g++ gcc tree curl wget tree 
```

## Install Rust (Select Nightly Build)
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
rustup install nightly
rustup update
rustup default nightly
```

## Init the Blockchain build
```
./scripts/init.sh

```
## Build the Blockchain

```bash
cargo build --release
```
and check the target/release
