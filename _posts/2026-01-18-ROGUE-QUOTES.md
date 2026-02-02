---
layout: single
title:  "ROGUE QUOTES"
date:   2026-01-18 15:25:00 -0500
last_modified_at: 2026-02-02 14:38:00 -0500
header:
    image: "/assets/images/ROGUEQUOTES/titlestripanimated.gif"
categories: games
---

A scrabble-like-rogue-like-game-like thing.

---

[**ROGUE QUOTES**](https://advance2112.itch.io/roguequotes) was made in 9 days for the [Godot Wild Jam #89](https://itch.io/jam/godot-wild-jam-89). The Jam's theme was "Repurposed".

### The Jam
The last 6 months have been rather eventful, and I've been feeling good about the pace I've been making games, despite everything. [Incremental Decay](https://advance2112.github.io/blog/games/2025/11/23/Incremental-Decay.html), in some ways, was refreshing. Sobering. It was a bad game, I'll admit it. Well-balanced, but lacking in nearly every other domain.

Needless to say, I was itching to do something kind of the opposite of Incremental Decay. Where it focused on gameplay, my next game would not. Where it lacked in juice, my next game would not. I wanted to challenge myself to make something really satisfying to interact with, even if the gameplay was simple, or even bad.

So, with December being busy with holidays, I waited until January to do the next GWJ.

### The Theme
"Repurposed" is pretty mild as themes go. While there are lots of ways something can be repurposed, many of those things are described better by a different word. Recycling comes to mind, in particular "upcycling". But, also just reusing things in general. Reselling, retooling, rewiring, rewriting, etc. It's fine, but a little too broad, if you ask me. I think "recycled" would have been a better theme.

### The Plan
I actually had a ton of ideas for this jam. At first, I was focused on a plastic recycling factory game, like [Factorio](https://store.steampowered.com/app/427520/Factorio/). Then something a bit simpler, like an idle game where you collect and grind up plastic. Perhaps you could just sort trash, and pick out the things that can be reused/recycled/resold? Or what about a game where you reclaim the land that was once used for a landfill? Uh... a rogue-like deck builder where you repurpose old board game pieces and a ripped up deck of cards?

None of these were really sticking in my mind. They all seemed either too complex to do in in the time given, or didn't have enough opportunity for juice. However, there was one I wrote down: "reusing letters to spell something". But letters from what? What has letters?

Thus the idea was born: take the letters from a famous quote, and "repurpose" them into new words. It would be like Scrabble and [Balatro](https://store.steampowered.com/app/2379780/Balatro/), and each letter would be worth some amount of points, and they would score individually, and... you get the picture. It's perfect. It's gameplay light, relatively simple to make, and there is tons of opportunity for juice.

### The Work
I started with something I knew would be a challenge for a word-entry/typing game: gathering a list of valid English words. I used [this list](https://github.com/dwyl/english-words), and filtered profanity with [this list](https://huggingface.co/datasets/PeterGraebner/LDNOOBW_V2). I later found out that this profanity list is a bit too aggressive, filtering words like "lop" and "food", so I wound up having to revise the list manually and take out many of these actually safe words.

From here, I made a simple word entry system, just a TextEdit and checking if the word is in the word list. Then I added the quote system, a display for the quote, plus a keyboard display that tells you how many of each letter is left. And, of course, I got started on the juice, making each letter do a little animation as it scores. It still looked very plain at the time, but the bones of the final game were already there by Monday night.

<figure>
<img src="{{ '/assets/images/ROGUEQUOTES/gameplay3.gif' | relative_url }}" alt="The word &quot;POLLUTION&quot; is typed into a TextEdit, and the keyboard below it has each letter count decrement as the word is typed. There is a quote by Max Planck at the top. The player enters the word, and a display of each letter appears and scores with a &quot;+1&quot; or &quot;+3&quot; depending on the point value of the letter.">
<figcaption>Balatro who?</figcaption>
</figure>

I think it was around this time that I started getting some conflicting feelings. On the one hand, I was sure I was definitely going to finish this game, no matter what. That point of no return had been reached, and not all projects reach that point. But, on the other hand, I felt that I knew this game was not going to be very interesting from a gameplay perspective. I more or less had the final gameplay finished already, and, I won't lie, it wasn't very fun. The main gameplay loop is just: "Think of a long word. Don't have enough letters for it? Try a different long word." It's more of a vocabulary test than anything tricky.

Either way, since I knew I was likely to finish the game, I decided to double down on that fact and get someone else involved. I reached out to my long-time collaborator and friend [Quenched Disorder](https://quencheddisorder.itch.io/) and asked him to make a track for this game, to which he graciously agreed.

I plugged away at the game, deciding that it was time to really get the juice flowing. I reused some code and some lessons learned from a previous project, an unreleased game I started working on nearly a year prior, to make the letter tiles more responsive. They now jiggle and shake and fly across the screen in a satisfying way.

<figure>
<img src="{{ '/assets/images/ROGUEQUOTES/gameplay1.gif' | relative_url }}" alt="Very similar to the first GIF, but now instead of a TextEdit, typed letters fly up from the keyboard to their place in the word. The word &quot;QUEEN&quot; is typed, entered, and scored. Other gibberish words are typed to demonstrate the functionality. The quote is now one by Winston Churchill.">
<figcaption>Scrabble who?</figcaption>
</figure>

Then I started on sound effects. Just as with previous games for which I've done sound effects, I went with foley sounds. Poker chips, a glass of water, a hand fart, a water bottle, and kitchen utensils make up all the sounds in the game. As fun as recording the sounds was, I'm realizing that one of my least favorite things to do during a jam is the post-processing on sounds, in particular, isolating each sound from the recording. But, I got it done, and put them in the game, reusing the sound effects code I wrote for [Crumbania](https://advance2112.github.io/blog/games/2025/08/17/Crumbania-and-pju.html).

Despite having a bit over 48 hours left in the jam at this point, I finally got started on actually making the game, you know, a game. I added a round system, a failure state, and items. I took inspiration for the item framework from [this video](https://www.youtube.com/watch?v=vADoiFE_Zvc) (source in the description) and implemented that. I also added the [Balatro paint swirl effect](https://godotshaders.com/shader/balatro-paint-mix/) to the background, and tweaked some settings to make it look at least somewhat distinct from Balatro.


It was at this point that I realized how much of a mess my code was, considering that this item code is some of the "cleanest" in the game. There are lots of things referencing things in ways that they probably shouldn't. This culminated in me having to migrate the entire GameManager script from being a global singleton to being attached to the game scene, which was a big pain. But, once it was done, it made adding a main menu trivial, since I just had to do a simple scene switch. I also finally tested the web build around this time and... yeah it was broken, it wasn't reading the word data correctly. So, I put in a quick workaround there (just made the words defined in their own GDScript global).

It's now the morning of the final day, just 6 short hours left in the jam, time to finish this out. Quenched Disorder sends [the final track](https://soundcloud.com/quenched-disorder/illumination), and it's excellent, no notes, so I slap it in the game, big thanks to him! I make the items look a little nicer. I add a display for the timer. I add backspace and enter buttons on the on-screen keyboard. I add volume sliders. I make the main menu. I add a difficulty selection. I enhance the point counting. And, finally, I add a win condition. I put the final build up just a little bit late, but I got permission from one of the mods to do so.

<figure>
<img src="{{ '/assets/images/ROGUEQUOTES/gameplay4.gif' | relative_url }}" alt="Starts on the main menu, which reads &quot;ROGUE QUOTES&quot; and has three difficulty options. The player selects &quot;Normal&quot; and starts playing, typing &quot;WESTERNER&quot;, &quot;LIMINAL&quot;, and &quot;TEETHE&quot;. There is a swirling purple and white background. The letter tiles slide around the screen satisfyingly. There is a timer counting down. The quote is the famous &quot;I have a dream...&quot; quote from Martin Luther King Jr.">
<figcaption>Scrabble who?</figcaption>
</figure>

### The Results
There were 116 games submitted, and I played 17 of them. [Ransom Noter](https://sl1ngshot.itch.io/ransom-noter) was a blast, but lacked any kind of "quality check" to see if you were playing the game "correctly". [Colony of Theseus](https://the-dev-dave.itch.io/colony-of-theseus), while flawed in many ways, I instantly clocked as using the same pixel planet generator that I used for [Project: Kardashev](https://advance2112.github.io/blog/games/2025/09/21/Project-Kardashev.html). [STROBE](https://offbytwodev.itch.io/strobe) had excellent vibes, [Fiora il Procione](https://senzameta.itch.io/fiora-il-procione) was beautiful but I had no idea what was going on, and [They Climb](https://hatmix.itch.io/gwj-89) was beautiful AND had great vibes, and went on to win the jam. My favorite, and shockingly underrated, was [Kleptoglob](https://fishynator.itch.io/kleptoglob).

As for ROGUE QUOTES' feedback, it was all rather positive, with a few expected gripes. Many people noted that the quotes don't really affect the gameplay all that much, one person saying "It's easy to pass through the levels without reading the initial quote." I expected this, as mentioned earlier. But, on the other hand, many people praised the look and feel of the game, which was appreciated. Some were confused about the rules of the game, some called for more varied items or changes to the rules, and one person even begged me to keep working on the game! I wound up getting 9th place overall, with 2nd in both Controls and Fun, and 7th in Accessibility. Theme and Originality dragged the score down, though, get 48th in both. I'm very happy with the reception, but I have no interest in working on this game any further. So, I won't.

### The Lessons

1. My suspicions were right; game-feel trumps gameplay.

   Of course, this isn't always true, but it is a good rule of thumb. The gameplay here is, in fact, pretty mediocre, a bit confusing, and overall only fun for a few minutes. But it looks and sounds pretty good, and that is what drew people in and kept them playing.


1. I could make a Balatro clone if I wanted to.

   This game is very much in the spirit of Balatro, which, if I haven't said, is one of my favorite games of all time. Making ROGUE QUOTES has made me realize that, yeah, I could make a game like Balatro if I really wanted to, and I even tried to once before! I might give it another shot one day.

### What's Next?
I don't really know what's next. I have some non-game things I've been itching to do, and I might write about them here, or I might not. Plus, there may or may not be some secret projects in the works at the moment. If those ever see the light of day, I'll be sure to write about them here.