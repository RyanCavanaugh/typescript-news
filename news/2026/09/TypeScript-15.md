# Report for 2026-09-15 (Tuesday, September 15th, 2026)

20 different users commented on 51 different issues.

## Recommended Actions

 * Response Recommended
    * @milkcask confirmed that the issue still reproduces on 7.1.0-dev in [microsoft/TypeScript#59715](https://github.com/microsoft/TypeScript/issues/59715#issuecomment-5690897872)
    * @typescript-automation[bot] asked to review the tsc comparison results in [microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688565223)
    * @typescript-automation[bot] reported build failures from automated suite in [microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688565525)
    * @typescript-automation[bot] reported compilation errors from top 1000 repos suite in [microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688566106)
    * @typescript-automation[bot] reported build failures on tldraw/tldraw in [microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688566504)
    * @typescript-automation[bot] provided performance run results as requested in [microsoft/TypeScript#64220](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5686328009)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript#64232](https://github.com/microsoft/TypeScript/pull/64232#issuecomment-5685832393)
    * @devanshj provided a minimal reproducible example showing the compile error in [microsoft/TypeScript#64252](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5684134246)
    * @typescript-automation[bot] provided test results highlighting infrastructure failures in [microsoft/TypeScript#64280](https://github.com/microsoft/TypeScript/pull/64280#issuecomment-5685304499)
    * @typescript-automation[bot] provided requested performance results in [microsoft/TypeScript#64280](https://github.com/microsoft/TypeScript/pull/64280#issuecomment-5685339740)
    * @typescript-automation[bot] provided test results in [microsoft/TypeScript#64280](https://github.com/microsoft/TypeScript/pull/64280#issuecomment-5685988647)

## Activity Summary

### [Issue microsoft/TypeScript#49150](https://github.com/microsoft/TypeScript/issues/49150) (Closed, `Bug`, `Help Wanted`, `Domain: Something Else`)

**\`ts\.convertToBase64\` does not handle emojis**

*ts.convertToBase64 fails to accurately encode emojis into Base64, yielding incorrect results.*

 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/49150#issuecomment-1439353535) **bartlomieju** said "Sorry for the confusion! I missed that we no longer use TSC for emitting source maps."
 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/49150#issuecomment-1439355920) **dsherret** said "@jakebailey thanks! If they are going away then maybe I will try again (https://github.com/microsoft/TypeScript/pull/21021) 😄"
 * **RyanCavanaugh** added label `Domain: Something Else`
 * [today](https://github.com/microsoft/TypeScript/issues/49150#issuecomment-5688865824) **RyanCavanaugh** said "Closing as we're not updating the 6.0 API"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#50195](https://github.com/microsoft/TypeScript/issues/50195) (Closed, `Bug`, `Rescheduled`, `Domain: Crashes`, **navya9singh**)

**Maximum call stack size exceeded**

*Compiling a large generated TypeScript project with generics causes the compiler to crash with "Maximum call stack size exceeded".*

 * (2.1 years ago) **RyanCavanaugh** added label `Domain: Crashes`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [today](https://github.com/microsoft/TypeScript/issues/50195#issuecomment-5688834009) **RyanCavanaugh** noted that the linked repro was too large, did not crash in 7.0+, encountered config errors in 6.0, and requested new self-contained isolated repros
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#59715](https://github.com/microsoft/TypeScript/issues/59715) (Open, `Bug`, `Help Wanted`, `Domain: check: Control Flow`)

**Type is not referred correctly in the while loop**

*After TypeScript 4.3.5, nested instanceof checks in a while loop no longer correctly narrow HTMLElement subclass types.*

 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/59715#issuecomment-2512320815) **nmain** described that behavior before #43183 still failed with an extra layer and provided a playground example
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/59715#issuecomment-2670059370) **milkcask** suggested tracking blocks/flows with CheckMode or adding a new flag since behavior before #43183 couldn’t be restored, and noted nmain’s observation that the checker infers `All | null` despite it being explicit
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [today](https://github.com/microsoft/TypeScript/issues/59715#issuecomment-5690897872) **milkcask** confirmed reproduction on 7.1.0-dev and noted that currentParent narrowed to Parent | GrandParent and that behavior remained unchanged from the 5.x checker
 * [today](https://github.com/microsoft/TypeScript/issues/59715#issuecomment-5691815584) **milkcask** described adding a reentered flag to the flow loop stack and using a fixed-point iteration of the antecedent pass to ensure correct type approximation

### [PR microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types**

*Add support for a 'not T' negated type operator with canonical simplification rules and enhanced control flow handling*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5631883925) **LukeAbby** described bugs in fresh literal type exactness logic and provided reproduction examples
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5687527325) **weswigham** described the conservative core implementation and outlined five planned PRs including control flow in false assertion branches, no control flow freshness for negations, driving type facts with negations, negated substitutions in conditional type false branches, and swapping Extract/Exclude to intersections
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5687528452) **typescript-automation[bot]** posted a status update with build jobs starting and links to results
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688565223) **typescript-automation[bot]** reported build failures in advaitpaliwal/feynman when comparing main and pull/63926 merge and asked for review
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688565365) **typescript-automation[bot]** provided additional compile errors from the top 1000 repos suite, noting that 85 of 329 projects failed to build and listing TS2322 type assignment errors in corsairdev/corsair and related packages
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688565525) **typescript-automation[bot]** reported build failures and type errors for darkreader/darkreader and date-fns/date-fns from running the top 1000 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688565670) **typescript-automation[bot]** reported build errors for earendil-works/pi and EKKOLearnAI/hermes-studio from the top 1000 repos suite run
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688565822) **typescript-automation[bot]** reported TypeScript build errors for krillinai/OpenCreator from the top 1000 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688565977) **typescript-automation[bot]** reported TypeScript build failures and type errors in MemTensor/MemOS from the top 1000 repos test suite
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688566106) **typescript-automation[bot]** reported compilation errors in nexu-io/open-design from running the top 1000 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688566241) **typescript-automation[bot]** reported multiple TypeScript type errors in presenton/presenton from the top 1000 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688566356) **typescript-automation[bot]** reported more changes from running the top 1000 repos suite, showing TS2322 errors in several tsconfig files for stablyai/orca
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688566504) **typescript-automation[bot]** reported build errors for tldraw/tldraw, showing TS2322 type assignment failures in multiple files
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688566632) **typescript-automation[bot]** reported type errors in trailhq/Graft, triggerdotdev/trigger.dev, and umami-software/umami from running the top 1000 repos suite

### [PR microsoft/TypeScript#64191](https://github.com/microsoft/TypeScript/pull/64191) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**, **jakebailey**)

**Fix FSEvents routing for differently cased watch paths**

*Modify FSEvents routing logic to handle watch paths that differ only by case correctly.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64191#issuecomment-5588265990) **jakebailey** described experimenting with Astra over the weekend, noting that it fixed everything; observed incorrect path casing in tspath; stated intention to keep fswatch self-contained and possibly reuse performance improvements for tspath’s ContainsPath checks
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64191#issuecomment-5588316346) **jakebailey** mentioned that kqueue on macOS also had the filename case sensitivity problem and that macOS was the only BSD with canonically insensitive filenames
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64191#issuecomment-5591021718) **jakebailey** noted that the fix resolved fswatch itself but its callers’ path checks could still cause confusion and investigated further
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64210](https://github.com/microsoft/TypeScript/pull/64210) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix case sensitivity fswatch and users**

*Implement system-based case matching and a watchalias package on macOS to correctly handle case sensitivity in file watchers.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64210#issuecomment-5691848244) **jakebailey** said "This is nasty, I'm going to try and simplify it, but I think it can only be simpler by doing less precise tracking..."

### [PR microsoft/TypeScript#64215](https://github.com/microsoft/TypeScript/pull/64215) (Closed, `Author: Team`, `For Uncommitted Bug`, **johnfav03**)

**Fix race in write loop marshal recovery test**

*Marshal recovery test for the write loop exhibits a race condition and requires a fix.*

 * (6 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **johnfav03**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64220](https://github.com/microsoft/TypeScript/pull/64220) (Open, `For Milestone Bug`, **johnfav03**)

**Schedule tsc \-b projects by dependency depth to reduce builder idle time on upstream projects**

*Sort topologically built TypeScript projects by dependency depth rather than references-first to reduce builder idle time and speed up large monorepo builds.*

 * (yesterday) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5685828576) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5685830448) **typescript-automation[bot]** reported build jobs starting and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5686328009) **typescript-automation[bot]** posted performance run results for tsc comparing baseline to pr

### [PR microsoft/TypeScript#64226](https://github.com/microsoft/TypeScript/pull/64226) (Open, `For Uncommitted Bug`)

**fix: report optional\-chain tagged templates after non\-null assertions**

*Ensure tagged template expressions following non-null assertions in optional chains correctly trigger TS1358 errors.*

 * created by **camc314**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64226#issuecomment-5616742706) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64226#issuecomment-5685276366) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64226#issuecomment-5685277381) **typescript-automation[bot]** posted automated CI build status update with links for test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/64226#issuecomment-5685773299) **typescript-automation[bot]** posted performance run results as requested, including comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64226#issuecomment-5686441164) **typescript-automation[bot]** reported user test results showing infrastructure failures but otherwise everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64226#issuecomment-5686691128) **typescript-automation[bot]** shared results of compiling top 400 repos comparing main and the pull request merge and reported everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64226#issuecomment-5692273915) **camc314** noted missing logs and assumed they were fine

### [Issue microsoft/TypeScript#64231](https://github.com/microsoft/TypeScript/issues/64231) (Open, `Bug`)

**Parser misinterprets async\(\) calls in conditional expressions as async arrow functions**

*TypeScript parser misinterprets calls to a function named async in ternary expressions as async arrow functions, causing syntax errors.*

 * **DanielRosenwasser** added to milestone `TypeScript 7.1.0 Beta`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64231#issuecomment-5662369126) **anbv29** asked if they could work on the issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64231#issuecomment-5668025041) **RyanCavanaugh** said "@anbv29 Why do you want to open a third PR for this?"
 * [later](https://github.com/microsoft/TypeScript/issues/64231#issuecomment-5696975059) **anbv29** said "I mea it still has a label of bug on it, and I love working on js so yeah!"

### [PR microsoft/TypeScript#64232](https://github.com/microsoft/TypeScript/pull/64232) (Open, `For Backlog Bug`)

**Fixed detection of optional chains containing a reference**

*Fixes detection of optional chains containing references in the TypeScript compiler.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64232#issuecomment-5685291047) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64232#issuecomment-5685292771) **typescript-automation[bot]** started CI jobs and updated statuses and result links for test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/64232#issuecomment-5685832393) **typescript-automation[bot]** provided the requested perf run results
 * [today](https://github.com/microsoft/TypeScript/pull/64232#issuecomment-5686577107) **typescript-automation[bot]** reported infrastructure failures in two package installs and one git clone and indicated that everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64232#issuecomment-5687050739) **typescript-automation[bot]** reported that everything looked good after running the top 400 repos with tsc comparing main and refs/pull/64232/merge

### [Issue microsoft/TypeScript#64240](https://github.com/microsoft/TypeScript/issues/64240) (Closed, `Bug`, **andrewbranch**)

**API panics when serializing number literal types with \`\+Infinity\` and \`\-Infinity\`**

*TypeScript’s unstable sync API panics when serializing number literal types representing +Infinity or -Infinity.*

 * (yesterday) **RyanCavanaugh** set milestone to `Backlog`, and assigned to **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64240#issuecomment-5675951235) **auvred** tested resolution of NaN in enum constants and added support for NaNs
 * (later) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64241](https://github.com/microsoft/TypeScript/pull/64241) (Closed, `For Milestone Bug`, **andrewbranch**)

**Properly serialize \`\+Infinity\`, \`\-Infinity\`, and \`NaN\` number literal type values in API**

*Implement correct serialization of +Infinity, -Infinity, and NaN number literals in the API.*

 * (yesterday) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript/pull/64241#issuecomment-5697116355) **auvred** said "Looks like the workflows haven't started"
 * (later) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64252](https://github.com/microsoft/TypeScript/pull/64252) (Open, `For Backlog Bug`)

**Fix reverse mapped type inference when all properties are context\-sensitive**

*Improve reverse mapped type inference to correctly handle scenarios where every property is context-sensitive.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5670687521) **typescript-automation[bot]** reported the user test results comparing main and PR merge, noting infrastructure failures but otherwise all good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5670695144) **typescript-automation[bot]** provided the perf run results for the requested comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5680822580) **devanshj** reported that xstate broke with 14 new errors and said they would investigate whether the break is acceptable or adjust the PR accordingly
 * [today](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5684134246) **devanshj** provided a minimal TypeScript snippet that compiled in main but failed in the PR, and noted that removing a type constraint resolved the issue

### [PR microsoft/TypeScript#64266](https://github.com/microsoft/TypeScript/pull/64266) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Improve performance of batched requests**

*Automatically batch requests across all API endpoints with code generation, remove hardcoded entrypoints, switch to struct-of-arrays layout for better performance.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64266#issuecomment-5687798292) **weswigham** explained that they updated the server to support efficient batch requests with shared parameters for all protocol methods, avoiding maintaining separate singular and bulk wire protocol implementations

### [PR microsoft/TypeScript#64268](https://github.com/microsoft/TypeScript/pull/64268) (Open, `For Milestone Bug`, **RyanCavanaugh**)

**lib: ZonedDateTime\.toLocaleString must not accept a timeZone option**

*Restrict ZonedDateTime.toLocaleString’s options type to exclude timeZone by introducing a specialized interface extending Intl.DateTimeFormatOptions.*

 * created by **lukiod**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64268#issuecomment-5685600903) **Sector6759** suggested defining the ZonedDateTimeToLocaleStringOptions interface by extending Intl.DateTimeFormatOptions and setting timeZone to never

### [Issue microsoft/TypeScript#64273](https://github.com/microsoft/TypeScript/issues/64273) (Closed)

**Crash: unexpected TypeElement: KindPropertyDeclaration**

*A nightly TypeScript compiler build crashes with unexpected TypeElement KindPropertyDeclaration when printing a private interface method*

 * created by **YuanchengJiang**
 * [today](https://github.com/microsoft/TypeScript/issues/64273#issuecomment-5680374232) **a-tarasyuk** said "@RyanCavanaugh, it seems the labels should be extended with a new crash-on-invalid label 😄 "
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64275](https://github.com/microsoft/TypeScript/pull/64275) (Closed, `For Uncommitted Bug`)

**fix\(64273\): fix declaration emit crash on private method signatures**

*A crash occurring during declaration file emission due to private method signatures has been resolved.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64277](https://github.com/microsoft/TypeScript/pull/64277) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Remove FS\(\)\.WalkDir**

*Remove FS().WalkDir from the virtual filesystem due to lack of usage and caching issues.*

 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64277#issuecomment-5684115534) **andrewbranch** said "I'll wait for #64269 to merge."
 * [today](https://github.com/microsoft/TypeScript/pull/64277#issuecomment-5687922050) **andrewbranch** said "Never mind, #64285 could use the helper."
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64278](https://github.com/microsoft/TypeScript/issues/64278) (Open, `Possible Improvement`)

**enhance: Add tests for premature caching of contextual parameter types**

*Add regression tests to cover premature caching of contextually typed parameters when their types widen during default value checking.*

 * created by **luchenxu73**
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/64278#issuecomment-5685058818) **RyanCavanaugh** said "Sure, go for it"

### [Issue microsoft/TypeScript#64279](https://github.com/microsoft/TypeScript/issues/64279) (Closed, **jakebailey**, **Copilot**)

**JSDoc \`@type\` on a function: the type in a type predicate is never checked \(unused \`@import\` reported, missing names not reported\)**

*TypeScript 7.0.2+ erroneously flags imported types used solely in JSDoc @type function type predicates as unused, causing TS6196 errors.*

 * created by **ljharb**
 * [today](https://github.com/microsoft/TypeScript/issues/64279#issuecomment-5686218786) **arslivinski** explained that TS 7 JSDoc uses @param and @return for function statements and @type for overloading, and that arrow functions or function expressions can use @type

### [PR microsoft/TypeScript#64280](https://github.com/microsoft/TypeScript/pull/64280) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Various type comparison fixes**

*Fix various type comparison issues based on tests and prior feedback, now applied in version 7.1.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64280#issuecomment-5684911426) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64280#issuecomment-5684912874) **typescript-automation[bot]** provided automated build status updates for multiple test commands
 * [today](https://github.com/microsoft/TypeScript/pull/64280#issuecomment-5685223857) **DanielRosenwasser** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64280#issuecomment-5685225439) **typescript-automation[bot]** posted CI build status updates for test jobs
 * [today](https://github.com/microsoft/TypeScript/pull/64280#issuecomment-5685304499) **typescript-automation[bot]** reported infrastructure failures and otherwise successful test results
 * [today](https://github.com/microsoft/TypeScript/pull/64280#issuecomment-5685339740) **typescript-automation[bot]** posted requested perf run results with a detailed comparison table
 * [today](https://github.com/microsoft/TypeScript/pull/64280#issuecomment-5685703731) **typescript-automation[bot]** noted that running tsc on the top 400 repos comparing `main` and the PR merge produced good results
 * [today](https://github.com/microsoft/TypeScript/pull/64280#issuecomment-5685727134) **typescript-automation[bot]** posted performance run results with detailed comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64280#issuecomment-5685988647) **typescript-automation[bot]** reported that user tests comparing main and the pull request merge had two package install failures and one git clone failure but otherwise passed
 * [today](https://github.com/microsoft/TypeScript/pull/64280#issuecomment-5686513873) **typescript-automation[bot]** reported that results of running the top 400 repos with tsc comparing main and the PR looked good
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64281](https://github.com/microsoft/TypeScript/pull/64281) (Open, `For Backlog Bug`)

**test: cover contextual parameter type caching**

*Add new TypeScript tests to cover and verify contextual parameter type caching*

 * created by **luchenxu73**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64281#issuecomment-5685136889) **luchenxu73** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64282](https://github.com/microsoft/TypeScript/issues/64282) (Closed)

**Dev Container postCreateCommand can hang when npx hereby runs concurrently with npm ci**

*Concurrent postCreateCommand steps can cause npx hereby to hang when npm ci hasn’t completed.*

 * created by **noamaanMulla-03**
 * [today](https://github.com/microsoft/TypeScript/issues/64282#issuecomment-5686190500) **DanielRosenwasser** pointed out that the Herebyfile should list pprof in the tools map and suggested splitting install steps into separate JSON5 entries
 * [today](https://github.com/microsoft/TypeScript/issues/64282#issuecomment-5686292072) **jakebailey** said "You can just do go tool pprof. The only reason to install it separately is to get bugfixes from upstream early."
 * [today](https://github.com/microsoft/TypeScript/issues/64282#issuecomment-5688408457) **noamaanMulla-03** updated the branch to split the independent Go dependency setup, removed the separate pprof install in favor of go tool pprof, and offered to raise a PR if acceptable

### [PR microsoft/TypeScript#64283](https://github.com/microsoft/TypeScript/pull/64283) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update dependencies**

*Update all dependencies to vsce v4 to drop over 150 modules, with an adm-zip CVE fix pending*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64284](https://github.com/microsoft/TypeScript/pull/64284) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add missing \`generate\` calls to \`validate\`**

*Add general, extension, and vendor generate steps to the validate command to catch CI diffs before testing.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64285](https://github.com/microsoft/TypeScript/pull/64285) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Move requestFileSystem into project**

*Move the requestFileSystem API into the project module in a smaller, more concrete refactoring.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64286](https://github.com/microsoft/TypeScript/pull/64286) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update main for TS7 tagged releases**

*Prepare the main branch for TypeScript 7 tagged releases in anticipation of the upcoming 7.0.3 release.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64287](https://github.com/microsoft/TypeScript/pull/64287) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update release\-7\.0 for TS7 tagged releases**

*Update the release-7.0 branch with essential changes required for TS7 tagged releases.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64288](https://github.com/microsoft/TypeScript/pull/64288) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add macOS entitlements to release binaries**

*Add macOS entitlements to the 7.0.3 release binaries following the implementation on main after version 7.0.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64289](https://github.com/microsoft/TypeScript/pull/64289) (Open, `For Uncommitted Bug`)

**Fix import type code fix comment duplication**

*‘import type’ quick fix avoids comment duplication by inserting ‘type’ directly after ‘import’ instead of rebuilding the declaration*

 * created by **noamaanMulla-03**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64289#issuecomment-5688656724) **noamaanMulla-03** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64290](https://github.com/microsoft/TypeScript/issues/64290) (Open, `Design Notes`)

**Design Meeting Notes, 2026\-09\-15**

*Propose deferring constraint checks and returning uninstantiated type parameters to improve TypeScript's inference for circular self-referential values.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Design Notes`

### [PR microsoft/TypeScript#64291](https://github.com/microsoft/TypeScript/pull/64291) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Move overlay management and filtering up the FS stack to allow requestFileSystems to override LSP overlays**

*Relocate overlay management and filtering out of SnapshotFS into higher-level file system layers to allow requestFileSystems to override LSP overlays*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64291#issuecomment-5689607056) **andrewbranch** said "Review race: you may have fixed some of those while I was writing it up"
 * [today](https://github.com/microsoft/TypeScript/pull/64291#issuecomment-5689646150) **weswigham** expressed an opinion that host symlinks should resolve to editor overlays and noted intent to test it
 * (later) **weswigham** closed the issue

### [PR microsoft/TypeScript#64292](https://github.com/microsoft/TypeScript/pull/64292) (Closed, `For Uncommitted Bug`, **andrewbranch**, **Copilot**)

**Implement Program resolution mode APIs**

*Add and expose Program.getModeForUsageLocation and getModeForResolutionAtIndex APIs in TypeScript with protocol handlers, async/sync/generator support, index resolution, and validation.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64292#issuecomment-5700036435) **Copilot** notified that custom setup steps failed during the Copilot code review run and suggested fixing the configuration and re-requesting a review

### [PR microsoft/TypeScript#64293](https://github.com/microsoft/TypeScript/pull/64293) (Closed, `For Uncommitted Bug`)

**Fix CompareStringsCaseInsensitive to fold to uppercase**

*Change Go's CompareStringsCaseInsensitive to fold runes to uppercase instead of lowercase to match upstream behavior*

 * created by **winklemad**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64293#issuecomment-5691536676) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64293#issuecomment-5691546220) **jakebailey** said "Can you please show a place where this matters that isn't just a hyperfocused unit test? Thanks."
 * [today](https://github.com/microsoft/TypeScript/pull/64293#issuecomment-5691855246) **winklemad** closed the issue and explained that the only difference is display-only in workspace-symbol ordering on match-score ties and not worth fixing
 * (today) **winklemad** closed the issue

### [PR microsoft/TypeScript#64294](https://github.com/microsoft/TypeScript/pull/64294) (Closed, `For Uncommitted Bug`)

**Fix index\-out\-of\-range panic in glob\.Match on separator\-terminated input**

*glob.Match panics when matching separator-terminated strings because the slash-case loop lacks a bounds check*

 * created by **winklemad**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64294#issuecomment-5691556404) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64294#issuecomment-5691571148) **jakebailey** noted that a bugfix was unnecessary without a real end-to-end case and reminded the contributor that bulk agent-driven contributions are prohibited after submitting multiple PRs in quick succession
 * [today](https://github.com/microsoft/TypeScript/pull/64294#issuecomment-5691629401) **winklemad** apologized and acknowledged that two AI-assisted PRs triggered the policy, explained they were separate bugs, and closed both PRs due to lack of an end-to-end case
 * (today) **winklemad** closed the issue

### [PR microsoft/TypeScript#64295](https://github.com/microsoft/TypeScript/pull/64295) (Open, `For Backlog Bug`)

**Iterate antecedent pass so self\-assignment in a loop correctly narrows**

*Fix narrowing for union-typed variables self-assigned in loops by iteratively re-running the antecedent pass until full convergence.*

 * created by **milkcask**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#64296](https://github.com/microsoft/TypeScript/issues/64296) (Closed, `Bug`)

**SEGV nil pointer dereference in tsc/internal/checker/checker\.go**

*TypeScript compiler panics with a nil pointer dereference in checker.go when processing an import declaration conflicting with a type alias.*

 * created by **YuanchengJiang**

### [PR microsoft/TypeScript#64297](https://github.com/microsoft/TypeScript/pull/64297) (Closed, `For Backlog Bug`)

**fix\(64296\): prevent crash when checking merged import aliases**

*Prevent compiler crashes when type checking merged import aliases.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64298](https://github.com/microsoft/TypeScript/pull/64298) (Closed, `For Uncommitted Bug`)

**Fix dev container post\-create command ordering**

*Combine npm ci and npx hereby install-tools in devcontainer, keep Go module and Graphviz separate, and use go tool pprof.*

 * created by **noamaanMulla-03**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

