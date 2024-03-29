---
description: Customizing the metadata for your smart contract
---

# Contract-level metadata

You can add a `contractURI` method to your ERC721 or ERC1155 contract that returns a URL for the storefront-level metadata for your contract.

```
//Solidity
contract MyCollectible is ERC721 {
    function contractURI() public view returns (string memory) {
        return "https://metadata-url.com/my-metadata";
    }
}
```

This URL should return data in the following format:

```
// JSON
{
  "name": "Tyche partner collection",
  "description": "imaginary creatures of Tyche partenr collection.",
  "image": "external-link-url/image.png",
  "external_link": "external-link-url"
}
```

You can also encode the data within the contract itself:

```
// Some code
contract MyCollectible is ERC721 {
    function contractURI() public pure returns (string memory) {
        string memory json = '{"name": "Tyche partner collection","description":"..."}';
        return string.concat("data:application/json;utf8,", json);
    }
}
```
