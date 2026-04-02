# Report for 2026-01-25 (Sunday, January 25th, 2026)

7 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @jogibear9988 reported generated TypeScript files lack linebreaks and one file exceeds 1MB in [microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3797205714)
    * @tikki100 asked if a linked issue was related in [microsoft/TypeScript-go#2555](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3798728940)
    * @ericnorris suggested investigating allowing an empty version field to fix auto-import leaks in [microsoft/TypeScript-go#2584](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3797320611)

## Activity Summary

### [Issue microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402) (Open, `Crash`)

**tsgo takes forever to compile, 325seconds vs typescript 42seconds**

*tsgo watch compilation takes 325s versus TypeScript’s 42s, and the reporter requests help diagnosing and resolving the slowdown.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3703426438) **jogibear9988** reported that the newest version still errored, observed that disabling sourcemaps reduced ts-go build time to 13s versus 32s for normal TypeScript, and noted a ~5s startup delay before the build message
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3771891076) **jogibear9988** said "Any ideas how we could proceed with this?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3794583430) **ffmiruz** pointed out that scanning from the start for each position causes O(n²) behavior on long lines, asked if the repository had long lines, and suggested using the TypeScript O(1) approach
 * [today](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3797205714) **jogibear9988** reported that generated TypeScript files lacked linebreaks and that one file exceeded 1MB
 * [today](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3797224077) **jakebailey** said "I'm sure we can come up with a better way to do this, this code hasn't been optimized. It was never an issue in the old compiler since strings were already UTF-16."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3798254127) **jogibear9988** noted that adding newlines to codegen reduced compilation to 24 seconds with ts-go and sourcemaps but left the issue unresolved in ts-go, suggested leaving the issue open, and mentioned the largest generated file was a js file

### [Issue microsoft/TypeScript-go#2555](https://github.com/microsoft/TypeScript-go/issues/2555) (Open, `Domain: Editor`)

**Installing Native Preview broke TS Imports**

*Installing VS Code’s Native Preview TypeScript extension on macOS breaks TypeScript auto-import suggestions despite reverting settings and reinstalling the editor.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3789626673) **rubnogueira** explained that with TypeScript 6.0 the tsconfig.json “types” array defaults to empty and requires explicitly listing relevant React types
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3790969410) **jakebailey** clarified that the change hasn't been made yet and that the issue is unrelated
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3794827972) **bastiankistner** described lacking import autocompletions, noted go-to-definition works, recalled it worked previously, and offered to post logs/traces
 * [later](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3798728940) **tikki100** said "Related?: https://github.com/microsoft/typescript-go/issues/2582"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3800314263) **ericnorris** stated that their issue was about the types field in package.json, not compilerOptions in tsconfig.json

### [Issue microsoft/TypeScript-go#2581](https://github.com/microsoft/TypeScript-go/issues/2581) (Open, `Domain: Editor`, **DanielRosenwasser**, **andrewbranch**, **Copilot**)

**Autocomplete incorrectly suggests transitive files from monorepo package**

*VS Code’s TypeScript autocomplete inaccurately includes internal files from a transitive monorepo package during auto-import suggestions.*

 * created by **ericnorris**
 * **ericnorris** added label `Domain: Editor`
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2582](https://github.com/microsoft/TypeScript-go/issues/2582) (Open, `Domain: Editor`)

**Auto\-import does not suggest updates from symlinked monorepo package sources**

*VS Code’s auto-import feature does not suggest updated symbols from symlinked packages in a monorepo workspace*

 * created by **ericnorris**
 * **ericnorris** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2583](https://github.com/microsoft/TypeScript-go/issues/2583) (Closed, `duplicate`, **ahejlsberg**)

**tsgo fails to report TS2769 for mutually\-exclusive object overloads**

*tsgo does not report TS2769 for mutually exclusive object overloads while tsc correctly flags the error.*

 * created by **r253hmdryou**

### [PR microsoft/TypeScript-go#2584](https://github.com/microsoft/TypeScript-go/pull/2584) (Open, **DanielRosenwasser**, **Copilot**)

**Fix autocomplete suggesting unexported internal files from monorepo packages**

*Update auto-import logic to exclude unexported internal files from monorepo packages that define exports.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3797320611) **ericnorris** noted that having a version field prevented auto-import from leaking transitive files and suggested investigating allowing an empty version field

### [PR microsoft/TypeScript-go#2585](https://github.com/microsoft/TypeScript-go/pull/2585) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 2 directories with 3 updates**

*Bump GitHub Actions dependencies across root and .github/actions/setup-go directories by updating actions/checkout, codeql-action, and actions/cache.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

