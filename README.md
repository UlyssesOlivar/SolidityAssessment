# Solidity
This assessment shows the basic minting and burning of an NFT token. The main goal of this program is to share knowledge on a new technology that is solidity that can be used by an individual for his daily life as a developer.
# Description
Solidity is a computer language used to build smart contracts for the Ethereum network. This application serves as an accessible introduction to Solidity programming and can be used as a launching pad for more challenging projects in the future.
# Getting Started
Remix is an online Solidity IDE that you may use to run this application. To get started, go to https://remix.ethereum.org/.
When you are on the Remix website, click the "+" icon in the left sidebar to start a new file. The file should be saved with a.sol extension (such as Solidity.sol). The code below should be copied and pasted into the file:

// SPDX-License-Identifier: MIT

pragma solidity 0.8.18;

contract MyToken {

    // public variables here
        string public name = "NOYPI";
        string public abbrv = "NYP";
        uint public supply = 0;

    // mapping variable here
        mapping(address => uint) public blnc;

    // mint function
        function mint(address add, uint val) public {
        supply += val;
        blnc[add] += val;
        }
        
    // burn function
        function burn(address add, uint val) public {
            if(blnc[add] >= val){
                supply -=val;
                blnc[add] -= val;
            }
        }
}


Click the "Solidity Compiler" tab in the left-hand sidebar to compile the code. Click the "Compile Solidity.sol" button after making sure the "Compiler" option is set to "0.8.18" (or another compatible version).

Go to "Deploy and run transactions" after the code has been compiled. You will then see the contract; simply choose "Solidity.sol" and press the deploy button.


Once the token has been deployed, click "Deploy Contracts" in the section at the bottom. You can see the "Account Address" copied in the example above, and you can see the "burn" and "mint" in the deploy contracts.

When entering, click the burn drop-down box, copy the Account Address, and then enter the value you want to use. Also, you can check if the minted token was successfully minted, just click the "blnc" button after that it will appear under the blnc button same in burn.

# Author
Ulysses O. Olivar

2.1 BSIT 


