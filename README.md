# Proof of picks

Each build's fingerprint (SHA-256) is meant to be pushed to `heads.log` when it is sealed, before the games. **20 of 74 builds were**; the rest were published late or not at all (a publishing outage from 2026-10-21 to 2026-11-18, and web-app builds that did not publish until 2026-11-19). `index.html` marks each one, and only the builds announced when sealed show the lineups existed before their games. After the games the full receipt is published in `receipts/`. Check one with:

```
sha256sum receipts/<slate>.json   # must equal the hash for <slate> in heads.log
```

Each receipt's `prev` is the hash of the build before it, so no build can be dropped or reordered. Results: `index.html`.
