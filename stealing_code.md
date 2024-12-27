# Stealing code
I — `zeph` — am going to adopt the first person here and speak about this from my own perspective, with my words, as this specific matter involves me personally.

### Sodium 2
When I first joined the Destination Home team, I’ve tried to become what could be defined as a mediator between the two teams. I was initially given my own team’s perspective on Home Headquarters and their warnings regarding them. **I chose to ignore them** because **I wanted to form my own opinion** without being influenced or biased towards either side.

One of the first things I’ve worked on, soon after I’ve joined Destination Home’s development team, was a space called `Sodium 2: Velocity Racer`. At that point I had already built an API that would answer the game’s requests, but this one was particular: it required plenty of XML files that were lost to time and never cached by the game originally.

At that point, I started disassembling the game and reverse-engineering the way it worked, to recreate the lost schema of the XML files needed for it to function. After approximately two days, I had gotten the game to function properly again, making me *the first person to ever play Sodium 2 again, after its death in 2015*.

### Sharing my work with Home Headquarters
I was extremely proud of my achievement, and decided to showcase it to Home Headquarters’ team members, as by that point I thought we had gotten to a point I could call a friendship.

I was immediately asked whether I’d hand them over my hard work, to which I declined. I was part of the opposing team, after all. *How could I straight-up hand my work over to the “competition”?*

### Home Headquarters turning hostile
Seeing me unwilling to give them my reverse-engineered XML files for them to use, **their entire team immediately turned against me**. I was accused of being a show-off and of being “fake” for my unwillingness.

### But why does all of this matter?‌
Sometime around a year later after that, Home Headquarters had released *their* own version of Sodium 2, the same space that I, a year ago, had gotten working once again.

I became immediately skeptical of them, and as such I decided to probe their CDN (hosted over HTTP on `64.20.35.146` — *check the WHOIS records for `homeheadquarters.online` for proof*) to check what their work looked like.

**To little surprise, their server responded with my files.** 
#### How did I know they were my files?
- *I had left plenty of comments meant for myself only*, to note the way the game expected the XML schema to look like.
- *The prices of the various items players can purchase was calculated by the other members of the Destination Home team*, while trying to achieve a balance between a fun experience and a challenging one.
- ***The files were SHA-1-identical to the copies first released on Destination Home around a year prior to that.***

### Questioning Home Headquarters about it
As soon as I found out about that, I’ve immediately messaged `AgentDark447` (Home Headquarters’ lead reverse engineer and developer) asking for an explanation as to why my files were released on their server.

**Every single time, I was lied to.** They kept saying that “they found the files inside of some `sodium.zip` folder Agent had on his Desktop for months”. The story eventually evolved into “someone giving Agent cached files from back in the day”.

### Development chat shows their lies
Their entire story was bullshit, as expected. Reading the \#development chat shows their team actively attempting to steal those files from our CDN.
1. First, *they tried capturing them from the game’s memory*.
2. After that, *they tried to capture them using `HTTP Debugger`*, a software for HTTP-packet network capture.
3. Later on, *they tried to probe our AWS CDN directly*.
4. Finally, *they joined our servers through various alt accounts, had the files downloaded by the game, and then extracted them from the `CACHE` directory* the game uses to store cached files.

> There’s literal mentions of `DeViL303` (one of their team members, at the time) suggesting the rest to straight-up admit to it like “yeah, we stole them, now cry about it”.