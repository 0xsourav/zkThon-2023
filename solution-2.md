txn link - https://testnet-zkevm.polygonscan.com/tx/0x344da25299017ee38a337f9f57096d8e40d4d71db080cd271ba3f118e35500c6

contract address - 0xF171610a828926521024c6D18d5Bd320c67C3C6E

txn hash - 0x344da25299017ee38a337f9f57096d8e40d4d71db080cd271ba3f118e35500c6

,,,sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

import "@openzeppelin/contracts@4.8.2/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts@4.8.2/token/ERC20/extensions/ERC20Burnable.sol";
import "@openzeppelin/contracts@4.8.2/access/Ownable.sol";

contract MyZK is ERC20, ERC20Burnable, Ownable {
    constructor() ERC20("MyZK", "ZKT") {
        _mint(msg.sender, 1000000 * 10 ** decimals());
    }

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }
}
'''
