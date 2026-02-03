---
layout: single
title:  "Project: Kardashev"
date:   2025-09-21 15:42:00 -0500
last_modified_at: 2026-02-02 14:38:00 -0500
header:
    image: "/assets/images/ProjectKardashev/Earthstrip.png"
categories: games
---

An idle game about humanity becoming a Type II civilization.

---

[**Project: Kardashev**](https://cache31522.itch.io/project-kardashev) was made in about 4 days for the [Godot Wild Jam #85](https://itch.io/jam/godot-wild-jam-85). The Jam's theme was "Expansion".

### The Jam

After wrapping up [The G.N.A.W. Protocol](https://advance2112.github.io/blog/games/2025/08/31/The-G.N.A.W.-Protocol.html) at the end of August, I had a number of things on my plate, including:

1. Playing Hollow Knight: Silksong (very important),
2. Working on something for [NOISE JAM](https://itch.io/jam/noise-jam) (which never got finished),
3. House sitting for a family member, and
4. Hunting for an apartment for myself.

In the middle of all of this, my brother, [Cache31522](https://itch.io/profile/cache31522), comes to me and says, in so many words, "I want to make a video game, can you teach me how?" And of course, I said yes. The [85th GWJ](https://itch.io/jam/godot-wild-jam-85) had begun just a few days prior, so I suggested we join and make a tiny little game. 

### The Theme
"Expansion" is a decent theme. It's almost a bit too generic in some ways, lots of things "expand", and there is an argument to be made that every incremental game ever made fits this theme. When a number goes up, it "expands", when you conquer new land, it "expands", when you learn something new, your mind "expands". This isn't a problem per se, but it feels like perhaps less creativity is required to come up with something that matches this theme. Either way, it's a fine theme.

### The Plan
Cache had the idea right after hearing the theme: a game about the "expansion" of human civilization, going from a Type I to a Type II civilization on the [Kardashev scale](https://en.wikipedia.org/wiki/Kardashev_scale) (hence the name). Initially, it was a more involved idea, including managing populations and transporting people and shipping things places, but we scoped it down to a simple, linear idle game.

Since the goal was to teach Cache about making games, we would do some partner programming, with me walking him through most of the steps. He would focus on the code, guided by me, and when he didn't need me, I would work on everything else (visuals, audio, exporting, all that stuff).

### The Work
We started with me teaching him the editor, showing him how to make nodes, move them around, and change their built-in settings. Then we got onto scripting, making a simple "number go up" button that updates its own text. We slowly built out more of the logic of the final game, and got to a point where I could leave him alone on some tasks. 

I started looking into finding some visuals we could use, and stumbled upon [Deep-Fold's Pixel Planet Generator](https://deep-fold.itch.io/pixel-planet-generator) and [Space Background Generator](https://deep-fold.itch.io/space-background-generator), which went on to inform the entire vibe of the game. With the game being entirely UI-based, the retro style of these made me think of an old DOS game, so I looked into creating a retro computer vibe. I found a [Windows 98 GUI pack](https://comp3interactive.itch.io/retro-windows-gui) that worked perfectly. It was a bit of a pain to get working in Godot, but we got there.

From here, I gathered some audio. There were no original sounds recorded for this game, just some reused keyboard sounds from [SUFFER.er](https://advance2112.github.io/blog/games/2024/10/20/SUFFER-er.html) and a song from [this excellent collection of public domain works](https://tallbeard.itch.io/music-loop-bundle) by [Abstraction](https://www.abstractionmusic.com/), which I previously used for [Crumbania](https://advance2112.github.io/blog/games/2025/08/17/Crumbania-and-pju.html). 

Of course, this was Cache's game, and he had full rights to veto any decision of mine, which he only did once or twice. We worked back and forth and in parallel a bit for a couple days, and got to a decent point with it by the end of the last full day of the jam. Unfortunately, Cache had an event the next morning, so I would have to take it home on my own.

I had yet to finish implementing all the visuals, so I spent the last day polishing those up, including getting the Dyson Swarm Parts looking clean (which took some doing). After that, we put the game up, I made up some stuff for the itch page, and we were done. In just 4 days, we managed to make a game with some incredibly immaculate vibes.

<figure>
<img src="{{ '/assets/images/ProjectKardashev/gameplay.png' | relative_url }}" alt="Final gameplay of Project: Kardashev. A Windows 98-style retro UI has a number of panels within it, labeled &quot;Planets&quot;, &quot;Resources&quot;, &quot;Buildings&quot;, and &quot;Currently Viewing: Mars&quot;. In the &quot;Currently Viewing: Mars&quot; panel, there is a depiction of the planet Mars floating in space. The other panels contain game information, such as how much Power and Materials the player has, how much it costs to buy the next buildings, and how much it costs to unlock the next planet. There is a CRT effect over the screen.">
<figcaption>Vibes.</figcaption>
</figure>

### The Results
As I mentioned, I had a lot of things going on at the time, and even moreso during the rating period. (To give you an idea, I signed the lease to my new apartment during this time.) But I did play a few, and my favorite has to be [Super Fighter X](https://ignsu.itch.io/super-fighter-x). Great, unique take on the theme, with some funny twists and turns. Such an excellent jam game. The game that won this jam, [Vena](https://loerting.itch.io/vena) has continued development since and is even [on Steam](https://store.steampowered.com/app/4165740/Vena/)! I have yet to play it, but it looks right up my alley, so it's on my wishlist.

As for Project: Kardashev, we got a decent ranking: 24th overall, with higher scores in Audio and Graphics. Overall, the feedback we got from this game was incredible, and a little overwhelming. We received a lot of praise for the visuals, the audio, and, of course, the vibes. What was unexpected was the actual volume of people playing this game. During the rating period, over 500 people played it, mostly coming from the itch.io "idle" tag section. But after the rating period? Someone out there put the game on something called [incrementaldb](https://www.incrementaldb.com/) and it "blew up". Well, not exactly. It got a lot of plays, 700 in one day (October 1st, 2025) and has had a very long tail. At time of writing, it just surpassed 3500 plays and has been hovering around 5-10 plays _per day_ since that spike. This is by far the best performing game I have ever released.

Once Cache and I discovered this, we immediately went into planning mode again, asking ourselves: how do we capitalize on this? We planned new features, new mechanics, new systems, a new genre... it was all a bit much, and a sickly feeling started to wash over me. I started pushing back after I remembered what happened the last few times I worked on a game that was intended to be commercial (it didn't go well). Eventually, we scrapped the idea, ultimately recognizing this for what it was: a flash in the pan. Honestly, any competently made, vibe-tastic idle game posted to itch and incrementaldb is likely to do numbers. [Gopher](https://quencheddisorder.itch.io/) shared with me that his game, [Biosphere](https://quencheddisorder.itch.io/biosphere) (which also has immaculate vibes, go play it), was picked up by the itch algorithm as well, and he got a bit over 1000 plays. Not to suggest that it is trivial to make a popular game on itch, but chasing popularity (or worse: money) leads down a path I'd rather not walk. Not today, at least.

### The Lessons

1. Using pre-made assets is awesome.

   I wrote something similar for [Crumbania](https://advance2112.github.io/blog/games/2025/08/17/Crumbania-and-pju.html): "Using pre-made assets is a superpower", but we kind of took that idea and ran with it. Literally nothing in this game that you see or hear was made specifically for this game, aside from how it is all laid out. This level of pre-made asset use and re-use really only works for certain kinds of games, but when it works, it can work really, really well.


1. Don't chase the bag.

   Never chase the bag. Never let money be your boss. The concept of having to hustle and make money every waking moment of your life is a capitalist lie to keep you unsatisfied and unhappy. Have fun, be free, seize the means of production, yadda yadda, you get it.

### What's Next?
As mentioned at the top, I had a lot going on. Hell, I had shit going on that I wasn't even aware of, like having a botched gallbladder that I had removed in early November. At the time, I told myself I would get settled into my new apartment and start making games again in the new year. But I just couldn't help myself, and made [Incremental Decay](https://advance2112.github.io/blog/games/2025/11/23/Incremental-Decay.html).