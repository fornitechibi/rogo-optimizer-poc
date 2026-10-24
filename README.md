# Image-optimizer delivery proof (authorized security research)

This repository hosts PoC assets for two authorized image-optimizer assessments.
Both images below are **rendered by GitHub from remote optimizer URLs** — the image
you see is fetched at view-time from each target's own `/_next/image` endpoint,
demonstrating the third-party embedding delivery.

## Rogo — image served from app.rogo.ai (cached 1 year, all tenant subdomains)

![rogo lure](https://app.rogo.ai/_next/image?url=https%3A%2F%2Fimages.crunchbase.com%2Fhttps%3A%2F%2Fraw.githubusercontent.com%2Ffornitechibi%2Frogo-optimizer-poc%2Fmain%2Flure-attacker-content.png&w=828&q=75)

## Ondo Perps — image served from app.ondoperps.xyz (cached 30 days)

![ondo lure](https://app.ondoperps.xyz/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2Fqr51tlj6%2Fproduction%2Ff50c6908f800c25f824fb5cb9bd114b476313c9c-1200x630.png&w=1200&q=90)

Both URLs are attacker-chosen content delivered through each product's public image
optimizer. Any platform that renders remote images (GitHub READMEs, chat unfurkers,
boards, email clients) displays this content without user interaction or download
prompts.
