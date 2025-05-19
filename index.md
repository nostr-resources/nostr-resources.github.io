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

```
LOOKING FOR MAINTAINERS

This site could be way better (and up-to-date) than it is. If you're interested in maintaining it, please reach out to me by leaving a comment in the "Looking for Maintainers" issues on GitHub. More info in the footnote at the very end.

Thank you.
```

> What is nostr?
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

While there are [many clients](#clients), the following three are currently
quite popular: Damus for iOS, Amethyst for Android, and noStrudel for Web.
Primal is often recommended too, as it works on all platforms.

Download a suitable client:

<div class="action-buttons">
  <div class="button button-black">
    <a href="https://apps.apple.com/ca/app/damus/id1628663131" target="_blank"><i class="fa-brands fa-apple"></i> Damus</a>
    <a href="https://play.google.com/store/apps/details?id=com.vitorpamplona.amethyst" target="_blank"><i class="fa-brands fa-android"></i> Amethyst</a>
  </div>
  <br/>
  <a href="https://nostrudel.ninja" target="_blank"><i class="fa-solid fa-globe"></i> noStrudel</a> &nbsp; &middot; &nbsp;
  <a href="https://primal.net/" target="_blank"><i class="fa-solid fa-globe"></i> Primal</a> &nbsp; &middot; &nbsp;
  <a href="https://coracle.social/" target="_blank"><i class="fa-solid fa-globe"></i> Coracle</a> &nbsp; &middot; &nbsp;
  <a href="https://snort.social/" target="_blank"><i class="fa-solid fa-globe"></i> Snort</a> &nbsp; &middot; &nbsp;
  <a href="https://iris.to/" target="_blank"><i class="fa-solid fa-globe"></i> Iris</a>
</div>

---

# FAQ

**What's the easiest way to create a profile?**  
🦚 Going to [nstart.me](https://nstart.me/) is probably easiest. There is also [nosta.me](https://nosta.me/)

**What is the best nostr client?**  
🦚 There is no best. You'll have to [pick a client](#clients) according to your
tastes!

**What is the second best nostr client?**  
🦚 This question is best answered by watching [this video](https://youtu.be/uDgnZn3SjLw).

**Is nostr just a twitter clone?**  
🦚 No, it's way more than that. I'd suggest you browse
[nostrapps.com](https://nostrapps.com/) and try one of the more adventurous apps
yourself!

**Where do I store my "nsec" aka private key?**  
🦚 Make sure read the [key management](#keys) section!

**What is an "npub"?**  
🦚 Your "npub", or nostr public key, is your public identity. It is unique to
you and can be used to look up your profile and initiate a connection with you,
either via a follow, a DM, or a zap.

**What are zaps?**  
🦚 Zaps are nostr's way of seamlessly transferring value between users. They are
neither "tips" nor "expensive likes," but a new way of expressing value and
counterfeit-resistant engagement. They are [sat-based][br] tokens of appreciation with
perfect scarcity. They are, as one nostrich so beautifully put it, a way to say:
[keep doing you][kdy]. Zaps are flowing through the system at all times, as you
can clearly see via [zaplife.lol](https://zaplife.lol).

[br]: https://bitcoin-resources.com/
[kdy]: https://coracle.social/nevent1qqs2f66rxmq5xdcpfc4mdzded083zse8qy2mnqkayyvtzruknqmuf3gzyphydppzm7m554ecwq4gsgaek2qk32atse2l4t9ks57dpms4mmhfxaaw0q4

**How do I set up my client properly?**  
🦚 Check out these guides:

- [Guide for Damus](https://nostr.how/guides/damus) (iOS)
- [Guide for Amethyst](https://nostr.how/guides/amethyst) (Android)
- [Guide for Iris](https://nostr.how/guides/iris) (Web)

**What are relays, and how do I find them?**  
🦚 Read the [relays](#relays) section.

**Are all nostr apps available on the App Store?**  
🦚 They are not. The existing monopolies are threatened by nostr and what it
represents. But fear not, we will build our own app stores. We have one on
Android already: [Zapstore](https://zapstore.dev/download/), an app store built on
nostr.

**Where do I find alternatives to existing stuff?**  
🦚 Have a look at [noalt.app](http://noalt.app/)

**How do I find people to follow?**  
🦚 Use various [search](#search) tools, look up [trending
people](https://nostr.band/?trending=people), or check out [Following._](https://following.space/) for convenient, user-curated packs of suggested follows.
You can follow topical hashtags like
[#introductions](https://nostr.band/?q=%23introductions), too. Yes, on nostr you can
follow hashtags. You can also visit [Npub.world](https://npub.world/) to search for 
a specific person.

**How do I find my twitter friends?**  
🦚 This is explained in the "[finding others](#finding-others)" section.

**I have more questions. Who can help me?**  
🦚 Consult this [external FAQ](https://uselessshit.co/resources/nostr/),
[swarmstr](https://swarmstr.com/), or the
[#asknostr](https://nostr.band/?q=%23asknostr) hashtag.

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

If you're on Android, it is recommended to use a native signer like [Amber].

[Amber]: https://github.com/greenart7c3/Amber?tab=readme-ov-file#download-and-install

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
- [Openvibe (iOS & Android)](https://play.google.com/store/apps/details?id=com.plebstr.client) - Nostr, Threads, Bluesky, and Mastodon in one client.
- [Primal (iOS & Android)](https://primal.net/downloads) - Clean & performant, but not very feature-rich (yet)

There are more native clients in development, Nostros[^nostros] and Voyage[^voyage] being two of them.

[Nootti](https://nootti.com) is the first iOS native cross-posting client for Nostr, Bluesky and Mastodon. [Nos](https://nos.social/) is another iOS client that integrates with other social protocols.

Web clients:

- [primal.net](https://primal.net/) - Explore your tribe, network, and global trends
- [snort.social](https://snort.social/) - Simple interface with automatic image-upload
- [snort.deck](https://snort.social/deck) - A tweetdeck like version of the snort client.
- [noStrudel](https://nostrudel.ninja/) - Supports many NIPs inc communities, streams, blogs and more
- [coracle.social](https://coracle.social/) - Search, filters, and micro-apps
- [jumble](https://jumble.social/]) - Explore content feeds by relay and create custom relay sets
- [iris.to](https://iris.to/) - Clean interface & rich in features

On Android you can use the [Kiwi Browser](https://kiwibrowser.com/) to use the
[Alby](https://getalby.com) or [nos2x](https://github.com/fiatjaf/nos2x)
extension, which allows you to use any web client.

[^nostros]: [KoalaSat/nostros](https://github.com/KoalaSat/nostros)
[^voyage]: [dluvian/Voyage](https://github.com/dluvian/voyage)

There's also [Nostr Console](https://github.com/vishalxl/nostr_console),
[algia](https://github.com/mattn/algia), and
[nostr-commander](https://github.com/8go/nostr-commander-rs) if you're into CLI
stuff.

[^fn-mac]: Apple Silicone only (M1 or M2 chip)

Web clients for content creators:

- [ZapStream](https://zap.stream/) - Streaming on nostr allows for instant monetarisation of content.
- [Habla](https://habla.news/) and [yakihonne](https://yakihonne.com/) - Long-form posts on nostr similar to Medium.
- [Highlighter](https://highlighter.com/) - Client focused on reading and highlighting long-form content.
- [Shipyard](https://shipyard.pub/) - Write, schedule, and boost your notes.
- [Wavlake](https://www.wavlake.com/) - A music platform similar to Spotify.
- [Satellite.earth](https://satellite.earth/) - Focuses on moderated communities like reddit but also offers CDN media hosting and other nostr services.
- [Npub.pro](https://npub.pro/) - Nostr-based websites to show case creator content.

Desktop clients:

- [Lume](https://lume.nu/) - Website
- [Gossip](https://github.com/mikedilger/gossip) - Github
- [Notedeck by Damus]([https://damus.io/notedeck/]) - Website
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

Paid relays effectively deal with spam by charging users a small usage fee in
sats. You can set your global feed to paid relays only, which will get rid of
almost all spam.

[^fn-fork]: Fork with small modifications/fixes: [Install a nostr relay](https://www.massmux.com/install-a-nostr-relay/)

## Tools

Managing your nostr keys AND your profile is as essential as backing up your private keys for Bitcoin!

- [Nostr Metadata](https://metadata.nostr.com/) - a profile and following list backup tool.
- [NostrSync](https://nostrsync.vercel.app/) - another service to backup profile AND nostr events.
- [Nostr Follows](https://follows.nostr.com/) - recover lost contacts/follows.
- [Nostr Delete](https://delete.nostr.com/) - request to delete any nostr event from its hosting relays.

nostr can do more than just social media.

- [Listr](https://listr.lol/) - create and manage lists to use in supporting nostr apps.
- [nosbin](https://nosbin.com/) - pastebin over nostr.
- [Zap.Cooking](https://zap.cooking/) - create, explore or share recipes.
- [Badges](https://badges.page/) - create badges and award them to your friends or followers.
- [Emojis](https://emojito.meme/) - create or use emoji packs supported on most nostr clients.
- [Pinja](https://www.pinja.in/) - pin urls as bookmarks.
- [Lantern](https://chromewebstore.google.com/detail/lantern/jjoijlenmgefkaeiomoaelcljfibpcgh) - highlight, annotate, and discuss anything on the web.
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

[Blossom](https://github.com/hzrd149/blossom) uses nostr to decentralizse media hosting. If your favorite social client offers blossom support, check out
[blossomservers.com](https://blossomservers.com/) to find a list of rated and reviewed blossom servers.

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

- [Wallet of Satoshi](https://walletofsatoshi.com/) - recommended for mobile (not available everywhere)
- [Coinos](https://coinos.io/) - a web wallet with Nostr Wallet Connect capabilities
- [Primal](https://primal.net/home) - nostr client with built-in Bitcoin wallet for iOS, Android, and web

The Cashu protocol is bringing bitcoin-backed ecash to custodial Nostr zaps and beyond. It is still quite new (aka experimental). You can read more about it [here](https://cashu.space/). A couple of nice wallets to try are:

- [Minibits](https://www.minibits.cash/) - Android native
- [Cashu.me](https://wallet.cashu.me/welcome) - PWA for iOS and Android

You can find ecash mints and read reviews at [bitcoinmints.com](https://bitcoinmints.com/?tab=mints).

Self-custodial solutions:
- [Zeus](https://zeusln.app/)
- [Alby Hub](https://blog.getalby.com/what-is-alby-hub/)

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

Some DVMs, like [Noogle](https://noogle.lol/), have search capabilities, as well.

### Bots

- [How to build a nostr gm bot](https://dergigi.com/2023/01/19/how-to-build-a-nostr-gm-bot/) by [Gigi](nostr:npub1dergggklka99wwrs92yz8wdjs952h2ux2ha2ed598ngwu9w7a6fsh9xzpc)
- [nostr_bot](https://docs.rs/nostr-bot/latest/nostr_bot/) Rust crate
- [nostr GPT bot](https://github.com/Marfusios/nostr-client/tree/master/apps/nostr-bot) A GPT 3.5 bot for nostr.

### RSS

You can also create an RSS feed on nostr by following [this guide](https://habla.news/a/naddr1qvzqqqr4gupzp89qh469qapddgsrr8qw84xx08y7q34fm3cw3m64c2g9ufq9ydqtqyghwumn8ghj7mn0wd68ytnhd9hx2tcqzpkngat8w4nhzve3ve6k2d3hvyus88uu4f) .
[Narr](https://github.com/fiatjaf/narr) is a self-hosted nostr and RSS reader.
[Feeder](https://github.com/spacecowboy/Feeder/) has added support for nostr feeds in their reader.
There is [Noflux](https://github.com/fiatjaf/noflux) too.

## Podcasts

- [nostrovia](https://nostrovia.org/) - weekly nostr news roundup
- [La Cosa Nostr](https://tunein.com/podcasts/Technology-Podcasts/La-Cosa-Nostr---The-Decentralized-Network-p3709902/?topicId=355452728) - interviews with relay operators and builders
- [Nostr Talks](https://www.curiousdk.com/podcast) - Nostr related news and interviews
- [Thank God For Nostr](https://tgfb.com/podcasts/thank-god-for-nostr/) - nostr from a Christian perspective
- [No Solutions](https://fountain.fm/show/1jdehAGo1tgBdKZXIo8K) - No solutions; only trade-offs. Walking towards a better internet.
- [Nostr Rising](https://bitcoin.review/nostr/) - a [Bitcoin.Review](https://bitcoin.review/) series
- [No Strings](https://nostrings.show/) -  episodes for those just learning about nostr and episodes for experts who want to stay updated
- [Bitcoin And...](https://fountain.fm/show/eK5XaSb3UaLRavU3lYrI) - It's the news you can use
- [Plebchain Radio](https://fountain.fm/show/0N6GGdZuYNNG7ysagCg9) - weekly live audio show made for plebs, by plebs

Episodes:

- [BR018](https://bitcoin.review/podcast/episode-18/) - [jack](nostr:npub1sg6plzptd64u62a878hep2kev88swjh3tw00gjsfl8f237lmu63q0uf63m), [fiatjaf](nostr:npub180cvv07tjdrrgpa0j7j7tmnyl2yr6yr7l8j4s3evf6u64th6gkwsyjh6w6), and [jb55](nostr:npub1xtscya34g58tk0z605fvr788k263gsu6cy9x0mhnm87echrgufzsevkk5s) talk nostr with [nvk](nostr:npub1az9xj85cmxv8e9j9y80lvqp97crsqdu2fpu3srwthd99qfu9qsgstam8y8) ([transcript](https://archive.is/wip/Qoh4M), [archive](https://archive.is/wip/dkQj2))
- [Lightning Tidbits 769571](https://pod.link/1586346643/episode/33f509c2a1990640334b48739c59e31f) - [fiatjaf](nostr:npub180cvv07tjdrrgpa0j7j7tmnyl2yr6yr7l8j4s3evf6u64th6gkwsyjh6w6) talks nostr with [André Neves](nostr:npub1rvg76s0gz535txd9ypg2dfqv0x7a80ar6e096j3v343xdxyrt4ksmkxrck)
- [CD63 - building nostr](https://pod.link/1546393840/episode/112bd2a52d54e203ec0c11022b5aaf11), a censorship resistant alternative to twitter, with [fiatjaf](nostr:npub180cvv07tjdrrgpa0j7j7tmnyl2yr6yr7l8j4s3evf6u64th6gkwsyjh6w6), [jb55](nostr:npub1xtscya34g58tk0z605fvr788k263gsu6cy9x0mhnm87echrgufzsevkk5s), and [kukks](https://github.com/Kukks), hosted by [ODELL](nostr:npub1qny3tkh0acurzla8x3zy4nhrjz5zd8l9sy9jys09umwng00manysew95gx) ([transcript](https://archive.is/wip/Qoh4M), [archive](https://archive.ph/Qoh4M))
- [BA691 - A Native Protocol for Social Media](https://pod.link/1359544516/episode/8e647d338c79265bed63dfb06dd71e7b) by [jack](nostr:npub1sg6plzptd64u62a878hep2kev88swjh3tw00gjsfl8f237lmu63q0uf63m)
- [BTC111 - Decentralized Social Media & Bitcoin](https://www.theinvestorspodcast.com/bitcoin-fundamentals/nostr-decentralized-social-media-william-casarin/) with [jb55](nostr:npub1xtscya34g58tk0z605fvr788k263gsu6cy9x0mhnm87echrgufzsevkk5s) hosted by [Preston Pysh](nostr:npub1s5yq6wadwrxde4lhfs56gn64hwzuhnfa6r9mj476r5s4hkunzgzqrs6q7z) ([transcript](https://chowcollection.medium.com/preston-pysh-btc111-nostr-decentralized-social-media-bitcoin-w-william-casarin-352f6dedce46), [archive](https://archive.ph/uCSDQ))
- [What's new with Stacker.News and Nostr?](https://www.curiousdk.com/p/whats-new-with-stackernews-and-nostr) a conversation with Keyan Kousha and Max Webster ([transcript](https://chowcollection.medium.com/david-king-whats-new-with-stacker-news-e49e3256eddc), [archive](https://archive.is/wip/wGrb8))
- [BAChat-83 - Decentralizing Global Markets with Nostr](https://play.pocketcasts.com/podcasts/d44c81b0-10eb-0136-c266-7d73a919276a/7f0a34a8-e0b3-4c13-8538-a9a863c644ce), with [PABLOF7z](nostr:npub1l2vyh47mk2p0qlsku7hg0vn29faehy9hy34ygaclpn66ukqp3afqutajft) ([archive](https://archive.is/C3xHd))
- [The pro-hashed podcast, episode 22](https://youtu.be/wiDNJPKWRmQ), a conversation between [Constant](nostr:npub1t6jxfqz9hv0lygn9thwndekuahwyxkgvycyscjrtauuw73gd5k7sqvksrw) and [fiatjaf](nostr:npub180cvv07tjdrrgpa0j7j7tmnyl2yr6yr7l8j4s3evf6u64th6gkwsyjh6w6) 

## Explorers

[Nostr Gateway](https://github.com/fiatjaf/nostr-gateway?tab=readme-ov-file)

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

Only the message content is encrypted on Nostr: the sender, recipient and timestamp are visible to everyone. There are a few approaches currently underway to improve this. To best understand how your direct messages are handled, check with your favorite message client developer.

---

## More info

- [nostr.how](https://nostr.how/) by [Jeff G.](nostr:npub1zuuajd7u3sx8xu92yav9jwxpr839cs0kc3q6t56vd5u9q033xmhsk6c2uc)
- [usenostr.org](https://usenostr.org/) by [Pluja](nostr:npub1jh4qu2g5e49syrwh293q8q90xeklvdx47pnj5vyca2tkljed08us0ctj6k)
- [nostr.net](https://www.nostr.net/) aka awesome-nostr by [Aljaz](nostr:npub1aljazgxlpnpfp7n5sunlk3dvfp72456x6nezjw4sd850q879rxqsthg9jp)
- [nostr-protocol/nostr](https://github.com/nostr-protocol/nostr) by [fiatjaf](nostr:npub180cvv07tjdrrgpa0j7j7tmnyl2yr6yr7l8j4s3evf6u64th6gkwsyjh6w6)
- [nostr.org](https://nostr.org/) by [elidy](nostr:npub1a7n2h5y3gt90y00mwrknhx74fyzzjqw25ehkscje58x9tfyhqd5snyvfnu)
- [whynostr.com](https://www.whynostr.com/) by [zach](nostr:npub10fu0hlkx3s4n4dsgfu0cpqephga4afr4qtzpz9vsyqf7vj88v2yqdp8vp4)

Articles and explainers:

- [Can Nostr Make Twitter's Dreams Come True?](https://reason.com/2024/08/13/can-nostr-make-twitters-dreams-come-true/) by [Alex Gladstein](nostr:npub1trr5r2nrpsk6xkjk5a7p6pfcryyt6yzsflwjmz6r7uj7lfkjxxtq78hdpu)
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
- [Nostr - FOSDEM 2025](https://youtu.be/Tbt3jL1Ms0w) by [Wouter Constant](nostr:npub1t6jxfqz9hv0lygn9thwndekuahwyxkgvycyscjrtauuw73gd5k7sqvksrw)

For conference videos have a look at the [nostr world](https://www.youtube.com/@nostrworld) channel.

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

If you would like to donate to nostr development, have a look at various [nostr projects](https://geyser.fund/?search=nostr) or visit the [OpenSats Nostr Fund](https://opensats.org/funds/nostr). 

This site is open source too. If you can, please [improve this page](https://github.com/nostr-resources/nostr-resources.github.io). You can also create a [translation](#translations).

---

## Translations

- [Chinese translation](https://mp.weixin.qq.com/s/RoO-oOgGAXpcGyjD8IYBdw) by Cakksakkas
- [French translation](https://nostr.fr) by Marco.BTC.fr
- [Spanish translation](https://bitcoinnostr.com/recursos-de-nostr/) by [BitByBit](nostr:npub1luhyzgce7qtcs6r6v00ryjxza8av8u4dzh3avg0zks38tjktnmxspxq903)
- [German translation](https://cercatrova.blog/nostr-info-de/) by [cercatrova](nostr:npub1nxzp3zn90r44z07aeajc7wyah4fju49c9d3g45mxvmm64rmnrdusffch7m)
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
If you have suggestions, please [create an issue](https://github.com/nostr-resources/nostr-resources.github.io/issues).[^fn-lfm]
If you want to scream at me because you think this whole thing is stupid, please [find me on nostr](nostr:npub1dergggklka99wwrs92yz8wdjs952h2ux2ha2ed598ngwu9w7a6fsh9xzpc).

[^fn-lfm]: As mentioned above, this site could be way better (and up-to-date) than it is. If you're interested in maintaining it, please leave a comment in the "[Looking for Maintainers][lfm]" issues on GitHub: [nostr-resources/issues/62][lfm]

[lfm]: https://github.com/nostr-resources/nostr-resources.github.io/issues/62

---
