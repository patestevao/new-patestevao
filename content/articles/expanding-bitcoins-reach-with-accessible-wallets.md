---
title: 'Expanding Bitcoin’s reach with accessible wallets'
slug: 'expanding-bitcoins-reach-with-accessible-wallets'
tags: ["ux", "bitcoin"]
date: '2019-09-20'
image: '/articles/expanding-bitcoins-reach-with-accessible-wallets/images/preview.jpeg'
socialimg: 'images/preview.jpeg'
featured: 'images/featured-image.jpeg'
intro: 'This article is an organized write-up of notes and insights collected
        during the on-going research we are doing on the subject of accessible
        wallets.'
---

Co-authored article with: Marco Agner.

This article is an organized write-up of notes and insights collected during
the on-going research we are doing on the subject of accessible wallets. Even
though there’s still much to be done, we wanted to share these first thoughts
since now.

There exists, already, a general awareness of the importance of creating
interfaces with good Usability for Bitcoin users. It’s a very straightforward
issue: if interfaces are hard to use — i.e. have a bad usability — people will
make more mistakes when operating the wallet. Mistakes in Bitcoin wallets can
manifest themselves as irreversible financial loss and privacy compromise. As a
consequence, there has been an effort by many different developing teams to
make their wallets more usable. But, usable to whom?

If Bitcoin’s goal is to be a revolution of the global financial system, it
needs to be available and accessible to people all around the world and,
potentially, to all of them. To make that possible, wallet developers need to
work with the need for accessibility in mind.

Throughout this article, we will present different types of disabilities and
special needs that may affect how people use the wallet software. The objective
is to create awareness over the range of distinct difficulties people may have
that should be considered when developing a solution. Also, we intend to show
the relevance of accessibility in terms of the number of people affected, and,
therefore, to give an idea of how many more people can make use of Bitcoin if
they have a proper interface designed for them.

## Who may not be your user (until now)

Here are some of the key information we have gathered so far that give a
dimension of how many potential users with special needs there are for us to
reach:

- 54,4% of the world population accesses the internet; [(1)](#data-sources)

- 1 in 7 people in the world experience some disability; [(2)](#data-sources)

- Color blindness (color vision deficiency, or CVD) affects approximately 1 in
12 men (8%) and 1 in 200 women in the world. [(3)](#data-sources)

- Brazil’s population is roughly 200 million people with 69% having access to
the internet and 7.2% people older than 15 years old being illiterate. [(4)](#data-sources) [(5)](#data-sources)

- An estimated 253 million people live with vision impairment: 36 million are
blind and 217 million have moderate to severe vision impairment. [(6)](#data-sources)

## The approaches for an accessible wallet

### Universal Design

> “Universal design is the design of products and environments to be usable by all people, to the greatest extent possible, without the need for adaptation or specialized design.” — Ron Mace

The idea behind Universal Design is that products can become accessible for a
great number of people, even some of those who have special needs or
disabilities, simply by leveraging the correct application of Design principles
or, in other words, by creating an objectively good design. The principles of
Universal Design clearly cross paths with the objectives for any interface that
desires to provide a good experience to its users. Let’s take a look at the
first six of those principles — the seventh belongs to the realm of the
meatspace — and consider how a good design approach is enough to address most
issues.


> Principle 1: Equitable Use
>
> The design is useful and marketable to people with diverse abilities.

Bitcoin wallets should be easy to use for both beginners and expert users. Provide the means for each user to make the most out of it. E.g.: offer tutorials and contextual help, provide advanced options (making it clear that they are advanced).

> Principle 2: Flexibility in Use
>
> The design accommodates a wide range of individual preferences and abilities.

People are very different in their personal needs. Your user might be
short-sighted, have short fingers, have a very large phone, be an elderly
person with difficulty of making precise moves, or even commuter on a very
shaky train that frequently uses the wallet app on his way to work. Examples of
how the wallet can account for this: offering different font sizes, considering
the effects of Fitt’s Law — the farther away a target is and the smaller its
size, the more difficult it is for the user to correctly land on the target —
on both desktop and mobile interfaces.

> Principle 3: Simple and Intuitive use
>
> Use of the design is easy to understand, regardless of the user’s experience,
> knowledge, language skills, or current concentration level.

This concerns every principle of good Usability, such as providing feedback,
eliminating unnecessary complexities, creating consistency throughout the
interface, arranging elements with a visual hierarchy that reflects their
importance, etc.

> Principle 4: Perceptible information
>
> The design communicates necessary information effectively to the user, regardless of ambient conditions or the user’s sensory abilities.

This concerns the need to communicate a message to the user, so your objective
needs to be making that message as clear and universal as possible. E.g.: use
combinations of text and visual information, make good use of contrast and
white space to improve readability.

> Principle 5: Tolerance for Error
>
> The design minimizes hazards and the adverse consequences of accidental or
> unintended actions.

Error forgiveness is one of the most essential elements of modern digital
interfaces. Can you imagine your life without “Ctrl + Z”? As such, good Design
also has a variety of principles that deal with this need: warnings, action
reversal (when possible), organization that avoid errors — such as isolating or
shielding possibly hazardous choices, flexible acceptance of inputs.

> Principle 6: Low Physical Effort
>
> The design can be used efficiently and comfortably and with a minimum of fatigue.

This might not seem very related to software, but it can be. Making users read
long texts with a very small font sure can be tiring. And, what about having to
copy by hand a Bitcoin address? That also causes some physical stress that all
users can benefit from not having to perform. That’s why is a best practice to
provide the options to copy/paste and to read the QR code.

The greatest benefit of Universal Design is that the application of these
principles on a Bitcoin wallet is perfectly achievable without the need for any
specialized knowledge and the results are a significant inclusion and improved
experience for different users. If we think of it, these simple measures can
improve usability for a wide range of people, such as elderly people, people
who are not proficient readers, children, people with mild visual difficulties,
novice users who are not perfectly comfortable with technology, or simply
anyone that encounters himself/herself in an imperfect environment for the use
of the wallet — e.g. under bright sun, on a shaky transport, etc.

### Accessible Design

Accessible design is the process in which the needs of people with disabilities
are specifically considered. The development of an accessible wallet through
this process may require knowledge of how people with the targeted disability
use software and a more strict set of participants during user tests, due to
the importance of getting feedback from the target audience. Therefore, this is
not always as easy to integrate into your development plan.

The creation of a wallet for the illiterate or semi-illiterate, for example,
requires that all main wallet communication be transformed into graphical
elements and sound. That requires an extra planning on which symbols and images
will better illustrate each action, as well as recording and implementing the
visual cues for the audio assistance.

However, there are some principles we can observe that similarly to the
Universal Design approach, can also be easy to implement or be of benefit to
most users. A few examples that can be listed:

- Include text alternatives to all non-text content, accounting for its
meaning. An example of that would be a text alternative for a search icon,
usually the magnifying glass, to be “search” rather than “magnifying glass”.
This will help users that depend on assistive technology like screen-readers.

- Don’t rely solely on color coding to convey a message or to differentiate
elements. This simple redundancy is enough not to exclude color-blind users
from your software. The image below shows an example of this in a mock up of a
Bitcoin wallet.

![article image](images/article-image.png)
*The screen on the left relies both on color and graphic elements to communicate
with the user, which is the correct approach. The screen on the right uses only
colors, making it a bad practice if we want to make the Design more accessible.*

- If animating, make sure users have enough time to read the content. And,
certainly, avoid presenting the content in a way that may cause seizures.

- Make your wallet possible to navigate using only the keyboard. This is
actually a feature that many programmers might like, due to the habit of using
command line interfaces that rarely need the mouse input.

These were just a few punctual examples, there are standards that guide the
design of accessible wallets which are a more complete source of information on
that matter.

## Our conclusion for now

As stated, this article just presents some preliminary insights from a bigger
research that we wanted to share now. Nevertheless, we already can take a
couple of important conclusions from the information we have analyzed until
now.

Making accessible wallets is not only for users with disabilities; the concept
of Universal Design is much broader and useful for all human users.
Nevertheless, knowing the numbers, we can see that polishing your software
specially to serve users with disabilities — or, at least, making it easier for
the software to interact with external accessibility tools — can have a huge
impact when compared to the investment in resources. And, this asymmetric
relationship we see here may mean that the resources directed toward
accessibility can be balanced to not overstretch a project while causing a
significant impact, especially if the main objective is making Bitcoin
meaningful for the world economy.

And, in case you are looking for an inspiration on how you can build a wallet
that has a distinct impact than the ones that exist so far, you can take the
challenge up to yourself and be the one that will go the extra mile to build a
specially-made software that suits a type disability.

##### Data sources:

1. [https://www.internetworldstats.com/stats.htm](https://www.internetworldstats.com/stats.htm)

2. [http://apps.who.int/iris/bitstream/handle/10665/199544/9789241509619_eng.pdf;jsessionid=68C20993733916C445F9EA4096E29316?sequence=1](http://apps.who.int/iris/bitstream/handle/10665/199544/9789241509619_eng.pdf;jsessionid=68C20993733916C445F9EA4096E29316?sequence=1)

3. [http://www.colourblindawareness.org/colour-blindness/](http://www.colourblindawareness.org/colour-blindness/)

4. [https://www.consumerbarometer.com/en/trending/?countryCode=BR&category=TRN-NOFILTER-ALL](https://www.consumerbarometer.com/en/trending/?countryCode=BR&category=TRN-NOFILTER-ALL)

5. [https://brasilemsintese.ibge.gov.br/educacao/taxa-de-analfabetismo-das-pessoas-de-15-anos-ou-mais.html](https://brasilemsintese.ibge.gov.br/educacao/taxa-de-analfabetismo-das-pessoas-de-15-anos-ou-mais.html)

6. [http://www.who.int/en/news-room/fact-sheets/detail/blindness-and-visual-impairment](http://www.who.int/en/news-room/fact-sheets/detail/blindness-and-visual-impairment)

##### Other sources:

- [http://universaldesign.ie/What-is-Universal-Design/](http://universaldesign.ie/What-is-Universal-Design/)

- [http://universaldesign.ie/what-is-universal-design/definition-and-overview/definition-and-overview.html](http://universaldesign.ie/what-is-universal-design/definition-and-overview/definition-and-overview.html)

- [http://universaldesign.ie/What-is-Universal-Design/The-7-Principles/](http://universaldesign.ie/What-is-Universal-Design/The-7-Principles/)

- [https://www.w3.org/WAI/fundamentals/accessibility-principles/](https://www.w3.org/WAI/fundamentals/accessibility-principles/)
