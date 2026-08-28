# Report for 2026-08-23 (Sunday, August 23rd, 2026)

16 different users commented on 33 different issues.

## Recommended Actions

 * Moderation
    * @asanaliopensource posted rude content in [microsoft/TypeScript#63748](https://github.com/microsoft/TypeScript/issues/63748#issuecomment-5395738128)
 * Response Recommended
    * @ivyhjk provided repro steps and linked the fix PR in [microsoft/TypeScript#63852](https://github.com/microsoft/TypeScript/issues/63852#issuecomment-5389611714)
    * @KiYugadgeter reported that the issue also affected vim-lsp in [microsoft/TypeScript#63928](https://github.com/microsoft/TypeScript/issues/63928#issuecomment-5391898251)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript#63932](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5388650536)
    * @vickvu asked if there are other unsupported features in TS 7.x and whether watch and watchOptions are still supported in [microsoft/TypeScript#63975](https://github.com/microsoft/TypeScript/issues/63975#issuecomment-5391942569)
    * @vickvu asked if the team still wants to address version differences and if there's documentation on unsupported features in [microsoft/TypeScript#63978](https://github.com/microsoft/TypeScript/pull/63978#issuecomment-5391720988)

## Activity Summary

### [Issue microsoft/TypeScript#63748](https://github.com/microsoft/TypeScript/issues/63748) (Closed)

**wtf**

*The user expresses surprise that the project’s code is written in TypeScript itself.*

 * created by **asanaliopensource**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63748#issuecomment-5268744988) **RyanCavanaugh** said "Well, not anymore 😛"
 * (1 week ago) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63748#issuecomment-5395738128) **asanaliopensource** said "WTF GO?"

### [Issue microsoft/TypeScript#63749](https://github.com/microsoft/TypeScript/issues/63749) (Closed, `Bug`, `Fix Available`, **ahejlsberg**)

**\[7\.0\] Can't access field if it is protected in one constituent of an intersection \(type order dependent\)**

*TypeScript 7 erroneously prevents accessing a property protected in one part of an intersection type when constituent order differs.*

 * **ahejlsberg** assigned to **ahejlsberg**
 * **typescript-automation[bot]** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`
 * (today) **ahejlsberg** added label `Fix Available`, set milestone to `TypeScript 7.1`, and removed from milestone `Backlog`

### [Issue microsoft/TypeScript#63852](https://github.com/microsoft/TypeScript/issues/63852) (Open, `Needs Investigation`, **andrewbranch**)

**Local auto\-imports disappear when a Yarn workspace dependency resolves a subpath back to the current project**

*TypeScript 7 in VS Code fails to suggest local auto-imports when a Yarn workspace dependency resolves a subpath back to the project.*

 * created by **sashamorozov**
 * **RyanCavanaugh** assigned to **andrewbranch**
 * **andrewbranch** added label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript/issues/63852#issuecomment-5389611714) **ivyhjk** described an independent reproduction using a pnpm workspace, highlighted that the symlink alone triggers the bug, and identified the already merged fix commit

### [Issue microsoft/TypeScript#63853](https://github.com/microsoft/TypeScript/issues/63853) (Closed, `Bug`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*Server errors were reported on the main TypeScript branch during an Azure pipeline run analyzing 300 popular GitHub repositories.*

 * (5 weeks ago) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1`, and assigned to **johnfav03**
 * (later) **johnfav03** closed the issue

### [PR microsoft/TypeScript#63904](https://github.com/microsoft/TypeScript/pull/63904) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**Add batched version for the several API**

*Add batched versions of the getDeclaredTypeOfSymbol, getAliasedSymbol, getImmediateAliasedSymbol, getExportsOfModule, and getMemberInModuleExports API methods.*

 * created by **dragomirtitian**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **typescript-automation[bot]** assigned to **andrewbranch**

### [Issue microsoft/TypeScript#63928](https://github.com/microsoft/TypeScript/issues/63928) (Open, `Needs Investigation`, **andrewbranch**)

**LSP server sends no per\-file diagnostics to clients without pull diagnostics support**

*Implement push-based per-file diagnostics for LSP clients without pull support by publishing diagnostics on open, change, and close.*

 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63928#issuecomment-5379757974) **el-pendeloco** mentioned that testing tsc’s LSP in the Helix editor didn’t produce diagnostics beyond tsconfig ones
 * [later](https://github.com/microsoft/TypeScript/issues/63928#issuecomment-5391898251) **KiYugadgeter** said "It also affect to vim-lsp too."

### [PR microsoft/TypeScript#63932](https://github.com/microsoft/TypeScript/pull/63932) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Fix \`getDeclarationModifierFlagsFromSymbolEx\` for synthetic properties**

*Fix accessibility checks so protected setters on synthetic properties in unions and intersections block writes.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5361493945) **typescript-automation[bot]** posted the requested performance run results
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5361502261) **typescript-automation[bot]** reported user test results comparing main and the pull request merge, noting two package install failures and one git clone failure, but otherwise indicating everything looked good
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5361935851) **typescript-automation[bot]** reported that TypeScript compilation tests on the top 400 repos passed successfully comparing main to the PR merge
 * [today](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5388525725) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5388526045) **typescript-automation[bot]** reported build statuses and result links for test top400, user test this, run dt, and perf test this faster jobs
 * [today](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5388626995) **typescript-automation[bot]** reported user test results comparing main and the pull request merge, noting two package install failures and one git clone failure, but otherwise indicating everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5388650536) **typescript-automation[bot]** posted the requested perf run results
 * [today](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5388679120) **typescript-automation[bot]** reported that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5388778630) **typescript-automation[bot]** reported that TypeScript compilation tests on the top 400 repos passed successfully comparing main to the PR merge
 * **ahejlsberg** added to milestone `TypeScript 7.1`

### [PR microsoft/TypeScript#63937](https://github.com/microsoft/TypeScript/pull/63937) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**, **andrewbranch**)

**Add arbitrary API request batching**

*Add a batchRequests method and tick-based auto-batching with manual batchContext support for async API clients*

 * (3 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript/pull/63937#issuecomment-5396890510) **dragomirtitian** suggested that the PR looked promising and asked for public exposure of batched requests, describing their internal yield*-based batching library

### [Issue microsoft/TypeScript#63959](https://github.com/microsoft/TypeScript/issues/63959) (Open, `Docs`)

**The new \`\-\-lsp\` flag is not mentioned in \`tsc \-\-help\`'s output**

*The new --lsp flag isn’t listed in tsc --help or tsc --help --all output, making it hard to find.*

 * created by **frou**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63959#issuecomment-5380994473) **MartinJohns** replied that the release notes contained that information
 * [today](https://github.com/microsoft/TypeScript/issues/63959#issuecomment-5391713416) **jakebailey** said "I don't this this is a flag that any random end user should know about, same with --api. Perhaps we should document it somewhere, but it doesn't seem useful otherwise?"
 * [later](https://github.com/microsoft/TypeScript/issues/63959#issuecomment-5391927215) **frou** criticized calling the omission patronising and questioned the assumption that all normal users use VSCode
 * [later](https://github.com/microsoft/TypeScript/issues/63959#issuecomment-5391964867) **jakebailey** asked for the context in which the flag documentation was missing
 * [later](https://github.com/microsoft/TypeScript/issues/63959#issuecomment-5392026205) **frou** explained that they installed TypeScript 7 and tweaked their Emacs config to use the new native LSP instead of typescript-language-server for TypeScript files

### [PR microsoft/TypeScript#63961](https://github.com/microsoft/TypeScript/pull/63961) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use pinned gzip for localization generation**

*Generate localization files using a pinned klauspost/compress gzip implementation to ensure consistent outputs across Go toolchains.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [later](https://github.com/microsoft/TypeScript/pull/63961#issuecomment-5397796900) **jakebailey** said "Actually, on second thought, my followup commit is a problem because it means every added or removed diagnostic changes every gz file. I'll undo that for now"

### [Issue microsoft/TypeScript#63966](https://github.com/microsoft/TypeScript/issues/63966) (Open, `Possible Improvement`)

**Performance regression for declaration emit of an oversized inferred type**

*TypeScript 7’s declaration emit for nested inferred types now uses significantly more memory and time and still produces TS7056 errors*

 * created by **daniellockyer**
 * [today](https://github.com/microsoft/TypeScript/issues/63966#issuecomment-5385271015) **yunasora** requested assignment to investigate and fix the declaration emit performance regression with tests and benchmarks
 * [today](https://github.com/microsoft/TypeScript/issues/63966#issuecomment-5391700327) **jakebailey** said "Did you have an actual project which hit this, or did you just find this with an LLM looking at the code?"
 * [today](https://github.com/microsoft/TypeScript/issues/63966#issuecomment-5391743046) **daniellockyer** explained that they found the repro via an LLM while improving memory usage of tsc/tsgo and noted they had other bugs tied to private projects for which they needed minimal public repros

### [Issue microsoft/TypeScript#63970](https://github.com/microsoft/TypeScript/issues/63970) (Open, `Suggestion`, `Awaiting More Feedback`)

**Inconsistent typing of endless generators between functions and lambdas**

*TypeScript infers void return for named infinite generators but never for generator lambdas, causing incompatible assignment errors.*

 * created by **jacekkopecky**
 * [today](https://github.com/microsoft/TypeScript/issues/63970#issuecomment-5387542405) **Andarist** explained that the behavior was deliberate for backwards compatibility and linked to the TypeScript rules for auto-inferring never return types

### [PR microsoft/TypeScript#63971](https://github.com/microsoft/TypeScript/pull/63971) (Open, `For Uncommitted Bug`)

**Fix crash on decorated anonymous class declaration**

*Prevent compiler crash when using decorators on anonymous class declarations.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63972](https://github.com/microsoft/TypeScript/pull/63972) (Open, `For Uncommitted Bug`)

**Fix crash on malformed object destructuring assignment**

*Ensure TypeScript no longer crashes when parsing malformed object destructuring assignments.*

 * created by **Andarist**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#63973](https://github.com/microsoft/TypeScript/pull/63973) (Open, `For Uncommitted Bug`)

**Fix crash on malformed super destructuring**

*Fix a TypeScript compiler crash when super destructuring is malformed.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63974](https://github.com/microsoft/TypeScript/pull/63974) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 3 updates**

*Upgrade the GitHub CodeQL Action steps (init, analyze, and upload-sarif) to their latest versions.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63975](https://github.com/microsoft/TypeScript/issues/63975) (Open, `Docs`)

**compilerOptions\.plugins is not inherited through tsconfig "extends"**

*compilerOptions.plugins defined in a base tsconfig.json are not inherited when using extends due to missing merge logic.*

 * created by **vickvu**
 * [today](https://github.com/microsoft/TypeScript/issues/63975#issuecomment-5391680191) **jakebailey** said "We don't even support plugins?"
 * [later](https://github.com/microsoft/TypeScript/issues/63975#issuecomment-5391942569) **vickvu** asked if there were other unsupported features in TS 7.x and whether watch and watchOptions were still supported

### [Issue microsoft/TypeScript#63976](https://github.com/microsoft/TypeScript/issues/63976) (Closed)

**Excessive string allocations in \`projectReferenceDtsFakingVfs\`**

*The directoryExistsIfProjectReferenceDeclDir method in projectReferenceDtsFakingVfs excessively allocates ephemeral strings, causing significant memory overhead.*

 * created by **auvred**

### [PR microsoft/TypeScript#63977](https://github.com/microsoft/TypeScript/pull/63977) (Closed, `For Uncommitted Bug`)

**Avoid allocations when checking project reference declaration directories**

*Replace allocation-heavy project reference directory checks with ContainsPath to eliminate allocations and improve textDocument/references performance.*

 * created by **auvred**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63978](https://github.com/microsoft/TypeScript/pull/63978) (Closed, `For Uncommitted Bug`)

**Fix inherit compilerOptions\.plugins across extends**

*Ensure compilerOptions.plugins are correctly inherited across extended TypeScript config files.*

 * created by **vickvu**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63978#issuecomment-5391650169) **vickvu** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63978#issuecomment-5391686325) **jakebailey** said "I don't think there's anything to do here. We don't support plugins. We just ignore that entirely, let alone do any extending."
 * [today](https://github.com/microsoft/TypeScript/pull/63978#issuecomment-5391720988) **vickvu** asked if the team still wanted to address 6.0/7.0 differences and if there was documentation on unsupported features
 * [later](https://github.com/microsoft/TypeScript/pull/63978#issuecomment-5391883514) **jakebailey** noted coverage by existing blog posts and asked how the need for fixing was determined
 * [later](https://github.com/microsoft/TypeScript/pull/63978#issuecomment-5391980973) **vickvu** explained having a fork of TypeScript that re-implemented all needed plugins in Go and said they would close the PR since the fix was unnecessary
 * (later) **vickvu** closed the issue

### [Issue microsoft/TypeScript#63979](https://github.com/microsoft/TypeScript/issues/63979) (Closed, `Out of Scope`, `Docs`)

**Official guidelines to build complex types**

*Proposal to add official TypeScript guidelines detailing supported tips, patterns, and pitfalls for constructing complex type definitions.*

 * created by **denis-migdal**

### [PR microsoft/TypeScript#63980](https://github.com/microsoft/TypeScript/pull/63980) (Open, `For Backlog Bug`)

**Re\-order Array\#reduce and Array\#reduceRight overloads in lib\.es5\.d\.ts**

*Prioritize generic Array#reduce and reduceRight overloads before same-type overloads in lib.es5.d.ts to improve type inference*

 * created by **sundeep8967**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#63981](https://github.com/microsoft/TypeScript/issues/63981) (Closed, `Bug`, `Fix Available`, **ahejlsberg**)

**\`TS2454\` false positive when a callback mutates an outer \`let\` and returns the enclosing function's parameter**

*TypeScript 7 falsely reports TS2454 when a closure compound-assigns an outer let and returns its parameter prior to that let’s initialization.*

 * created by **bent0b0x**

