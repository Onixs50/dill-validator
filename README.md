# dill-validator
*You must be choosen as Andes role in the discord to be able to join this*

*Join [Galxe](https://app.galxe.com/quest/Dill/GCVWntghfL) first and be active in Discord to get Andes role.*

```bash
sudo apt update && apt upgrade -y
sudo apt install curl make wget clang net-tools pkg-config libssl-dev build-essential jq lz4 gcc unzip snapd -y
```
```bash
cd $HOME && curl -O https://dill-release.s3.ap-southeast-1.amazonaws.com/linux/dill.tar.gz && \
tar -xzvf dill.tar.gz && cd dill
```
```bash
./dill_validators_gen new-mnemonic --num_validators=1 --chain=andes --folder=./
```
```bash
ls -ltr ./validator_keys
```
```bash
./dill-node accounts import --andes --wallet-dir ./keystore --keys-dir validator_keys/ --accept-terms-of-use
```
# Write the password
```bash
echo 123@dill > walletPw.txt
```
*replace `123@dill` as a password*
# Start light validator
```bash
./start_light.sh -p walletPw.txt
```
# Check health node
```bash
./health_check.sh -v
```
Get faucet by typing `$request your-evm-address` in [Andes](https://discord.gg/Nkzwk3g3) channel.
# Delegate
*Go to /dill/validator_keys directory and transfer deposit_data-xxxx.json file to your local system and send them to your pc*
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
