# AstroNicoEmbed

AstroNicoEmbed allows easy embedding of Niconico Douga (ニコニコ動画) videos in Astro projects.

AstroNicoEmbed is a component library for easily embedding Niconico Douga videos into Astro projects. With minimal setup, it enables you to display Niconico video players on your pages, providing an engaging and seamless embedding experience.

> [!NOTE]
> Please note that embedded videos may not play on a local server.

## Installation

```bash
npm install astro-nico-embed
```

## Usage

```astro
---
import { NicoVideo } from "astro-nico-embed";
---

<NicoVideo videoId="sm9" />
```

## Props

### `videoId`

The ID of the Niconico video to embed. This is the part of the video URL after `watch/`, e.g. `sm9` for `https://www.nicovideo.jp/watch/sm9`

- Type: `string`
- Required: `true`

### `loading`

The loading strategy for the video player. If set to `lazy`, the video player will only be loaded when it is in the viewport. If set to `eager`, the video player will be loaded immediately.

- Type: `lazy` | `eager`
- Required: `false`
- Default: `lazy`

### `aspectRatio`

The aspect ratio of the video player. This is used to calculate the height of the video player based on the width. Its format is same as CSS `aspect-ratio` property.

- Type: `string`
- Required: `false`
- Default: `16 / 9`
