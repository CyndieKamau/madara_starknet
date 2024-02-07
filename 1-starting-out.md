
# RUNNING A SUBSTRATE NODE LOCALLY

## 1. Clone the Node template repository

```bash
git clone https://github.com/substrate-developer-hub/substrate-node-template
```

## 2. Change to the root directory of the cloned repo

```bash
cd substrate-node-template
```

## 3. Create a new branch to do your work in

❇️  N.B. Substrate generally recommend this format while creating your branch;

```bash
git switch -c my-learning-branch-2023-10-06
```

## 4. Compile the node template 

```bash
cargo build --release
```

❇️  `--release` flag is generally for building optimized artifacts

❇️   The first compile will take some time!!

A FEW MOMENTS LATER....

```bash
 Finished release [optimized] target(s) in 24m 33s
```
The node has successfully compiled!!


# TODO:

Summary of Madara as a sequencer
- Madara's Architecture
- Running a node using the starter app template
- Pallet and runtime configuration
- Creating a sample app chain using the pallet_starknet
- Creating a new pallet for your appchain
