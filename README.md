## Connect your Metamask to Binance Smart Chain in one click

[Deployed on github-pages](https://alexey-zhdanov.github.io/metamask-to-bsc/)

## How it works

See [eip-3085](https://eips.ethereum.org/EIPS/eip-3085) and [metamask method](https://docs.metamask.io/guide/rpc-api.html#wallet-addethereumchain)

For security use [chains.json](https://chainid.network/chains.json) (https://chainid.network/)

```javascript
const chain = {
  chainId: "0x38",
  chainName: "Binance Smart Chain Mainnet",
  nativeCurrency: {
    name: "Binance Chain Native Token",
    symbol: "BNB",
    decimals: 18,
  },
  rpcUrls: [
    "https://bsc-dataseed1.binance.org",
    "https://bsc-dataseed2.binance.org",
    "https://bsc-dataseed3.binance.org",
    "https://bsc-dataseed4.binance.org",
    "https://bsc-dataseed1.defibit.io",
    "https://bsc-dataseed2.defibit.io",
    "https://bsc-dataseed3.defibit.io",
    "https://bsc-dataseed4.defibit.io",
    "https://bsc-dataseed1.ninicoin.io",
    "https://bsc-dataseed2.ninicoin.io",
    "https://bsc-dataseed3.ninicoin.io",
    "https://bsc-dataseed4.ninicoin.io",
    "wss://bsc-ws-node.nariox.org",
  ],
  blockExplorerUrls: ["https://www.bscscan.com/"],
  iconUrls: [
    "https://bin.bnbstatic.com/image/admin_mgs_image_upload/20201110/550eda20-1b9a-4bc7-9a65-e4a329e8bb57.png",
  ],
};

window.ethereum
  .request({
    method: "wallet_addEthereumChain",
    params: [chain],
  })
  .catch((error) => {
    console.log(error);
    alert(
      "An error has occurred. Please make sure the metamask is ready to go. See error in log"
    );
  });
```
