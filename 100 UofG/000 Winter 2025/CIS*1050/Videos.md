**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Intermediate HTML]]

## Video Formats
In *HTML5*, we have 3 different supported video formats:

| Format | Video Codec | Audio Codec  | File  |
| ------ | ----------- | ------------ | ----- |
| MPEG 4 | H264        | AAC, MP3     | .mp4  |
| WebM   | VP8, VP9    | Vorbis, Opus | .webm |
| Ogg    | Theora      | Vorbis       | .ogg  |

Below are what browsers support what video formats:

| Browser           | MP4      | WebM | Ogg |
| ----------------- | -------- | ---- | --- |
| Internet Explorer | ✓        | -    | -   |
| Chrome            | ✓        | ✓    | ✓   |
| Firefox           | ✓        | ✓    | ✓   |
| Safari            | ✓        | -    | -   |
| Opera             | ✓ (v.25) | ✓    | ✓   |

## Embedding a Video
To embed a video in HTML, use the `<video>`, element:
```html
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  Your browser does not support the video tag.
</video>
```

*NOTE*: Hosting a video on your own website is very resource intensive. 

### Adding a YouTube Video
1. Upload a video to YouTube
2. Obtain the video ID
3. Define an `<iframe>` element in the web page
4. Define the `src` attribute as pointing to the video URL
5. Use the width and height attributes to specify the dimension of the player
6. Define any other parameters
7. Done

```html
<!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="utf-8" />
      <title>A Basic Web Page</title>
    </head>
    <body>
      <h1>Iceland by Drone</h1>
        <iframe width="420" height="315"
          src="https://www.youtube.com/embed/D37aDfmWBag">
        </iframe>
    </body>
  </html> 
```

#### Modifiable Parameters
- `autoplay`: self-explanatory
- `loop`: self-explanatory
- `controls`: the player controls do not display (0), or do display (1=default)

These parameters are used by adding a `?` at the end of the `src video ID`

```html title="Example of modifiable parameters being used"
<iframe width="420" height="315"
  src="https://www.youtube.com/embed/D37aDfmWBag?controls=0">
</iframe> 
```

## Audio Formats
In *HTML5* there are three supported audio formats: MP3, WAV and Ogg

Audio file type compatibility for browsers:

| Browser           | MP3 | WAV | Ogg |
| ----------------- | --- | --- | --- |
| Internet Explorer | ✓   | -   | -   |
| Chrome            | ✓   | ✓   | ✓   |
| Firefox           | ✓   | ✓   | ✓   |
| Safari            | ✓   | ✓   | -   |
| Opera             | ✓   | ✓   | ✓   |
