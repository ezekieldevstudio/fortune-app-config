# FO PICK public configuration repository

Public files for FO PICK / 포픽:

The final user-facing brand is **FO PICK / 포픽**. Repository names `fortune-app` and `fortune-app-config` and the existing public URLs remain unchanged.

- `faq.json` — Current Korean FAQ in the existing array format. All five original public IDs remain available, including `data-storage`.
- `faq-locales.v1.json` — Versioned FAQ content for `ko`, `en`, `ja`, `es`, `pt`, `fr`, `de`, `it`, `zh-Hans`, `zh-Hant`, `id`, and `vi`. Its shape is `{ schemaVersion: 1, locales: { [locale]: [{ id, question, answer }] } }`.
- `notices.json` — Notices; the initial development notice is disabled.
- `privacy-policy.html` — English Privacy Policy, intended to be served through GitHub Pages.

The Privacy Policy reflects local reading history, deletion, usage allowances, and reward access/transaction storage. History is not synchronized to a FO PICK server or account. Remote fortune content/config is not connected.

Stage 9 integrates optional Google AdMob rewarded ads for detailed-reading access and one bonus regular reading after the three free periods are used. It documents SDK data handling, preloading, UMP consent/privacy choices where applicable, and that topic/mood and reading content are not directly supplied as ad targeting values. Basic readings do not require watching ads. FO PICK replays, banners, and interstitials are not provided.

The advertising SDK integration and local dependency installation checks are complete; native-device validation, production ad configuration, and policy publication are still pending. This is not a claim that production ads or an updated public page are already live.

FO PICK v1 is free with optional rewarded ads. Premium is deferred to a later version; payment UI, SDK integration and entitlement access have been removed from the app. The policy removes the former Billing section and retains the existing AdMob/UMP, local history, usage and reward-storage disclosures.

The FAQ reflects local history, the 06:00 usage-day boundary, three regular time slots, one ad-earned regular bonus and optional rewarded detail access. Historical IDs `premium`, `subscription` and `restore` remain for compatibility, but their visible questions and answers now explain free use, optional ads and retrying reward storage. They do not offer payments. The multilingual file is a separate additive endpoint so older clients expecting the `faq.json` array are not broken. The current app still reads its bundled Korean FAQ; neither public FAQ file is fetched by the app. Multilingual FAQ content is ready for integration, not proof of complete multilingual app support. No notices were enabled or invented.

FAQ sources are maintained in the sibling app's `src/locales/faq.ts`. From `fortune-app`, `node scripts/sync-faq.cjs` exports the bundled Korean FAQ and both local public files. It does not publish. `node scripts/check-locales.cjs` checks that exports match their source. Translation content still needs native-speaker review.

The Privacy Policy remains one English page at the existing URL. Its verified developer contact is still missing. These local policy/FAQ changes have not been published. Korean traditional calendar context and seasonal events remain unimplemented.

## TODO

- Add a verified developer contact to the Privacy Policy before public release.
- Publish the reviewed policy and verify the existing GitHub Pages `privacy-policy.html` URL. Local edits alone do not update the public page.
- Verify production ad identifiers, UMP configuration, native-device rewarded advertising and interrupted reward-storage recovery before release.
