# 🗺️ The Universal Decay Map: Async-Era Primitives

## ⚡ Primitive: [The Async-State-Desync]
**Observed in**: Linux (`io_uring`), Windows (`IOCP`), macOS (`kqueue`/`GCD`).

### Synthesis
The industry has moved toward asynchronous I/O to maximize throughput. The primitive is the **State Desync**: a race condition where the asynchronous request is submitted, the state is modified by a concurrent thread, but the async completion handler operates on the *stale* state.

### The "Mad Scientist" Angle
Async interfaces like `io_uring` are not just features; they are **Complexity Engines**. By submitting thousands of mixed-type requests in a single ring, an attacker can induce "pressure" on the kernel's state machine, increasing the probability of a desync from 1 in a million to 1 in a thousand.

**Exploit Vector:**
1. Submit a complex chain of asynchronous operations (e.g., Read -> Write -> Close).
2. Trigger a state change in a separate thread precisely between the request submission and the handler execution.
3. The handler executes a write to a closed or re-allocated object.
4. Result: Kernel-mode Write-What-Where.

## ⚡ Primitive: [The Generic-Interface-Overload]
**Observed in**: Cross-platform driver frameworks.

### Synthesis
OS vendors are pushing "Generic" interfaces to simplify driver development. The primitive is the **Overload**: using a generic interface to reach a specific, legacy, and un-audited function.

---
*The map is not the territory, but the ruins are consistent.*
