# Report for 2026-09-29 (Tuesday, September 29th, 2026)

27 different users commented on 88 different issues.

## Recommended Actions

 * Response Recommended
    * @futursolo asked about supporting the Node.js loader API in [microsoft/TypeScript#63919](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5908981564)
    * @SiddhantShedge45 offered to work on the issue in [microsoft/TypeScript#64438](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-5911162732)
    * @SHULMIT volunteered to work on the issue in [microsoft/TypeScript#64497](https://github.com/microsoft/TypeScript/issues/64497#issuecomment-5895021858)
    * @hardikkaurani asked whether removing the legacy .js/.d.ts exception is the intended direction before updating the implementation and tests in [microsoft/TypeScript#64527](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5895552152)
    * @hardikkaurani requested maintainer direction on the legacy exception compatibility question in [microsoft/TypeScript#64527](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5896734927)
    * @hardikkaurani asked how include should consistently resolve various file extensions in [microsoft/TypeScript#64527](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5901269687)
    * @hardikkaurani asked if maintainers would proceed with the current approach to extend companion declaration behavior to .mjs and .cjs files in [microsoft/TypeScript#64527](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5908105828)
    * @Fugu0141 asked whether treating missing and circularly-unavailable properties identically was intentional in [microsoft/TypeScript#64534](https://github.com/microsoft/TypeScript/issues/64534#issuecomment-5901290050)
    * @leonidaz asked to close this issue in favor of two new issues #64549 and #64548 in [microsoft/TypeScript#64546](https://github.com/microsoft/TypeScript/issues/64546#issuecomment-5901727760)
    * @aleclarson offered to share a resolution fixture for testing variant resolution in [microsoft/TypeScript#64549](https://github.com/microsoft/TypeScript/issues/64549#issuecomment-5912337356)

## Activity Summary

### [Issue microsoft/TypeScript#33611](https://github.com/microsoft/TypeScript/issues/33611) (Open, `Needs Investigation`, **rbuckton**)

**TS3\.6 regression: Map constructor overloads**

*TypeScript 3.7 regression breaks Map constructor overload resolution when using spread entries mixed with new tuples.*

 * (7 years ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **rbuckton**
 * [today](https://github.com/microsoft/TypeScript/issues/33611#issuecomment-5888769796) **tbknl** suggested a more generic type for MapConstructor::new to allow heterogeneous entries, provided example code, and offered to supply proof if the approach is deemed plausible
 * [later](https://github.com/microsoft/TypeScript/issues/33611#issuecomment-5906044926) **tbknl** cross-linked two TypeScript issues and suggested they could be solved with the proposed interface

### [Issue microsoft/TypeScript#51661](https://github.com/microsoft/TypeScript/issues/51661) (Closed, `Bug`, `Needs More Info`, `Help Wanted`, `Domain: This-Typing`)

**Type\-asserting function call on variable initialized using \`this\` causes false implicit\-any in VSCode**

*VSCode's TypeScript support falsely flags implicit-any when using a type-asserting function on a property accessed via untyped `this` in callbacks.*

 * (1 week ago) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`, and removed label `Needs Human Review`
 * [today](https://github.com/microsoft/TypeScript/issues/51661#issuecomment-5904970780) **OxleyS** said "I actually haven't run into this bug in a while, so it may have been inadvertently fixed at some point. I will close this for now, and re-open it if I run into it again."
 * (today) **OxleyS** closed the issue

### [Issue microsoft/TypeScript#62508](https://github.com/microsoft/TypeScript/issues/62508) (Open, `Discussion`)

**6\.0 Migration Guide**

*Placeholder issue for drafting and publishing the migration guide for version 6.0.*

 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4871588327) **andrewbranch** explained the distinctions between node10, bundler, and node16 module resolution algorithms and justified dropping node10 from TypeScript’s maintained algorithms
 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4871607338) **ljharb** argued that in latest node all code was CJS or ESM because they're indistinguishable; noted that testing multiple TypeScript versions was prohibitively hard due to TS 6 incompatibility; decided to use bundler; mentioned that resolve@next already models all node resolution permutations and has near-zero maintenance cost
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-5023031732) **xr0master** advised updating code instead of requesting libraries to support Node 10
 * [today](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-5905649338) **ljharb** said "@xr0master no, it's just not supported. even if it was actually dead (no usage), equivalent browsers are still VERY MUCH in use, and these browsers should be delivered type-checked code too."

### [PR microsoft/TypeScript#63730](https://github.com/microsoft/TypeScript/pull/63730) (Open, `For Backlog Bug`)

**fix\(lib\): rectify docs error for Array\.prototype\.at**

*Update Array.prototype.at TSDoc comment to replace the term 'code unit' with 'item' for the index parameter.*

 * (7 weeks ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/63730#issuecomment-5209708140) **grundb** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63730#issuecomment-5894900316) **RyanCavanaugh** said "@copilot resolve the merge conflicts in this pull request"

### [Issue microsoft/TypeScript#63761](https://github.com/microsoft/TypeScript/issues/63761) (Closed, `Bug`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Panic "Diagnostic emitted without context" ts\-go in declaration emit for \`export default\` arrow/function expression with non\-portable inferred return type**

*Native TypeScript compiler panics on declaration emit for default-exported arrow functions with non-portable inferred return types*

 * (5 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.1`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#63919](https://github.com/microsoft/TypeScript/pull/63919) (Open, `For Uncommitted Bug`)

**Add Yarn PnP module resolution support**

*Add native Yarn Plug’n’Play module resolution support to TypeScript Go, including PnP VFS, API, and manifest handling.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5471741188) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #63769. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5737540898) **louisscruz** asked what blocks the PR from merging and explained being blocked on upgrading to TypeScript 7 due to a related issue
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5868202880) **malyzeli** reported that their company required Yarn PnP due to a contractual obligation in the medical domain, preventing migration to TS7 without PnP
 * [today](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5898089808) **jakebailey** expressed reservations about the current PnP implementation’s design, its reliance on globals, unclear JS API integration, and uncertain ecosystem adoption
 * [today](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5901034425) **arcanis** explained that Node 26+ package maps could be seen as the standard successor to PnP, shipping since Node v26.4, supported by Yarn, pnpm, and soon Vite, and compatible with node_modules installs unlike PnP
 * [later](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5908981564) **futursolo** suggested supporting the Node.js loader API as a pathway to support PnP with smaller modifications and noted that package maps lack many PnP benefits

### [Issue microsoft/TypeScript#63966](https://github.com/microsoft/TypeScript/issues/63966) (Closed, `Possible Improvement`)

**Performance regression for declaration emit of an oversized inferred type**

*TypeScript 7’s declaration emit for nested inferred types now uses significantly more memory and time and still produces TS7056 errors*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63966#issuecomment-5391743046) **daniellockyer** explained that they found the repro via an LLM while improving memory usage of tsc/tsgo and noted they had other bugs tied to private projects for which they needed minimal public repros
 * (5 weeks ago) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#63969](https://github.com/microsoft/TypeScript/pull/63969) (Closed, `For Backlog Bug`)

**Avoid cloning cached declaration types after truncation**

*Prevent cloning of cached declaration type nodes after truncation threshold is reached, drastically improving compile performance.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/63969#issuecomment-5386818021) **butros10games** said "@microsoft-github-policy-service agree"
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/63969#issuecomment-5401140601) **butros10games** moved the truncation check to the start of visitAndTransformType, updated test expectations, and confirmed the full test suite passed
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#63989](https://github.com/microsoft/TypeScript/pull/63989) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix panic in declaration emit for \`export default\` arrow/function expression with unnameable inferred return type**

*Default-exported arrow or function expressions with unnameable inferred return types cause a compiler panic due to missing diagnostic context.*

 * **Copilot** assigned to **RyanCavanaugh**
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/63989#issuecomment-5401122264) **Copilot** implemented the change by moving the diagnostic context assignment and PushErrorFallbackNode above the unwrapped assignment, sharing them across all branches, and adding a PopErrorFallbackNode before each return
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64243](https://github.com/microsoft/TypeScript/pull/64243) (Closed, `For Uncommitted Bug`)

**fix: disallow NoSubstitutionTemplate in module import attribute types**

*Enforce rejecting empty template literals in module import attribute types by requiring quoted string literals.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5633219206) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5638319287) **DanielRosenwasser** appreciated test coverage and asked if there are tests for template string types with interpolations, requesting their addition if missing
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5647642629) **camc314** explained that requiring quoted string literals is better design due to spec distinctions and consistency; noted the downstream tool impact and that it can change since unreleased; added a test case for template string types with interpolations
 * [later](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5909635356) **camc314** pinged maintainers for clarity before the 7.1 beta to avoid blocking user adoption

### [PR microsoft/TypeScript#64366](https://github.com/microsoft/TypeScript/pull/64366) (Closed, `For Uncommitted Bug`, **johnfav03**)

**Watch projects and program files close to the filesystem root**

*tsc --watch and tsc -b --watch fail to rebuild projects in shallow root-level directories due to regression in directory watching.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64366#issuecomment-5801319830) **Generalsimus** implemented full 6.0 rule for program file watching in both tsc --watch and tsc -b --watch, updated description, added tests to verify correct shallow project watching, and validated behavior in Docker-based real build scenarios
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64366#issuecomment-5803161876) **jakebailey** asked to file an issue
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64366#issuecomment-5813130599) **Generalsimus** said "Filed #64424 for the tsc -b --watch one. I also opened #64425 for the regression this PR fixes, since the bot asked for a linked issue."
 * **typescript-automation[bot]** assigned to **johnfav03**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64412](https://github.com/microsoft/TypeScript/issues/64412) (Closed, `Won't Fix`)

**Crash in getLocalModuleSpecifier when formatting a type: normalizeSlashes receives undefined \(regression in 6\.0\)**

*TypeScript 6.0.3 regression crash in getLocalModuleSpecifier because normalizeSlashes gets undefined after ESLint fix-dry-run.*

 * created by **AlexisDevMaster**
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/64412#issuecomment-5826112137) **yksr-melt** identified the cause of a TypeError in getLocalModuleSpecifier due to an undefined base directory when imports resolution is enabled without paths or baseUrl, reproduced it in a unit test, and proposed a one-line fallback patch while asking if a PR against release-6.0 would be accepted
 * **RyanCavanaugh** added label `Won't Fix`
 * [today](https://github.com/microsoft/TypeScript/issues/64412#issuecomment-5894381304) **RyanCavanaugh** said "We're not patching the 6.0 API line except for critical security fixes, and it sounds like this is more likely a case of ESLint failing to set up a correct environment."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64420](https://github.com/microsoft/TypeScript/issues/64420) (Open, `Possible Improvement`)

**Recursive schema through a call\-wrapped callback property \(\`lazy\(\(\) =\> Self\)\`\) still infers \`any\` after \#64311**

*Wrapping a recursive schema callback in lazy(() => Self) still triggers implicit any inference, breaking Zod-style recursion despite #64311.*

 * created by **ethndotsh**
 * [today](https://github.com/microsoft/TypeScript/issues/64420#issuecomment-5892958219) **colinhacks** noted that z.lazy supports recursive schemas, described the callback-style API pattern for recursion, and mentioned that PR #64426 fixes it in the published zod package
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64421](https://github.com/microsoft/TypeScript/issues/64421) (Closed, `Bug`, **weswigham**)

**panic: unexpected Expression: KindArrayBindingPattern \[recovered, repanicked\]**

*TypeScript’s compiler unexpectedly panics with an unexpected KindArrayBindingPattern error when printing nested array destructuring using a spread element.*

 * (4 days ago) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64422](https://github.com/microsoft/TypeScript/pull/64422) (Closed, `For Milestone Bug`, **weswigham**)

**fix\(64421\): convert nested rest bindings to assignment targets**

*Convert nested rest bindings into valid assignment targets to correct destructuring behavior.*

 * (4 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Backlog Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64425](https://github.com/microsoft/TypeScript/issues/64425) (Closed, **johnfav03**)

**\`tsc \-\-watch\` doesn't pick up changes when the project is in a shallow folder like \`/app\`**

*TypeScript watch mode stops detecting changes in shallow project folders like /app after a new path-depth check introduced in v7*

 * created by **Generalsimus**
 * **RyanCavanaugh** assigned to **johnfav03**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64426](https://github.com/microsoft/TypeScript/pull/64426) (Open, `For Backlog Bug`)

**Type a recursive call\-initialized object literal property lazily**

*Enable object literal properties initialized by function calls to be typed lazily to handle recursive types.*

 * created by **ethndotsh**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64426#issuecomment-5817989945) **ethndotsh** said "@microsoft-github-policy-service agree"
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64432](https://github.com/microsoft/TypeScript/pull/64432) (Closed, `Author: Team`, `For Backlog Bug`, **jakebailey**, **johnfav03**)

**Fixes for recursive declarations, elided placeholders, cycles**

*Error on elided placeholders, detect deferred type cycles, and preserve recursive and reverse-mapped types during TypeScript declaration emit.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5829951254) **typescript-automation[bot]** reported that 144 of 147 projects failed to build with the old tsc and highlighted a cyclic type inference error in teableio/teable
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5836809889) **jakebailey** said "Thanks for the info. I guess more stuff to figure out."
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5839341604) **jakebailey** noted that after talking with @ahejlsberg he submitted #64452 instead and said he would split out other parts of the big PR
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64433](https://github.com/microsoft/TypeScript/issues/64433) (Closed, `Bug`, `Help Wanted`)

**empty mappings in \.d\.ts\.map for export default of a non\-identifier expression**

*Exporting an anonymous object literal as default in TypeScript 7.0 yields empty .d.ts.map mappings, unlike previous versions or named exports.*

 * (4 days ago) **RyanCavanaugh** added label `Help Wanted`, and set milestone to `Backlog`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64433#issuecomment-5878304962) **vladyslav005** said "hello, i would like to contribute to this, if it's available"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64435](https://github.com/microsoft/TypeScript/issues/64435) (Closed, `Bug`, **weswigham**)

**Declaration emit: expando alias assignment \(\`F\.x = someIdentifier\`\) un\-exports the other expando members in the generated namespace**

*tsgo emits alias assignments in namespaces as export declarations, which inadvertently un-exports other expando members in the generated .d.ts file.*

 * (4 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64435#issuecomment-5884506321) **yksr-melt** offered a fix and test applying retroactive export modifier logic to alias branches and asked whether a PR would be welcome
 * (later) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64437](https://github.com/microsoft/TypeScript/issues/64437) (Open, `Needs Investigation`, **ahejlsberg**)

**\`keyof\` over computed property keys yields widening literal types, unlike the same object with literal keys**

*TypeScript’s keyof on computed property keys widens to string instead of the expected literal union types like literal keys.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/64437#issuecomment-5826258900) **trevorade** explained how keyof on enum-keyed maps now widens enum literals due to .d.ts changes and described potential workarounds
 * **RyanCavanaugh** removed label `Needs More Info`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#64438](https://github.com/microsoft/TypeScript/issues/64438) (Open, `Bug`, `Help Wanted`, `Good First Issue`)

**Incorrect/unhelpful error message for non\-module jsx file**

*TypeScript shows misleading missing module errors for JSX in non-module scripts instead of stating scripts cannot import modules.*

 * (5 days ago) **DanielRosenwasser** added labels `Help Wanted`, `Good First Issue`
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-5826551653) **sh011** said "Hi @calebegg @DanielRosenwasser I went through the issue and found that the diagnostic chain needs to be looked up properly. I would like to work on this issue, can you please assign it to me. Thanks!"
 * [later](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-5911162732) **SiddhantShedge45** offered to work on the issue by investigating JSX diagnostic generation, improving the error message, adding a regression test, and verifying existing behavior

### [PR microsoft/TypeScript#64447](https://github.com/microsoft/TypeScript/pull/64447) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Improve callback FS**

*Callback-based file system now mandates explicit implementations for all functions and moves createVirtualFileSystem to test utilities.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64447#issuecomment-5836919279) **andrewbranch** explained semver constraints on adding new keys before a major version bump and asked for clarification on inspecting specific calls
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64447#issuecomment-5837028973) **DanielRosenwasser** said "Is there a reason why you delegate to a symbol instead of providing the "native" function? Is it because that'd involve an extra back-and-forth in sending the same arguments to the API server?"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64447#issuecomment-5837049212) **andrewbranch** said "Yes, exactly. The idea is if you can name a well-known server implementation, you can save a lot of round trips."
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64450](https://github.com/microsoft/TypeScript/issues/64450) (Closed, `Needs Investigation`, **johnfav03**)

**createWatchProgram\(\)\.close\(\) does not cancel the pending program update timer**

*close() does not cancel the pending program update timer in createWatchProgram, causing updates to run after closure and preventing process exit.*

 * created by **sdjayna**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript#64453](https://github.com/microsoft/TypeScript/issues/64453) (Open, `Needs Investigation`, **weswigham**)

**\`EFNoLeadingComments\` suppresses synthesized leading comments in tsgo; Strada only suppresses source comments**

*In tsgo, the EFNoLeadingComments emit flag also suppresses synthesized leading comments, unlike TypeScript’s NoLeadingComments which only suppresses source comments.*

 * created by **trevorade**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64453#issuecomment-5862919851) **z0rimo** investigated printer behavior on main branch, identified a semantic difference with Strada emitter, and opened draft PR #64488 with a compatibility fix and regression tests pending triage
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **weswigham**

### [Issue microsoft/TypeScript#64456](https://github.com/microsoft/TypeScript/issues/64456) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[JavaScript\] main vs **

*The main branch JavaScript ServerErrors pipeline run processed 196 of 300 popular TypeScript repositories, encountering clone failures, timeouts, and detecting seven interesting changes.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840617867) **typescript-automation[bot]** reported server connection closed prematurely error for parcel-bundler/parcel and included last requests and repro steps
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840618336) **typescript-automation[bot]** logged a panic when handling textDocument/diagnostic request, including a stack trace and affected repository details
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840618913) **typescript-automation[bot]** reported a panic handling request for textDocument/diagnostic with a stack trace and build artifact details
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**

### [PR microsoft/TypeScript#64457](https://github.com/microsoft/TypeScript/pull/64457) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Generate compiler option definitions, create JSON schema**

*Generate compiler option metadata to code-generate Go and TypeScript bindings and include a JSON schema in the package*

 * (4 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64457#issuecomment-5895331697) **weswigham** said "(I say this simply because gen-proto is already generating the API's CompilerOptions type - you should just be able to add a .json output to it)"
 * [today](https://github.com/microsoft/TypeScript/pull/64457#issuecomment-5896253300) **jakebailey** explained that most of the content was data not types and that the AST was generated from a JSON file with a TS script, and that using a TS file made diagnostic declarations easier than a Go implementation would
 * [today](https://github.com/microsoft/TypeScript/pull/64457#issuecomment-5900957359) **andrewbranch** mentioned that he moved user preferences generation to JSON because Go's type system is less expressive than TypeScript's
 * [later](https://github.com/microsoft/TypeScript/pull/64457#issuecomment-5914329460) **weswigham** suggested generating the CompilerOptions interface in generate-options.ts and updating gen-proto to import the generated type to remove sequencing-reliant codegen

### [Issue microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript error-delta Azure pipeline on main encountered server errors, failures, and timeouts across 300 repository analyses.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841269708) **typescript-automation[bot]** reported server connection closed prematurely with undefined error and provided affected repo details, error artifacts, last requests, and repro steps
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841270070) **typescript-automation[bot]** reported a 'Server connection closed prematurely: undefined' error for openclaw/openclaw
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841270413) **typescript-automation[bot]** reported a panic in JSX transformer due to unhandled node kind KindBinaryExpression and included a stack trace
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript#64459](https://github.com/microsoft/TypeScript/issues/64459) (Open, `Suggestion`)

**Publish \`fswatch\` Go package**

*Publish fswatch as a standalone Go package by dropping its internal flag and adding a go.mod for filesystem event monitoring.*

 * created by **emersion**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64459#issuecomment-5865066241) **jakebailey** expressed reluctance to maintain a stable API and proposed copying the code with attribution
 * **RyanCavanaugh** added label `Suggestion`
 * [today](https://github.com/microsoft/TypeScript/issues/64459#issuecomment-5894607978) **RyanCavanaugh** said "Yeah, we don't really want to incur the added workload of "This sequence of calls (that tsc never does) results in X problem". File watching is cursed enough already."
 * [today](https://github.com/microsoft/TypeScript/issues/64459#issuecomment-5902381933) **emersion** thanked the maintainer for the reply, acknowledged the API design complexity, and asked to close the issue

### [PR microsoft/TypeScript#64460](https://github.com/microsoft/TypeScript/pull/64460) (Closed, `For Backlog Bug`)

**Fix declaration maps for export assignment expressions**

*Assign original source-map ranges to synthesized export default and export= statements in declaration maps to restore missing mappings.*

 * (4 days ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64460#issuecomment-5881553205) **maricastroc** said "@microsoft-github-policy-service agree"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64461](https://github.com/microsoft/TypeScript/pull/64461) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Report cyclic structures and truncation during declaration emit**

*Enhance declaration emit to detect and report cyclic type structures and truncation instead of silently returning elided anys*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5842706490) **typescript-automation[bot]** reported test results comparing main and the pull request merge, noted infrastructure failures but indicated everything else looked good
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5842766246) **typescript-automation[bot]** reported DT test run failure and pointed to the log
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5842957733) **typescript-automation[bot]** reported build comparison results for top 400 repos between main and the pull request and highlighted failures for review
 * [today](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5899157363) **jakebailey** said "@typescript-bot run dt"
 * [today](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5899159114) **typescript-automation[bot]** reported dt build job start and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5899943301) **typescript-automation[bot]** notified that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5901110586) **jakebailey** retriggered the TypeScript bot to run dt tests
 * [today](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5901111734) **typescript-automation[bot]** started jobs and provided an initial status table
 * [today](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5901344302) **typescript-automation[bot]** reported main-only DT test errors for wicg-task-scheduling due to incompatible scheduler type
 * [today](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5901446288) **jakebailey** said "Exciting, the new DT run found a flake in main."

### [Issue microsoft/TypeScript#64465](https://github.com/microsoft/TypeScript/issues/64465) (Closed)

**Language server retains the pre\-edit program and its checkers for the rest of the session after the first edit**

*The Go-based TypeScript language server leaks memory by retaining pre-edit Program and checker pools via closure-captured options after edits.*

 * created by **ghost2023**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64466](https://github.com/microsoft/TypeScript/pull/64466) (Closed, `For Uncommitted Bug`)

**Fix language server retaining pre\-edit program and its checkers after program clone**

*Prevent TypeScript language server cloned programs from retaining previous program checker pools to reduce memory leaks.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64466#issuecomment-5846290311) **ghost2023** said "@microsoft-github-policy-service agree"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64466#issuecomment-5850307599) **jakebailey** said "I think there's actually another one of these in ReuseProgram via processedFiles."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64466#issuecomment-5880715981) **jakebailey** said "I think this PR is in itself fine, but I'm going to try and put together a very invasive version which prevents us from making this mistake in the future."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64467](https://github.com/microsoft/TypeScript/issues/64467) (Closed, `Bug`, **andrewbranch**)

**getTypeAtLocation crashes on the ImportClause of a type\-only import**

*getTypeAtLocation crashes on type-only ImportClause due to missing symbol causing nil pointer or undefined property errors.*

 * created by **lsh4711**
 * (today) **RyanCavanaugh** added label `Bug`, set milestones to `TypeScript 7.1.0 Beta`, `TypeScript 7.1.1 RC`, removed from milestone `TypeScript 7.1.0 Beta`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64468](https://github.com/microsoft/TypeScript/pull/64468) (Closed, `For Milestone Bug`, **andrewbranch**)

**Prevent getTypeAtLocation crash on type\-only import clause**

*TypeScript's getTypeAtLocation crashes on type-only import clauses without default bindings due to missing symbol guard.*

 * created by **lsh4711**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64468#issuecomment-5846956201) **lsh4711** said "@microsoft-github-policy-service agree"
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64477](https://github.com/microsoft/TypeScript/issues/64477) (Open, `Bug`, **iisaduan**)

**TS6059 error count flakes between runs unless \-\-singleThreaded**

*TypeScript’s TS6059 error count fluctuates between parallel compilations but remains consistent when using --singleThreaded.*

 * created by **maschwenk**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **iisaduan**

### [Issue microsoft/TypeScript#64478](https://github.com/microsoft/TypeScript/issues/64478) (Open, `Suggestion`)

**An \`internal\` property modifier as an alternative to \`protected\`**

*Introduce an internal modifier that keeps properties visible in type definitions but accessible only within class methods.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5856323072) **denis-migdal** clarified that the issue was not a duplicate, explained the desired package visibility as public in declaration files, and suggested renaming ‘internal’ due to ambiguity
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5856738197) **MartinJohns** apologized for the mistake and noted the issue was a duplicate of #37487
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5857413979) **denis-migdal** explained that their suggestion provides a public-facing property that is inaccessible externally but writable internally to serve as an internal interface for helper functions, offering more flexibility and type safety than protected
 * **RyanCavanaugh** added label `Suggestion`
 * [today](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5894466979) **RyanCavanaugh** said "Even a single code example of how you'd expect this to be used would be illuminating. Honestly I'm still not understanding what the goal of this is."
 * [later](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5908822519) **denis-migdal** provided sample code illustrating possible use cases for an `internal` modifier and described current workarounds for friend functions, class implementation, and interface definitions

### [PR microsoft/TypeScript#64479](https://github.com/microsoft/TypeScript/pull/64479) (Closed, `For Uncommitted Bug`)

**Fix flaky diagnostic added by declaration emit for untyped module imports**

*Resolves crash caused by inconsistent diagnostic messages emitted during declaration file generation for untyped module imports.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64479#issuecomment-5855046316) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64482](https://github.com/microsoft/TypeScript/pull/64482) (Closed, `For Uncommitted Bug`)

**Fix flaky diagnostic added by declaration emit through \`MarkLinkedReferencesRecursively\`**

*Modify the declaration emit process to fix flaky diagnostics introduced by MarkLinkedReferencesRecursively and prevent crashes.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64482#issuecomment-5857888374) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64486](https://github.com/microsoft/TypeScript/issues/64486) (Open, `Bug`)

**TS2589 error in TSGo with recursive mapped type over DOM types but not is tsc; ~18x more instantiations than tsc**

*TSGo 7.0.2 triggers TS2589 deep instantiation applying a recursive DeepPartial type to DOM types, performing ~18× more instantiations than tsc.*

 * created by **promitdan**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64488](https://github.com/microsoft/TypeScript/pull/64488) (Open, `For Uncommitted Bug`, **weswigham**)

**Fix synthesized comment emission with comment flags**

*Restore Strada-compatible comment emission so EFNoLeadingComments and EFNoTrailingComments suppress only source comments but still emit synthesized comments.*

 * created by **z0rimo**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **typescript-automation[bot]** assigned to **weswigham**

### [PR microsoft/TypeScript#64491](https://github.com/microsoft/TypeScript/pull/64491) (Open, `For Backlog Bug`)

**Match Strada and don't resolve imports of ambient modules declared in the same file**

*Do not resolve imports of ambient modules declared in the same file to external typings, preventing excessive type instantiations.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64491#issuecomment-5865431338) **jakebailey** said "How does this fix a type explosion issue? Did you misquote the fixed issue?"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64491#issuecomment-5866502732) **Andarist** said "@jakebailey the referenced issue is correct, I put more info to the PR description to explain why this resolves that issue"
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64495](https://github.com/microsoft/TypeScript/issues/64495) (Open, `Bug`, `Cursed?`)

**Record\<K1, T\> & Record\<K2, U\> is assignable to Record\<K1 \| K2, T & U\>**

*TypeScript allows Record<K1, T> & Record<K2, U> to be assigned to Record<K1 | K2, T & U>, unsoundly merging property types.*

 * created by **ahmedajiz629**
 * (today) **RyanCavanaugh** added labels `Bug`, `Cursed?`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64497](https://github.com/microsoft/TypeScript/issues/64497) (Open, `Bug`, `Help Wanted`)

**Find all references on \`from\` of a default import drops results after an unsaved edit in another file**

*In TypeScript 7.0.2, an unsaved edit causes find-all-references on a default import's from in another file to drop results*

 * created by **wangzhihao-lab**
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/64497#issuecomment-5895021858) **SHULMIT** said "Hi! I’d like to work on this issue. I’ve started investigating the references behavior and will work on a fix and regression test."

### [PR microsoft/TypeScript#64513](https://github.com/microsoft/TypeScript/pull/64513) (Closed, `For Uncommitted Bug`)

**Don't let parallel per\-file workers reuse their request's checker**

*Remove request IDs from parallel file worker contexts to prevent unsafe concurrent reuse of the TypeScript checker.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64513#issuecomment-5876854815) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64513#issuecomment-5898744299) **jakebailey** said "This doesn't feel right to me but I can't put my finger on why; I'll try and look into this also."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64518](https://github.com/microsoft/TypeScript/pull/64518) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Make binder\-produced symbols owned by SourceFiles in the client, like the server and 6\.0**

*Cache binder-produced symbols in client SourceFiles to maintain symbol identity across snapshots and enable context-independent symbol retrieval.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64519](https://github.com/microsoft/TypeScript/pull/64519) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Better manage Program options lifetimes**

*Refactor ProgramOptions into separate Config, Hosts, and Factories components to properly manage lifetimes and prevent stale state.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64520](https://github.com/microsoft/TypeScript/issues/64520) (Closed, `Bug`)

**TS2565 false positive in JS for a class field initialized in the base class**

*With allowJs and checkJs enabled, TypeScript incorrectly reports TS2565 for subclass fields initialized in their base class.*

 * created by **harshmandan**
 * [today](https://github.com/microsoft/TypeScript/issues/64520#issuecomment-5887375975) **jwbth** mentioned that assigning the base property in the constructor rather than as a class field likewise triggered TS2565 and noted that destructuring (const { element }= this) avoids it
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64523](https://github.com/microsoft/TypeScript/pull/64523) (Closed, `For Backlog Bug`)

**Fix regression reporting TS2565 for inherited class fields reassigned in JS**

*TypeScript regression incorrectly reports TS2565 errors for inherited class fields reassigned in JavaScript.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64524](https://github.com/microsoft/TypeScript/issues/64524) (Open, `Bug`, **gabritto**)

**JSDoc \`@override\` on an \`@overload\` signature is ignored under \`noImplicitOverride\` \(TS4119\)**

*In TypeScript 7.x, JSDoc @override on overload signatures is ignored under noImplicitOverride, causing TS4119 errors.*

 * created by **jwbth**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.2.0 Beta`, and assigned to **gabritto**

### [PR microsoft/TypeScript#64525](https://github.com/microsoft/TypeScript/pull/64525) (Closed, `For Backlog Bug`)

**Avoid contextually typing static properties by their own class to prevent spurious circularities**

*Modify TypeScript’s type checker to prevent contextually typing a class’s static properties with the class itself, avoiding spurious circularities.*

 * [today](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5887494388) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5898049534) **jakebailey** stated that the change seemed fine and asked the typescript-bot to run tests
 * [today](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5898051569) **typescript-automation[bot]** posted CI build statuses and result links for multiple commands
 * [today](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5898553281) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5898609705) **typescript-automation[bot]** reported new TS2565 errors in webpack tests comparing main and pull request merge
 * [today](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5898784320) **typescript-automation[bot]** reported that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5899496028) **typescript-automation[bot]** provided results of running the top 400 repos with tsc comparing main and the pull request merge branch and noted everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5905887060) **Andarist** explained that the reported issues were due to the branch not being synced with main and then synced with main
 * [later](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5906027151) **jakebailey** questioned how tests could run on a stable merge commit and invoked the bot to test
 * [later](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5906028905) **typescript-automation[bot]** reported that build jobs started and provided status updates with result links
 * [later](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5906108130) **Andarist** said "Hm, ok - then that's confusing. I'll wait for the re-run results and dig into this again."
 * [later](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5906420781) **typescript-automation[bot]** reported that user tests comparison between main and the pull request merge looked good

### [PR microsoft/TypeScript#64527](https://github.com/microsoft/TypeScript/pull/64527) (Open, `For Uncommitted Bug`)

**Fix checkJs behavior for \.mjs and \.cjs files next to declarations**

*Remove legacy wildcard exception to ensure wildcard include consistently prefers declaration files over .js, .mjs, and .cjs implementations.*

 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5891462911) **hkleungai** said "Looks like this PR has a chance to resolve https://github.com/microsoft/TypeScript/issues/63523 too. 😀 "
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5891856716) **hardikkaurani** acknowledged the fix for issue #63523, linked the PR to issue #64312 for consistent .mjs/.d.mts and .cjs/.d.cts behavior, and invited feedback
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5893125311) **jakebailey** said "No tests?"
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5893936578) **hardikkaurani** added a regression test reproducing the original issue and confirmed that .mjs and .cjs files are included in compilation with checkJs enabled
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5895123078) **weswigham** said "...Why would we make the new extensions have an explicitly legacy behavior?"
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5895155427) **weswigham** said "If anything, we should remove the legacy lookup behavior from .js, no? Seems unlikely at this point that anyone intentionally includes a .js and .d.ts file referring to the same input."
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5895552152) **hardikkaurani** investigated the extension-priority behavior and noted the legacy .js/.d.ts exception, proposed either extending it to .mjs/.d.mts and .cjs/.d.cts or removing the exception for consistency, and asked the team to confirm the intended direction before proceeding
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5896251279) **hkleungai** described intentionally including .js and .d.ts files as a non-interruptive typechecking strategy akin to C headers and sources, preferring explicit typedef files over JSDoc and noting its historical viability in older TypeScript
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5896734927) **hardikkaurani** explained the compiler’s handling of .js and .d.ts files discovered via wildcards and noted that maintainer direction is needed on the legacy exception compatibility question
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5897419484) **hkleungai** described that switching to the files array for js-source-ts-type mixes felt hacky and mentally demanding and expressed a preference to include all sources in the include array
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5901269687) **hardikkaurani** agreed with the previous suggestion, clarified explicit inclusion vs files, emphasized consistent include resolution for multiple file extensions, and deferred design decisions to the maintainers
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5905678191) **ljharb** said "@weswigham i intentionally include a .js and .d.ts in all of my typed npm packages, and intend to continue to do so. That's the only way to write typed JS (without writing TS) that I'm aware of."
 * [later](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5908105828) **hardikkaurani** thanked ljharb for context, proposed preserving the companion .js/.d.ts pattern for .mjs and .cjs files, and asked if maintainers would proceed with the current approach
 * [later](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5914546447) **weswigham** rejected preserving side-by-side .js and .d.ts files and argued for aligning include behavior with modern extensions and using JSDoc-annotated JS for typing

### [Issue microsoft/TypeScript#64529](https://github.com/microsoft/TypeScript/issues/64529) (Closed, `Needs Investigation`, **ahejlsberg**)

**Type parameter escapes its constraint in a recursive call resolution**

*Recursive resolution of object calls leaks the type parameter P outside its constraint, causing incorrect inference.*

 * created by **colinhacks**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript#64530](https://github.com/microsoft/TypeScript/pull/64530) (Closed, `For Uncommitted Bug`, **ahejlsberg**)

**Keep a pure return type inference filtered by its constraint in a recursive call resolution**

*Restore constraint filtering for pure return type inferences during recursive call resolution to prevent invalid type arguments*

 * created by **colinhacks**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64530#issuecomment-5892953821) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#64531](https://github.com/microsoft/TypeScript/issues/64531) (Open, `Possible Improvement`)

**Support spread in recursive object inference**

*TypeScript does not correctly infer recursive object schema types when a base shape is spread, resulting in any types instead of the intended schema.*

 * created by **colinhacks**
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64532](https://github.com/microsoft/TypeScript/issues/64532) (Open, `Needs Investigation`, **andrewbranch**)

**\[API\] \`getImmediateAliasedSymbol\` returns a different symbol than classic \`tsc\`**

*getImmediateAliasedSymbol for namespace imports in TypeScript 7 returns a cloned symbol instead of the original file symbol when a module has a default export.*

 * created by **dragomirtitian**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64533](https://github.com/microsoft/TypeScript/issues/64533) (Open, `API Request`, **andrewbranch**)

**\[API\] Expose some type checker features  that were available in TS6**

*Expose four TypeScript 6 type checker APIs—UnionType.getOrigin, Checker.symbolToString, unique symbol properties, and ConditionalType.getInferTypeParameters—for the documentation system.*

 * created by **dragomirtitian**
 * (today) **RyanCavanaugh** added label `API Request`, set milestone to `TypeScript 7.1.0 Beta`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64534](https://github.com/microsoft/TypeScript/issues/64534) (Open, `Needs More Info`)

**Circular mapped property is treated as missing when selecting contextual type from intersections**

*Circular mapped properties in intersection types bypass contextual typing and fall back to index signatures, causing unexpected type inference*

 * created by **Fugu0141**
 * [today](https://github.com/microsoft/TypeScript/issues/64534#issuecomment-5895377674) **RyanCavanaugh** stated that the inference was correct and asked why the expected behavior would be preferable
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/64534#issuecomment-5896176125) **Andarist** pointed out that after skimming the issue, an implementation defect was causing the name property to be treated as circular specifically for reverse mapped type properties
 * [today](https://github.com/microsoft/TypeScript/issues/64534#issuecomment-5901290050) **Fugu0141** asked whether treating missing and circularly-unavailable properties identically as undefined was intentional or incidental

### [PR microsoft/TypeScript#64535](https://github.com/microsoft/TypeScript/pull/64535) (Open, `For Milestone Bug`, **andrewbranch**)

**Expose some type checker features that were available in TS6**

*Expose four previously internal TypeScript 6 type checker features—UnionType.getOrigin, Checker.symbolToString, unique symbol name accessors, and ConditionalType.getInferTypeParameters—for the documentation system.*

 * created by **dragomirtitian**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64536](https://github.com/microsoft/TypeScript/pull/64536) (Closed, `For Backlog Bug`)

**Fix Array\.at documentation: change 'code unit' to 'item'**

*Updated Array.at and TypedArray.at documentation to replace 'code unit' with 'item' in index parameter descriptions.*

 * created by **iamawanishmaurya**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64536#issuecomment-5894534242) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64536#issuecomment-5900379984) **RyanCavanaugh** said "This is good to go but I can't merge it until the CLA is signed"

### [PR microsoft/TypeScript#64537](https://github.com/microsoft/TypeScript/pull/64537) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Verify VSIX signatures with vsce**

*Verify VSIX signatures using vsce post-sign instead of attempting to sign them with OpenSSL*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64538](https://github.com/microsoft/TypeScript/pull/64538) (Open, `For Backlog Bug`)

**Detect self\-referencing mapped type constraints**

*Report a circular constraint error when a mapped type’s type parameter references itself, preventing it from escaping.*

 * created by **Naji-Ullah**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64538#issuecomment-5895201003) **Naji-Ullah** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64539](https://github.com/microsoft/TypeScript/pull/64539) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fuse local syntax lowerings into one traversal**

*Combining local syntax lowerings into one transformer traversal to boost performance and reduce memory usage pending benchmarks.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5895820866) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5895822662) **typescript-automation[bot]** posted an automated build status update for the perf test
 * [today](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5896217293) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5896679911) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5896681435) **typescript-automation[bot]** reported CI build jobs start and provided status table with result links
 * [today](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5897198748) **typescript-automation[bot]** provided the requested perf run results
 * [today](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5897621618) **jakebailey** said "No change???"

### [PR microsoft/TypeScript#64540](https://github.com/microsoft/TypeScript/pull/64540) (Closed, `For Uncommitted Bug`)

**Bump vscode\-typescript to 1\.0\.1**

*Upgrade the vscode-typescript extension to version 1.0.1.*

 * created by **typescript-automation[bot]**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64541](https://github.com/microsoft/TypeScript/pull/64541) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use package feed proxy for global npm installs**

*Global npm installs bypass the local .npmrc and use public registry because the PowerShell script does not exit on errors.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64542](https://github.com/microsoft/TypeScript/pull/64542) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix extension publisher approval job compilation**

*Disable MicroBuild’s publish authorization task injection in agentless approval jobs to allow YAML validation and queueing.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64543](https://github.com/microsoft/TypeScript/pull/64543) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Enforce exclusive checker acquisition**

*Disallow reentrant or concurrent checker reuse to enforce exclusive acquisition, prevent crashes, and simplify the checker management code.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64544](https://github.com/microsoft/TypeScript/pull/64544) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Typed path prep bugfixes**

*Pulled out typed path preparation bugfixes from PR 64159 for separate early review and merge.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64545](https://github.com/microsoft/TypeScript/pull/64545) (Closed, `Author: Team`, `For Milestone Bug`, **weswigham**)

**Add export modifiers to other expando exports of namespaces on all codepaths which add export declarations**

*Ensure expando namespace exports include export modifiers on every code path that adds export declarations.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **weswigham**
 * (later) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64546](https://github.com/microsoft/TypeScript/issues/64546) (Closed, `Working as Intended`)

**Content mappers: registered extensions are not probed for extensionless imports in bundler mode**

*In bundler mode, TypeScript does not probe registered custom contentMapper extensions for extensionless imports, causing TS2307 errors.*

 * created by **leonidaz**
 * [today](https://github.com/microsoft/TypeScript/issues/64546#issuecomment-5900568575) **RyanCavanaugh** clarified that content mappers don't participate in module resolution and asked where this was inferred in the description
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/64546#issuecomment-5901727760) **leonidaz** clarified a misunderstanding about content mappers and module resolution, opened new suggestion issue #64549 and a separate issue #64548 for moduleSuffixes, and asked to close this one in favor of those issues

### [PR microsoft/TypeScript#64547](https://github.com/microsoft/TypeScript/pull/64547) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update Azure pipeline Node installation task**

*Update the outdated Node installation task in the Azure pipeline to the latest version.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64548](https://github.com/microsoft/TypeScript/issues/64548) (Closed, `Working as Intended`)

**Content mappers: \`moduleSuffixes\` probes \`card\.foo\.web\` instead of \`card\.web\.foo\` for a registered extension**

*When using moduleSuffixes with a registered content mapper, a fully specified import probes the suffix after the custom extension (card.foo.web) instead of before (card.web.foo), resolving to the wrong file.*

 * created by **leonidaz**

### [Issue microsoft/TypeScript#64549](https://github.com/microsoft/TypeScript/issues/64549) (Open, `Suggestion`)

**Content mappers: let registered extensions take part in extensionless module lookup**

*Enable TypeScript to include contentMappers’ registered custom extensions in extensionless module import resolution for bundler and Node modes*

 * created by **leonidaz**
 * [later](https://github.com/microsoft/TypeScript/issues/64549#issuecomment-5912337356) **aleclarson** described a concrete use case for cross-platform file variants with .tsrx extensions, explained the current shim workaround and its drawbacks, mentioned a one-line patch enabling resolveHiddenExtensions in TS5/Volar, and offered to share a resolution fixture

### [PR microsoft/TypeScript#64550](https://github.com/microsoft/TypeScript/pull/64550) (Open, `For Backlog Bug`)

**Fix references after unrelated project edits \(\#64497\)**

*Fix lost references after unrelated project edits by loading the source definition's project before inferred-project searches and adding regression tests*

 * created by **SHULMIT**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64551](https://github.com/microsoft/TypeScript/pull/64551) (Open, `For Uncommitted Bug`)

**perf\(checker\): fast\-path compareNodes for identical AST parent containers and use cmp\.Compare**

*Introduces a fast-path compareNodes for identical AST parents and uses cmp.Compare to prevent 64-bit symbol ID overflow.*

 * created by **hazyhaar**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5907391690) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5907502775) **hazyhaar** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5914036976) **jakebailey** criticicized that the PR contained unrelated changes and needed splitting, and noted that increasing GOGC would increase memory footprint
 * [later](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5914567421) **hazyhaar** reduced the PR to only checker optimizations, implemented a fast-path in compareNodes for same-parent nodes, switched to cmp.Compare for SymbolId fallback, removed 32-bit ID narrowing, dropped GOGC tuning, and withdrew SIMD kernels
 * [later](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5914905234) **jakebailey** said "The PR description is still describing the original state."

### [Issue microsoft/TypeScript#64552](https://github.com/microsoft/TypeScript/issues/64552) (Open, `Needs Investigation`, **johnfav03**)

**\`\-\-incremental\` keeps stale diagnostics after \`lib\` or \`target\` changes in tsconfig\.json \(7\.0\.2, regression from 6\.0\.3\)**

*TypeScript 7.0.2’s --incremental compiler retains stale diagnostics after toggling tsconfig.json lib or target settings.*

 * created by **valeralebedz**

### [PR microsoft/TypeScript#64553](https://github.com/microsoft/TypeScript/pull/64553) (Closed, `Author: Team`, `For Backlog Bug`, **ahejlsberg**)

**Cache inferences made from type arguments**

*Cache type argument inferences in the existing invokeOnce infrastructure and include variance states to prevent false matches*

 * created by **ahejlsberg**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5914522225) **ahejlsberg** asked the contributor to describe what happens in the test after manually verifying its effect on check times
 * [later](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5914537348) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5914538753) **typescript-automation[bot]** reported CI job statuses and result links for various test commands

### [PR microsoft/TypeScript#64554](https://github.com/microsoft/TypeScript/pull/64554) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Ensure completion symbols returned to API always come from the current snapshot**

*Ensure completion symbols returned by the API originate from the current snapshot and allow configuring auto-import behavior.*

 * created by **andrewbranch**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

