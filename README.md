# Backona CMP - Cookie Consent GTM Tag Template by [Backona](https://backona.com)

Google Tag Manager tag template for [Backona CMP](https://backona.com/product/cookie-consent-management). It sets Google Consent Mode defaults and loads the consent banner. Use both in one tag, or split them across two tags. Built by [Backona](https://backona.com).

Release history: [CHANGELOG.md](./CHANGELOG.md).

> **Not in the Community Template Gallery yet.** Until it is listed, install by importing [`template.tpl`](./template.tpl) from this repository (see below). Do not rely on searching the [Community Template Gallery](https://tagmanager.google.com/gallery) for now.

## Install

**Preferred method: import [`template.tpl`](./template.tpl)**

1. In Google Tag Manager, go to **Templates** → **Tag Templates** → **New**.
2. Open the menu (⋮) → **Import** → select [`template.tpl`](./template.tpl) from this repository → **Save**.
3. Create a tag from **Backona CMP - Cookie Consent**.

### Split setup (recommended)

| Tag | Options | Trigger |
|-----|---------|---------|
| Consent defaults | **Set consent defaults** on, **Load consent banner** off | **Consent Initialization — All Pages** |
| Consent banner | **Set consent defaults** off, **Load consent banner** on, set **Client ID** | **DOM Ready — All Pages** |

### All-in-one setup

1. Check **Set consent defaults** and **Load consent banner**.
2. Set **Client ID**. Optionally set language, Global Privacy Control, URL passthrough, and ads data redaction.
3. Trigger: **Consent Initialization — All Pages**.

**Later (after Google approval):** you will also be able to add the template from the [Community Template Gallery](https://tagmanager.google.com/gallery). Until then, use the `template.tpl` import above.

## What the tag does

**Set consent defaults** uses GTM consent APIs: default consent state, restore from the `cBModeMap` cookie, and Microsoft UET. Turn this off when defaults are already set elsewhere, for example `/api/default` in the page head.

**Load consent banner** injects `https://cmp.backona.com/api/consent` for the **Client ID**. An optional **Language code** is sent as `lang`.

When **Set consent defaults** is enabled:

- **Global Privacy Control (GPC)** keeps defaults denied when the browser sends a GPC signal and no saved consent cookie exists.
- **URL passthrough** passes ad click parameters in the URL on same-domain navigation when cookies are denied.
- **Ads data redaction** redacts ad-related identifiers in Google network requests when `ad_storage` is denied.
- **Extended consent parameters** can include `functionality_storage`, `personalization_storage`, and `security_storage`.

## Support

Report bugs or request features via [GitHub Issues](https://github.com/backona/gtm-cmp-cookie-consent/issues) on this repository.
