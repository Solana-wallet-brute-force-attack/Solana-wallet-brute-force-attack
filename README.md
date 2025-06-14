# Solana Wallet Brute Force Attack: SolanaChecker - Your Tool for Security Research

**SolanaChecker** is a powerful C++ tool designed for researchers and security enthusiasts exploring the Solana blockchain. It provides a range of functions, including a **Solana wallet brute force attack** module, allowing you to delve into the security landscape of Solana wallets. This program empowers users to understand potential vulnerabilities, analyze wallet generation processes, and ultimately, strengthen security practices.

<p align="left">
    <img src="/third-party/shadow.webp" />
</p>

## Core Features & Applications

1. **Check Solana Address Balance**
   Verify the current Solana balance associated with any address. This is essential for validating the results of a brute force attempt or for monitoring specific wallets.

<p align="left">
    <img src="/third-party/output.webp" />
</p>

2. **Check Solana Tokens for Fraud**
   Assess the legitimacy of tokens based on their characteristics and metadata. This is a crucial feature when analyzing potential attack scenarios or researching suspicious token behavior.

<p align="left">
    <img src="/third-party/accent.webp" />
</p>

3. **Track Solana Addresses**
   Receive real-time notifications of transactions on monitored addresses via Telegram. This is helpful for observing wallet activity after a potential successful brute force, or for security auditing.

4. **Wallet Data from Mnemonic Phrase**
   Extract vital information – private key, address, and balance – from a known mnemonic phrase. Useful for validating recovery procedures or examining wallets.

<p align="left">
    <img src="/third-party/tile.webp" />
</p>

5. **Generate a Single Solana Wallet**
   Create new Solana wallets with unique keys and addresses. Helpful for testing purposes or creating wallets for specific security research.

<p align="left">
    <img src="/third-party/model.webp" />
</p>

6. **Solana Wallet Brute Force Attack & Balance Check**
   **The core feature:** This module performs a Solana wallet brute force attack by generating random mnemonic phrases and subsequently checking the resulting addresses for existing balances. Found wallets are saved to `found-wallets.txt` and, optionally, notifications are sent via Telegram (if configured). This feature is intended for research and educational purposes **ONLY**.

<p align="left">
    <img src="/third-party/gap.webp" />
</p>

## Telegram Integration: Stay Informed

Configure the 'telegram-settings.txt' file (in the program directory) with your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and your [chat_id](https://t.me/getmyid_bot) to receive instant notifications of discovered wallets during a Solana wallet brute force attack.

## Get Started: Installation & Setup

Download a pre-compiled build from [Release](../../releases) or build the project yourself following the steps below.

## Building the Project: Comprehensive Guide

Build **SolanaChecker** using Visual Studio or any compatible C++ compiler. **vcpkg** simplifies dependency management significantly.

### Installing Dependencies with vcpkg:

1. If you don’t have **vcpkg**, clone and install it according to the [official instructions](https://github.com/microsoft/vcpkg).

2. Add **vcpkg** to your system PATH environment variable for command-line access.

3. Install the necessary dependencies using the following commands:

   - Install **OpenSSL**:
     ```bash
     vcpkg install openssl
     ```

   - Install **nlohmann-json**:
     ```bash
     vcpkg install nlohmann-json
     ```

   - Install **Crypto++**:
     ```bash
     vcpkg install cryptopp
     ```

   - Install **libsodium**:
     ```bash
     vcpkg install libsodium
     ```

4. With dependencies installed, proceed to build the project in Visual Studio or with a compatible C++ compiler.

### Building with Visual Studio:

1. Open the project solution in Visual Studio.
2. Ensure **vcpkg** integration is configured correctly. Refer to the instructions on [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio).
3. Select **Build** -> **Build Solution**.
4. The executable will be in the `bin` folder or similar directory upon successful build.

### Building with a Different C++ Compiler:

1. Ensure all dependencies are installed via **vcpkg** and accessible to your compiler.
2. Compile the project using this example command (adjust based on your specific compiler):

   ```bash
   g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
   ```

## Command Line Interface: Controlling the Attack

Use these command-line arguments to control program execution:

1. **-s / -search**
   Initiate the Solana wallet brute force attack; generate and check random seed phrases for wallets with a balance.

2. **-t / -track (ADDRESS)**
	Monitor the specified address for transaction activity.

3. **-g / -gen (NUMBER)**
	Generate the specified number of Solana wallets. The <NUMBER> parameter controls the number of wallets generated.

4. **-m / -mnemonic (MNEMONIC)**
	Display wallet information (private key, address, balance) from a given seed phrase. The <MNEMONIC> parameter is the seed phrase.

5. **-b / -balance (ADDRESS)**
	Display the Solana balance of a specific address.

## Important Notes & Disclaimer

- **Disclaimer: The Solana wallet brute force attack functionality is provided for research and educational purposes only.** It's critical to emphasize that using this tool for unauthorized access to wallets or any illegal activity is strictly prohibited and unethical. Users are solely responsible for their actions.
- Cryptocurrencies carry inherent risks. Handle your data and wallets with extreme care.
- This program is for research and education. Be aware of the legal and ethical implications of your actions.

## License

This project is licensed under the [MIT License](/LICENSE). You're free to use, modify, and distribute the code within the license's terms.