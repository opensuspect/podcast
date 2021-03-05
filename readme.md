# OpenSuspect Podcast Feed
## Updating
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

### Compiling the updated feed

To compile your new feed, just run `./compile.sh` If you don't have the `Cheetah` Python3 package, you'll need to install it first. If anything happens to go wrong, the old version of the feed will be stored in `feed.xml.bak` If you screw up again, that's what git is for ;)