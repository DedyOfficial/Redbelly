# RedBelly </br>

## **Token Contract Documentation** </br>

**Contract Address:** `0xab12e02e33ef9288c561b6c793a892fff404c54f` </br>

**Token Name :** `Redbelly Devnet`  </br>

**Token Symbol :**  `RED` </br>

[Open Remix](https://remix.ethereum.org/) and click on the `New File`

Name your file, in our case we've named it `Redbelly.sol` - yes, that [famous token standard]


Now add code. 

pragma solidity 0.8.17;

 // SPDX-License-Identifier: MIT

 contract Bustaaal { string public name = "Redbelly Devnet"; string public symbol = "RED"; uint8 public decimals = 18; uint256 public totalSupply = 100000000;

 mapping (address => uint256) public balances; address public owner;

 constructor() { owner = msg.sender; balances[owner] = totalSupply; }

 function transfer(address recipient, uint256 amount) public { require(balances[msg.sender] >= amount, "Insufficient balance."); balances[msg.sender] -= amount; balances[recipient] += amount; } }


On the left sidebar, you will click on Solidity compiler and Compile Redbelly.sol

```text
Solidity Compiler >>> Compile Contract
```

Now click to the `Deploy & Run Transactions` on the left in the sidebar and open Metamask to check if is our account connected. If it's connected you can skip to next steps


You will see your contract has been successfully deployed.
