### Fractal Bitcoin Overview

**Website:** [Fractal Bitcoin](https://fractalbitcoin.io)

**What is Fractal Bitcoin?**

Fractal Bitcoin is the only Bitcoin scaling solution that uses the Bitcoin Core code itself to recursively scale unlimited layers on top of the world’s most-secure and -held blockchain.

It is the first instance of a virtualization methodology applied to Bitcoin in the world. Fractal gradually extends the Bitcoin blockchain into a scalable computing system without breaking consistency with the Bitcoin main chain.

With strong tooling and support, building on Fractal is straightforward.

### Running Fractal Bitcoin

**Run on linux:**
open two Terminals -

In first terminal run these commands 

1. Download the release:

```bash
wget https://github.com/fractal-bitcoin/fractald-release/releases/download/v0.1.8/fractald-0.1.8-x86_64-linux-gnu.tar.gz
```

2. Extract the files:

```bash
tar -zxvf fractald-0.1.8-x86_64-linux-gnu.tar.gz
```

3. Navigate to the directory:

```bash
cd fractald-0.1.8-x86_64-linux-gnu
```

4. Set up the data directory:

```bash
mkdir data
cp ./bitcoin.conf ./data
```

5. Run the Bitcoin daemon:

```bash
./bin/bitcoind -datadir=./data/ -maxtipage=504576000
```

**Using Docker:**

1. Clone the repository:

```bash
git clone https://github.com/fractal-bitcoin/fractald-release.git
```

2. Navigate to the Docker directory:

```bash
cd fractald-docker
```

3. Start the service with Docker Compose:

```bash
docker-compose up -d
```


Open the second terminal, and go to the cd fractald-0.1.8-x86_64-linux-gnu/bin directory

Create a Legacy wallet

./bitcoin-wallet -wallet=TestnetWallet -legacy create



Dump Bitcoin wallet private key

Dump pkey command 
#to check your home name and path echo $HOME 

./bitcoin-wallet -wallet=/home/YOUR_NAME/.bitcoin/wallets/TestnetWallet/wallet.dat -dumpfile=/home/YOUR_NAME/.bitcoin/wallets/TestnetWallet/MyPK.dat dump


Go to the data wallet directory 

1. cat MyPK.dat 
2. The last string is your PK



#3. Import PK into Unisat 

1. Copy that PK from the previous step 
2. Open Unisat Wallet -> Settings cog -> Expand view -> Top left corner click on the wallet #1 ->  Top right corner click on the "+" icon  -> Restore from single private key -> paste key -> Select wallet type, I created legacy wallet in my case.





