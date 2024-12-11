---
### **Step-by-Step Guide to Deploying with Foundry on Lisk Sepolia**

#### **1. Install Foundry**
1. Open your terminal and install Foundry:
   ```bash
   curl -L https://foundry.paradigm.xyz | bash
   ```
2. Install the latest (nightly) build of Foundry:
   ```bash
   foundryup
   ```

---

#### **2. Set Up the Project**
1. Create a directory for your project and navigate to it:
   ```bash
   mkdir LiskFoundry
   cd LiskFoundry
   ```
2. Initialize the Foundry project:
   ```bash
   forge init
   ```

---

#### **3. Update the Script File**
1. Open the `script/Counter.s.sol` file or create a new one.
2. Update the script with the following content:

   ```solidity
   // SPDX-License-Identifier: UNLICENSED
   pragma solidity ^0.8.13;

   import {Script, console} from "forge-std/Script.sol";
   import {LearningHub} from "../src/LearningHub.sol"; 

   contract LearningHubScript is Script {
       function setUp() public {}

       function run() public {
           vm.startBroadcast();
           
           LearningHub learningHub = new LearningHub();

           console.log("LearningHub deployed at:", address(learningHub));

           vm.stopBroadcast();
       }
   }
   ```

3. Rename the script file to match the main contract's name for consistency. For example:
   ```bash
   mv script/Counter.s.sol script/LearningHub.s.sol
   ```

---

#### **4. Compile the Smart Contract**
1. Run the following command to compile your contract:
   ```bash
   forge build
   ```
2. **Expected Output:**
   If the contract compiles successfully, you’ll see:
   ```
   [⠢] Compiling...
   [⠰] Compiling 1 files with 0.8.24
   [⠔] Solc 0.8.24 finished in 40.36ms
   Compiler run successful!
   ```

---

#### **5. Set Up Environment Variables**
1. Create a `.env` file in the root of your project:
   ```bash
   touch .env
   ```
2. Add your wallet's private key to the `.env` file:
   ```env
   PRIVATE_KEY=your_private_key_here
   ```
   Replace `your_private_key_here` with your actual private key.

3. Source the environment variables:
   ```bash
   source .env
   ```

---

#### **6. Deploy the Smart Contract**
1. Use the following command to deploy the contract to the Lisk Sepolia network:
   ```bash
   forge create --rpc-url https://rpc.sepolia-api.lisk.com \
   --etherscan-api-key 123 \
   --verify \
   --verifier blockscout \
   --verifier-url https://sepolia-blockscout.lisk.com/api \
   --private-key $PRIVATE_KEY \
   src/LearningHub.sol:LearningHub --legacy
   ```
   **Explanation of Flags:**
   - `--rpc-url`: The RPC URL for the Lisk Sepolia network.
   - `--etherscan-api-key`: A placeholder API key (`123`) for verification, as Blockscout doesn't require a real key.
   - `--verifier blockscout`: Specifies Blockscout as the verification service.
   - `--verifier-url`: URL of the Blockscout API for the Lisk Sepolia network.
   - `--private-key`: Uses the private key stored in the `.env` file.
   - `--legacy`: Indicates compatibility with older Ethereum-style transactions.

2. **Expected Output:**
   After running the command, Foundry will deploy the contract and log the contract's address.

---

### **Key Points**
1. **Environment Management:** Use `.env` to securely store sensitive information like your private key.
2. **Verification Support:** Foundry integrates with Blockscout for contract verification on Lisk Sepolia.
3. **Ease of Debugging:** Use `console.log` in scripts for debugging and logging deployment details.

