# Report for 2026-02-07 (Saturday, February 7th, 2026)

4 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @Cellule reported important information about tsgo’s incorrect output behavior causing silent data corruption in [microsoft/TypeScript-go#2708](https://github.com/microsoft/TypeScript-go/issues/2708#issuecomment-3864762029)
    * @juhort asked if the union order will always be deterministic given the same inputs in [microsoft/TypeScript-go#787](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3866952237)

## Activity Summary

### [PR microsoft/TypeScript-go#2680](https://github.com/microsoft/TypeScript-go/pull/2680) (Closed, **andrewbranch**, **Copilot**)

**Fix module resolver bug exposed by malformed package\.json import patterns**

*Fix module resolver bug that crashed the language server with malformed package.json wildcard import patterns*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3862596709) **andrewbranch** said "@copilot tests failed"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3862627198) **Copilot** fixed test failures by adding missing reference baselines
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3863080260) **Copilot** explained that all tests now passed after adding missing baselines
 * [today](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3864768635) **Copilot** described the changes in commit 85d2d5e1, preserved the first panic, inlined extraction logic in the second block, updated tests and baselines with directives, and renamed tests

### [PR microsoft/TypeScript-go#2707](https://github.com/microsoft/TypeScript-go/pull/2707) (Closed)

**Update NOTICE for go\-winio**

*Update go-winio NOTICE file to include dependencies and correct JSON and xxhash entries misidentified by the NOTICE tool*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2708](https://github.com/microsoft/TypeScript-go/issues/2708) (Open, **jakebailey**, **Copilot**)

**tsgo emits files next to source instead of outDir when include references parent directories via \.\./**

*tsgo emits files from parent-directory includes next to their sources instead of respecting the configured outDir.*

 * created by **Cellule**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2708#issuecomment-3863666446) **jakebailey** said "Can you please compare against the 6.0 nightly instead of 5.9?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2708#issuecomment-3863669710) **jakebailey** said "(I was assuming it was rootDir, but it probably isn't)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2708#issuecomment-3864762029) **Cellule** compared tsc 6.0 behavior with tsgo and reported that tsgo silently wrote .js files next to .ts sources, causing silent data corruption
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2708#issuecomment-3864827529) **Cellule** confirmed that setting the rootDir fixed the issue and supposed that the lack of error reporting on tsgo vs tsc v6 was the real problem

### [PR microsoft/TypeScript-go#2709](https://github.com/microsoft/TypeScript-go/pull/2709) (Open, **jakebailey**, **Copilot**)

**Implement TS5011 migration diagnostic for common source directory mismatch**

*Add TS5011 diagnostic to tsgo to alert when include patterns referencing parent directories cause output directory mismatches.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2710](https://github.com/microsoft/TypeScript-go/pull/2710) (Closed)

**Watch mode: clean up output files when source files are deleted**

*Add functionality to tsc --watch to automatically remove compiled output files when their source files are deleted.*

 * created by **DukeDeSouth**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2710#issuecomment-3866215462) **DukeDeSouth** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#2711](https://github.com/microsoft/TypeScript-go/pull/2711) (Closed)

**Optimize distributive conditional type instantiation for trivial extends types**

*Optimize distributive conditional type instantiation by directly applying branch results when the extends type is never, any, or unknown*

 * created by **DukeDeSouth**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2711#issuecomment-3866215482) **DukeDeSouth** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript-go#787](https://github.com/microsoft/TypeScript-go/issues/787) (Closed)

**\`UnionToTuple\` type returns "inverted" tuple in TSGO compared to TypeScript 5\.8\.3 and gives type error**

*TSGO's UnionToTuple type generates tuples in reverse order compared to TypeScript 5.8.3, causing type errors*

 * [43 weeks ago](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-2796307493) **alexwork1611** thanked maintainers and explained that they refactored their code to avoid using UnionToTuple, provided before/after screenshots and type definitions
 * (43 weeks ago) **alexwork1611** closed the issue
 * [40 weeks ago](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-2844237064) **LukeAbby** explained that uncommenting a declaration changes the tuple order produced by UnionToTuple, and that adding types elsewhere can lead to inconsistent ordering
 * [later](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3866952237) **juhort** asked whether the union order would always be the same given identical generic inputs, avoiding issues like the one mentioned by LukeAbby

