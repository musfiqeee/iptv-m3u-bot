# IPTV Working Streams Combined M3U Bot

[![Check and Combine M3U Streams](https://github.com/musfiqeee/iptv-m3u-bot/actions/workflows/check-and-combine.yml/badge.svg)](https://github.com/musfiqeee/iptv-m3u-bot/actions/workflows/check-and-combine.yml)

This bot fetches multiple IPTV M3U playlists, checks each video stream for availability, and combines all working streams into a single `.m3u` file.

## 📺 Playlist URL

Click to copy:
```
https://raw.githubusercontent.com/musfiqeee/iptv-m3u-bot/main/output/all.m3u
```

## Features

- Fetches and parses several M3U playlist files
- Checks each stream for availability
- Produces one combined M3U (`all.m3u`) with working streams only
- Automated update via GitHub Actions (fetches + generates daily)

## Usage

### Local

1. **Install dependencies**
    ```
    pip install -r requirements.txt
    ```

2. **Run the script**
    ```
    python scripts/m3u_working_streams_combined.py
    ```

3. Your working streams will be in `output/all.m3u`.

### Automated Workflow

A GitHub Actions workflow runs daily and/or on repository push to regenerate and commit `all.m3u`.

## Customization

- To check different playlists, add URLs to `data/feed.txt`.
- To adjust concurrency or request timeouts, modify respective params in the script.

## License

MIT