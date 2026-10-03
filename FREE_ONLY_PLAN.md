# Free-only review — 2026-10-03

## User requirements

Use Windows without owning a Mac. Avoid paid services and do not rely on a monthly free build-minute allowance. Keep the POS project separate.

## Changes completed

- Retain the existing separate `phut-laew-tuean-ios` repository. No new GitHub account is required.
- The user explicitly approved public source disclosure for this app only. GitHub email verification completed and the repository was confirmed public on 2026-10-03. The POS repository was not changed.
- Public hosted build run #3 succeeded on 2026-10-03: https://github.com/topzonenet999-collab/phut-laew-tuean-ios/actions/runs/37126169965, workflow commit `2f82e6a`. Simulator and Release iPhone device compilations passed, all three processed permission descriptions passed validation, and the unsigned IPA plus SHA-256 were saved in a draft GitHub Release. Total run time was 1 minute 28 seconds.
- No paid build provider, Apple Developer subscription, paid AI API or new domain has been configured for this native app.

## Available native route

1. This app repository is now public with the user's approval. Everyone can view and download its source and history. It contains app source, workflow, icon and documentation; no POS source is included.
2. Use GitHub's standard macOS runner. GitHub documents free unlimited build minutes for public repositories. This removes the private repository's monthly minute allowance, but does not remove operational limits or all storage limits.
3. Run #3 successfully compiled both simulator and Release iPhone device targets, validated nonempty `NSAlarmKitUsageDescription`, `NSMicrophoneUsageDescription`, and `NSSpeechRecognitionUsageDescription` in the processed app, and saved the unsigned IPA plus SHA-256 in a draft GitHub Release. It uses neither Actions artifact storage nor a build cache. The draft has not been published as a public release; the unsigned package still needs personal signing before installation.
4. A Windows AltServer/AltStore personal install may avoid buying a Mac or paid Apple membership. A free Apple Account's signing expires after seven days and allows three installed apps per device. Actual phone installation, refresh and AlarmKit behavior have not yet been tested. Do not describe this as a permanent commercial installation.
5. Standard App Store distribution still requires Apple Developer Program membership; it is not a free replacement available for this project.

## Existing website

The deployed website uses Cloudflare Pages plus Workers and D1 for closed-app Web Push. This is a zero-dollar free tier with usage limits, not unlimited free infrastructure. It cannot be replaced with a browser-only solution that also provides reliable closed-app alarms on iPhone. No backend shutdown was performed because that would remove the working notification feature.

The native app schedules AlarmKit locally and stores reminders locally. Once signed and installed, alarm execution has no Cloudflare server dependency.

## Alternatives for personal use

Built-in iPhone Clock alarms need no developer account or custom app hosting. Apple Reminders on iOS 26.2+ supports Urgent alarms at the reminder's due date/time, but requires iCloud Reminders and retains iCloud storage limits. These are existing Apple apps, not this custom app for sale.

## Official references

- GitHub standard public runners: https://docs.github.com/en/actions/reference/runners/github-hosted-runners
- GitHub billing: https://docs.github.com/en/billing/concepts/product-billing/github-actions
- Windows AltStore installation: https://faq.altstore.io/altstore-classic/how-to-install-altstore-windows
- Apple free personal signing limits: https://developer.apple.com/help/account/basics/about-your-developer-account
- Apple membership and distribution: https://developer.apple.com/support/compare-memberships/
- Cloudflare Workers limits: https://developers.cloudflare.com/workers/platform/limits/
- Cloudflare D1 pricing: https://developers.cloudflare.com/d1/platform/pricing/
- Apple Urgent Reminders: https://support.apple.com/en-gb/102484
