
# Error Handling Smart Contract

This project contains a Solidity smart contract that demonstrates the usage of the require(), assert(), and revert() statements for error handling in Ethereum smart contracts.


## Contract details
The contract implements the following functions:

1 .testrequire(uint256 _input)
This function uses the require() statement to validate a condition. It takes an unsigned integer _input as a parameter and sets the contract's public variable value to the input value if _input is greater than zero. If the condition is not met, the function will revert with an error message.

2. testassert()
The testassert() function showcases the assert() statement. It compares two unsigned integers a and b (initialized with values 40 and 20, respectively). The assert() statement checks if a is less than b, and if the condition is false, it will trigger an unrecoverable error (i.e., the contract will be permanently halted).

3 . testrevert(uint256 _input)
The testrevert() function uses the revert() statement with a conditional check. If the input _input is equal to zero, the function will revert with an error message stating that the input cannot be zero. Otherwise, it will set the contract's public variable value to the input value.
## Executing Program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:
You can then call the functions testrequire(), testassert(), and testrevert() with appropriate parameters to observe the error handling behavior.
## code

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract ErrorHandlingContract {
    uint256 public value;

    function testrequire(uint256 _input) public {
        
        require(_input > 0, "Input must be greater than zero");
        value = _input;
    }

    function testassert() public {
        uint256 a = 40;
        uint256 b = 20;

        
        assert(a < b);
        
        
        value = 42;
    }

    function testrevert(uint256 _input) public {
        if (_input == 0) {
           
            revert("Input cannot be zero");
        }
        value = _input;
    }
}
## Disclaimer
This code is provided as-is with no warranties or guarantees. The authors are not responsible for any potential issues or losses that may arise from the use of this code. Use it at your own risk.
## Author
Kuldeep Yadav