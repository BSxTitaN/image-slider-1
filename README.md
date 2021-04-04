# React image slider

![Player Preview](https://i.imgur.com/qVX68ve.gif)

### Demo: [https://image-slider-madza.vercel.app](https://image-slider-madza.vercel.app)

---

## Installation

```javascript
 npm install @madzadev/image-slider
```

## Usage

```javascript
import Player from "@madzadev/image-slider";
import "@madzadev/image-slider/dist/index.css";
```

```javascript
const tracks = [
  {
    url: "https://audioplayer.madza.dev/Madza-Chords_of_Life.mp3",
    title: "Madza - Chords of Life",
    tags: ["house"],
  },
  {
    url: "https://audioplayer.madza.dev/Madza-Late_Night_Drive.mp3",
    title: "Madza - Late Night Drive",
    tags: ["dnb"],
  },
  {
    url: "https://audioplayer.madza.dev/Madza-Persistence.mp3",
    title: "Madza - Persistence",
    tags: ["dubstep"],
  },
];
```

```javascript
<Player trackList={tracks}>
```

`trackList` is the mandatory prop and requires to pass in an array consisting of objects with `url`, `title` and `tags` keys.

## Options

The default values of available options props are displayed.

```javascript
<Player
  trackList={tracks}
  includeTags={true}
  includeSearch={true}
  showPlaylist={true}
  autoPlayNextTrack={true}
/>
```

## Color schemes

The player uses 5 color palette by default.

You can further customize the player by editing the colors variable below.

```javascript
const colors = `html {
          --tagsBackground: #9440f3;
          --tagsText: #ffffff;
          --tagsBackgroundHoverActive: #2cc0a0;
          --tagsTextHoverActive: #ffffff;
          --searchBackground: #18191f;
          --searchText: #ffffff;
          --searchPlaceHolder: #575a77;
          --playerBackground: #18191f;
          --titleColor: #ffffff; 
          --timeColor: #ffffff;
          --progressSlider: #9440f3;
          --progressUsed: #ffffff;
          --progressLeft: #151616;
          --volumeSlider: #9440f3;
          --volumeUsed: #ffffff;
          --volumeLeft:  #151616;
          --playlistBackground: #18191f;
          --playlistText: #575a77;
          --playlistBackgroundHoverActive:  #18191f;
          --playlistTextHoverActive: #ffffff;
      }`;
```

```javascript
<Player trackList={tracks} customColorScheme={colors} />
```

## Final notes

It's recommended to use CMS like Contentful or DatoCMS to manage your audio files and access them via API.
