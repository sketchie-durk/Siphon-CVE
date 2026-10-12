# 🕯️ The Siphoner's Guide: Contributing to the Decay

To add to the Necronomicon, you must not simply report a bug. You must **synthesize a primitive**.

### The Synthesis Workflow
1. **The Vacuum**: Find a cluster of CVEs that feel "similar" despite different targets.
2. **The Distillation**: Identify the exact moment the system failed. Was it a TOCTOU? A Type Confusion? A state-machine contradiction?
3. **The Abstraction**: Strip away the specific function names. Describe the flaw as a logic error (e.g., "Trusting user-mode state after a privilege transition").
4. **The Projection**: Identify other areas of the OS where this same logic is likely implemented.

### Submission Standard
All entries in the `/grimoire` must follow the **Siphon Format**:
- **Primitive Name**: [The-Short-Name]
- **Root Cause**: The fundamental logic error.
- **Siphon Data**: The CVEs that prove the pattern.
- **Actionable Pattern**: How to find this in the wild.
