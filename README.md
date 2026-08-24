# PEER — Features and Platform Support

PEER is a cross-platform media discovery and playback client. It brings movies, TV, anime, manga, sports, IPTV, personal
libraries, playback sources, and local profiles into one application.

> PEER does not provide or host media or adult content. Playback availability depends on the
> sources, add-ons, playlists, and services configured by the user.

## Highlights

- Browse featured, trending, curated, and genre-based movie and TV collections.
- Search for titles and open detailed pages with artwork, ratings, metadata,
  synopsis, cast, trailers, seasons, and related content.
- Explore dedicated anime and manga catalogues without mixing them into the
  main discovery feed.
- Discover sports and open playback only when a compatible source is
  available.
- Maintain a profile-specific library with watchlist, watching, watched, and
  continue-watching progress.
- Play direct streams, embedded web players, IPTV channels, debrid links, and
  supported torrent sources.
- Use built-in playback or hand a ready stream to a compatible external player.
- Search for, download, parse, display, resize, reposition, and synchronize
  subtitles.
- Configure multiple local profiles, including kids profiles, with separate
  libraries, settings, downloads, add-ons, and usage statistics.
- Use a responsive interface designed for phones, tablets, desktops, keyboards,
  remotes, Android TV, and Fire TV.

## Discovery and Browsing

PEER includes a home experience with featured content, collection shortcuts,
continue watching, recommendations influenced by local interactions, and
curated shelves. Its discovery feed supports trailer previews, contextual
browsing, popular searches, filters, cast pages, and collection pages.

Separate content modes provide:

- **Cinema:** movies and television.
- **Anime:** seasonal titles, established series, and discovery collections.
- **Manga:** a reading-oriented catalogue kept separate from playback content, upon selection redirects you to its official site to read (typically mangadex) which is free.
- **Sports:** schedules, categories, events, and available stream sources.
- **IPTV:** user-configured live television playlists and channels, bring your own playlists.

## Playback

The built-in player supports normal video sources and live feeds, playback
progress tracking, buffering feedback, retry handling, source selection, and
configurable subtitles. IPTV playback uses a larger read-ahead budget and
automatic reconnection for interrupted live streams.

Supported playback paths include:

- Direct video and HLS links.
- Embedded web players with request-level content blocking.
- IPTV playlists in M3U format.
- Add-on-provided streams and subtitles.
- Real-Debrid and Premiumize source resolution.
- Native on-device torrent streaming.
- External-player handoff for compatible Android torrent streams.

Torrent video selection recognizes MP4, MKV, WebM, MOV, M4V, AVI, TS, M2TS,
MTS, MPEG, VOB, OGV, FLV, and WMV containers. Actual codec support still depends
on the decoder available on the device.

## Torrent Streaming and Downloads

PEER contains an optional torrent engine. It starts only when on-device
playback is requested, selects and prioritizes the relevant movie or episode,
and exposes it to the player through a HTTP server.

- Temporary stream data is removed when playback closes by default.
- **Keep downloads** can preserve data in app-specific storage.
- Kept items appear in a profile-specific Downloads catalogue.
- Downloads can use internal or external app storage on Android.
- Retention dates can be assigned, changed in bulk, or set to keep indefinitely.
- Expired and manually deleted entries remove both the catalogue record and
  validated app-owned files.
- Previously downloaded pieces can be verified and reused when a source is
  reopened.

## Direct torrent playback joins a BitTorrent swarm and may expose the user's public IP address to peers. PEER displays a privacy warning and does not claim to verify VPN routing or split-tunnel behavior as PEER does not come with a built-in VPN.

## Library, Profiles, and Integrations

- Multiple local profiles with names, avatars, colors, and an optional kids
  designation.
- Independent watchlists, playback progress, history, preferences, add-ons,
  downloads, and statistics for each profile.
- Local profile backup and restore support.
- Real-Debrid and Premiumize credentials stored through secure local storage.
- Configurable add-on catalogues for streams and subtitles - supports most stremio add-ons.
- OpenSubtitles support when an API key is configured or from an add-on.
- IPTV configuration and playlist parsing.

## Subtitles

PEER can retrieve subtitles from configured services and add-ons, parse subtitle
files locally, and render them over the built-in player. Users can adjust:

- Subtitle language/source selection.
- Font size.
- Timing offset.
- Distance from the bottom of the player.

## Content Blocking and Privacy

The embedded player keeps JavaScript enabled for compatibility while blocking
matching network requests before they reach the page. The clean-room filter
engine supports common EasyList, Adblock Plus, AdGuard, and hosts-file syntax,
including network exceptions, resource types, domain restrictions, standard
cosmetic rules, and regular-expression rules with safety limits.

PEER also blocks pop-up windows and cross-origin main-frame redirects. Critical
media requests are protected from overly broad rules unless they match a strong
advertising signature. However although PEER does not have ads some embedded players sometimes inject ads through different methods which sneak through the ad blocker, trying to target this could lead to compatibility and playback issues with embedded links

Usage statistics are stored locally and per profile. They include watch time,
streams started, completed titles, blocked advertising requests, recent
activity, and playback-source breakdowns. These counters are not uploaded as
analytics. PEER does not send any user analytics anywhere.

## Reliability and Offline Behavior

- API response caching.
- Cached artwork with controlled decode sizing.
- Stale-data fallback when fresh requests fail.
- Safe URL construction, request timeouts, and typed failures.
- Connectivity awareness and user-facing diagnostics.
- Bounded torrent metadata and readiness checks instead of endless loading.
- In-app update checking and update prompts on supported builds, auto updating included but never forced.
- PEER can still operate through add-ons even if the backend ever dies.

## PEER brief summary

> Cross-platform media discovery and playback client for Android, Android TV,
> Windows, Linux, macOS, and Web. Featuring movies, TV, anime, manga, sports,
> IPTV, profiles, local libraries, subtitles, add-ons, debrid integrations,
> content blocking, and optional native torrent streaming.

## For github

`flutter` · `dart` · `rust` · `android` · `android-tv` · `windows` · `linux` ·
`macos` · `web` · `media-player` · `iptv` · `m3u` · `torrent-streaming` ·
`real-debrid` · `premiumize` · `movie` · `subtitles` . `free` . `stremio`

