# Known Security Advisories

## RUSTSEC-2026-0580 - Heapless Treiber Stack Race Condition

**Package**: heapless (transitive dependency)

**Severity**: Unsound

**Description**: The treiber stack implementation in heapless had a race condition that could allow two threads running concurrently to race, causing one to read from a pointer that had been invalidated by another execution context.

**Status**: This is a transitive dependency of soroban-sdk@26.0.0. Monitor for updates to soroban-sdk that upgrade or replace heapless.

**Mitigation**: 
- Upgrade soroban-sdk when a patched version becomes available
- Consider alternative concurrency patterns if heapless is a critical blocker

**Reference**: https://rustsec.org/advisories/RUSTSEC-2026-0580
