# Youtube album download tools
- ## yt-split
  - Downloads audio from a youtube url and tries to split it by chapter
  - If there are no chapters it falls back on silence-detection
  - Runs autotag
  - *todo:*
    - *if there's no chapters, try to find a track list in the comments before attempting the often-unsuccessful "split-by-silence"*
    - *cuesheet support maaaay be useful too*
- ## autotag
  - takes an audio filename and fingerprints it with AcoustID
  - looks up the fingerprint on MusicBrainz, returns the earliest ever release that contains that track  
  - re-streams the file with ffmpeg, including the tags found, into a new folder
  - if successful, deletes the original file
  - *todo:*
    - *determine if it's an album, or a single for cases where the single was released first*
    - *replaygain album scan*
    - *artwork*

## Dependencies
### Linux
- node
- ffmpeg

### Android
- termux, plus all the above