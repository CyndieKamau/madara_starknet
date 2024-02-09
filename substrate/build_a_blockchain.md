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

- A successful compilation should be like this:

```sh
 Finished release [optimized] target(s) in 12m 46s
```

## 3.Start the local node
- After the node compiles we can start the local node:

```sh
./target/release/node-template --dev

```

- The terminal output should be as follows:

```sh
2024-02-08 14:49:05 〽️ Prometheus exporter started at 127.0.0.1:9615    
2024-02-08 14:49:05 Running JSON-RPC server: addr=127.0.0.1:9944, allowed origins=["*"]    
2024-02-08 14:49:06 🙌 Starting consensus session on top of parent 0x103cf0541c0cf3601b134ecef71837ceeeb6768b76ad829e0efb47fb2fcde3ff    
2024-02-08 14:49:06 🎁 Prepared block for proposing at 1 (1 ms) [hash: 0x2333e117b007e74d63f3520951d4aab01245ee30682dd772b6be866cb1de8b64; parent_hash: 0x103c…e3ff; extrinsics (1): [0x679f…feb5]    
2024-02-08 14:49:06 🔖 Pre-sealed block for proposal at 1. Hash now 0x6225b6855a22bbf18ee4bac8266024fd809caabd5e12bc90e98a00cd5b2769d3, previously 0x2333e117b007e74d63f3520951d4aab01245ee30682dd772b6be866cb1de8b64.    
2024-02-08 14:49:06 ✨ Imported #1 (0x6225…69d3)    
2024-02-08 14:49:10 💤 Idle (0 peers), best: #1 (0x6225…69d3), finalized #0 (0x103c…e3ff), ⬇ 0 ⬆ 0    
2024-02-08 14:49:12 🙌 Starting consensus session on top of parent 0x6225b6855a22bbf18ee4bac8266024fd809caabd5e12bc90e98a00cd5b2769d3    
2024-02-08 14:49:12 🎁 Prepared block for proposing at 2 (0 ms) [hash: 0xdec0502e3242b7c0e58a532a1444cb26a8e69c6bae94daec7f189490cf224861; parent_hash: 0x6225…69d3; extrinsics (1): [0x02c9…abf0]    
2024-02-08 14:49:12 🔖 Pre-sealed block for proposal at 2. Hash now 0xd590e5c00ca6f2c2f2d063fbffc3da9001950b724f250860633f24bf8bfe0222, previously 0xdec0502e3242b7c0e58a532a1444cb26a8e69c6bae94daec7f189490cf224861.    
2024-02-08 14:49:12 ✨ Imported #2 (0xd590…0222)    
2024-02-08 14:49:15 💤 Idle (0 peers), best: #2 (0xd590…0222), finalized #0 (0x103c…e3ff), ⬇ 0 ⬆ 0    
2024-02-08 14:49:18 🙌 Starting consensus session on top of parent 0xd590e5c00ca6f2c2f2d063fbffc3da9001950b724f250860633f24bf8bfe0222    
2024-02-08 14:49:18 🎁 Prepared block for proposing at 3 (0 ms) [hash: 0x3023a39814111ef63f6c2091599deb583ee897da75a46186a742da313649931f; parent_hash: 0xd590…0222; extrinsics (1): [0x688f…c846]    
2024-02-08 14:49:18 🔖 Pre-sealed block for proposal at 3. Hash now 0x160c5980934a15526d7d0107c9f6955be0bfcb0fe34ea752ee4006a7b2a454e5, previously 0x3023a39814111ef63f6c2091599deb583ee897da75a46186a742da313649931f.    
2024-02-08 14:49:18 ✨ Imported #3 (0x160c…54e5)    
2024-02-08 14:49:20 💤 Idle (0 peers), best: #3 (0x160c…54e5), finalized #1 (0x6225…69d3), ⬇ 0 ⬆ 0    
2024-02-08 14:49:24 🙌 Starting consensus session on top of parent 0x160c5980934a15526d7d0107c9f6955be0bfcb0fe34ea752ee4006a7b2a454e5    
2024-02-08 14:49:24 🎁 Prepared block for proposing at 4 (1 ms) [hash: 0x32a16d3c2c433e0f49acaa6beea75471609667ef978a3cb209581c66a1023b3f; parent_hash: 0x160c…54e5; extrinsics (1): [0x3eca…200b]    
2024-02-08 14:49:24 🔖 Pre-sealed block for proposal at 4. Hash now 0x1fa56501a9c9a3404382936e0b2896a89966ad7cf69972dd89d61c21713f60f7, previously 0x32a16d3c2c433e0f49acaa6beea75471609667ef978a3cb209581c66a1023b3f.    
```

## 3. Install the front-end template

- We'll then setup the frontend for interacting with our local node.
- The front-end template uses ReactJS to render a web browser interface that enables you to interact with the Substrate-based blockchain node.
- The front-end template requires [Yarn](https://yarnpkg.com/) and [Node.js](https://nodejs.org/). 
- Cd into the `substrate-front-end-template` in the root repo

```sh
cd substrate-front-end-template

```

- install the dependencies:

```sh
yarn install
```

- Output should be as follows:

```sh
➤ YN0000: Done with warnings in 1s 14ms
```

## 4. Start the frontend template

- Start the front-end template by running the following command:

```sh
yarn start
```


## TODO!

- Finish madara docs
- Finish rust macros
- Build a substrate pallet








