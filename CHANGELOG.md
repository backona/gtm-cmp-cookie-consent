# Changelog

All the project changes should be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Do not edit the NEW_VERSION and VERSION_DATE fields, they will be updated automatically by the Github Action script.

## [<NEW_VERSION>] - <VERSION_DATE>
### Added
- Backona CMP - Cookie Consent GTM tag template: Consent Mode defaults and consent banner, together on one tag or split across two tags
- Consent defaults cover Google Consent Mode, `cBModeMap` cookie restore, Microsoft UET, optional GPC, URL passthrough, ads data redaction, and extended storage types
- Banner loader injects the Backona CMP script for a Client ID, with an optional language code
