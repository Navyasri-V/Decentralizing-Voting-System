# Decentralised Voting (dVoting)

A decentralised voting system based on [Ethereum blockchain](https://ethereum.org/dapps/) technology.

> This is my final year project for the CSE(AI&ML) BTECH  that I am pursuing, now eager to explore BLOCKCHAIN Technology through projects.

## Application Workflow 

Here’s a step-by-step overview of how the system operates:

# Election Setup:
 The admin starts by deploying the system on a blockchain network (EVM), setting up the election parameters, and defining the candidates.

# Voter Registration: 
Voters connect to the blockchain network and register. Their registration details are then forwarded to the admin's control panel.

# Verification:
 The admin reviews the submitted registration details (including blockchain account address, name, and phone number) to ensure they are accurate. Approved registrants are authorized to vote.
# Voting: 
Approved voters cast their votes for their preferred candidates through the voting interface.

# Election Closure:
After the election period ends, as determined by the election’s scope, the admin closes the voting. The final results are then compiled and displayed, highlighting the winning candidate at the top of the results page.

## Setting up the development environment

### Requirements

- [Node.js](https://nodejs.org)
   > Download and install **NodeJS**

   > Download and install NodeJS from [here](https://nodejs.org/en/download/ "Go to official NodeJS download page.").

- [Truffle](https://www.trufflesuite.com/truffle); [Ganache](https://github.com/trufflesuite/ganache-cli) (Cli)
   > Install **truffle** and **ganache-cli** using node packager manager (npm)

      ```shell
        npm install -g truffle
        npm install -g ganache-cli
      ```
- [Metamask](https://metamask.io/) (Browser Extension)
   >  Install **metamask** browser extension
      Download and install metamask from [here](https://metamask.io/download "Go to official metamask download page.").

### Project Development Setup

1. Clone this repository/zip and download

   clone: ```shell
             git clone https://github.com/navyasweet/Decentralizing Voting System.git
            cd dVoting
          ```
   zip:```cmd
           cd "file path"
      ```

2. Run local Ethereum blockchain(In Terminal)

   ```shell
   ganache-cli
   ```

   > Note:  `ganache-cli` the blockchain network needs to be running all the time & while existing close it using ctrl+c`

3. Create account by Import account(s) using private keys from ganache-cli thats running from step 2 to the metamask extension on the browser
  

4. Configure metamask on the browser with the following details
   create a network manually /by network name
   network name:localhost:8545 ,New RPC URL: `http://127.0.0.1:8545` ,Chain ID: `1337`,Currency symbol:ETH


5. Deploy smart contract to the (local) blockchain network (i.e ganache-cli)

   ```shell
   # on the dVoting directory
   truffle migrate
   ```
   > Note:  `truffle migrate --reset` for re-deployments

6. Activate the Frontend Development Environment

   ```shell
   cd client
   npm install
   npm start
   ```

