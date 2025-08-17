---
layout: single
title:  "Crumbania (and Its Post-Jam Update)"
date:   2025-08-17 00:00:00 -0500
last_modified_at: 2025-08-17 12:44:00 -0500
header:
    image: "/assets/images/Crumbania/logothin.png"
categories: games
---

Eat crumb... consume crumb... become crumb...

---

[**Crumbania**](https://advance2112.itch.io/crumbania) was made in 9 days for the [Godot Wild Jam #83](https://itch.io/jam/godot-wild-jam-83). The Jam's theme was "CONSUME".

### The Start
It's been a long, long time, hasn't it? [The last game jam I did](https://advance2112.github.io/blog/games/2024/11/17/LaRtOoD.html) went rather well, so why did it take me nearly 9 months to do another one? Well, four things were going on between LaRtOoD and this game. In this time, I:

1. Did post jam updates for all my previous jam games.
1. Started a personal game project that since has been put on pause.
2. Joined another large game project (Hemocoven) that, while good progress was made, I ultimately decided to quit working on for reasons detailed later in this post.
3. Played lots of really damn good video games, including getting Balatro's Completionist++ achievement, playing 3 different 3D RPGs, and buying both a PS5 and a Switch 2.

I wouldn't say I was 'busy' in this time, but rather 'occupied' and 'a bit depressed'. Even the two game projects I worked on never felt quite right in this time, not quite the same as a jam game.

Come late June, I'm occupying my time with a bunch of games throughout the month, and I'm just feeling a bit burnt out by it all. I was half-assing my work on Hemocoven, and even decided to put it on hold around this time. I told the team something like "my desire to create is really low right now", which was true, but, in retrospect, I think it was moreso my desire to work on Hemocoven was really low. I suspected this, even at the time, and I wanted to test it, and the best way to do that was to work on something other than Hemocoven.

### The Jam
I eventually convince myself to make a game, and by then, the next GWJ is just a few days away from starting. So I say to myself: "Fuck it, I'll make a tiny little game, just something simple, a clone of some simple game. I'll make it in a weekend, I'll use pre-made assets or make some simple assets, do whatever I need to do to just shit this game out in like 2 or 3 days. It won't be good, it won't be pretty, but it will be a good test of whether I really do have a low desire to create or if it's just Hemocoven dragging me down." So I join GWJ #83.

### The Theme
CONSUME. Excellent theme. Unlike something like "Reflections" from GWJ #75, "CONSUME" can only be interpreted in a number of ways: consume food, consume media, consume items, and that's pretty much it. But consumerism and food are such large parts of our culture (especially as gamers) that it's hard not to like this theme for the breadth of ideas that can come from it.

The wildcards (optional themes) were "Twinkle Star" (have a bunch of particles), "Unreliable Narrator", and "Analog" (make assets in the real world). 

### The Plan
Within just a few minutes of the theme's announcement, I had the idea. It's Vampire Survivors. Instead of monsters, you fight food. Instead of weapons, you have cutlery. Instead of exp orbs, you collect crumbs. It's dumb, it's stupid, and it's also dumb. But it's enough of an idea to latch onto, and it's simple enough to do in a weekend.

From here, I thought I'd take the most straightforward approach to the "Twinkle Star" and "Analog" wildcards, namely making there be a bunch of particles whenever you kill an enemy, and drawing everything on paper and scanning it in.

### The Work, Part 1: The Weekend
I got to work right away. I tried to recreate as much of the Survivor formula as I could from memory, choosing not to play any Survivor-like games until the jam was over. I got some simple weapons, enemies, and experience orbs working, and 8 hours into the jam, I had something that vaguely resembles the final game, as well as Vampire Survivors.

<figure>
<img src="{{ '/assets/images/Crumbania/progress1.gif' | relative_url }}" alt="Early Gameplay of Crumbania. A handful of collision shapes with their debug visuals on roam around the screen in a fashion vaguely resembling Vampire Survivors gameplay.">
<figcaption>Where would I be without Godot's "Visible Collision Shapes" option?</figcaption>
</figure>

No upgrades yet though, that was the focus on Saturday, as well as getting started on visuals. I got out a pen, some paper, and an old box of colored pencils. The first thing I drew was the mouth, and that informed the rest of the game's design.

<figure>
<img src="{{ '/assets/images/Crumbania/MouthOpen.png' | relative_url }}" alt="The mouth from Crumbania. A mouth, poorly drawn on paper with pen and colored pencil, gaping and ready to eat some crumbs.">
<figcaption>Partially inspired by the cover of In The Court of the Crimson King by King Crimson</figcaption>
</figure>

But in doing some performance testing, I found that when there were a lot of crumbs in play, the game would lag horribly, and it was even worse on the web build. I figured "ah well, I'll just tone the crumbs down a bit". But that problem ate at me the rest of the day. By the end of Saturday, we wind up with something pretty damn close to the final game, even with visuals.

<figure>
<img src="{{ '/assets/images/Crumbania/progress2.gif' | relative_url }}" alt="Early Gameplay of Crumbania. Where previously there were collision shapes, there is now a mouth, a fork, a spoon, and various foods, all poorly drawn in pen and colored pencil.">
<figcaption>The graphics are childish, but charming.</figcaption>
</figure>

On Sunday, I would polish the game up, and get it ready to submit. That was the plan, at least. I got caught up in some tiny polish items, like making the particles have shadows, reorganizing code, and making the main menu look nice. Plus, ideas for solving the performance issues were still bouncing around in my head. By the end of Sunday, I knew I'd have to let this development bleed into Monday a bit, but I told myself I'd finish it by Monday evening.

### The Work, Part 2: The Week
I did not finish the game Monday evening. Instead, I continued to polish the game a bit more, adding the animations for the enemies and the player. But then I did do some necessary stuff, like music and sounds. The sound effects are all foley sounds, very similar to those done for [Moon Viewing](https://advance2112.github.io/blog/games/2024/07/31/Moon-Viewing.html). The music is from [this collection of public domain works](https://tallbeard.itch.io/music-loop-bundle) by [Abstraction](https://www.abstractionmusic.com/). One of the first things I did after the jam started was pick the songs I wanted to use. I went through most of all the music in this collection and picked what I thought fit the vibe of the game best: Drum & Bass music. I really like the two tracks I picked, and after listening to them for hours, I have yet to get tired of them.

Tuesday I spent doing some more polish, like fixing the particle lag by changing them from GPUParticles to CPUParticles (something to do with the Compatibility renderer not liking GPUParticles), fixing some bugs, adding a tutorial and an options menu. By the end of Tuesday, I pretty much knew that the idea of this game being a "weekend game" had long since been thrown out the window. But holy shit... I was having SO much fun making this game. Even the tedious stuff, like menus and UI, I was having a blast doing.

So I kept going. Wednesday, I added a couple of small things, but then I got started on finally solving the performance issues I was seeing. Specifically, I had taken what I call the "naïve" approach to many of the objects in the game. The enemies, player, weapons, crumbs, and the player's "magnet area", are all controlled by an Area2D with a CollisionShape2D. Then they check for either what areas overlap them or when something enters their area, and all is good. I call it naïve not because it's bad, but rather because it is the first approach most people think of. And 90% of the time, the naïve approach is the correct approach, since it's all you need. But this game falls in that other 10%, since there are hundreds of enemies on screen and tens of thousands of crumbs in play.

So how did I get around this? After spending Wednesday and Thursday on it, I can tell you exactly how: [MultimeshInstance2D](https://docs.godotengine.org/en/stable/classes/class_multimeshinstance2d.html). I used these [two](https://www.youtube.com/watch?v=DwMoEdAhtYQ) [tutorials](https://www.youtube.com/watch?v=kKK4yWs3eh4) to stumble my way into something that works reasonably well. I even wrote my first (very simple) shader to make this work, adapting it from both of the shaders shown in the tutorials. The shader simply cuts a sprite out of a sprite sheet based on instance data.

From here, instead of having a bunch of objects floating around with their own _process methods, I have a single object that handles all of them. I have the data for each crumb split into a series of arrays (an array containing the size of each crumb, another containing the color, another containing the value, another containing its rotation, etc.). Then, this "master" object loops through each crumb during its _process method, doing what it needs to for each one (skipping if it's "dead", updating if it's moving, etc.). I also added level of detail (LOD), making further away crumbs do the heavy calculations less often.

After all of this, I finally managed to get the performance to be reasonable. Except for in the web build. It was definitely better than before, but the web version just couldn't keep up. I looked into it and, for one, I changed from doing a debug build to doing a release build (an option that only shows up in the file explorer as you're choosing where to export??). That helped a bit. But looking into it some more... yeah, the web platform just has too much overhead to really be able to squeeze a ton of performance out of it. At this point I had to concede, and just not commit to a web build. I would revisit this once I had the native builds working and finished.

### The Work, Part 3: The End
<figure>
<img src="{{ '/assets/images/Crumbania/progress3.gif' | relative_url }}" alt="Gameplay of the jam version Crumbania. Some assets have changed slightly, and there are now particles when enemies are killed. The UI all has the appearance of paper, and the enemies and mouth wiggle around as they move.">
<figcaption>Gameplay from the jam version. It really is Vampire Survivors.</figcaption>
</figure>

Friday and Saturday, I polished the game up some more. From balancing (which was surprisingly boring to do), to making the menus look like paper, to making a handwritten font with [Calligraphr](https://www.calligraphr.com/), to adding some juice here and there, it all felt very natural at this point. By that I mean that it was getting really easy to slip into "flow state" while working on this game. It was intense, and fun, a bit stressful, but good stressful.

I tested what I could of the native builds on a few different machines of varying computing power, and was happy with performance overall. I finally had some close family play the game to get some feedback, and they loved it, which felt great to hear. By Sunday, I did manage to get some time to work on a "performance mode" for the web build. I also added a warning/thank you message at the start for the different versions, the web version stating that it is not the intended experience of the game. I finished the game about 3 and a half hours before the end of the jam, and submitted.

### The Play
193 games were submitted to this jam. By far the biggest GWJ I had ever participated in and the biggest jam I've been in since the [Pirate Software 15 Jam](https://advance2112.github.io/blog/games/2024/07/31/Moon-Viewing.html). I started playing some games and damn... there were a lot of great games. [Dopamine Dash](https://ace-of-4s.itch.io/dopamine-dash), [It Came From Below](https://sixthgear.itch.io/below), [Eat Everything](https://chickwich.itch.io/eat-it), [Paravore](https://exonaut.itch.io/paravore), and, my personal favorite of the jam, [Canvas Variations](https://dominicwillismusic.itch.io/canvas-variations). 

I was getting a lot of great feedback as well, many people saying they... what's this? They... like the art? What? That shit that an 8-year-old could draw? But for real, a lot of people were impressed by the dedication to the paper style. I would say that Crumbania getting #8 in graphics is a bit high, though, especially when [The Feed](https://systemeffect.itch.io/the-feed) and [Candil](https://chusgames.itch.io/candil) are in the running. Of course, Crumbania is rather derivative of Vampire Survivors, and a lot of the criticism I got for the game was either criticizing the fact that it's a clone of Vampire Survivors, or was a criticism of a gameplay element stolen directly from Vampire Survivors. I suppose that comes with the territory of cloning a game, though: you clone its problems, too.

As I was rating other games (I managed to rate 60), I remember being obsessed with the thought of "is this game better or worse than mine", which is such a toxic thought. I like to think that I don't approach a jam as a competition, but rather as an opportunity to learn and grow and participate in a community and gush about other people's cool games. I mean, it is a competition, there is a winner, even though they win basically nothing in this jam (a golden discord username... for a month). I don't want to think of it as a competition, but with it being set up like one, I can't help but think of it that way. 

I remember being a bit bitter about It Came From Below, since it was the first game I came across that I thought was clearly better than my own. More people were interested in it, more people were rating it, and more people were leaving positive comments. This should be something to celebrate, I should be happy for them, but I wasn't. It brings me back to what I was feeling and thinking while making [SUFFER.er](https://advance2112.github.io/blog/games/2024/10/20/SUFFER-er.html), that idea of seeking validation from others, but it's twisted even more into this toxic knot of ideas: "I need to be the MOST validated, or else it doesn't count." I calmed down as the rating period went on, recognizing the thoughts and rejecting them as best I could. But in the moments leading up to the results, I was on edge, certain I was in the running to win the jam. And to be fair, I was in the running, a lot of people liked my game... but I was consumed by the thought, I couldn't help it. I wound up getting 6th overall. Percentage-wise, that's the highest I've ever ranked in a jam, top 3%.

### The Work, Part 4: The Long Update
I had previously done post-jam updates for all but one of my games, and I felt that Crumbania deserved one as well. With it being my highest rated game, yet still having issues in my eyes, I decided to take a crack at it.

First thing I did was add an option to remove the mouth sounds, replacing them with vox sound effects. I considered doing this during the jam, but never got around to it. After someone left a comment mentioning the mouth sounds made them uncomfortable, I figured this was necessary.

Next was additional input method support, including mouse controls and controller controls. Well, at least for gameplay, I came back and worked on controller support for the menus later, which is such a big pain in the ass in Godot for no good reason.

I added option saving, so the game doesn't clear your options every time you load it. It was [surprisingly easy to do](https://docs.godotengine.org/en/stable/classes/class_configfile.html), so I'll probably do that for all my future games. I changed the way crumb spawning works so it culls older ones when there are too many (previously they would just stop spawning). I fixed an issue where the mouse cursor would lag behind the camera. And a number of other small tweaks like that.

The biggest thing I wanted to do, however, was rebalance the game. There was a very clear "best" strategy in the jam version: use the knife, ignore the spoon and fork. I wanted to buff all three while making each one a viable "main" weapon, so I added some new upgrades that I think achieve that reasonably well. The spoon is still the worst, but you can still make it to level 50 with it as your main weapon.

Another big (and probably unnecessary) change was to update the UI. I didn't like the look of the stretched color pencil marks on the buttons, so I figured I would redraw them to be wider. I also redrew a few other things... and doubled the number of enemy sprites. Unfortunately I had to go back and re-scan and crop a lot of these, since my scanner settings were wrong the first time. I was really frustrated by that, and almost went with the darker versions of these sprites just to avoid that effort, but I'm glad I took the time, I think everything looks as it should.

<figure>
<img src="{{ '/assets/images/Crumbania/progress4.gif' | relative_url }}" alt="Gameplay of the final version of Crumbania. Some elements have been updated to have more contrast, the player and enemies move faster, and a few new upgrades are shown.">
<figcaption>I also sped up the player and enemies a bit, based on some feedback.</figcaption>
</figure>

As smooth as all this work sounds, I had a lot of shit going on in my personal life at the time. I won't go into it all here, but just to give you an idea, I planned on finishing this update before the start of the next GWJ on August 8th, this blogpost included. I didn't wind up finishing until the END of that GWJ, on August 17th. Needless to say, I didn't participate in GWJ #84, but I am itching to make another game soon.

### The Lessons

1. Good art isn't just about being competent, it's also about being consistent.

   This was really powerful for me. I always felt defeated by my ability to do visual art, but somehow I stumbled into something that worked really well. Would I do it again in the same way? Probably not. But at least now I know I'm capable of making decent art.

2. Using pre-made assets is a superpower.

   I don't know what I would have done without that music from Abstraction. The songs are great, and they fit in the game so well, it's honestly a miracle. I think I might start doing this more, especially if I'm working alone.

3. I don't need to do post-jam updates for every game.

   If I knew it would take nearly a month, I wouldn't have done a post-jam update for this game. And sometimes, especially for a game like Crumbania that doesn't have any major glaring issues, I would say that it isn't really necessary. I'm not saying I'll never do one again, I do like that they let me uncover quick things I could have found time for during a jam (such as saving options and mouse controls) and practice things that take longer (like controller support). But some games just don't need them.

4. I love making video games, but I'm over the idea of making money from them.

   This is a hobby, and after my experience with Hemocoven and getting burnt out there, I'm ready to draw the line in the sand. No more long projects, no more monetized projects, at least not until it feels right. If I make a game for a jam that I want to turn into something bigger, that's great, and I'll keep that idea open. But for the time being, this is a hobby, and it is not something I ever expect to make money on.

5. I have to stop taking things so damn seriously.

   Crumbania is a goofy silly stupid little game, and I love that. I need to make more of these goofy silly stupid kinds of games. Additionally, I need to stop taking ratings and rankings so seriously. Yes it's a "competition", but it doesn't matter who wins. Everyone who submitted a game is a winner in some way, since they finished the thing they set out to do, which for something like a video game, is an amazing accomplishment.

### What's Next?
After such a long development time and still quite a busy personal life, I think I'm going to take a bit of time off. Not too long though. I've got some great momentum, and I want to keep that up. Another jam in September? Possibly.