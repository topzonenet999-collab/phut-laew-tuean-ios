# iOS cloud build status

Verified on 2026-10-03:

- Public repository: https://github.com/topzonenet999-collab/phut-laew-tuean-ios
- Successful run #3: https://github.com/topzonenet999-collab/phut-laew-tuean-ios/actions/runs/37126169965
- Workflow commit: `2f82e6a`.
- Runner: `macos-26`.
- Simulator compilation: Success, with signing disabled.
- iPhone device compilation: Success, Release configuration, with signing disabled.
- Processed app permission checks: Success for nonempty `NSAlarmKitUsageDescription`, `NSMicrophoneUsageDescription`, and `NSSpeechRecognitionUsageDescription`.
- Packaging: Unsigned IPA and SHA-256 saved successfully in a draft GitHub Release.
- Result: Success; total duration 1 minute 28 seconds, job duration 1 minute 19 seconds.
- Draft release: https://github.com/topzonenet999-collab/phut-laew-tuean-ios/releases/tag/untagged-3756f5b0fe44cb797e9b
- IPA downloaded to the Windows Downloads folder and copied to `ios-upload/PhutLaewTuean-unsigned.ipa`. Its SHA-256 matches the release asset: `02971f40f0cc8b314c949335f4e0792fb14e9d99d3875bef962b2731cb41102a`.

## Using Windows

The public repository contains `ios-source.zip`. Extract it to obtain the Xcode project and Swift source files. The root GitHub workflow extracts the same archive before compilation. To repeat the compiler check, open Actions → Build iOS app → Run workflow → main.

On 2026-10-03 the user approved making this app's source public. The repository is now public and run #3 completed on GitHub's standard macOS runner. The POS repository was not changed. This build does not use the private repository's monthly build-minute allowance.

The workflow runs only when manually requested and has a 15 minute timeout. Default repository permissions are read-only; the build job has `contents: write` to save its package in a draft release. GitHub's documented free unlimited monthly build minutes apply to standard runners in public repositories; execution, concurrency and storage limits still apply. Creating another GitHub account is unnecessary and does not remove a private repository's limits.

## Still required before use or sale

The successful simulator and Release device compilations produce an unsigned IPA. The draft release is available to the repository owner, and has not been published as a public release. The package still needs personal signing and installation on an iPhone. Actual phone installation and alarm testing have not been completed. This is not an App Store release.

The next free personal-device route to test is Windows AltServer/AltStore with an Apple Account, signing the IPA for an iPhone 11 running iOS 26 or later. Free personal signing expires after seven days and requires refresh. A borrowed Mac with Xcode is another option. Paid Apple Developer membership is a separate option for distribution, not configured here.

On the real phone, verify microphone/speech permission, AlarmKit permission, a two-minute alarm with the app closed and screen locked, the title displayed, the Stop control, and cancellation when deleting a future reminder. No personal-device test has been completed yet.
