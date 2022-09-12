# Module-21-Challenge

For this project, I am utilizing Solidity and Remix IDE to create a Solidity smart contract that develops a monetary system based on blockchain technologies and launches a crowdsale. The smart contract allows people to convert ether to the new KaseiCoin.

---

## Technologies

This project uses Solidity, Remix IDE, Git Bash, Visual Studio, Github, Ganache, MetaMask and contracts from the OpenZeppelin library.

---

## Installation Guide

The web version of Remix IDE was used and this is the Solidity version that was used:

    pragma solidity ^0.5.0


Required Imports:

    import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/release-v2.5.0/contracts/token/ERC20/ERC20.sol";

    import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/release-v2.5.0/contracts/token/ERC20/ERC20Detailed.sol";

    import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/release-v2.5.0/contracts/token/ERC20/ERC20Mintable.sol";

    import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/release-v2.5.0/contracts/crowdsale/Crowdsale.sol";

    import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/release-v2.5.0/contracts/crowdsale/emission/MintedCrowdsale.sol";

---

## Usage

* Step 1: Create the KaseiCoin Token Contract:

I defined a new contract named KaseiCoin with the following variables:

    contract KaseiCoin is ERC20, ERC20Detailed, ERC20Mintable {
    constructor(
        string memory name,
        string memory symbol,
        uint initial_supply
    )
        ERC20Detailed(name, symbol, 18)
        public {
            
        }
}


* Step 2: Create the KaseiCoin Crowdsale Contract:

    contract KaseiCoinCrowdsale is Crowdsale, MintedCrowdsale { 
        constructor(
            uint rate,
            address payable wallet,
            KaseiCoin token
    )   public Crowdsale(rate, wallet, token) {
    }
}


* Step 3: Create the KaseiCoin Deployer Contract:

    contract KaseiCoinCrowdsaleDeployer {
        address public kasei_token_address;
        address public kasei_crowdsale_address;

    constructor(
        string memory name,
        string memory symbol,
        address payable wallet
    ) public
}

---

## Evaluation Evidence

I successfully compiled the KaseiCoin contract:

![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot3.png)


I successfully compiled the KaseiCoinCrowdsale contract:

![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot4.png)


I successfully compiled the KaseiCoinCrowdsaleDeployer contract:

![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot5.png)


I deployed the KaseiCoinCrowdsaleDeployer contract:

![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot6.png)


I deployed the KaseiCoinCrowdsale contract:

![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot7.png)


![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot8.png)


Addresses were assigned for the token:

![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot9.png)


I deployed the KaseiCoin contract:

![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot10.png)


![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot11.png)


I funded with 7 wei:

![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot13.png)


![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot14.png)


![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot15.png)


I funded with 20 wei:

![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot16.png)


![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot17.png)


The full funded amount so far:

![Screenshot](https://github.com/abcarmin/Module-21-Challenge/blob/main/Evaluation%20Evidence/Screenshot18.png)


---

## Contributors

Allyssa Carmin

---

## License

SMU Fintech Course