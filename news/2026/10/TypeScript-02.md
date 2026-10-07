# Report for 2026-10-02 (Friday, October 2nd, 2026)

20 different users commented on 62 different issues.

## Recommended Actions

 * Response Recommended
    * @ethndotsh asked for a review now that the bug is marked as backlog in [microsoft/TypeScript#64426](https://github.com/microsoft/TypeScript/pull/64426#issuecomment-5958215226)
    * @gwkline offered to run additional tests and asked if a second public repro would be useful in [microsoft/TypeScript#64469](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-5969259018)
    * @gwkline provided a link to their final implementation in [microsoft/TypeScript#64469](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-5969338823)
    * @michaelfig asked whether the Related Work section of #64451 is sufficient to close the issue and how to satisfy @typescript-automation in [microsoft/TypeScript#64585](https://github.com/microsoft/TypeScript/issues/64585#issuecomment-5959601794)

## Activity Summary

### [Issue microsoft/TypeScript#44174](https://github.com/microsoft/TypeScript/issues/44174) (Closed, `Needs Investigation`, `Domain: Performance`, **jakebailey**)

**normalizeSlashes should probably no\-op on \*nix**

*Propose making normalizeSlashes a no-op on non-Windows platforms to avoid altering valid backslash filenames and improve performance.*

 * (3.4 years ago) **jakebailey** removed label `Rescheduled`, set milestone to `Backlog`, and removed from milestone `TypeScript 5.1.0`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#61216](https://github.com/microsoft/TypeScript/issues/61216) (Closed, `Suggestion`, `Help Wanted`, `Committed`)

**Support source phase imports**

*Enable TC39 source phase imports in TypeScript to allow importing raw WebAssembly modules directly.*

 * (6 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.1`, and removed from milestone `TypeScript 5.9.0`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/61216#issuecomment-5914953287) **RyanCavanaugh** described offline discussion and proposed a minimal implementation for source-phase imports in 7.1
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63248](https://github.com/microsoft/TypeScript/pull/63248) (Closed, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Add lib types for JSON\.rawJSON, JSON\.isRawJSON, and reviver context**

*Add ES2025 JSON lib type definitions for JSON.rawJSON, JSON.isRawJSON, and JSON.parse reviver context support.*

 * (yesterday) **VedantMadane** closed the issue
 * (yesterday) **VedantMadane** reopened the issue
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-5927679800) **VedantMadane** rebased onto main and resolved merge conflicts, regenerated embedded files, kept es2025 JSON typings, and called for a maintainer decision on retaining es2025.json
 * [today](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-5966012635) **VedantMadane** said "Closing this PR as the feature has already landed upstream under lib.es2026.json.d.ts via #64096. Thank you!"
 * (today) **VedantMadane** closed the issue

### [Issue microsoft/TypeScript#63722](https://github.com/microsoft/TypeScript/issues/63722) (Closed, `Help Wanted`, `Domain: lib.d.ts`)

**\`Array\.prototype\.at\` docs use "code unit" instead of "item"**

*Array.prototype.at documentation mistakenly uses 'code unit' instead of 'item' or 'element' terminology.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63722#issuecomment-5217573985) **grundb** said "PR done! 😃  "
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63722#issuecomment-5490018388) **LeonxLJX** said "I'd like to take this one — I'll follow up with a PR. (claiming via @LeonxLJX)"
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63722#issuecomment-5492440463) **LeonxLJX** said "Hi! I'd like to fix the Array.prototype.at docs wording ('code unit' -> 'item'). Trivial docs fix. May I be assigned?"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63800](https://github.com/microsoft/TypeScript/issues/63800) (Closed, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63800#issuecomment-5351503962) **NullVoxPopuli** explained Ember component format in glimmer-ts preserving block scope semantics and provided code examples
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63800#issuecomment-5351503987) **andrewbranch** asked for confirmation about the need for multiple virtual backing files due to global script scope across multiple HTML-like files
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63800#issuecomment-5351503998) **andrewbranch** noted that multiple distinct files mapping from a single non-TS file is now supported in microsoft/typescript-go#4712
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#63915](https://github.com/microsoft/TypeScript/pull/63915) (Closed, `For Milestone Bug`)

**Support source phase imports**

*Implement support for the TC39 Source Phase Imports proposal*

 * created by **a-tarasyuk**
 * (6 weeks ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Milestone Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64159](https://github.com/microsoft/TypeScript/pull/64159) (Closed, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Strongly type file paths**

*Add branded types for absolute, normalized file and directory paths to enforce path invariants and reduce normalization overhead.*

 * (1 month ago) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64159#issuecomment-5702887286) **jakebailey** said "I guess I can try and flip the API side back to strings, but there's a bunch of conversions we get to skip because of it, and some of the bugs found were on the API side outside the Go code."
 * [today](https://github.com/microsoft/TypeScript/pull/64159#issuecomment-5961659959) **andrewbranch** said "(not that the conflict-free state is going to survive the stuff already enabled to auto-merge)"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64426](https://github.com/microsoft/TypeScript/pull/64426) (Open, `For Backlog Bug`)

**Type a recursive call\-initialized object literal property lazily**

*Enable object literal properties initialized by function calls to be typed lazily to handle recursive types.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64426#issuecomment-5817989945) **ethndotsh** said "@microsoft-github-policy-service agree"
 * (3 days ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64426#issuecomment-5958215226) **ethndotsh** said "Just following up now that this is marked as a backlog bug if we can get this reviewed :)"

### [Issue microsoft/TypeScript#64450](https://github.com/microsoft/TypeScript/issues/64450) (Closed, `Needs Investigation`, **johnfav03**)

**createWatchProgram\(\)\.close\(\) does not cancel the pending program update timer**

*close() does not cancel the pending program update timer in createWatchProgram, causing updates to run after closure and preventing process exit.*

 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/issues/64450#issuecomment-5950681585) **skywalkersPadawan** opened PR #64587 targeting release-6.0 that cleared the pending timerToUpdateProgram in createWatchProgram().close with a regression test and asked if the issue needs linking or different triage
 * [today](https://github.com/microsoft/TypeScript/issues/64450#issuecomment-5957580501) **jakebailey** said "I do not think we're going to be patching or releasing TS 6.0."

### [Issue microsoft/TypeScript#64463](https://github.com/microsoft/TypeScript/issues/64463) (Open, `Bug`)

**\[LSP\] Memory of configured projects is never released, even after didClose of all files — ~70 MB retained per project \(7\.0\.2 and 7\.1\.0\-dev\.20260926\.1\)**

*TypeScript LSP never frees memory for closed projects, retaining about 70MB per project and causing memory bloat.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64463#issuecomment-5865093315) **jakebailey** said "If you're using VS Code, we have pprof commands to take profiles, but in this case you actually would need to build from source and then use goref or something to find the leak."
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64463#issuecomment-5865101761) **jakebailey** said "Possibly https://github.com/microsoft/TypeScript/pull/64466 resolves this, though?"
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64463#issuecomment-5873826780) **jakebailey** explained that the test verifies longstanding behavior of not closing the project on file close to avoid reloads and asked if the same was tried on TS 6.0
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64469](https://github.com/microsoft/TypeScript/pull/64469) (Open, `For Uncommitted Bug`, **johnfav03**)

**Index re\-exporting modules for declaration emit**

*Optimize TypeScript’s declaration emit performance by caching an export-to-module index to avoid repeated scans during incremental rebuilds*

 * created by **resure**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-5847125871) **resure** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-5969259018) **gwkline** provided independent performance benchmarks applying the PR’s checker changes to a large monorepo, reported byte-identical outputs, noted speedups and minor memory increase, described optional incremental changes, highlighted a merge conflict, and offered further tests with a public repro
 * [later](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-5969338823) **gwkline** provided a link to their final implementation commit

### [PR microsoft/TypeScript#64536](https://github.com/microsoft/TypeScript/pull/64536) (Closed, `For Backlog Bug`)

**Fix Array\.at documentation: change 'code unit' to 'item'**

*Updated Array.at and TypedArray.at documentation to replace 'code unit' with 'item' in index parameter descriptions.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64536#issuecomment-5900379984) **RyanCavanaugh** said "This is good to go but I can't merge it until the CLA is signed"
 * [today](https://github.com/microsoft/TypeScript/pull/64536#issuecomment-5948397985) **iamawanishmaurya** said "@microsoft-github-policy-service agree"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64546](https://github.com/microsoft/TypeScript/issues/64546) (Closed, `Working as Intended`)

**Content mappers: registered extensions are not probed for extensionless imports in bundler mode**

*In bundler mode, TypeScript does not probe registered custom contentMapper extensions for extensionless imports, causing TS2307 errors.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64546#issuecomment-5900568575) **RyanCavanaugh** clarified that content mappers don't participate in module resolution and asked where this was inferred in the description
 * **RyanCavanaugh** added label `Working as Intended`
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64546#issuecomment-5901727760) **leonidaz** clarified a misunderstanding about content mappers and module resolution, opened new suggestion issue #64549 and a separate issue #64548 for moduleSuffixes, and asked to close this one in favor of those issues
 * [today](https://github.com/microsoft/TypeScript/issues/64546#issuecomment-5964096360) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#64548](https://github.com/microsoft/TypeScript/issues/64548) (Closed, `Working as Intended`)

**Content mappers: \`moduleSuffixes\` probes \`card\.foo\.web\` instead of \`card\.web\.foo\` for a registered extension**

*When using moduleSuffixes with a registered content mapper, a fully specified import probes the suffix after the custom extension (card.foo.web) instead of before (card.web.foo), resolving to the wrong file.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64548#issuecomment-5915868733) **RyanCavanaugh** clarified that content mappers do not change moduleSuffixes behavior and that import specifiers must include the mapper's extension
 * **RyanCavanaugh** added label `Working as Intended`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64548#issuecomment-5916751267) **leonidaz** filed issue #64560 suggesting an optional moduleSuffixes list on contentMappers entries and offered to close this issue in favor of it
 * [today](https://github.com/microsoft/TypeScript/issues/64548#issuecomment-5964096116) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#64562](https://github.com/microsoft/TypeScript/pull/64562) (Closed, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump brace\-expansion from 5\.0\.9 to 5\.0\.12**

*Update brace-expansion dependency from version 5.0.9 to 5.0.12.*

 * (2 days ago) **dependabot[bot]** added labels `dependencies`, `javascript`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64564](https://github.com/microsoft/TypeScript/issues/64564) (Closed, `Domain: Content Mappers`, **andrewbranch**)

**TypeScript 7 VS Code extension: closing JSX tags are not inserted in content\-mapped files, although tsc \-\-lsp provides them**

*The VS Code TypeScript 7 extension omits on-auto-insert for closing JSX tags in content-mapped files despite language server support.*

 * created by **leonidaz**
 * (yesterday) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `Domain: Content Mappers`, assigned to **andrewbranch**, and unassigned **RyanCavanaugh**, **Copilot**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64572](https://github.com/microsoft/TypeScript/pull/64572) (Closed, `For Uncommitted Bug`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**Enable JSX auto\-insert in content\-mapped files**

*Enable JSX closing tag auto-insertion in content-mapped files by extending auto-insert registration and updating event listeners.*

 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64572#issuecomment-5939616122) **jakebailey** said "This seems like a good fix but I'm a bit confused how it fixes the linked issue."
 * [today](https://github.com/microsoft/TypeScript/pull/64572#issuecomment-5956683429) **RyanCavanaugh** said "It moves the code to the CM-specific block https://github.com/microsoft/TypeScript/pull/64572/changes#diff-c3b70804ef705332d4984e12414f615177053a389860c92e7eea9db6c4319ce1L374"
 * **RyanCavanaugh** assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64582](https://github.com/microsoft/TypeScript/issues/64582) (Open, `Possible Improvement`)

**Info missing when hover on a proptery compare to TS6**

*TS7 hover on an index-signature property shows only its base type instead of the full index signature info from TS6.*

 * created by **Withered-Flower-0422**
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64583](https://github.com/microsoft/TypeScript/pull/64583) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Allow other VS Code extensions to install LSP middleware on language feature responses**

*Enable third-party VS Code extensions to register custom LSP middleware for TypeScript language feature responses*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64585](https://github.com/microsoft/TypeScript/issues/64585) (Open, `Duplicate`)

**TS Symbol typing clashes with standard, idiomatic JS**

*TypeScript’s symbol typing model conflicts with JavaScript’s native Symbol behavior, hindering idiomatic JS symbol usage.*

 * created by **michaelfig**
 * [today](https://github.com/microsoft/TypeScript/issues/64585#issuecomment-5956824676) **RyanCavanaugh** said "This seems like a straightforward duplicate of #35909, not a separate request"
 * [today](https://github.com/microsoft/TypeScript/issues/64585#issuecomment-5959601794) **michaelfig** identified the issue as a duplicate of #35909, offered to close it if the Related Work section of #64451 sufficed, and noted uncertainty about satisfying @typescript-automation

### [PR microsoft/TypeScript#64586](https://github.com/microsoft/TypeScript/pull/64586) (Open, `For Backlog Bug`)

**Restore index signature details in property hovers**

*Restore index signature details in TypeScript property hover tooltips to show key and value type information.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64587](https://github.com/microsoft/TypeScript/pull/64587) (Closed, `For Uncommitted Bug`)

**fix\(64450\): clear the pending program update timer when a watch program is closed**

*Clear the pending program update timer when a watch program is closed to prevent lingering watchers and process hangs.*

 * (today) **skywalkersPadawan** closed the issue
 * (today) **skywalkersPadawan** reopened the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64587#issuecomment-5950617247) **skywalkersPadawan** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64587#issuecomment-5957572617) **jakebailey** said "We're definitely not going to be backporting this or releasing 6.0."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64588](https://github.com/microsoft/TypeScript/pull/64588) (Open, `For Uncommitted Bug`)

**Restore symbol names in JSX import action titles**

*Restores symbol names in JSX import action titles by porting Strada’s logic and fixes two skipped tests.*

 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64588#issuecomment-5953399343) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64588#issuecomment-5957506745) **jakebailey** said "Copilot absolutely hates this 😄 "

### [PR microsoft/TypeScript#64595](https://github.com/microsoft/TypeScript/pull/64595) (Open, `For Milestone Bug`)

**Avoid duplicate assignability errors on literal unions**

*Eliminate redundant assignability errors when a literal union's generalized type matches its constituents.*

 * created by **bodapatisaikrishna**
 * **typescript-automation[bot]** added label `For Milestone Bug`

### [Issue microsoft/TypeScript#64596](https://github.com/microsoft/TypeScript/issues/64596) (Open, **RyanCavanaugh**, **Copilot**)

**npm package has "engines": "\>=16\.2\.0" but \`npx tsc\` fails on node \<20**

*npx tsc fails on Node 16/18 with TypeScript 7.0.2 due to unsupported extensionless bin file in module context.*

 * created by **sandersn**
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#64597](https://github.com/microsoft/TypeScript/pull/64597) (Closed, `For Uncommitted Bug`)

**Fixup misported \`TokensAreOnSameLine\`**

*Correct the misporting of the TokensAreOnSameLine rule to ensure it functions as intended.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64597#issuecomment-5957246778) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64598](https://github.com/microsoft/TypeScript/pull/64598) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add various merged symbol checker methods**

*Add various merged symbol checker methods to the TypeScript API following previous review feedback*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64599](https://github.com/microsoft/TypeScript/pull/64599) (Open, `For Milestone Bug`, **weswigham**)

**Check package reachability before using exports in declarations**

*Reorder TypeScript’s export resolution logic to ensure package reachability is checked before applying exports in declarations*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64599#issuecomment-5957454475) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64600](https://github.com/microsoft/TypeScript/pull/64600) (Closed, `For Uncommitted Bug`)

**don't copy union and intersection properties into the augmented property cache**

*Prevent unnecessary copying of union and intersection properties into the augmented property cache and defer cache map allocation to reduce memory overhead.*

 * created by **maschwenk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64600#issuecomment-5963635621) **maschwenk** said "Withdrawing this one: the gain is too small to be worth reviewer time on its own. The larger change is #64475 / #64526."
 * (today) **maschwenk** closed the issue

### [PR microsoft/TypeScript#64601](https://github.com/microsoft/TypeScript/pull/64601) (Closed, `For Uncommitted Bug`)

**instantiate conditional types without a combined mapper for the cache lookup**

*Optimize conditional type instantiation to bypass composite mapper creation for cache lookups, saving millions of allocations.*

 * created by **maschwenk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64601#issuecomment-5963635944) **maschwenk** said "Withdrawing this one: the gain is too small to be worth reviewer time on its own. The larger change is #64475 / #64526."
 * (today) **maschwenk** closed the issue

### [Issue microsoft/TypeScript#64602](https://github.com/microsoft/TypeScript/issues/64602) (Open, `Waiting for TC39`)

**Support deferred re\-exports**

*Support Stage 2 TC39 deferred re-export syntax in TypeScript, preserving JavaScript output and declaration types.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript#64603](https://github.com/microsoft/TypeScript/pull/64603) (Open, `Author: Team`, `For Backlog Bug`, **RyanCavanaugh**)

**Release unused LSP configured projects during idle cleanup**

*Unused LSP-configured projects are released during idle cleanup to free resources.*

 * created by **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Backlog Bug`, removed label `For Uncommitted Bug`, and assigned to **RyanCavanaugh**

### [PR microsoft/TypeScript#64604](https://github.com/microsoft/TypeScript/pull/64604) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update DOM types**

*Add and refine TypeScript DOM types to support new Web APIs, HTML sanitization, CSS and animation features, and compatibility changes*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5958359210) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5958360672) **typescript-automation[bot]** posted an automated build status comment listing started CI jobs
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5958815037) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5958890584) **typescript-automation[bot]** reported user test results comparing baseline and pr and indicated a new TS2322 error in axios-src tests
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5958899681) **typescript-automation[bot]** reported DT tests results showing compile errors in d3-fetch packages due to crossOrigin type incompatibility
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5959285715) **jakebailey** said "The perf regressions seem to entirely be due to the checker affinity heuristic, where lib.d.dom's size increase pushes something over the edge. A shame, but requires some future tweaks."
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5959300230) **jakebailey** said "The other errors are of couse just "DOM has more decls" and so will require some typesVersions etc."
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5959842795) **typescript-automation[bot]** reported tsc comparison results on top 400 repos and pointed out build failures and type errors in alibaba/page-agent
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5959901336) **jakebailey** noted that fetch accepting extra parameters caused confusion among implementers unfamiliar with its signature and expressed uncertainty about resolving the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5961950897) **saschanaz** said "Should we back it out and investigate the options? "
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5962132954) **jakebailey** said "Yeah, I think that would be wise"

### [Issue microsoft/TypeScript#64605](https://github.com/microsoft/TypeScript/issues/64605) (Open, `Needs Investigation`, **gabritto**)

**TS5115 in published Zod 4\.5–4\.6 types after \#64372**

*Zod 4.5.0–4.6.5 z.json() types cause TS5115 infinite circularity errors in TypeScript 7.1 nightlies after PR #64372, impacting ~62M weekly downloads.*

 * created by **colinhacks**

### [PR microsoft/TypeScript#64606](https://github.com/microsoft/TypeScript/pull/64606) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix tsc launcher compatibility with Node\.js 16 and 18**

*Rename TypeScript's tsc CLI launcher to .js and update package metadata for Node.js 16 and 18 compatibility.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64606#issuecomment-5960941253) **jakebailey** attributed the break to replacing bin/tsgo.js with bin/tsc during the repo move and questioned its safety

### [PR microsoft/TypeScript#64607](https://github.com/microsoft/TypeScript/pull/64607) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Wrap all fsevents event\-delivery tests in runWithRetry**

*Wrap all fsevents event-delivery tests in runWithRetry to enhance test reliability on macOS CI*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64608](https://github.com/microsoft/TypeScript/pull/64608) (Closed, `For Uncommitted Bug`)

**Update localization files**

*Update localization files and regenerate corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64609](https://github.com/microsoft/TypeScript/pull/64609) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Enable OneLoc handback**

*Configure the package ID containing localizations to enable the working OneLoc handback flow.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64609#issuecomment-5961574630) **jakebailey** said "Actually, want to do some cleanup here quick"
 * [today](https://github.com/microsoft/TypeScript/pull/64609#issuecomment-5965048954) **jakebailey** said "#64608 basicalyl merges this for me, so I'll just do that"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64610](https://github.com/microsoft/TypeScript/issues/64610) (Open, `Suggestion`)

**Associate companion files with \`ProjectService\` without Content Mappers**

*Allow ProjectService to include companion files such as .html templates without requiring content mappers.*

 * created by **atscott**

### [Issue microsoft/TypeScript#64611](https://github.com/microsoft/TypeScript/issues/64611) (Open, `Suggestion`)

**In\-memory virtual file overlay over LSP without faking \`didOpen\`**

*Add an LSP overlay mechanism to inject synthetic in-memory files into TS-Go’s virtual file system without faking didOpen notifications.*

 * created by **atscott**

### [Issue microsoft/TypeScript#64612](https://github.com/microsoft/TypeScript/issues/64612) (Closed)

**\[ServerErrors\]\[JavaScript\] main vs **

*An Azure pipeline run on 300 popular TS repos comparing main reported seven interesting changes, timeouts, and failures.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/64612#issuecomment-5962868741) **typescript-automation[bot]** reported a panic debug failure with a stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/64612#issuecomment-5962869247) **typescript-automation[bot]** reported a panic during textDocument/diagnostic handling and listed affected repos, artifacts, and recent requests
 * [today](https://github.com/microsoft/TypeScript/issues/64612#issuecomment-5962869766) **typescript-automation[bot]** reported a premature server connection closure error (undefined) for apache/pouchdb integration tests
 * [today](https://github.com/microsoft/TypeScript/issues/64612#issuecomment-5962870246) **typescript-automation[bot]** reported that the server connection closed prematurely with undefined error for rollup/rollup and provided repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64612#issuecomment-5962870675) **typescript-automation[bot]** reported server connection closed prematurely (undefined) for hakimel/reveal.js and provided error details with repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64612#issuecomment-5962871165) **typescript-automation[bot]** logged a panic while handling textDocument/diagnostic and provided a stack trace with affected repositories
 * [today](https://github.com/microsoft/TypeScript/issues/64612#issuecomment-5962871642) **typescript-automation[bot]** reported a panic handling request for textDocument/diagnostic and included a stack trace and affected repos
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64613](https://github.com/microsoft/TypeScript/issues/64613) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch’s error-deltas CI pipeline experienced clone failures, timeouts, and unknown errors when analyzing 300 popular repositories.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963664419) **typescript-automation[bot]** reported a panic while handling textDocument/diagnostic request with stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963664798) **typescript-automation[bot]** logged a panic stack trace for textDocument/diagnostic during LSP server execution on mksglu/context-mode
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963665237) **typescript-automation[bot]** reported panic handling textDocument/diagnostic request with a stack trace and affected pubkey/rxdb repo
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963665646) **typescript-automation[bot]** reported a panic: runtime error index out of range in the internal checker
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963666070) **typescript-automation[bot]** reported a panic during request textDocument/diagnostic due to an unhandled AST.CallExpression case
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963666498) **typescript-automation[bot]** reported a panic in the textDocument/diagnostic handler with a stack trace and affected repository details
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963666977) **typescript-automation[bot]** logged a panic handling textDocument/diagnostic request with a stack trace affecting date-fns/date-fns
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963667377) **typescript-automation[bot]** reported a panic while handling a textDocument/diagnostic request with a stack trace in the typescript-go LSP server affecting the mermaid-js/mermaid repo
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963667829) **typescript-automation[bot]** reported a panic in request textDocument/diagnostic with stack trace and affected repos
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963668208) **typescript-automation[bot]** reported that the server connection closed prematurely with undefined
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963668685) **typescript-automation[bot]** reported server connection closed prematurely with undefined error for vercel/ai in automated CI run
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963669069) **typescript-automation[bot]** reported server connection closed prematurely with undefined and provided affected repo, last requests, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963669442) **typescript-automation[bot]** reported server connection closed prematurely error and provided affected repo, error details, last requests, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963669874) **typescript-automation[bot]** reported a premature server connection closure with undefined and provided affected repos, logs, last requests, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963670317) **typescript-automation[bot]** reported a server connection closed prematurely error with affected repo details and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963670816) **typescript-automation[bot]** reported that the server connection closed prematurely and provided logs, affected repository details, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64613#issuecomment-5963671259) **typescript-automation[bot]** reported a runtime panic due to invalid memory address or nil pointer dereference
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64614](https://github.com/microsoft/TypeScript/issues/64614) (Open, `Bug`, **weswigham**)

**TS 7 declaration emit writes unbound type parameters \(TOutputOut, $Output\) into \.d\.ts where 6\.0 emits any**

*TypeScript 7 declaration emit leaks TOutputOut and $Output into .d.ts instead of using any*

 * created by **nextor2k**
 * [later](https://github.com/microsoft/TypeScript/issues/64614#issuecomment-5968338199) **Andarist** observed that emitting `any` was not expected behavior and that the declaration emitter should error, but the error was accidentally suppressed in TS6

### [PR microsoft/TypeScript#64615](https://github.com/microsoft/TypeScript/pull/64615) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Restore dependency\-depth build scheduling**

*Restore the dependency-depth-based build scheduling functionality removed by PR #64158 that regressed PR #64220.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64616](https://github.com/microsoft/TypeScript/pull/64616) (Open, `For Uncommitted Bug`)

**fix: improve error message for JSX in non\-module files \(Issue \#64438\)**

*Show a clear TS7026 error for JSX in non-module files instead of the misleading missing react/jsx-runtime message.*

 * created by **OMD-123**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#64617](https://github.com/microsoft/TypeScript/pull/64617) (Closed, `For Uncommitted Bug`)

**Handle JSDocParameterTag in ast\.GetTypeAnnotationNode**

*Include handling for JSDocParameterTag in ast.GetTypeAnnotationNode to ensure consistency with Node.Type*

 * created by **auvred**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64617#issuecomment-5967118139) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64618](https://github.com/microsoft/TypeScript/issues/64618) (Open, `Bug`, **RyanCavanaugh**)

**Non\-enum CLI options with multiple values separated by comma and space aren't whitespace trimmed**

*Comma-separated non-enum TypeScript CLI options retain leading whitespace instead of trimming values.*

 * created by **auvred**

### [PR microsoft/TypeScript#64619](https://github.com/microsoft/TypeScript/pull/64619) (Open, `For Milestone Bug`, **RyanCavanaugh**)

**Trim whitespaces in comma\+space separated string\-list CLI option values**

*Trim whitespace around comma-and-space-separated string-list CLI option values to match TypeScript parser behavior.*

 * created by **auvred**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64620](https://github.com/microsoft/TypeScript/pull/64620) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove legacy localization handbacks**

*Remove legacy localization handbacks since OneLoc now provides translations.*

 * created by **jakebailey**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

