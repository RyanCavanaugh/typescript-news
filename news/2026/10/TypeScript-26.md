# Report for 2026-10-26 (Monday, October 26th, 2026)

19 different users commented on 47 different issues.

## Recommended Actions

 * Response Recommended
    * @Amatewasu asked why no other users reported this issue in [microsoft/TypeScript#64423](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-6446103670)
    * @ebidel reported that postcss-selector-parser typings triggered TS5115 errors despite previous fixes in [microsoft/TypeScript#64605](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6426420558)
    * @blt-r offered to submit a PR to implement warning semantics in [microsoft/TypeScript#64932](https://github.com/microsoft/TypeScript/issues/64932#issuecomment-6427493602)

## Activity Summary

### [Issue microsoft/TypeScript#35909](https://github.com/microsoft/TypeScript/issues/35909) (Open, `Suggestion`, `Awaiting More Feedback`)

**Can't evaluate equality of symbols made by Symbol\.for**

*TypeScript treats Symbol.for calls as distinct types, causing erroneous type errors on equality comparisons and assignments.*

 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-2585209754) **yuhr** reposted an excerpt from issue #60944 explaining the use-case for non-unique symbol keys to support multiple library versions and the compile-time issues with string keys
 * [20 weeks ago](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-4626919034) **lygstate** said "It's a bug, can it fixed? As Symbol.for("literal") basically act like "literal" with symbol attribute"
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-6277055373) **michaelfig** encouraged people following the issue to review PR #64451 and provide feedback
 * [later](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-6438798683) **Richiban** proposed adding a literal symbol type in TypeScript for matching specific sentinels

### [Issue microsoft/TypeScript#40604](https://github.com/microsoft/TypeScript/issues/40604) (Open, `Suggestion`, `Awaiting More Feedback`)

**List @deprecated strikethroughs in Problems tab**

*Add an optional setting to list TypeScript @deprecated strikethroughs in the Problems tab for easier tracking*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/40604#issuecomment-2707242430) **sehrgut** said "I found this when looking for the setting I assumed to already exist to enable deprecation warnings. It's surprising to me that this isn't base functionality, and I hope we get it included."
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/40604#issuecomment-2777729588) **AstroGD** said "I agree - Would love to see this as it would make development much easier"
 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/40604#issuecomment-3838839787) **X-lem** said "2026... this would be very helpful. Upgrading some dependencies and going file by file sucks."
 * [today](https://github.com/microsoft/TypeScript/issues/40604#issuecomment-6423006402) **oj4b** said "would be an improvement for sure"

### [Issue microsoft/TypeScript#49584](https://github.com/microsoft/TypeScript/issues/49584) (Open, `Suggestion`, `Awaiting More Feedback`)

**Narrowing \`typeof\` operator comparison by type**

*Enable TypeScript to narrow an unknown variable’s type when comparing its typeof result against another union-typed value.*

 * (4.3 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [3.9 years ago](https://github.com/microsoft/TypeScript/issues/49584#issuecomment-1318651117) **graphemecluster** said "Related: #28144"
 * [today](https://github.com/microsoft/TypeScript/issues/49584#issuecomment-6422030399) **smichelForHire** pointed out a narrower sub-case and provided example code and playground link

### [Issue microsoft/TypeScript#64423](https://github.com/microsoft/TypeScript/issues/64423) (Open, `Needs More Info`)

**\[7\.0 regression\] Unbounded type relation expansion during variance computation causes OOM**

*TypeScript 7.0.2's variance computation causes unbounded type relation expansion leading tsc to hang and exhaust memory.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-5828271795) **Amatewasu** provided TypeScript compiler output showing a fatal heap out of memory error
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-5828937397) **Amatewasu** reported LLM-generated investigation findings including measurements and a minimal reproduction for a TypeScript 7.0.2 OOM issue
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-5870461095) **Amatewasu** reported a second independent OOM trigger in TypeScript 7 when calling methods on three/tsl nodes and supplied a minimal reproduction with dependency versions and stack trace
 * [later](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-6446103670) **Amatewasu** said "I wonder why no other people are having this issue. I would have expected other people to comment on this issue?"

### [Issue microsoft/TypeScript#64605](https://github.com/microsoft/TypeScript/issues/64605) (Open, `Needs Investigation`, **gabritto**)

**TS5115 in published Zod 4\.5–4\.6 types after \#64372**

*Zod 4.5.0–4.6.5 z.json() types cause TS5115 infinite circularity errors in TypeScript 7.1 nightlies after PR #64372, impacting ~62M weekly downloads.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6053406731) **RedesignedRobot** traced the cause of a recursive member resolution issue introduced by #64372, proposed a fix that preserves declared members on a stack during inheritance resolution, reported passing tests and a cleaned-up baseline, and offered to open a PR
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6084855435) **rsnodgrass** confirmed the issue reproduced with TypeScript 7.1.0-dev and Zod 4.6.5, provided minimal reproduction code and version comparison, and requested review
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6299246463) **salemkode** confirmed reproduction on typescript@7.1.0-beta with a standalone zod example and provided reproduction steps and error output
 * [today](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6426420558) **ebidel** demonstrated that postcss-selector-parser's type definitions still produced TS5115 infinite circular instantiation errors in recent builds and provided reproduction steps and build comparisons

### [Issue microsoft/TypeScript#64849](https://github.com/microsoft/TypeScript/issues/64849) (Open, `Needs Investigation`)

**\[ServerErrors\]\[JavaScript\] main**

*The main JavaScript pipeline run analyzing 300 TypeScript repositories reported server errors, timeouts, and unknown failures.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64849#issuecomment-6226258189) **typescript-automation[bot]** reported a server connection closed prematurely error for apache/pouchdb and included affected repo details and repro steps
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64849#issuecomment-6226258746) **typescript-automation[bot]** reported a server connection closed prematurely error and provided affected repo details, logs, last requests, and repro steps
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64849#issuecomment-6226259334) **typescript-automation[bot]** logged a panic handling a textDocument/diagnostic request and reported flaky diagnostics with stack trace for chartjs/Chart.js
 * **RyanCavanaugh** added label `Needs Investigation`

### [Issue microsoft/TypeScript#64851](https://github.com/microsoft/TypeScript/issues/64851) (Open, `Needs Investigation`)

**\[ServerErrors\]\[TypeScript\] main**

*The TypeScript main Azure pipeline run encountered errors, timeouts, and clone failures analyzing 300 GitHub repos, completing 133 analyses.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64851#issuecomment-6227406949) **typescript-automation[bot]** reported a runtime panic error during textDocument/codeAction handling
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64851#issuecomment-6227407511) **typescript-automation[bot]** reported a server connection closed prematurely error and provided affected repo details, error artifacts, replay commands, recent request logs, and repro steps
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64851#issuecomment-6227408044) **typescript-automation[bot]** reported server connection closed prematurely and provided repro steps
 * **RyanCavanaugh** added label `Needs Investigation`

### [Issue microsoft/TypeScript#64882](https://github.com/microsoft/TypeScript/issues/64882) (Closed, `Bug`, **RyanCavanaugh**, **gabritto**, **Copilot**)

**7\.1 regression: import resolving to a non\-module file falls back to a pattern ambient module instead of TS2306**

*TypeScript 7.1 incorrectly applies a pattern ambient module for imports resolving to non-module files instead of reporting TS2306.*

 * (5 days ago) **RyanCavanaugh** added label `Bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript#64884](https://github.com/microsoft/TypeScript/pull/64884) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **gabritto**)

**Preserve non\-module errors for imports without attributes**

*Ensure imports without attributes still produce non-module errors and avoid unintended ambient module resolution*

 * created by **Andarist**
 * (6 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** assigned to **gabritto**, **RyanCavanaugh**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript#64905](https://github.com/microsoft/TypeScript/pull/64905) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Restore TS2306 for resolved non\-module files matching ambient patterns**

*Restore TS2306 error reporting for script imports incorrectly matched to ambient wildcard modules due to import-attribute support regression.*

 * (5 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64905#issuecomment-6323418549) **Andarist** said "@RyanCavanaugh there is already an approved PR for this here: https://github.com/microsoft/TypeScript/pull/64884"
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript#64916](https://github.com/microsoft/TypeScript/pull/64916) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Make symbol tables insertion\-ordered**

*Use insertion-ordered symbol tables to eliminate nondeterministic iteration and ensure consistent diagnostics, declaration emissions, and type ID assignments.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6329431244) **typescript-automation[bot]** provided performance run results to @jakebailey
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6329564110) **jakebailey** said "Seems like this causes nondeterminism in the tests, note the concurrent and race tests (which use multi-checker programs) erroring."
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6335492219) **Andarist** clarified that the performance and memory benefit came from the representation rather than ordering; explained testing fixes using @singleThreaded for nondeterminism; noted plans for further ordering fixes
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6424362327) **ahejlsberg** said "What's an example of when a symbol needs a key different from it's name? I didn't realize we had that happening. I just tried compiling VS Code and it doesn't seem to occur in that code base."
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6424519641) **ahejlsberg** wondered whether using an alias could shrink symbol table entries to just the symbols
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6424697797) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6424699353) **typescript-automation[bot]** said "Hey @jakebailey, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6425764179) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6425766196) **typescript-automation[bot]** reported that the perf test build had started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6430075994) **typescript-automation[bot]** said "@ahejlsberg, the perf run you requested failed. You can check the log here."
 * [later](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6439707277) **typescript-automation[bot]** provided the requested perf run results including a provisional hosted-runner comparison report for tsc

### [Issue microsoft/TypeScript#64919](https://github.com/microsoft/TypeScript/issues/64919) (Open, `Bug`, `Domain: API`)

**API: parameter documentation \(getDocumentationComment / getJsDocTags\) diverges from the classic services in TypeScript 7\.1**

*TypeScript 7.1’s programmatic API getDocumentationComment and getJsDocTags for parameters no longer return inherited JSDoc comments as the classic services did.*

 * created by **WinterYukky**
 * (today) **RyanCavanaugh** added labels `Domain: API`, `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64924](https://github.com/microsoft/TypeScript/pull/64924) (Closed, `For Backlog Bug`)

**Reuse this\-independent interface member instantiations**

*Reuse instantiations of interface members that don’t depend on `this` to avoid redundant allocations.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64924#issuecomment-6344056899) **jakebailey** said "Are there any real world codebases that hit this? Note how none of our benchmarks were affected by that other PR"
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **777genius** closed the issue

### [PR microsoft/TypeScript#64931](https://github.com/microsoft/TypeScript/pull/64931) (Open, `For Backlog Bug`)

**LS/API: align parameter JSDoc resolution with the classic services semantics**

*Align the programmatic API’s parameter JSDoc resolution with classic compiler semantics to fix override, constructor, and tag retrieval inconsistencies.*

 * created by **WinterYukky**
 * (4 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64932](https://github.com/microsoft/TypeScript/issues/64932) (Open, `Suggestion`)

**Allow content mappers emit diagnostics with different severity levels**

*Enable content mappers to emit diagnostics with varying severity levels, including warnings.*

 * created by **blt-r**
 * **RyanCavanaugh** added label `Suggestion`
 * [today](https://github.com/microsoft/TypeScript/issues/64932#issuecomment-6424617159) **RyanCavanaugh** said "Notably, TS itself does not have a 'warning' concept, so this is a heavy lift on its own"
 * [today](https://github.com/microsoft/TypeScript/issues/64932#issuecomment-6427493602) **blt-r** explained that tsc supports warnings via diagnostic.category but never produces them, noted that the pipeline treats all diagnostics as errors, advocated for adding build-failing semantics for errors vs warnings, and offered to create a PR

### [Issue microsoft/TypeScript#64947](https://github.com/microsoft/TypeScript/issues/64947) (Open, `Needs Investigation`)

**\[ServerErrors\]\[JavaScript\] main**

*The main CI pipeline detected server errors during JavaScript analysis of 300 popular TypeScript repositories, yielding 4 interesting changes, 226 unchanged results, 42 timeouts, and 28 failures.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64947#issuecomment-6376749193) **typescript-automation[bot]** reported that the server connection closed prematurely with undefined error and included affected repos, raw error text, last requests, and repro steps
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64947#issuecomment-6376749773) **typescript-automation[bot]** reported a server connection closing prematurely with undefined error and included affected repo details, artifacts, old results, and recent requests
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64947#issuecomment-6376750359) **typescript-automation[bot]** reported a server connection closed prematurely error with logs and repro steps for nosir/cleave.js
 * **RyanCavanaugh** added label `Needs Investigation`

### [Issue microsoft/TypeScript#64948](https://github.com/microsoft/TypeScript/issues/64948) (Closed, `Won't Fix`)

**Stack overflow in getEffectsSignature for long comma\-separated call chains \(e\.g\. minified bundles with allowJs\)**

*Very long comma-separated call chains in minified JS with allowJs cause getEffectsSignature to overflow the call stack.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64948#issuecomment-6379651574) **AbbasFullstack** said "I would like to fix it "
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64948#issuecomment-6379712381) **AbbasFullstack** said "Ah, I see you already have a patch ready on your branch — I'll leave this one to you. Looking forward to the fix!"
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64948#issuecomment-6379725408) **AbbasFullstack** said "If you need any type help tell me I am 24/7  for help"
 * [today](https://github.com/microsoft/TypeScript/issues/64948#issuecomment-6424079965) **RyanCavanaugh** noted the issue was fixed in version 7.0, called static analysis of heavily minified files largely useless, and recommended using a different parser for degenerate inputs
 * **RyanCavanaugh** added label `Won't Fix`

### [Issue microsoft/TypeScript#64950](https://github.com/microsoft/TypeScript/issues/64950) (Open, `Bug`)

**7\.1 regression: comparing a recursive \`\-?\` mapped type is quadratic in the number of properties and hits TS2589 \(since typescript\-go\#4820\)**

*A TypeScript 7.1 regression makes comparing recursive '-?' mapped types incur quadratic instantiation growth and hit TS2589 errors.*

 * created by **matej21**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64950#issuecomment-6385437712) **matej21** provided follow-up analysis of TypeScript 7.0/7.1 variance measurement issue, demonstrated how declaration order and -? mapped types affect soundness and performance, related it to issues #64930 and #64935, and suggested declaring variance to restore performance
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64953](https://github.com/microsoft/TypeScript/issues/64953) (Closed, `Bug`)

**Unsaved export not offered for auto\-import after reopening the importing file**

*TypeScript does not offer auto-import suggestions or import edits for functions defined in unsaved files when reopening the importing file.*

 * created by **johnsoncodehk**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64954](https://github.com/microsoft/TypeScript/issues/64954) (Open, `Bug`)

**Type annotations cause contextual \`this\` in object literal returned from an async function to be inferred as \`Promise\<This\> \| This\`**

*Async function type annotations cause object methods’ this to be inferred as a union with PromiseLike instead of the object type.*

 * created by **kanashimia**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64955](https://github.com/microsoft/TypeScript/issues/64955) (Closed, `Won't Fix`)

**Checking deeply nested array/object literals is quadratic and can hang in TS7**

*TypeScript 7’s checker exhibits quadratic time complexity for deeply nested array or object literals, causing compiler hangs on large depths.*

 * created by **qiyuhuating**
 * **RyanCavanaugh** added label `Won't Fix`
 * [today](https://github.com/microsoft/TypeScript/issues/64955#issuecomment-6424178156) **RyanCavanaugh** said "Performant checking of adversarial inputs is not a design goal."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64956](https://github.com/microsoft/TypeScript/pull/64956) (Closed, `For Uncommitted Bug`)

**Fix quadratic const\-context checking for deeply nested literals**

*Add per-node caching to Checker.isConstContext to change deeply nested literal const-context checks from quadratic time to linear time.*

 * created by **qiyuhuating**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64956#issuecomment-6394506819) **qiyuhuating** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64956#issuecomment-6424182901) **RyanCavanaugh** said "Closing as the original issue is Won't Fix."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64957](https://github.com/microsoft/TypeScript/issues/64957) (Closed, `Question`)

**type Exclude on class hierarchy resolves to never**

*Excluding a subclass from a union of structurally identical classes unexpectedly resolves to never in TypeScript.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/64957#issuecomment-6401013445) **xtnw** noted that the behavior was intended and suggested closing the bug as wontfix
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64957#issuecomment-6401436606) **irfanstract** suggested adding private fields to classes to preserve type soundness without bloating runtime properties
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64957#issuecomment-6401749375) **jcalz** offered an alternative using type-only class fields and asked for a concrete use case to justify distinguishing structurally identical types
 * **RyanCavanaugh** added label `Question`

### [Issue microsoft/TypeScript#64959](https://github.com/microsoft/TypeScript/issues/64959) (Open, `Suggestion`)

**Preserve narrowing in closures for imports that resolve to \`const\` variables**

*Extend TypeScript’s constant variable narrowing inside nested closures to apply to imported values that resolve to const bindings.*

 * created by **mcmimik**
 * **RyanCavanaugh** added label `Suggestion`

### [PR microsoft/TypeScript#64960](https://github.com/microsoft/TypeScript/pull/64960) (Closed, `For Backlog Bug`)

** Fix auto\-import not offering unsaved exports after auto\-imports were computed**

*Delay bucket cleanup until multiple files are dirty to ensure auto-import suggestions include unsaved exports*

 * created by **1-DARK**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64960#issuecomment-6401269835) **1-DARK** said "@microsoft-github-policy-service agree"
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64961](https://github.com/microsoft/TypeScript/issues/64961) (Open, `Possible Improvement`)

**/\*\* \*/ Style comments in code examples don't convert correctly**

*JavaDoc code snippets with inline /** */ comments are incorrectly rendered with escape characters instead of proper comment delimiters.*

 * created by **adligo**
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64962](https://github.com/microsoft/TypeScript/pull/64962) (Open, `For Backlog Bug`)

** Fix this type in object literal methods returned from async functions**

*Exclude PromiseLike from contextual types when returning object literals in async functions to fix incorrect this typing*

 * created by **1-DARK**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64963](https://github.com/microsoft/TypeScript/pull/64963) (Open, `For Backlog Bug`)

**fix\(64954\): exclude PromiseLike from contextual this in object literal methods**

*Exclude PromiseLike from the contextual this type in object literal methods returned by async functions.*

 * created by **servusdei2018**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64964](https://github.com/microsoft/TypeScript/pull/64964) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Speed up union subset checks by scanning sorted constituents**

*Optimize subset checks on unions by scanning sorted constituent elements to improve performance.*

 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6410410676) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6410412053) **typescript-automation[bot]** provided automated build status update including job start and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6410524011) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6420923751) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6420926160) **typescript-automation[bot]** posted automated job start status for performance tests
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6421095836) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6421749384) **DanielRosenwasser** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6421755534) **typescript-automation[bot]** reported CI build status for performance tests
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6421983049) **typescript-automation[bot]** said "@DanielRosenwasser, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6424707497) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6424709541) **typescript-automation[bot]** reported CI jobs start with status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6424773822) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6425156199) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6425158178) **typescript-automation[bot]** reported CI jobs starting and linking status URLs
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6430143516) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [later](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6439425517) **typescript-automation[bot]** reported the requested performance run results

### [Issue microsoft/TypeScript#64967](https://github.com/microsoft/TypeScript/issues/64967) (Open, `Bug`, `Domain: tsc: --incremental`)

**Incremental builds miss diagnostics after UMD declaration changes**

*Incremental TypeScript builds fail to report updated type errors when UMD namespace declarations change.*

 * created by **Dunqing**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: tsc: --incremental`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64968](https://github.com/microsoft/TypeScript/issues/64968) (Closed, `Duplicate`)

**API scanner: a \`\#\` not followed by an identifier never advances, so \`scan\(\)\` loops forever**

*TypeScript's API scanner in 7.x loops infinitely on an isolated '#' because the token position isn't advanced properly.*

 * created by **knutwannheden**
 * [today](https://github.com/microsoft/TypeScript/issues/64968#issuecomment-6417855009) **MartinJohns** said "Sounds like a duplicate of #64490."
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/64968#issuecomment-6420906710) **knutwannheden** said "Indeed. Somehow I didn't find it..."
 * (today) **knutwannheden** closed the issue

### [Issue microsoft/TypeScript#64971](https://github.com/microsoft/TypeScript/issues/64971) (Closed)

**Nit: Filename mismatch in the test case\.​**

*The test case for classMemberInitializerWithLamdaScoping4 incorrectly references classMemberInitializerWithLamdaScoping3_x.ts instead of the correct filename.*

 * created by **bvanjoi**
 * [today](https://github.com/microsoft/TypeScript/issues/64971#issuecomment-6424034934) **RyanCavanaugh** said "This level of nitpicking is not useful, please just don't."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64972](https://github.com/microsoft/TypeScript/pull/64972) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Only pre\-size the printer buffer when printing a whole file**

*The printer buffer should only be pre-sized when printing an entire file to avoid wasting memory.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64972#issuecomment-6425177155) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64972#issuecomment-6425179003) **typescript-automation[bot]** posted a status update with build start and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64972#issuecomment-6429198483) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64972#issuecomment-6430924112) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [later](https://github.com/microsoft/TypeScript/pull/64972#issuecomment-6439402180) **typescript-automation[bot]** provided the requested performance run results including comparison metrics

### [PR microsoft/TypeScript#64973](https://github.com/microsoft/TypeScript/pull/64973) (Open, `Author: Team`, `For Uncommitted Bug`, **johnfav03**)

**Fix non\-root dependency tracking in build watch mode**

*Enable build watch mode to detect changes in non-root imported files even when incremental builds are disabled.*

 * created by **johnfav03**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/pull/64973#issuecomment-6429603044) **jakebailey** described a Go test case demonstrating stale output due to coalesced directory delete/recreate events and noted a fix by removing an early return

### [Issue microsoft/TypeScript#64974](https://github.com/microsoft/TypeScript/issues/64974) (Open, `Bug`)

**7\.1: destructured parameter with a \`= {}\` default loses its contextual type \(TS7031\)**

*TypeScript 7.1 regression causes destructured parameters with a default {} to lose their contextual types and trigger implicit any errors.*

 * created by **raimonade**

### [Issue microsoft/TypeScript#64975](https://github.com/microsoft/TypeScript/issues/64975) (Closed)

**Missing namespace qualifier in \`import =\` emit across merged namespaces**

*TypeScript 7 fails to qualify import-equals aliases in merged namespaces, causing runtime ReferenceError due to missing namespace qualifier.*

 * created by **magic-akari**

### [PR microsoft/TypeScript#64976](https://github.com/microsoft/TypeScript/pull/64976) (Closed, `For Uncommitted Bug`)

**Qualify merged namespace references in import\-equals emit**

*Qualify merged namespace references in import-equals emit with explicit namespace names and add conformance tests.*

 * created by **magic-akari**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64977](https://github.com/microsoft/TypeScript/pull/64977) (Closed, `For Uncommitted Bug`)

**Fix document highlights for client URIs with unencoded characters**

*Corrects document highlight handling for client URIs containing unencoded characters.*

 * created by **yogesh968**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (later) **yogesh968** closed the issue
 * [later](https://github.com/microsoft/TypeScript/pull/64977#issuecomment-6439569062) **microsoft-github-policy-service[bot]** prompted the contributor to agree to the CLA by replying with the appropriate command

### [PR microsoft/TypeScript#64978](https://github.com/microsoft/TypeScript/pull/64978) (Open, `For Backlog Bug`)

**fix\(64974\): fix contextual typing for destructured parameter defaults**

*Correct contextual type inference for destructured parameters with default values.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

