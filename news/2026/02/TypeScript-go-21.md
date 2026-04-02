# Report for 2026-02-21 (Saturday, February 21st, 2026)

3 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @jogibear9988 asked for approval to implement the proposed performance fix in [microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3940694707)

## Activity Summary

### [Issue microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo takes forever to compile, 325seconds vs typescript 42seconds**

*tsgo watch compilation takes 325s versus TypeScript’s 42s, and the reporter requests help diagnosing and resolving the slowdown.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3805742727) **ffmiruz** mentioned wanting confirmation of the approach, noted that iterating over bytes was necessary, suggested checking for ASCII-ness for optimization with a rune fallback, and provided benchmark results
 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3940694707) **jogibear9988** identified a performance bottleneck in GetECMALineAndCharacterOfPosition due to O(n²) rune counting and proposed caching rune-to-byte offsets for O(1) character queries

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3931729619) **shinichy** reported that tsgo got stuck, did not produce a `custom/saveHeapProfile` response in LSP logs, and missed cache statistics information when following reproduction steps
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3931736730) **shinichy** said "@neo773 Are you able to reproduce this issue in https://github.com/twentyhq/twenty/? I couldn't reproduce this issue in the repo."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3936503506) **andrewbranch** said "@shinichy could you try out #2855 and see if that improves things for you?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3940248161) **shinichy** reported that the memory leak slowed but persisted, that the tsgo LSP process still hung and memory usage hit ~30GB, traced the hang to extractFromFile(entrypoint), and shared an AI-generated explanation of unbounded work per entrypoint and lack of cancellation

### [PR microsoft/TypeScript-go#2864](https://github.com/microsoft/TypeScript-go/pull/2864) (Closed)

**Enable \`noUncheckedSideEffectImports\` by default**

*Port PR 62443 to enable the noUncheckedSideEffectImports compiler option by default.*

 * created by **Andarist**
 * (yesterday) **jakebailey** closed the issue
 * (yesterday) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2866](https://github.com/microsoft/TypeScript-go/pull/2866) (Closed)

**Fix package\.json file watching**

*Update file watcher to respond to any change in existing package.json files rather than only file creation*

 * created by **andrewbranch**
 * (yesterday) **jakebailey** closed the issue
 * (yesterday) **jakebailey** reopened the issue
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2870](https://github.com/microsoft/TypeScript-go/pull/2870) (Closed)

**2x speedup of binary AST encoding**

*Directly appending uint32 instead of using a runtime type switch doubles binary AST encoding performance.*

 * created by **auvred**

