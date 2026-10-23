# Taquería Los Pérez — five-location client demo

Prepared locally 2026-10-23. English/Spanish customer and administrative previews cover Riverdale, Baltimore, Laurel, Washington DC and Jessup. Four existing menu snapshots and prices are preserved. Jessup has its confirmed address, a menu-pending message and paused ordering; no menu or prices were invented.

Browser-only simulation: no payment API calls, live ordering links, card fields, kitchen printing, real staff authentication or restaurant fulfillment. Use sample contact details. Menu edits, photos and demo orders stay in this browser, not across devices. The server-backed local application is separate.

## Local startup

From this directory run `python3 -m http.server 8797 --bind 127.0.0.1` and open `http://127.0.0.1:8797/`. Staff preview: `staff.html`; it requires no real credentials. Close the server to stop it.

## Walkthrough

Choose each restaurant, check its address and own menu, switch English/Español, review item options and the bag, then explore staff item creation, editing, photo upload, modifier groups, availability and readable weekly hours. Jessup shows an empty menu pending confirmation. Existing browser edits survive the five-location upgrade; reset only to deliberately clear demo data.

## Verification and release boundary

`node tests/five-location-demo.cjs`: 25 offline checks pass for five profiles, separate menus/quotes, paused empty Jessup, invalid modifier groups, preserved older edits/orders, corrected addresses, translations and no live destinations. Browser checks verify both languages, all five addresses, Jessup’s pending state and Laurel’s 148-item menu. Native language-engine checks pass. Physical tablets, live Clover access, payments and printers remain unverified.

This five-location static release is intended for GitHub Pages at https://jedidiahbowlding.github.io/los-perez-riverdale-demo/. It is a simulation, not the Clover-connected backend. No restaurant DNS or account settings changed. Never copy backend environment files, credentials, vault or database into this repository.
