## Welcome to MIX reality group 


### Week 1 - Week 2

Introduction to the course and a quick walkthrough on how vofuria works in unity.
Managed to get a linerendere to reflect a beam once.

Progress was made we now have a fully working prototype showing the idea working.
We corrected a bug that made extra lines in the line rendere by incrementing the amount of lines allowed to be drawed per frame.
(Even under shitty lightning) 
We have set up image targets to add a laser and two walls. Each wall is set up as being a mirror. When the laser collides with the wall, the laser is reflected according to the angle of the laser impacting the wall.

During this week’s course in MIX, we experimented with another augmented reality game which was 'brick breaker'. But, we also tried to improve upon the product we already had which was the laser game. We got the reflection of lasers to work, and now we had to make use of this functionality and make a game out of it. We experimented with a sort of labyrinth, where the player would need to place the mirrors so that the laser would hit a goal to win the game. The player would have a limited amount of place able mirrors and the laser would be placed statically on the map. The goal would also be placed statically. The only things the player should be able to move is the limited number of mirrors at his disposal.

We were also able to experiment further with the brick breaker game, so that now we have a the basic functionality of the brick breaker game. Which means that we have a simple scene and a player controlled 'platform' which can bounce the ball when it hits.

All that would be required now is to add more imarge targets to work as bricks to be destroyed, that would be able to give a minimal viable product for the brick breaker game.


<iframe width="560" height="315" src="https://www.youtube.com/embed/ryngT-RShsA" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/HyWZ5eS5H48" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/PZm6BHpJhmk" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

### Week 3

During this week we first presented what we had made for the marker based AR card game, the games we presented was the prototype or proof of concept the 'brick breaker' and the laser game. 

More information on the two games can be read about in week 1-2.

After the presentation we were introduced to markerless AR, here we also started implementing a project. The requirements was that the markerless AR game should be "add experience in a meaningful way", hence things to consider was which domain(s) to use such as biology, geography and astronomy.

The domain we chose was astronomy, this decision was mostly based on something we had previously created. This to augment a virtual solar system which the user would then be able to view. 

Somethings which were to be considered was, if we wanted to perhaps let the player be able to interact with the solar system in some way. However we have yet to decide on that.

When augmenting the solar system, we had a few issues such as the suns particles, rotation speed of the planets around the sun were too fast and the scaling of most planets were too large.

We also made a few changes from the non AR version to the AR version, one of which was to be able to immerse the player more into the game by removing the linerenderer which created the visual aspect of the orbit lanes.

A thing we also have considered to implement to further captivize the player is to implement a sort of 'skybox' so that the user will feel as though he is in space and viewing the solar system!

During this week a lot of considerations were made as mentioned, but we also got to do the implementation. View the video in this section for week 3 to view what we were so far able to implement!

<iframe width="560" height="315" src="https://www.youtube.com/embed/1xA4zpKZsHI" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

### Week 4

We spent a lot of times trying to work out why the scaling of the solar system would not work.
After hours of discussion and a lot of debugging we concluded that a variable is getting a weird value set even though it should not get a value like this at any point in the code.

We therefore accepted defeat and ignored the scaling issue and finished the demo with some minor tweaks like a freeze button that would stop every planet from rotating around the sun when the program registered at finger press.

### Week 5

We presented the solarsystem application runnning the ARcore from google in class to the other student and got a new assignment.
Using Samsung Gear VR and its controller we were to make a small vr "game" that would demonstrate the locomotion and movement in a virtual space using these devices to move an object or move around the world ourself.

We decided on making a small mini game were the user controls a small race car and is able to turn left,right and reverse, as a extra feature the user would be able to teleport to the car in order to keep track of the car when operating it.

### Week 6

We started implementing the solution and we all agreed on that the graphics would not be a requirement for this exercise rather the functionaly of of the locomitive and movement in a virtual space would work well enough for show.
We started by testing if we were able to control a simple cube in virtual reality using the controller, and this worked out pretty well.
We then discussed how we could split the touchpad up into 4 zones so it would work as 4 buttons on the controller to control the race car, to move left,right, reverse and teleport the user near the car if neccessary.

After a few hours of descussion and coding a solution was made so the car is able to drive forward, backwards, left and right with no issue.
However the teleport function had some issues since we wanted the user to teleport to the back of the car and not directly on it.

We also wanted the teleport function to fade to black and then fade back in, as to reduce the risk of motion sickness. But we didn't get it to work, we tried to use some coroutines that would increase and reduce the alpha value of an image as to simulate a fade in and fade out. 

Later we stumbled up OVRScreenfade, this could be used between scenes, but also mid scenes to introduce screen fade. However, we did not quite get this to work either.


<iframe width="560" height="315" src="https://www.youtube.com/embed/upoRDpEDgoc" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>


### Week 7  - Week 8

We presented our solution to locomotive tasm using a virtual reality game and presenting inside that game aswell.
After the presentation we were given af new task using emmersive audio ( Resonance audio ) plugin for unity3d.
WHat the resonance audio gives you is emmersive sound so that the sound produced in the scene is beeing "bounced" around the room hitting the "ears" correctly.

We decided making a blind game were the player can control at helicopter with WASD and be able to hear the opper is movent.
<blockquote class="imgur-embed-pub" lang="en" data-id="a/d2vKL"><a href="//imgur.com/d2vKL"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>

### Week 9

During this week we formulated our game design document, this document contains all relevant considerations as well as technologies that we expect to utilize to formulate the project. Furthermore, the minimum viable product has also been considered for the project.

### Game title: VR Batter

### Brief description of the game

The game is basically that the player will take the role as a batter, and then there will be a pitcher throwing baseballs towards the player, the player is then supposed to hit the baseball. 

### Assets: 

Baseball bat prefabs from Unity marketplace (Can be found free)
Possible baseball stadium (No free on marketplace, but perhaps some can be found from other sources.)
Baseball prefabs from Unity marketplace (Workaround if it can’t be found, could simple be a sphere.)
Prefabs of baseball players, to immerse the player even further.

### Purpose

The purpose of the game is to help the user increase their reaction time and accuracy. By allowing them to train batting in a virtual environment that is supposed to ‘emulate’ a situation in which the player is the batter.

### Technologies to experiment with

* Object interaction in VR
	* Interaction with the bat and baseball connecting, if the player hits the ball
	* Some links to documentation for this technology: 
		* http://academyofvr.com/intro-vr-development-unity-htc-vive/ (From: Mads)
		* https://vrtoolkit.readme.io/ (From: Kasper)
* Spatialized audio
	* Sound of the ball approaching
	* Sound of hitting the ball
	* Sound of audience cheering in background (Optional.)
	

### Hardware to use for this experience

The game will be developed using HTC vive.

Scripts that we expect to create for this experience

This section has been deliberately left out, as we intend to first research the object interaction in VR. And determine which tool we should use.

### Minimum viable product (MVP)

This document lists several features and components that could be added to the game. E.g. a baseball stadium and baseball players as well as spatialized audio for an audience cheering and the sound of the baseball approaching as well as the sound of hitting the baseball. These mentioned parts aren’t strictly necessary to deliver the concept, however they would be good to have as it can help immerse the player and make him/her feel as though he/she is a batter in a baseball game.

The minimum viable product for this game is the object interaction and that there is a ‘pitcher’ (The pitcher could simply be a cube), but the pitcher would be the game object to shoot out baseballs towards the player.


### Week 10

We started out by getting the feeling on how unity and steamvr was working, we then set out to make diffrent demo's testing how the build in features handling physics in the game was acting when met with diffrent scenarios.

This quickly showed us that the build in phsycis engine could not handle the speed of the moving object and sometimes the object would not get regonized by the collision detection system and just pass through the object itself. We tried several things such as allowing the interacting colliders to be continous dynamic; Which should be used for high speed collisions. But this didn't work either, as sometimes it still simply went through the bat.

We discussed a bit in regards to what we could do instead; We decided to implement a slightly different game, however it would still be based on improving ones reaction time; But it can also help with physical activity as the game would allow for evading and blocking incoming balls.

As such we wrote a new game design in regards to this alteration, and this document intends to describe the altered game.

The document can be found below: 




