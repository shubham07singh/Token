
# MyToken Solidity Contract

This repository contains a Solidity contract for MyToken, a custom token implementation on the Ethereum blockchain.

## Requirements

1. The contract has public variables that store the details of the token:
   - Token Name: META
   - Token Abbreviation: MTA
   - Total Supply: 0 (initially)

2. The contract includes a mapping of addresses to balances:
   ```
   mapping(address => uint) public balances;
   ```

3. The contract has a mint function that increases the total supply and the balance of the specified address:
   ```
   function mint(address _address, uint _value) public {
       // Increase the total supply
       totalSupply += _value;
       // Increase the balance of the specified address
       balances[_address] += _value;
   }
   ```

4. The contract includes a burn function that decreases the total supply and the balance of the specified address:
   ```
   function burn(address _address, uint _value) public {
       // Check if the balance of the specified address is greater than or equal to the burn amount
       if (balances[_address] >= _value) {
           // Decrease the total supply
           totalSupply -= _value;
           // Decrease the balance of the specified address
           balances[_address] -= _value;
       }
   }
   ```

## Usage

1. Clone the repository:

   ```
   git clone https://github.com/your-username/your-repository.git
   ```

2. Compile and deploy the contract to an Ethereum network of your choice.

3. Interact with the contract:
   - Use the `mint` function to create new tokens by specifying an address and the amount.
   - Use the `burn` function to destroy tokens by specifying an address and the amount.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

## Contact

For any questions or inquiries, please contact [kumarshubham2958@mail.com]

Feel free to customize the content according to your needs, such as adding more detailed information, including instructions on deploying the contract, or providing additional sections.
