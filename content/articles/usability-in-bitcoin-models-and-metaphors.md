---
title: 'Usability in Bitcoin: models and metaphors'
slug: 'usability-in-bitcoin-models-and-metaphors'
tags: ["bitcoin", "ux"]
date: '2018-02-28'
image: '/articles/usability-in-bitcoin-models-and-metaphors/images/preview.jpeg'
socialimg: 'images/preview.jpeg'
featured: 'images/featured.jpeg'
intro: 'Through these next articles, I want to strengthen this relationship between
usability and security of people’s funds. This first one will be talking about the use of mental models and metaphors in Bitcoin intefaces.'
---

> “Usability is a quality attribute that assesses how easy user interfaces are to use.”
>
> From Nielsen Norman Group.

## The context

Bitcoin, as a software or protocol, is meant to be used by people and, therefore, should have its design as a relevant aspect to be developed.

Proper usability is one of the key elements to facilitate the portion of
user security and privacy that depends on how good is the interaction between the user and the software, especially, but not exclusively, to non-technical users. It makes Bitcoin more comprehensible, as well as offers the best options for action. It can not only avoid mistakes but also inform users about the best practices for keeping their funds safe, at the same time that makes these practices simpler.

Through these next articles, I want to strengthen this relationship between
usability and security of people’s funds. For this purpose, I’ll narrate some of
the main difficulties I find in Bitcoin’s usage and how the proposed approaches to some of these problems represented a big step forward in securing cryptocurrencies. I’ll leave out of this analysis any protocol improvements that, even though are crucial to security, did not affect Bitcoin’s usability directly.

## Mental and Conceptual Models

![picture of a lightbulb](images/image1.jpeg)

Bitcoin is a completely new system in a lot of ways. It’s a technological
innovation because it brings together different pieces of cryptography and
computer science to create a decentralized digital money that works. At the
same time, it’s an economic and politic innovation for the fiat money society,
since our previous idea of money was attached to the need for a central
authority to control and issue the coin.

One’s ability to grasp Bitcoin’s purpose and usage will depend on her
building a mental model of it. And, to make that possible, the builder
(programmer, designer, etc) should provide a good conceptual model in its
product.

> “A mental model is the representation that a person has in his mind about the object he is interacting with. A conceptual model is the actual model that is given to the person through the design and interface of the actual product.”
>
> Susan M. Weinschenk. 2011. 100 Things Every Designer Needs to Know About People.

The more aligned a person’s mental model is with the reality of how the system works, the smoother will be the interaction between her and the technology, i.e., usability will be better. So how do we help users build this mental model and what does this mean in terms of practical consequences?

The most obvious way to build a correct mental model is to study the relevant
aspects of Bitcoin through a well crafted and accurate material which will
provide a proper conceptual model. But that’s not what we expect to offer users when building solutions on top of the protocol. We have to make sure the person is in the best possible situation with only the local education through the interface itself. That’s how we get to the use of metaphors.

Metaphors are used to create a reference between a system people already
understand and are familiar with and the functionality of the new user
experience. A good metaphor hopes to illustrate a good conceptual model so that the person’s mental model will be aligned with reality and she will be able to make her own decisions instead of blindly following instructions (Norman, 2013). In Bitcoin, there are a few common metaphors used to create this parallel with the old financial system and I’m going to comment three of them here.

## Bitcoin as a coin

![picture of a coins](images/image2.jpeg)

As obvious as it may seem, this metaphor helps the understanding of bitcoin as a currency, where the “coins” are actually the unspent transaction outputs (UTXOs [(1)](#references)). People’s mental model of a coin is already attached to features like
using it to pay for goods, being divisible (coins of multiple values) and having the concept of change because you don’t always have a coin with the exact amount you want to pay.

Nevertheless, the materialization caused by the association with the term
“coin” has been a source of confusion for users that weren’t presented with the limits of this conceptual model. Bitcoins aren’t separate entities stored in a user’s computer wallet — much less a physical object — so the concept of “possession” gets very blurry if not properly presented. And **if the person doesn’t understand possession, she can’t know how to prevent theft**. Also, this sense of material makes people inclined to use other metaphoric expressions such as “sending” and “receiving” bitcoins. Again, without really understanding what defines who has the ability to spend the money.

So although it makes Bitcoin easier to grasp in the first moment, this is one of the metaphors that can lead to security breaches caused by the user’s own misunderstanding. Which consequently means that it doesn’t provide as good a usability as one would hope for such a protagonist element in the system’s vocabulary, but it’s what we have to work with so far. In this case, a complementary explanation beyond saying “it’s a digital coin” is primordial for anyone who’s going to have money on it. And that’s where some friendly step-by-step tutorials can come in.

## Addresses

![picture of a mailbox](images/image3.jpeg)

The number we call Bitcoin address is, in its essence, a derivation
from a user’s public key that passes through hashing and encoding algorithms. By creating a metaphor with physical or email addresses, we give the user a better sense of destination for a particular payment. However, there are a number of unintended consequences derived from this denomination, which makes the term “address” one of the most problematic of the common Bitcoin expressions.

Addresses give a strong sense of reuse and direct connection to a specific
person/entity. They make it seem as if the money has a “from” that you can
reply to. If someone sends me a message from an e-mail address, I’m inclined to think that I can later reply or send new messages to this same e-mail, even if that’s not necessarily true. **In Bitcoin, the reuse of addresses can lead to severe loss of privacy, possible security issues, and accidental loss** — in a possible case when the recipient doesn’t retain control over that address’s private key. The long-term validity implied by the term is exactly the opposite of what should be considered normal when it comes to Bitcoin, they are single-use tokens.

Also, some wallets implementations for Bitcoin show addresses as capable of holding balances, as if they were accounts. This misconception implies that that address will always hold the bitcoins until they are completely spent, i.e., if you spend half of “the balance” you should remain with the other half in the same address, which is not the case since wallet implementations usually send change to a different address. The unexpected consequence is that it’s possible to **create partial backups** for some addresses and lose the ones that actually have money.

This is, in my opinion, a failed metaphor that jeopardizes usability in bitcoin systems and the concept would be better represented by a term such as “payment code”, which has a stronger sense of ephemerality. Nonetheless, it can be a difficult saga to revert a whole naming pattern that is already spread through the industry. So, for now, builders can focus on making the limitations very clear when not able to use a new metaphor and, of course, apply other design elements to guide the user into proper behavior.

*Obs: he problem of partial backups is fairly addressed by BIP32 which I will talk about in my next article.*

## Mining

![picture of a mining tunnel](images/image4.jpeg)

The mining metaphor was a very clever way to bring familiarity for the computational race that gives writing permission of transactions on the
blockchain. Not that saying “Bitcoin mining” explains much or that the non-metaphorical explanation would be too complicated for non-technical people, that’s only a matter of having a good explainer and interested listeners. But it created a common vocabulary for regular use and reinforced the idea of Bitcoin as an asset with value.

Some of the aspects that are accurately illustrated by the metaphor are:

- Mining requires investment and effort.
- Mining activity should be competitive between miners, otherwise, you have a monopoly.
- Mining depends on a certain amount of luck, but also on a preparation to increase your chances of luck.
- Mining should be lucrative.
- The product of mining is an asset with financial value.
- The asset being mined is finite.

It isn’t a perfect reflection of Bitcoin, but no metaphor is supposed to be
taken to the extreme. The worst arguments I can have against the mining
metaphor are the following:

- Unnecessary use of metaphor in some cases where the actual understanding of how the technology works gets left behind over the desire to use hype Bitcoin words.
- Mental and subconscious reinforcement of Bitcoin as an extremely capitalist system. The incentives are capitalist, of course, but a generalized loss of idealistic view might lead us to nothing more than a PayPal 2.0.

## Not the best student

As I hope I could show, the use of metaphors to create conceptual models for new products is an imperfect technique. Especially if we’re dealing with a security critical system such as a digital decentralized money, helping users construct a correct mental model is as important as writing code with fewer vulnerabilities since people can be a vulnerability themselves. And the metaphor is an approach to make the user “get” how things work as much as possible without much engagement in studying.

Should this be the only method in creating an usable product? Of course not.

Building an interface with the proper design elements for user security (limitations, secure default options, avoid cognitive overload, warnings, confirmations, etc.) is a basic but huge step already. And, whenever possible, focus on the pursuit of the holy grail of user security: making them learn the real thing. Not the push of buttons or the pretty names, but the real workings of the technology. After all, Bitcoin is about sovereignty and we can only help people get so far.

##### References

(1) https://bitcoin.org/en/glossary/unspent-transaction-output
