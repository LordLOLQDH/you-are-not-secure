# YOU ARE NOT SECURE.

A privacy-education website that demonstrates what a normal website can learn from a browser visit.

## Features
- Live, local browser exposure report.
- Optional public-IP lookup. This explicitly contacts ipapi.co; that provider receives the visitor's IP address.
- Local URL structure inspector; it does not visit or scan the entered site.
- Signup data exposure simulator; checklist only, never asks for real personal data.
- Responsive light interface. No account, backend, analytics, cookies, or report upload implemented.

## Run
Open index.html or publish with GitHub Pages from main and the repository root.

## Privacy and limits
The browser report is computed locally. Hosting and network providers may still process connection metadata such as IP address and request headers. The optional IP lookup sends a request to ipapi.co. Approximate IP geolocation is not GPS.

This project does not read passwords, private files, messages, contacts, or exact GPS location. It does not request camera, microphone, or location permissions. The URL inspector parses text locally and does not scan arbitrary websites; browser CORS and security restrictions prevent a static page from freely inspecting other origins.

A real cross-site scanner would need a carefully designed backend or browser extension, explicit user consent, safe URL fetching, SSRF protections, rate limits, and clear limits around authenticated pages. Never collect credentials or attempt to bypass access controls.
