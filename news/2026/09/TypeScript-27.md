# Report for 2026-09-27 (Sunday, September 27th, 2026)

19 different users commented on 32 different issues.

## Recommended Actions

 * Response Recommended
    * @danfry1 provided a workaround example in [microsoft/TypeScript#41160](https://github.com/microsoft/TypeScript/issues/41160#issuecomment-5859698553)
    * @malyzeli explained that their company requires Yarn PnP support before migrating to TS7 in [microsoft/TypeScript#63919](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5868202880)
    * @Amatewasu provided additional reproduction steps in [microsoft/TypeScript#64423](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-5870461095)
    * @z0rimo opened draft PR #64488 for a compatibility fix and requested triage in [microsoft/TypeScript#64453](https://github.com/microsoft/TypeScript/issues/64453#issuecomment-5862919851)
    * @typescript-automation[bot] provided perf results as requested in [microsoft/TypeScript#64481](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5857621494)

## Activity Summary

### [Issue microsoft/TypeScript#41160](https://github.com/microsoft/TypeScript/issues/41160) (Open, `Suggestion`, `Awaiting More Feedback`)

**Regex\-validated string types \(feedback reset\)**

*Requesting feedback on remaining TypeScript regex-validated string type use cases after recent design updates.*

 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/41160#issuecomment-2546810676) **RyanCavanaugh** praised feature #43335 and questioned how malformed UUIDs occur and why they are common despite immediate exceptions
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/41160#issuecomment-2547003197) **HansBrende** explained that correctly typing UUIDs would ensure they round-tripped to the server and prevent other string identifiers in the id field, noted that opaque tags solve this but feel hacky with hardcoded UUIDs, and proposed typed hex codes such as RGB or RGBA to avoid extra error handling
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/41160#issuecomment-3194518322) **codpro2005** proposed supporting composable Regex-validated string types via an intrinsic Regex<'pattern','flags'> type with inverse extraction
 * [today](https://github.com/microsoft/TypeScript/issues/41160#issuecomment-5859698553) **danfry1** provided a workaround that type-checked fixed-length hex strings in TypeScript using placeholder intersections and template literal types, with example code and explanation

### [PR microsoft/TypeScript#63919](https://github.com/microsoft/TypeScript/pull/63919) (Open, `For Uncommitted Bug`)

**Add Yarn PnP module resolution support**

*Add native Yarn Plug’n’Play module resolution support to TypeScript Go, including PnP VFS, API, and manifest handling.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5471741188) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #63769. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5737540898) **louisscruz** asked what blocks the PR from merging and explained being blocked on upgrading to TypeScript 7 due to a related issue
 * [later](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5868202880) **malyzeli** reported that their company required Yarn PnP due to a contractual obligation in the medical domain, preventing migration to TS7 without PnP

### [Issue microsoft/TypeScript#64423](https://github.com/microsoft/TypeScript/issues/64423) (Open, `Needs More Info`)

**TypeScript 7\.0\.2 silently runs out of memory while typechecking a project that TypeScript 6\.0\.3 checks successfully**

*TypeScript 7.0.2’s typechecker exhausts memory and fails on a project that compiles successfully under TypeScript 6.0.3.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-5828271795) **Amatewasu** provided TypeScript compiler output showing a fatal heap out of memory error
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-5828937397) **Amatewasu** reported LLM-generated investigation findings including measurements and a minimal reproduction for a TypeScript 7.0.2 OOM issue
 * [later](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-5870461095) **Amatewasu** provided an independent OOM reproduction using three/tsl method calls in TS 7.0.2

### [Issue microsoft/TypeScript#64453](https://github.com/microsoft/TypeScript/issues/64453) (Open)

**\`EFNoLeadingComments\` suppresses synthesized leading comments in tsgo; Strada only suppresses source comments**

*In tsgo, the EFNoLeadingComments emit flag also suppresses synthesized leading comments, unlike TypeScript’s NoLeadingComments which only suppresses source comments.*

 * created by **trevorade**
 * [today](https://github.com/microsoft/TypeScript/issues/64453#issuecomment-5862919851) **z0rimo** investigated printer behavior on main branch, identified a semantic difference with Strada emitter, and opened draft PR #64488 with a compatibility fix and regression tests pending triage

### [Issue microsoft/TypeScript#64459](https://github.com/microsoft/TypeScript/issues/64459) (Open)

**Publish \`fswatch\` Go package**

*Publish fswatch as a standalone Go package by dropping its internal flag and adding a go.mod for filesystem event monitoring.*

 * created by **emersion**
 * [later](https://github.com/microsoft/TypeScript/issues/64459#issuecomment-5865066241) **jakebailey** expressed reluctance to maintain a stable API and proposed copying the code with attribution

### [Issue microsoft/TypeScript#64462](https://github.com/microsoft/TypeScript/issues/64462) (Closed)

**Codex\.lunix{program\.null\.dull}**

*The .vscode/extensions.json file contains a malformed recommendation 'Codex.lunix{program.null.dull}' at line 4.*

 * created by **anno24075-bit**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64463](https://github.com/microsoft/TypeScript/issues/64463) (Open)

**\[LSP\] Memory of configured projects is never released, even after didClose of all files — ~70 MB retained per project \(7\.0\.2 and 7\.1\.0\-dev\.20260926\.1\)**

*TypeScript LSP never frees memory for closed projects, retaining about 70MB per project and causing memory bloat.*

 * created by **talkstream**
 * [later](https://github.com/microsoft/TypeScript/issues/64463#issuecomment-5865093315) **jakebailey** said "If you're using VS Code, we have pprof commands to take profiles, but in this case you actually would need to build from source and then use goref or something to find the leak."
 * [later](https://github.com/microsoft/TypeScript/issues/64463#issuecomment-5865101761) **jakebailey** said "Possibly https://github.com/microsoft/TypeScript/pull/64466 resolves this, though?"

### [Issue microsoft/TypeScript#64474](https://github.com/microsoft/TypeScript/issues/64474) (Open, **ahejlsberg**)

**checker builds member tables and intersection props it never uses**

*The TypeScript checker’s eager member and intersection property instantiation causes high memory use and is optimized to build needed properties.*

 * created by **maschwenk**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64474#issuecomment-5852758422) **maschwenk** described the benchmarking methodology and results comparing main and PR commits, including hardware specifications, commands, scenarios, replication details, performance and memory improvements, and a gist link
 * **ahejlsberg** assigned to **ahejlsberg**

### [PR microsoft/TypeScript#64481](https://github.com/microsoft/TypeScript/pull/64481) (Open, `Author: Team`, `For Backlog Bug`, **ahejlsberg**)

**Don't reduce intersections of mappings of the same object type**

*Prevent TypeScript from reducing intersections of homomorphic object mappings to enable recursive Zod schemas*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5857421924) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5857422515) **typescript-automation[bot]** reported CI jobs starting and their status with result links
 * [today](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5857621494) **typescript-automation[bot]** provided the results of the requested perf run
 * [today](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5857640803) **typescript-automation[bot]** reported one Git clone failure and one package install failure and indicated everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5857701525) **typescript-automation[bot]** notified that DT tests results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5857806432) **ahejlsberg** said "Apparently this pattern accounts for a substantial number of types in mui-docs, so nice savings there."
 * [today](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5857997842) **typescript-automation[bot]** ran tests on the top 400 repos and reported everything looked good

### [PR microsoft/TypeScript#64482](https://github.com/microsoft/TypeScript/pull/64482) (Open, `For Uncommitted Bug`)

**Fix flaky diagnostic added by declaration emit through \`MarkLinkedReferencesRecursively\`**

*Modify the declaration emit process to fix flaky diagnostics introduced by MarkLinkedReferencesRecursively and prevent crashes.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64482#issuecomment-5857888374) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64483](https://github.com/microsoft/TypeScript/issues/64483) (Open)

**\`getChildren\(\)\` includes synthetic NodeObjects, that can't easily be discerned from RemoteNodes**

*In TypeScript’s unstable API, getChildren() returns synthetic NodeObjects alongside RemoteNodes without distinguishing them, causing getNodeId errors.*

 * created by **Qjuh**

### [Issue microsoft/TypeScript#64484](https://github.com/microsoft/TypeScript/issues/64484) (Open)

**Unused locals in class static block declarations are not reported**

*TypeScript fails to report unused local variables declared in class static blocks when noUnusedLocals is enabled.*

 * created by **Andarist**

### [PR microsoft/TypeScript#64485](https://github.com/microsoft/TypeScript/pull/64485) (Open, `For Uncommitted Bug`)

**Report unused locals in class static blocks**

*Add support for detecting and reporting unused local variables declared inside class static blocks.*

 * created by **Andarist**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64485#issuecomment-5858665378) **jakebailey** said "@typescript-bot test top1000"
 * [today](https://github.com/microsoft/TypeScript/pull/64485#issuecomment-5858666039) **typescript-automation[bot]** reported that the test top1000 job started and provided status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64485#issuecomment-5859682405) **typescript-automation[bot]** provided tsc comparison results for the top 1000 repos and confirmed that everything looked good

### [Issue microsoft/TypeScript#64486](https://github.com/microsoft/TypeScript/issues/64486) (Open)

**TS2589 error in TSGo with recursive mapped type over DOM types but not is tsc; ~18x more instantiations than tsc**

*TSGo 7.0.2 triggers TS2589 deep instantiation applying a recursive DeepPartial type to DOM types, performing ~18× more instantiations than tsc.*

 * created by **promitdan**

### [PR microsoft/TypeScript#64487](https://github.com/microsoft/TypeScript/pull/64487) (Open, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 3 updates**

*Upgrade github/codeql-action init, analyze, and upload-sarif actions to their latest released versions.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64488](https://github.com/microsoft/TypeScript/pull/64488) (Open, `For Uncommitted Bug`)

**Fix synthesized comment emission with comment flags**

*Restore Strada-compatible comment emission so EFNoLeadingComments and EFNoTrailingComments suppress only original comments while preserving synthesized ones.*

 * created by **z0rimo**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64489](https://github.com/microsoft/TypeScript/pull/64489) (Open, `For Backlog Bug`)

**Contextually type array literal spread operands**

*Contextually type array literal spread operands to prevent premature property widening and assignability errors.*

 * created by **WhitefistEmperor**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64489#issuecomment-5865394478) **WhitefistEmperor** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64490](https://github.com/microsoft/TypeScript/issues/64490) (Open)

**TypeScript 7\.0\.2 scanner does not advance on bare hash**

*TypeScript 7.0.2 scanner gets stuck on a bare '#' and repeatedly returns the same token without advancing.*

 * created by **yum45f**

### [PR microsoft/TypeScript#64491](https://github.com/microsoft/TypeScript/pull/64491) (Open, `For Uncommitted Bug`)

**Match Strada and don't resolve imports of ambient modules declared in the same file**

*Do not resolve imports of ambient modules declared in the same file to external typings, preventing excessive type instantiations.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64491#issuecomment-5865431338) **jakebailey** said "How does this fix a type explosion issue? Did you misquote the fixed issue?"
 * [later](https://github.com/microsoft/TypeScript/pull/64491#issuecomment-5866502732) **Andarist** said "@jakebailey the referenced issue is correct, I put more info to the PR description to explain why this resolves that issue"

### [Issue microsoft/TypeScript#64492](https://github.com/microsoft/TypeScript/issues/64492) (Open)

**External directory from tsconfig \`files\` gets no watcher in LSP**

*The TypeScript LSP fails to add file watchers for external directories specified in tsconfig.json’s files array.*

 * created by **auvred**

### [PR microsoft/TypeScript#64493](https://github.com/microsoft/TypeScript/pull/64493) (Open, `For Uncommitted Bug`)

**Don't let \`append\` overwrite sibling results in \`tspath\.GetCommonParents\`**

*tspath.GetCommonParents' use of append on subslices with leftover capacity causes sibling results to overwrite each other.*

 * created by **auvred**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64494](https://github.com/microsoft/TypeScript/issues/64494) (Open)

**Decorated class gets \`name === "\_a"\` when a \`\#private\` field initializer references the class \(regression in 7\.0\)**

*Decorated classes with private field initializers referencing the class incorrectly get named `_a` instead of their declared name.*

 * created by **bagbag**

### [Issue microsoft/TypeScript#64495](https://github.com/microsoft/TypeScript/issues/64495) (Open)

**Record\<K1, T\> & Record\<K2, U\> is assignable to Record\<K1 \| K2, T & U\>**

*TypeScript allows Record<K1, T> & Record<K2, U> to be assigned to Record<K1 | K2, T & U>, unsoundly merging property types.*

 * created by **ahmedajiz629**

### [Issue microsoft/TypeScript#64496](https://github.com/microsoft/TypeScript/issues/64496) (Open)

**display the inferred return type**

*Provide hover tooltips on individual return keywords to display the specific returned expression’s inferred type.*

 * created by **iuliust**
 * **vs-code-engineering[bot]** assigned to **dbaeumer**
 * **dbaeumer** unassigned **dbaeumer**

### [Issue microsoft/TypeScript#64497](https://github.com/microsoft/TypeScript/issues/64497) (Open)

**Find all references on \`from\` of a default import drops results after an unsaved edit in another file**

*In TypeScript 7.0.2, an unsaved edit causes find-all-references on a default import's from in another file to drop results*

 * created by **wangzhihao-lab**

### [Issue microsoft/TypeScript#64498](https://github.com/microsoft/TypeScript/issues/64498) (Open)

**Program\.emitToString\(\) silently omits real files due to nondeterministic isSourceFileFromExternalLibrary\(\) misclassification**

*TypeScript’s Program.emitToString sometimes excludes real source files because isSourceFileFromExternalLibrary nondeterministically marks them as external library files.*

 * created by **jelical**

### [PR microsoft/TypeScript#64499](https://github.com/microsoft/TypeScript/pull/64499) (Open, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Only check properties with multiple declarations for never\-reduction**

*Optimize getReducedType by limiting never-type reduction checks to properties declared in multiple intersection constituents.*

 * created by **ahejlsberg**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/pull/64499#issuecomment-5873312085) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/64499#issuecomment-5873314200) **typescript-automation[bot]** posted initial build status table with pending jobs

