# Metadata structure

OpenSea supports metadata that is structured according to [the official ERC721 metadata standard](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-721.md) or the [Enjin Metadata suggestions](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1155.md#erc-1155-metadata-uri-json-schema).

Additionally, we support several other properties that allow for multimedia attachments&#x20;

Here's an example of metadata:\




```
// Some code
{
  "description": "imaginary creatures of Tyche partenr collection.", 
  "external_url": "https://imaginarycreatures.io/390", 
  "image": "https://storage.pinnata/puffs/390.png", 
  "name": "example",
  "attributes": [ ... ]
}
```
