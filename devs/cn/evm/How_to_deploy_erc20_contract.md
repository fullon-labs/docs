# 如何部署ERC20合约

1. ## 打开MetaMask, 并连接FLON EVM网络

2. ## 打开合约编译器remix

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

3. ## 将编译器版本配成0.8.0和berlin，并编译

4. ## 连上MetaMask对应有FLON的账户地址，部署就可以了