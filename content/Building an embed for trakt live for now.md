I like documenting things, and automating documenting things is even better. For this reason, I have set-up trakt.tv and last.fm to track(scrobble) my movies/TV and Music listening habits respectively. Already, one can access my profile there on the website. 

But I wanted a live view on my website as well, a-la MySpace. Honestly, making it public seems like an oddly intimate thing to do, but it's a fun technical exercise. Trakt offers a prebuilt widget that offers this functionality, but to get it you must subscribe to their VIP feature, which costs $60 a year, not worth it for me for this one feature.

I then built my own. It went well.
## What do i want?
I want to display my most recently watched tv series or show, on my website, along with the date and an image to go along with it.

## How am I going to accomplish this?
TL;Dr: I used a python script to fetch the recently watched Media from the Trakt API, and image links from the TMDB API. 
I use GitHub actions to run that script to generate an HTML file on my site's repo
Integrating that HTML into my Jekyll site was then easy.

For images, trakt itself has helpful ids within it's JSON response that map to images from TMDB or TVDB, so we are going to use those


1. Authenticate with Trakt.tv API
2. Fetch latest watched show data
3. Extract relevant info (show title, year, etc.)
4. Use this info to query image database API
6. Generate HTML for embed with show info and image URL
7. Save embed HTML to a file or database for your website to access

## Challenges:
I had to figure out Authentication properly through the secrets feature on GitHub, which took some trial and error. Debugging it was also annoying because while it was working on my local machine, it wouldn't on GitHub actions, so testing a new version each time was annoying because I had to wait for the commit+the action to run. 

## Results:
The widget is live on [Now | Rudra Kabir.](https://rudrakabir.com/now/), works flawlessly, and hopefully should update every six hours(I'll check once it's been six hours).

The code for the script is available at [rudrakabir/Trakt-Embed (github.com)](https://github.com/rudrakabir/Trakt-Embed) and you can check it out there. I also wrote a tutorial for it [[Integrating Trakt.tv Watch History into a Jekyll Site]]


# To Do
- Customise the styling a little more, I don't quite like the way it looks but it's late in the night and I want to sleep already. 