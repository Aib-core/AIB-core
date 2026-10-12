# AIB Keyboard + Persian Voice — UI and Interaction Specification v1

Status: SPECIFICATION DRAFT — implementation and runtime behavior are not yet verified.
Branch: aib/master-protocol-v1

## 1. Scope

Define the first user-facing requirements for the AIB Keyboard and Persian voice-to-text flow. Keep keyboard UI requirements separate from the standalone AIB Voice app MVP. The standalone voice app remains the first executable milestone; keyboard integration follows after the voice flow is tested.

## 2. Persian voice-to-text flow

1. User taps the keyboard microphone.
2. The app captures Persian speech and converts it to Persian text.
3. The transcript is inserted into the current text field when the host app permits it.
4. Sending is a separate step from transcription:
   - Prefer the host app's supported direct-send action only when it is available and permitted.
   - If direct send is unavailable, leave the transcript ready for review; use Enter only where the host app's behavior is known and the user has enabled/approved that behavior.
5. Show meaningful recording, processing, success, empty-result, permission-denied, offline, and recognition-error states.
6. Never claim transcription or sending succeeded without observing the result.

## 3. Recognition modes

- Design for five selectable Persian speech-recognition modes.
- Include lightweight modes suitable for lower-resource phones, including Samsung Galaxy A15 4G.
- Exact mode names, model/provider mapping, network requirements, and performance costs remain TBD until verified.
- Do not assume the heaviest mode will run acceptably on the target phone without testing.

## 4. Keyboard layout requirements

- Separate Persian and English letter layouts/pages.
- Provide a dedicated numbers-and-symbols page, with expanded symbols and mathematical operators.
- Keep number keys and symbol keys distinct where specified; do not collapse them into one ambiguous key.
- Include accessible keys/actions for #, @, punctuation, and common symbols.
- Include dedicated entry points for voice input, search, and translation.
- The first/primary page should prioritize ordinary typing; symbol and mathematical characters should be easy to reach through a clear page switch.
- Preserve predictable page switching and key positions across Persian and English layouts where practical.
- Exact key positions and final page hierarchy must be validated against the user's reference image before implementation.

## 5. Visual identity

- Preserve the intended logo silhouette and overall keyboard structure from the user's reference; do not redraw or rename the identity by assumption.
- Final logo, detailed shapes, animation, and color palette are a separate design stage after the structure and interaction requirements are agreed.
- No final colors or logo geometry are locked by this specification.
- Do not copy another keyboard's assets; references may inform layout principles only.

## 6. Acceptance checklist

- [ ] Persian typing works.
- [ ] English typing works.
- [ ] Number/symbol page works and includes #, @, punctuation, and mathematical symbols.
- [ ] Microphone permission and recording states work.
- [ ] Persian speech produces editable text.
- [ ] Empty results and recognition errors are handled.
- [ ] Transcript can be copied and inserted into the active field.
- [ ] Direct send is used only when supported; otherwise the transcript remains ready for review.
- [ ] Enter fallback is tested per target host app and is not assumed to mean “send” universally.
- [ ] Lightweight recognition mode is tested on Galaxy A15 4G.
- [ ] UI matches the user's reference image after that image is available for inspection.
- [ ] Build, install, runtime, and feature tests are reported separately with evidence.

## 7. Evidence and status policy

Until real implementation and tests are available, all behavior above is a requirement, not a claim that it already works. Report each acceptance item as PASS, FAIL, BLOCKED, or NOT TESTED, with evidence.
