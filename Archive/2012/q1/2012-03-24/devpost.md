Rain World is a sneaker/action platformer under construction.

[header.jpg]
[lizardfight.gif]

Video!


The gameplay consists of platforming and fast paced sneaking, both sneaking on your prey and sneaking in order to avoid larger creatures. A lot of focus in the development has been on enemy AI.

The player character moves a little differently from in most 2D platformers, it is not animated by traditional means but with simple physics. This is an attempt to make a character that appears a little softer, as well as an experiment with a different control scheme.



Alongside the game I'm also working on a level editor, which will allow you to make your own levels and render their graphics. Right now both game and level editor are unfinished, but it's likely that the game will be released before the level editor.

The level editor uses a voxel-like method to create graphics, and does some basic raytracing for light. If you go to the newer pages you'll see a lot of level editor related progress.

[levelsnip.png]

Everything, including the title, is subject to change, but the project is much more defined now than when this thread was started! Below is the original post from some time ago, if you want to follow the progress of the project from the start.

I post updates more or less every day, and am making slow but steady progress.


If you find the project interesting, please feel free to ask, suggest, comment or otherwise contribute.
Thanks for your time!

----------------------

Hi! Maze Runner is of course a working title.

A while ago I posted a movement prototype in the feedback section. Since then I have worked some more on the project, starting to turn it into a game.

I haven't started on the visuals yet, and the game will probably look very different from this screen shot, but the movement of the player will be mostly the same.

I decided to start a dev log to keep track of my progress and keep myself motivated. I work at the game at a low but steady pace, and will hopefully be able to post updates every so often.

## The Game
Try out the prototype to get a feel for what kind of basic mechanics I'm working with. More on that to be found in the old thread. More moves are to be added, such as balancing on poles, maybe some gripping mechanics, stuff like that. The core of the game is the movement of the player character in the environment.

The game will have three types of creatures in it. I won't go in to detail on how I plan to design them visually, that's not entirely worked out yet and will hopefully be an exciting surprise. Together the creatures will form a little eco system, where creature B eats creature A and creature C eats creature B. B, the player, is in the middle of this food chain, and the gameplay will consist of trying to hunt while at the same time avoiding to be eaten.

A is a flying creature, that can move quickly and reach every part of the map.

B, let's call it "the Bear" because of its ears, is a running and jumping creature, with medium mobility and probably also access to most of the map, as maps will be designed mainly from this creature's perspective. This is the player avatar in the game world.

C, let's call it "the Croc" is a crawling, climbing creature that can't jump, and is somewhat less mobile than the bear. This one will come in a few sub-species, some of which will be capable of wall climbing, increasing access the different areas of the map. They will have different stats and abilities and be threatening in different ways.

The game will work with one or more players sitting at the same computer. I like 2D, single screen multiplayer games as they according to me have all the feats of a board game as well as those of a computer game. The players have complete overview of the play area, and can shout stuff at each other while interacting in the game world. However I felt that my last game lost a bit of its potential audience due to being multiplayer only, so this one will be playable alone as well. The players will be playing against the computer units, but some competive elements might be doable as well.

## The level editor
I love level editors, and especially did when I was a kid and couldn't really make actual games myself. I've been doing some work on the level editor already, and it seems to be coming together nicely.



It's fun to make and play levels together with friends, and I've made the level editor so that two or more people will be able to work at the same level simultaneously.

## What's going on right now?
AI, AI and more AI... path finding, to be specific.

To be even more specific, it's the path finding of unit C that's a hassle. Thing is, C is not supposed to be able to reverse. Unless it's really stuck it should move forward, trying to find a way that doesn't require moving backwards into its own body. As anyone who has worked with an A* knows the main thing is crossing out tiles, like "OK, this one is checked, now I don't have to think about it again". But, if this unit is moving to a target behind it, it has to start moving away from the target until it finds a turning place, and then move back over the same tiles towards its target.

This is difficult, especially as even a conventional A* can be a sort of complicated matter... And yeah, both the start and goal positions are constantly moving and I can't afford to calculate the entire path in one frame, so it has to be realtime... And different crocs have access to different tiles... This has been, and is, very very hard. However, I'm starting to see the light at the end of the tunnel, which is why I'm going online with this now. Hopefully from now on every single update won't be about croc path finding, as it would if I started two weeks ago.

The combination of giving the user access to a level editor and having autonomous units moving around in the environments is an interesting challange. I don't want the user to be required to place "flags" of any sort, you're supposed to be able to simply create a level and then have the units move around in it in a sensible way. Moving around without reversing, that is... Well, enough on that.

The development so far has been very technical, and will probably continue to be for a while, but I'm originally an art guy and I'm much looking forward to creating some juicy sounds and visuals for this.

I hope you find the project interesting, and am looking forward to your comments, suggestions and questions.
Thanks for your time!