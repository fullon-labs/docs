# How to deploy an ERC-20 smart contract?

1. ## Open MetaMask and connect with FLON EVM network

2. ## Open Remix

Paste the following sample ERC-20 smart contract code in `Solidity` into [Remix](https://remix.ethereum.org/):

```solidity
pragma solidity ^0.8.0;


import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract MyToken is ERC20, Ownable {
    constructor() ERC20("MyToken","MT") Ownable(msg.sender) {
       _mint(msg.sender, 10000*10000*10000*10000*10000*10000);
    }

    function mint(address to, uint256 amount) public onlyOwner {
       _mint(to, amount);
    }
}

```

3. ## Config the compiler version to be `0.8.0` & `berlin`

Compile the code

4. ## Connect `MetaMask` to FullOn network to deploy the code via Remix