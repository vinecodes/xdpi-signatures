# xDPI signatures

Signature files that xDPI fetches daily (xDPI's `signature_feed.py`):

| File | What it holds |
|---|---|
| `cert_signatures.json` | Certificate issuer patterns → app and category |
| `ssh_signatures.json` | What SSH implementations offer |
| `media_signatures.json` | How files of each media type begin |
| `ja4_signatures.json` | TLS client fingerprints of tunnelling software |

Each router accepts a file only when it parses and isn't empty; otherwise it
keeps the set it has (or the one bundled with xDPI). A fix here reaches
routers within a day, with no xDPI release.

Published from xDPI with `python xdpi-threat/publish_signatures.py <this checkout>`,
which checks every file with the same parser first. Don't edit files here by hand.
