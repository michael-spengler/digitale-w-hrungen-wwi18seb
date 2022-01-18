# Übungsklausur 2 - Under Construction

## Grundlagen zur Blockchaintechnologie
### Einwegfunktionen

### asynchrone Verschlüsselung / Public Key Verschlüsselung --> 1. Digitale Signaturen (Authentizität) 2. Verschlüsselung an sich (Privacy)

### Datenstrukturen (Merkletrees, Bloomfilter, Merkle-Patricia-Trie)
Erläutern Sie einen Anwendungsfall von Bloomfilters   
Bitset Länge Optimieren / Number of Hash Functions optimieren   
Inwiefern spielt die Anzahl der genutzten Hash Funktionen bei einem Bloomfilter eine Rolle...?
https://hur.st/bloomfilter/?n=100000&p=0.6&m=&k=1


### Konsensalgorithmen 
Proof of Work  
Proof of Stake 

### Implementierungen 
#### TypeScript
https://deno.land/x/bloomfilter  
https://deno.land/x/merkletrees  
https://deno.land/x/tries
https://deno.land/x/hash


```ts
import { BloomFilter } from "https://deno.land/x/bloomfilter/mod.ts"

const bloomFilter = new BloomFilter(1024)

const expectedExampleArray = ["dog", "chicken", "cat", "ant", "spider", "lion", "tiger", "elephant", "giraffe", "monkey", "uhu", "bird", "fish", "chamäleon"]

for (const entry of testArray) {
    bloomFilter.add(entry)
}

```

#### Solidity
tbd

## Anwendungsgebiete der Blockchaintechnologie
### Digitale Währungen 
CBDCs vs. Ether

### Decentralized Finance

### Decentralized Governance 
Votingpower hängt z.B. von der Anzahl der gesammelten governance tokens ab... 
https://github.com/distributed-ledger-technology/airdrop

### Decentralized Web
Distributed Deployments & DDNS- see https://ens.domains  

### NFTs - Kunst / Collectibles
```sol
tbd
```

### Implementierungen 
#### TypeScript
https://deno.land/x/web3  
https://deno.land/x/airdrop  

Welche Informationen und Module benötigen Sie wenn Sie einen Airdrop für Ihre Early Adopters gestalten möchten, welchen Sie über ein TypeScript Programm lancieren?

1. Empfänger Wallet Address
2. ABI
3. https://deno.land/x/web3


```ts

``` 

#### Solidity
### ERC20 Basics
Ziel: Der folgende SC soll eine Währung namens QuinoaCoin mit den folgenden Eigenschafte definieren:  
1. Nachkommastellen: 18
2. Gesamtzahl an Tokens (fixed supply): 2000000

Bitte streichen Sie fehlerhafte Zeilen und ersetzen Sie diese durch korrekte Anweisungen:   

// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.8.0 < 0.9.0;

import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/release-v4.4/contracts/token/ERC20/ERC20.sol";


contract QuinoaCoin is ERC20 { 


    constructor () ERC20("QuinoaCoin", "QNC") { 
    
        
        _mint(msg.sender, 2000*10**17);
    
    
    }
    
}



## On-Chain / Off-Chain Verbindungen
Example: https://deno.land/x/airdrop@v0.1.0/example-airdrops/launch-airdrop-for-wwi19seb.ts ... via TypeScript programm
Application Binary Interfaces Usage Example: https://deno.land/x/airdrop@v0.1.0/src/airdrop-service.ts#L16 ... um eine Repräsentation des Smart Contracts (der z.B. auf der Ethereum Blockchain deployed ist) im TypeScript Programm zu erhalten und damit Funktionen dieses Smart Contracts vom TypeScript Programm aus zu triggern.


### Implementierungen
#### TypeScript
https://deno.land/x/airdrop@v0.1.0/example-abis/ropsten-0x7910f84868488da3377833ccaa0e5b2b42edd9a6.ts


#### Solidity


## Eigeninitiative / Eigeninteresse
Describe you own favorite topic wrt the Blockchain space (4 Punkte)    








