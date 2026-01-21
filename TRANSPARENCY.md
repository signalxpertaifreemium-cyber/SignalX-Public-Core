# SignalX Transparency Statement

SignalX is currently in Private Beta. We open-source the Feature Contract and
Logic Documentation for community audit and reproducibility, while keeping the
core Execution Engine proprietary to mitigate front-running risks by
institutional bots and adversarial actors.

This balanced approach is intended to support scientific scrutiny without
exposing execution pathways that could be exploited to degrade performance or
harm users.

## Public Subset & Protocols

The Hugging Face dataset is a Public Subset of internal telemetry. The 17-dim
Market DNA is proprietary and is not released in full form. We provide a
curated slice for auditability without exposing live execution mechanics.

SignalX uses the T1 (Strict Closed Candle) protocol to eliminate look-ahead
bias by computing signals only after candle close. This enforces strict
temporal ordering for all features and prevents leakage from future data.

Roadmap: v9.0 NEON expands the forensic stack with OBI/VPIN monitoring for
institutional liquidity detection and adverse selection defense.
