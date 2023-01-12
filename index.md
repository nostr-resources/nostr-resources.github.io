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

## WTF is nostr?

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

⚠️ **DO NOT PASTE YOUR PRIVATE KEYS INTO WEBSITES**[^fn-xss] ⚠️

Keys exist in two formats, `hex` and the above mentioned npub/nsec. You can use
a [key converter tool](https://github.com/rot13maxi/key-convertr)[^fn-keys] to
convert between the two formats.

[^fn-keys]: There's also the [damus.io/key](https://damus.io/key/) but DO NOT use it for private key conversions. Don't paste your private key into websites. Just don't.

[^fn-xss]: You have to trust whoever is running the website, obviously, and some clients are vulnerable to XSS attacks. A lot of people got rekt already, and had to re-build their nostr identity because of it.

Use [Alby](https://getalby.com) or [nos2x](https://github.com/fiatjaf/nos2x) to
generate your keys. These extensions will store your keys safely (or at least
more safely).

- [Nostr in the Alby Extension](https://blog.getalby.com/nostr-in-the-alby-extension/)
- [The nos2x browser extension and why you should use it](https://youtu.be/IoLw-3ok3_M)

You can also generate your keys by other means if you know what you're doing.[^bip85]
It's still early days, so be prepared to get rekt.

[^bip85]: [BIP-85](https://bip85.com/) is an option, for example.

## Clients

Periodically check [nostr.net](https://www.nostr.net/) which keeps a curated
list of clients. Here are some I like:

- [nostr.rocks](https://nostr.rocks/) - Twitter-style interface (Branle)
- [astral.ninja](https://astral.ninja/) - Fork of Branle with different UI & global feed
- [snort.social](https://snort.social/) - Very simple feed with automatic image-upload
- [yosup.app](https://yosup.app/) - Mobile-friendly and twitter-like

Mobile clients:
- [Damus](https://testflight.apple.com/join/CLwjLxWl) - Twitter-style iOS client, also works on MacOS
- On Android, you can use the [Kiwi Browser](https://kiwibrowser.com/) which allows you to install Alby or nos2x, which in turn allows you to use any web client. [Yosup](https://yosup.app/) has a good mobile experience, for example.

There are no native Android clients as of today. Nosky[^nosky] and Nostros[^nostros]
are in development and should be available for testing soon.

[^nosky]: [KotlinGeekDev/Nosky](https://github.com/KotlinGeekDev/Nosky)
[^nostros]: [KoalaSat/nostros](https://github.com/KoalaSat/nostros)

There's also [Nostr Console](https://github.com/vishalxl/nostr_console),
[noscl](https://github.com/fiatjaf/noscl), and
[nostr-commander](https://github.com/8go/nostr-commander-rs) if you're into CLI
stuff.


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

## Pro Tips

Some things work a bit differently and aren't obvious.


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

### Verification

If you have a domain and want to have a "verified" checkmark, here is some
useful info:

- [NVK's guide (using Github Pages)](https://nvk.org/n00b-nip5)
- [metasikander's guide (generic)](https://gist.github.com/metasikander/609a538e6a03b2f67e5c8de625baed3e)

### Stats

Ever since [Jack](https://twitter.com/jack/status/1603945963944480768) joined
(and funded some nostr devs) and [Elon put it on his naughty
list](https://twitter.com/dergigi/status/1604548665196138499) a flood of people
came streaming in. Since everything is out in the open, you can see this nicely
in the stats.

- [nashboard.space](https://nashboard.space/)
- [nostr.io](https://nostr.io/stats)
- [nostr.band](https://nostr.band/stats.html)

### Sats

Some clients will render Lightning invoices natively, showing the recipient, 
amount, and a pay button. One such client is Damus, which shows a nice 
[little widget and a pay button](https://i.ibb.co/zhd4Fbs/damus-invoice-render.png).

### Explorers

There's [brb.io](https://brb.io/) (also a relay) which indexes public notes and makes them [searchable](https://brb.io/search) and stuff. 
It also allows you to [view all public notes](https://brb.io/n/search?kind=1).

There's also [nostr.guru](https://www.nostr.guru/) which allows you view events by their ID.

And at [nostr.band](https://nostr.band/) you can search profiles and posts by keyword, and also check out links/hashtags/people that are currently trending on the network. 

### Bots

You can create a search bot at [sb.nostr.band](https://sb.nostr.band) and then follow it to receive new posts matching a keyword or hashtag right into your feed. 

---

### More info

- [nostr.net](https://www.nostr.net/) aka awesome-nostr by @aaaljaz
- [nostr-protocol/nostr](https://github.com/nostr-protocol/nostr) by fiatjaf

Articles and explainers:

- [What Is Nostr and How Do I Use It?](https://www.btctimes.com/news/what-is-nostr-and-how-do-i-use-it) by Walker V.
- [usenostr.org](https://usenostr.org/) by Pluja
- [What is Nostr, and how to start using Nostr](https://github.com/vishalxl/nostr_console/discussions/31) by Vishal
- [Nostr, an Introduction](https://wiki.wellorder.net/post/nostr-intro/) by Greg Heartsfield
- [Nostr Newcomers Most Common Questions and Answers](https://uselessshit.co/resources/nostr/) by pitiunited

It's still very early days. 
There's known [privacy issues](https://consentonchain.github.io/blog/posts/nostr-privacy/) and other things. 

nostr is an open protocol and most clients are open-source.
You are encouraged to report bugs and create PRs!

## Translations

- [Chinese translation](https://mp.weixin.qq.com/s/RoO-oOgGAXpcGyjD8IYBdw) by Cakksakkas
- [French translation](https://nostr.fr) by Marco.BTC.fr

## About these Resources

Most of the text above is copied from
[nostr-protocol/nostr](https://github.com/nostr-protocol/nostr) and
[nostr.net](https://www.nostr.net/). I just left some stuff out, so consider this an
opinionated summary.

This site is open source. [Improve this page.](https://github.com/nostr-resources/nostr-resources.github.io)

---
