---
layout: page
title:  "more FinuxOS"
permalink: /more-finuxos/
---
# Turning “boring & mundane” into “tense & engaging”
I worked with the team to brainstorm a list of everyday office tasks that we could do a creative spin on for the minigames, as well as an interview with my dad who worked white collar office work.

The common consensus, however, was that **office jobs were boring** and slamming a bunch of boring tasks under a time limit doesn’t necessarily make for effective tension. They needed to be **engaging** first.

A task I’d like to highlight as a good example of that “creative spin” was **emptying the recycle bin.**

![Image](/images/FinuxOS/recycle.gif)

I took quite the literal approach to reimagining the task. I thought “what if you were actually taking out the recycling / garbage on your computer? What would that look like?” 

The cars add an immediate sense of danger, and the player now suddenly being in control of a character in danger adds a lot of immediate tension, all while being put under the pressure of a looming time limit. I’ve gotten a lot of laughs out of people when they first open this task, as well as a lot of yelps from being hit by cars.

# FinuxOS: A Fictional Operating System

When I first came up with the idea for the project, I knew that I wanted to have some sort of “gimmick” for the working simulator genre. That gimmick became **multitasking.**

I had a certain playstyle in mind where the player would have multiple tasks open at once, fully optimizing their fantasy as a white-collar wage slave. 

Ok but, *how* exactly can multitasking be implemented? With a virtual operating system of course!

![Image](/images/FinuxOS/fictionalOS.gif)

The window system was mainly implemented using UnityUI, there’s a lot of support for doing draggable windows with UI elements already baked into UnityUI. 

The main challenge, however, was “focusing” on windows. Keyboard inputs would affect other windows, dragging one window could indirectly be calculated as an input for another, and I found myself doing a lot of reading about how they tackled this problem back in the 90’s.

I created a system that handled all of the windows, just like an operating system. You couldn’t open a window without talking to this system, or close a window, and it would store all of the currently open windows to prevent misinputs from happening. Whenever you clicked on a window, it would focus that window and all inputs from all other windows would be disabled.

With multitasking implemented, it left room for another axis I wanted to explore with this multitasking fantasy. I wanted to tell a story that could only be told within a fictional operating system.

A fictional operating system? What narrative possibilities could that open up to the player? 

The player is constantly under surveillance by a “big brother” kind of system that is grading them on their performance. The virtual desktop allowed the immersion of this to be explored even further. I really wanted it to feel like you were being watched.

![Image](/images/FinuxOS/instructFin.png)
