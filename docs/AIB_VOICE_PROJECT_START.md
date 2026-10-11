# AIB Voice — Independent Android App (Project Kickoff)

## Project identity
- **Display name:** AIB Voice
- **Technical project name:** AIB Voice Core
- **Android application ID (provisional; confirm before implementation):** `com.aib.voice`
- **Repository:** `Aib-core/AIB-core`
- **Working branch:** `aib/master-protocol-v1`
- **Status:** PROJECT KICKOFF RECORDED — SOURCE / BUILD / APK / RUNTIME NOT VERIFIED

## Purpose
Build a **standalone Android application first** for Persian speech-to-text. Only after the standalone app is built and tested should its capability be integrated into the wider AIB ecosystem.

## MVP
1. Request microphone permission through the official Android permission flow.
2. Start and stop speech recognition using a permitted Android API.
3. Prefer Persian (`fa-IR`) when supported by the recognition provider/device.
4. Display recognized text clearly.
5. Let the user copy the result.
6. Show useful permission, unavailable-service, network, and recognition error states.
7. Never claim a feature works until it has been tested on a real device or emulator.

## Scope boundary
**Phase 1 — Standalone app only**
- Android app identity and project structure
- Persian speech recognition
- Text display and copy
- Permission and error handling
- Build an APK
- Install and test on the target Android device

**Phase 2 — AIB integration, only after Phase 1 verification**
- Define a small interface for sending recognized text to AIB
- Keep the standalone app usable without AIB
- Do not introduce Brain, Eye, Hand, Keyboard, or other modules during Phase 1

## Required engineering sequence
DISCOVER AVAILABLE SOURCE → VERIFY PROJECT IDENTITY → AUDIT ENVIRONMENT → CREATE MINIMAL PROJECT ONLY IF NO USABLE SOURCE EXISTS → BUILD → VERIFY APK → INSTALL → RUNTIME TEST → TEST REAL PERSIAN SPEECH → DOCUMENT EVIDENCE.

The current repository has no verified Android Voice source files. Before writing implementation code, inspect all explicitly available project/archive locations for an existing source archive. If none is accessible, record the search scope and then create the minimal standalone project in this repository—do not pretend recovered source exists.

## Acceptance criteria
- [ ] Android project files exist in the repository
- [ ] Build succeeds in a verified environment
- [ ] APK artifact exists and is inspected
- [ ] APK installs on the target device/emulator
- [ ] App launches without crashing
- [ ] Microphone permission flow behaves correctly
- [ ] Persian speech produces Persian text on a real test
- [ ] Text can be copied
- [ ] Errors are visible and do not crash the app
- [ ] Evidence and limitations are documented
- [ ] Only after all required Phase 1 checks pass: plan AIB integration

## Search keywords
AIB Voice, AIB Voice Core, Persian speech-to-text, Persian voice typing, Android speech recognition, `fa-IR`, SpeechRecognizer, microphone permission, Kotlin, Android app, standalone APK, text display, copy transcript, offline capability (investigate; do not promise), runtime verification.

## Reporting rule
For each criterion, report PASS / FAIL / BLOCKED / NOT TESTED and include evidence. A project document or unchecked checklist is not proof of implementation.

## Immediate next action
Perform a bounded source/archive search and environment audit. Then report whether usable source was found. If no usable source is found, proceed with an explicitly documented minimal standalone Voice app; do not block indefinitely on planning.
