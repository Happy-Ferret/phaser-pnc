Phaser Adventure Game Plugin Design Document
============================================
Introduction
------------
Plugin to simplify development of traditional point and click adventure games, in the style of Lucasarts, Sierra, etc, in the Phaser/Lazer framework.

[From this thread on HTML5 Game Devs forum](http://www.html5gamedevs.com/topic/3612-anyone-working-on-a-point-and-click-adventure)

Design Considerations
---------------------
Features typical (but not necessarily definitive) of game style:

Static 2D backgrounds (‘screens’) with some interactive objects and characters that can move around
Mouse driven gameplay with the protagonist moving to where the player clicks
Inventory
Item combination
Multiple actions (‘verbs’) that can be used to do different things to the same object (less common in modern games so should be an optional feature)
Multiple choice dialog system with character subtitles

Technical Considerations
------------------------
Level editor (not tile based?)
Pathfinding over a static background - collision masks or predefined waypoint routes?
Layered backgrounds allowing for foreground objects
Save/Load system
Event triggers to allow for progression - eg having x item enables y dialog option, y dialog option causes person z to arrive in the game
Character animation system
Dialog system should be heavily abstracted from the general dev process for ease of writing- maybe even just supplying json files generated by some external tool? While still allowing fine grained programmer control
Music system
Modular design? Don’t want to restrict people to using eg requirejs but feel that the components of the plugin should use a module pattern of some description
Sod it let’s just make a JS SCUMM clone. Though somebody’s probably already done it!

Constraints
-----------
Memory, especially if targeting mobile devices - lots of background images and frame by frame animations = need to be careful with memory usage. Can make use of Phaser’s state system to mitigate this.
Voice acting? HTML5 sound support is getting much better but could it handle a lengthy game fully voice acted? This is a long way off as I doubt anyone would try this any time soon ;)

Goals
-----
A flexible enough plugin that it can be used by experienced programmers and novices alike - sort of how Twine can be used in a fully graphical way or scripted entirely by hand using Twee
Ideally allow for art, writing and coding to be as easy to integrate as possible while remaining separate processes
Open source, open licensed, go nuts with it

Development Methods
-------------------
I dunno, <del>get a github started and</del> just do it, we’ll work out how later
