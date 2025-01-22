## t3rn-airdrop-bot: 
(t3rn site facing issue's so our bot also getting some error)

-A bot designed to automate transactions and bridge assets on the t3rn network, making the process seamless and efficient.
Now supports both Base Sepolia, Optimism Sepolia and Arbitrum Sepolia testnets.

## Features :

- Automates asset bridging and swapping on the t3rn network.
- Supports multiple wallets through a .py file containing private keys.
- Robust error handling with retry mechanisms to ensure all transactions are completed.
- User-friendly and easy to set up.
- Supports bridging from Base Sepolia, Optimism Sepolia and Arbitrum Sepolia.


## Requirements

Before running the script, make sure you have installed and configured:

1. Python (Version 3.7 or later)
2. Python Dependencies :
      * web3
      * eth_account
3.Configuration File :
      * data_bridge.py: Contains data for each bridge.
      * keys_and_addresses.py: Contains the private key, address, and account label. 


## Installation

1. Clone this repository:     

          git clone https://github.com/adityapatil343/t3rn-auto-bridge
          cd t3rn-auto-bridge
2. Install python3: 

          sudo apt update && sudo apt install -y python3

3. Install dependencies:

        pip install web3 eth_account

4. File configuration:
     _Enter the private key and address into keys_and_addresses.py.

### for file edit use nano 
example:

     nano keys_and_addresses.py


### edit file Example format:

for 1 account:

     # keys_and_addresses.py
     # replace you key and address 
     private_keys = [
         'your_private_key_here'  # Example: '9da...365' 
     ]
     
     my_addresses = [
         'your_address_here'  # Example: '0x087....E85' 
     ]

     labels = [
         'wallet1' 
     ]
     
for multi accounts:

         private_keys = [
     '0xYourPrivateKey1',
     '0xYourPrivateKey2'
         ]

         my_addresses = [
     '0xYourAddress1',
     '0xYourAddress2'
         ]

         labels = [
     'Account 1',
     'Account 2'
         ]
### exit using command:  control + x and then enter


## Usage

## 1. Run the script with the command:

     python3 t3rn-bot.py

## 2. Select one of the options in the menu:
   1. OP -> BASE Sepolia
   2. BASE -> OP Sepolia
   3. BASE -> Arbitrum Sepolia
   4. Arbitrum -> BASE Sepolia
   5. Run all transactions repeatedly.

## 3. The script will process the transaction and display the results in the terminal, including:

   * Return address
   * Gases used
   * Block number
   * ETH and BRN balance
   * Link to blockchain explorer

## Security Notes
  * Make sure the configuration file is only accessed by you.


## License
### This project is licensed under the MIT license. You are free to use, modify, and distribute it.
