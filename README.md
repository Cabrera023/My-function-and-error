# My-function-and-error

# Discription
A simple smart contract that uses the following functions: require(), assert(), and revert().

# Getting Launched
Installing Remix Online IDE
* Make sure to finish all necessary installations in advance.
* Extract "ErrorHandling.sol" from the source file, then move it.
* Go to  https://remix.ethereum.org and let`s start

# Using Remix to Run a Program
Make a folder within Remix
* Make a copy of ErrorHandling.sols unedited content, then add it to the new file
* To build the contract click the solidity compiler button
* Upon selected the deploy and run traction option the smart contract can be configured
* Examine the user interface for contract interaction following a successful launch

#  Quartet of Functions 

function requireValue(uint256 _newValue) external {

        require(_newValue >= 1 && _newValue <= 2000, "There is a value range of 1 to 2000 that you cannot exceed.");
        value = _newValue;
    }

 function assertValue(uint256 _num) external pure returns (uint256) {
 
        assert(_num >= 1 && _num <= 2000);
        return _num;
    }

   function revertValue(uint256 _num) external pure returns (uint256) {
   
        if (!(_num >= 1 && _num <= 2000)) {
            revert("The value must be between 1 and 2000.");
        }
        return _num;
    }

   // Function where sets a given value if each of the checks match.
   
    function setValue(uint256 _value) external {
        require(_value >= 1 && _value <= 2000, "Value must be between 1 and 2000.");
        assert(_value >= 1 && _value <= 2000); 

        value = _value;
    }
}   

# Author
Michaela Ariane Cabrera 
8214136@gmail.com
