
---

### **Step-by-Step Guide to Deploy with Hardhat on Lisk (Sepolia)**

#### 1. **Initialize the Project**
1. **Create a new directory for your project:**
   ```bash
   mkdir LiskHardhat
   cd LiskHardhat
   ```
2. **Initialize the project with `npm`:**
   ```bash
   npm init --y
   ```
   This generates a `package.json` file with default configurations.

3. **Install Hardhat as a development dependency:**
   ```bash
   npm install --save-dev hardhat
   ```

4. **Initialize Hardhat in your project:**
   ```bash
   npx hardhat init
   ```
   - Follow the prompts to set up your Hardhat project. It creates a basic directory structure.

5. **Install dotenv to manage sensitive information:**
   ```bash
   npm install --save-dev dotenv
   ```

---

#### 2. **Update Hardhat Configuration**
- Edit the `hardhat.config.js` file to include the following setup:
  ```javascript
  require("@nomicfoundation/hardhat-toolbox");
  require('dotenv').config();

  module.exports = {
    solidity: {
      version: "0.8.28",
      settings: {
        optimizer: {
          enabled: true,
          runs: 200,
        },
        viaIR: true,
      },
    },
    networks: {
      // Lisk Testnet (Sepolia)
      'lisk-sepolia': {
        url: 'https://rpc.sepolia-api.lisk.com',
        accounts: [process.env.WALLET_KEY], // Your private key stored in .env
        gasPrice: 1000000000, // 1 Gwei gas price
      },
    },
    etherscan: {
      // Use a placeholder for Blockscout, as no real API key is needed
      apiKey: {
        "lisk-sepolia": "123"
      },
      customChains: [
        {
          network: "lisk-sepolia",
          chainId: 4202,
          urls: {
            apiURL: "https://sepolia-blockscout.lisk.com/api",
            browserURL: "https://sepolia-blockscout.lisk.com"
          }
        }
      ]
    },
    sourcify: {
      enabled: false
    },
  };
  ```

---

#### 3. **Prepare the Deployment Script**
- Create a deployment module in the `ignition/modules` directory (e.g., `Lock.js`) to define the logic for deploying your contracts.

---

#### 4. **Set Up Environment Variables**
- Create a `.env` file in the root of your project with your wallet private key:
  ```env
  WALLET_KEY=your_private_key_here
  ```
  Replace `your_private_key_here` with your actual private key. Keep this file secure and never share it publicly.

---

#### 5. **Deploy Your Contracts**
- Use the following command to deploy your contracts:
  ```bash
  npx hardhat ignition deploy ignition/modules/Lock.js --network lisk-sepolia --verify
  ```
  - `ignition/modules/Lock.js`: The path to your deployment script.
  - `--network lisk-sepolia`: Specifies the Lisk Sepolia network.
  - `--verify`: Ensures the contract gets verified on Blockscout.

---

### **Key Points**
1. **Optimizer Configuration**: Enables optimized contract bytecode for deployment efficiency.
2. **Network Configuration**: Uses Lisk Sepolia RPC and includes your private key for signing transactions.
3. **Verification**: Custom chains (Lisk Sepolia) integrate with Blockscout for contract verification.
4. **Sensitive Information**: Store private keys in `.env` to maintain security.

This guideline ensures a streamlined setup and deployment process for Hardhat on the Lisk blockchain.
