# Report for 2026-10-14 (Tuesday, October 13th, 2026)

17 different users commented on 108 different issues.

## Recommended Actions

 * Response Recommended
    * @tadhgmister requested a playground build to provide runnable example links in [microsoft/TypeScript#36165](https://github.com/microsoft/TypeScript/issues/36165#issuecomment-6160834637)
    * @alexicum asked if they missed anything about path rules and validation for export and import targets in [microsoft/TypeScript#63803](https://github.com/microsoft/TypeScript/issues/63803#issuecomment-6155919191)
    * @alexicum asked if they should open a separate issue in [microsoft/TypeScript#63803](https://github.com/microsoft/TypeScript/issues/63803#issuecomment-6162680190)
    * @alexicum provided context on publint's checks and suggested dedicated validation in tsc/LSP in [microsoft/TypeScript#63803](https://github.com/microsoft/TypeScript/issues/63803#issuecomment-6162831428)
    * @DerekZiemba reported a memory consumption issue and provided details and screenshot in [microsoft/TypeScript#64568](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-6160927576)
    * @seunghyun-24 provided context about how they noticed the issue during a pilot study in [microsoft/TypeScript#64730](https://github.com/microsoft/TypeScript/issues/64730#issuecomment-6158338383)

## Activity Summary

### [Issue microsoft/TypeScript#36165](https://github.com/microsoft/TypeScript/issues/36165) (Open, `Suggestion`, `In Discussion`)

**\`inherit\` keyword as shorthand to refer to super class fields and methods\.**

*Introduce an `inherit` keyword to TypeScript for shorthand referencing of superclass field and method types.*

 * [50 weeks ago](https://github.com/microsoft/TypeScript/issues/36165#issuecomment-3457191493) **tadhgmister** explained that new features start at a low priority requiring a lot of interest and someone to prototype, and suggested using a type alias (A&B&C) instead of the super keyword to refer to combined base types in type positions
 * [50 weeks ago](https://github.com/microsoft/TypeScript/issues/36165#issuecomment-3457357004) **FrameMuse** mentioned that `this` already works similarly and expressed willingness to work on alternative syntax for interface method resolution if a suitable syntax is proposed
 * [49 weeks ago](https://github.com/microsoft/TypeScript/issues/36165#issuecomment-3478181051) **tadhgmister** provided an example playground link quoting the original post
 * [today](https://github.com/microsoft/TypeScript/issues/36165#issuecomment-6160834637) **tadhgmister** described creating a sample PoC listing its implementation issues and requested a playground build to provide runnable example links

### [Issue microsoft/TypeScript#63803](https://github.com/microsoft/TypeScript/issues/63803) (Open, `Needs Investigation`, `Domain: LS: Auto-import`, **andrewbranch**)

**Missing auto\-import for subpath imports of other local packages**

*VS Code TypeScript auto-imports fail to recognize subpath imports from sibling local workspace packages.*

 * [27 weeks ago](https://github.com/microsoft/TypeScript/issues/63803#issuecomment-5351501674) **psznm** described that deleting node_modules/pkg2 enabled auto imports for "#pkg4/*" but that the workaround failed without including ../pkg2 in tsconfig.json
 * (1 week ago) **RyanCavanaugh** added labels `Needs Investigation`, `Domain: LS: Auto-import`
 * [today](https://github.com/microsoft/TypeScript/issues/63803#issuecomment-6155919191) **alexicum** summarized Node.js package export and import path rules and asked if anything was missing
 * [today](https://github.com/microsoft/TypeScript/issues/63803#issuecomment-6162680190) **alexicum** said "@andrewbranch Maybe LSP and tsc should report an error if spec rules are violated. Should I open a separate issue for this?"
 * [later](https://github.com/microsoft/TypeScript/issues/63803#issuecomment-6162831428) **alexicum** noted that publint will catch the case incidentally and suggested adding a dedicated validation in tsc/LSP
 * [later](https://github.com/microsoft/TypeScript/issues/63803#issuecomment-6171245773) **andrewbranch** said "I think that would probably be good to have as a resolution diagnostic in the Node module resolution modes, yeah."

### [PR microsoft/TypeScript#63914](https://github.com/microsoft/TypeScript/pull/63914) (Open, `For Uncommitted Bug`, **gabritto**)

**Don't defer index types for non\-generic substitution types**

*Prevent index types from being deferred when substitution types are non-generic.*

 * created by **Andarist**
 * (7 weeks ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript/pull/63914#issuecomment-6156910861) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63914#issuecomment-6156912109) **typescript-automation[bot]** updated CI job statuses and provided results links for various test commands
 * [today](https://github.com/microsoft/TypeScript/pull/63914#issuecomment-6157240115) **typescript-automation[bot]** informed that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/63914#issuecomment-6157322069) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/63914#issuecomment-6157481794) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63914#issuecomment-6158150710) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [Issue microsoft/TypeScript#63962](https://github.com/microsoft/TypeScript/issues/63962) (Closed, `Bug`)

**Crash: class\-level decorator on an anonymous class panics during ES decorator emit**

*Using a class decorator on an unnamed class triggers a TypeScript compiler panic during ES decorator emission*

 * created by **daniellockyer**
 * (7 weeks ago) **RyanCavanaugh** added label `Bug`, and set milestone to `TypeScript 7.1`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63971](https://github.com/microsoft/TypeScript/pull/63971) (Closed, `For Milestone Bug`)

**Fix crash on decorated anonymous class declaration**

*Prevent compiler crash when using decorators on anonymous class declarations.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63980](https://github.com/microsoft/TypeScript/pull/63980) (Closed, `For Backlog Bug`)

**Re\-order Array\#reduce and Array\#reduceRight overloads in lib\.es5\.d\.ts**

*Prioritize generic Array#reduce and reduceRight overloads before same-type overloads in lib.es5.d.ts to improve type inference*

 * created by **sundeep8967**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/63980#issuecomment-5400942975) **sundeep8967** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63980#issuecomment-6153628684) **sundeep8967** acknowledged the generic reduce overload inference issue and closed the PR
 * (today) **sundeep8967** closed the issue

### [Issue microsoft/TypeScript#64053](https://github.com/microsoft/TypeScript/issues/64053) (Closed, `Needs Investigation`, **andrewbranch**)

**content\-mapper generates inconsistent declaration extensions, making management of package\.json\#exports hard / verbose**

*Content-mapper generates inconsistent declaration file extensions, complicating package.json exports configuration.*

 * **andrewbranch** assigned to **andrewbranch**
 * (6 weeks ago) **andrewbranch** reopened the issue
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5495687055) **NullVoxPopuli** shared a spike link and cautioned about its quality due to lack of Go experience
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64063](https://github.com/microsoft/TypeScript/pull/64063) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Ditch nodeData interface in favor of generated accessors**

*Replace dynamic nodeData interface with generated accessors to reduce binary size, cut AST symbols, and improve compile performance.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-6026260616) **jakebailey** said "@typescript-bot perf test this"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-6026261943) **typescript-automation[bot]** started performance test builds and posted status update with links to build results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-6026643943) **typescript-automation[bot]** provided the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-6151517581) **jakebailey** said "Superseded by #64773, the bottom of the stack summarized in #64734."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64072](https://github.com/microsoft/TypeScript/pull/64072) (Closed, `For Backlog Bug`)

**fix\(64058\): fix reparse jsdoc @extends type arguments for call expressions**

*Corrects the re-parsing of JSDoc @extends type arguments in call expressions.*

 * (6 weeks ago) **a-tarasyuk** closed the issue
 * (6 weeks ago) **a-tarasyuk** reopened the issue
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64072#issuecomment-6154904228) **jakebailey** revisited the implementation and requested two tweaks, supplying a test case
 * [later](https://github.com/microsoft/TypeScript/pull/64072#issuecomment-6171794220) **jakebailey** pointed out that extends null now gets type arguments and asked to skip KindNullKeyword in the reparser and add a test

### [PR microsoft/TypeScript#64077](https://github.com/microsoft/TypeScript/pull/64077) (Open, `For Backlog Bug`)

**Fixed signature caching issue caused by reentrant signature checking**

*Ports a prior fix and adds an extra commit to resolve reentrant signature caching issues without regressions.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64077#issuecomment-6156888177) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64077#issuecomment-6156889589) **typescript-automation[bot]** posted automated build status updates for test commands
 * [today](https://github.com/microsoft/TypeScript/pull/64077#issuecomment-6157197974) **typescript-automation[bot]** reported that DT test results were ready and unchanged and linked to the logs
 * [today](https://github.com/microsoft/TypeScript/pull/64077#issuecomment-6157288930) **typescript-automation[bot]** posted performance run results with a comparison report table
 * [today](https://github.com/microsoft/TypeScript/pull/64077#issuecomment-6157297002) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64077#issuecomment-6157905724) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [PR microsoft/TypeScript#64114](https://github.com/microsoft/TypeScript/pull/64114) (Closed)

**Add typed array constructor regression coverage**

*Add regression tests to ensure typed array constructors continue rejecting byteOffset and length when passed another typed array.*

 * created by **barislabs**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64169](https://github.com/microsoft/TypeScript/pull/64169) (Open, `For Backlog Bug`)

**Preserve \`\<\` in \`getChildren\(\)\` when type arguments begin with \`\<\`**

*Update getChildren() to preserve the leading “<” token when type arguments begin with “<”*

 * (5 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64169#issuecomment-6156966758) **jakebailey** said "Is there an equivalent to this in Corsa?"

### [PR microsoft/TypeScript#64214](https://github.com/microsoft/TypeScript/pull/64214) (Closed, `For Backlog Bug`)

**Fix getChildren\(\) dropping opening '\<' token when immediately followed by '\<' \(\#64168\)**

*Fix addSyntheticNodes to split '<<' tokens so getChildren includes the missing '<' in consecutive type argument lists.*

 * (1 month ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64214#issuecomment-5605470327) **vaibhavsrv** rebased the branch onto clean upstream/main to remove deferred import commits and included only the getChildren() fix for issue #64168 with its AST invariant regression test
 * [today](https://github.com/microsoft/TypeScript/pull/64214#issuecomment-6156955844) **jakebailey** said "#64169"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64356](https://github.com/microsoft/TypeScript/issues/64356) (Open, `Needs Investigation`, `Domain: Content Mappers`, **andrewbranch**)

**TypeScript 7 VS Code extension: let extensions that serve their language through content mappers opt out of the tsserver\-plugin warning**

*Enable extensions using TypeScript 7 content mappers to suppress tsserver-plugin warnings via a declarative flag*

 * (2 weeks ago) **RyanCavanaugh** added label `Domain: Content Mappers`, and assigned to **andrewbranch**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64356#issuecomment-5936832948) **leonidaz** suggested using registered content mappers to skip tsserver plugin warnings instead of requiring manifest flags and noted a timing detail about re-running the check after registration
 * **andrewbranch** added to milestone `TypeScript 7.1.1 RC`

### [PR microsoft/TypeScript#64360](https://github.com/microsoft/TypeScript/pull/64360) (Open, `For Backlog Bug`)

**Fix union overload signature ordering instability**

*Ensure consistent union overload resolution by ordering synthesized candidates based on each constituent’s signature precedence.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5767834549) **adilalperenciftci** dropped the post-sorting approach and replaced it with expanding optional-parameter signatures into exact-arity variants in getUnionSignatures so findMatchingSignatures matches without extra sorting
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5843031820) **adilalperenciftci** rebased cleanly on current main and asked if the revised getUnionSignatures arity expansion was preferable or if union overload matching should be handled differently
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6096350640) **adilalperenciftci** followed up on the PR, stated the branch was rebased cleanly on main with no conflicts, and asked for a review of the revised getUnionSignatures approach
 * [today](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6154780445) **jakebailey** said "I don't think this PR is right but can't put my finger on why. Figuring out why it feels wrong probably means I have to figure out a fix myself, which defeats the purpose a bit."

### [Issue microsoft/TypeScript#64486](https://github.com/microsoft/TypeScript/issues/64486) (Closed, `Bug`)

**TS2589 error in TSGo with recursive mapped type over DOM types but not is tsc; ~18x more instantiations than tsc**

*TSGo 7.0.2 triggers TS2589 deep instantiation applying a recursive DeepPartial type to DOM types, performing ~18× more instantiations than tsc.*

 * created by **promitdan**
 * (2 weeks ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64491](https://github.com/microsoft/TypeScript/pull/64491) (Closed, `For Backlog Bug`)

**Match Strada and don't resolve imports of ambient modules declared in the same file**

*Do not resolve imports of ambient modules declared in the same file to external typings, preventing excessive type instantiations.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64491#issuecomment-5866502732) **Andarist** said "@jakebailey the referenced issue is correct, I put more info to the PR description to explain why this resolves that issue"
 * (2 weeks ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64532](https://github.com/microsoft/TypeScript/issues/64532) (Open, `Needs Investigation`, **andrewbranch**)

**\[API\] \`getImmediateAliasedSymbol\` returns a different symbol than classic \`tsc\`**

*getImmediateAliasedSymbol for namespace imports in TypeScript 7 returns a cloned symbol instead of the original file symbol when a module has a default export.*

 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/64532#issuecomment-6151189735) **andrewbranch** said "We have checker.getTargetSymbol(symbol). Does that not address this?"

### [PR microsoft/TypeScript#64551](https://github.com/microsoft/TypeScript/pull/64551) (Closed, `For Uncommitted Bug`)

**perf\(checker\): fast\-path compareNodes for identical AST parent containers and use cmp\.Compare**

*Introduces a fast-path compareNodes for identical AST parents and uses cmp.Compare to prevent 64-bit symbol ID overflow.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5916574307) **typescript-automation[bot]** posted automated build status update
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5917030053) **typescript-automation[bot]** reported the requested performance run results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5917132564) **jakebailey** suggested checking additional parent nodes and considering a more clever parent traversal to optimize comparisons
 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-6157165515) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-6157166753) **typescript-automation[bot]** reported initiation of perf test jobs and provided status links
 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-6157530877) **typescript-automation[bot]** provided the requested performance run results

### [PR microsoft/TypeScript#64563](https://github.com/microsoft/TypeScript/pull/64563) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Build all platforms in parallel in release pipeline**

*Build all platforms concurrently in the release pipeline to accelerate full release builds.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64568](https://github.com/microsoft/TypeScript/issues/64568) (Open, **dbaeumer**)

**Bug Report: Severe memory leak triggered by "TypeScript \(Native Preview\)" extension**

*Enabling the TypeScript Native Preview extension causes a memory leak when opening a TS file in a folder without package.json.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-5931170441) **dbaeumer** said "@lszomoru forget my last comment."
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-5931170553) **dbaeumer** reproduced the issue using GPT-6 Astra and identified that TypeScript requests an overly broad recursive file watcher when package.json is absent, analysed the cause in watch-root calculation and parcel watcher behavior, provided memory evidence suggesting ZFS ARC fill rather than a heap leak, and requested trace-level log entries for further comparison
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-5931170686) **dbaeumer** said "Moving back to the TS team based on the above analysis."
 * [today](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-6160927576) **DerekZiemba** reported that opening a TypeScript file triggered the built-in extension to launch tsc.exe consuming ~10 GB memory despite goMemLimit settings and without having typescript-next installed

### [PR microsoft/TypeScript#64581](https://github.com/microsoft/TypeScript/pull/64581) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Add content mapper output extensions**

*Add support for specifying content mapper output file extension mappings in TypeScript configs and package manifests.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64581#issuecomment-5971700909) **leonidaz** thanked andrewbranch and argued that TypeScript should allow extensionless resolution for mapper-supported formats when configured to match bundler behavior
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64586](https://github.com/microsoft/TypeScript/pull/64586) (Open, `For Backlog Bug`)

**Restore index signature details in property hovers**

*Restore index signature details in TypeScript property hover tooltips to show key and value type information.*

 * (1 week ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64586#issuecomment-6154874697) **jakebailey** said "This PR needs a merge from main"

### [PR microsoft/TypeScript#64615](https://github.com/microsoft/TypeScript/pull/64615) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Restore dependency\-depth build scheduling**

*Restore the dependency-depth-based build scheduling functionality removed by PR #64158 that regressed PR #64220.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64648](https://github.com/microsoft/TypeScript/pull/64648) (Closed, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Add cache to \`getSimplifiedConditionalType\`**

*Add caching for conditional types in getSimplifiedType to improve performance and ensure consistency.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64648#issuecomment-6002061254) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64648#issuecomment-6002735350) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64648#issuecomment-6004798872) **ahejlsberg** said "No measurable effect on perf tests, likely because we don't have react tests which is where it's supposed to help."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64667](https://github.com/microsoft/TypeScript/issues/64667) (Closed, `Bug`)

**runtime error: invalid memory address or nil pointer dereference**

*TypeScript compiler panics with a nil pointer dereference when emitting declaration files using --stripInternal on an internal type alias.*

 * created by **YuanchengJiang**
 * (6 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64689](https://github.com/microsoft/TypeScript/issues/64689) (Open, `Suggestion`)

**TS 7 language server: "Add missing properties" quick fix not offered**

*The TypeScript 7 native language server in VS Code no longer provides the "Add missing properties" quick fix for objects missing required properties as it did in TS 6.0.3.*

 * created by **erengeez**
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#64690](https://github.com/microsoft/TypeScript/issues/64690) (Open, `Bug`, **ahejlsberg**)

**TS2322: \`const\` type parameter infers \`readonly \[\]\`, rejected through a union return type \(7\.1\.0\-dev regression from typescript\-go\#4591\)**

*A regression in TypeScript 7.1.0-dev causes const type parameters to infer readonly[] instead of string[], resulting in a TS2322 error when returning ok([]) in a union return type.*

 * created by **paoValle**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript#64695](https://github.com/microsoft/TypeScript/pull/64695) (Open, `For Milestone Bug`, **ahejlsberg**)

**\[experiment\] Skip incompatible discriminants when inferring**

*Experimentally skip incompatible discriminant properties during TypeScript union type inference to reduce workload and validate via tests.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6133547696) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6133547985) **typescript-automation[bot]** provided the requested performance run results for tsc
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6134265513) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript#64697](https://github.com/microsoft/TypeScript/pull/64697) (Open, `For Uncommitted Bug`)

**feat: add missing properties and JSX attributes code fixes**

*Add missing properties and rectify JSX attribute handling via code fixes.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64697#issuecomment-6151573899) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #64689. If you can get it accepted, this PR will have a better chance of being reviewed."

### [Issue microsoft/TypeScript#64700](https://github.com/microsoft/TypeScript/issues/64700) (Open, `Needs Investigation`, **andrewbranch**)

**LSP middleware cannot handle \`textDocument/prepareRename\` errors, which blocks rename in embedded templates**

*The LSP middleware fails to process prepareRename error responses, blocking renames within embedded templates.*

 * created by **mantou132**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.2.0 Beta`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/64700#issuecomment-6151025387) **RyanCavanaugh** said "I don't think LSP middleware is how we want to solve this problem in general, but this might be a reasonable tweak"

### [Issue microsoft/TypeScript#64701](https://github.com/microsoft/TypeScript/issues/64701) (Open, `Bug`)

**typescript\-go: Infinite recursion in inferFromTypes via getReturnTypeOfSignature \(tsc 5\.9 OK\)**

*typescript-go infinite recursion in inferFromTypes via getReturnTypeOfSignature for type-fest overloads blocks oxlint, whereas tsc 5.9 finishes.*

 * created by **jandolezal71**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64702](https://github.com/microsoft/TypeScript/issues/64702) (Open, `Help Wanted`, `Possible Improvement`)

**\[7\.0 regression\] hover on calls through object properties loses function JSDoc while signature help works**

*Hovering on object property calls in TypeScript 7.0.x omits JSDoc comments whereas signature help still shows them.*

 * created by **lixiaoyan**
 * (today) **RyanCavanaugh** added labels `Help Wanted`, `Possible Improvement`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64704](https://github.com/microsoft/TypeScript/pull/64704) (Open, `For Backlog Bug`)

**Restore function signature documentation in native hover**

*Hovering function calls now shows the declaration’s JSDoc (even through aliases or wrappers), with fallback to the function’s own comments.*

 * created by **lixiaoyan**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64705](https://github.com/microsoft/TypeScript/issues/64705) (Open, `Bug`)

**False negative issues in function type parameters of ts2824**

*Function type parameter destructuring with unused renamed generics does not trigger the expected TS2824 error.*

 * created by **bvanjoi**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64706](https://github.com/microsoft/TypeScript/issues/64706) (Open, `Bug`)

**Declaration emit renames value references when a shadowed type parameter shares its parameter's name**

*TypeScript declaration emit incorrectly renames value references in nested functions when inner and outer type parameters share the same name.*

 * created by **jasonkuhrt**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64706#issuecomment-6101243821) **maricastroc** reproduced the issue on main, traced it to declaration emit identifier rewriting, and prepared a fix and regression tests while awaiting issue triage before opening a PR per the contribution guidelines
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64710](https://github.com/microsoft/TypeScript/issues/64710) (Open, **johnfav03**)

**\[ServerErrors\]\[JavaScript\] main**

*CI tests on the main branch reported server errors, timeouts, and unknown failures while analyzing 300 popular TypeScript repositories.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64710#issuecomment-6090296476) **typescript-automation[bot]** reported a panic during textDocument/diagnostic handling with a stack trace and details for chartjs/Chart.js
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64710#issuecomment-6090297018) **typescript-automation[bot]** reported a server connection closed prematurely error with undefined and provided affected repo, artifact links, last requests, and repro steps
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64710#issuecomment-6090297648) **typescript-automation[bot]** reported a server connection closed prematurely error for the vuejs/vue-cli repository with associated logs and repro steps
 * **RyanCavanaugh** assigned to **johnfav03**

### [Issue microsoft/TypeScript#64714](https://github.com/microsoft/TypeScript/issues/64714) (Open, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main**

*The TypeScript main build pipeline encountered server errors analyzing 300 repositories, successfully completing 147 analyses and logging several timeouts, clone failures, and unknown errors.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64714#issuecomment-6091661594) **typescript-automation[bot]** reported a panic handling textDocument/completion due to path containing a URL query or fragment
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64714#issuecomment-6091662030) **typescript-automation[bot]** reported a server connection closed prematurely for babel/babel and provided error details, recent requests, and repro steps
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64714#issuecomment-6091662486) **typescript-automation[bot]** reported a server connection closing prematurely with undefined error for openclaw/openclaw and included affected repo details, logs, and repro steps
 * **RyanCavanaugh** assigned to **johnfav03**

### [PR microsoft/TypeScript#64716](https://github.com/microsoft/TypeScript/pull/64716) (Open, `For Backlog Bug`)

**Re\-scan '\<\<' when parsing type arguments in heritage clauses, typeof queries, and JSX**

*Adjust parser to split '<<' tokens into two '<' when parsing type arguments in heritage clauses, typeof queries, and JSX.*

 * created by **ahmad65saad**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64716#issuecomment-6093450032) **ahmad65saad** agreed with microsoft-github-policy-service
 * [today](https://github.com/microsoft/TypeScript/pull/64716#issuecomment-6155000453) **jakebailey** noted that esbuild accepted the syntax and requested the typescript-bot to test it
 * [today](https://github.com/microsoft/TypeScript/pull/64716#issuecomment-6155002518) **typescript-automation[bot]** posted CI job statuses and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64716#issuecomment-6155389069) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64716#issuecomment-6155502830) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64716#issuecomment-6155504416) **typescript-automation[bot]** posted the perf run results requested by @jakebailey
 * [today](https://github.com/microsoft/TypeScript/pull/64716#issuecomment-6156224299) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [Issue microsoft/TypeScript#64730](https://github.com/microsoft/TypeScript/issues/64730) (Open)

**TS 7\.0 reports declaration\-emit diagnostics \(e\.g\. TS2527\) under \-\-noEmit when other semantic errors exist; TS 6\.0 does not \(undocumented difference\)**

*TypeScript 7.0 reports declaration-emit diagnostics under --noEmit when other semantic errors are present, unlike 6.0.*

 * created by **seunghyun-24**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64730#issuecomment-6123969870) **jakebailey** said "Is this a problem, or something you just happened to notice?"
 * [today](https://github.com/microsoft/TypeScript/issues/64730#issuecomment-6158338383) **seunghyun-24** explained that they just noticed the issue during a pilot study comparing TS conformance test outputs between tsc 6.0 and 7.0

### [PR microsoft/TypeScript#64735](https://github.com/microsoft/TypeScript/pull/64735) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Resolve instantiated object members through a shared worker**

*Allow instantiated object members to be resolved properly when used inside shared workers.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6129177084) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6129178555) **typescript-automation[bot]** reported that performance tests started and provided links to status and results
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6129638105) **typescript-automation[bot]** posted the requested perf run results comparing baseline and PR, showing symbol count reduction and memory usage improvements
 * [today](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6151656466) **jakebailey** said "Superseded by #64765."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64741](https://github.com/microsoft/TypeScript/pull/64741) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 6 updates**

*Upgrades six GitHub Actions (setup-node, upload/download-artifact, and CodeQL) in the project root to newer versions.*

 * **dependabot[bot]** added label `github_actions`
 * (2 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64750](https://github.com/microsoft/TypeScript/pull/64750) (Open, `For Uncommitted Bug`)

**Add support for Jujutsu conflict markers**

*Extend TypeScript’s conflict marker detection to support Jujutsu-style markers using %, \ and + separators.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6130727617) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6130729363) **typescript-automation[bot]** posted initial build status with results table
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6131219606) **typescript-automation[bot]** reported the results of the requested perf run
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6150291835) **RyanCavanaugh** inquired if opening an issue was mandatory or optional and suggested using an issue to discuss conflict marker forms
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6159916825) **rf-** said "Good points, thanks @jakebailey! Apologies for not covering all of the possible formats, it definitely makes sense to do them all at once. I'll open an issue to ref in the PR."

### [Issue microsoft/TypeScript#64754](https://github.com/microsoft/TypeScript/issues/64754) (Closed)

**\[api\] createSnapshot never returns when the opened tsconfig\.json has a circular extends**

*createSnapshot hangs indefinitely on projects whose tsconfig.json files have circular extends.*

 * created by **cplieger**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64755](https://github.com/microsoft/TypeScript/pull/64755) (Closed, `For Uncommitted Bug`)

**\[api\] Leave a config out of its own extended source files**

*Skip adding a tsconfig file to its own ExtendedSourceFiles list to prevent createSnapshot hangs on circular extends chains*

 * created by **cplieger**
 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64762](https://github.com/microsoft/TypeScript/pull/64762) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix symbol table kind mask**

*Restore alias caching and the members fast path by ensuring the symbol table kind mask includes all three kind bits.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64762#issuecomment-6138956554) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64762#issuecomment-6138957785) **typescript-automation[bot]** reported build status for performance test and provided results link
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64762#issuecomment-6139283586) **typescript-automation[bot]** posted the requested perf run results
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64766](https://github.com/microsoft/TypeScript/issues/64766) (Open, `Bug`)

**\`===\` narrowing of a primitive union now produces a non\-widening literal type \(regression from microsoft/typescript\-go\#4781\)**

*Primitive union values narrowed by an equality check now generate non-widening literal types in TypeScript Go, causing assignment errors.*

 * created by **sophiebits**
 * (today) **RyanCavanaugh** added labels `Bug`, `Bug`, removed label `Bug`, and set milestone to `TypeScript 7.1.1 RC`

### [Issue microsoft/TypeScript#64768](https://github.com/microsoft/TypeScript/issues/64768) (Closed)

**TS2536 indexing an \`as\`\-remapped mapped type by \`Exclude\<keyof T & string, \.\.\.\>\` \(native 7\.0\.2 only\)**

*TypeScript 7.0.2 incorrectly reports TS2536 when indexing an as-remapped mapped type with Exclude<keyof T & string>.*

 * created by **kokipsiho**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64770](https://github.com/microsoft/TypeScript/pull/64770) (Closed, `For Backlog Bug`)

**Fix nil panic when stripInternal elides type alias RHS**

*Substitute any for stripped internal type alias right-hand sides under stripInternal to avoid nil pointer panics during declaration emit.*

 * created by **andre-fajar-n**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64771](https://github.com/microsoft/TypeScript/pull/64771) (Open, `For Milestone Bug`)

**Preserve widening literals when narrowing primitive unions by equality**

*Preserve widened literal types during equality-based narrowing of primitive unions in TypeScript.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64772](https://github.com/microsoft/TypeScript/pull/64772) (Closed, `For Uncommitted Bug`)

**Port missing keyof simplification for generic mapped types with name types**

*Port missing keyof simplification support for generic mapped types with name types and correct a misported pull request.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64773](https://github.com/microsoft/TypeScript/pull/64773) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Replace nodeData interface with generated AST accessors**

*Replace the dynamic nodeData interface with generated AST kind-switch accessors, reducing code size and improving compile performance.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64774](https://github.com/microsoft/TypeScript/pull/64774) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compact checker type metadata**

*Replace self-referential type metadata with a compact kind tag to save 16 bytes per type and remove GC pointer storage.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64775](https://github.com/microsoft/TypeScript/pull/64775) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compress paged link\-store references**

*Convert pointer-sized page entries in dense checker link stores to four-byte arena indexes, halving storage and eliminating pointers.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue

### [PR microsoft/TypeScript#64776](https://github.com/microsoft/TypeScript/pull/64776) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Batch allocations of common checker types**

*Use typed arenas to batch allocate common checker type records, reducing small-object heap allocation overhead while enabling independent block collection.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64777](https://github.com/microsoft/TypeScript/pull/64777) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Presize checker type\-list cache keys**

*Reserve the encoded size upfront for type-list cache keys to minimize temporary hash buffer allocations.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64778](https://github.com/microsoft/TypeScript/pull/64778) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid allocating normalized types on interning cache hits**

*Reuse cached union and intersection types during normalization to avoid temporary allocations and improve memory efficiency.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64779](https://github.com/microsoft/TypeScript/pull/64779) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compact type mappers and coallocate inference mapper storage**

*Compact type mappers by replacing interfaces with a concrete header and coallocating two inference mappers, reducing allocations by 3.90%.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64780](https://github.com/microsoft/TypeScript/pull/64780) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Move cold value\-symbol links out of the hot records**

*Move optional value-symbol link fields into a sidecar structure to shrink hot records and improve memory usage*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64781](https://github.com/microsoft/TypeScript/pull/64781) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Index checker members without redundant symbol maps**

*Use ordered property lists and pointer-free integer slots instead of redundant symbol maps, decreasing heap retention and GC scanning.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64782](https://github.com/microsoft/TypeScript/pull/64782) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Recover concrete AST nodes from their embedded headers**

*Recover AST nodes from embedded headers at offset zero with kind-checked casts to shrink header size and reduce memory usage*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64783](https://github.com/microsoft/TypeScript/pull/64783) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep optional symbol tables out of hot symbol records**

*Optional symbol tables are relocated to arena-batched metadata, shrinking symbol records and reducing memory usage.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64784](https://github.com/microsoft/TypeScript/pull/64784) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Move optional structured type shape into cold storage**

*Move unused StructuredType fields into optional storage to shrink its size and cut memory and GC overhead.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64785](https://github.com/microsoft/TypeScript/pull/64785) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep optional type\-node and signature state out of hot records**

*Reduce TypeScript compiler memory usage by extracting optional type-node parameters and signature state from hot record structures.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64786](https://github.com/microsoft/TypeScript/pull/64786) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Bound arena retention by bytes instead of object count**

*Bound arena chunk size by 512 bytes instead of object count to reduce heap retention and GC work.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64787](https://github.com/microsoft/TypeScript/pull/64787) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use paged indexes for type\-node and signature caches**

*Type-node and signature caches are migrated from AST pointer maps to paged indexes using existing node-link stores, reducing heap usage, GC scanning, and allocations.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64788](https://github.com/microsoft/TypeScript/pull/64788) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Store ordinary relationship keys as exact type ID pairs**

*Store ordinary comparison keys as 64-bit type ID pairs instead of 128-bit hashes, improving memory usage.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64789](https://github.com/microsoft/TypeScript/pull/64789) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Share complete union and intersection property cache entries**

*Share complete property cache entries between augmented and non-augmented lookups to reduce duplicate entries, memory usage, and GC scanning overhead.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64790](https://github.com/microsoft/TypeScript/pull/64790) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reuse ordered property counts during intersection reduction**

*Reuse bounded, checker-local property-count tables during intersection reduction to reduce allocated memory by around 27% and allocations by about 8%.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64791](https://github.com/microsoft/TypeScript/pull/64791) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Lint writes to protected record kind fields**

*Introduce a custom lint analyzer that marks record kind fields as protected and rejects unsafe writes or copies.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64791#issuecomment-6157230696) **jakebailey** described that layout lint is a best-effort guard, noted that checked casts panic on mismatched kinds, fixed shadowed `kind` and copy/variadic `append` cases, and remarked that further Go-level value tracking is out of scope for the PR

### [PR microsoft/TypeScript#64793](https://github.com/microsoft/TypeScript/pull/64793) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Batch allocations of common checker types**

*Use typed arenas to batch-allocate common checker types, reducing small-object allocation overhead and preserving independent block collection.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64794](https://github.com/microsoft/TypeScript/pull/64794) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Presize checker type\-list cache keys**

*Reserve known encoded size for checker type-list cache keys to reduce temporary hash buffer allocations and improve memory efficiency.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64795](https://github.com/microsoft/TypeScript/pull/64795) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid allocating normalized types on interning cache hits**

*Eliminate unnecessary allocations in union and intersection normalization by reusing cached equivalent types to reduce memory usage.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64796](https://github.com/microsoft/TypeScript/pull/64796) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compact type mappers and coallocate inference mapper storage**

*Replace mapper interfaces with concrete kind headers and coallocate inference context’s two mappers to reduce allocations.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64797](https://github.com/microsoft/TypeScript/pull/64797) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Move cold value\-symbol links out of the hot records**

*Relocate cold value-symbol link fields into an optional arena-backed sidecar to shrink hot records and reduce memory usage.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64798](https://github.com/microsoft/TypeScript/pull/64798) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Recover concrete AST nodes from their embedded headers**

*Embed AST node headers at offset zero with kind checks to shrink header size, boost memory efficiency, and omit non-debug DWARF.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64799](https://github.com/microsoft/TypeScript/pull/64799) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep optional symbol tables out of hot symbol records**

*Move optional symbol tables into arena-batched metadata to shrink symbol records and lower heap and GC overhead*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64800](https://github.com/microsoft/TypeScript/pull/64800) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Move optional structured type shape into cold storage**

*Move optional type metadata into cold storage to reduce StructuredType memory footprint and improve GC performance.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64801](https://github.com/microsoft/TypeScript/pull/64801) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep optional type\-node and signature state out of hot records**

*Relocate optional outer type parameters and signature state out of hot records to reduce memory usage.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64802](https://github.com/microsoft/TypeScript/pull/64802) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Bound arena retention by bytes instead of object count**

*Use 512-byte arena chunks instead of fixed object counts to reduce memory retention and GC at cost of more allocations.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64803](https://github.com/microsoft/TypeScript/pull/64803) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use paged indexes for type\-node and signature caches**

*Replace AST pointer maps with paged indexes keyed by stable node IDs for type-node and signature caches to reduce memory usage.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64804](https://github.com/microsoft/TypeScript/pull/64804) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reuse ordered property counts during intersection reduction**

*Reuse bounded, checker-local property-count tables in intersection reduction to reduce allocated memory by 26.6%, allocations by 7.6%, and CLI instructions by 8.9%.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64804#issuecomment-6162382028) **DanielRosenwasser** said "Weird that we need a free list. Maybe it's worth exploring a pool of 16, a bitset that indicates which one is currently in use, and just allocates if they're all occupied."

### [Issue microsoft/TypeScript#64807](https://github.com/microsoft/TypeScript/issues/64807) (Closed, `Working as Intended`)

**\`\-\-stableTypeOrdering\`: \`unknown \|\| {}\` is assignable to \`Record\<string, T\>\` in 6\.0\.3 with the option, and not in 7\.0\.2 nor in 6\.0\.3 without it**

*With --stableTypeOrdering, TS 6.0.3 allows unknown||{} to be assigned to Record<string, number>, unlike TS 6.0.3 without it and TS 7.0.2.*

 * created by **MARCROCK22**
 * [later](https://github.com/microsoft/TypeScript/issues/64807#issuecomment-6166781526) **Andarist** said "FWIW, the diff between TS 6 and TS 7 is this: https://github.com/microsoft/typescript-go/pull/1603 and it's an intended change. It was just not backported to TS 6 (and my bet is that it won't be)."

### [PR microsoft/TypeScript#64808](https://github.com/microsoft/TypeScript/pull/64808) (Open, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Share a single cache for all type relationships and propagate results hierarchically**

*Proposes consolidating separate type relationship caches into a unified hierarchical cache to reduce redundancy and overlap in cached results.*

 * created by **DanielRosenwasser**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6157839924) **DanielRosenwasser** requested the typescript-bot to run top1000 tests, dt tests, and perf tests
 * [today](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6157841156) **typescript-automation[bot]** started jobs and posted build statuses for 'test top1000' and 'perf test this'
 * [today](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6158218269) **typescript-automation[bot]** reported the requested perf run results
 * [today](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6159309899) **typescript-automation[bot]** reported that running tsc on the top 1000 repos showed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6159953622) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6159954762) **typescript-automation[bot]** started jobs and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6160267025) **typescript-automation[bot]** posted the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6162005757) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6162006945) **typescript-automation[bot]** reported that perf test jobs had started and included status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6162361810) **typescript-automation[bot]** reported the results of the requested performance run including compiler metrics such as errors, symbols, types, and memory usage

### [Issue microsoft/TypeScript#64809](https://github.com/microsoft/TypeScript/issues/64809) (Closed, `Declined`)

**TS 7: backport typescript\-go\#4665 to a 7\.0\.x patch release; the same bug also drops declaration emit**

*Dependent .d.ts files aren’t re-emitted in TypeScript 7.0.2’s isolatedModules incremental build after global-scope changes, so microsoft/typescript-go#4665 must be backported to a 7.0.x patch release.*

 * created by **Nabil372**

