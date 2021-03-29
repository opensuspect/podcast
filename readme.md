# OpenSuspect Podcast Feed
## Updating the Feed
### Editing the `feed.tmpl` file
All of the show details are inside the `$showinfo` variable. It is in the JSON format, so it's fairly easy to read. Here's a snippet:
```JSON
"title": "OpenSuspect Podcast",
    "description": "This is our description",
    "subtitle": "this is like a short description",
    "image": {
        "url":"https://podcast.opensuspect.com/image.jpg",
        "width": "1080",
        "height": "1080"
    }
```
The `$categories` list must only include categories that are officially dedicated by iTunes, these are not keywords.

To add an episode, edit the `$episodes` variable. It is also in the JSON format. Here's an example episode:

```JSON
{
        "title": "OpenSuspect Podacst Episode #1",
        "description": """
            This is a description
        """,
        "subtitle":"this episode's subtitle!",
        "length": "48:33",
        "link":"https://youtu.be/Xk9XgsOiFcE",
        "url": "https://podcast.opensuspect.com/episodes/ep1.mp3",
        "format": "audio/mpeg",
        "date": "Tue, 02 Mar 2021 00:00:00 +0000"
}
```
Make sure to add new episodes to the top, and not the bottom of the list, so that more recent episodes appear at the top.

### Compiling the updated feed

To compile your new feed, just run `./compile.sh` If you don't have the `Cheetah` Python3 package, you'll need to install it first. If anything happens to go wrong, the old version of the feed will be stored in `feed.xml.bak` If you screw up again, that's what git is for ;)

## Updating the landing page


### Changing the podcatchers
The list of podcatchers is stored in the list called `$podcatchers`. Each item follows this format:
```JSON
{
        "name": "Apple Podcasts",
        "url": "https://podcasts.apple.com/podcast/id1556916527",
        "icon": "https://podcasts.apple.com/favicon.ico"
}
```
It's fairly self explanatory.

Don't forget to run `./compile.sh` before commiting

### Updating show info

It's in the `$showinfo` array. It's also very self explanatory.