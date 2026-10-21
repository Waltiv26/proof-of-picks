# Proof of picks

Every official build's fingerprint (SHA-256) is pushed to `heads.log` before the games. After the games the full receipt is published in `receipts/`. Check one with:

```
sha256sum receipts/<slate>.json   # must equal the hash for <slate> in heads.log
```

Each receipt's `prev` is the hash of the build before it, so no build can be dropped or reordered. Results: `index.html`.
