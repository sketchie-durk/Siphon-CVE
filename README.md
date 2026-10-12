# 💀 Siphon-CVE: The Necronomicon of OS Vulnerabilities

`Siphon-CVE` is not a vulnerability database. It is a high-agency synthesis engine designed to strip the noise from the NVD and extract the raw, actionable primitives of OS failure.

## 👁️ The Philosophy: Primitive over Patch
Most CVE feeds are graveyard listings—static records of what was fixed. **Siphon-CVE** treats vulnerabilities as **Primitives**. We don't care that `CVE-202X-XXXX` was patched; we care that the *logic* allowing the exploit is a recurring pattern in the OS kernel.

### The Siphon Pipeline
1. **Ingest**: Vacuuming raw data from NVD, OSV.dev, and GitHub Advisories.
2. **Distill**: Stripping the bureaucratic language to find the "breaking point" (e.g., "Heap Overflow in IOCTL handler").
3. **Synthesize**: Mapping the bug to a class of failure (Memory Corruption, Logic Flaw, Race Condition).
4. **Project**: Predicting where similar primitives likely exist in related OS versions.

## 🏗️ Architecture
- `/siphons`: The vacuum tubes. Specialized extractors for different data streams.
- `/synthesis`: The reasoning core. Where CVEs are converted into primitives.
- `/grimoire`: The living record of synthesized OS vulnerabilities, categorized by attack surface.
- `/deploy`: The sentinel configuration. Cron-driven autonomous monitoring.

## 🛠️ Operational State
Currently in **Alpha-Omega Phase**. The engine is designed for autonomous operation:
- **High-Signal Mode**: Only reports critical primitives with reachable exploit vectors.
- **Comprehensive Mode**: Maps the entire landscape of OS decay.

---
*Built by STOOLAR. Unauthorized use is encouraged; blindness is the only crime.*
