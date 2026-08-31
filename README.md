# OOKA_thankyou

> 3LI Global — AIR Global integration estate. Generated 2026-08-31 by the US-Infrastructure audit. Facts below are drawn from this repo's code; anything not directly evidenced is marked _unverified_.

## Connected Resource
- **Azure resource:** none — single static HTML page (no `.github/workflows`, no Azure config, no form)
- **Deploy trigger:** _unverified_ — no CI/CD workflow is committed; hosting is external to this repo
- **Talks to:**
  - Loads one image asset from HubSpot's CDN: `https://25636661.fs1.hubspotusercontent-eu1.net/hubfs/25636661/check-mark-circular-black-lineal-16220.svg` (HubSpot portal **25636661**, AIR Global's UAE/OOKA HubSpot). No form submission or API call of its own.

## What It Does
A static confirmation ("thank you") page. It centres a check-mark icon and the text "THANK YOU! YOUR MESSAGE HAS BEEN SENT".

## Why It Exists
It is the post-submission acknowledgement page for an OOKA web form — the destination a visitor lands on (or which is embedded) after a support/contact form is submitted. It complements the OOKA form repos (`OOKASupport` / `OOKASupportForm` / `OOKA-Horeca-USA-Form`) in the same estate, which capture into Zoho; this page is the visual "sent" confirmation, styled with the OOKA Brandon Grotesque font and a HubSpot-hosted checkmark. _Unverified:_ which specific form(s) redirect here (the OOKA forms in this estate leave `zf_redirect_url` empty in-repo).

## How It Works
1. `index.html` renders a single centred panel: a check-mark SVG (pulled from the HubSpot CDN) above an uppercase confirmation message.
2. All styling is inline/`<style>`; there is no JavaScript, no form, and no dynamic behaviour.
- **Operator note:** the only external dependency is the HubSpot-hosted SVG; if that asset moves, the icon breaks.

---
_Environment:_ Production (single public confirmation page — inferred)
_Runtime:_ static HTML (no CSS/JS files, no server component)
