A web wallet for Sirius.

# Running the web wallet for development/production

Clone this repo

```bash
https://github.com/siriuscore/sirius-web-wallet
```

Cd into the folder and install dependencies

```bash
npm install
```

Build the wallet for production

```bash
npm run build
```

Run the wallet

```bash
npm run start
```

# Using the Web Wallet

## Export address from desktop wallet

With the desktop wallet open navigate to Help-->Debug Window and then select the Console tab. If your wallet is locked you need to unlock it first.

```bash
walletpassphrase "your-wallet-address" 300
```

Then you can export your current wallet address.

```bash
dumpprivkey your-private-wallet-address
```

## Import address into the web wallet

First open the web wallet. If you already have a Sirius wallet you can import the wallet in one of 3 ways:

-  From mnemonic phrase: 12 work phrase
-  From a WIF: private address
-  From a key file (exported from another wallet)

You will be prompted to enter the relevant information based on the method you choose.

If you don't have a SIRX wallet yet you can create a new address in one of two ways:

-  With a generated key file: creates address and downloads key file
-  With a generated mnemonic phrase: generate 12 word phrase and creates address

You will be prompted to enter a password when creating a new wallet with the passphrase or key file depending on which method you chose. KEEP THIS INFORMATION SAFE! If you lose your password, key file, or passphrase you will LOSE YOUR ADDRESS and all the funds that is currently in it. Make sure you save this information in a safe place. The password is specific to the key file or passphrase. This password is not stored on the blockchain.

## General use of the web wallet functions

Before you send any coins to the wallet make sure you can close and reopen the wallet with the same receive address. Using the menu option Dump as Key File and Restore from Key File is a safe way to do this. Using the menu option to restore from seed words to reopen the wallet is riskier because entering a typo for the seed words or password will create an unexpected random address. In order to receive funds you need to supply your public address (first line in wallet info) to the sender. Wait a few minutes for the next block to be published and reload the web wallet to see the new balance. You can also click on the menu option View Wallet Txs to see the receiving transaction. Always double check that you are using the correct address when sending or receiving funds as sending funds to the wrong account cannot be retrieved once processed.

#### View Wallet Info

Contains the balance and address information for your wallet.

Fields:

-  Address: Your public address
-  Balance: Your current balance
-  Unconfirmed balance: Pending balance not yet confirmed on the blockchain
-  Private key: Your private key, hidden as standard

#### View Wallet Transactions (Txs)

Displays the last 10 transactions for the loaded SIRX address.

#### Send

Used to send funds to another account.

Fields:

-  Address: The receiving address for the transfer
-  Amount: The amount to be transferred
-  Fee: The fee charged to complete the transaction (default can be left at 0.01)

#### Request Payment

Used to send a payment request to another account.

Fields:

-  Address: The address that will send you the funds
-  Amount: The amount to be received
-  Message: A message to the sender for the transaction
-  QR code: An easy to scan QR code for the receiving transaction

#### Dump As Key File

When creating a key file to export your wallet you will be prompted to enter a password. This password is specific to the file being created. The password is not stored on blockchain and is specific to the key file being generated and not your address. Once a password has been entered you can select the green download button to create and download the file to your local drive.

#### Settings

Settings allows you to change the language of the wallet and also run the wallet in offline mode.