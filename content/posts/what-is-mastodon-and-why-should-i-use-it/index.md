---
title: "What is Mastodon and why should I use it?"
date: 2018-09-05T10:45:21+01:00
tags: ["twitter","mastodon","Moving to Mastodon","safety","ethical design"]
categories: ["Social Networks"]
type: "post"
body_classes: "blog"
colours:
    primary-bg: "327,100%,93%" # hsl(327,100%,93%)
    secondary-bg: "330,66%,86%" # hsl(330,66%,86%)
    text: "229,16%,19%" # hsl(229,16%,19%)
    linktext: "208,92%,30%" # hsl(208,92%,30%)
    darklinktext: "204,16%,6%" # hsl(204,16%,6%)
    brilliant: "208,63%,52%" # hsl(208,63%,52%)
    tab-two: "277,40%,86%" # hsl(277,40%,86%)
    tab-three: "235,40%,82%" # hsl(235,40%,82%)
    tab-four: "219,50%,74%" # hsl(219,50%,74%)
    tab-five: "213,56%,66%" # hsl(213,56%,66%)
    tab-six: "211,61%,60%" # hsl(211,61%,60%)
image: "images/2018/08/mastodon-elephant.png"
imagealt: "The Mastodon mascot is a cute elephant."
description: "Now you know why I’m moving away from Twitter, you probably have a vague idea of what I’m looking for in a social network. Mastodon is unique for a few reasons: it is federated, ethical, and inclusive."
---

This post is a follow-up to [What’s wrong with Twitter?](/what-is-wrong-with-twitter).

[You can read this post en français on the Framasoft blog](https://framablog.org/2018/09/17/bye-bye-twitter-hello-masto/).

<hr/>

[Mastodon](https://joinmastodon.org) started out as a microblogging platform similar to Twitter, but has evolved with more features that show an ethical, progressive and inclusive focus. Instead of tweets, your posts on Mastodon are called toots.<!--more-->

Jump to:

- [Why use Mastodon and not another new social network?](#why-use-mastodon-and-not-another-new-social-network)
- [How to use Mastodon](#how-to-use-mastodon)
- [My instance-of-one](#my-instance-of-one)
- [How to set up an instance-of-one](#how-to-set-up-an-instance-of-one)
- [But but but](#but-but-but)
- [Join me there!](#join-me-there)

<img src="/images/2018/08/mastodon-elephant.png" alt="The Mastodon mascot is a cute elephant." style="max-width: 500px;"/>

## Why use Mastodon and not another new social network?

Now you know why [I’m moving away from Twitter](/what-is-wrong-with-twitter), you probably have a vague idea of what I’m looking for in a social network. Mastodon is unique for a few reasons:

### Mastodon is federated

> “Mastodon isn’t just a website, it is a federation—think Star Trek. Thousands of independent communities running Mastodon form a coherent network, where while every planet is different, being part of one is being part of the whole.”

Federation means there are lots of different communities running the Mastodon software, but every individual in each community can talk to each other using Mastodon too. Each domain where Mastodon is being run is referred to as an “instance.”

#### Federation vs centralisation

In my post about Twitter, I mentioned “because we are using the platforms of big corporations, we hand the responsibility for decisions on how to handle abuse over to corporate control.” That way the power is held by an individual or small group of people is a form of centralisation.

There are different ways [centralisation](https://en.wikipedia.org/wiki/Centralized_computing) is manifested across the web, but for platforms like Twitter, centralisation means the platform is run on a server owned and controlled by that corporation. So to use Twitter, you have to go to Twitter.com, or use a service or app that communicates directly with Twitter.com. This means that Twitter has absolute control over its software, how people use it, and the profile and behavioural data about those people too. [Aral](https://ar.al) explains this by saying [these platforms are not like parks, but like shopping malls](https://2018.ar.al/notes/encouraging-individual-sovereignty-and-a-healthy-commons/). You can enter freely, meet your friends there, have conversations and buy stuff, but you are subject to their rules. They can monitor you with surveillance cameras, they can surround you with advertising, and they can kick you out if they don’t like what you’re saying or doing.

The opposite of centralisation is decentralisation. One decentralising alternative to publishing on Twitter is posting your little status updates to your blog, like I do with [my Notes](/notes). That way I own and control my own content. (Within the bounds of my web host.) If everyone posted their status updates to their blogs, but goes to read each other’s blogs, that would be a decentralised network.

But posting status updates to a blog misses the social element of social networks. We don’t just use social networks to shout into the void, we use them to [share experiences with each other](/insecure). [Aral and I are working on ways](https://ind.ie) for us to do this with our personal sites, but we’re not there yet. And that’s where federation comes in.

I have my own Mastodon instance, [mastodon.laurakalbag.com](https://mastodon.laurakalbag.com) where it’s just me (and [Oskar](https://mastodon.laurakalbag.com/@gigapup)). This is referred to as an “instance-of-one.” It’s hosted on my own domain, so I own and control everything I post on there, but because I have the Mastodon installed on there, I can see what other people post on their Mastodon instances, and reply to them with mentions, or favourite and boost (like retweet) their toots, even though they are on different instances. It’s like having my own Twitter which can talk to other Twitters, where I make the rules.

### Mastodon is ethical

You can tell a lot about Mastodon’s approach from the [Join Mastodon homepage](https://joinmastodon.org):

> “Mastodon is free, open-source software that anyone can install on a server.”

Mastodon is free and open, which is why we can have our own instances with our own rules. It also means that if Eugen Rochko, who makes Mastodon, went in a direction that people didn’t like, we (dependent on our capabilities) can fork it, and make our own version.

> “Using a suit of standard protocols, Mastodon servers can exchange information with each other, allowing users to interact seamlessly… Thanks to standard protocols, the network is not limited to Mastodon servers. If better software comes along, it can continue with the same social graph.”

Mastodon uses standard protocols, which means that you can federate with Mastodon even if you are not using Mastodon yourself. This means you’re not locked into Mastodon, as it is interoperable, but also that other technology can work with your toots in the future.

> “There is no advertising, monetizing, or venture capital. Your donations directly support full-time development of the project.”

This is a big deal. Mastodon is funded by donations, not advertising or any other nefarious way to monetise your information, and not by venture capital. This means there’s no board of directors who will decide that they need to start doing stuff to monetise you to get a return on their investment, or for “growth.” It does mean that we are dependent on the good will and generosity of Eugen. But, as I mentioned above, because Mastodon is free and open, if Eugen somehow becomes a monster (it seems unlikely), we can fork Mastodon and make a different version that works for us.

### Mastodon is inclusive

One of the biggest issues with Twitter is the moderation (or lack thereof) of harassment and abuse. [Cage The Mastodon](https://blog.joinmastodon.org/2018/07/cage-the-mastodon/) is a post by Eugen which explains how Mastodon is designed to prevent harassment where possible, and give you tools to ensures your timeline, and your replies, are only what you want to see. 

> “Mastodon comes with effective anti-abuse tools to help protect yourself. Thanks to the network's spread out and independent nature there are more moderators who you can approach for personal help, and servers with strict codes of conduct.”

Of course, Mastodon is not perfect—this [constructive criticism by Nolan Lawson covers some of the biggest issues and potential approaches](https://nolanlawson.com/2018/08/31/mastodon-and-the-challenges-of-abuse-in-a-federated-system/)—but Mastodon prioritises anti-abuse tools, and folks working on Mastodon prioritise design decisions that favour safety. For example, you cannot just search for a keyword on Mastodon. This means people looking to start a fight or a pile-on can’t just go searching for ammunition in other people’s toots. If you do want keywords in your toots to be searchable, you can use hashtags, which are searchable.

Another of my favourite features of Mastodon is that you can provide alternative text descriptions for images a as default without the option being hidden in an “Accessibility” menu.

<figure>
<img src="/images/2018/09/mastodon-screenshot.png" alt="screenshot of Mastodon interface for posting a toot with an image. By default an input box is shown over the image with the label “Describe for the visually impaired”"style="max-width: 350px;">
<figcaption><p>It’s a subtle way of Mastodon telling people that they’re expected to make their images accessible for their friends.</p></figcaption>
</figure>

## How to use Mastodon

I’m not an expert, and my use of Mastodon is still in its infancy. Here are a list of great How-To guides by people who know Mastodon far better than me:

- **[An Increasingly Less-Brief Guide to Mastodon by @joyeusenoelle](https://github.com/joyeusenoelle/GuideToMastodon/)**—Simply-written guide following a Frequently-Asked-Questions format. Useful if you want to find an answer to a specific question.
- **[Toot How-to: Intro to Mastodon by Ginny McQueen](https://medium.com/@GinnyMcQueen/toot-how-to-intro-to-mastodon-e5655bfa87d2)**—Covers all the introductory basics to Mastodon with an eye on keeping yourself safe. 
- **[What is Mastodon and why is it better than Twitter by Nolan Lawson](https://nolanlawson.com/2017/10/23/what-is-mastodon-and-why-is-it-better-than-twitter/)**—A detailed introduction to Mastodon and some of its history.
- **[Cage The Mastodon by Eugen Rochko](https://blog.joinmastodon.org/2018/07/cage-the-mastodon/)**—“An overview of features for dealing with abuse and harassment” which also explains the design decisions behind Mastodon.
- **[How Does Mastodon Work? By Kev Quirk](https://kevq.uk/how-does-mastodon-work/)**—Introduces Mastodon with comparisons to Twitter, in case that makes it easier to understand.
- **[Mastodon Post Privacy](https://dev.glitch.social/@cassolotl/99942218361780184)**—A toot explaining who can see what when you toot on Mastodon with various settings.
- **[The Definitive List](https://github.com/tootsuite/documentation/blob/master/Using-Mastodon/Apps.md)**—A handy of apps and web clients for using with Mastodon, beyond the default interface. It also has other useful stuff listed, such as cross-posting tools.

### Join a small instance, or get your own

If you’re interested in Mastodon, you will have to pick an instance you want to join, or set up your own. I’m an advocate for instances-of-one in most cases, but if you just want to dip your toes in, or have bad experiences being harassed on social media elsewhere, I recommend you join a small instance with a Code of Conduct that suits you.

Most people join mastodon.social (I did) first. **You should not join mastodon.social.** It is the largest English-language instance run by the developers of Mastodon, including Eugen Rochko (also known as @gargron.) They have [a No-Nazis policy and seem to care a great deal](https://mastodon.social/about/more). However, mastodon.social has a lot of people using it. When I last checked, it was just short of 230,000 people. This means there’s a lot of pressure on the moderators, and on the server, and it really defeats the federated design if everyone joins the same instance. Remember, you can easily communicate with a person on any other Mastodon instance. If people are nagging you to join *their* instance, and it’s not for the superior Code of Conduct and moderation, I would question their motives.

**Be aware that an instance’s admin can read your direct messages.** Also the admin of the instance that the person you are messaging belongs to. This is because your private messages are not end-to-end encrypted. While I don’t think this is catastrophic to Mastodon (it’s exactly the same with your messages on Twitter, Facebook, Slack etc.), it’s a reminder that you really need to be able to trust the admin for your instance. Also if you want truly secure and private messaging, you should always use a dedicated messenger with end-to-end encrypted messaging, such as [Wire](https://wire.com/en/features/).

#### Why doesn’t Ind.ie have an instance we can join?

A few people have encouraged Aral and I to start our own instance. We won’t do this because:

1. Most importantly: **decentralisation is our goal.** We don’t want to be responsible for owning and controlling your content, even if you trust us with it. (You shouldn’t!)
2. Also, we would be lousy moderators. Moderators should be trained and have relevant experience. They are the first defence against harassment and abuse. Moderators must be fair arbiters in disagreements, and enforce their Code of Conduct. That is a full-time job, and I believe it can only be effective on small instances.

## My instance-of-one

I first joined Mastodon.social [in late 2016](https://mastodon.social/@laurakalbag/54674). While I was fairly active on the [@Better](https://mastodon.social/@better) and [@Indie](https://mastodon.social/@indie) accounts, my own account was very quiet. Mastodon.social was already fairly big, and I wanted to have my own instance, and not invest too much of my time in an account that would eventually cease to exist.

But I didn’t want to host and maintain a Mastodon instance by myself. It’s big and complex software, and I am not a big and complex backend developer or sysadmin. Also I just don’t have time for learning the skills required, or even keeping up-to-date with new releases and security updates.

So when Masto.host, a webhost for “fully managed Mastodon hosting” was recommended to me, I knew this was what I needed to make the leap into hosting my own instance.

### Why set up an instance-of-one?

Everything I post is under my control on my server. I can guarantee that my Mastodon instance won’t start profiling me, or posting ads, or inviting Nazis to tea, because I am the boss of my instance. I have access to all my content for all time, and only my web host or Internet Service Provider can block my access (as with any self-hosted site.) And all blocking and filtering rules are under my control—you can block and filter what you want as an individual on another person’s instance, but you have no say in who/what they block and filter for the whole instance.

You can also make [custom emoji](/custom-emoji-on-mastodon) for your own Mastodon instance that every other instance can see and/or share.

### Why not set up an instance-of-one?

In a previous post about levels of decentralisation being [beyond my means](/beyond-my-means), I looked at the privilege that make us able, or unable, to embrace owning and controlling our own content. The same goes for social networking, particularly in terms of safety. Sometimes we don’t want to, or can’t, moderate our own social network.

I am a privileged person because I can deal with the low-level harassment I get. This is not a marker of my mental fortitude, it’s just the worst I get is creepy dudes coming on to me in my <abbr title="Direct Messages">DM</abbr>s, and some people slagging off our work at [Ind.ie](https://ind.ie) in an non-constructive and/or hurtful manner. It is not endless, it is manageable through conventional blocking and muting tools. (I’m also a fan of the pre-emptive block, but that is a post for another day.) I’ve not (yet?!) been the victim of a pile-on, targeted harassment, or more explicit abuse.

But many folks are the victims of this type of harassment and abuse, and they cannot be expected to maintain their own instances. Because in order to be able to effectively block, mute and moderate bad people and things, you have to see those bad people and things. 

In the same way that I believe government should provide safety nets for society’s vulnerable and marginalised people, the web should too provide safety nets for the web’s vulnerable and marginalised people. I see small moderated instances as these safety nets. Ideally I reckon you should know your instance admin in person. Instances should be akin to families (with good relationships) or small clubs in the offline world. In those situations you may have someone who represents the group as a leader when required, but it’s an otherwise flat hierarchy. 

Knowing good people who have your back is something of a privilege, so perhaps taking a word-of-mouth recommendation for a small instance from a person you know could suffice. I’ve not been in this position, so take my suggestions with a pinch of salt, I just want to emphasise the potential for negative repercussions when deciding who can control your online social life. (Take heed from those who have faced repercussions of Twitter or Facebook deciding [how much racist abuse is ok](https://twitter.com/ssoper/status/1034489632795308032) or what is [their real name](http://money.cnn.com/2015/06/01/technology/facebook-protest-names/index.html).)

## How to set up an instance-of-one

If, like me, you are not great with sysadmin, or just don’t have the time to maintain your own Mastodon instance, I recommend [Masto.host](https://masto.host). At Masto.host, Hugo Gameiro does the installation and hosting of small Mastodon instances for €5 a month. The process goes something like this:

1. **Buy a domain name** (if you don’t already have one you want to use)
2. **Sign up for Masto.host** and let Masto.host (Hugo) know the domain name you want to use. I’ve set mine up at `mastodon.laurakalbag.com` which is quite long, but it’s very clear that it is my Mastodon instance just from the name.
3. **Set DNS settings**. Masto.host then sends you a couple of changes that you need to make to your domain’s DNS settings. Most domain name providers will have a page where you can do this. Then let Masto.host know you’ve made those changes.
4. **Create your Mastodon account**. Masto.host will install your Mastodon instance. You will then get an email asking you to create your Mastodon account. Create the Mastodon account for your admin. Then let Masto.host know that is your chosen admin account. Masto.host will then grant your admin account those privileges.
5. **Make your Mastodon instance what you want it to be**. Once you have admin privileges, you can customise your Mastodon instance however you like. You probably want to start by closing registration to others (Settings > Administration > Site Settings.)

The whole process with Masto.host took around an hour for me. But bear in mind that this is a process that requires some manual intervention, so it could take longer. Masto.host is run by a single real human (Hugo), not a faceless corporation, who needs to sleep, eat, have a life, and maintain other instances, so if you do sign up for Masto.host, please be kind and polite!

## But but but

Whenever you start to recommend an alternative social network, people will have their reasons for telling you why it is not for them. That’s fine. As long as the criticism is warranted. As Blaine Cook summarised well on Twitter…

> “While I've been thinking about and working on this problem since the very beginnings of Twitter, I haven't had much success at addressing these problems. Nor has anyone else.
>
> These are *hard problems*. Facile criticism of earnest efforts isn't going to get us anywhere. 
>
> Which isn't to say criticism isn't warranted. There are many legitimate issues. But if the argument defaults to "so we should all just continue to hang out on and moan about Twitter" it seriously undercuts the legitimacy of any criticism.” —[Blaine Cook on Twitter](https://twitter.com/blaine/status/1030586266532933633?s=21).

Still, there are some arguments worth quickly covering:

### All my friends/cool people/interesting discussions are on Twitter…

Were all your friends, the cool people, and the interesting discussions on Twitter when you joined? Treat Mastodon as a chance to start afresh, find new people to follow, maybe even take the opportunity to follow a more diverse group of people…! You can cross-post across Twitter and Mastodon if you must. (Just don’t cross-post retweets or @replies, it looks ugly and unreadable.) 

I subscribe to accounts and lists on Twitter using RSS with [Feedbin](https://feedbin.com), so I can still keep an eye on Twitter while weaning myself off.

### I don’t have the time to join another social network

Even setting up my own instance only took an hour. Joining an existing instance takes less than 30 seconds once you’ve decided which instance to join. [Instances.social](https://instances.social) can help you find a small instance that works for you. Make sure you read their Code of Conduct!

## Join me there!

If you read this post and sign up for Mastodon, [toot me!](https://mastodon.laurakalbag.com/@laura) I’ll be happy to follow you and answer any questions you have about Mastodon or running your own instance (or boost them when I don’t know the answer!)

Mastodon may not be our final destination as a social network, it might be a stopgap along the way. But it is a genuine alternative to what already exists. We’re currently stuck with platforms that amplify our society’s systemic issues (racism, sexism, homophobia, transphobia) because we don’t have alternatives. We can’t escape these platforms because they’ve become our new social infrastructure. We’ve got to try out alternatives to see what sticks, and as folks who work with the web day-to-day, we should take responsibility for finding safe technology we can share with our loved ones.

<hr/>

Part 2 of a series on [Social Networks](/categories/social-networks)

- Part 1: [What’s wrong with Twitter?](/what-is-wrong-with-twitter)