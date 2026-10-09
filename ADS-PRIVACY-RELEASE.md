# Apple Ads privacy release candidate — October 9, 2026

These are draft policies for the attribution source updates in [Meme Vault PR 1](https://github.com/IsaiahDupree/MemeVault/pull/1), [Kawaii Coffee Timer PR 1](https://github.com/IsaiahDupree/KawaiiCoffeeTimerNative/pull/1), and [Relay PR 1](https://github.com/IsaiahDupree/Relay/pull/1). No website deployment or App Store privacy publication is performed by this branch.

The three integrations use RevenueCat's anonymous customer identity and Apple AdServices. They do not supply custom account IDs, emails, IDFA, or app content to this integration. The public copy describes purchase validation, acquisition analytics, provider retention, local-content boundaries and platform/version differences. Kawaii's existing Supabase account and diagnostic disclosures remain in place. Relay's previous claim of no retained data was inconsistent with its existing RevenueCat billing integration and is corrected.

Before enabling or releasing the associated code:

1. Review the complete signed app/extension privacy report and publish matching App Store answers. Native purchase history is declared for app functionality and analytics; Apple advertising data is declared for analytics. Preserve each app's other categories.
2. Publish and verify the reviewed app-specific pages. Meme Vault's new path is `/meme-vault/privacy/`; its current live metadata URL still points to the general policy. Apply the new metadata URL only after the new page is live.
3. Verify the final version's build configuration, real purchase/restore/refund flow and attribution identity. Do not treat anonymous identifiers as a promise that no data is collected.

Mac apps and Meme Vault's share extension do not gain the new iOS measurement integration. No ads are displayed in the apps by this work. No new campaign or spending is authorized.

Validation: the four changed/new HTML pages parse successfully, links to the new Meme Vault page resolve to a source file, and `git diff --check` passes. Browser rendering and live publication remain separate checks.
