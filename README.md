# BAND-MAID Tweet Archive

A searchable archive of translated BAND-MAID tweets, hosted on GitHub Pages.

## Overview

This archive contains approximately 52,000 tweets from BAND-MAID and its five members, spanning from 2013 to present. All tweets include the original Japanese text alongside an English translation.

🔗 **View the archive here:**  
[https://drivetimebm.github.io/BAND-MAID_tweets/](https://drivetimebm.github.io/BAND-MAID_tweets/)

[Project Description](https://www.reddit.com/r/BandMaid/comments/1nn2aof/bandmaid_translated_tweet_archive_20132025/)

## Features

- Full-text search across English translations and original Japanese text
- Filter by member (BAND-MAID, Saiki, Miku, Kanami, Akane, MISA)
- Date range filtering
- Links to original tweets on X (Twitter)
- Virtual scrolling for smooth performance across the full dataset

## Files

| File | Description |
|---|---|
| `index.html` | Self-contained search interface |
| `tweets.json` | Archive data (~22 MB) |
| `favicon.png` | Site favicon |

## Data Format

```json
[
  {
    "id": 1,
    "dateJST": "2013-07-19T13:58:37",
    "member": "BAND-MAID",
    "jp": "～Twitter始めます～",
    "en": "I'm starting Twitter!",
    "url": "https://x.com/bandmaid/status/358088464937390080"
  }
]
```

| Field | Description |
|---|---|
| `id` | Sequential record ID |
| `dateJST` | Tweet datetime in Japan Standard Time (ISO 8601) |
| `member` | Posting member: `BAND-MAID`, `Saiki`, `Miku`, `Kanami`, `Akane`, or `MISA` |
| `jp` | Original Japanese tweet text |
| `en` | English translation |
| `url` | Link to the original post on X |

## Members

| Member | Color |
|---|---|
| BAND-MAID | White |
| Saiki | Blue |
| Miku | Pink |
| Kanami | Green |
| Akane | Gold |
| MISA | Purple |

## Performance Notes

The full dataset is approximately 22 MB. The archive page streams and parses `tweets.json` client-side on first load, displaying a progress indicator while fetching. Once loaded, all filtering and search runs locally in-memory with no additional network requests.

## Related

- [BAND-MAID Instagram Archive](https://github.com/drivetimebm/BAND-MAID_instagram)
