# ⚙️ The Siphon Logic: From Noise to Signal

### The Filter Matrix
We utilize a three-tier filtering system to avoid the 'CVE Noise' problem:

| Tier | Name | Filter Criteria | Goal |
|---|---|---|---|
| 0 | **The Vacuum** | All OS-related CVEs | Raw Data Collection |
| 1 | **The Sieve** | CVSS >= 7.0 OR 'Remote' OR 'Privilege Escalation' | High-Signal Identification |
| 2 | **The Prism** | Mapping to known 'Primitive' patterns | Actionable Synthesis |

### Primitive Mapping Example
Instead of listing 50 different Buffer Overflows, Siphon-CVE aggregates them under:
**`Primitive: [Kernel-Heap-Corruption]`**
- *Pattern*: Mismatched size calculations in network drivers.
- *CVEs*: [CVE-A], [CVE-B], [CVE-C]...
- *Exploit Vector*: Memory grooming -> Overwrite function pointer -> Kernel-mode execution.
