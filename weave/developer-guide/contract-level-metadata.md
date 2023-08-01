---
description: Customizing the metadata for your smart contract
---

# Contract-level metadata

You can add a `contractURI` method to your ERC721 or ERC1155 contract that returns a URL for the storefront-level metadata for your contract.

```
contract MyCollectible is ERC721 {
    function contractURI() public view returns (string memory) {
        return "https://metadata-url.com/my-metadata";
    }
}
```
