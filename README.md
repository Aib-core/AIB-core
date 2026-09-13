# AIB — Android Intelligence Bridge

**Modular Android AI-agent ecosystem**

> Evidence first. No guess. No blind action. No unnecessary rebuild.

## Architecture

```text
User Intent
    ↓
Brain — Reasoning / Planning
    ↓
Action Plan
    ↓
Permission / Policy Check
    ↓
Executor / AIC
    ↓
Android
    ↓
Eye — Observation
    ↓
Result
    ↓
Brain
```

### Core separation

- **AIB** — intelligence/bridge and modular ecosystem
- **AIC** — Executor / Agent Core
- **Brain** — reasoning, planning, decision-making
- **Eye** — observation through permitted Android mechanisms
- **Hand** — permitted, observable action execution
- **Android** — execution environment
- **User** — final authority

## Verification Policy

Nothing is declared `Working` without evidence.

| Level | Meaning |
|---|---|
| SOURCE VERIFIED | Source was actually located and inspected |
| BUILD VERIFIED | A real build completed successfully |
| INSTALL VERIFIED | APK installed successfully |
| RUNTIME VERIFIED | Required behavior was exercised |
| FEATURE VERIFIED | Specific requested feature passed its test |
| UNVERIFIED | Evidence is insufficient or test has not been run |
| BLOCKED | Progress is prevented by a documented root cause |

**Build success does not equal runtime success.**

## Current Baseline

The repository is currently an early project record. The initial repository commit contained only the default profile `README.md`; it did not contain the Android Voice Core source. Therefore this repository must not claim that any AIB Android module is currently working based on repository contents alone.

Known external source-recovery evidence has established an AIB Voice Core source archive as the current Voice Core source baseline. The next engineering gate is:

```text
Source Audit
→ Environment Audit
→ Real Build
→ Install
→ Runtime Test
→ Feature Verification
```

## Master Worker Protocol

See [`docs/AIB_MASTER_WORKER_PROTOCOL.md`](docs/AIB_MASTER_WORKER_PROTOCOL.md) for the complete engineering rules, module responsibilities, verification gates, security constraints, and reporting format.

## Module Roadmap

- [ ] Persian Voice-to-Text
- [ ] AIB Keyboard
- [ ] AIB Browser
- [ ] AIB Archive Manager
- [ ] AIB VPN Client
- [ ] AIB Telegram Client
- [ ] AIB AI Development Environment
- [ ] AIB Eye
- [ ] AIB Hand
- [ ] AIB Brain
- [ ] AIB Companion Core
- [ ] Integration

Unchecked items are **not claims of absence**; they mean the required evidence has not yet been recorded in this repository.

## Security

AIB must use permitted Android APIs and minimum necessary permissions. No security bypass, hidden access, credential harvesting, or secret committed to source control is permitted.

## Development Rule

```text
DISCOVER
→ VERIFY
→ AUDIT
→ MINIMAL CHANGE
→ BUILD
→ TEST
→ VERIFY
→ DOCUMENT
```

Healthy existing source takes priority over a new implementation.
