---
layout: single
title:  "Post-jam Update: Lapis and Rhubarb: The Orb of Doom"
date:   2024-11-30 03:52:00 -0500
last_modified_at: 2024-12-03 18:00:00 -0500
header:
    image: "/assets/images/lartood/lartoodCoverThin2.png"
categories: games
---

Let's keep the magic going.

Art by [ƒ(Dis)](https://x.com/dicksuction).

---

[**Lapis and Rhubarb: The Orb of Doom**](https://lyon-mistwalker.itch.io/the-orb-of-doom) was made in about 8 days for the [Godot Wild Jam #75](https://itch.io/jam/godot-wild-jam-75). You can read about my experience making the game [here](https://advance2112.github.io/blog/games/2024/11/17/LaRtOoD.html).

### The Beginning
After the jam had ended but before ratings were out, the team kept in touch and discussed people's reactions and feedback about the game. I started keeping a list of all the potential improvements, some more obvious than others. I spent the first few days of the rating period rating games, I wound up rating over 2/3rds of the submissions. But once that was done, I set out to make some improvements to the game.

### The UI
One of my biggest gripes with the final game was the UI. Not that Lyon, our UI programmer and designer, did a bad job. It was his first time managing all the UI for a game, so I have to give him a break there. He did what he could. And even then, a lot of the UI problems were in parts of the UI I implemented, like the status UI in game, which we found could obstruct some enemies.

One thing I spent a good amount of time on was the experience of opening the game. There are some limitations with how that can work with Godot web builds, but I think I made it pretty smooth all things said and done. I also timed the splash screen logos with Gopher's opening piece, or at least tried to. And one of my favorite changes was with the main menu, adding a slow spin to the magic circle and enhancing one of my already favorite things about the game.

<figure>
<img src="{{ '/assets/images/lartood/update/CoverAnimated.gif' | relative_url }}" alt="The key art Lapis and Rhubarb: The Orb of Doom. Lapis and Rhubarb or positioned in the upper left and lower right respectively, each holding their arms out as if they are shooting their magic bullets. The Orb of Doom rests between them, energy escaping from it in sparks. The two layers of the magic circle rest behind them and rotate slowly in opposite directions. The corner behind each girl is colored with cyan for Lapis, and red for Rhubarb.">
<figcaption>Lapis and Rhubarb: The Orb of Doom: now with 200% more spinning! (Art by <a href="https://x.com/dicksuction">ƒ(Dis)</a>)</figcaption>
</figure>

We also had a ton of problems with the font in the web build. The issues we had were reminiscent of the issues I had with [The Tower of Babel](https://advance2112.github.io/blog/games/2024/09/22/The-Tower-of-Babel.html)'s font not appearing correctly. In this case, we decided to get a new font for the whole game. The new font is a Google font, [DynaPuff](https://fonts.google.com/specimen/DynaPuff), and it is excellent.

The tutorial was completely reworked, now pausing player input during certain text boxes and explaining some things more clearly. The controls menu was completely redone as well. The size and padding of the UI was standardized, we added new custom UI elements like dropdowns and checkboxes. A bunch of tiny little polish things like this were sprinkled throughout and I absolutely love it. It feels like a real game's menus for once!

### Accessibility
Accessibility is something I haven't focused on too much with previous games. This is despite [SUFFER.er](https://advance2112.github.io/blog/games/2024/10/20/SUFFER-er.html) getting 1st place in accessibility. Personally, I think one can go too far with accessibility, and it can compromise the intended experience of a game. However, one of our team members mentioned that they have "eye problems", and struggle with games that have too much motion in them. So this time around, I had a vested interest in making the game more accessible.

The most apparent bits of accessibility we made were a colorblind mode and an option to reduce motion. The reduce motion option is relatively straightforward. Many of the large, moving objects in the game were controlled by scripts already, so the scripts simply stop doing anything if the option is turned on.

Colorblind mode was a bit more of a challenge, and I'm still not sure if we got it right. We added symbols to each girl's back that represent their elements. Then the orb, instead of just changing colors, changes which symbol appears on it.

<figure>
<img src="{{ '/assets/images/lartood/update/colorblindMode.gif' | relative_url }}" alt="A zoomed-in shot of gameplay of Lapis and Rhubarb: The Orb of Doom. The girls move around the central ring and shoot at all the bad guys. The orb bounces around in the center, changing which symbol appears on it after certain bounces.">
<figcaption>Colorblind mode in action.</figcaption>
</figure>

Some less obvious changes include new keyboard controls, correct prompts for the special moves when using said keyboard controls, and mobile controls. Mobile controls were relatively quick, being done almost entirely within a day. Lyon had found a simple touch joystick plugin and that was pretty straightforward to integrate. The only thing that was a bit annoying about them was getting them to only show up when they are wanted, but I figured it out.

### The Polish and the Juice
This stuff was really fun. It started small, adding y-sorting to the girls so Rhubarb isn't always overlapping Lapis. Then adding a bit of a subtle float animation to each girl. Then adding menus and animations for the fail and win state. A parallax effect on the whole game. The magic circle now reacts to your health and your combo and taking damage. A bunch of these tiny little enhancements to the gameplay that make it such a joy to play now. I need to find time to do this kind of stuff to all my games now, because it's relatively easy to do and adds to the feel so much.

<figure>
<img src="{{ '/assets/images/lartood/update/juice.gif' | relative_url }}" alt="Gameplay of Lapis and Rhubarb: The Orb of Doom. The girls move around the central ring and shoot at all the bad guys. The orb bounces around in the center. The center of the game appears to move around gently as the girls move. Every time an enemy reached the center, the screen shakes and the magic circle spins a bit faster for a second, then slows down">
<figcaption>Look at that JUICE.</figcaption>
</figure>

### The Gameplay
The gameplay received only minor tweaks, the biggest one being making the projectiles slightly larger. We did this to help deemphasize aiming which is, frankly, very bad and difficult on anything other than a controller. The gameplay was, as far as I'm concerned, perfectly fine in the jam version, and I believe we preserved that.

### Endless Mode
We discussed doing an endless mode many times. It's something I would like to play, honestly. But I'm not sure if I'd like to make it. Endless mode would require a bunch of new systems and tweaks for the game, something I just didn't have the patience for at the time. If there is significant interest (and I doubt there will be), then I will humor making an endless mode. But for now, the campaign is all there is.

### The End
At the time of writing, the game has been played maybe 2 dozen times since the post-jam update was released. And a third of those were probably me. But that's not what this update was about. It was about doing the polish and making the features we wish we had time for during the jam. It's about learning about how to do these things for future games. And it's about being motivated to do something for no reason other than wanting it to be done. And I think we accomplished all of these things with this update.

### What's Next?
This blog is what's next, I resumed writing it the day after finishing this update. But as far as the next game, I think I'll be doing something a bit different this time. The plan is to take a break from jams, at least for the month of December, maybe January as well. I plan to take this time to make an idea I've had since June, just to get it out of my head. Shocker: it's a card game. From there, if I like the game, I may spend some more time with it. Then I might be looking at a larger project, but that's yet to be determined. We'll have to see how the cards are dealt.