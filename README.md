# my-iptv-playlist

A personal M3U playlist for the **From Me To You** IPTV player (bring-your-own-source).

## Use it in the app

Once this repo is public on GitHub, load this raw URL in the app's **Add Source → Playlist URL**:

```
https://raw.githubusercontent.com/<your-username>/my-iptv-playlist/main/playlist.m3u
```

## Format

Each entry is two lines — a `#EXTINF` metadata line and the stream URL below it:

```m3u
#EXTINF:-1 tvg-logo="https://…/logo.png" group-title="News",CNN
https://your-host.com/streams/cnn.m3u8
```

- **`group-title`** decides the section: `movie`/`vod` → Movies, `series`/`show` (or a `SxxExx` in the title) → Series, anything else → Live TV. Multiple categories: `group-title="News;Business"`.
- **`tvg-logo`** is the channel logo / movie-series poster.
- The `url-tvg="…"` on the first `#EXTM3U` line (optional) points at an XMLTV EPG guide.

## Note

Only add streams you own, free-and-legal feeds, or content from a provider you're licensed with.
