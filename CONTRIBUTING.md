# Contributing to oculink-gpu-bypass

Thanks for improving the GPU bypass notes and scripts. This repository covers
hardware enumeration workarounds for POWER and PowerPC systems, so contributions
should be careful, reproducible, and explicit about hardware risk.

## Useful Contributions

- Improve setup steps for internal PCIe rescans or OCuLink adapters.
- Add tested notes for POWER8, POWER9, or PowerPC Mac systems.
- Document GPU, adapter, cable, and kernel combinations that work or fail.
- Improve scripts with clearer checks, dry-run behavior, or diagnostics.
- Clarify kernel patch application and rollback steps.

## Development Workflow

1. Fork the repository and create a focused branch.
2. Keep script, patch, and documentation changes separated where possible.
3. Include host model, firmware, kernel, GPU, adapter, and cable details.
4. Treat hot-plug and kernel patch instructions as safety-sensitive.

## Validation

- Documentation-only changes: run `git diff --check`.
- Shell changes: run `bash -n` on modified scripts where Bash is available.
- Hardware workflow changes: include `lspci` output before and after the rescan,
  plus the kernel version and driver state.

## Pull Request Checklist

- The affected workflow is named: internal PCIe or OCuLink external.
- Validation commands and hardware details are included.
- Risky steps are clearly called out.
- Rollback or recovery notes are included when kernel patches change.
- Generated logs and local machine paths are not committed.

## Reporting Issues

Include system model, firmware, Linux distribution, kernel version, GPU model,
adapter/cable details, commands run, and relevant `dmesg` or `lspci` output.
Remove serial numbers or secrets before posting logs.
