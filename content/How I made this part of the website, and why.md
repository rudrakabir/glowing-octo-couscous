This is the "notes" section of my website. 

I want to take a bit to my document the process of creating this section of the website, both in the interests of reducing friction for me personally in terms of remembering to keep it updated, and to help you make a notes section for your website, if you want to.

This section is inspired by the working-in-public philosophy, that celebrates the existence of "unfinished", or work in progress projects, as something not to be hidden away until it's time for the grand reveal, but a continuous act over time. Much like gardening. I wanted to have a place where I can put down drafts of thoughts while they take shape in my brain, of any size and shape. I also wanted freedom from the constraints of the posting methods of social platforms and the dark patterns they employ, so I hosted this on my own website(also a work still in progress). I hope this is a safe nourishing environment where my ideas will mature before they are ready to go out into the world on their own.

The beauty of it is that it integrates with my favourite program in the world, Obsidian, where I already do most of my writing, so posting and editing content is damn damn easy. Apart from the domain registration charges(which are optional, if you don't want your own domain), it is also hosted online completely free.

On to the tutorial!

(A lot of the information here is taken from various sources online, I am collating it here for my easy reference)

Step 1. Get a Website. I used Namecheap to register the domain itself, and am currently learning how to use Astro + Netlify to build and host the site. rudrakabir.com

Step 2. Get quartz on a subdomain in the website and get it synced up with GitHub, and your obsidian vault. 

Step 3. Now, whenever I am done writing a new thing, and want to publish, all I need to do is

```
cd ~/Directory/to/Quartz
npx quartz sync
```
It will automatically handle it from there. This makes it really easy to do. 

Step 4. I made this even easier, by using Automator.app to create an applet that runs it on command, so I don't have to type it out every time(but let's be honest, I was scrolling through my shell history anyway)
To do that, add an applescript action to a new autoamtor app with the following code

```
source ~/.zshrc
cd /Users/rudrakabir/Desktop/Website/quartz
npx quartz sync
```

the source ~/.zshrc is so that Automator can use the same environment as your terminal, which is needed otherwise you have to manually define a path.

Now, all i need to do when I want to publish is finish writing in Obsidian, and hit the publish icon on my desktop, and Voila! time to go do just that. 


To Update:

```
npx quartz update
```
if node is out of date,

```
npm update
nvm install $required_version
nvm use $required_version
```


The end result should be a frictionless writing environment that is tailored foremost for the organisation and management of useful information, and yet takes 5 seconds to publish, and just a few minutes to propagate on an interface that is clean, and customisable. 

Welcome to notes.rudrakabir.com!


