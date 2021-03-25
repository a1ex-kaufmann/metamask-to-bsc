## Connect your Metamask to Binance Smart Chain in one click

[Deployed on github-pages](https://alexey-zhdanov.github.io/metamask-to-bsc/)

## How it works

See [eip-3085](https://eips.ethereum.org/EIPS/eip-3085) and [metamask method](https://docs.metamask.io/guide/rpc-api.html#wallet-addethereumchain)

```
const chain = {
    chainId: "0x38",
    chainName: "Binance Smart Chain",
    rpcUrls: ["https://bsc-dataseed.binance.org/"],
    iconUrls: ["https://bin.bnbstatic.com/image/admin_mgs_image_upload/20201110/550eda20-1b9a-4bc7-9a65-e4a329e8bb57.png"],
    nativeCurrency: {
        name: "BNB",
        symbol: "BNB",
        decimals: 18,
    },
    blockExplorerUrls: ["https://www.bscscan.com/"]
};

window.ethereum.request({
    method: "wallet_addEthereumChain",
    params: [chain],
});
```
