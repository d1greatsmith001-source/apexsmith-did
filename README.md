# Apex Smith DID Infrastructure

W3C Decentralized Identity infrastructure for Apex Smith Management Company.

## DID: `did:web:apexsmith.pw`

This repository contains the complete DID infrastructure for institutional provenance and decision attestation.

## Quick Setup

1. **Clone/Download this repository**
2. **Enable GitHub Pages**: Settings → Pages → Deploy from branch → main
3. **Verify DID**: Visit https://apexsmith.pw/.well-known/did.json
4. **Test credentials**: `cd scripts && npm install && node issue-credential.js retroactive`

## Structure

- `/.well-known/did.json` - DID Document (W3C compliant)
- `/index.html` - Public landing page  
- `/scripts/` - Veramo credential issuance tools
- `/credentials/` - Credential archive (auto-created)

## Credential Issuance

### Retroactive Queue
Issue all 10 queued Decision Log credentials:
```bash
cd scripts
npm install
node issue-credential.js retroactive
