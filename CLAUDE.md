# Tracklist Matcher

## Overview
Standalone frontend for matching tracklists against the Discogs database. Talks to the production Discogs API at `https://api.shovelfordiscogs.com`.

## Files
- `matcher.html` - Live/current version deployed to production
- `test.html` through `test7.html` - Development iterations

## Deployment
The matcher is served from the Discogs API server at `matcher.shovelfordiscogs.com`.

- **Server**: `root@46.224.37.237`
- **Path**: `/var/www/matcher/index.html`
- **Deploy**: `scp matcher.html root@46.224.37.237:/var/www/matcher/index.html`

## Architecture
- Fully standalone HTML — inline JS, no build step, no dependencies
- Calls the `/tracklist` endpoint on the production API
- Streams results via NDJSON
