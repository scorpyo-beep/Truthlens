# TruthLens — GitHub Pages Starter

TruthLens is a mobile-friendly fact-checking app prototype. It helps users identify claims, open research searches, keep local review notes, and use a transparent source-transparency checklist.

## Included in this starter

- `index.html` — complete responsive app (HTML, CSS, JavaScript in one file)
- No build tools or package installation required
- Local check history saved in the current browser using `localStorage`
- Claim extraction heuristics for pasted text
- Research links to web search, Google Fact Check Explorer, and Google News
- Source transparency checklist with a clearly labeled checklist score
- Navigation for Check a Claim, Source Ratings, My History, and How It Works

## Run it locally

Open `index.html` in a browser, or open the project in SPCK Editor on Android.

## Publish with GitHub Pages

1. Create a new GitHub repository, for example `truthlens`.
2. Upload `index.html` and `README.md` to the repository's root.
3. In GitHub, open **Settings → Pages**.
4. Under the build/deployment section, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)` folder, then save.
6. Wait for GitHub Pages to publish the site. Open the URL shown in Settings → Pages.

## Important: prototype versus real verification

This is a static front-end prototype. It **does not automatically establish truth or falsity**. It prepares research links and gives you a structured way to record evidence. A real production fact-checking system needs a server-side backend to:

- fetch and safely extract article content (with SSRF protections, allowlists/denylists, timeouts, and content-size limits)
- call fact-check databases and other APIs
- transcribe audio/video where permitted
- extract claims with an AI model
- retrieve and compare primary evidence
- generate assessments tied to specific citations and dates
- log uncertainty, provenance, corrections, and model limitations
- rate-limit requests and protect against abuse

**Never put private API keys in `index.html`, browser JavaScript, or a public GitHub repository.** GitHub Pages is static hosting and cannot safely keep secrets. Add a backend (for example, a small Node.js API deployed to a server platform) before integrating paid AI services or private API keys.

## Recommended result labels

- Supported by available evidence
- Contradicted by available evidence
- Misleading / missing context
- Unverified / insufficient evidence
- Opinion / prediction / not objectively checkable

Avoid presenting an unsupported numeric “truth score.” Source ratings should disclose their methodology, evidence base, sample size, time window, and uncertainty. Keep factual accuracy, transparency, political perspective, and writing style as separate dimensions.

## Suggested next development phases

1. Backend API with a `/api/check` endpoint.
2. Google Fact Check API integration (API key stored on the server).
3. Evidence cards that show publisher, headline, date, excerpt, and direct URL.
4. Server-side article extraction and claim-level citations.
5. Speech/video upload and transcription.
6. Accounts and cloud-synced history, with clear privacy controls.
7. Independent methodology review and security testing before public launch.

## Privacy note

This prototype saves history and notes in the browser on the device being used. Clearing browser site data may delete it. It does not currently sync across devices.
