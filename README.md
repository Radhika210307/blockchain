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
8a8af518-ddc5-45bb-b015-31e93945fda8

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
./network.sh up
```
to create channel
```bash
./network.sh createChannel
```bash
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
e7b71e7d-a8d3-4b68-a3c9-2ed12403307a

to use kubo
```bash
tar -xvzf kubo_v0.32.1_linux-amd64.tar.gz
```
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
```bash
a03f8658-b73e-4f68-8e4d-9396b86d367b

to use daemon
```bash
ipfs daemon
```
1a10884d-f0be-43cb-8de2-a9a9d351dbd4 3907b456-4a88-48ba-947a-9a64cdeb1e73

to add file
```bash
echo "Hello, komal!" > hello.txt
ipfs add hello.txt
ipfs cat <CID>
```
f2a3158b-e70f-41ab-bac9-7e563878664e

28e2d85e-354f-45ac-adc5-d1c2507255f5

to add a directory
```bash
mkdir myfolder
echo "File 1 content" > myfolder/file1.txt
echo "File 2 content" > myfolder/file2.txt
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
```bash
encrypting and decrypting
```bash
echo "hi komal" > myfile.txt
ipfs add myfile.txt
openssl enc -aes-256-cbc -pbkdf2 -iter 100000 -salt -in myfile.txt -out myfile_encrypted.txt -pass pass:yourpassword
ipfs add myfile_encrypted.txt
cat myfile_encrypted.txt
openssl enc -d -aes-256-cbc -pbkdf2 -iter 100000 -in myfile_encrypted.txt -out decrypted_file.txt -pass pass:yourpassword
cat decrypted_file.txt
ipfs add decrypted_file.txt
```
875effa0-41ee-4b1b-a2ae-9decfb23c4d8




   ![photo_6314183803450541654_y](https://github.com/user-attachments/assets/cd7b4be2-d904-4a26-a988-33c1b4f2f4fe)


**IPFS**
Commands (IPFS)
1.	Install the IPFS through WSL: wget https://dist.ipfs.tech/kubo/v0.32.1/kubo_v0.32.1_linux-amd64.tar.gz 
Or 
wget https://github.com/ipfs/kubo/releases/download/v0.32.1/kubo_v0.32.1_linux-amd64.tar.gz
2.	tar -xvzf kubo_v0.32.1_linux-amd64.tar.gz
3.	Kubo is a reference implementation of IPFS in Go: cd kubo 
4.	ls
5.	sudo bash install.sh
6.	ipfs –version
7.	ipfs init
8.	ipfs daemon
9.	On Browser: http://127.0.0.1:5001/webui
10.	To run ipfs daemon in background: ipfs daemon > ipfs.log 2>&1 &
11.	This is daemon ID: [1] 772
12.	Add file: echo "Hello, IPFS!" > hello.txt
13.	ipfs add hello.txt
14.	ipfs cat <CID>
15.	Add a directory: 
mkdir myfolder
echo "File 1 content" > myfolder/file1.txt
echo "File 2 content" > myfolder/file2.txt
16.	ipfs add -r myfolder
17.	ps aux | grep ipfs
18.	kill <PID>
19.	in Browser you can directly run this to see the IPFS: https://ipfs.io/ipfs/QmWd9cavD8UGZQcqYBVhZqs2Jure5W9cgxR7S6TC4StfZe

