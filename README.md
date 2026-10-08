# FO PICK public configuration repository

Public files for FO PICK / 포픽:

The final user-facing brand is **FO PICK / 포픽**. Repository names `fortune-app` and `fortune-app-config` and the existing public URLs remain unchanged.

- `faq.json` — Current Korean FAQ in the existing array format. All five original public IDs remain available, including `data-storage`.
- `faq-locales.v1.json` — Versioned FAQ content for `ko`, `en`, `ja`, `es`, `pt`, `fr`, `de`, `it`, `zh-Hans`, `zh-Hant`, `id`, and `vi`. Its shape is `{ schemaVersion: 1, locales: { [locale]: [{ id, question, answer }] } }`.
- `notices.json` — Notices; the initial development notice is disabled.
- `privacy-policy.html` — English Privacy Policy, intended to be served through GitHub Pages.

The Privacy Policy reflects local reading history, deletion, usage allowances, and reward access/transaction storage. History is not synchronized to a FO PICK server or account. Remote fortune content/config is not connected.

FO PICK integrates one Google AdMob banner at the bottom of Home and optional rewarded ads for two purposes: detailed access to that saved reading and one bonus regular reading after the three free periods are used. Banners are absent from selection, reveal, results, history, settings and FAQ screens. Basic readings do not require completing a rewarded ad. Additional FO PICK readings and ordinary interstitials are not provided. The policy documents SDK data handling, banner loading/refresh and rewarded preloading after UMP permits requests, privacy options, and that topic/mood and reading content are not directly supplied as ad targeting values.

The Android production App ID and three ad units are connected and verified locally in the app's ignored environment file and Expo configuration. Development uses official Google test ads. Native-device ad delivery, AdMob/UMP console validation and publication of these policy changes remain pending. This is not a claim that production ads or an updated public page are already live.

FO PICK v1 is free with a Home banner and optional rewarded ads. Premium is deferred to a later version; payment UI, SDK integration and entitlement access have been removed from the app. The policy removes the former Billing section and retains the existing AdMob/UMP, local history, usage and reward-storage disclosures.

The FAQ reflects local history, the 06:00 usage-day boundary, three regular time slots, one ad-earned regular bonus, optional rewarded detail access and the Home banner. Historical IDs `premium`, `subscription` and `restore` remain for compatibility; their visible text does not offer payments. Only the two advertising answers per language changed in this update. The multilingual file remains additive so older clients expecting the `faq.json` array are not broken. The app reads its bundled FAQ for the selected language; neither public FAQ file is fetched by the app. No notices were enabled or invented.

FAQ sources are maintained in the sibling app's `src/locales/faq.ts`. From `fortune-app`, `node scripts/sync-faq.cjs` exports the bundled Korean FAQ and both local public files. It does not publish. `node scripts/check-locales.cjs` checks that exports match their source. Translation content still needs native-speaker review.

The Privacy Policy remains one English page at the existing URL. Its verified developer contact is still missing. These local policy/FAQ changes have not been published. Korean traditional calendar context and seasonal events remain unimplemented.

## TODO

- Add a verified developer contact to the Privacy Policy before public release.
- Publish the reviewed policy and verify the existing GitHub Pages `privacy-policy.html` URL. Local edits alone do not update the public page.
- Verify AdMob/UMP console configuration, native-device Home banner and both rewarded placements, and interrupted reward-storage recovery before release. Local identifier and configuration checks have passed.
