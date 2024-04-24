I am forced to use instagram because their network effects make it so that most of the people I want to talk to are on instagram as their preferred messaging medium. I kinda hate it because 
A. It makes message archival very difficult
B. It doesn't allow simple shit like sending files or voice recordings longer than 1 minute
C. The stories and posts are too easy to spend a lot of time on

but most importantly because
D. It's reels and suggested content inserted all over the place are too sweet to resist for my ADHD brain and I spend minutes enthralled in them in all sorts of inbetween uncomfortable positions because my brain is too occupied to notice my body is in discomfort. 

So I decided to make an automation to automatically break that circuit so that I could notice it happening and rescue me. 

Let me call it a light pattern. 

instagram's dark pattern is that even in your home page, where you (or at least me, given their A/B testing) see reels as small thumbnails. Even worse, they are three or four at a time, so impossible to not notice at least a bit, and then naturally start scrolling from there. 

the light pattern then, or positive enshittification, i tried first was to make instagram as irritating to use as possible. I implemented a shortcut(using the inbuilt automations/shortcuts app in iOS) to close instagram every 15 seconds. This was damn annoying, and succeeded in breaking the loop. 

Experimenting with the timing made me settle on a 90 second timer. Above that, and it was too easy to use and I'd spend a lot of time in the App, but too much below that and I'd invariably run into a situation where I'd _neeed_ to use it and I'd disable the automation, and it would stay disabled a while. 90 seconds was a comfortable medium where I couldn't watch more than 2-3 reels without interruption, and then choose what to do next. Usually, this choice was enough to make me move on. This is more or less what I've settled on, and it works for me.

I still wish instagram had a post only + messages mode. 

Exact Shortcuts, in case you want to replicate

1. Create a new focus, I called mine Instatimer
2. Make 4 automations
	1. When "App"(check instagram) is opened, turn focus on 
	![[i1.jpeg]]
	3. when "App" is opened, turn focus off 
	![[i2.jpeg]]
	5. When focus turned on, wait X time(this is modifiable), and then turn focus off
	![[i3.jpeg]] ![[i4.jpeg]]
	7. When focus is turned off, Go to Home screen.
	![[i5.jpeg]]

3. Make Sure all of them are set to run immediately, and not notify you(the notifications will get cluttered fast)

here is what happens

When you Open instagram, and keep scrolling past the 65 second deadline, the automation will turn the focus off, which will trigger a Go to homescreen, hopefully giving you a much needed space to reset your intention.







