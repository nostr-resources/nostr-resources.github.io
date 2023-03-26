---
layout: resources
title: nostr Resources
image: /assets/images/cover.png
description: nostr is new and confusing but also really cool.
redirect_from: resources
---

**TL;DR:** nostr[^fn-nostr] is a protocol that has the power to replace twitter, Telegram, and other things.

[^fn-nostr]: nostr = Notes and Other Stuff Transmitted by Relays

---

<div class="action-buttons">
  <div class="button button-black button-medium">
    <a href="#get-started"><i class="fa-solid fa-rocket"></i> Get Started</a>
    <a href="#learn-more"><i class="fa-solid fa-book-open-reader"></i> Learn More</a>
  </div>
  <br/>
  <a href="#get-involved"><i class="fab fa-github"></i> Get Involved</a>
</div>

---

> WTF is nostr?
>
><cite>You, probably</cite>


nostr is new and confusing but also really cool. It is **the simplest open protocol that is able to create a
censorship-resistant global "social" network** once and for all.

- It doesn't rely on any trusted central server, hence it is resilient.
- It is based on cryptographic keys and signatures, so it is tamperproof.
- It does not rely on P2P techniques, therefore it works.

---

<center>
  <p><small><a href="#toc">↓ Table of Contents ↓</a></small></p>
</center>

---

# Get Started

While there are [many clients](#clients), the following three are currently quite popular: Damus for iOS, Amethyst for Android, and Iris for Web.

Download a suitable client:

<div class="action-buttons">
  <div class="button button-black">
    <a href="https://apps.apple.com/ca/app/damus/id1628663131" target="_blank"><i class="fa-brands fa-apple"></i> Damus</a>
    <a href="https://play.google.com/store/apps/details?id=com.vitorpamplona.amethyst" target="_blank"><i class="fa-brands fa-android"></i> Amethyst</a>
  </div>
  <br/>
  <a href="https://iris.to/" target="_blank"><i class="fa-solid fa-globe"></i> Iris</a>
</div>

---

Need help? Check out these guides:
- [Guide for Damus](https://nostr.how/guides/damus) (iOS)
- [Guide for Amethyst](https://nostr.how/guides/amethyst) (Android)
- [Guide for Iris](https://nostr.how/guides/iris) (Web)

Make sure to take care of your [key management](#keys)!

Not happy with the client choice above? Pick one of the [many other clients](#clients)!

---

# Learn More

nostr's design is very basic:

- There are two components: **clients** and **relays**. Each user runs a client. Anyone can run a relay.
- Every user is identified by a public key. Every post is signed. Every client validates these signatures.
- Clients fetch data from relays of their choice and publish data to other relays of their choice. A relay doesn't talk to another relay, only directly to users.

To use nostr, you need a [key](#keys) and a [client](#clients).

- Everybody runs a client. It can be a native client, a web client, etc. 
- To publish something, you write a post, sign it with your key and send it to multiple relays (servers hosted by someone else, or yourself). 
- To get updates from other people, you ask multiple relays if they know anything about these other people. 
- Anyone can run a relay. A relay is very simple and dumb. It does nothing besides accepting posts from some people and forwarding to others.
- Relays don't have to be trusted. Signatures are verified on the client side.

## Keys

Your keys are your identity. You can think of your public key (`npub...`) as
your username and your private key (`nsec...`) as your password. 

Two quick things:
- ⚠️ **DO NOT PASTE YOUR PRIVATE KEY INTO WEBSITES**[^fn-xss] ⚠️
- Store your keys securely and do not share your private key

Keys exist in two formats, `hex` and the above mentioned npub/nsec. You can use
a [key converter tool](https://github.com/rot13maxi/key-convertr)[^fn-keys] to
convert between the two formats.

[^fn-keys]: There's also the [damus.io/key](https://damus.io/key/) but DO NOT use it for private key conversions. Don't paste your private key into websites. Just don't.

[^fn-xss]: You have to trust whoever is running the website, obviously, and some clients are vulnerable to XSS attacks. A lot of people got rekt already, and had to re-build their nostr identity because of it.

Use [Alby](https://getalby.com) or [nos2x](https://github.com/fiatjaf/nos2x) to
generate your keys, or generate them using a dedicated tool like
[rana](https://github.com/grunch/rana) or
[nostrogen](https://hitony.com/nostrogen/). The aforementioned extensions will
store your keys safely (or at least more safely).

- [Nostr in the Alby Extension](https://blog.getalby.com/nostr-in-the-alby-extension/)
- [The nos2x browser extension and why you should use it](https://youtu.be/IoLw-3ok3_M)

You can also generate your keys by other means if you know what you're doing.[^bip85]
It's still early days, so be prepared to get rekt.

[^bip85]: [BIP-85](https://bip85.com/) is an option, for example.

## Clients

Periodically check [nostr.net](https://www.nostr.net/) which keeps a curated
list of clients or have a look at the [client comparison table](https://github.com/vishalxl/Nostr-Clients-Features-List). 

Here are some I like:

- [iris.to](https://iris.to/) - Clean interface & rich in features
- [snort.social](https://snort.social/) - Simple interface with automatic image-upload
- [yosup.app](https://yosup.app/) - Mobile-friendly and twitter-like
- [hamstr.to](https://hamstr.to/) - Twitter interface, multi-account support
- [nostrgram.co](https://nostrgram.co/) - Focus on images and media, supports multiple layout styles

Mobile clients:
- [Damus (iOS)](https://apps.apple.com/ca/app/damus/id1628663131) - Twitter-style iOS client, also works on MacOS[^fn-mac]
- [Amethyst (Android)](https://play.google.com/store/apps/details?id=com.vitorpamplona.amethyst) - Twitter-style Android client

On Android, you can also use the [Kiwi Browser](https://kiwibrowser.com/) which allows you to install Alby or nos2x, which in turn allows you to use any web client. [Yosup](https://yosup.app/) and [Hamstr](https://hamstr.to/) have good mobile experiences, for example.

There are more native clients in development, Nostros[^nostros] and Nozzle[^nozzle] being two of them.

[^nostros]: [KoalaSat/nostros](https://github.com/KoalaSat/nostros)
[^nozzle]: [kaiwolfram/Nozzle](https://github.com/kaiwolfram/Nozzle)
[^amethyst]: [vitorpamplona/amethyst](https://github.com/vitorpamplona/amethyst/)

There's also [Nostr Console](https://github.com/vishalxl/nostr_console),
[noscl](https://github.com/fiatjaf/noscl), and
[nostr-commander](https://github.com/8go/nostr-commander-rs) if you're into CLI
stuff.

[^fn-mac]: Apple Silicone only (M1 or M2 chip)

## Relays

Relays are dumb servers that you can leave behind at any time (so they can't
turn evil). You need to connect your client to a relay for it to work. There are
many relays & you can run your own.

- [nostr.watch](http://nostr.watch/)
- [nostr.info](https://nostr.info/relays/)

Run your own:

- [Set up a Nostr Relay server in under 5 minutes](https://andreneves.xyz/p/set-up-a-nostr-relay-server-in-under)[^fn-fork]

[^fn-fork]: Fork with small modifications/fixes: [Install a nostr relay](https://www.massmux.com/install-a-nostr-relay/)

## Tools

nostr can do more than just social media.

- [Sendstr](https://sendstr.com/) - shared clipboard between devices over nostr
- [nosbin](https://nosbin.com/) - pastebin over nostr


## Games

Games? WTF? Yes, games:

- [Jester](https://jesterui.github.io/) - Chess over nostr by theborakompanioni

---

## Pro Tips

Some things work a bit differently and aren't always obvious, such as:

- [Finding others](#finding-others)
- [Posting images](#posting-images)
- [Verifying yourself](#verifying-yourself)
- [Receiving Zaps](#receiving-zaps)

### Finding others

Use this search query to find nostr keys of people you follow on twitter:

- [🔎 "verifying my account on nostr" (ppl you follow)](https://twitter.com/search?q=%22verifying%20my%20account%20on%20nostr%22&f=live&pf=1)

This uses the [nostr.directory](https://www.nostr.directory/) verification
message, but the `&pf=1` limits the twitter search to only people you follow.

### Posting images

Most clients will display image URLs as images, so you can just upload any image
to image sharing sites and post the URL like this:

```
https://i.ibb.co/w4WvnYb/image.png
```

This also works for videos.

Here are some free image hosts:

- [nostr.build](https://nostr.build/)
- [imgbb.com](https://imgbb.com/)
- [imgur](https://imgur.com/)
- [postimages.org](https://postimages.org/)

You can also use your Twitter display picture by [following this guide](https://medium.com/@_Bosch_/how-to-use-your-twitter-display-picture-on-nostr-fd43c6a26257).

### Verifying yourself

If you have a domain and want to have a "verified" checkmark, here is some
useful info:

- [NVK's guide (using Github Pages)](https://nvk.org/n00b-nip5)
- [metasikander's guide (generic)](https://gist.github.com/metasikander/609a538e6a03b2f67e5c8de625baed3e)

### Receiving Zaps

Zaps are [V4V](https://value4value.info/) lightning payments that are broadcast
as nostr events, so that clients can display them on user profiles and specific
notes.

To receive zaps you need a lightning wallet that supports
[NIP-57](https://github.com/nostr-protocol/nips/blob/master/57.md). Two popular
custodial solutions are [Stacker News](https://stacker.news) and [Lightning Tip
Bot](https://ln.tips).

To use the latter in a more private way, you can:

1. Use [sms4sats](https://sms4sats.com/) to sign up to Telegram
2. Create an [LN.tips](https://ln.tips) wallet
3. Type `/nostr add <your_npub>` to add your npub
4. Type `/advanced` to see your anonymous lightning address...
5. ...and add it to your nostr profile. Done!

## Stats

Ever since [Jack](https://twitter.com/jack/status/1603945963944480768) joined
(and funded some nostr devs) and [Elon put it on his naughty
list](https://twitter.com/dergigi/status/1604548665196138499) a flood of people
came streaming in. Since everything is out in the open, you can see this nicely
in the stats.

- [nashboard.space](https://nashboard.space/)
- [nostr.io](https://nostr.io/stats)
- [nostr.band](https://nostr.band/stats.html)

## Sats

Some clients will render Lightning invoices natively, showing the recipient, 
amount, and a pay button. One such client is Damus, which shows a nice 
[little widget and a pay button](https://i.ibb.co/zhd4Fbs/damus-invoice-render.png).

## Search

Most clients support search, but there's also:

- [nostrview.com](https://nostrview.com) 
- [brb.io/search](https://brb.io/search)

You can also create a search bot at [sb.nostr.band](https://sb.nostr.band) and then follow it to receive new posts matching a keyword or hashtag right into your feed.

### Bots

- [How to build a nostr gm bot](https://dergigi.com/2023/01/19/how-to-build-a-nostr-gm-bot/) by [Gigi](https://www.nostr.guru/p/npub1dergggklka99wwrs92yz8wdjs952h2ux2ha2ed598ngwu9w7a6fsh9xzpc)
- [nostr_bot](https://docs.rs/nostr-bot/latest/nostr_bot/) Rust crate

### RSS

You can also create an RSS feed with posts matching some keywords at [rss.nostr.band](https://rss.nostr.band) and use your favorite RSS reader app to follow different nostr conversations.

## Pods

- [nostrovia](https://nostrovia.org/) - weekly roundup
- [BR018](https://bitcoin.review/podcast/episode-18/) - [jack](https://www.nostr.guru/p/npub1sg6plzptd64u62a878hep2kev88swjh3tw00gjsfl8f237lmu63q0uf63m), [fiatjaf](https://www.nostr.guru/p/npub180cvv07tjdrrgpa0j7j7tmnyl2yr6yr7l8j4s3evf6u64th6gkwsyjh6w6), and [jb55](https://www.nostr.guru/p/npub1xtscya34g58tk0z605fvr788k263gsu6cy9x0mhnm87echrgufzsevkk5s) talk nostr with [nvk](https://www.nostr.guru/p/npub1az9xj85cmxv8e9j9y80lvqp97crsqdu2fpu3srwthd99qfu9qsgstam8y8) ([transcript](https://archive.is/wip/Qoh4M), [archive](https://archive.is/wip/dkQj2))
- [Lightning Tidbits 769571](https://pod.link/1586346643/episode/33f509c2a1990640334b48739c59e31f) - [fiatjaf](https://www.nostr.guru/p/npub180cvv07tjdrrgpa0j7j7tmnyl2yr6yr7l8j4s3evf6u64th6gkwsyjh6w6) talks nostr with [André Neves](https://www.nostr.guru/p/npub1rvg76s0gz535txd9ypg2dfqv0x7a80ar6e096j3v343xdxyrt4ksmkxrck)
- [CD63 - building nostr](https://pod.link/1546393840/episode/112bd2a52d54e203ec0c11022b5aaf11), a censorship resistant alternative to twitter, with [fiatjaf](https://www.nostr.guru/p/npub180cvv07tjdrrgpa0j7j7tmnyl2yr6yr7l8j4s3evf6u64th6gkwsyjh6w6), [jb55](https://www.nostr.guru/p/npub1xtscya34g58tk0z605fvr788k263gsu6cy9x0mhnm87echrgufzsevkk5s), and [kukks](https://github.com/Kukks), hosted by [ODELL](https://www.nostr.guru/p/npub1qny3tkh0acurzla8x3zy4nhrjz5zd8l9sy9jys09umwng00manysew95gx) ([transcript](https://archive.is/wip/Qoh4M), [archive](https://archive.ph/Qoh4M))
- [BA691 - A Native Protocol for Social Media](https://pod.link/1359544516/episode/8e647d338c79265bed63dfb06dd71e7b) by [jack](https://www.nostr.guru/p/npub1sg6plzptd64u62a878hep2kev88swjh3tw00gjsfl8f237lmu63q0uf63m)
- [BTC111 - Decentralized Social Media & Bitcoin](https://www.theinvestorspodcast.com/bitcoin-fundamentals/nostr-decentralized-social-media-william-casarin/) with [jb55](https://www.nostr.guru/p/npub1xtscya34g58tk0z605fvr788k263gsu6cy9x0mhnm87echrgufzsevkk5s) hosted by [Preston Pysh](https://www.nostr.guru/p/npub1s5yq6wadwrxde4lhfs56gn64hwzuhnfa6r9mj476r5s4hkunzgzqrs6q7z) ([transcript](https://chowcollection.medium.com/preston-pysh-btc111-nostr-decentralized-social-media-bitcoin-w-william-casarin-352f6dedce46), [archive](https://archive.ph/uCSDQ))
- [What's new with Stacker.News and Nostr?](https://www.curiousdk.com/p/whats-new-with-stackernews-and-nostr) a conversation with Keyan Kousha and Max Webster ([transcript](https://chowcollection.medium.com/david-king-whats-new-with-stacker-news-e49e3256eddc), [archive](https://archive.is/wip/wGrb8))

## Explorers

- [nostr.guru](https://www.nostr.guru/)

---

## More info

- [nostr.how](https://nostr.how/) by [Jeff Gardner](https://nostr.guru/p/npub1zuuajd7u3sx8xu92yav9jwxpr839cs0kc3q6t56vd5u9q033xmhsk6c2uc)
- [nostr.net](https://www.nostr.net/) aka awesome-nostr by @aaaljaz
- [nostr-protocol/nostr](https://github.com/nostr-protocol/nostr) by fiatjaf

Articles and explainers:

- [What Is Nostr and How Do I Use It?](https://www.btctimes.com/news/what-is-nostr-and-how-do-i-use-it) by Walker V.
- [usenostr.org](https://usenostr.org/) by Pluja
- [What is Nostr, and how to start using Nostr](https://github.com/vishalxl/nostr_console/discussions/31) by Vishal
- [Nostr, an Introduction](https://wiki.wellorder.net/post/nostr-intro/) by Greg Heartsfield
- [Nostr Newcomers Most Common Questions and Answers](https://uselessshit.co/resources/nostr/) by pitiunited
- [Why Nostr Matters](https://blog.lopp.net/why-nostr-matters/) by Jameson Lopp

It's still very early days. 
There's known [privacy issues](https://consentonchain.github.io/blog/posts/nostr-privacy/) and other things. 

---

# Get Involved

nostr is an open protocol and most clients are open-source.
You are encouraged to report bugs and create pull requests!

nostr protocol:
- [NIPs](https://github.com/nostr-protocol/nips)

Clients:
- [Damus](https://github.com/damus-io/damus)
- [Amethyst](https://github.com/vitorpamplona/amethyst)
- [Iris](https://github.com/irislib/iris-messenger)

Check out [awesome-nostr](https://github.com/aljazceru/awesome-nostr) for links to other clients, libraries, relay implementations, and related projects to work on.

Also make sure to have a look at the various [nostr bounties](https://bountsr.org/) if you're in the mood to earn sats.

This site is open source too. If you can, please [improve this page](https://github.com/nostr-resources/nostr-resources.github.io). You can also create a [translation](#translations).

---

## Translations

- [Chinese translation](https://mp.weixin.qq.com/s/RoO-oOgGAXpcGyjD8IYBdw) by Cakksakkas
- [French translation](https://nostr.fr) by Marco.BTC.fr
- [Spanish translation](https://bitcoinnostr.com/recursos-de-nostr/) by [BitByBit](https://nostr.guru/p/npub1luhyzgce7qtcs6r6v00ryjxza8av8u4dzh3avg0zks38tjktnmxspxq903)
- [German translation](https://nostr-info.de) by [cercatrova](https://nostr.guru/p/npub1nxzp3zn90r44z07aeajc7wyah4fju49c9d3g45mxvmm64rmnrdusffch7m)
- [Italian translation](https://gist.github.com/theRescuer/717295270a35b4641081b6ef2cdf3025) by [avallanosterza](https://nostr.guru/p/npub1l0cwargp532n6x62pdcetkau783sxhpfhwu9d6qgpqm8r0mvt0eqqhlf2c)
- [Brazilian Portuguese translation](https://gist.github.com/fernandoporazzi/d1c47b4f2a1d2c1a2e0654a2a31668ff) por [fernandoporazzi](https://www.nostr.guru/p/npub1wh30wunfpkezx5s7edqu9g0s0raeetf5dgthzm0zw7sk8wqygmjqqfljgh)

Please [create a PR](https://github.com/nostr-resources/nostr-resources.github.io/pulls?q=is%3Apr+is%3Aclosed) to add your translation to the list above.

## About

This project evolved out of [a
gist](https://gist.github.com/dergigi/1ee8dc7e3da4b6572ed785ab24bc9907/revisions)
that was quite hastily put together. Its purpose was to help people wrap their heads
around nostr, and I guess this is the purpose still.

Some of the text above is copied from
[nostr-protocol/nostr](https://github.com/nostr-protocol/nostr) and
[nostr.net](https://www.nostr.net/). I just left some stuff out, so consider
the descriptions and explanations an opinionated summary.

If you found a typo, please [fix it](https://github.com/nostr-resources/nostr-resources.github.io/blob/master/index.md).
If you have suggestions, please [create an issue](https://github.com/nostr-resources/nostr-resources.github.io/issues).
If you want to scream at me because you think this whole thing is stupid, please [find me on nostr](https://www.nostr.guru/p/npub1dergggklka99wwrs92yz8wdjs952h2ux2ha2ed598ngwu9w7a6fsh9xzpc).

---
