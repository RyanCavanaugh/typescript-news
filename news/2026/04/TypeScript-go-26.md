# Report for 2026-04-26 (Sunday, April 26th, 2026)

5 different users commented on 10 different issues.

## Activity Summary

### [PR microsoft/TypeScript-go#3603](https://github.com/microsoft/TypeScript-go/pull/3603) (Closed)

**Fix go to implementation crash on invalid CJS shorthand exports**

*Prevent go to implementation crashes on invalid CommonJS shorthand exports.*

 * created by **Andarist**
 * (later) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3604](https://github.com/microsoft/TypeScript-go/pull/3604) (Closed)

**Fix rename panic on unresolved reexports**

*Add handling to prevent rename operation panics caused by unresolved reexports*

 * created by **Andarist**
 * (later) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3607](https://github.com/microsoft/TypeScript-go/issues/3607) (Closed, `bug`, `Domain: Editor`, **ahejlsberg**)

**Missing hover for nullable method in type and interface**

*Hover tooltips for optional methods declared in type aliases and interfaces are not displayed in VS Code’s TypeScript extension.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3607#issuecomment-4320395685) **Withered-Flower-0422** identified missing '?' suffix for nullable property and method and missing hover output in tsgo
 * (later) **ahejlsberg** added label `bug`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#3615](https://github.com/microsoft/TypeScript-go/issues/3615) (Open, **andrewbranch**, **Copilot**)

**Server stops responding after \`Running scheduled diagnostics refresh\`**

*The TypeScript language server hangs after running scheduled diagnostics refresh in large monorepos with many open editors and file system event bursts.*

 * created by **ekazakov14**

### [PR microsoft/TypeScript-go#3616](https://github.com/microsoft/TypeScript-go/pull/3616) (Open)

**API \`emit\` support to generate \.d\.ts / \.js files from sources**

*Expose compiler emit in TSGO API and TypeScript client to generate .js and .d.ts files using virtual FS*

 * created by **pfumagalli**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4323425060) **pfumagalli** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript-go#3617](https://github.com/microsoft/TypeScript-go/issues/3617) (Open)

**fix: FindBestPatternMatch incorrectly allows wildcard pattern to override exact match**

*FindBestPatternMatch misuses StarIndex so exact matches set longestMatchPrefixLength to -1, allowing later wildcard patterns to override exact matches.*

 * created by **kuishou68**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4323559489) **kuishou68** filed PR #3618 with a fix that sets longestMatchPrefixLength to math.MaxInt on exact matches to prevent wildcard override, matching original TypeScript behavior

### [PR microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618) (Open)

**fix: prevent wildcard pattern from overriding exact match in FindBestPatternMatch**

*Assign math.MaxInt for exact matches in FindBestPatternMatch to ensure wildcard patterns cannot override exact matches.*

 * created by **kuishou68**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4323606759) **jakebailey** said "This will require a test, preferably one we can cross check with the old code to double check it"

### [PR microsoft/TypeScript-go#3619](https://github.com/microsoft/TypeScript-go/pull/3619) (Open)

**perf: Make \`NodeArray\` no longer inherit from \`Array\`**

*Detach NodeArray from Array prototype to prevent direct array method usage and achieve significant performance gains.*

 * created by **liuxingbaoyu**

