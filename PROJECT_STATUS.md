# Project status: Unwind App

## Summary

- **Status:** In progress
- **Started:** 2026-09-04 AEST
- **Last updated:** 2026-09-04 AEST
- **Completed:** Not complete
- **Project directory:** `/Users/sabrina/Documents/Codex/projects/unwind-app`
- **GitHub repository:** https://github.com/sabrinabettini/unwind-app
- **Branch:** `main`
- **Latest commit:** `83100fdf9395625b5feb4bbb36a7404834856dc3`

## Goal

Create a calm, low-friction wellbeing app for moments when a user feels anxious or overwhelmed. It offers short breathing, grounding, body-scan, journaling, and ambient sessions based on how the user feels, without positioning itself as medical treatment.

## Agreed product direction

- **Tone:** Warm, human, reassuring, and concise; never clinical, patronising, or falsely cheerful.
- **Privacy:** Journal entries saved locally on the device by default. The UI must explain that local storage is not automatically encrypted and provide clear delete/export controls.
- **Platform:** Mobile-first installable web application/PWA, with desktop support and no backend required for the first release.
- **Sensory scope:** No audio, ambient sound, music, spoken guidance, or autoplay in the MVP.

## Current scope under discussion

- A minimal emotional check-in that recommends one exercise without requiring diagnosis.
- Short, optional breathing exercises with an immediate switch to non-breath-based grounding.
- Sensory grounding, body scan or muscle release, journal prompts, and silent visual sessions.
- Clear duration choices, pause/skip/stop controls, reduced-motion support, and no success/failure scoring.
- Local-first private journaling and transparent data handling.
- Calm but accessible safety/support information appropriate to the user's region.

## Product boundaries

- Not medical treatment, diagnosis, therapy, crisis care, or a replacement for professional support.
- No claims that an exercise will stop panic, regulate the nervous system, or work for everyone.
- No forced breath holds, competitive streaks, guilt-based reminders, or emotional surveillance.

## Current checkpoint

The first meaningful mobile-first preview is built in `app/`: welcome, low-pressure check-in, duration selection, recommendation, and a complete text-only grounding flow with stop/skip paths. The production build passes. The agreed content governance, Australia-only adult scope, local-data boundaries, and accessibility requirements remain in force.

## Next action

Implement the local IndexedDB journal, expanded practice library, support and settings screens, then add PWA/offline behaviour and verification.

## Interaction log

| # | Started | Finished | Approx. duration | Model / reasoning | Exact tokens | Work completed | Learning / decisions |
|---:|---|---|---:|---|---:|---|---|
| 1 | 2026-09-04 AEST | In progress | In progress | GPT-5 / Not available | Not available | Started product sparring; defined initial wellbeing and safety boundaries | Reduce decisions during overwhelm and route by present experience rather than diagnosing an emotion |
| 2 | 2026-09-04 AEST | 2026-09-04 AEST | Less than 1 minute | GPT-5 / Not available | Not available | Chose a warm human tone, local journal storage and a mobile-first product | A PWA is the best first-release fit, but local-only storage must not be described as encrypted unless encryption is implemented |
| 3 | 2026-09-04 AEST | 2026-09-04 AEST | Not available | GPT-5 / Not available | Not available | Removed audio and spoken guidance from the MVP and created a complete model-handover review/build plan | A silent, text-led MVP reduces sensory load, licensing, autoplay, accessibility, and offline-size complexity |
| 4 | 2026-09-04 AEST | 2026-09-04 AEST | Not available | GPT-5 / Not available | Not available | Reviewed the handover plan for product safety, privacy, PWA and delivery gaps | The core scope is sound; implementation risk now lies in omitted operational detail rather than missing features |
| 5 | 2026-09-04 AEST | 2026-09-04 AEST | Not available | GPT-5 / Not available | Not available | Added the plan-review amendments and new acceptance criteria to the handover plan | Content governance, interruption behavior, local-storage failures and browser-specific PWA behavior need explicit requirements before implementation |
| 6 | 2026-09-04 AEST | In progress | In progress | GPT-5 / Not available | Not available | Began implementation and scaffolded the site project | First delivery slice is the check-in and a grounding practice, retaining the approved safety, privacy and accessibility boundaries |
| 7 | 2026-09-04 AEST | 2026-09-04 AEST | Not available | GPT-5 / Not available | Not available | Built and verified the first meaningful preview: check-in, duration, recommendation and text-only grounding flow | A single responsive PWA surface will serve iOS Safari and Android Chrome; platform-specific storage and install behaviour will be handled in later verification |
| 8 | 2026-09-04 AEST | 2026-09-04 AEST | Not available | GPT-5 / Not available | Not available | Attempted to launch and inspect the iOS Simulator for PWA testing | This environment has an incomplete Xcode installation: the Simulator executable and CoreSimulator service are unavailable |
| 9 | 2026-09-04 AEST | 2026-09-04 AEST | Not available | GPT-5 / Not available | Not available | Reworked the initial visual palette and production-verified the change | The first colour change was too subtle; the current direction uses visibly distinct pale aqua, blush, deep teal and coral |
| 10 | 2026-09-04 AEST | 2026-09-04 AEST | Not available | GPT-5 / Not available | Not available | Replaced the formal type treatment with a friendly rounded system-font stack | Local system fonts preserve the no-external-network-data boundary while giving the product a warmer voice |
| 11 | 2026-09-04 AEST | 2026-09-04 AEST | Not available | GPT-5 / Not available | Not available | Replaced the placeholder single-practice routing with a deterministic feeling/duration matrix and distinct practice library | The first slice had incorrectly sent all routes to the same grounding flow; the current preview now has multiple modality-specific exercises and a breathing-to-grounding exit |
| 12 | 2026-09-04 AEST | 2026-09-04 AEST | Not available | GPT-5 / Not available | Not available | Added a five-finger breathing practice with a text-led tracing guide | Breathing is always optional, unpaced and has an immediate grounding alternative; the guide avoids a moving visual or mandatory breath timing |
| 13 | 2026-09-04 AEST | 2026-09-04 AEST | Not available | GPT-5 / Not available | Not available | Changed duration routing from a label-only choice into progressively longer practice sessions | Thirty seconds gives one concise practice; two minutes adds one extra small practice; five minutes and untimed choices offer a three-practice sequence, always one screen at a time and skippable |
| 14 | 2026-09-04 AEST | 2026-09-04 AEST | Not available | GPT-5 / Not available | Not available | Removed unimplemented Journal and Settings navigation from the footer | The navigation now exposes only working Today and Practices flows until the local journal and settings are implemented |
| 15 | 2026-09-04 AEST | 2026-09-04 AEST | Not available | GPT-5 / Not available | Not available | Diagnosed stale local preview servers that kept serving an earlier purple stylesheet and restarted the app with cache re-optimisation | Future preview changes must be verified against the actual served CSS/asset rather than only the edited source or production build |
| 16 | 2026-09-04 AEST | 2026-09-04 AEST | Not available | GPT-5 / Not available | Not available | Created and pushed the public GitHub repository | The public `main` branch was pushed through an authenticated HTTPS remote; generated build files and the local dependency link were excluded |

## Issues and risks

- Breath-focused exercises can feel uncomfortable or intensify distress for some people; every breathing flow needs a visible alternative.
- Journals may contain highly sensitive information and should remain local by default.
- Audio is deliberately excluded from the MVP because it may be overwhelming and adds licensing, autoplay, accessibility, and offline-size risks.
- “Unwind” is descriptive and may not be sufficiently distinctive as a final product name; availability should be checked before publishing.
- Crisis information must be accessible without making every ordinary use feel like a clinical emergency.
- iOS Simulator testing is blocked in this environment because Xcode/Simulator is not installed as a runnable application; physical-device and simulator validation remain required before release.

## Technologies, portfolio record, and ideal prompt

To be completed after product scope and implementation choices are agreed.
