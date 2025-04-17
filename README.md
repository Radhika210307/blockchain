# blockchain
Blockchain is a decentralized, distributed ledger technology that securely records transactions across many computers so that the data cannot be altered retroactively without changing all subsequent blocks and gaining consensus from the network. It’s the foundational technology behind cryptocurrencies like Bitcoin and Ethereum but has applications beyond just digital currencies.

**key concepts:**

**1. Blocks:**
Each "block" contains a list of transactions. When a block is completed, it's linked to the previous one, forming a chain, which is why it’s called a "blockchain."

**2. Decentralization:**
Unlike traditional databases controlled by a central authority (like a bank or government), blockchain is decentralized. This means that no single entity controls the data, and multiple participants (nodes) validate and maintain the network.

**3. Immutability:**
Once a block is added to the blockchain, it’s nearly impossible to change. This ensures the integrity of the data, making it tamper-resistant.

**4. Cryptography:**
Blockchain uses cryptographic techniques to secure transactions. Every transaction is encrypted, and participants use private and public keys to verify transactions.

**5. Consensus Mechanisms:**
These are protocols that allow all participants in the network to agree on the validity of transactions. Two common mechanisms are:

Proof of Work (PoW): Miners solve complex mathematical puzzles to validate transactions (used by Bitcoin).

Proof of Stake (PoS): Participants validate transactions based on the number of coins they hold and are willing to "stake" as collateral.

**6. Smart Contracts:**
On platforms like Ethereum, blockchain supports "smart contracts," which are self-executing contracts with the terms of the agreement written directly into the code. These contracts automatically execute when certain conditions are met, removing the need for intermediaries.

**7. Applications Beyond Cryptocurrencies:**
Blockchain has many uses beyond digital currencies. For example:

Supply Chain Management: Blockchain can track the provenance of goods, ensuring transparency and authenticity.

Voting Systems: It could be used for secure, transparent elections.

Healthcare: Blockchain can securely store medical records and share them between institutions.

NFTs (Non-Fungible Tokens): Digital ownership of unique items (art, music, etc.) is verified on the blockchain.

**8. Advantages of Blockchain:**
**Security: **Data is stored in multiple places, making it harder to hack.

**Transparency: **All transactions are visible to participants in the network.

**Efficiency:** It can reduce the need for intermediaries (like banks or notaries).

**Reduced Costs:** By eliminating middlemen and reducing fraud, blockchain can lower costs.

**9. Challenges:**
**Scalability: **As the blockchain grows, it becomes more challenging to handle a large number of transactions quickly.

**Energy Consumption:** Proof of Work, especially in cryptocurrencies like Bitcoin, consumes a significant amount of energy.

**Regulation:** Governments and regulatory bodies are still figuring out how to manage blockchain-based applications, especially in areas like cryptocurrencies.

Blockchain technology has the potential to revolutionize industries by offering a more transparent, secure, and efficient way of managing data. However, it’s still evolving, and challenges such as scalability and regulatory concerns need to be addressed.

**Practical-1:HYPERLEDGER FEBRIC**


It is a permissioned blockchain framework designed for enterprise use, offering modular architecture, privacy through private channels, and customizable consensus mechanisms. It ensures secure and scalable transactions, allowing businesses to build tailored solutions for supply chain, finance, and healthcare.

to update the system
```bash
sudo apt update
```
to install golang-go

```bash
sudo apt install golang-go
```
to install docker
```bash
sudo snap install docker
```


to install git
```bash
sudo apt install git
```
to install fabric-samples
```bash
git clone -b main https://github.com/hyperledger/fabric-samples.git
```
to install curl
```bash
sudo apt install curl
```
to get in fabric-samples
```bash
cd fabric-samples
```
2cba31d9-fc1d-48dc-902f-70a5779f3526

to pull hyperledger docker images
```bash
sudo bash
curl -sSL https://bit.ly/2ysbOFE | bash -s
```

ed4f2ca3-9832-4180-aae7-cd793f2fc674

to get into test network
```bash
cd test-network
```
to up the network
```bash
./network.sh
```
```bash
./network.sh up
```
to create channel
```bash
./network.sh createChannel
```

577607d3-e238-48f2-aaed-4b79ad64bb35

to down the network
```bash
./network.sh down
```



Practical- 2 : IPFS
InterPlanetary File System is a decentralized protocol for storing and sharing files across a distributed network. By using content addressing (file hashes), IPFS removes the reliance on centralized servers, providing permanent and efficient file storage. It’s ideal for blockchain applications needing large off-chain data storage.

to install IPFS
```bash
wget https://dist.ipfs.io/kubo/v0.32.1/kubo_v0.32.1_linux-amd64.tar.gz
```

to use kubo
```bash
tar -xvzf kubo_v0.32.1_linux-amd64.tar.gz
```

![image](https://github.com/user-attachments/assets/1c77650e-6448-49e9-9ce1-b623476f409a)

to get into kubo directory
```bash
cd kubo
```
to move to local bin
```bash
sudo bash install.sh
```
to initialise ipfs
```bash
ipfs init
```

![6323373766448629554](https://github.com/user-attachments/assets/375709fa-751c-4307-8991-4a3791578309)

to use daemon
```bash
ipfs daemon
```
1a10884d-f0be-43cb-8de2-a9a9d351dbd4 3907b456-4a88-48ba-947a-9a64cdeb1e73

to add file
```bash
echo "Hello, komal!" > hello.txt
```
```bash
ipfs add hello.txt
```
```bash
ipfs cat <CID>
```
f2a3158b-e70f-41ab-bac9-7e563878664e

28e2d85e-354f-45ac-adc5-d1c2507255f5

to add a directory
```bash
mkdir myfolder
```
```bash
echo "File 1 content" > myfolder/file1.txt
```
```bash
echo "File 2 content" > myfolder/file2.txt
```
```bash
ipfs add -r myfolder
```
ef29ef9a-0da6-45a2-9e49-d1606524e427

lists running processes
```bash
ps aux | grep ipfs
```
to kill the process
```bash
kill <PID>
```
encrypting and decrypting
```bash
echo "hi komal" > myfile.txt
```
```bash
ipfs add myfile.txt
```
```bash
openssl enc -aes-256-cbc -pbkdf2 -iter 100000 -salt -in myfile.txt -out myfile_encrypted.txt -pass pass:yourpassword
```
```bash
ipfs add myfile_encrypted.txt
```
```bash
cat myfile_encrypted.txt
```
```bash
openssl enc -d -aes-256-cbc -pbkdf2 -iter 100000 -in myfile_encrypted.txt -out decrypted_file.txt -pass pass:yourpassword
```
```bash
cat decrypted_file.txt
```
```bash
ipfs add decrypted_file.txt
```
875effa0-41ee-4b1b-a2ae-9decfb23c4d8




   ![photo_6314183803450541654_y](https://github.com/user-attachments/assets/cd7b4be2-d904-4a26-a988-33c1b4f2f4fe)


**Practical-3 Metamask**

What is metamask? MetaMask is a crypto wallet and gateway to blockchain applications. It lets you store, manage, and transfer cryptocurrencies, especially those on the Ethereum blockchain and other EVM-compatible networks (like BNB Chain, Polygon, Arbitrum, etc.).

Steps to Create a MetaMask Account

**Step 1:** Install MetaMask Browser Extension: Go to https://metamask.io and download the extension for Chrome, Firefox, Brave, or Edge.

Mobile App: Alternatively, install the MetaMask app from Google Play Store or Apple App Store.

**Step 2:** Create a New Wallet Click “Get Started”.

Choose “Create a Wallet”.

Set a strong password (at least 8 characters).

Agree to the terms and conditions.

**Step 3:** Backup the Secret Recovery Phrase MetaMask will generate a 12-word Secret Recovery Phrase.

Important: Write it down and store it in a secure and offline place. Never share it with anyone.

Confirm the phrase to complete setup.

Your account is ready to use!



Now in order to add tokens in the wallet we can add them via sepolia faucet, these are the test token because we can't efford the etherum coin , also for the learning purpose we use them , these faucet can be get from the Google Cloud.

430856293-015216ac-1931-407c-a698-238a237f2c91

in the above we need to select our network and add our public key then click on recieve. you will get some test tokens... Screenshot (156)

Now if we want to send money,we can di it by....

clicking on send

Now enter the public key of whom you want to send tokens

Then, add tokens

And, continue

Screenshot (161)

**Practical-4** To learn solidity through cryptozombie
CryptoZombies is an interactive and game baesd platform where we can learn Solidity, the programming language used for writing smart contracts on the Ethereum blockchain. It teaches us by building a zombie game step-by-step. From different lessons we can learn the following:-



Lesson 1: Making the Zombie Factory

In this lesson we learned...

Solidity basics

Contract structure

State variables

Functions

Events

Here is the program I've created
```bash
pragma solidity ^0.8.0;

contract ZombieFactory {
    event NewZombie(uint zombieId, string name, uint dna);

    uint dnaDigits = 16;
    uint dnaModulus = 10 ** dnaDigits;

    struct Zombie {
        string name;
        uint dna;
    }

    Zombie[] public zombies;

    function _createZombie(string memory _name, uint _dna) private {
        zombies.push(Zombie(_name, _dna));
        emit NewZombie(zombies.length - 1, _name, _dna);
    }

    function _generateRandomDna(string memory _str) private view returns (uint) {
        return uint(keccak256(abi.encodePacked(_str))) % dnaModulus;
    }

    function createRandomZombie(string memory _name) public {
        uint randDna = _generateRandomDna(_name);
        _createZombie(_name, randDna);
    }
}

```

Lesson 2: Zombie Attributes

In this chapter we learnt:-

to access modifiers (public, private, internal)

msg.sender

Mappings

require statement
```bash
mapping (uint => address) public zombieToOwner;
mapping (address => uint) ownerZombieCount;

function createRandomZombie(string memory _name) public {
    require(ownerZombieCount[msg.sender] == 0);
    uint randDna = _generateRandomDna(_name);
    _createZombie(_name, randDna);
    zombieToOwner[zombies.length - 1] = msg.sender;
    ownerZombieCount[msg.sender]++;
}

```


Lesson 3: Advanced Solidity Concepts

in this lesson we learned to...

import

Inheritance

Function overriding
```bash
import "./ZombieFactory.sol";

contract ZombieFeeding is ZombieFactory {
    function feedAndMultiply(uint _zombieId, uint _targetDna, string memory _species) public {
        require(msg.sender == zombieToOwner[_zombieId]);
        Zombie storage myZombie = zombies[_zombieId];
        _targetDna = _targetDna % dnaModulus;
        uint newDna = (myZombie.dna + _targetDna) / 2;
        if (keccak256(abi.encodePacked(_species)) == keccak256(abi.encodePacked("kitty"))) {
            newDna = newDna - newDna % 100 + 99;
        }
        _createZombie("NoName", newDna);
    }
}

```

Lesson 4: Zombie Battle System

we learnt...

time units in Solidity (e.g., 1 days)

Cooldowns

Struct updates

Randomness
```bash
uint cooldownTime = 1 days;

function _triggerCooldown(Zombie storage _zombie) internal {
    _zombie.readyTime = uint32(block.timestamp + cooldownTime);
}

function _isReady(Zombie storage _zombie) internal view returns (bool) {
    return (_zombie.readyTime <= block.timestamp);
}
```


Lesson 5: ERC721 & Crypto Collectibles In this lesson we learnt...

ERC721 standard (NFTs)

transferFrom, ownerOf

Interfacing with other contracts
```bash
import "./erc721.sol";

contract ZombieOwnership is ERC721 {
    mapping (uint => address) zombieApprovals;

    function transferFrom(address _from, address _to, uint256 _tokenId) public override {
        require(_from == msg.sender || zombieApprovals[_tokenId] == msg.sender);
        ownerZombieCount[_to]++;
        ownerZombieCount[_from]--;
        zombieToOwner[_tokenId] = _to;
        emit Transfer(_from, _to, _tokenId);
    }
}
```
