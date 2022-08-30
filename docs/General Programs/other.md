# Other

## youtube-dl

The custom command I use for music:  
`youtube-dl -x --audio-format mp3 --embed-thumbnail --restrict-filenames -o "~/Music/%(title)s.%(ext)s" <<URL>>`

Explanation, in flag order:

1. Download the music only
2. Download the music in MP3 format
3. Set the video's thumbnail as the cover art
4. Give the final file the name of the YouTube video name, minus any non-ASCII chcaracters, and save it into your `~/Music` folder
