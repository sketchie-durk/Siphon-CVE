# 📖 The Grimoire: Windows Kernel Primitives

## ⚡ Primitive: IOCTL-Handler-Corruption
Many Windows CVEs stem from improper validation of input buffers in `DeviceIoControl` handlers.

### Synthesis
- **Root Cause**: Failure to validate `Irp->AssociatedIrp.SystemBuffer` length.
- **Siphon Data**: Historically appears in 3rd party drivers and legacy kernel components.
- **Actionable Pattern**: Search for `ProbeForRead`/`ProbeForWrite` omissions.

## ⚡ Primitive: Win32k.sys Logic Flaws
The windowing subsystem is a playground for privilege escalation.

### Synthesis
- **Root Cause**: Race conditions in object lifetime management (UAF).
- **Siphon Data**: Consistent recurrence in GDI and User32.
- **Actionable Pattern**: Analyze object reference counting in multi-threaded contexts.
