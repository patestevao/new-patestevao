---
title: 'Lightning wallet wireframes'
slug: 'lightning-wireframes'
tags: ["bitcoin", "ux", "mobile"]
date: '2019-11-29'
image: '/work/lightning-wireframes/images/preview.png'
socialimg: 'images/preview.png'
featured: ''
intro: 'Wireframes concepts for a Bitcoin Lightning network wallet.'
---

## About the wireframes

The following wireframes represent a mobile Lightning-enabled Bitcoin wallet and were developed to support my talk about “Designing Lightning Wallets for the Bitcoin User”, presented on July 3rd, 2018 at the Building on Bitcoin Conference in Lisbon.
For a better understanding of what is being proposed with the following designs, [you can listen to the talk here](/talks/designing-lightning-wallets).

### The Concepts

The image below illustrates the “Send” page of a Bitcoin wallet with elements that are fundamental to this operation. After the user inputs the address, clear feedback is given on whether it calls for a regular Bitcoin transaction or a Lightning transaction. The interface, then, adapts to the situation, as it does with the elimination of the Priority section for Lightning transactions.

![Send page](images/lightning-wireframes1.png)

The concept for the request page proposes the use of two modes, which are selected by the use of the toggle button on top and define the type of payment that is being requested. The complete change of the background color for each mode is the proposed feedback in order to avoid mode-error.

![Request page](images/lightning-wireframes2.png)

One of the most important messages of the talk is that we can remove Channels operations from the user’s main activities and leave it as a last resort approach to failed payments. Such as the following example, where the link displayed in the error message would take users to the “Open channel” page.

![Request page](images/lightning-wireframes3.png)

Apart from an occasional necessity as showed above, Channels operations could be accessed by a less prominent part of the interface, such as the proposed “Lightning actions” section located on the settings page. That’s because they can be useful for more experienced users.

![Request page](images/lightning-wireframes4.png)

Finally, I purpose the design of a “wallet page”. It highlights the total amount of wallet funds in bitcoins, but it also shows the division between regular wallet funds and funds committed to Lightning channels. This last value is a link that leads to the option of settling money out of the Lightning channels (screen on the left).

In the transaction list, I prioritize the display of the most useful information in the daily use of the wallet, such as the type of transaction —which can be filtered to search more efficiently, the amount, the date and the label. Detailed information would be available in a "transaction detail" page, accessed by clicking each transaction on the list.

![Request page](images/lightning-wireframes5.png)