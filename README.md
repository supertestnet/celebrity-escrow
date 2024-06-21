# Celebrity escrow
Celebrity Escrow is a censorship resistant peer to peer escrow built with bitcoin and nostr. It allows two parties to create an escrow contract, with an impartial third party "celebrity" acting as the escrow.

## Inspiration

[Smart Contracts Unchained](https://zmnscpxj.github.io/bitcoin/unchained.html)

## How it works

*See the [spec](https://github.com/ArcadeLabsInc/celebrity-escrow/wiki/Spec) for more detail.*

1. The maker creates a new contract by entering their details, the taker's details, escrow's details, contract terms and stake amounts. They then publish this to the Nostr protocol.

2. The taker views the contract details and can choose to accept the contract. If they accept, they enter their nsec and sign the contract with their Bitcoin private key. They then publish this acceptance to Nostr, referencing the original contract event.

3. If there is a dispute, the escrow can view the contract details and decide on the outcome. They declare either the maker or taker as the winner by publishing to Nostr.

4. The contract funds are then released to the winner's Bitcoin address.

## Project stack

- Nostr for encrypted event publishing
- Noble Secp256k1 for encryption/decryption and signing
- Bech32 for npub/nsec encoding
- BitcoinJS/TaprootJS for Bitcoin script construction and signing
- TailwindCSS for styling

## Setup

1. Clone the repo

2. Open `index.html` in your browser to access the app

3. There is no step 3

## Demo pic

![pic](https://github.com/ArcadeLabsInc/celebrity-escrow/assets/14167547/595d78d9-6a3d-4b67-a63a-118e86d0076e)
