# Lemmy - Beginner's Guide for Redditors
You’ve recently seen a post, comment or message telling you to "try out Lemmy". It sounds interesting but you have no idea where to find it. Googling "Lemmy" gives 50 different sites that all look the same. You go back to the post and find replies mentioning "federation" and "instances". This is the moment you give up due to confusion.

And I agree: discussion around Lemmy IS confusing. However, Lemmy is the best alternative to Reddit if you can get past the onboarding.

**This guide aims to bridge the gap between Reddit and Lemmy.** It is intentionally written in an order that does not dump everything onto you at once, but instead goes further in depth the further you get. For now, let’s begin with the basics: the registration process.

# Getting Started
**Go to "https://lemmy.world".** In the top right corner, click Sign Up. Enter your desired username together with your email and a password. Then click Sign Up.

**If the Sign Up button spins indefinitely after clicking it, the username is already taken.** There is currently an issue where the site does not inform you of this and instead stops responding. You can check if a username is taken by searching for that username's profile page at "https://lemmy.world/u/[the-username]" (replace "[the-username]" with the username you want).

After creating the account, go to your email's inbox and click the verify link in the mail you received from lemmy.world. There can be a delay of up to 30 minutes before the mail is sent. Sometimes the mail is detected as spam so check your spam folder too. Once verified, you can click Login in the top right corner of lemmy.world and enter your username and password to log in.

So far, so good. The procedure was identical to other social media platforms: **create an account, verify your email address, login.**

Now you can start browsing content. **Posts, comments, upvotes, downvotes, users, mods and admins are all functionally identical to Reddit.** Subreddits are too, but are renamed to communities. I recommend using the "Top Day" or "New" sorting options in "All" mode to find recent content.

That was all you needed to know to get started. You can choose to stop reading here, close this page, and enjoy lemmy.world for the next 10 years. Or you can keep reading, and get a glimpse of the (somewhat confusing) technology that future-proofs Lemmy from the same fate as Reddit.

*(Note: I recommend using a password that you’re not using anywhere else - which is standard practice on the internet nowadays.)*

# Lemmy Instances
A Lemmy website is like a self-contained Reddit clone. If you’re on lemmy.world you can tell people to come create an account on there and join you as if the site is a standalone Reddit alternative.

I mentioned in the introduction that there are other websites that show the same Lemmy layout. There are many of them - **because anyone can set up their own Lemmy website!** The developers of Lemmy made the technology available free of charge, open for modification to the wider public, and prevented companies from monetizing it.

You, as a regular user, are better off using an existing Lemmy website like lemmy.world. Setting up your own is a complicated process and there is no guarantee you will receive visitors.

I've been referring to these Lemmy websites as "websites", but this is inaccurate, just like calling Reddit a website is inaccurate. There are mobile apps that can access the same content shown on Lemmy websites. **Underlying each website is a "Lemmy instance" with its own storage for all posts and users on that instance.** This is what both the website and all mobile apps connect to.

The division between website/app and instance is similar to how email apps connect to email servers. Just like any email app can connect to Gmail, Microsoft Outlook or any other email server, an app that speaks in "Lemmy" can connect to lemmy.world, lemmy.ml or any other Lemmy instance.

# Lemmy Federation

## How it works in theory
The large social media platforms like Facebook, Twitter and Reddit are all isolated from each other. Connections between the platforms are limited to manual copy-pasting of links between them. I can send a tweet from twitter.com to someone on Reddit, but that forces them to open that tweet on twitter.com or in the Twitter app.

Imagine someone sends you a tweet that you open in your Facebook app and reply to with your Facebook account. Then someone on Reddit sees the tweet and replies to it with a Reddit account. All three of you can see the original tweet and both replies. Even better, imagine being able to follow Twitter users from within Facebook and seeing their Tweets merged into your Facebook timeline. You would never have to leave Facebook to interact with Twitter at all.

Facebook, Twitter and Reddit are like three Lemmy instances in that analogy. This is why you might have seen the claim that "it does not matter on which Lemmy instance you register, and you only need to register on one". **All Lemmy instances show identical posts and comments, and let you follow all users and communities.** Instances collaborate and transparently exchange data to make this possible. "Federation" is the name given to the collaborative process.

And that’s not all. It is possible to reply to a post created on a Lemmy instance that is currently offline, if you are browsing from another Lemmy instance. Right now, if Twitter would go down, no one would be able to reply to a tweet. But in a "federated" system, Facebook and Reddit would have saved their last seen version of the replies to that tweet, and would let you queue up a reply for when Twitter comes back online. If you replied to a tweet while Twitter is offline from another platform, other users on that platform would even be able to see your reply immediately. The moment Twitter comes back online, all replies are sent to Twitter and added to the original tweet, so that users on all platforms will see the new replies.

## How to navigate in practice
OK, it sounds good, but how do you as a user navigate the website to manually find content from other instances? Subscribing to communities and sending messages to users on other instances is by far the most confusing part of Lemmy.

**TL;DR of the following paragraphs: You need to paste "original" links into the search bar on the Lemmy instance where you created your account.**

### Communities and users
Let’s say you followed this guide and registered on lemmy.world. That means your account is stored on lemmy.world. A friend asks you to join the "music" community from lemmy.ml. Your first instinct might be to open lemmy.ml - but when you try that, you see that you are not logged in there and cannot log in with your lemmy.world account.

**Instead, you should always stay on lemmy.world.** To join the "music" community from lemmy.ml, you click the search icon in the top right corner on lemmy.world (not the "Communities" link) and search for ```!music@lemmy.ml``` including the exclamation mark (!) at the start. You should see the community pop up in the list after clicking Search. **In general, the search term is "![community-name]@[instance-name]".**

The process for finding users is similar. If you want to find me ("Amir" on lemmy.ml) you click that same search icon and search for ```@Amir@lemmy.ml``` including the at sign (@) at the start. Exclamation marks precede communities, at signs precede users. **In general, the search term is "@[user-name]@[instance-name]".**

You can also use the full link to the community or user on another instance. For example, pasting "https://lemmy.ml/u/Amir" into the search bar on lemmy.world will bring up my account. 

### Posts and comments
If someone outside of Lemmy sends you a link to a post or comment from a Lemmy instance that is not your own, you should open the link by pasting it in the search bar on your home instance, similar to finding a community or user. From there you can interact with it using your own account.

There is one issue with this copy-pasting of links between instances. What happens when you open a link from lemmy.ml on lemmy.world - either from your feed or by pasting it in the search bar - and you then share the post from within lemmy.world? You will send a link that's something like https://lemmy.world/post/123456, instead of the original post at https://lemmy.ml/post/234567.

If you share the lemmy.world link to someone from beehaw.org (another Lemmy instance) and they try to open this through their search bar on beehaw.org, it fails to find the post. But why? If it would have been possible to paste the link from lemmy.world, they would see a view on beehaw.org, of a view on lemmy.world, of a post on lemmy.ml. If a dozen people keep sending links like this between instances, there would eventually be a massive chain of links. The developers of Lemmy have prevented this by forcing you to find and share the original link instead.

To find the post on e.g. beehaw.org, **either you or the receiver needs to find the original link on lemmy.ml.** That is fortunately straightforward: **open any "wrong" link to the post and click the colourful rainbow star icon** next to or under the post. This brings you to the original link. The beehaw.org user can copy that link into their beehaw.org search bar and interact with the content as expected.

Once again, this is currently the biggest hurdle on Lemmy. Mobile apps are in development and should streamline this process soon™.

(Note: the links to the posts contain random numbers. I don't know what post they open.)

# Lemmy Defederation
Some owners of Lemmy instances have decided they want to keep their users from interacting with content on some other instances. Lemmy instances refusing to share content with another through instance banlists is called defederation. **If the instance you registered on either defederates or is defederated, there will be some potentially desirable content not reaching your feed.**

There is a misconception spreading that "it does not matter which Lemmy instance you register on". This claim would be correct in a perfect world. However, some owners defederate all instances they deem "too political". Others take "zero censorship" to the extreme and even refuse to defederate instances solely containing hate speech.

It is important that you choose an instance that aligns with your philosophy regarding content moderation. From my limited experience I found lemmy.world to be the easiest to recommend to anyone, especially with its almost 100% uptime. I have also heard that sh.itjust.works has been reasonable. If you don't trust a random guy on the internet (me) then ask around and search for an instance that you deem trustworthy.

# Fediverse
Lemmy as a platform is trying to fill the gap that Reddit left. However, the underlying federation technology that makes all the Lemmy instances work together is not limited to just Reddit clones. "Mastodon", which is to Twitter what Lemmy is to Reddit, already popularised federation years ago during the beginning of Twitter's enshittification. There is also "kbin" if you want to try out federated Facebook clones. And there are many more federated clones of popular centralised networks: https://en.wikipedia.org/wiki/Fediverse

All of these platforms use the same technology under the hood (ActivityPub). This lets these platforms interact to a certain extent. There are even comments on Lemmy from Mastodon and kbin users! This is the strength of what is called the "Fediverse": all of these services are nicely working together to provide one global network.

# Conclusion
I have seen other Reddit alternatives popping up: Squabbles, Tildes, Raddle, Teddit. In my opinion, they cannot be trusted anymore. Their owner could become the next Steve Huffman (/u/spez) at any moment and start yet another internet migration.

For the nonbelievers in decentralisation: email has been around for at least 40 years and is still chugging along as one of the most important communication channels to date. It was able to stay relevant due to the lack of centralised forces pressuring towards increased year-over-year profits.

Guess which decentralised networks are also still around: cellular phone lines, and the internet itself.

**If we as consumers want to break the cycle of platform migration, we should switch to a platform that cannot be destroyed. A platform that is not owned by anyone yet serves everyone. A platform that must be, by definition, federated.**

# Links

### Official list of instances:

https://join-lemmy.org/instances

### Community-created instance recommendations:

https://github.com/maltfield/awesome-lemmy-instances

### Community-created subreddit migration list:

https://sub.rehab

### Source code for Lemmy:

https://github.com/LemmyNet

### Setting up your own instance:

https://join-lemmy.org/docs/en/administration/from_scratch.html
