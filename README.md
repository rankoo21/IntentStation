# Intent Station

Intent Station is a routing board for public-web context. A visitor writes a request, chooses a public service catalog, and lets validators bind the request to one allowed lane with a catalog digest.

## Contract

`contracts/checkpoint_graph.py` contains `IntentRouter`. It stores the owner, request, HTTPS catalog, allowlist, canonical lane, confidence, explanation, and SHA-256 catalog digest. Lifecycle: `DRAFT -> ROUTED -> CONFIRMED`.

- Studionet contract: `0xD3b147EE46206a9a8055529eeAa74617A1093874`
- Live site: https://intent-station-genlayer.pages.dev
- Public repository: https://github.com/rankoo21/IntentStation

## Checks

```text
python -m pytest tests -q
genvm-lint contracts/checkpoint_graph.py
npm run build
```
