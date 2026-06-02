# Report for 2026-05-31 (Sunday, May 31st, 2026)

11 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @matyasf provided repro steps as requested in [microsoft/TypeScript-go#3617](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4592514890)
    * @kuishou68 asked for another review of the changes in [microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4590877856)

## Activity Summary

### [Issue microsoft/TypeScript-go#3617](https://github.com/microsoft/TypeScript-go/issues/3617) (Open, `Needs Investigation`, **iisaduan**)

**fix: FindBestPatternMatch incorrectly allows wildcard pattern to override exact match**

*FindBestPatternMatch misuses StarIndex so exact matches set longestMatchPrefixLength to -1, allowing later wildcard patterns to override exact matches.*

 * (3 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4401880065) **RyanCavanaugh** said "@kuishou68 how does this manifest? There's no external-visible behavorial description nor testcase in that PR, so it's hard to know the severity/priority of this"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4592514890) **matyasf** described reproduction steps demonstrating incorrect import paths when building with tsgo in a composite TypeScript project

### [PR microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618) (Open)

**fix: prevent wildcard pattern from overriding exact match in FindBestPatternMatch**

*Assign math.MaxInt for exact matches in FindBestPatternMatch to ensure wildcard patterns cannot override exact matches.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4527660962) **kuishou68** added a new test file internal/core/pattern_test.go covering exact versus wildcard orderings, longer versus shorter prefix wildcard precedence, no-match behavior, and single/multiple wildcard match scenarios with self-documenting assertions
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4527804370) **kuishou68** said "I have added the test cases as requested. Could you please take another look?"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [later](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4590877856) **kuishou68** explained why they traced tsconfig paths resolution, identified and fixed the StarIndex logic in FindBestPatternMatch, and added the requested test cases while requesting another review

### [PR microsoft/TypeScript-go#4113](https://github.com/microsoft/TypeScript-go/pull/4113) (Open)

**Add missing APIs required for WebStorm integration\.**

*Add missing TS-GO service APIs required for WebStorm inspections, find usages, and refactorings to avoid forking.*

 * created by **piotrtomiak**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4113#issuecomment-4590353737) **piotrtomiak** said "@microsoft-github-policy-service agree company="JetBrains""

### [Issue microsoft/TypeScript-go#4122](https://github.com/microsoft/TypeScript-go/issues/4122) (Open)

**Different emit for import\.defer\(\) in a CommonJS module**

*tsgo emits a Promise.resolve().then wrapper for import.defer in CommonJS modules instead of preserving import.defer calls like TypeScript 6.0*

 * created by **mds-ant**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4122#issuecomment-4594203100) **a-tarasyuk** recalled that import.defer cannot be used with --module commonjs and asked if the lowering should be fixed and what the intended use case is

### [Issue microsoft/TypeScript-go#4135](https://github.com/microsoft/TypeScript-go/issues/4135) (Closed)

**Nameless \`@param {T}\` tag is a parse error in tsc but silently types the positional parameter in tsgo**

*tsgo silently applies a nameless JSDoc @param tag to the first parameter instead of producing tsc’s parse errors*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4135#issuecomment-4587572383) **a-tarasyuk** said "This behavior is expected and follows the decisions made in #2632 and #2647."
 * [later](https://github.com/microsoft/TypeScript-go/issues/4135#issuecomment-4591466372) **mds-ant** said "Sounds good, will close this issue given that the discrepancy in behavior is intentional (and arguably better in tsgo)."
 * (later) **mds-ant** closed the issue

### [Issue microsoft/TypeScript-go#4136](https://github.com/microsoft/TypeScript-go/issues/4136) (Closed)

**tsgo does not produce TS6053 for a missing root file**

*tsgo does not emit TS6053 file not found error for a missing root file*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4136#issuecomment-4589547405) **JoostK** said "https://github.com/microsoft/typescript-go/issues/3753"

### [PR microsoft/TypeScript-go#4144](https://github.com/microsoft/TypeScript-go/pull/4144) (Open)

**fix\(checker\): align template literal inference with tsc UTF\-16 surrog…**

*Template literal inference now splits supplementary Unicode characters into UTF-16 surrogate pairs to match TypeScript’s behavior.*

 * created by **Utsav006**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4144#issuecomment-4589427919) **Utsav006** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript-go#4145](https://github.com/microsoft/TypeScript-go/issues/4145) (Open)

**strict\-family checks \(strictPropertyInitialization, useUnknownInCatchVariables\) incorrectly enabled when only strictNullChecks is set — regression in dev\.20260206\.1**

*tsgo dev.20260206.1 erroneously enables strictPropertyInitialization and useUnknownInCatchVariables when only strictNullChecks is set, resulting in false errors.*

 * created by **JerryPeace**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4145#issuecomment-4589740264) **jakebailey** advised checking against TS 6.0 instead of 5.9 and linked the announcement

### [Issue microsoft/TypeScript-go#4146](https://github.com/microsoft/TypeScript-go/issues/4146) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**\`FreshableType\` interface is missing in the API**

*Add a FreshableType interface and the complementary getFreshType and getRegularType methods to the API alongside the TypeFlags.Freshable flag.*

 * created by **mrazauskas**

### [Issue microsoft/TypeScript-go#4147](https://github.com/microsoft/TypeScript-go/issues/4147) (Open)

**tsgo \-b emits src/ subpath in declaration files where tsc \-b emits types/**

*tsgo -b emits declaration files referencing ./src/* subpaths instead of ./types/* like tsc, causing downstream type errors.*

 * created by **matyasf**

### [Issue microsoft/TypeScript-go#4148](https://github.com/microsoft/TypeScript-go/issues/4148) (Closed)

**hc\<\> RPC client instantiates ~12× more types under tsgo than tsc \(server app type at parity\)**

*tsgo generates about 12× more type instantiations than tsc when instantiating Hono’s hc<> RPC client over a chained .openapi app*

 * created by **daviduzumeri**

