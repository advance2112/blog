---
layout: single
title:  "Incremental Decay"
date:   2025-11-23 15:01:00 -0500
last_modified_at: 2026-01-31 21:36:00 -0500
header:
    image: "/assets/images/IncrementalDecay/buildings.png"
categories: games
---

An incremental game about radioactive decay.

---

[**Incremental Decay**](https://advance2112.itch.io/incremental-decay) was made in 4 and a half days for the [Godot Wild Jam #87](https://itch.io/jam/godot-wild-jam-87). The Jam's theme was "Decay".

### The Jam
Between finishing [Project: Kardashev](https://advance2112.github.io/blog/games/2025/09/21/Project-Kardashev.html) and the start of GWJ#87, I had a number of major events happen:

1. I signed the lease for and moved into my new apartment,
2. I set up a large chunk of my stuff at my new apartment,
3. I bought and started tinkering with a 3D printer,
4. I had my gallbladder removed,
5. I had the worst comedown from medication (opioids) I've ever had,
6. I played Skyrim for like the 20th time, and
7. I house-sat for some friends who were out of town. Twice.

So, needless to say, I was having a rough time of it. But, that said, I was getting bored of Skyrim and needed a pick-me-up. What better thing to do than to make a game?

### The Theme
"Decay". Great theme, kind of the opposite of the "Expansion" theme from [GWJ#85](https://advance2112.github.io/blog/games/2025/09/21/Project-Kardashev.html). Whereas many things "Expand" in games, it's much more rare to see "Decay". Decay has many associations, including: death and decay, exponential decay, radioactive decay, signal decay, orbital decay, etc. I was instantly gripped by the theme, and decided to start work on a game right away.

### The Plan, Part 1
My new apartment is in the neighboring town to where I used to live. In order to get between these two towns, it is essentially required to cross a train track, be it by going under a bridge or through a railroad crossing. One common route I take has a railroad crossing, and on either side of the tracks, both ways, is an unusually thick line of trees, at least in comparison to the industrial area surrounding it. One night, before the jam but after I had my gallbladder removed, I passed through this crossing. I glanced down the tracks as my car coasted over the rails, and a vision struck me: a ghost train. Not that I actually saw a ghost train, but I imagined what it would be like to see such a thing, and how one might interact with it.

Also during this time, I remember coming across this game, [FAITH](https://store.steampowered.com/app/1179080/FAITH_The_Unholy_Trinity/). Not sure how, not sure when, but I saw a clip of it and was immediately struck with the thought "I have to make a game that looks like this."

So, with these two ideas floating in my head and hearing the theme "Decay"... it all made sense, and an idea solidified quickly. It would be like [Nodebuster](https://store.steampowered.com/app/3107330/Nodebuster/), but you'd be capturing spirits along the tracks of the ghost train. Or something like that.

### The Work, Part 1
I got to work quickly, slapping together something resembling Nodebuster's gameplay. I did a lot of this same stuff for [LaRtOoD](https://advance2112.github.io/blog/games/2024/11/17/LaRtOoD.html), spawning objects that move along a random path across the screen, so it didn't take me very long to get here:

<figure>
<img src="{{ '/assets/images/IncrementalDecay/ProjectLocomotiveGameplay.gif' | relative_url }}" alt="A number of Godot Area2D debug visuals move across the screen along Godot Path2D debug visuals.">
<figcaption>Nodebuster? More like Ghostbuster.</figcaption>
</figure>

### The Fall
And then I stopped. I guess I just got bored? I was recovering from surgery, still in a bit of pain, and in the middle of playing Skyrim. So, for whatever reason I dropped this and I... went back to Skyrim.

That's not to say that I'm disappointed. My goal at the time was survival, recovery, and comfort. Skyrim was bringing me all of these things. That was, right up until I was bored of that, too, but by then, there were only 4 days left in the jam. I knew this idea needed more time than that. So, I came up with a new idea.

### The Plan, Part 2
When you think of an incremental game, usually the growth of the game is somewhat exponential in nature. More cookies lead to more buildings lead to more cookies lead to more buildings... ad nauseam. But what if your cookies went stale? What if they "decayed"? What if they decayed exponentially?

A natural extension of the idea of a decaying currency is to make that currency some kind of radioactively decaying material. And thus, the concept for Incremental Decay was born: you are a mad scientist collecting every atom of radioactive material you can get your hands on, and you will stop at nothing to gather more. However, your stash will decay, and it will decay faster the more you have, so you need to "use it or lose it".

I did some research on how radioactive decay works. Of course, this concept of something decaying faster based on how much of it is around is more or less physics fan fiction, but realism often gets in the way of fun, if you ask me. I gathered up some common resources of radioactive materials and designed a system similar to [Cookie Clicker](https://orteil.dashnet.org/cookieclicker/)'s buildings, one building based on each source. I drafted the idea Tuesday night, and got to work Wednesday morning.

### The Work, Part 2
I started with a button that makes a number go up, simple stuff. Then a simple building and upgrade system. Then the unique part, making the currency decay into a different currency. I realized at this point that there was going to have to be some kind of soft cap to the amount of atoms you can hold, so I added the concept of "carrying capacity", which is upgradable.

And, I'll be honest, as far as the code, there really isn't much left to talk about. Like, it was pretty straightforward to develop once the concept was down. I spent more time balancing the game than anything else, and I had some help from [this article](https://blog.kongregate.com/the-math-of-idle-games-part-i/). And aside from that, I had no time for audio, and barely any time for visuals, all of which were either gathered from one of a few clip art sites or were just something built into Godot.

I had a lot more I wanted to do with it, such as making clicking and upgrading juicier, adding sounds and music, and adding a save system, but I just ran out of time. As the jam deadline neared, I went ahead and submitted what I had.

<figure>
<img src="{{ '/assets/images/IncrementalDecay/gameplay1.png' | relative_url }}" alt="A dark, black UI has three columns, the center being for buildings, the right for upgrades, and left for status. The left side shows a large number of &quot;Unstable Atoms&quot; and &quot;Stable Atoms&quot;. Below the status is a large depiction of an atom, which appears to be where you click, since there are numbers flying over top of the atom.">
<figcaption>I also spent a non-trivial amount of time coming up with the upgrade names. My favorite is "Nuclear Fuel Island".</figcaption>
</figure>

### The Results
As I mentioned earlier, I threw realism out the window very early on, so I was surprised to see that many people interpreted the game as educational. It most definitely is not. But, regardless, praise rolled in, saying that it was a well-balanced incremental game, and it was satisfying to finish. However, the lack of audio and lackluster visuals did get broad criticism, which is fair enough. 

I wound up with a pretty low rating, 101 out of 178 entries, with the highest category being Theme, and I didn't even break the top 10 there. The overall score here is, in fact, the lowest I have ever received in any jam, at least percentage-wise. Even compared to [Moon Viewing](https://advance2112.github.io/blog/games/2024/07/31/Moon-Viewing.html) and [The Tower of Babel](https://advance2112.github.io/blog/games/2024/09/22/The-Tower-of-Babel.html). I think that shows just how important audio and visuals are. Even with gameplay that many people praised, I wound up with the worst game I've ever made, at least critically.

As for other people's games, I didn't get a chance to play too many, only 8, but there were some standouts. [NumCrumMatch](https://felixleonggames.itch.io/num-crum-match) I could play for hours, [ace_of_4s' Gankenstein](https://ace-of-4s.itch.io/gankenstein) was yet another banger from them, and I played [URANIUM x PIT](https://calzark.itch.io/uranium-x-pit) for so long that I broke the game. I have yet to play the winning game, [The Moving Sands](https://blatalzar.itch.io/the-moving-sands), but it looks very good.

### The Lessons

1. Ok, but seriously, don't chase the bag.

   I won't lie. There was a small part of me that chose to do an idle game solely because of the success of [Project: Kardashev](https://advance2112.github.io/blog/games/2025/09/21/Project-Kardashev.html), which, at the time, had a couple thousand plays. Part of me was ready to chase that popularity once again. For my own sake, I'm glad this game didn't do as well as Project: Kardashev, because I might have fallen further down this hole that I keep saying I should step over, yet keep falling into.


1. In the context of a jam, juice and polish are actually more important than solid gameplay.

   Incremental Decay is, I think, pretty well balanced for what it is. It's a relatively short incremental game, but the progression is smooth and satisfying. As nice as all of that is, it just simply didn't perform well, and it's no surprise. The game is balanced, but it isn't fun to interact with. If I could go back and make this game again, I would have focused much less on balance and much more on the visuals and the juice.

### What's Next?
Shortly after finishing this game, I returned to work, and was feeling pretty much fully recovered from my surgery. With Thanksgiving and end-of-year Holidays coming up, I wasn't going to commit myself to anything major. Plus, there was still a good chunk of work that needed done around my apartment, mainly sorting and putting away my books, records, tapes, and CDs. I told myself that I'd pick things back up in the new year, if I felt up to it, and come January, I did, and made [ROGUE QUOTES](https://advance2112.github.io/blog/games/2026/01/18/ROGUE-QUOTES.html).