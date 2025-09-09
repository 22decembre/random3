# Random3

This is my Hugo theme, translated form my Pelican theme, which was an adaptation of Sam Hocevar's dev-random theme.

This Hugo theme is provided "as-is" by the author. You are kindly asked to use, fork, modify or twick it to fit your needs.
Please just keep my name as the original author and provide a link to my [website](https://www.22decembre.eu).

## installation

Clone the git repo, and write the theme's name in the conf' file and you're on tracks.

    cd ~/hugo/themes/
    git clone https://github.com/22decembre/random3.git
    
In config.toml :

    theme = "random3"

## Responsive

The theme is responsive, with the nav bar being placed at the bottom on mobiles screens.

## extras

This theme has a few extras that you can configure through config.toml:

    [params]
    isso="https://www.your.website.net/isso/"
    spamtrap="honey@your.website.net"

[Isso](https://posativ.org/isso/) is a python self-hosted comment system. It will be placed at the bottom of articles.

## Tags

The tags in the tagcloud are bigger depending on the number of articles that are tagged in them.


## Shortcodes

The theme is provided with shortcodes, some of which (tags and categories) are internals and necessary to run it.

### videoloop

This will load an mp4 videoclip and run it on loop, muted, without controls. Ideal for meme placement.

Example (running in https://www.22decembre.eu/en/2024/03/31/serenpidity/) :

{{< videoloop src="/images/Confused_Travolta.mp4" width="80%">}}

src is mandatory. width and height are optional and are to be provided the same way you would for a regular video/image (% or pixel sizes).

### img

This places your pictures in a more controlled way than the bare []().

Example :

{{< img src="https://photos.22decembre.eu/danemark/aarhus/20170306_144129.jpg" width="25%" alt="Aarhus Ø: detailed plan." >}}

src is mandatory. width, height (provided in % or pixel size) and alt (replacement text for accessibility) are optional.

### peertube

This allows to place videos hosted on peertube.

Example (running in https://www.22decembre.eu/en/2021/04/13/entreprises-francaises/):

{{< peertube instance="video.passageenseine.fr" id="8bb3993e-9734-4dba-941b-02d00dd051fa" >}}

instance and id indicate which instance to load the video from, and the id of said video. width and height, once again in % or pixels, are optional.

### wp

wp will create a link to a wikipedia article in the language of the post.

Example :

{{< wp LaTeX >}}
 
will link to the page related to the LaTeX typesetting framework on the wikipedia of the current language.


## languages

The theme is translated in English, French and Danish.

## Sidebar links.

The sidebar provide a blogroll listing, links to social networks and local links to your sites. If you wish to use them, you have to configure them in the data folder of your Hugo installation :

    cd ~/hugo/data/

Blogroll.json:

    {  "Cborne":
        {   "name": "Cyrille Borne",
            "url": "https://cborne.fr" },
            
        "Indre":
        { "name": "Indre's Tumblr",
        "url": "https://damage-girl.tumblr.com/" },
        
        ...
        
        "Authueil":
        { "name": "Authueil",
        "url": "https://authueil.fr/" }
    }
   
Social.json :

    { "Mastodon":
        {   "name": "Mastodon",
            "url": "https://mamot.fr/@you" },
        
        "Diaspora":
        { "name": "Diaspora",
        "url": "https://diasp.eu/u/you" }
    }
   
Local.json :

    { "Photos":
        {   "name": "Your photos",
            "url": "https://photos.your.website.net" }
    }

Logos of Mastodon, Facebook and Diaspora are just pictures and not tracking links.
