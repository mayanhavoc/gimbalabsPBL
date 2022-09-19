from Gimbalab's Summer 2022 PBL course

## Minting

### "Native" vs "Plutus" Scripts

**Native** scripts can be written by hand and used directly in Cardano transactions.
**Plutus** scripts are compiled from plutus code, and used in Cardano transactions.

**What is a native script?**
Native scripts are sets of rules for taking action on Cardano, for example, defining the signatures required to mint a token or wether a token can or cannot be minted.

**Native** scripts are of file type .script, i.e. my-first-policy.script
```
{
    "keyHash": "22117fbd0f86a213ae4f4d824cd0d38eea29e49764ae22f5f50ba3d3",
    "type": "sig"
}
```
Native script with rule "type" "sig" which means a signature is required by any tx using the script. The `keyHash` defines **which** signature is required. 

## Public Key Hash

### Generating a public key hash
`cardano-cli address key-hash --payment-verification-file payment.vkey

## Policies

### How to generate a minting policy Id
`cardano-cli transaction policyid --script-file my-first-policy.script`