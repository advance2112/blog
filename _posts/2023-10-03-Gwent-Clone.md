---
layout: single
title:  "Gwent Clone"
date:   2023-10-03 04:55:00 -0500
last_modified_at: 2024-12-03 20:00:00 -0500
header:
    image: "/assets/images/GwentClone/gameplay1thin.jpg"
categories: games
---

The greatest form of flattery.

---

**Gwent Clone** was my first ever "real" game. It was made over the course of a year and a half, from May of 2022 to October of 2023. It was (kind of) made with two friends of mine, Jon B and Jon H. Due to the nature of this game and its use of copyrighted assets, there is intentionally no publicly available version. I will not willingly distribute this game either, so do not ask.

### The Plan
Jon B and I are huge fans of The Witcher 3. Gwent, the card game inside of the The Witcher 3, was a particular fixation in both of our playthroughs. But Jon B was always disappointed in the fact that you could never play Gwent against another person, only against an AI.

Now, of course, there is the Gwent standalone card game, but that game is very different from the Gwent inside The Witcher 3. In fact, it's so different that it's not even really the same game anymore. And I don't like it, and neither does Jon B. So, the plan was to remake Gwent from The Witcher 3, but this time with the ability to play against other people.

We are not the first people to have this idea. I won't link to them, but there are many other versions of this same idea, most if not all done better than how we did it. But we still wanted to make this. In my mind it was a project to do in my free time, something to occupy my evenings other than playing video games. So I hopped on the project. We also roped in Jon H, who had never (and I believe still has not) played The Witcher 3. But he was there.

### The Work
We began by watching a tutorial for making a 2D card game in Unity. Sadly, this tutorial is no longer public. We followed the tutorial pretty much to the letter, but skipping elements we knew we wouldn't need. We did this an hour or two at a time for literal months. If I were to do this over again, I would not have started it this way, but it's what we did.

By October of 2022, we had more or less done everything in the tutorial that we needed, and there was no tutorial left to watch. Being the most experienced programmer there, I figured I would take over the code and help the other two understand what I was doing as I went along. That didn't work out so well.

So I just wound up taking the project over almost entirely. I also recorded myself making the game in the hopes that the others would at least have it on in the background while they worked or something, but from what I know they never did that. Either way, through the end of the year I worked on the game pretty consistently, and by January we had a lot of the functionality of the game done.

But there was one crucial feature still absent: networked play. I wound up taking a break from the project for a bit and when I returned to it, I started looking into how to do networking and... wow. It's very complex. And there weren't any great (free) resources for how to do something like that with Unity. I got a few very basic things working in a very hack-y way, but I just felt overwhelmed with networking. So I kind of naturally took another break from the game.

A lot of projects would have died right here. Frankly, this project should have died a long time ago, even before starting on networking. But something kept me going, I couldn't exactly tell you what it was. But somehow, in June, I decided to pick the game up again. Importantly, I switched from using Visual Studio to Rider, and that made a huge difference, genuinely.

And I did it. I managed to work my way through making the game networked. It was a hack, honestly a joke in retrospect. Not that I could do it much better today but my goodness is it done poorly.

I then worked on polishing the game up. Polish is the wrong word. I made the game *not* look like hot garbage, it now just looks like garbage. But the game was never meant to look amazing, just function as Gwent does. And that's what it does. It's missing a lot, in particular effects and animations are highly lacking. But I'll be damned if it ain't Gwent you can play with a friend.

<figure>
<img src="{{ '/assets/images/GwentClone/gameplay1.jpg' | relative_url }}" alt="Gameplay of Gwent Clone. A Gwent board is laid out with 6 rows and a hand row. The player who's turn it is is winning. The board looks very simple, solid colors with shadow gradients. However the cards look very similar to how they appear in The Witcher 3.">
</figure>

### What's Next?

While the development was troubled and lengthy, I enjoyed a good chunk of the time spent making Gwent Clone. It sort of kick-started my interest in game development and directly led to the explosion of game development work I did in 2024. I had a bit of a slump from the end of 2023 until mid-2024, but I found my footing eventually and made [Moon Viewing](https://advance2112.github.io/blog/games/2024/07/31/Moon-Viewing.html).