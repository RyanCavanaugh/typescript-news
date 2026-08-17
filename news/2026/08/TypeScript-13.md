# Report for 2026-08-13 (Thursday, August 13th, 2026)

8 different users commented on 10 different issues.

## Recommended Actions

 * Response Recommended
    * @danyreyna asked if the fix would be available in v7.1 in [microsoft/TypeScript#63646](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-5287274144)
    * @nmain provided reproduction information for version 6.0 in [microsoft/TypeScript#63749](https://github.com/microsoft/TypeScript/issues/63749#issuecomment-5292998642)

## Activity Summary

### [Issue microsoft/TypeScript#62707](https://github.com/microsoft/TypeScript/issues/62707) (Closed, `Bug`, `Help Wanted`, `Domain: Parser`)

**TS1508: Unexpected '?'\. Did you mean to escape it with backslash? shouldn't report even with \`v\` flag**

*TypeScript wrongly reports TS1508 for unescaped '?' in regex character classes when using the v flag.*

 * [40 weeks ago](https://github.com/microsoft/TypeScript/issues/62707#issuecomment-3484170740) **graphemecluster** noted that three lines were unnecessary and provided a diff to remove them
 * **RyanCavanaugh** added label `Domain: Parser`
 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/62707#issuecomment-4629401261) **Ijtihed** said "I fixed lone & handling in /v character classes and added a  compiler regression test for it asw. "
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#63646](https://github.com/microsoft/TypeScript/issues/63646) (Closed, `Needs Investigation`, **johnfav03**)

**tsc \-\-watch does not work in docker**

*tsc --watch fails to detect file changes in Docker bind-mounted workspaces on macOS after upgrading to version 7.0.2.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-5137934722) **danyreyna** reported a similar issue when building with Docker using node:22.22.3-slim, where subsequent tsc --watch builds stalled due to a fanotify_mark operation not supported error
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-5145530428) **johnfav03** thanked maintainers and explained that Docker's filesystem returns EOPNOTSUPP and that the watch will fall back from fanotify to inotify once the PR is merged
 * (3 days ago) **johnfav03** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-5287274144) **danyreyna** said "Thank you for the prompt fix @johnfav03, but will it be available until v7.1?"
 * [today](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-5287292595) **jakebailey** said "We have yet to discuss 7.0 patches (focusing on moving the code back to this repo and then reenabling releasing) but I would suspect this would be on the table"

### [PR microsoft/TypeScript#63745](https://github.com/microsoft/TypeScript/pull/63745) (Closed, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump js\-yaml from 4\.1\.1 to 4\.3\.1**

*Bump js-yaml to 4.3.1 for security fix removing quadratic complexity in omap duplicate detection*

 * (3 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (later) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/pull/63745#issuecomment-5295085353) **dependabot[bot]** explained how to ignore dependency update notifications or reopen the PR to resolve conflicts

### [Issue microsoft/TypeScript#63746](https://github.com/microsoft/TypeScript/issues/63746) (Closed, `Duplicate`)

**\[7\.0\] Downlevel emit places a comment after a synthesized return, causing arrow functions to return undefined**

*TypeScript 7.0's downlevel emit places comments after synthesized returns in arrow functions with optional chaining, causing ASI to return undefined.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63746#issuecomment-5248716689) **SnowingFox** reproduced the issue on the TS 7.0 native compiler and confirmed it as a native-port regression, provided reproduction steps, compared native and JS emitter outputs, and identified the root cause in typescript-go
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63746#issuecomment-5249376232) **MartinJohns** said "Duplicate of https://github.com/Microsoft/typescript-go/issues/4722."
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63746#issuecomment-5288391046) **typescript-automation[bot]** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#63749](https://github.com/microsoft/TypeScript/issues/63749) (Open, `Bug`)

**\[7\.0\] Can't access field if it is protected in one constituent of an intersection \(type order dependent\)**

*TypeScript 7 erroneously prevents accessing a property protected in one part of an intersection type when constituent order differs.*

 * created by **dragomirtitian**
 * [later](https://github.com/microsoft/TypeScript/issues/63749#issuecomment-5292998642) **nmain** said "This repros in 6.0 if stableTypeOrdering is used."

### [Issue microsoft/TypeScript#63750](https://github.com/microsoft/TypeScript/issues/63750) (Open, `Bug`, `Fix Available`)

**tsgo: parser nil\-pointer panic when a JSDoc @overload tags an anonymous default\-export function**

*tsgo’s parser crashes with a nil-pointer panic when a JSDoc @overload tags an anonymous default-export function*

 * created by **johnsoncodehk**

### [PR microsoft/TypeScript#63751](https://github.com/microsoft/TypeScript/pull/63751) (Closed, `For Backlog Bug`)

**fix: remove false tslib requirement for native \#private fields at ES2022\+**

*Removes unnecessary tslib dependency for native #private fields in ES2022+ in favor of the Go-based fix.*

 * created by **ErfanBagheri404**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63751#issuecomment-5295063528) **ErfanBagheri404** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/63751#issuecomment-5295079421) **RyanCavanaugh** informed that the TypeScript repo was closed for development and directed the PR to the typescript-go repo referencing CONTRIBUTING.md and issue #62963
 * (later) **RyanCavanaugh** closed the issue

