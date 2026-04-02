# Report for 2026-01-31 (Saturday, January 31st, 2026)

7 different users commented on 10 different issues.

## Recommended Actions

 * Response Recommended
    * @sigmaSd provided necessary environment variable setting information in [microsoft/TypeScript-go#2612](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3829043043)
    * @amyssnippet reported that running the commands did not reproduce the error in [microsoft/TypeScript-go#2612](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3830412825)
    * @sigmaSd provided a suggestion to clear cache and rerun deno check in [microsoft/TypeScript-go#2612](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3830419234)
    * @amyssnippet asked if they should start working on this issue in [microsoft/TypeScript-go#2612](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3830432114)

## Activity Summary

### [Issue microsoft/TypeScript-go#2501](https://github.com/microsoft/TypeScript-go/issues/2501) (Open, `Crash`)

**textDocument/completion: runtime error: slice bounds out of range \[:2615\] with length 2590**

*The TypeScript-Go language server panics with a slice bounds out of range error during textDocument/completion requests.*

 * created by **sanny-io**
 * **sanny-io** added label `Crash`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2501#issuecomment-3747026777) **rubenferreira97** reported experiencing the error but was unable to reproduce it
 * [today](https://github.com/microsoft/TypeScript-go/issues/2501#issuecomment-3829141424) **frodi-karlsson** suggested adding bounds checking to LineAndCharacterToPosition to prevent panics when positions exceed text length
 * [today](https://github.com/microsoft/TypeScript-go/issues/2501#issuecomment-3829229887) **jakebailey** expressed concern that having them elsewhere could introduce mismatches and break things, and that this shouldn't be inevitable

### [Issue microsoft/TypeScript-go#2599](https://github.com/microsoft/TypeScript-go/issues/2599) (Closed, `bug`, **ahejlsberg**, **Copilot**)

**JSDoc for overloads and implementation is not displayed**

*VS Code TS Native Preview fails to show JSDoc for non-top overloads and implementation of overloaded TypeScript functions.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2599#issuecomment-3811719304) **ahejlsberg** explained that the changes to overload count display were intentional and compared how Strada and Corsa show overload information
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2599#issuecomment-3815144737) **tats-u** said "I see, but the disappearance of JSDoc matters much more. Can Corsa inherit the JSDoc for the top overload declaration like Strada (include 6)?"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2599#issuecomment-3818238847) **ahejlsberg** agreed that Corsa should inherit the JSDoc for the top overload declaration like Strada
 * (today) **ahejlsberg** added label `bug`, assigned to **ahejlsberg**, and unassigned **DanielRosenwasser**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2612](https://github.com/microsoft/TypeScript-go/issues/2612) (Open, `Crash`)

**tsgo crashes**

*tsgo crashes with a stack trace when running deno check on ignore_test.ts with DENO_UNSTABLE_TSGO enabled in Deno 2.6.6.*

 * created by **sigmaSd**
 * **sigmaSd** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3828657207) **amyssnippet** reported that they didn’t get any errors and shared clone commands and deno version output
 * [today](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3829043043) **sigmaSd** said "You also need to set DENO_UNSTABLE_TSGO=1"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3830412825) **amyssnippet** ran the provided commands and reported that they still did not encounter the error
 * [today](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3830419234) **sigmaSd** diagnosed caching prevented deno check from running and suggested editing the file or running "deno clean"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3830432114) **amyssnippet** asked if they should start working on the reported fatal error after a concurrent map read and write panic

### [PR microsoft/TypeScript-go#2627](https://github.com/microsoft/TypeScript-go/pull/2627) (Closed)

**Multiple improvements to Quick Info**

*Enhance Quick Info to reuse first-overload JSDoc, correctly display symbol meanings, fix translation bug, and improve 'this' hover info.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2627#issuecomment-3830445876) **jakebailey** said "Failure is a test flake I believe #2628 fixes"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2628](https://github.com/microsoft/TypeScript-go/pull/2628) (Closed)

**Fix dedupe/redirect nondeterminism**

*Ensure deterministic deduplication and redirection ordering by updating comparison logic and removing misleading stable sorts.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2629](https://github.com/microsoft/TypeScript-go/pull/2629) (Open)

**Experiment: Distribute Control Flow**

*TypeScript fails to distribute union types when mapping over a discriminated union array and returning the same object*

 * created by **devanshj**

### [Issue microsoft/TypeScript-go#961](https://github.com/microsoft/TypeScript-go/issues/961) (Open, `bug`, `Domain: Emit`, `Domain: Type Checking`, **jakebailey**)

**tsgo fails to resolve namespace symbols in non\-extends contexts across files**

*tsgo fails to qualify namespace symbols A and Afunc outside extends contexts across files, causing incorrect JS and runtime errors.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3824394383) **dtscd** provided a code example demonstrating that a simple patch resolves nested namespace access within the same file
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3828459486) **magic-akari** thanked @dtscd for the patch, confirmed it worked for same-file scenarios, and asked whether cross-namespace value qualification should be supported, noting architectural consistency and ecosystem precedent
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3828685368) **dtscd** argued that removing cross-namespace resolution trivialized namespaces, highlighted ES modules' per-file scoping and minimal linking performance impact, and lamented added user complexity compared to Go
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3828862365) **dtscd** shared a proof-of-concept change adding outfile support with sourceMaps and a commit link, asserted it worked for their project and challenged the performance argument

