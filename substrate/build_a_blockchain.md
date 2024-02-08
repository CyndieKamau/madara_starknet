- A blockchain consists of decentralized computers—called nodes—to form a network.
- We'll build and start a single node blockchain using the node template.

## Objectives

- Compile the node template and start a local Substrate-based blockchain.
- Install a front-end template to interact with the local blockchain node.
- Use the front-end template to submit a transaction and view the result.

## 1. Prerequisites
- Good internet Connection
- Access to shell terminal
- Familiarity with blockchains

## 2. Compile a Substrate node

- Clone the substrate node repo:

```sh
git clone https://github.com/substrate-developer-hub/substrate-node-template
```

- Change to the root of the node template directory 

```sh
cd substrate-node-template
```

- Create a new branch to contain your work:

```sh
git switch -c my-learning-branch-yyyy-mm-dd
```

- Compile the node template:

```sh
cargo build --release
```






