### Youtube-dl is a simple, yet powerful tool that can help you to download music on your devices.

### Installation :
```
 wget https://yt-dl.org/downloads/latest/youtube-dl -O /usr/local/bin/youtube-dl
```
### After downloading the script, set the executable permission.
```
 chmod a+rx /usr/local/bin/youtube-dl
 cp /usr/local/bin/youtube-dl /usr/bin/
 ```

### To download a video file, simply run the following command

```
 #youtube-dl ( video file URL / link )
 ```

### To download a video as mp3 file, you can use the following commands:
```
# youtube-dl -x --audio-format mp3 https://youtu.be/AGcioUkXQTI
[youtube] AGcioUkXQTI: Downloading webpage
[download] Destination: 4The People - Loka Samastha song-AGcioUkXQTI.webm
[download] 100% of 4.56MiB in 00:35
[ffmpeg] Destination: 4The People - Loka Samastha song-AGcioUkXQTI.mp3
Deleting original file 4The People - Loka Samastha song-AGcioUkXQTI.webm (pass -k to keep)
```
### If you want to have a cover art for the mp3 file, you can add the --embed-thumbnail option :

```

# youtube-dl -x --embed-thumbnail --audio-format mp3 https://youtu.be/dsmKPyTvjFY
[youtube] dsmKPyTvjFY: Downloading webpage
[youtube] dsmKPyTvjFY: Downloading js player c0a91787
[youtube] dsmKPyTvjFY: Downloading js player c0a91787
[youtube] dsmKPyTvjFY: Downloading thumbnail ...
[youtube] dsmKPyTvjFY: Writing thumbnail to: S5 - Malarey-dsmKPyTvjFY.jpg
[download] Destination: S5 - Malarey-dsmKPyTvjFY.webm
[download] 100% of 3.15MiB in 00:11
[ffmpeg] Destination: S5 - Malarey-dsmKPyTvjFY.mp3
Deleting original file S5 - Malarey-dsmKPyTvjFY.webm (pass -k to keep)
[ffmpeg] Adding thumbnail to "S5 - Malarey-dsmKPyTvjFY.mp3"
```
### Youtube-dl provides an option to download a whole playlist or just a range of songs within it. For that purpose, you will need to use the following options:

```
--playlist-start NUMBER – Playlist video to start at (default is 1)
--playlist-end NUMBER – Playlist video to end at (default is last)
Where "NUMBER" is the starting and ending point of the playlist. The command below will download the first 5 songs from the given playlist:

# youtube-dl -x --audio-format mp3 --playlist-start 1 --playlist-end 5 https://www.youtube.com/playlist?
```
### To download many songs from different playlists :

```
Write the URLs in a file called videos.txt and make sure to keep one URL at a line. Then you can use the following "for" loop to download the songs:

# for i in $(<videos.txt); do youtube-dl -x --audio-format mp3 $i; done
```
