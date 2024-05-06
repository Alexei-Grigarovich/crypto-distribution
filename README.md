# CRYDIS API - Crypto Distribution 

## Installation

### Clone the Repository Locally
```console
git clone https://github.com/Alexei-Grigarovich/crypto-distribution.git
```

### Install Dependencies
```console
yarn install
```

### Create .env file

```console
cp .env.example .env
```

### Add Environment Variables

Add your values to the .env file after the equals (=) sign.

> Private Keys are from an Ethereum based wallet. The private key added to the .env should have a сryptocurrency on the network specified in the .env under RPC_URL.

## Usage

### Get Request

```console
GET https://your_domain.com/claim/:address
```
your_domain.com replace with your endpoint. Address must also be valid. Example: https://myapi.onrender.com/claim/0x1234567890ABCDEF1234567890ABCDEF

### Cryptocurrency

The сryptocurrency of the blockchain(e.g., ETH) is used to pay for the transaction gas. This API distributes the currency to the right wallet. Use it before sending a transaction so that the user always has enough currency to pay for the gas.

> The PRIVATE_KEY passed in through the .env must have enough сryptocurrency to cover costs otherwise the application will fail.