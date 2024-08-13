---
layout: resources
title: nostr Resources
image: /assets/images/cover.png
description: nostr is new and confusing but also really cool.
redirect_from: resources
---

**TL;DR:** nostr[^fn-nostr] is a protocol that has the power to replace twitter,
Instagram, and all the other data silos that force various feeds down our
collective throats.

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

It is free as in freedom and puts the user in control.

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
  <a href="https://snort.social/" target="_blank"><i class="fa-solid fa-globe"></i> Snort</a> &nbsp; &middot; &nbsp;
  <a href="https://iris.to/" target="_blank"><i class="fa-solid fa-globe"></i> Iris</a> &nbsp; &middot; &nbsp;
  <a href="https://primal.net/" target="_blank"><i class="fa-solid fa-globe"></i> Primal</a> &nbsp; &middot; &nbsp;
  <a href="https://coracle.social/" target="_blank"><i class="fa-solid fa-globe"></i> Coracle</a>
</div>

---

Not happy with the client choice above? Pick one of the [many other clients](#clients)!

---

Need help? Check out these guides:

- [Guide for Damus](https://nostr.how/guides/damus) (iOS)
- [Guide for Amethyst](https://nostr.how/guides/amethyst) (Android)
- [Guide for Iris](https://nostr.how/guides/iris) (Web)

Make sure to take care of your [key management](#keys)!

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

Mobile clients:

- [Damus (iOS)](https://apps.apple.com/ca/app/damus/id1628663131) - Twitter-style iOS client, also works on MacOS[^fn-mac]
- [Amethyst (Android)](https://play.google.com/store/apps/details?id=com.vitorpamplona.amethyst) - Twitter-style Android client
- [Snort (Android)](https://play.google.com/store/apps/details?id=social.snort.app)
- [Nostur (iOS)](https://apps.apple.com/us/app/nostur/id1672780508) - native iOS/iPad client with MacOS[^fn-mac] version
- [Plebstr (iOS & Android)](https://play.google.com/store/apps/details?id=com.plebstr.client) - Good short message client similar to Twitter
- [Primal (iOS & Android)](https://primal.net/downloads) - Clean & performant, but not very feature-rich (yet)

There are more native clients in development, Nostros[^nostros] and Nozzle[^nozzle] being two of them.

[Nootti](https://nootti.com) is the first iOS native cross-posting client for Nostr, Bluesky and Mastodon.

Web clients:

- [primal.net](https://primal.net/) - Explore your tribe, network, and global trends
- [snort.social](https://snort.social/) - Simple interface with automatic image-upload
- [snort.deck](https://snort.social/deck) - A tweetdeck like version of the snort client.
- [noStrudel](https://nostrudel.ninja/) - Supports many NIPs inc communities, streams, blogs and more
- [coracle.social](https://coracle.social/) - Search, filters, and micro-apps
- [yosup.app](https://yosup.app/) - Mobile-friendly and twitter-like
- [iris.to](https://iris.to/) - Clean interface & rich in features
- [nostrgram.co](https://nostrgram.co/) - Focus on images and media, supports multiple layout styles

On Android you can use the [Kiwi Browser](https://kiwibrowser.com/) to use the
[Alby](https://getalby.com) or [nos2x](https://github.com/fiatjaf/nos2x)
extension, which allows you to use any web client.

[^nostros]: [KoalaSat/nostros](https://github.com/KoalaSat/nostros)
[^nozzle]: [dluvian/Nozzle](https://github.com/dluvian/Nozzle)

There's also [Nostr Console](https://github.com/vishalxl/nostr_console),
[noscl](https://github.com/fiatjaf/noscl), and
[nostr-commander](https://github.com/8go/nostr-commander-rs) if you're into CLI
stuff.

[^fn-mac]: Apple Silicone only (M1 or M2 chip)

Web clients for content creators:

- [ZapStream](https://zap.stream/) - Streaming on nostr allows for instant monetarisation of content.
- [Habla](https://habla.news/) and [yakihonne](https://yakihonne.com/) - Longform posts on nostr similar to Medium.
- [Stemstr](https://stemstr.app/) - Share your music with the world and let others collaborate.
- [Wavelake](https://www.wavlake.com/) - A music platform similar to Spotify.
- [Satellite.earth](https://satellite.earth/) - Focuses on moderated communities like reddit but also offers CDN media hosting and other nostr services.

Desktop clients:

- [Lume](https://lume.nu/) - Website
- [Gossip](https://github.com/mikedilger/gossip) - Github
- [Nostrid](https://github.com/lapulpeta/Nostrid) - Github
- [more-speech](https://github.com/unclebob/more-speech) - Github, a Nostr client in Clojure

## Relays

Relays are dumb servers that you can leave behind at any time (so they can't
turn evil). You need to connect your client to a relay for it to work. There are
many relays & you can run your own.

- [nostr.watch](http://nostr.watch/) - directory of paid and free relays
- [nostr.info](https://nostr.info/relays/) directory of known nostr relays
- [relay.tools](https://relay.tools/) - public relay browser

Run your own:

- [Set up a Nostr Relay server in under 5 minutes](https://andreneves.xyz/p/set-up-a-nostr-relay-server-in-under)[^fn-fork]

Paid relays:

- [relay.exchange](https://relay.exchange/)

Paid relays effectively deal with spam by charging users a small usage fee in
sats. You can set your global feed to paid relays only, which will get rid of
almost all spam.

[^fn-fork]: Fork with small modifications/fixes: [Install a nostr relay](https://www.massmux.com/install-a-nostr-relay/)

## Tools

Backing up your nostr keys AND your profile is as essential as backing up your private keys for Bitcoin!

- [Metadata Nostr](https://metadata.nostr.com/) - a profile and following list backup tool.
- [NostrSync](https://nostrsync.live/) - another service to backup profile AND nostr events.

nostr can do more than just social media.

- [Sendstr](https://sendstr.com/) - shared clipboard between devices over nostr.
- [nosbin](https://nosbin.com/) - pastebin over nostr.
- [Nostr.Cooking](https://nostr.cooking/) - create, explore or share recipes.
- [Badges](https://badges.page/) - create badges and award them to your friends or followers.
- [Emojis](https://emojis-iota.vercel.app/) - create or use emoji packs supported on most nostr clients.
- [ZapGoals](https://goals-silk.vercel.app/) - create zap goals for fund raisers or other events.
- [NsecBunker](https://nsecbunker.com/) - keep your nostr keys in a single place and provide fine-grained access to team members.

## Games

Games? WTF? Yes, games:

- [Jester](https://jesterui.github.io/) - Chess over nostr by theborakompanioni

---

## Tips & Tricks

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

Many popular clients support image uploads directly. (Keep in mind that all
uploaded images to external hosts are public, so don't upload confidential
things willy-nilly.)

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
- [nostrcheck.me](https://nostrcheck.me/public/)

You can also use your Twitter display picture by [following this guide](https://medium.com/@_Bosch_/how-to-use-your-twitter-display-picture-on-nostr-fd43c6a26257).

### Verifying yourself

If you have a domain and want to have a "verified" checkmark, here is some
useful info:

- [NVK's guide (using Github Pages)](https://nvk.org/n00b-nip5)
- [metasikander's guide (generic)](https://gist.github.com/metasikander/609a538e6a03b2f67e5c8de625baed3e)

There are also centralized verification services that you can use, but be aware
that all these are centralized and that they can rug-pull you at any moment:

{% for provider in site.data.nip05providers %}{% if provider.price %}{% continue %}{% endif %}
- [{{ provider.name }}]({{ provider.link }})
{% endfor %}

Paid services:

{% for provider in site.data.nip05providers %}{% unless provider.price %}{% continue %}{% endunless %}
- [{{ provider.name }}]({{ provider.link }}) ({{ provider.price }})
{% endfor %}

Provider missing? Price changed? \\
Please [create a PR](https://github.com/nostr-resources/nostr-resources.github.io/blob/master/_data/nip05providers.yml) or [open an issue](https://github.com/nostr-resources/nostr-resources.github.io/issues) to fix it!

### Receiving Zaps

Zaps are [V4V](https://value4value.info/) lightning payments that are broadcast
as nostr events, so that clients can display them on user profiles and specific
notes.

To receive zaps you need a lightning wallet that supports
[NIP-57](https://github.com/nostr-protocol/nips/blob/master/57.md).

Popular custodial solutions are:

- [Wallet of Satoshi](https://walletofsatoshi.com/) - recommended for mobile
- [Alby](https://getalby.com/) - recommended for desktop as browser extention 
- [Stacker News](https://stacker.news)
- [Lightning Tip Bot](https://ln.tips)

Self-custodial solutions:
- [Mutiny Wallet](https://www.mutinywallet.com/)
- [Zeus](https://zeusln.app/)

To use Lightning Tip Bot in a more private way, you can:

1. Use [sms4sats](https://sms4sats.com/) to sign up to Telegram
2. Create an [LN.tips](https://ln.tips) wallet
3. Type `/nostr add <your_npub>` to add your npub
4. Type `/advanced` to see your anonymous lightning address...
5. ...and add it to your nostr profile. Done!

### Mentions & Deep Links

You can mention a note or a user by putting an "@" before an _npub_ or _note_ like this:

- `@npub1dergggklka99wwrs92yz8wdjs952h2ux2ha2ed598ngwu9w7a6fsh9xzpc`
- `@note1m2ev3e2ma7a84rr8053qhsggeg6apmp00445v8k7tyeqvhu5u8aqpc30sp`

When mentioning a note in another note, the note will be shown as a quote-note.[^fn-quotenote]

Most clients support the `nostr:` URL scheme as defined in
[NIP-21](https://github.com/nostr-protocol/nips/blob/master/21.md), which means
you can link to your nostr profile by putting "nostr:" in front of your npub.
This will result in a link that opens in the user's nostr client, like
so: [open my nostr
profile](nostr:npub1dergggklka99wwrs92yz8wdjs952h2ux2ha2ed598ngwu9w7a6fsh9xzpc).

You can use this for http redirects too, which can be used as a way to verify your nostr profile if you own a domain, like so: [dergigi.com/npub](https://dergigi.com/npub)

There is even a [redirect tool](https://nostredirect.davidcoen.it/) that you can use; h/t to [David](nostr:npub149mp2m0q8prpdys7x2lusv2vceraxwzr4ajf6tv3l24my3gtszxsncas0t) for putting it together.

[^fn-quotenote]: How's that for a tongue twister?

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

- [nostr.band](https://nostr.band/)
- [nostrview.com](https://nostrview.com)
- [nos.today](https://nos.today)

You can also create a search bot at [sb.nostr.band](https://sb.nostr.band) and then follow it to receive new posts matching a keyword or hashtag right into your feed.

### Bots

- [How to build a nostr gm bot](https://dergigi.com/2023/01/19/how-to-build-a-nostr-gm-bot/) by [Gigi](nostr:npub1dergggklka99wwrs92yz8wdjs952h2ux2ha2ed598ngwu9w7a6fsh9xzpc)
- [nostr_bot](https://docs.rs/nostr-bot/latest/nostr_bot/) Rust crate
- [nostr GPT bot](https://github.com/Marfusios/nostr-client/tree/master/apps/nostr-bot) A GPT 3.5 bot for nostr.

### RSS

You can also create an RSS feed with posts matching some keywords at [rss.nostr.band](https://rss.nostr.band) and use your favorite RSS reader app to follow different nostr conversations.

## Podcasts

- [nostrovia](https://nostrovia.org/) - weekly nostr news roundup
- [La Cosa Nostr](https://cast.bitcoiner.social/@lacosanostr/about) - interviews with relay operators and builders
- [Nostr Talks](https://www.curiousdk.com/podcast) - Nostr related news and interviews
- [Thank God For Nostr](https://tgfb.com/podcasts/thank-god-for-nostr/) - nostr from the Christian perspective

Episodes:

- [BR018](https://bitcoin.review/podcast/episode-18/) - [jack](nostr:npub1sg6plzptd64u62a878hep2kev88swjh3tw00gjsfl8f237lmu63q0uf63m), [fiatjaf](nostr:npub180cvv07tjdrrgpa0j7j7tmnyl2yr6yr7l8j4s3evf6u64th6gkwsyjh6w6), and [jb55](nostr:npub1xtscya34g58tk0z605fvr788k263gsu6cy9x0mhnm87echrgufzsevkk5s) talk nostr with [nvk](nostr:npub1az9xj85cmxv8e9j9y80lvqp97crsqdu2fpu3srwthd99qfu9qsgstam8y8) ([transcript](https://archive.is/wip/Qoh4M), [archive](https://archive.is/wip/dkQj2))
- [Lightning Tidbits 769571](https://pod.link/1586346643/episode/33f509c2a1990640334b48739c59e31f) - [fiatjaf](nostr:npub180cvv07tjdrrgpa0j7j7tmnyl2yr6yr7l8j4s3evf6u64th6gkwsyjh6w6) talks nostr with [André Neves](nostr:npub1rvg76s0gz535txd9ypg2dfqv0x7a80ar6e096j3v343xdxyrt4ksmkxrck)
- [CD63 - building nostr](https://pod.link/1546393840/episode/112bd2a52d54e203ec0c11022b5aaf11), a censorship resistant alternative to twitter, with [fiatjaf](nostr:npub180cvv07tjdrrgpa0j7j7tmnyl2yr6yr7l8j4s3evf6u64th6gkwsyjh6w6), [jb55](nostr:npub1xtscya34g58tk0z605fvr788k263gsu6cy9x0mhnm87echrgufzsevkk5s), and [kukks](https://github.com/Kukks), hosted by [ODELL](nostr:npub1qny3tkh0acurzla8x3zy4nhrjz5zd8l9sy9jys09umwng00manysew95gx) ([transcript](https://archive.is/wip/Qoh4M), [archive](https://archive.ph/Qoh4M))
- [BA691 - A Native Protocol for Social Media](https://pod.link/1359544516/episode/8e647d338c79265bed63dfb06dd71e7b) by [jack](nostr:npub1sg6plzptd64u62a878hep2kev88swjh3tw00gjsfl8f237lmu63q0uf63m)
- [BTC111 - Decentralized Social Media & Bitcoin](https://www.theinvestorspodcast.com/bitcoin-fundamentals/nostr-decentralized-social-media-william-casarin/) with [jb55](nostr:npub1xtscya34g58tk0z605fvr788k263gsu6cy9x0mhnm87echrgufzsevkk5s) hosted by [Preston Pysh](nostr:npub1s5yq6wadwrxde4lhfs56gn64hwzuhnfa6r9mj476r5s4hkunzgzqrs6q7z) ([transcript](https://chowcollection.medium.com/preston-pysh-btc111-nostr-decentralized-social-media-bitcoin-w-william-casarin-352f6dedce46), [archive](https://archive.ph/uCSDQ))
- [What's new with Stacker.News and Nostr?](https://www.curiousdk.com/p/whats-new-with-stackernews-and-nostr) a conversation with Keyan Kousha and Max Webster ([transcript](https://chowcollection.medium.com/david-king-whats-new-with-stacker-news-e49e3256eddc), [archive](https://archive.is/wip/wGrb8))

## Explorers

- [nostr.guru](https://www.nostr.guru/)

---

## Privacy

There are multiple [privacy issues](https://consentonchain.github.io/blog/posts/nostr-privacy/) when it
comes to using nostr.

Your IP address is exposed to the relays you connect to, so consider using a VPN
or similar. Some clients also support connecting via Tor.
Tor nostr relays exist, but not all clients support Tor nostr relays.

Relays also know which public keys you are requesting, meaning your public key
will be tied to your IP address.

### Privacy & Image Uploads

Some third party media hosters may be able to see, and share your IP address.

### Privacy & Direct Messages

Only the message content is encrypted on Nostr: the sender, recipient and timestamp are visible to everyone.

---

## More info

- [nostr.how](https://nostr.how/) by [Jeff G.](nostr:npub1zuuajd7u3sx8xu92yav9jwxpr839cs0kc3q6t56vd5u9q033xmhsk6c2uc)
- [heynostr.com](https://www.heynostr.com/) by [Karnage](nostr:npub1r0rs5q2gk0e3dk3nlc7gnu378ec6cnlenqp8a3cjhyzu6f8k5sgs4sq9ac)
- [usenostr.org](https://usenostr.org/) by [Pluja](nostr:npub1jh4qu2g5e49syrwh293q8q90xeklvdx47pnj5vyca2tkljed08us0ctj6k)
- [nostr.net](https://www.nostr.net/) aka awesome-nostr by [Aljaz](nostr:npub1aljazgxlpnpfp7n5sunlk3dvfp72456x6nezjw4sd850q879rxqsthg9jp)
- [nostr-protocol/nostr](https://github.com/nostr-protocol/nostr) by [fiatjaf](nostr:npub180cvv07tjdrrgpa0j7j7tmnyl2yr6yr7l8j4s3evf6u64th6gkwsyjh6w6)

Articles and explainers:

- [The Power of Nostr: Decentralized Social Media and More](https://www.lynalden.com/the-power-of-nostr/) by [Lyn Alden](nostr:npub1a2cww4kn9wqte4ry70vyfwqyqvpswksna27rtxd8vty6c74era8sdcw83a)
- [Implications of Open Monetary and Information Networks](https://www.lynalden.com/open-networks/) by [Lyn Alden](nostr:npub1a2cww4kn9wqte4ry70vyfwqyqvpswksna27rtxd8vty6c74era8sdcw83a)
- [What Is Nostr and How Do I Use It?](https://www.btctimes.com/news/what-is-nostr-and-how-do-i-use-it) by [Walker V.](nostr:npub1cj8znuztfqkvq89pl8hceph0svvvqk0qay6nydgk9uyq7fhpfsgsqwrz4u)
- [What is Nostr, and how to start using Nostr](https://github.com/vishalxl/nostr_console/discussions/31) by Vishal
- [Welcome to Nostr](http://lnshort.it/nostr-welcome/) by [Tony](nostr:npub10awzknjg5r5lajnr53438ndcyjylgqsrnrtq5grs495v42qc6awsj45ys7)
- [Nostr, an Introduction](https://wiki.wellorder.net/post/nostr-intro/) by Greg Heartsfield
- [Nostr Newcomers Most Common Questions and Answers](https://uselessshit.co/resources/nostr/) by pitiunited
- [Why Nostr Matters](https://blog.lopp.net/why-nostr-matters/) by Jameson Lopp

Videos:

- [How To Use NOSTR](https://youtu.be/qn-Zp491t4Y) by [BTC Sessions](nostr:npub1rxysxnjkhrmqd3ey73dp9n5y5yvyzcs64acc9g0k2epcpwwyya4spvhnp8)
- [Social Media is broken. Can we fix it?](https://youtu.be/aA-jiiepOrE) by [Max DeMarco](nostr:npub1lelkh3hhxw9hdwlcpk6q9t0xt9f7yze0y0nxazvzqjmre3p98x3sthkvyz)

For more videos have a look at [nostrvision.com](https://www.nostrvision.com/).

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

There is also [NostrDesign](https://nostrdesign.org/), a great resource for developers and UIX design for nostr. 

Also make sure to have a look at the various [nostr bounties](https://bountsr.org/) if you're in the mood to earn sats.

This site is open source too. If you can, please [improve this page](https://github.com/nostr-resources/nostr-resources.github.io). You can also create a [translation](#translations).

---

## Translations

- [Chinese translation](https://mp.weixin.qq.com/s/RoO-oOgGAXpcGyjD8IYBdw) by Cakksakkas
- [French translation](https://nostr.fr) by Marco.BTC.fr
- [Spanish translation](https://bitcoinnostr.com/recursos-de-nostr/) by [BitByBit](nostr:npub1luhyzgce7qtcs6r6v00ryjxza8av8u4dzh3avg0zks38tjktnmxspxq903)
- [German translation](https://nostr-info.de) by [cercatrova](nostr:npub1nxzp3zn90r44z07aeajc7wyah4fju49c9d3g45mxvmm64rmnrdusffch7m)
- [Italian translation](https://gist.github.com/theRescuer/717295270a35b4641081b6ef2cdf3025) by [avallanosterza](nostr:npub1l0cwargp532n6x62pdcetkau783sxhpfhwu9d6qgpqm8r0mvt0eqqhlf2c)
- [Brazilian Portuguese translation](https://gist.github.com/fernandoporazzi/d1c47b4f2a1d2c1a2e0654a2a31668ff) por [fernandoporazzi](nostr:npub1wh30wunfpkezx5s7edqu9g0s0raeetf5dgthzm0zw7sk8wqygmjqqfljgh)

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
If you want to scream at me because you think this whole thing is stupid, please [find me on nostr](nostr:npub1dergggklka99wwrs92yz8wdjs952h2ux2ha2ed598ngwu9w7a6fsh9xzpc).

---
