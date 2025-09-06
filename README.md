# Smart IP AutoFill (Chrome Extension)

A privacy-first extension to capture and autofill form data across websites. Create reusable profiles, apply them with one click, and stay in control of your data.

---

## Table of Contents

1. [Features](#features)
2. [Supported Sites](#supported-sites)
3. [Security & Privacy](#security--privacy)
4. [Permissions](#permissions)
5. [Install (Unpacked)](#install-unpacked)
6. [How to Use](#how-to-use)
   - [Create a Profile](#create-a-profile)
   - [Apply a Profile](#apply-a-profile)
   - [URL Autofill Modes](#url-autofill-modes)
7. [Validation Rules](#validation-rules)
8. [Troubleshooting](#troubleshooting)
9. [Changelog (1.0.5)](#changelog-105)

---

## Features

- Secure profiles stored locally (encrypted at rest with a per‑device key)
- Smart form detection: names, ids, placeholders, labels, and fuzzy matching
- Robust autofill for inputs, selects (single & multi), checkboxes, and radios
- Platform-aware URL filling (Facebook/Instagram, TikTok, or any site)
- Real‑time validation and clear inline feedback in the popup
- No sign‑in required, no tracking, no external data transfers

## Supported Sites

- Facebook and Instagram (optimized; 30 URL limit; one URL per textarea if present)
- TikTok (optimized; de‑duplicated newline‑joined list)
- Any other website (generic strategy; 100 URL limit)

## Security & Privacy

- All data remains in your browser via Chrome storage (may sync via Chrome Sync)
- Profiles are encrypted at rest using Web Crypto (AES‑GCM) with a per‑device key
- Sensitive fields (e.g., passwords, tokens, SSN) are automatically ignored on capture
- Strict Content Security Policy for extension pages; no remote scripts

## Permissions

- `activeTab`: Interact with the current page when you capture/apply data
- `scripting`: Inject content scripts on demand to read/fill forms
- `storage`: Persist profiles and settings locally
- `notifications`: Optional user alerts for critical background errors

See PERMISSIONS_JUSTIFICATION.md for details.

## Install (Unpacked)

1. Download this repository
2. Open `chrome://extensions/`
3. Enable “Developer mode” (top‑right)
4. Click “Load unpacked” and select the project directory
5. Pin the extension and open the popup from the toolbar

## How to Use

### Create a Profile

1. Navigate to a page with forms and fill in your data
2. Open the extension → “Create New AutoFill”
3. Enter a profile name (you’ll review data before saving)
4. Click “Capture AutoFill Data”, review, optionally edit, then “Save Profile”

### Apply a Profile

1. Open the extension → “AutoFill Now”
2. Pick a saved profile
3. Optionally paste URLs (see limits below) and click “AutoFill Now”

### URL Autofill Modes

- Facebook/Instagram: auto‑detected; 30 URL limit; one URL per textarea if multiple are present
- TikTok: auto‑detected; de‑duplicated list pasted into the TikTok URL textarea
- Other sites: generic detection; 100 URL limit; URLs filled into URL‑related fields

## Validation Rules

- Only `http`/`https` URLs are accepted
- On Facebook/Instagram pages: only `facebook.com` or `instagram.com` URLs
- On TikTok pages: only `tiktok.com` URLs
- Limits: 30 (FB/IG) or 100 (default/TikTok)
- The popup disables the action button until inputs are valid

## Troubleshooting

- Button disabled? Check the URL counter message for validation errors or limits
- Nothing fills? Ensure the page isn’t a restricted scheme (e.g., Chrome Web Store)
- SPA pages sometimes need a re‑open of the popup after navigation
- Still stuck? Open DevTools Console for messages and try again

## Changelog (1.0.5)

- Added TikTok support with dedicated handling
- Profiles encrypted at rest (AES‑GCM via Web Crypto)
- Centralized sanitization and URL validation; stricter platform URL rules
- Safer popup rendering (no risky innerHTML for profile list)
- Listener guards for content scripts to avoid duplicate handlers
- UI refinements: review/edit before save, delete profiles, URL counters (30/100)

---
