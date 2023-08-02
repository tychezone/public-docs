---
description: How to add rich metadata to your ERC721 or ERC1155 NFTs
---

# Metadata Standards

Providing _asset metadata_ allows applications like Tyche to pull in rich data for digital assets and easily display them in-app. Digital assets on a given smart contract are typically represented solely by a unique identifier (e.g., the `token_id` in ERC721), so metadata allows these assets to have additional properties, such as a name, description, and image

```
//nft.sol
/**
 * @dev Returns an URI for a given token ID
 */
function tokenURI(uint256 _tokenId) public view returns (string) {
  return Strings.strConcat(
      baseTokenURI(),
      Strings.uint2str(_tokenId)
  );
}
```

The `tokenURI` function in your ERC721 or the `uri` function in your ERC1155 contract should return an HTTP or IPFS URL. When queried, this URL should in turn return a JSON blob of data with the metadata for your token. You can see an example of a simple Python server for serving metadata in the OpenSea creatures repo [here](https://github.com/ProjectOpenSea/opensea-creatures/tree/master/metadata-api).
