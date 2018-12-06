# sirius-web-wallet
A web wallet for SIRX

## Export address from desktop wallet

With the desktop wallet open navigate to Help-->Debug Window-->Terminal. If your wallet is locked you need to unlock it first.

```bash
walletpassphrase "your-wallet-address" 300
```

Then you can export your current wallet address.

```bash
dumpprivkey your-wallet-address(wif)
```

## Import address into the webwallet

First open the web wallet [here](). If you already have a SIRX wallet you can import the wallet in one of 4 ways:

-  From mnemonic phrase
-  From a WIF
-  From the mobile wallet
-  From a key file (export from another wallet)

Follow the instructions on the page for whichever method you choose.

If you don't have a SIRX wallet yet you can create a new address in one of two ways:

-  With a generated key file
-  With a generated mnemonic phrase

You will be prompted to enter a password when creating a new wallet and provided with the passphrase or key file depending on what method you chose. KEEP THIS INFORMATION SAFE! If you lose your password, key file, or passphrase you will LOSE YOUR ADDRESS and all the funds that is currently in it. Make sure you save this information in a safe place.

## General use of the web wallet functions

#### View Wallet Info

address
balance
unconfirmed balance
private key (hidden)

#### View Wallet Transactions (Txs)

recent 10 transactions

#### Send

address
amount
fee

#### Request Payment

address
amount
message
qr code

#### Dump As Key File

request for password, password is specific to the dump file. Password not on blockchain and has nothing to do with account, only to the specific key file
press the button
