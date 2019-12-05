---
title: 'Usability in Bitcoin: wallets'
slug: 'usability-in-bitcoin-wallets'
tags: ["bitcoin", "ux"]
date: '2018-05-11'
image: '/articles/usability-in-bitcoin-wallets/images/preview.jpeg'
featured: 'images/featured.jpeg'
intro: 'Following up the last two articles on Bitcoin usability, we’re going to approach the vast topic of wallets focusing on the advantages and disadvantages perceived in each described type in terms of usability.'
---

Following up the last two articles on Bitcoin usability, we’re going to approach the vast topic of wallets focusing on the advantages and disadvantages perceived in each described type in terms of usability.

Since wallet software is the main medium with which the regular user interacts when managing his bitcoins, it’s also one of the main places where mistakes can happen and attack vectors are explored. To distinguish and understand some usability issues and how they affect the safety of funds, let’s establish five main categories of wallets to be studied according to their type of key storage, based on [this paper](https://arxiv.org/abs/1802.04351):

1. Local key storage
2. Local key storage with password protection
3. Cold storage
4. Hardware wallet
5. Third-party storage

## The wallets

![picture of a wallet](images/image1.jpeg)

### 1.  Local key storage

This type of wallet stores your keys in a local file on a network-enabled device, usually going by the name “wallet.dat”. The greatest advantage of this model is the simplicity in terms of actions that a user has to perform. A quick task analysis will show the necessary steps to make a transaction:

1. Open wallet software.
2. Fill transaction information (amount, priority, address).
3. Hit “send” — i.e. construct and broadcast transaction.

In this case, the client has direct access to the keys in the wallet.dat file and the user doesn’t need to go through any other step to complete the task. Although this is the simplest interaction possible, which should indicate a strong usability advantage, the attack vectors that are possible with this type of wallet will counter-balance the usability in a negative way.

If your device that holds the wallet client is infected, for example, the attacker can easily access the key’s file and, consequently, the bitcoins. There would be no further obstacle between him and your money. Or he could intervene in your copy-paste process — like this malware— making you paste a different address from the one you wanted to copy and unknowingly send funds to the attacker’s address.

Other risks associated with this type of wallet are the accidental sharing of a folder that contains the key file, physical theft of the device and file destruction or deletion.

But why are attack vectors considered in the usability balance? To understand that, we simply have to remember what is the purpose of a wallet: to be a good interface to manage your bitcoins. And part of being a good interface to deal with an asset with value is being able to keep that asset safe. After all, what’s the use of the interface if you can’t access your money. Therefore, if security risks are derived from what the nature of the wallet allows, it’s definitely an issue of bad usability. We’ll see, in the following paragraphs, other types of wallet that have counter-measures against some of these attack vectors I presented. This means that, regarding those particular aspects, they have a better usability.

Considering the weight of the easiness to use and the risk of losing the money, the local storage wallet can play its part as an appropriate option for keeping a small amount of money which will be very easy to access. For example, you can keep a few dollars for a quick and trivial transaction that you might need to make.

### 2. Local storage with password protection

This type of wallet is very similar to the first one in the sense that a key file is stored locally in a device with a network connection. The difference here is in the use of a password chosen by the user to encrypt the wallet data. That way, a person need both the password and the key file to gain access to the bitcoins.

It might seem like an obvious improvement of security and, therefore, usability. However, the introduction of a password is not as effective as one would like to believe and it also introduces new problems, as we will shortly see.

In the case an attacker has infected your device with a malware, you are still very exposed since he could use a keylogger to identify the keys you are typing while entering the password — effectively watching you password — and send it back to himself. So, in this specific situation, it may be a bit of a security theater. There are a few mitigating approaches, like a digital pin pad that will display the numbers in a random order each time you enter the wallet, but they can’t guarantee safety.

Therefore, the scenario where password protection will make the most difference is the physical theft of the device in which the wallet is installed. That’s because the attacker will have the wallet.dat file but won’t be able to decrypt it instantly due to the unknown password. But if we’re dealing with a non-opportunistic attacker, i.e. that chose you specifically and knows what he is robbing, there is a strong possibility that he will first observe you to learn the password through a simple shoulder surfing (i.e. watching your screen over your shoulder from behind). Also, someone with physical access to your machine may infect it and then leave it there for you to continue using it, so he can now watch the password being typed.

On the other hand, we have to consider the problems brought up when the user’s cognitive requirement is increased by the need to choose and memorize a password. One of two options will be true:

- The user will choose a weak password.
- The user will choose a strong password.

In the first scenario, the user will have chosen an easy password — something small, something with personal meaning or a password used in other services — and the attacker will be able to brute-force his way around it — whether with specific knowledge about the victim or with password tables. There is, of course, the advantage of buying some time to move your funds to another wallet, if you quickly notice the attack. The problem is that, in the case of a malware attack, it’s pretty common for it to stay hidden until it’s too late to take any measure.

In the second scenario, a good password will be chosen in the most random possible way and with a significative number of characters. You can be quite certain that the attacker won’t be able to brute-force this password. You will have to make sure you remember it, though. And, since remembering large pieces of information with no apparent meaning is a hard task for the human brain, the break in the usability will be quite significant.

One option is to actually memorize the password, a cumbersome job. Another is to store the password somewhere — be it on a piece of paper or on your device — and force you to access that password every time you need to send a transaction. The latter degrades usability because you need to worry about one extra element — the location of the password— each time you open your wallet, at the same time that you’ll have to worry about it being stored in a safe place where no one will see. Both can result in the not unlikely scenario where the user will forget or lose the password, turning a security measure into the actual cause of financial loss. And, just to reinforce it, if the device is compromised, the user will be vulnerable with any of these schemes.

The task analysis for sending a transaction in this wallet will look the following:

1. Open wallet software.
2. Remember/access the password.
3. Fill transaction information.
4. (Re-enter the password, depending on the wallet implementation).
5. Send.

Even though just one extra is necessary, it’s a very problematic one. The usefulness of this type of wallet will depend on the security model of the user and what are the main risks he is vulnerable to in his daily life.

### 3. Cold Storage

Cold storage refers to the method of keeping the wallet keys offline, i.e. without ever having passed through a device with a network connection. It’s probably the most secure option of storage if done correctly. However, it’s very unlikely that a non-expert user will be able to complete the setup process correctly. Also, once it’s set, spending the money without compromising the storage is complex and, therefore, it’s not meant to be used for funds that should be quickly available or that need constant access.

In addition, the choice of where the keys will be stored will introduce problems of their own, such as deterioration of the material, water damage, magnetic damage, easy reading by others — in the case of paper wallets, loss, theft, etc. So not only the setup is difficult, but also the posterior storage in the physical world. The potential security of this method comes at a high price in the usability of managing the bitcoins.

In contrast, this type of wallet has a curious advantage — considering the setup was successful. Since there is no risk of digital attack, the user only has to worry about the physical security of the keys, which is considered much easier — centuries of experience with physical security make us feel more comfortable with it than with digital security, which is much more abstract.
The task analysis for this wallet will be omitted due to its highly complex nature, involving a great number of steps that can vary a lot depending on the storage choices.

As it was said before, this isn’t a trivial method so a user should choose it only if:

- He’s an expert.
- He has enough money that’s it’s worth for him to educate himself deeply about how to create the wallet or to pay an expert to guide him — which is a dubious choice because of the trust he will put upon the expert.

In both cases, the funds should be destined for a long-term storage without the need to be accessed frequently.

### 4. Hardware wallets

Hardware wallets store the private keys in a secure hardware device that is used to sign transactions. The device is connected to a network-enabled computer (usually through the USB port) that doesn’t need to be trusted because the hardware wallet will, hopefully, never communicate the private keys to it.

After you connect the hardware wallet to your computer, the process of using the wallet is very similar to regular wallets. One important difference is in the validation of the transaction information, which is usually implemented. The original model of the Ledger wallet, one of Bitcoin’s hardware wallets, used a security card specifically made for your wallet. The Trezor wallet, another widely used hardware wallet, uses the independent wallet display to confirm the information that is being shown on the computer screen. Whatever the method, it requires an extra learning from the user and extra attention (cognitive load) every time a transaction is sent.

To better visualize the user’s action, let’s take a look at the task analysis for sending a transaction:

1. Connect hardware wallet device to the computer.
2. Open wallet software.
3. (Provide further authentication, if necessary, such as a PIN.)
4. Fill transaction information.
5. Validate transaction information.
6. Send.

There are two major difficulties for the user in the regular use of a hardware wallet:

- The necessity to have a special device every time the wallet needs to be accessed, which might create a burden of having to remember and carry around carefully one more small object, besides the usual objects a person has to worry about (phone, home keys, car keys, wallet, glasses, etc).
- The validation process, which needs to be learned and requires focused attention — and might even require another object to be carried, such as Ledger’s security card.

Other problems associated with the hardware wallet, but that are not part of the regular use, are:

- Risks of tampering on the issuance and transportation stages. If someone tampers your device before you receive it, it loses all its appeal of security. This entrusts the user with the responsibility of properly verifying the integrity of the package according to the manufacturer’s specifications. — As a side note, this is a kind of “unaddressed” issue, since some security professionals agree that there isn’t a manufacturer that uses a really secure packaging. And that the use of a more secure one would possibly result in an excessive verification process for the user that may just ignore it favor of practicality.
- Risk of losing the device — be it a memory slip or a theft. As a small device, the risk of the user losing it is significant and will result in a stressful situation. A proper backup will mitigate the risk of financial loss if the problem was only a memory slip resulting in the device having an unknown location. In the case of theft, the barrier against the robber having access to the money would be the previous setup of a password by the user to encrypt the wallet. This will buy time for the user to recover his backup and move the funds, but will also add in the cognitive load of using the wallet because now a password needs to be used as well.
- Cost of the product. Hardware wallets are devices offered by companies for buying and the cost will probably be a barrier if the user feels his security model doesn’t require this spent. Unfortunately, the accuracy of his assessment of whether he should or not spend the money in a hardware wallet — which usually sums up to the amount in Bitcoin he has to protect — will not always be reliable.

Although it adds to the difficulty of the task of managing bitcoins, the hardware wallet is relatively simple to use in comparison with a Cold storage, for example, and it provides much better security than the local storage of keys. In theory, it’s immune to network attacks that take advantage of compromised computers, which is a lot to say about a wallet. Also, it can easily be used for regular transactions, different from the Cold Storage. Therefore, this is probably the best wallet for the common user who needs a good balance between security and simplicity of use and learning.

### 5. Third-party storage

Third-party storage is the outsourcing of the responsibility of storing the private keys to another party, usually a company that provides this service. This is the most familiar — in the sense that doesn’t require much learning — method of managing bitcoins for most users because the necessary steps to use it are common to many internet services: register an account and use a dashboard. No other burdens exist here, such as downloading software, creating a backup or buying a device. It’s the most straightforward way of using a bitcoin wallet and that’s why so many novice users choose it.
But does this mean a good usability?

Apart from the security risks, which will be mentioned in the following paragraphs, there is a huge usability problem with third-party storage that affects most poorly-informed users: it violates the user’s mental model of a Bitcoin wallet.

The expectations about a Bitcoin wallet will generally involve, at least:

- Being able to send your bitcoins to others.
- Being able to request others to send you their bitcoins.
- Storing your bitcoins.

Which leads us to the violation perpetrated by the third-party storage: the bitcoins are not yours, they belong to the service that is providing you the management dashboard. They promise to keep it safe and to let you use it when you want — it’s an IOU. This situation is analogous to the myth that the money you have in a bank account is yours. It’s actually the bank’s money and they, hopefully, will let you take it back when you want.

For you to be able to say that you possess the bitcoins, you have to be in control of the private keys that control those coins — likewise, the money you have in your physical wallet that is kept in your pocket is actually yours. This is the case with every other wallet described in this article, but not with the third-party wallet.

If users don’t realize the truth of their situation, as is the case of many users that choose the third-party model due to it being easy, they won’t be able to correctly determine the risks they are willing to take. Which leads us to four great financial risks of third-party wallets:

- **Fraud**. Some wallet “services” are actually groups of fraudsters taking advantage of a new ecosystem full of uninformed people that moves a great amount of value. After functioning for a while, they will simply disappear with their money — which the users thought was theirs.
- **Bugs/unexpected situations**. If a wallet service makes a mistake that costs it a lot of money — having the wrong exchange price and letting people buy bitcoins for 100 dollars instead of 1000 dollars, for example — it might become insolvent. This means that there won’t be enough money for everyone to withdrawal back to their local wallets and, consequently, people will lose money they thought it was theirs.
- **Hacking**. Since the wallet service now holds the funds from many different users, they become a huge honey-pot for attackers. Now, even if it takes the attackers a long time and a good amount of money invested, it will be worth it because the prize will be much more money than it would be if they attacked a single user.
- **Privacy/censorship**. A third-party service will be able to follow all your transactions, creating a profile of your spending habits, which goes against the expectation of having a certain level of privacy in Bitcoin. Things will be significantly worse if a KYC/AML process is required, as it is the case with many of the third-party services provided today, because you’ll be completely identified. Not only will you be at risk of having this valuable personal information leaked — when a government agency not so kindly asks the company, for example — but you’ll have the possibility of being directly censored if the wallet decides to block certain kinds of payments.

Does this mean that third-party wallets are useless? Not really, but the user has to be aware that he is accepting all those risks when he decides to use a service of this type. It’s usually a necessary trade-off for people that do day-trading and need the money to be readily available for exchange between currencies. And it can still be used by eventual exchanges between currencies where the user quickly withdrawals the money after the operation is complete.

## Real life storage

![picture of a chest](images/image2.jpeg)

The reality for the user is that to take advantage of the different features of each wallet, he will need to learn about all of them and divide his funds into the appropriate methods for different situations. It’s possible, for example, that a user divides his money in the following way:

- Most of his money in a hardware wallet with a backup that is kept as a paper wallet cold storage — maybe with a multi-signature scheme if it’s a more experienced user.
- A little money in a local storage wallet in his smartphone.
- Active third-party wallet account in an Exchange where eventual transactions are made.

This doesn’t mean it’s the best or the only way to divide your storage. There are actually people considered experts in Bitcoin who declare that they keep most of their money in third-party storage because they don’t trust themselves to do it the right way. The point is: it’s a conscious and informed decision based on their necessities.

Even though it’s quite an amount of learning, it’s expected that the user will dedicate more time to educate himself according to the increase in the value he holds. In other words, if a user is very new to Bitcoin and has only a few dollars, he won’t have to learn much. Almost any option will work for him — even the less secure ones — because the value at risk is very low. If a user has a considerable amount of money — a threshold that will vary according to the user’s perception — he is expected to dedicate more time and money to protect his bitcoins.

In the end, a wallet’s usability will be perceived as better or worse depending on the situation it’s applied. It’s all about how it balances the easy operational tasks the user has to perform with the need to keep the funds protected.