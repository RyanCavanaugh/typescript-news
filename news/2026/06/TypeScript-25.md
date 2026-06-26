# Report for 2026-06-25 (Thursday, June 25th, 2026)

8 different users commented on 11 different issues.

## Recommended Actions

 * Response Recommended
    * @ajvincent provided a relevant npm package link in [microsoft/TypeScript#4881](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4803563120)
    * @ajvincent provided a relevant npm package link in [microsoft/TypeScript#4881](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4803563120)
    * @Osamaali313 provided reproduction details and offered to adjust the fix or tests in [microsoft/TypeScript#63587](https://github.com/microsoft/TypeScript/pull/63587#issuecomment-4804094918)

## Activity Summary

### [Issue microsoft/TypeScript#4881](https://github.com/microsoft/TypeScript/issues/4881) (Open, `Suggestion`, `Needs Proposal`)

**Request: Class Decorator Mutation**

*Enable TypeScript to correctly type-check class decorators that add properties for mixins.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4085396431) **lolmaus** argued that the decorator design was settled at Stage 3 and criticized TypeScript’s refusal to implement decorator mutations as frustrating and ridiculous
 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4085488077) **HolgerJeromin** noted that not implementing decorator mutations isn't a refusal and that resource constraints and TS7 stabilization timeline make addressing it now ineffective
 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4085488077) **HolgerJeromin** noted that not implementing decorator mutations isn't a refusal and that resource constraints and TS7 stabilization timeline make addressing it now ineffective
 * [today](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4803563120) **ajvincent** provided a link to an npm package for mixin type definitions
 * [today](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4803563120) **ajvincent** provided a link to an npm package for mixin type definitions

### [Issue microsoft/TypeScript#63566](https://github.com/microsoft/TypeScript/issues/63566) (Closed, `Working as Intended`)

**TypeScript doesn't consider contravariance in member functions even with strictFunctionTypes**

*TypeScript ignores contravariance in function-typed object members, allowing unsafe assignments even with strictFunctionTypes.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63566#issuecomment-4772274987) **nmain** described a case of unsoundness on property writes when subtyping is involved and provided example code
 * **RyanCavanaugh** added label `Working as Intended`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63566#issuecomment-4780976150) **RyanCavanaugh** explained that the problem was due to writes on properties rather than generic variance and pointed to issue #18770
 * [today](https://github.com/microsoft/TypeScript/issues/63566#issuecomment-4805709709) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#63580](https://github.com/microsoft/TypeScript/issues/63580) (Closed, `Bug`, `Domain: Parser`)

**Parser hangs on comment ending with \`\-\*/\`**

*TypeScript's createSourceFile function hangs indefinitely when parsing a comment that begins with /** and ends with -*/.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63580#issuecomment-4790844410) **RyanCavanaugh** said "Doesn't repro in tsgo but a total LS hang is quite bad; we might want to take this for a 6.0 patch"
 * (yesterday) **RyanCavanaugh** added labels `Bug`, `Domain: Parser`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63581](https://github.com/microsoft/TypeScript/pull/63581) (Closed, `For Uncommitted Bug`)

**Fix infinite loop**

*Correct loop termination logic to fix an infinite loop in the application.*

 * created by **core-dumpling**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63581#issuecomment-4800446635) **core-dumpling** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63581#issuecomment-4803525889) **RyanCavanaugh** merged the changes into main and noted that no standalone patch release would be issued for this fix
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63585](https://github.com/microsoft/TypeScript/issues/63585) (Open, `Duplicate`)

**Spread operator with computed property is not being checked**

*TypeScript does not enforce type safety when overriding record entries with computed properties in object spreads, allowing invalid values.*

 * created by **val-o**
 * [today](https://github.com/microsoft/TypeScript/issues/63585#issuecomment-4804068160) **RyanCavanaugh** noted duplicate issues and explained the challenge of representing computed property names for union keys in the type system
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#63586](https://github.com/microsoft/TypeScript/issues/63586) (Open)

**invalid export syntax when emitting declaration for JS file using \`as module\.exports\` \(does not happen with TS file\)**

*Generating declarations for a JS file that exports an alias named module.exports produces invalid unquoted syntax in the .d.ts, whereas TS files generate correct output.*

 * created by **G-Rath**

### [PR microsoft/TypeScript#63587](https://github.com/microsoft/TypeScript/pull/63587) (Closed, `For Uncommitted Bug`)

**Fix normalizePath rooting a relative path that begins with \./ followed by a slash**

*Adjust fast-path logic in normalizePath and getNormalizedAbsolutePath to prevent stripping './' before separators and incorrectly converting relative paths to absolute.*

 * created by **Osamaali313**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63587#issuecomment-4803897990) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63587#issuecomment-4803898001) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63587#issuecomment-4804006880) **RyanCavanaugh** said "@Osamaali313 what coding agent are you using?"
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63587#issuecomment-4804094918) **Osamaali313** described using Claude Code to verify changes and noted opening issue #63588 about the bug, offering to adjust the fix or tests
 * [today](https://github.com/microsoft/TypeScript/pull/63587#issuecomment-4804210325) **RyanCavanaugh** said "@Osamaali313 Any idea why Claude Code didn't read https://github.com/microsoft/TypeScript/blob/main/AGENTS.md#-do-not-create-coding-prs-for-this-repository ?"
 * [today](https://github.com/microsoft/TypeScript/pull/63587#issuecomment-4804261604) **Osamaali313** acknowledged not reading AGENTS.md before opening the PR, apologized, stated they would direct future fixes to typescript-go, and closed the linked issue

### [Issue microsoft/TypeScript#63588](https://github.com/microsoft/TypeScript/issues/63588) (Closed)

**normalizePath roots a relative path beginning with \`\./\` followed by a slash**

*normalizePath and getNormalizedAbsolutePath erroneously convert relative paths starting with './' and redundant separators into absolute paths instead of preserving relativity.*

 * created by **Osamaali313**
 * [today](https://github.com/microsoft/TypeScript/issues/63588#issuecomment-4804261819) **Osamaali313** said "Closing — microsoft/TypeScript is in maintenance mode per AGENTS.md and this is a general bug fix, not an accepted category. Recording it here only for reference; no action needed from maintainers."
 * (today) **Osamaali313** closed the issue

### [PR microsoft/TypeScript#63589](https://github.com/microsoft/TypeScript/pull/63589) (Open, `For Uncommitted Bug`)

**lib: add Math\.sumPrecise type definition \(ES2025\)**

*Add Math.sumPrecise type declarations to the TypeScript esnext.math library for upcoming ES2026 support.*

 * created by **kamalkarki111**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63589#issuecomment-4809926294) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63589#issuecomment-4809926301) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63589#issuecomment-4809928048) **microsoft-github-policy-service[bot]** requested the contributor to read the CLA and reply with an agree statement including optional company info
 * [later](https://github.com/microsoft/TypeScript/pull/63589#issuecomment-4809928061) **microsoft-github-policy-service[bot]** requested the contributor to read the CLA and reply with an agree statement including optional company info

### [PR microsoft/TypeScript#63590](https://github.com/microsoft/TypeScript/pull/63590) (Open, `For Uncommitted Bug`)

**lib: add Math\.sumPrecise type definition \(ES2025\)**

*Add TypeScript definitions for the new ES2026 Math.sumPrecise method in the esnext.math library.*

 * created by **kamalkarki111**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63590#issuecomment-4809947237) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63590#issuecomment-4809947257) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63590#issuecomment-4809949119) **microsoft-github-policy-service[bot]** requested the contributor to read the CLA and reply with an agree statement including optional company info

