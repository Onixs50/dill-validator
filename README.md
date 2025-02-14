# dill-validator
*first do the galex task*
*Reach Level 6 in the Discord*
*Join [Galxe](https://app.galxe.com/quest/Dill/GCVWntghfL) first and be active in Discord to get Andes role.*
![image](https://github.com/user-attachments/assets/ba253739-4992-455b-bb36-338de803e047)

```bash
sudo apt update && apt upgrade -y
sudo apt install curl make wget clang net-tools pkg-config libssl-dev build-essential jq lz4 gcc unzip snapd -y
```
```bash
curl -sO https://raw.githubusercontent.com/DillLabs/launch-dill-node/main/dill.sh  && chmod +x dill.sh && ./dill.sh
```
1. There are two options:
1. Launch a new dill node: Start a new Dill node. Choose this option if you want to create and run a new node from scratch.

2. Add a validator to existing node: Add a validator to an existing node. Choose this option if you want to add a new validator to an existing node.

![image](https://github.com/user-attachments/assets/e7b5044d-e3a9-495b-ba1e-457054741bc9)

2. Validator Keys are generated from a mnemonic:
1. From a new mnemonic: Choose this option if you want to generate a new mnemonic.

2. Use existing mnemonic: Choose this option if you want to use a mnemonic that you already have.

Option 1: The mnemonic will be automatically saved to /root/dill/validator_keys/.... Please back up the validator_keys folder to your local machine after you have successfully run the node.

Option 2: You will need to back up your existing mnemonic yourself.


![image](https://github.com/user-attachments/assets/7eeea2a8-fe02-46ce-b30a-28d59cc05030)


3. Please choose an option for deposit token amount [1, 3600, 2, 36000]:
Option 1: 3600 for light node Option 2: 36000 for full node

4. Please enter your withdrawal address:
You can use any wallet as long as you have the mnemonic for it. Suggestion: you can use a staking wallet.
Fill evm wallet & click enter.


![image](https://github.com/user-attachments/assets/542b3ee5-f42c-464d-b1c2-d9250ce28e8d)


5. Verify Node is Running
Run the following command to check if the node is up and running:

# Check health node
```bash
./health_check.sh -v
```
Get faucet by typing `$request your-evm-address` in [Andes](https://discord.gg/EQAZbsqg) channel.
# Delegate
*Go to /dill/validator_keys directory and transfer deposit_data-xxxx.json file to your local system and send them to your pc*
or 
```bash
cat ./validator_keys/deposit_data-xxxx.json
```
# Upload and Delegate
*Upload deposit_data-xxxx.json in https://staking.dill.xyz/*
*stake your token `3600 is min`*
*Open your deposit_data-xxxx.json file and Copy your Pubkey*

# Search it here: https://andes.dill.xyz/validators
# Check Validator
```bash
cd ~ && cd $HOME/dill
./health_check.sh -v
```
*Add new node into existing machine*
```bash
./2_add_validator.sh
```

