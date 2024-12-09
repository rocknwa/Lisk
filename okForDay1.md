Layer 2 (L2) is a collective term to describe a specific set of Ethereum scaling solutions. A layer 2 is a separate blockchain that extends Ethereum and inherits the security guarantees of Ethereum.

Now let’s dig into it a bit more. To do this we first need to explain layer 1 (L1).

What is layer 1?
Layer 1 blockchains, such as Ethereum and Bitcoin, are the underlying foundation that layer 2 projects build on top of. Examples of layer 2 projects include zero-knowledge rollups and optimistic rollups on Ethereum and the Lighting Network on top of Bitcoin.

Ethereum also functions as a data availability layer for Layer 2s, and if there are any disputes on previous transactions data is provided from Ethereum for these disputes.

Ethereum as the layer 1 includes:

a network of node operators to secure and validate the network
the blockchain itself and the history of transaction data
the consensus mechanism for the network

Why do we need layer 2?
The three desirable properties of a blockchain are that it is decentralized, secure, and scalable. The blockchain trilemma states that a simple blockchain architecture can only achieve two out of three. Want a secure and decentralized blockchain? You need to sacrifice scalability. This is where layer 2 networks come in.

Ethereum has reached the network's current capacity with 1+ million transactions per day, with high demand for each of these transactions. The success of Ethereum and the demand to use it has caused gas prices to rise substantially. Therefore the need for scaling solutions has peaked as well.

Scalability
The main goal of scalability is to increase transaction speed (faster finality), and transaction throughput (high transactions per second), without sacrificing decentralization or security (more on the Ethereum vision).

The Ethereum community has taken a strong stance that it would not throw out decentralization or security in order to scale. Until sharding, Ethereum Mainnet (layer 1) will only be able to process roughly 15 transactions per second. When demand to use Ethereum is high this causes network congestion, increasing transaction fees, and pricing out those who cannot afford it from using Ethereum until the fees reduce. That is where layer 2 comes in to scale Ethereum today.

💸
Lower fees
By combining multiple transactions into a single transaction on layer 1, transaction fees are massively reduced, making Ethereum more accessible for all.

🔐
Maintain security
Layer 2 blockchains settle their transactions on the Ethereum Mainnet, allowing users who use them to benefit from the security of the Ethereum network.

🛠️
Expand use cases
With higher transactions per second, lower fees, and new technology, projects will expand into new applications with improved user experience.

How does layer 2 work?
As we mentioned above, layer 2 is a collective term for Ethereum scaling solutions that handle transactions off Ethereum layer 1 while still taking advantage of the robust decentralized security of Ethereum layer 1. A layer 2 is a separate blockchain that extends Ethereum. How does that work?

There are several different types of layer 2, each having their own trade-offs and security models. Layer 2s take the transactional burden away from the layer 1 allowing it to become less congested, and everything becomes more scalable.

Rollups
Rollups bundle (or 'roll up') hundreds of transactions into a single transaction on layer 1. This distributes the L1 transaction fees across everyone in the rollup, making it cheaper for each user.

The transaction data in the rollup is submitted to layer 1, but the execution is done separately by the rollup. By submitting transaction data onto layer 1, rollups inherit the security of Ethereum. This is because once the data is uploaded to layer 1, reverting a rollup transaction requires reverting Ethereum. There are two different approaches to rollups: optimistic and zero-knowledge - they differ primarily on how this transaction data is submitted to L1.

Optimistic rollups
Optimistic rollups use fault proofs where transactions are assumed to be valid, but can be challenged if an invalid transaction is suspected. If an invalid transaction is suspected, a fault proof is ran to see if this has taken place.


KEY TAKEAWAYS:
— The perfect blockchain boasts three elements: Security, decentralization, and scalability. But finding a balance between the three is difficult and presents a problem referred to as the blockchain trilemma.

— Scalability and decentralization are often held back by security, but security tends to be compromised by any shifts on a network that offer scalability.

— Projects either choose to focus on two out of three or work on finding a solution to tackle the trilemma once and for all. Innovative ideas like sharding, side-chains and state channels are used to address the trilemma but they’re still experimental.

— A solution to the problem could lead to greater adoption of cryptocurrency and blockchain and a wide-spread use of the technology across industries.
Security. Decentralization. Scalability. Three of cryptocurrency’s pillars that all seem to constantly strive to co-exist but struggle to live in harmony.

The blockchain trilemma, as coined by Vitalik Buterin himself, refers to this idea and it’s leading to some interesting ways that projects and networks are looking to solve the problem once and for all. But what exactly is the blockchain trilemma, and why isn’t there an easy solution? Let’s get into it!

The Three Fighting Factors
You know how you can’t balance a social life, work, and sleep easily? The blockchain trilemma is similar. It’s the belief held across the cryptocurrency community that truly decentralized networks need to choose between security and scalability. Let’s have a quick look at them before we dive in.

What is Decentralization?
Decentralization talks about how control is shifted from one central entity, company, or government and is split across smaller groups to govern something. In blockchain, decentralization gives power to people across the world to govern using their computer (crypto nodes) rather than having a central control of the network live with one person or party.

What is Security On The Blockchain?
Blockchain is inherently secure, but is not entirely immune to hacking. If a hacker is able to secure control of more than half of the network (51%), they are able to alter a blockchain and manipulate transactions to steal from the network. In blockchain, the more nodes, the more security.

What is Scalability?
Scalability in blockchain is the same as in business – it refers to how much a network can grow in the future while maintaining the same sort of transaction speed and output.

Scalability and decentralization tag-teaming up tends to compromise security, while security restricts changes that allow the decentralized network to scale. Why? Well, basically because decentralized networks take a bit of work to operate and it makes scaling a little difficult.

Decentralization and Security: Blockchain Best Friends
Decentralization is basically the backbone of blockchain and cryptocurrency. It means there is no central authority or entity driving the project and eliminates the need for third parties to allow industries to operate. For example, in traditional finance, we’ve got banks. They’re centralized and act as a party that sits in the middle between you and your money. This is generally accepted because banks take responsibility to offer a way for us to store and send money safely – we expect money to go where we send it and in exchange for security we give some control of our money.

With blockchain, decentralized networks hand the keys to the individual, with direct access to their money. 

It does this by making use of community control and relies on blockchain technology rather than the corporation. Blockchain, by means of a set of self-executing rules, offers an alternative to a middleman approach. The network keeps its security because each transaction needs to be validated by more than half of the network’s nodes (and remember: the more nodes that are part of the network, the more the blockchain becomes decentralized, enhancing the security that the network offers). 

This is great because no one is in control, but it comes with a bit of a tricky drawback: because of the sheer weight of information processed to maintain the shared system, transaction times can be slow, and the system is harder to scale.

Adding in Scalability and the Threat It Presents to Security
On a blockchain, you can think of each bit of information as something with weight. As more information is added, the data becomes heavier and it is slower to move around. It’s important to keep the information up to date to streamline the cumbersome amount of information moving around. One way of doing that is by limiting how far and wide the blockchain is distributed.

But, by limiting how far the network is spread, there is less of a barrier for attackers who want to take over the network. This means there’s more chance of an attack because hackers will have an easier time taking over enough of the network and they’ll be able to manipulate the blockchain. It’s not ideal and it shows how adding in scalability to the blockchain trifecta comes at a price.

But Why Do Blockchains Need To Scale?
You know how awful it is to sit in traffic? Traffic on a road exists because roads weren’t built to scale the number of cars that would be on the road at the same time. Imagine every time you had to make a transaction, you had to wait in traffic for your transaction to be validated and go through. And more people transacting means the more the network and validation process needs to happen. It creates traffic on an unscalable network, presenting an unsustainably slow approach.

So simply put, if blockchain technology is going to reach any sort of mass adoption, scalability is critical. If a network can’t scale, it just won’t be able to compete with traditional platforms in convenience, transaction speed, and throughput. 

So to scale, a project either needs to cash in security or decentralization, right? Well, no.
