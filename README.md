# FO PICK public configuration repository

Public files for FO PICK / 포픽:

The final user-facing brand is **FO PICK / 포픽**. Repository names `fortune-app` and `fortune-app-config` and the existing public URLs remain unchanged.

- `faq.json` — Korean FAQ.
- `notices.json` — Notices; the initial development notice is disabled.
- `privacy-policy.html` — English Privacy Policy, intended to be served through GitHub Pages.

The Privacy Policy reflects local reading history, deletion, usage allowances, and reward access/transaction storage. History is not synchronized to a FO PICK server or account. Remote fortune content/config is not connected.

Stage 9 integrates optional Google AdMob rewarded ads for detailed-reading access and one bonus regular reading after the three free periods are used. It documents SDK data handling, preloading, UMP consent/privacy choices where applicable, and that topic/mood and reading content are not directly supplied as ad targeting values. Basic readings do not require watching ads. FO PICK replays, banners, and interstitials are not provided.

The advertising SDK integration and local dependency installation checks are complete; native-device validation, production ad configuration, and policy publication are still pending. This is not a claim that production ads or an updated public page are already live.

Stage 10 activates Google Play Billing integration in the app source for optional **one-time, non-consumable lifetime Premium**, with no subscription. SDK installation, Play Console product creation/activation and real purchase validation are still pending; live paid availability is not claimed. Google Play processes payments. The policy now describes minimal local entitlement caching, ownership refresh/restore, and Premium removing rewarded-ad requirements for details and the shared daily bonus, without changing reading outcomes. Existing AdMob/UMP and local-history disclosures remain.

The remote FAQ still contains early development descriptions and must be reviewed against the app before remote FAQ integration; it is not connected to the current app. Remote fortune content/config remains unconnected.

## TODO

- Add a verified developer contact to the Privacy Policy before public release.
- Publish the reviewed policy and verify the existing GitHub Pages `privacy-policy.html` URL. Local edits alone do not update the public page.
- Complete the app README's Billing installation, Play Console setup and license-tester checks before enabling public purchases.
