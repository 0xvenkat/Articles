# Lumoz: ZK-RaaS & Modular Computation Engine 
#### Published July, 2024 for LVResearch

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/ce5f041d-b76a-4348-9798-3057be8ba9da" />

## Introduction
Have you ever heard of Rollup-as-Service or RaaS? 
Using this protocol you can spin up customized Rollups without any prior dev knowledge in less than 10 minutes! 

Simply choose the Rollup stack (Arbitrum, Optimism), Sequencer (Espresso, Astria), Settlement (Bitcoin, Ethereum) & Data Availability Layer (Celestia, Eigen, NERA) according to your requirement and use case - And, BINGO! You’re all set to deploy a production-ready modular Rollup! 
This makes the development of Rollups widely accessible, marching one step closer to Blockchain scalability and adoption.

Lumoz is one of the leading RaaS providers with more than $3.5 billion TVL that gives you the ability to deploy modular ZK-Rollups in a few clicks. The platform’s ZK-PoW algorithm run by permissionless miners takes care of ZK-Proof (ZKP) generation & other complex computational operations. The protocol also has an EigenLayer AVS for universal computation powered by zkProver and zkVerifier. The report below digs deep into the intricacies of the ZK-RaaS & Modular Computation Engine and presents you with a comprehensive analysis.

### 1. Background
Before we go ahead & deep dive into Lumoz, let’s set up some quick context by reviewing why exactly we need ZK-Rollups, how they work, and the current gaps with ZK systems.
By this time everyone who is involved in the web3 ecosphere knows that ZK-Rollups are the ultimate solution for Ethereum scaling. The technology first erupted when Ethereum was on the hunt for a secure & scalable solution.
Here the transactions are batched, rolled, executed off-chain, and a ZK-proof is posted back to the underlying Layer 1 chain. The process offloads the heavy computational energy from the canonical chain that reduces the cost of transaction processing & execution. All this while inheriting the security of the parent blockchain.

Optimistic Rollup is another type of Rollup that operates almost in a similar way. But, instead of sending ZK or Validity proofs, they first optimistically accept all the transactions and send Fraud proofs only if the network validators spot malicious activity.

In comparison to Optimistic Rollups, ZK Rollups are more secure and fast with their validity proofs & instant finality. Hence, they’re considered “The End Game” of blockchain scaling. But, unlike Optimistic Rollups, ZK needs much higher computational power to generate the validity proofs along with rarely available individuals having strong cryptographic & engineering skills. This is the reason why you see most Optimistic Rollups are functional while ZK-Rollups are still largely in production with only a handful of popular applications built over them.

However, the problems with ZK haven’t restricted founders, researchers, and thinkers to put a pause in ZK development. The space saw an explosion of new ZK-Rollups in the last few quarters.
According to L2Beat, currently, there are 26 ZK-based Rollups, 12 live & 14 in development across general & app-specific categories.

<img width="1614" height="1103" alt="Image" src="https://github.com/user-attachments/assets/86706472-9515-435f-84d2-c614a658ad12" />

With the advancement of the underlying infra layer & growing blockchain demand, the need for App-Specific Rollups, fancily known as RollApps, catering to a niche use case will go up significantly. But as mentioned above, ZK-based systems need massive computational capability & strong intellectual prowess. We need solutions that make the development of RollApps viable & simple.

### 2. Enters Lumoz ZK-RAAS
Presenting ZK-RaaS by Lumoz. Now developers or anyone interested can launch a ZK-Rollup in a few clicks without any prior ZK-tech knowledge. Lumoz’s ZK-PoW algorithm run by permissionless miners takes care of ZK-Proof (ZKP) generation & other complex computational operations required in the process.
With Lumoz’s RaaS platform, Devs can build customized Rollups fit for certain use cases in a few clicks and minutes. Think Lumoz is providing Lego blocks to build the ultimate ZK-Rollup of your dreams, tailor-made for your needs.

One can choose the base chain & zkEVM of their choice, garnish with the needed Data Availability (DA) Layer & Sequencers and finally add the preferred network (gas) token as the topping. Lumoz Prover run by miners will be the default Prover, responsible for generating ZKP for the security of assets.
The below chart shows all the options available in the Lumoz-RaaS platform to create a ZK-Rollup of one’s choice & requirement.

<img width="2318" height="2666" alt="Image" src="https://github.com/user-attachments/assets/e106c3b4-35f1-4742-92d9-2e39efe77a13" />

Lumoz deploys a Rollup Smart Contract (RSC) on each base chain (Bitcoin, Ethereum, Solana, etc) to manage the lifecycle of Rollups on that chain. Developers can lease a Rollup slot in exchange with MOZ (Lumoz native token) & gain access to an independent execution environment that they can customize according to their needs. This idea of leasing a slot is similar to Polkadot’s Parachain & Cosmos’s app chain lease.

Devs need not worry about the hardware requirements for DA, Sequencing, and ZKP generation as all of these will be managed by the Lumoz ZK-PoW cloud. Plus native cross-rollup connection can be implemented amongst chains with the same base. This will solve the massive problem of rollup fragmentation while enabling interoperability. We’ll learn more about these in the later sections.

#### 2.1 Lumoz Prover Network
By now you must have realized how big ZK Rollups are going to be in the near future. With this, the demand for ZK computation i.e. the Proving will also significantly rise up. To solve this Lumoz has got a cutting-edge Prover network powered by a ZK-PoW mechanism that incentivizes miners to provide ZKP computation power. We’ll deep dive into the components of the Prover Network in this section.

##### ZK-PoW Architecture

The Zk-PoW mechanism possesses several pieces illustrated below.

Zk-PoW Cloud: The cloud infra is responsible for ZKP computation coordination and management. It is deployed across multiple chains including Ethereum, BNB, Polygon PoS, and Lumoz.

Miner Nodes: These are the nodes operated by miners who contribute their computational power to perform ZKP computations. Miners can participate in the ZK-PoW network by running specialized software on their mining hardware.

ZKP task distribution: The cloud distributes tasks of generating and verifying ZK Proofs for Rollups to miners in a trustless manner.

ZKP Computation: The miner nodes receive the ZKP computation tasks, execute cryptographic algorithms, and perform complex calculations to generate the required proofs.

Proof Submission & Verification: The miner submits the generated proofs to the ZK-PoW cloud for verification where it verifies the correctness of the proofs to ensure validity & integrity.

Incentive Mechanism: Lumoz miners are incentivized for network participation, providing computational resources for ZKP generation and securing the network.

<img width="2222" height="1370" alt="Image" src="https://github.com/user-attachments/assets/27341a79-5e9f-4304-9138-053bfff6c129" />

Overall, ZK-PoW combines the power of miners' computational resources with Lumoz cloud infrastructure to provide efficient and scalable ZKP computation for a wide range of ZK-Rollups.

##### Aggregator
Aggregator is an important component of the Prover Network. It is responsible for distributing ZKP tasks, collecting task results (proofs), managing the proofs, and submitting them to the base chain for rewards. 

Based on function, Aggregator is divided into the following three modules:

<img width="1458" height="1234" alt="Image" src="https://github.com/user-attachments/assets/0f86acde-aa9b-4ccf-9343-32522bae999a" />

##### Lumoz ZK-PoW
Proof Generator

The Proof Generator module is responsible for assigning proof tasks to the Prover (miner network), receiving the task results (ZKP proofs), and storing the ZKP proofs in the DB database.

Proof Manager
The Proof Manager is in charge of managing the completed ZKP proofs and packaging the proofs that are ready for on-chain submission as tasks for the Proof Sender module.

Proof Sender
The Proof Sender module handles the on-chain submission of ZKP proofs by submitting them to the zkEVM contract deployed on the Base Chain.

### 2.2 Lumoz NCRC: Solving Cross-Rollup Communications

As we already saw in the above sections, in recent times a sea of Rollups has flooded the web3 ecosystem. On top of that consider platforms like Lumoz that give anyone the ability to spin up customized Rollups (zk) in under 10 minutes. Now, more and more rollups will pop up in no time.

Although this is great progress towards the scalability and adoption of blockchains, it creates major issues like liquidity fragmentation & poor UX. The funds present in one rollup are non-transferable to another in real-time. A user needs to use an unsecured bridge, have the gas token of that particular rollup, and wait for several minutes to perform simple transactions. From a tech perspective, the current Rollup bridging solutions often involve deploying new sets of interchain contracts on Rollup chains.

Enters Lumoz Native Cross Rollup Communication.
Each Rollup has a native L1<>L2 bridge. These operate through a “mint-burn” cross-chain mechanism, ensuring security through ZKPs and trustlessness. Lumoz uses this secured native bridge vs hack-prone third-party bridge to solve Rollup fragmentation and interoperability issues.


### 2.3 Lumoz RaaS Ecosystem
Currently, there are 18 Rollups, 2 in Mainnet & 16 in Testnet that are using the Lumoz ZK-RaaS stack.

<img width="15801" height="8888" alt="Image" src="https://github.com/user-attachments/assets/fb7bfadf-4a4b-4f8c-9cc5-edd05aed0e8d" />

Merlin Chain, a Bitcoin Layer 2 with $2.5B+ TVL accounts for 90% of the TVL, transactions & users for the Lumoz RaaS Platform.
Community-owned L2 ZKFair is another protocol that uses Lumos RaaS and has $220M+ TVL, 9K+ transactions & 670K+ users.

#### Lumoz Ecosystem Stats
<img width="861" height="441" alt="Image" src="https://github.com/user-attachments/assets/52fc1ad6-2d21-4eb3-8066-07a128c56a44" />

## 3. Lumoz as EigenLayer AVS
Recently, Lumoz announced the launch of the EigenLayer AVS Computation layer composed of zkProver and zkVerfier. zkProver will be responsible for generating the ZK-Proofs while zkVerfier will handle the verification of these proofs. The innovation will not only leverage Ethereum’s security via EigenLayer but will also provide additional incentives for the validators (miners). With Lumos AVS, developers and users now have the opportunity to take the application of the computational layer to other complex operations beyond ZK.

##### Lumoz Computation Layer

The Lumoz Computation Layer is composed of multiple modules. Besides providing a secure and efficient computation environment, the modular design of the layer enables open innovation for future use cases. The following are the main components of the Lumoz AVS Engine:

<img width="2616" height="3162" alt="Image" src="https://github.com/user-attachments/assets/2c7c3877-df48-49ea-8958-6df46234146b" />

Ethereum: Enables AVS operation via EigneLayer where the restaking mechanism guarantees AVS security.

EVM Chain: Supports EVM-compatible chains including Polygon, zkSync, and Scroll amongst others.

Lumoz AVS Oracle: Responsible for accruing and storing data; Ensures fast availability with integrity

Lumoz Chain: Core element of the Lumoz computation layer responsible for task scheduling, reward collection, zkProver & zkVerfier management.

zkProver: Generates zkProofs of the tasks and also executes other computation tasks.

zkVerifier: Verifies the generated zkProofs and other execution results.

#### zkProver
As already mentioned, zkProver is responsible for producing zero-knowledge proofs (ZKPs). 
It proves the data received without revealing the underlying information. 

Lumoz zkProver has three components zkRollup Prover, zkFraud Prover, and zkML Prover. 
Each one of them is developed for a specific use case. Below is the demonstration of the zkProver workflow.

<img width="8670" height="6002" alt="Image" src="https://github.com/user-attachments/assets/ac7b5c97-98cd-4a63-a83c-2b919dc7ba69" />

Task Acquisition: The Lumoz AVS Oracle receives tasks like generating proofs for (complex) computations from the Blockchain and pass on to the Lumoz Chain which it forwards to the Dispatch module.

Task Distribution: The Dispatch Module is responsible for distributing the tasks to the specific Provers based on requirements. The module dynamically allocates tasks to optimize efficiency and maintain a stable system.

##### Proof Generation:
zkRollup Prover: Focuses on generating proofs related to transaction batch compression.

zkFraud Prover: Generates fraud proofs that help detect and prevent improper behavior.

zkML Prover: Produces complex proofs related to ML model verification, ensuring the validity of model outputs without revealing the underlying model and input data

#### Proof Submission
The generated proofs are returned to the Lumoz Chain for verification and archiving.

#### zkVerifier
zkVerifier verifies the ZKPs submitted by the zkProver to the chain, ensuring the trust and security of the system. 
The workflow of the zkVerifier is as follows:

<img width="5397" height="5828" alt="Image" src="https://github.com/user-attachments/assets/e79ee016-f58b-4f5d-a16e-027a0a037972" />

Proof Submission: Proof Submitted by the zkProver to the Chain, initiates the verification process.

Proof Verification: Lumoz Chain sends the proof to multiple zkVerifiers, independently performing distributed verification.

Collective Decision: Atleast two-thirds of the verification nodes confirm the Proof’s validity to ensure the confirmation of the verification results.

Verification Result Processing: Valid Proofs are sent to the Lumoz Proof Contract on the Blockchain via the AVS Oracle. The Task Manager Contract records and responds to the task results on the Lumoz Chain.

## 4. Tokenomics
#### $MOZ & $esMOZ

Lumoz is fundamentally governed by two tokens MOZ & esMOZ.

MOZ: The Core Asset of the Lumoz Network

MOZ is the native token of the Lumoz network that has utilities across various spheres.
MOZ is the network (gas) token of the Lumoz Network that is used to pay the Transaction fees.

The utilization of the Lumoz Computational layer powered by ZK-Prover requires MOZ tokens to pay for the resources.

MOZ can be exchanged with esMOZ at a 1:1 ratio for additional utility.

esMOZ: Symbol of Incentives and Participation

ezMOZ has a crucial role in the Lumos network to incentivize the participants and boost network performance.

Miners who provide computational power to the Lumos Network get rewarded in esMOZ for their services.

esMOZ tokens act as tokens for participating in the network delegation mechanism and promoting decentralized governance.

esMOZ can be redeemed for MOZ with redemption rates varying based on the length of the redemption period.

<img width="3430" height="2245" alt="Image" src="https://github.com/user-attachments/assets/3df253b9-21c2-4388-b897-5a1a0d1d3f11" />

##### Lumoz Points
The Lumoz Network is supporting its early supporters by distributing Lumoz Points proportionate to their involvement with the platform. With the official launch of Lumoz mainnet, these loyal users will receive MOZ tokens as airdrop rewards based on established ratios. One can still collect Lumoz Points by participating in the ongoing Lumoz Node Sale Campaign. More on that in the next section.

## 5. Lumoz Node Sale
Lumoz Network with its deep expertise in the ZK-tech has optimized circuits and algorithms to make ZK computation more efficient while being affordable. The Lumoz zkVerfier Node Sale is providing opportunities to the web3 citizens to participate in ZK computation, secure the Lumoz Network, and earn rewards during the process.

##### Node Sale Rewards

40 Million Lumoz Points (can be exchanged for MOZ tokens after TGE)

25% MOZ incentive (after TGE)

Potential airdrops from Lumoz ecosystem chains

The Public Sale is currently live with 60K+ licenses already sold. Participate now before the campaign ends: (https://node.lumoz.org/)

## 6. Competitive Landscape
With the growing need for customized Rollups serving specific niches, the demand for RaaS providers has also proportionately gone up. 
The RaaS space is booming with many projects battling to serve the massive market. 
Already, $80M+ VC funds have been raised by the Top 4 RaaS providers. 

This shows the conviction of the elite minds for the growth of the sector. 
Below is a comprehensive analysis comparing the Top 4 RaaS protocols demonstrated in a chart. 

<img width="1274" height="790" alt="Image" src="https://github.com/user-attachments/assets/95a67dcb-6067-4b2c-a4f8-961091cde31f" />

## 7. Recent Updates
#### 7.1 Fundraising
On May 29th 2024, Lumoz announced the raise of an undisclosed strategic funding round. Participants include IDG Blockchain, Blockchain Coinvestors, Gate Ventures, Summer Ventures, EVG, SevenUpDAO, and Sweep Ventures.

This is shortly after its Pre-Series A Round of $6 Million at $120 Million valuation from Hashkey Capital, OKX Venture, Kucoin Ventures, Polygon, Comma3, Waterdrip, Bware Labs, YBB, Kernel Ventures, D11-Labs, MH Ventures, Kronos Research and Fermion Capital.
Before this, Lumoz raised a seed round of $4 Million in April 2023 led by Web3.com ventures.

#### 7.2 News
Node Sale Partnerships
Lumoz has partnered with many leading web3 organizations including NodeOps, YAY Network, and DIN to make the sale of zkVerifier nodes widely accessible.

Lumoz x Optimism
Recently Lumoz announced its Modular Compute Layer powered by Lumoz Prover Network will support the Op Stack + ZK Fraud Proof Layer 2 architecture.

## 8. Closing Remarks

Ethereum followed by other leading Layer 1 chains has chosen Rollups powered by ZK-tech as the preferred way of scaling. 
Protocols like Lumoz will make the development of customized modular Rollups a cakewalk without compromising on security. 

Super optimistic about the future of the project driven by strong tech, continuous innovation, and early traction backed by strong minds. 



