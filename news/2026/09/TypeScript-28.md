# Report for 2026-09-28 (Monday, September 28th, 2026)

29 different users commented on 84 different issues.

## Recommended Actions

 * Response Recommended
    * @tbknl proposed a generic signature for MapConstructor::new and asked for acknowledgement of its plausibility in [microsoft/TypeScript#33611](https://github.com/microsoft/TypeScript/issues/33611#issuecomment-5888769796)
    * @z0rimo asked for another review in [microsoft/TypeScript#64257](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-5883585069)
    * @Emut asked about whether a 7.0.3 release will be available or if they should wait for 7.1.0 in [microsoft/TypeScript#64262](https://github.com/microsoft/TypeScript/issues/64262#issuecomment-5891481987)
    * @vladyslav005 asked if they could contribute to the project in [microsoft/TypeScript#64433](https://github.com/microsoft/TypeScript/issues/64433#issuecomment-5878304962)
    * @Fugu0141 asked whether to close in favor of #64525 or explore a broader approach in [microsoft/TypeScript#64502](https://github.com/microsoft/TypeScript/pull/64502#issuecomment-5887759684)
    * @hkleungai noted that the PR might resolve issue #63523 in [microsoft/TypeScript#64527](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5891462911)
    * @Amatewasu provided benchmarking results as requested in [microsoft/TypeScript#64528](https://github.com/microsoft/TypeScript/pull/64528#issuecomment-5892189219)

## Activity Summary

### [Issue microsoft/TypeScript#33611](https://github.com/microsoft/TypeScript/issues/33611) (Open, `Needs Investigation`, **rbuckton**)

**TS3\.6 regression: Map constructor overloads**

*TypeScript 3.7 regression breaks Map constructor overload resolution when using spread entries mixed with new tuples.*

 * created by **mprobst**
 * (7 years ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **rbuckton**
 * [later](https://github.com/microsoft/TypeScript/issues/33611#issuecomment-5888769796) **tbknl** suggested a more generic type for MapConstructor::new to allow heterogeneous entries, provided example code, and offered to supply proof if the approach is deemed plausible

### [Issue microsoft/TypeScript#51329](https://github.com/microsoft/TypeScript/issues/51329) (Closed, `Suggestion`, `Awaiting More Feedback`)

**Allow to emit sourcemaps when printing ast**

*Add a printFileWithSourceMaps method to the TypeScript printer API to emit both generated code and source maps when printing AST.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/51329#issuecomment-1481783109) **tmcw** requested sourcemap support for printFile or emitted information to build sourcemaps
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/51329#issuecomment-2197859814) **maxpatiiuk** shared undocumented TypeScript source map generation code, explained why program.emit and transpileModule were unsuitable for a Vite plugin, and requested a public API
 * (today) **goloveychuk** closed the issue

### [Issue microsoft/TypeScript#62180](https://github.com/microsoft/TypeScript/issues/62180) (Closed, `Help Wanted`, `Domain: Mapped Types`, `Possible Improvement`, **ahejlsberg**)

**Confusing missing property error in a circular situation**

*TypeScript reports confusing missing property error in circular mapped types when mixing optional and required Zod schemas.*

 * **RyanCavanaugh** added label `Domain: Mapped Types`
 * **ahejlsberg** assigned to **ahejlsberg**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62180#issuecomment-5733698384) **ahejlsberg** described that resolveObjectTypeMembers first resolved declared members then incrementally added inherited members, noted that missing members could be observed during base class resolution, and mentioned that enforcing idempotent resolution would break some cases
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#63271](https://github.com/microsoft/TypeScript/issues/63271) (Closed, `Bug`, `Domain: Crashes`)

**Crash: RangeError: Invalid string length in addSpans during instantiation of recursive template literal types**

*TypeScript crashes with a RangeError due to exponential string growth in deeply recursive template literal type instantiation*

 * (27 weeks ago) **RyanCavanaugh** added labels `Bug`, `Domain: Crashes`, and set milestone to `Backlog`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#63704](https://github.com/microsoft/TypeScript/issues/63704) (Closed, `Suggestion`, `Committed`, `Domain: lib.d.ts`, `ES Next`, **DanielRosenwasser**)

**Add \`es2026\` as valid \`target\` and \`lib\`**

*Add es2026 support with Math.sumPrecise, Iterator.concat, JSON.rawJSON and stringify overloads, Error.isError, default-valued Map/WeakMap methods, Uint8Array hex/base64 methods, and Array.fromAsync.*

 * (1 month ago) **DanielRosenwasser** set milestone to `TypeScript 7.1.0 Beta`, and assigned to **DanielRosenwasser**
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63704#issuecomment-5458880393) **DanielRosenwasser** said "Updated list since we already have Array.fromAsync."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#64093](https://github.com/microsoft/TypeScript/pull/64093) (Open, `For Milestone Bug`)

**feat: add Promise\.allKeyed and Promise\.allSettledKeyed to esnext**

*Add Promise.allKeyed and Promise.allSettledKeyed methods to the ESNext Promise API.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64093#issuecomment-5876580113) **DanielRosenwasser** said "After the merge conflicts we can get it in. Thanks for the patience here!"
 * [today](https://github.com/microsoft/TypeScript/pull/64093#issuecomment-5877090080) **a-tarasyuk** said "@DanielRosenwasser I've resolved conflicts"

### [PR microsoft/TypeScript#64096](https://github.com/microsoft/TypeScript/pull/64096) (Closed, `For Milestone Bug`, **DanielRosenwasser**)

**feat: add es2026 as a valid target and lib**

*Add ES2026 as a recognized compilation target and library option in TypeScript.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-5823200282) **typescript-automation[bot]** reported test results against main and PR merge showing infrastructure failures and a lodash type error
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-5823632574) **typescript-automation[bot]** reported that running the top 400 repos with tsc comparing main and the pull request merge produced no issues
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-5827319061) **typescript-automation[bot]** notified that DT tests results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-5874852728) **DanielRosenwasser** expressed happiness about lib tests and noted baseline merge conflicts
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#64194](https://github.com/microsoft/TypeScript/pull/64194) (Closed, `For Backlog Bug`)

**fix\(checker\): cap template literal type size to avoid unbounded growth**

*Cap template literal type size with character and placeholder limits to prevent infinite type instantiation and memory exhaustion.*

 * created by **ekalinin**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64257](https://github.com/microsoft/TypeScript/pull/64257) (Open, `For Backlog Bug`)

**Fix non\-null discriminant narrowing consistency**

*Fix discriminant narrowing inconsistency between small and large nullable unions by retaining null and undefined constituents in optimized paths.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-5657958944) **z0rimo** agreed with microsoft-github-policy-service
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-5662956364) **z0rimo** addressed both #62511 and #64260 by reworking mutation analysis around invocation sites and adding tests for union-size inconsistency and stale-fact cases
 * [today](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-5883585069) **z0rimo** reworked the fix based on feedback and asked for another review

### [Issue microsoft/TypeScript#64262](https://github.com/microsoft/TypeScript/issues/64262) (Open, `Bug`, `Domain: tsc -b`, **jakebailey**)

**Port \`DirWatchSet\` over to TS7**

*Cherry-pick commit e05860d9328a894189b49d9c43fb8a52e6c6d5a2 implementing DirWatchSet into a new 7.0.x branch of the TypeScript repository.*

 * (2 weeks ago) **DanielRosenwasser** added labels `Bug`, `Domain: tsc -b`, and assigned to **jakebailey**
 * [later](https://github.com/microsoft/TypeScript/issues/64262#issuecomment-5891481987) **Emut** expressed satisfaction with the nightly version and asked whether a 7.0.3 release will be available or if they should wait for 7.1.0
 * [later](https://github.com/microsoft/TypeScript/issues/64262#issuecomment-5891943211) **CSenshi** expressed support for including the fix in version 7.0.3 and noted that TypeScript compilation is slow in large repositories

### [Issue microsoft/TypeScript#64312](https://github.com/microsoft/TypeScript/issues/64312) (Open, `Bug`, `Needs Proposal`)

**\`checkJs\` skips \`\.mjs\`/\`\.cjs\` beside a \`\.d\.mts\`/\`\.d\.cts\`, but not \`\.js\` beside a \`\.d\.ts\`**

*TypeScript’s checkJs mode skips .mjs and .cjs files beside .d.mts/.d.cts declarations but not .js beside .d.ts*

 * (5 days ago) **RyanCavanaugh** added labels `Bug`, `Needs Proposal`
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64312#issuecomment-5814473949) **sbrilenko** identified that the wildcard include discovery logic only special-cased .d.ts/.js(x) duplicates, causing .d.ts/.mjs and .d.ts/.cjs files to be incorrectly excluded
 * [later](https://github.com/microsoft/TypeScript/issues/64312#issuecomment-5889551053) **hardikkaurani** said "This issue is being addressed by #64527."

### [PR microsoft/TypeScript#64372](https://github.com/microsoft/TypeScript/pull/64372) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Restore idempotency to \`resolveObjectTypeMembers\`**

*Reestablish idempotent resolveObjectTypeMembers by blocking eager base class type argument resolution and improving circular type instantiation errors.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5785661549) **typescript-automation[bot]** reported that the test top1000 job had started with status and results links
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5787027455) **typescript-automation[bot]** reported automated build comparison results across the top 1000 repos and noted an interesting change
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5804602336) **ahejlsberg** identified two circular-reference breakages in zod and postcss-selector-parser and proposed code changes to fix the type declarations
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64394](https://github.com/microsoft/TypeScript/issues/64394) (Closed, `API Request`, **andrewbranch**)

**\# \[API\] \`getJSDocCommentsAndTags\` is no longer exposed**

*TS7 removed getJSDocCommentsAndTags, so the API needs an equivalent that returns full JSDoc nodes including descriptions and tags*

 * **RyanCavanaugh** added label `API Request`
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64394#issuecomment-5784854686) **andrewbranch** clarified JSDoc API guidelines with three cases for exposing or omitting functionality
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/64394#issuecomment-5795022573) **dragomirtitian** suggested exposing getJSDocCommentsAndTags in the new API to match the old implementation and address JSDoc tag standardization
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64413](https://github.com/microsoft/TypeScript/pull/64413) (Closed, `For Backlog Bug`)

**Defer constraint checks on inferred type arguments that mention an unresolved accessor**

*Eager constraint checking of inferred Zod type arguments referencing unresolved accessors triggers TS7023 recursion errors.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64413#issuecomment-5804517605) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (4 days ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64413#issuecomment-5892954046) **colinhacks** said "Superseded by #64481. The only thing this still changed on top of main was the return type constraint leak, which is now #64530."
 * (later) **colinhacks** closed the issue

### [Issue microsoft/TypeScript#64415](https://github.com/microsoft/TypeScript/issues/64415) (Closed, `Possible Improvement`)

**Constraint check resolves an un\-annotated accessor while its object literal is still being inferred**

*Constraint checking in TypeScript prematurely resolves an unannotated accessor while its object literal type is still being inferred.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64415#issuecomment-5824032707) **colinhacks** explained that removing `this` from the base cleared the small repro but not the library because ZodType and each classic schema interface redeclare “~standard” through a subtype which resolves during the check, and provided a detailed repro closer to the library
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64415#issuecomment-5824083540) **ahejlsberg** explained why the “~standard” property caused an issue and proposed heuristics to avoid unnecessary member resolution in intersection reduction checks
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64415#issuecomment-5834499211) **colinhacks** said "Thanks Anders!"
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64419](https://github.com/microsoft/TypeScript/pull/64419) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Prevent nil dereference during package export resolution**

*Package export/import resolution treats absent tables as empty to avoid nil dereferences during program construction.*

 * **Copilot** assigned to **DanielRosenwasser**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64419#issuecomment-5823308975) **DanielRosenwasser** said "@copilot you need a realistic test case that is not just a unit test"
 * [today](https://github.com/microsoft/TypeScript/pull/64419#issuecomment-5876778666) **Copilot** replaced the synthetic resolver test with a compiler test using normal package.json exports resolution and removed the cache-injection unit test

### [Issue microsoft/TypeScript#64420](https://github.com/microsoft/TypeScript/issues/64420) (Open, `Possible Improvement`)

**Recursive schema through a call\-wrapped callback property \(\`lazy\(\(\) =\> Self\)\`\) still infers \`any\` after \#64311**

*Wrapping a recursive schema callback in lazy(() => Self) still triggers implicit any inference, breaking Zod-style recursion despite #64311.*

 * created by **ethndotsh**
 * [later](https://github.com/microsoft/TypeScript/issues/64420#issuecomment-5892958219) **colinhacks** noted that z.lazy supports recursive schemas, described the callback-style API pattern for recursion, and mentioned that PR #64426 fixes it in the published zod package

### [Issue microsoft/TypeScript#64430](https://github.com/microsoft/TypeScript/issues/64430) (Open, `Needs Investigation`)

**Declarations in \`declare global\` can have \`export\` modifiers**

*TypeScript permits export modifiers on declarations inside declare global blocks, prompting questions about whether this behavior is intentional.*

 * created by **DanielRosenwasser**
 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/64430#issuecomment-5884674395) **yksr-melt** explained that export inside declare global isn't an error and described two cases where it matters

### [Issue microsoft/TypeScript#64433](https://github.com/microsoft/TypeScript/issues/64433) (Closed, `Bug`, `Help Wanted`)

**empty mappings in \.d\.ts\.map for export default of a non\-identifier expression**

*Exporting an anonymous object literal as default in TypeScript 7.0 yields empty .d.ts.map mappings, unlike previous versions or named exports.*

 * (3 days ago) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/64433#issuecomment-5878304962) **vladyslav005** said "hello, i would like to contribute to this, if it's available"

### [Issue microsoft/TypeScript#64435](https://github.com/microsoft/TypeScript/issues/64435) (Closed, `Bug`, **weswigham**)

**Declaration emit: expando alias assignment \(\`F\.x = someIdentifier\`\) un\-exports the other expando members in the generated namespace**

*tsgo emits alias assignments in namespaces as export declarations, which inadvertently un-exports other expando members in the generated .d.ts file.*

 * (3 days ago) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/issues/64435#issuecomment-5884506321) **yksr-melt** offered a fix and test applying retroactive export modifier logic to alias branches and asked whether a PR would be welcome

### [PR microsoft/TypeScript#64451](https://github.com/microsoft/TypeScript/pull/64451) (Open, `For Uncommitted Bug`)

**ES\-conformant symbol typing**

*Add ES-standard symbol typing support in TypeScript by introducing a RegisteredSymbol intrinsic, deferred registry keys, and preserved unique symbol types.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64451#issuecomment-5838892634) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64451#issuecomment-5839205369) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #27524. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [today](https://github.com/microsoft/TypeScript/pull/64451#issuecomment-5875128111) **michaelfig** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64454](https://github.com/microsoft/TypeScript/pull/64454) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Replace vscode l10n\-dev with local localization generator**

*Replace @vscode/l10n-dev with lighter in-repo tooling for string extraction and pseudo-localization, removing 85 dependencies and an npm warning*

 * (3 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64455](https://github.com/microsoft/TypeScript/pull/64455) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**Add getJSDocCommentsAndTags back with functionality of 6\.0**

*Reintroduce getJSDocCommentsAndTags with its full TypeScript 6.0 functionality.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64455#issuecomment-5840244978) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64460](https://github.com/microsoft/TypeScript/pull/64460) (Closed, `For Backlog Bug`)

**Fix declaration maps for export assignment expressions**

*Assign original source-map ranges to synthesized export default and export= statements in declaration maps to restore missing mappings.*

 * created by **maricastroc**
 * (3 days ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64460#issuecomment-5881553205) **maricastroc** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64463](https://github.com/microsoft/TypeScript/issues/64463) (Open)

**\[LSP\] Memory of configured projects is never released, even after didClose of all files — ~70 MB retained per project \(7\.0\.2 and 7\.1\.0\-dev\.20260926\.1\)**

*TypeScript LSP never frees memory for closed projects, retaining about 70MB per project and causing memory bloat.*

 * created by **talkstream**
 * [today](https://github.com/microsoft/TypeScript/issues/64463#issuecomment-5865093315) **jakebailey** said "If you're using VS Code, we have pprof commands to take profiles, but in this case you actually would need to build from source and then use goref or something to find the leak."
 * [today](https://github.com/microsoft/TypeScript/issues/64463#issuecomment-5865101761) **jakebailey** said "Possibly https://github.com/microsoft/TypeScript/pull/64466 resolves this, though?"
 * [today](https://github.com/microsoft/TypeScript/issues/64463#issuecomment-5873826780) **jakebailey** explained that the test verifies longstanding behavior of not closing the project on file close to avoid reloads and asked if the same was tried on TS 6.0

### [Issue microsoft/TypeScript#64464](https://github.com/microsoft/TypeScript/issues/64464) (Open, `Needs Investigation`, **johnfav03**)

**First incremental rebuild after a clean build is up to 75× slower than a full check**

*First incremental rebuild after a clean build can be up to 75× slower than a full type check in TypeScript*

 * created by **resure**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**

### [PR microsoft/TypeScript#64466](https://github.com/microsoft/TypeScript/pull/64466) (Closed, `For Uncommitted Bug`)

**Fix language server retaining pre\-edit program and its checkers after program clone**

*Prevent TypeScript language server cloned programs from retaining previous program checker pools to reduce memory leaks.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64466#issuecomment-5846290311) **ghost2023** said "@microsoft-github-policy-service agree"
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64466#issuecomment-5850307599) **jakebailey** said "I think there's actually another one of these in ReuseProgram via processedFiles."
 * [today](https://github.com/microsoft/TypeScript/pull/64466#issuecomment-5880715981) **jakebailey** said "I think this PR is in itself fine, but I'm going to try and put together a very invasive version which prevents us from making this mistake in the future."

### [PR microsoft/TypeScript#64470](https://github.com/microsoft/TypeScript/pull/64470) (Closed, `For Uncommitted Bug`)

**Fixed a crash on JSX emit trying to emit unexpectedly recovered \`BinaryExpression\` in a JSX attribute**

*Fixed crash during JSX emission when an unexpectedly recovered binary expression appears in a JSX attribute.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64470#issuecomment-5848348825) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64470#issuecomment-5880223541) **jakebailey** invoked the TypeScript bot to run user tests and top1000 tests
 * [today](https://github.com/microsoft/TypeScript/pull/64470#issuecomment-5880224774) **typescript-automation[bot]** reported automated build status updates for `user test this` and `test top1000` jobs
 * [today](https://github.com/microsoft/TypeScript/pull/64470#issuecomment-5880593724) **typescript-automation[bot]** reported that user tests comparing main and the pull request passed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/64470#issuecomment-5881504034) **typescript-automation[bot]** reported successful tsc test results comparing main and pull request merge across the top 1000 repositories
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64471](https://github.com/microsoft/TypeScript/pull/64471) (Closed, `For Uncommitted Bug`)

**Fix crash in \`isolatedDeclarations\` on \`this\.x = …\` assignments**

*Fix a crash in the isolatedDeclarations stage caused by this.x assignment expressions.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64471#issuecomment-5848471053) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64474](https://github.com/microsoft/TypeScript/issues/64474) (Closed, `Suggestion`, `Domain: Performance`, **ahejlsberg**)

**checker builds member tables and intersection props it never uses**

*The TypeScript checker’s eager member and intersection property instantiation causes high memory use and is optimized to build needed properties.*

 * created by **maschwenk**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64474#issuecomment-5852758422) **maschwenk** described the benchmarking methodology and results comparing main and PR commits, including hardware specifications, commands, scenarios, replication details, performance and memory improvements, and a gist link
 * **ahejlsberg** assigned to **ahejlsberg**
 * (today) **DanielRosenwasser** added labels `Suggestion`, `Domain: Performance`, and set milestone to `TypeScript 7.1.0 Beta`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64475](https://github.com/microsoft/TypeScript/pull/64475) (Open, `For Uncommitted Bug`, **ahejlsberg**)

**build member tables of instantiated classes/interfaces lazily**

*Implement lazy construction of class and interface member tables to avoid unneeded instantiations and improve performance and memory usage.*

 * created by **maschwenk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64475#issuecomment-5875331276) **ahejlsberg** expressed support for landing PR #64499, suggested evaluating additional savings afterward, and noted concern about adding ~500 lines to member resolution
 * (today) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, removed labels `For Uncommitted Bug`, `For Milestone Bug`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/pull/64475#issuecomment-5885611567) **maschwenk** thanked the maintainer for landing the PR and reported code size reductions and performance improvements across various projects, noted non-determinism in the never-reduction check and submitted a fix via PR #64521

### [PR microsoft/TypeScript#64476](https://github.com/microsoft/TypeScript/pull/64476) (Closed, `For Milestone Bug`, **ahejlsberg**)

**only build intersection props that can reduce it to never**

*Modify TypeScript’s intersection type reduction to skip creating properties that cannot reduce to never, reducing memory and improving performance.*

 * created by **maschwenk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64476#issuecomment-5875220163) **ahejlsberg** said "@maschwenk I have a simpler implementation in #64499 with equally nice results. Thanks much for the research!"
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64476#issuecomment-5878048790) **maschwenk** said "@ahejlsberg shall I close this out?"
 * [today](https://github.com/microsoft/TypeScript/pull/64476#issuecomment-5878420125) **ahejlsberg** confirmed that #64499 was already in main
 * (today) **maschwenk** closed the issue

### [PR microsoft/TypeScript#64481](https://github.com/microsoft/TypeScript/pull/64481) (Closed, `Author: Team`, `For Backlog Bug`, **ahejlsberg**)

**Don't reduce intersections of mappings of the same object type**

*Prevent TypeScript from reducing intersections of homomorphic object mappings to enable recursive Zod schemas*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5857701525) **typescript-automation[bot]** notified that DT tests results were ready and unchanged
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5857806432) **ahejlsberg** said "Apparently this pattern accounts for a substantial number of types in mui-docs, so nice savings there."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5857997842) **typescript-automation[bot]** ran tests on the top 400 repos and reported everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5875543153) **jakebailey** requested the typescript-bot to run the top1000 tests
 * [today](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5875544872) **typescript-automation[bot]** updated the comment with CI job start and result links for test top1000
 * [today](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5877376386) **typescript-automation[bot]** reported that tsc runs on the top 1000 repos comparing main and the pull request merge passed without issues
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64483](https://github.com/microsoft/TypeScript/issues/64483) (Open, `Needs Investigation`, **andrewbranch**)

**\`getChildren\(\)\` includes synthetic NodeObjects, that can't easily be discerned from RemoteNodes**

*getChildren() now returns synthetic NodeObjects indistinguishable from RemoteNodes, causing getNodeId to error without a RemoteNode typeguard*

 * created by **Qjuh**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64484](https://github.com/microsoft/TypeScript/issues/64484) (Closed)

**Unused locals in class static block declarations are not reported**

*TypeScript fails to report unused local variables declared in class static blocks when noUnusedLocals is enabled.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64485](https://github.com/microsoft/TypeScript/pull/64485) (Closed, `For Uncommitted Bug`)

**Report unused locals in class static blocks**

*Add support for detecting and reporting unused local variables declared inside class static blocks.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64485#issuecomment-5858665378) **jakebailey** said "@typescript-bot test top1000"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64485#issuecomment-5858666039) **typescript-automation[bot]** reported that the test top1000 job started and provided status and result links
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64485#issuecomment-5859682405) **typescript-automation[bot]** provided tsc comparison results for the top 1000 repos and confirmed that everything looked good
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64492](https://github.com/microsoft/TypeScript/issues/64492) (Closed)

**External directory from tsconfig \`files\` gets no watcher in LSP**

*The TypeScript LSP fails to add file watchers for external directories specified in tsconfig.json’s files array.*

 * created by **auvred**
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64493](https://github.com/microsoft/TypeScript/pull/64493) (Closed, `For Uncommitted Bug`)

**Don't let \`append\` overwrite sibling results in \`tspath\.GetCommonParents\`**

*tspath.GetCommonParents' use of append on subslices with leftover capacity causes sibling results to overwrite each other.*

 * created by **auvred**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64494](https://github.com/microsoft/TypeScript/issues/64494) (Open, `Bug`, **weswigham**)

**Decorated class gets \`name === "\_a"\` when a \`\#private\` field initializer references the class \(regression in 7\.0\)**

*Decorated classes with private field initializers referencing the class incorrectly get named `_a` instead of their declared name.*

 * created by **bagbag**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64499](https://github.com/microsoft/TypeScript/pull/64499) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Only check properties with multiple declarations for never\-reduction**

*Optimize getReducedType by limiting never-type reduction checks to properties declared in multiple intersection constituents.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64499#issuecomment-5873312085) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64499#issuecomment-5873314200) **typescript-automation[bot]** reported build job statuses for `test top400`, `user test this`, `run dt`, and `perf test this faster`
 * [today](https://github.com/microsoft/TypeScript/pull/64499#issuecomment-5873791787) **typescript-automation[bot]** posted requested perf run results
 * [today](https://github.com/microsoft/TypeScript/pull/64499#issuecomment-5873900673) **typescript-automation[bot]** ran user tests with tsc comparing main and the PR merge, reported one git clone failure and one package install failure, and said everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64499#issuecomment-5874059872) **typescript-automation[bot]** reported that the DT test run failed and provided a link to the build log
 * [today](https://github.com/microsoft/TypeScript/pull/64499#issuecomment-5874662475) **typescript-automation[bot]** reported that running the top 400 repos with tsc comparing main and the PR merge yielded no issues
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64501](https://github.com/microsoft/TypeScript/pull/64501) (Open, `For Backlog Bug`)

**Improve error when break/continue label is in the same function but not enclosing**

*Modify the break/continue checker to report non-enclosing same-function labels instead of misreporting a crossed-function-boundary error.*

 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64501#issuecomment-5873511947) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64501#issuecomment-5890901769) **britsync07-prog** said "@microsoft-github-policy-service agree"
 * (later) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64501#issuecomment-5891101326) **britsync07-prog** addressed both findings by caching label sets per function, adding breakTargetSameFunctionLabel, signing the CLA, and confirming tests passed with unchanged baselines

### [PR microsoft/TypeScript#64502](https://github.com/microsoft/TypeScript/pull/64502) (Open, `For Backlog Bug`)

**Fix false circularity for static fields in generic class expressions**

*Avoid treating contextual property lookups as circular in generic class expressions, preventing incorrect TS7022 on static fields.*

 * created by **Fugu0141**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64502#issuecomment-5874708002) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`, and removed labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64502#issuecomment-5874793429) **Fugu0141** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/64502#issuecomment-5887522333) **Andarist** reopened a prior PR to TS 6.0 with a simpler fix and suggested using another test case to advocate for the current approach
 * [later](https://github.com/microsoft/TypeScript/pull/64502#issuecomment-5887759684) **Fugu0141** acknowledged that issue #64525 was more targeted and offered to close the change in its favor unless maintainers preferred the broader approach

### [PR microsoft/TypeScript#64503](https://github.com/microsoft/TypeScript/pull/64503) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Fix AST generation of diamond inheritance and add missing DeclarationBase extends**

*Correct AST generation for diamond inheritance patterns and add a missing DeclarationBase extension*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64504](https://github.com/microsoft/TypeScript/pull/64504) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid npm bin relinking during extension version bump**

*Work around npm version’s unintended relinking of node_modules/.bin/tsc to the workspace binary during extension version bumps.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64505](https://github.com/microsoft/TypeScript/pull/64505) (Open, `For Uncommitted Bug`, **weswigham**)

**fix\(64494\): fix decorated class names with private member self\-references**

*Corrects decorated class naming to properly preserve private member self-references*

 * created by **a-tarasyuk**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64505#issuecomment-5874738643) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** assigned to **weswigham**

### [PR microsoft/TypeScript#64506](https://github.com/microsoft/TypeScript/pull/64506) (Closed, `For Backlog Bug`)

**fix: heavy root\-cause refactor for \#62294 and \#63814 \- non\-dismissible with technical facts**

*A refactor adding pre-generic-deferral private property conflict checks and export-equals symbol accessibility handling to resolve TypeScript issues #62294 and #63814.*

 * created by **hesam-oxe**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64506#issuecomment-5875631324) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64507](https://github.com/microsoft/TypeScript/pull/64507) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Restore OneLoc LCL files for localization onboarding**

*Restore OneLoc LCL files to facilitate localization team onboarding, with plans to delete them later.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64508](https://github.com/microsoft/TypeScript/pull/64508) (Closed, `For Backlog Bug`)

**fix\(heavy\-refactor\): root cause fixes for \#62294 and \#63814 with undeniable technical facts**

*Heavy refactor corrects generic intersection deferral logic to properly error on private property conflicts.*

 * created by **hesam-oxe**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64508#issuecomment-5875785919) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64509](https://github.com/microsoft/TypeScript/pull/64509) (Closed, `For Backlog Bug`)

**fix\(checker\): root cause fix for conflicting private properties in generic indexed access \(\#62294\) \- HEAVY REFACTOR**

*Introduce a reusable conflict-check helper and early checks to ensure generic indexed access fails for classes with conflicting private properties.*

 * created by **hesam-oxe**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64510](https://github.com/microsoft/TypeScript/pull/64510) (Closed, `For Uncommitted Bug`)

**fix\(checker\): root cause fix for export= module augmentation visibility \(\#63814\) \- HEAVY REFACTOR**

*Refactor the TypeScript checker to correctly handle visibility of export= module augmentations, fixing TS4060 errors.*

 * created by **hesam-oxe**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64511](https://github.com/microsoft/TypeScript/issues/64511) (Open, `Bug`, `Infrastructure`, **DanielRosenwasser**, **Copilot**)

**Remove ts\-expect\-error comments from \`promiseTry\.ts\`**

*Remove ts-expect-error comments from promiseTry.ts and tests that do not specifically illustrate error suppression.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Bug`, `Infrastructure`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript#64512](https://github.com/microsoft/TypeScript/pull/64512) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Remove Promise\.try error suppression directives**

*Remove @ts-expect-error directives in promiseTry.ts and update diagnostics and baselines for invalid Promise.try arities*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64513](https://github.com/microsoft/TypeScript/pull/64513) (Closed, `For Uncommitted Bug`)

**Don't let parallel per\-file workers reuse their request's checker**

*Remove request IDs from parallel file worker contexts to prevent unsafe concurrent reuse of the TypeScript checker.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64513#issuecomment-5876854815) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64514](https://github.com/microsoft/TypeScript/pull/64514) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Cache Go modules in CI**

*Re-add Go module caching in CI workflows to reduce flaky failures from the unreliable Go module proxy*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64515](https://github.com/microsoft/TypeScript/pull/64515) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Define Extract and Exclude in terms of intersections and negations**

*Defines Extract and Exclude as intersections with negation instead of conditional types, causing Extract<T, any> to yield any rather than T.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64517](https://github.com/microsoft/TypeScript/pull/64517) (Closed, `For Uncommitted Bug`)

**Bump vscode\-typescript to 1\.0\.0**

*Bump the vscode-typescript extension to version 1.0.0*

 * created by **typescript-automation[bot]**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64518](https://github.com/microsoft/TypeScript/pull/64518) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Make binder\-produced symbols owned by SourceFiles in the client, like the server and 6\.0**

*Cache binder-produced symbols in client SourceFiles to maintain symbol identity across snapshots and enable context-independent symbol retrieval.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64519](https://github.com/microsoft/TypeScript/pull/64519) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Better manage Program options lifetimes**

*Refactor ProgramOptions into separate Config, Hosts, and Factories components to properly manage lifetimes and prevent stale state.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#64520](https://github.com/microsoft/TypeScript/issues/64520) (Closed, `Bug`)

**TS2565 false positive in JS for a class field initialized in the base class**

*With allowJs and checkJs enabled, TypeScript incorrectly reports TS2565 for subclass fields initialized in their base class.*

 * created by **harshmandan**
 * [later](https://github.com/microsoft/TypeScript/issues/64520#issuecomment-5887375975) **jwbth** mentioned that assigning the base property in the constructor rather than as a class field likewise triggered TS2565 and noted that destructuring (const { element }= this) avoids it

### [PR microsoft/TypeScript#64521](https://github.com/microsoft/TypeScript/pull/64521) (Closed, `For Uncommitted Bug`)

**check intersection props for never\-reduction in a stable order**

*Change the intersection property reduction to use an OrderedMap for stable ordering, eliminating run-to-run symbol count variability.*

 * created by **maschwenk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64521#issuecomment-5892140205) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64522](https://github.com/microsoft/TypeScript/pull/64522) (Closed, `For Uncommitted Bug`)

**Fix moduleResolution \-\> customConditions test to actually apply both conditions**

*CustomConditions test in moduleResolution fails to trim whitespace on comma-separated values, resulting in only the first condition applying.*

 * created by **auvred**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64522#issuecomment-5886317751) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64523](https://github.com/microsoft/TypeScript/pull/64523) (Closed, `For Backlog Bug`)

**Fix regression reporting TS2565 for inherited class fields reassigned in JS**

*TypeScript regression incorrectly reports TS2565 errors for inherited class fields reassigned in JavaScript.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64524](https://github.com/microsoft/TypeScript/issues/64524) (Open, `Bug`, **gabritto**)

**JSDoc \`@override\` on an \`@overload\` signature is ignored under \`noImplicitOverride\` \(TS4119\)**

*In TypeScript 7.x, JSDoc @override on overload signatures is ignored under noImplicitOverride, causing TS4119 errors.*

 * created by **jwbth**

### [PR microsoft/TypeScript#64525](https://github.com/microsoft/TypeScript/pull/64525) (Closed, `For Backlog Bug`)

**Avoid contextually typing static properties by their own class to prevent spurious circularities**

*Modify TypeScript’s type checker to prevent contextually typing a class’s static properties with the class itself, avoiding spurious circularities.*

 * created by **Andarist**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5887494388) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64526](https://github.com/microsoft/TypeScript/pull/64526) (Open, `For Uncommitted Bug`)

**build members of keyof mapped types lazily**

*Implement lazy member tables for keyof mapped types to defer property symbol creation and enhance performance*

 * created by **maschwenk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64527](https://github.com/microsoft/TypeScript/pull/64527) (Open, `For Uncommitted Bug`)

**Fix checkJs behavior for \.mjs and \.cjs files next to declarations**

*Remove legacy wildcard exception to ensure wildcard include consistently prefers declaration files over .js, .mjs, and .cjs implementations.*

 * created by **hardikkaurani**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5889090694) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5891462911) **hkleungai** said "Looks like this PR has a chance to resolve https://github.com/microsoft/TypeScript/issues/63523 too. 😀 "
 * [later](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5891856716) **hardikkaurani** acknowledged the fix for issue #63523, linked the PR to issue #64312 for consistent .mjs/.d.mts and .cjs/.d.cts behavior, and invited feedback
 * [later](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5893125311) **jakebailey** said "No tests?"

### [PR microsoft/TypeScript#64528](https://github.com/microsoft/TypeScript/pull/64528) (Open, `For Uncommitted Bug`)

**Skip combined\-constraint check while measuring variances to avoid unbounded chase**

*Skip combined-constraint checks during variance measurement to prevent infinite type chase and memory exhaustion in TypeScript 7.*

 * created by **Amatewasu**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64528#issuecomment-5892189219) **Amatewasu** verified the fix against a private React 19+R3F+TSX project, reported memory and time benchmarks for unpatched TS7, patched TS7, and TS6, and noted diagnostics parity and caveats

### [Issue microsoft/TypeScript#64529](https://github.com/microsoft/TypeScript/issues/64529) (Closed, `Needs Investigation`, **ahejlsberg**)

**Type parameter escapes its constraint in a recursive call resolution**

*Recursive resolution of object calls leaks the type parameter P outside its constraint, causing incorrect inference.*

 * created by **colinhacks**

### [PR microsoft/TypeScript#64530](https://github.com/microsoft/TypeScript/pull/64530) (Closed, `For Uncommitted Bug`, **ahejlsberg**)

**Keep a pure return type inference filtered by its constraint in a recursive call resolution**

*Restore constraint filtering for pure return type inferences during recursive call resolution to prevent invalid type arguments*

 * created by **colinhacks**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64530#issuecomment-5892953821) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64531](https://github.com/microsoft/TypeScript/issues/64531) (Open, `Possible Improvement`)

**Support spread in recursive object inference**

*TypeScript does not correctly infer recursive object schema types when a base shape is spread, resulting in any types instead of the intended schema.*

 * created by **colinhacks**

### [Issue microsoft/TypeScript#64532](https://github.com/microsoft/TypeScript/issues/64532) (Open, `Needs Investigation`, **andrewbranch**)

**\[API\] \`getImmediateAliasedSymbol\` returns a different symbol than classic \`tsc\`**

*getImmediateAliasedSymbol for namespace imports in TypeScript 7 returns a cloned symbol instead of the original file symbol when a module has a default export.*

 * created by **dragomirtitian**

