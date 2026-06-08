# Report for 2026-06-07 (Sunday, June 7th, 2026)

4 different users commented on 10 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#1685](https://github.com/microsoft/TypeScript-go/issues/1685) (Open, `Domain: Type Checking`, `Domain: JS`, **sandersn**)

**\`ts\-check\` used with \`@typedef\` causes an error on \`module\.exports = \.\.\.\`**

*Combining @ts-check and @typedef in a CommonJS file causes a TS2309 export assignment error with tsgo.*

 * (1 month ago) **RyanCavanaugh** reopened the issue
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4636409370) **ahejlsberg** explained the errors in the example were a known TS7 restriction and referenced CHANGES.md describing the Corsa module.exports assignment rule
 * [later](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4650033848) **jbeaudoin-lf** said "@ahejlsberg I guess we gonna have to find an alternative and migrate away from this pattern... Thanks anyways"

### [Issue microsoft/TypeScript-go#4208](https://github.com/microsoft/TypeScript-go/issues/4208) (Open, `Needs Investigation`)

**\`isSourceFile\(\)\` is missing in the API**

*The project lacks an isSourceFile() type guard in the API despite having a SourceFile interface.*

 * created by **mrazauskas**
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Post-7.0`
 * (later) **mrazauskas** closed the issue
 * (later) **mrazauskas** reopened the issue

### [PR microsoft/TypeScript-go#4210](https://github.com/microsoft/TypeScript-go/pull/4210) (Closed)

**Add \`isSourceFile\(\)\` type guard**

*Introduce an isSourceFile() type guard function, ported from the TypeScript compiler, to enhance AST node checking.*

 * created by **mrazauskas**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [later](https://github.com/microsoft/TypeScript-go/pull/4210#issuecomment-4647088843) **mrazauskas** closed the issue after it was marked as Needs Investigation and noted the change might not be as simple as initially assumed
 * (later) **mrazauskas** closed the issue

### [Issue microsoft/TypeScript-go#4221](https://github.com/microsoft/TypeScript-go/issues/4221) (Closed, `bug`, **ahejlsberg**)

**tsgo reports TS2345 instead of TS2379 for exactOptionalPropertyTypes argument mismatches**

*tsgo reports TS2345 errors without exactOptionalPropertyTypes hints instead of TS2379 for property type mismatches*

 * (yesterday) **ahejlsberg** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4228](https://github.com/microsoft/TypeScript-go/pull/4228) (Closed)

**fix exact optional argument diagnostic**

*Refines the TypeScript diagnostic for non-assignable arguments when exactOptionalPropertyTypes is enabled to recommend adding undefined to target properties.*

 * created by **a-tarasyuk**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4237](https://github.com/microsoft/TypeScript-go/issues/4237) (Open)

**Consider shipping API enums without the \`const\` modifier**

*Ship API enums without the const modifier to prevent compile-time inlining and align with Strada*

 * created by **mrazauskas**

### [PR microsoft/TypeScript-go#4238](https://github.com/microsoft/TypeScript-go/pull/4238) (Open)

**Several performance optimizations for the scanner's hot path**

*Implements five hot-path scanner optimizations for ASCII parsing and comment/trivia scanning, yielding roughly 7.8% faster parse times.*

 * created by **mds-ant**

### [PR microsoft/TypeScript-go#4239](https://github.com/microsoft/TypeScript-go/pull/4239) (Open)

**Replace ForEachReturnStatement closure with direct kind\-switched walk**

*Replace ForEachReturnStatement closure with a direct kind-switched recursive function to reduce allocations and improve performance.*

 * created by **mds-ant**

### [PR microsoft/TypeScript-go#4240](https://github.com/microsoft/TypeScript-go/pull/4240) (Open)

**Inline \`GetCombinedNodeFlags\` and \`GetCombinedModifierFlags\` bodies**

*Inline flag computations by replacing generic helper with direct node field reads, boosting performance by about 27%.*

 * created by **mds-ant**

### [PR microsoft/TypeScript-go#4241](https://github.com/microsoft/TypeScript-go/pull/4241) (Open, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 3 updates**

*Update three GitHub Actions in the root directory: bump actions/checkout to v6.0.3, codecov/codecov-action, and github/codeql-action.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

