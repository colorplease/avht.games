---
layout: page
title:  "more SORRY, SORRY, SORRY"
permalink: /more-sorry-sorry-sorry/
---
# Designing for Your Past Self
A problem I quickly faced while designing this game was that **It's actually really hard to balance a game that operates on a different time axis.** As in, creating items that played nicely with the time mechanic *as well as* being a strategic platforming was incredibly difficult. 

This meant, we needed lots and lots and lots and lots and lots and lots and lots of **iterative playtesting** and **user feedback**.

The two items I’ll talk about here will be the **glock** and the **bomb.** 

Let’s see how they both evolved in our playtests.

![Image](/avht.games/images/SORRY,SORRY,SORRY/sorryplaytest1-ezgif.com-cut.gif)

The glock is a basic turret. It shoots whichever player is closer to it. In its first iteration, the glock had infinite range and could see players through walls. 

This was *supposed* to incentivize players to be very careful where they placed it. It could easily harm themselves as much as their opponent, so I tried to make an item that was very strong so that players could naturally learn what good positioning was when building stages, as well as using some of their own lives to block it. 

Yeah that just didn’t go as planned. You can see what players did with the glock up there, they would just stack them to make it as lethal as possible. This would make ending games *impossible* so something clearly had to change by the next iteration.

![Image](/avht.games/images/SORRY,SORRY,SORRY/sorryplaytest2.gif)

The glock now has a detection range! And a laser!! No more tracking through walls, no more cross map snipes, no more…oh hold on.

The glock’s firing timer didn’t reset if you left the detection range, so there would be these nightmare cases where you’d be shot either instantly or not at all. Plus, we still have that pesky problem of players making impossible death traps that keep games in stasis.

Not only did the glocks need another nerf, we also needed some way to affect the level state during gameplay. There has to be some more counterplay to these inescapable death traps.

So during one of the post-playtest-surveys, one of my playtesters came up with a lovely idea. 

“Why not a bomb?”

![Image](/avht.games/images/SORRY,SORRY,SORRY/sorryplaytest3.gif)

The bomb, when touched by a player or clone, detonates after a brief period, destroying any other item close to it.

This worked ***amazingly*** for this playtest. What would normally be a SAW III trap has now turned into a much more strategic question of “how can pop the bomb to make it to the end?” It causes players to sacrifice lives solely to try to detonate it, and when they get a successful run, they can begin to think of other paths to victory now that they can affect the terrain of the level.

The past was now an axis that players could actually use to their advantage, and *that* was the game I set out to create.

This game was such a blast to balance and playtest, and I think the game would’ve been impossible to balance without my lovely playtesters. 

# Programming Your Past Self

Replay systems are hard. VALORANT took nearly 5000 years to implement theirs, so how could I implement a replay system that could handle *hundreds* of instances all running at once?

![Image](/avht.games/images/SORRY,SORRY,SORRY/imNOThavingfun.gif)

Initially, I thought that recording the **position* for every life was a good idea. It really, really, really wasn’t. It would  bug out really bad because the PlayerController uses Rigidbodies rather than affecting the Transform itself. 

In simple terms, sometimes the recordings would phase through objects. Really takes out a lot of the strategy, no?

![Image](/avht.games/images/SORRY,SORRY,SORRY/imhavingfun.gif)

So, I ended up taking the route most games do. Instead of actually recording *the position* of the player, the game would record only the inputs of each life. It would then playback those inputs using the same PlayerController that the players would use, like a ghost connecting another controller and just mimicking the moves of yesterday.
