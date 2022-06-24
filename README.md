# pwned-hdwalletprovider
This hd wallet provider was specifically developed for OpenSea SDK developers to use programmatic order submission.

# Why was this created

This repository was created to solve a famous issue with truffles hdwallet-provider when submitting programmatic orders through the new OpenSea v4 SDK.

**TypeError: Cannot read properties of undefined (reading 'EIP712Domain')**

This issue has been fixed by parsing JSON data before sanitizing inputs within the eth-sig-util package.

# Installation

Replace **@truffle** and **@metamask** with **@metamask** folder and **@pwned** folder from this repo in your **node-modules** folder.

Within your node-js script initate HDWalletProvider like this:

`const HDWalletProvider = require("@pwned/hdwallet-provider");`

All previous usage can be found within `@truffle/hdwallet-provider`

# Example usage

```
const HDWalletProvider = require("@truffle/hdwallet-provider");
const mainnetRPC="https://speedy-nodes-nyc.moralis.io/**YOUR-API-KEY**/eth/mainnet"

const decryptedUser=new HDWalletProvider({
        privateKeys: [""],
        providerOrUrl: mainnetRPC
});
```

# Important

Make sure you have the latest version of opensea-js library before using



