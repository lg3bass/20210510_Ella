# Ellie Belly

	Ellie Belly - My favorite song I wrote for my daughter.  Produced in Live/Jitter and output realtime.

	#visualmusic 
	#kaleidoscope 
	#opengl 
	#motiondesign 
	#shader 
	#realtime 
	#computerart  
	#creativecoding 
	#newmedia 
	#7stringbassguitar 
	#motiongraphics

	#jitter74 
	#madewithjitter 
	#jitter 
	#abletonlive 
	#cycling74 
	#maxmspjitter 
	#maxjitter 
	#c74connect

	//shader (via smoothstep.io)
	https://smoothstep.io/anim/66e8f77dea84


## PUBLISH

[Vimeo](https://vimeo.com/556865684)
[YouTube](https://youtu.be/Gm83Z6rt370)
[Instagram](https://www.instagram.com/p/CPWe8abHBW_/?utm_source=ig_web_copy_link)
[Twitter](https://twitter.com/lg3bass/status/1397670087944032262?s=20)

## Observations/Work notes

To date, of all the visual music animation so far this project went the smoothest by comparison.  It seemed like all pieces just worked together but it was not without trouble and shortcomings. 

Sometime when you switch scenes there is glitch.  This doesn't happen often.  At the end of this animation there is glitch on the last transition.  I couldn't figure out why exactly this happened.  I recored a number of different takes thinking I could get a version where this didn't happen but none of them were a success.   This brought out a good comparison.  I had created the function curves so I can do 3 things: 1. Ultimately I want to be able to export out to .chn files for houdini.   2.  If I needed I can edit the curve points for exact timing. 3. I was under the assumption that running exclusively from the curve windows and using pattr would be faster.  I found that the 3rd point here is not true.  Timing ran just as well, if not better, when the function curves were created on the fly though js rather than pattr.  The glitch I am getting during scene transitions is proof of this. 

Another observation is it is not very well documented and kinda cumbersome especially the key command combinations used to place keys. Would remember how to use the ADSR tool if I came back to this in a year? Probably not.

#### Shaders

Creating shaders is challenge.  I dread having to make shaders from scratch.   A, I'm not good enough at it yet and B, There is no feed back loop where I can develop.  I've found that smoothstep.io is the best for rapid development but it has it shortcomings.   Ideally I may look at the code used in this site to make my own shader editor someday.  But for now smootstep will have to do.  Here are my work for this animation:

The visual style for this animation is based off this shader by [fizzer](https://www.shadertoy.com/user/fizzer).  I like the way the shadows were done making it look 3d. I was looking for example now to do a kaleidoscope effect.  I reversed engineered this shader (sometimes lifting code exactly) and modified it for my version.  Thank you [Fizzer](https://www.shadertoy.com/user/fizzer).

[Shadertoy - inspiration, credits](https://www.shadertoy.com/view/ls3GRr)

[Final Shader](https://smoothstep.io/anim/66e8f77dea84)

[WIP - Basic kaleidoscope shader - layer 4 only](https://smoothstep.io/anim/8d5dd9a0ec08)

[WIP - Paper Kaleidoscope5](https://smoothstep.io/anim/9f1b440c1ec5)

[WIP - Paper Kaleidoscope](https://smoothstep.io/anim/b925ee3f2843)

#### Tools/Files

	/20210510_Ella/Ella_1 Project/M4L/JXS-files/paperKaleidoscope2.jxs
	/20210510_Ella/Ella_1 Project/M4L/JSON/bakedFunctions3.json
	/20210510_Ella/Ella_1 Project/M4L/JSON/20210517_track4.json
	/20210510_Ella/Ella_1 Project/M4L/JSON/20210517_track3.json
	/20210510_Ella/Ella_1 Project/M4L/JSON/20210517_track2.json
	/20210510_Ella/Ella_1 Project/M4L/JSON/20210517_track1.json
	/20210510_Ella/Ella_1 Project/M4L/ADSR-JXS_0.064.amxd
	/20210510_Ella/Ella_1 Project/M4L/ADSR-automation_v0.06.amxd
	/20210510_Ella/Ella_1 Project/M4L/ADSR_0.249.amxd
	/20210510_Ella/Ella_1 Project/Ella_7.als

#### ADSR Bugs

1. Keying on tab 2 of ADSR gridwindow sets keys on tab 1
2. Saving is cumbersome without SaveAll and loadAll.
3. When AVRecorder (part of ADSR-JXS_0.064.amxd) is visible it lowers framerate dramatically. 
	- Need to hide or minimize all M4L to have it run full frame.
	- Remove AVRECORDER from ADSR-JXS.
	- Recreate AVRRECORDER without pwindow.
4. (ADSR_0.249.amxd) Testing ezdac is enabled when project loads.   
5. Need a way to see fpsgui when M4L devices are hidden.
6. (ADSR_0.249.amxd) Function Curve Windows
	- Double points on attack-decay states. Not all have double states.
	- Fill up space at beginning and end with zero.
	- Accidentally jumping scenes will destroy unsaved work in editor 
	- Need documentation on how to use pattr/curve mode. What do the buttons mean?
7. (ADSR_0.249.amxd)Key commands to set keys need to be documented. 



#### Music ©2011 bobwhitemedia

I wrote this song in 2011 after my 2nd daughter was born.  Very much inspired by Gilberto Gil who i was listening to a lot at the time. 

[Sheet Music]()
[Soundcloud](https://soundcloud.com/lg3bass/ella)

#### Thanks for watching/listening!
