# Report for 2026-08-01 (Saturday, August 1st, 2026)

3 different users commented on 2 different issues.

## Activity Summary

### [PR microsoft/TypeScript-go#4515](https://github.com/microsoft/TypeScript-go/pull/4515) (Open)

**Test and fix nonlocal callable variance cycles**

*Add tests and fixes for nonlocal callable variance cycles caused by specific checker associations and ordering*

 * created by **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4515#issuecomment-5157034423) **ahejlsberg** said "What exactly happened with xstate and variance that this PR fixes? And is there a way to reproduce to help reasoning about it?"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4515#issuecomment-5158608693) **jakebailey** said "This nasty test was the best I could get, the other option being to take #4313 and undo the checker changes and then build xstate"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4515#issuecomment-5158611148) **jakebailey** said "I'll try to get something more minimal when I have a chance"

### [Issue microsoft/TypeScript-go#4817](https://github.com/microsoft/TypeScript-go/issues/4817) (Closed)

**Generic inference resolves the type argument from a wrapper union member instead of the direct/overriding member \(tsc clean\)**

*tsgo’s generic inference picks a wrapped function union member over the intersected overriding function member, causing D to resolve incorrectly compared to tsc.*

 * created by **johnsoncodehk**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4817#issuecomment-5156271341) **jakebailey** said "Make sure you check 6.0 with --stableTypeOrdering as I believe this should fail there too"
 * [later](https://github.com/microsoft/TypeScript-go/issues/4817#issuecomment-5156612537) **johnsoncodehk** confirmed that stock 6.0.3 with --stableTypeOrdering failed both the minimal repro and the original TanStack vue-query case, noted tsgo matches the stable-ordering behavior, and closed the issue
 * (later) **johnsoncodehk** closed the issue

