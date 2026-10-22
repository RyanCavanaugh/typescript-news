# Report for 2026-10-16 (Friday, October 16th, 2026)

7 different users commented on 22 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#64552](https://github.com/microsoft/TypeScript/issues/64552) (Closed, `Needs Investigation`, **johnfav03**)

**\`\-\-incremental\` keeps stale diagnostics after \`lib\` or \`target\` changes in tsconfig\.json \(7\.0\.2, regression from 6\.0\.3\)**

*TypeScript 7.0.2’s --incremental compiler retains stale diagnostics after toggling tsconfig.json lib or target settings.*

 * created by **valeralebedz**
 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript#64763](https://github.com/microsoft/TypeScript/issues/64763) (Closed, `Won't Fix`)

**Parser: exponential time and memory on nested \`a \< \(b = …\)\` \(failed type argument speculation is retried\)**

*Nested 'a < (b = …)' expressions trigger exponential parsing time and memory growth in TypeScript due to retrying failed type argument speculation.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64763#issuecomment-6139366580) **moznion** said "I’ve already prepared a patch in https://github.com/microsoft/TypeScript/compare/main...moznion:TypeScript:fix/parser-type-arguments-retry, so I’d be happy to submit a pull request to fix this issue."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64763#issuecomment-6174547190) **RyanCavanaugh** mentioned receiving flack for memory usage and stated that increasing memory for degenerate code wasn't a good trade-off and they'd reevaluate if it had a legitimate use case
 * **RyanCavanaugh** added label `Won't Fix`
 * [today](https://github.com/microsoft/TypeScript/issues/64763#issuecomment-6227888376) **typescript-automation[bot]** said "This issue has been marked as "Won't Fix" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#64765](https://github.com/microsoft/TypeScript/pull/64765) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Resolve class and interface members through shared layouts**

*Introduce shared member layouts and lazy resolution for class and interface instantiations to significantly reduce memory usage and symbol creation.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6187294341) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6187296535) **typescript-automation[bot]** reported starting the perf test job and provided status and result links
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6187748114) **typescript-automation[bot]** provided performance run results for tsc comparing baseline to PR
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6226103984) **jakebailey** said "Drafting, I think Anders is redoing this"

### [Issue microsoft/TypeScript#64807](https://github.com/microsoft/TypeScript/issues/64807) (Closed, `Working as Intended`)

**\`\-\-stableTypeOrdering\`: \`unknown \|\| {}\` is assignable to \`Record\<string, T\>\` in 6\.0\.3 with the option, and not in 7\.0\.2 nor in 6\.0\.3 without it**

*With --stableTypeOrdering, TS 6.0.3 allows unknown||{} to be assigned to Record<string, number>, unlike TS 6.0.3 without it and TS 7.0.2.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64807#issuecomment-6166781526) **Andarist** said "FWIW, the diff between TS 6 and TS 7 is this: https://github.com/microsoft/typescript-go/pull/1603 and it's an intended change. It was just not backported to TS 6 (and my bet is that it won't be)."
 * **RyanCavanaugh** added label `Working as Intended`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64807#issuecomment-6177387309) **MARCROCK22** said "I guess this issue should be closed then"
 * [today](https://github.com/microsoft/TypeScript/issues/64807#issuecomment-6227887786) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#64842](https://github.com/microsoft/TypeScript/issues/64842) (Closed)

**\[api\] Paths not resolved relative to tsconfig**

*TypeScript's unstable API fails to resolve tsconfig-defined path mappings relative to the project's directory after a recent update.*

 * created by **dragomirtitian**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64843](https://github.com/microsoft/TypeScript/pull/64843) (Closed, `For Uncommitted Bug`)

**Ensure \`pathsBasePath\` is correctly forwarded from the API**

*Ensure the API correctly forwards the pathsBasePath setting to downstream components.*

 * created by **dragomirtitian**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64845](https://github.com/microsoft/TypeScript/pull/64845) (Closed, `Author: Team`, `For Uncommitted Bug`, **johnfav03**)

** Fix incremental diagnostics after global file deletion**

*An inverted SyncMap.Range callback convention caused incremental diagnostics to halt after the first file deletion and leave stale reports.*

 * created by **johnfav03**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/pull/64845#issuecomment-6221236005) **jakebailey** said "I actually think I have a fix for this in #64712 that's broader and fixes all possible variants."
 * [today](https://github.com/microsoft/TypeScript/pull/64845#issuecomment-6221255184) **jakebailey** said "Though I think you have some extra good stuff on top, looking harder."
 * [today](https://github.com/microsoft/TypeScript/pull/64845#issuecomment-6221317315) **jakebailey** said "Yeah, probably better to take yours and I'll deal with the rebase."
 * [today](https://github.com/microsoft/TypeScript/pull/64845#issuecomment-6221328516) **johnfav03** said "Okay, that sounds good to me; I'll give your PR a review when I get a minute"
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript#64846](https://github.com/microsoft/TypeScript/pull/64846) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add timing collection and dump via environment variable**

*Add a TS_API_TIMING_DIR environment variable to enable the API client to collect and dump timing information to a file on close.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64846#issuecomment-6224621358) **RyanCavanaugh** said "The proposed change from the above comment is https://github.com/microsoft/TypeScript/commit/c8b1982436e85f6fd85e96b931d85c4843b5b367"
 * [today](https://github.com/microsoft/TypeScript/pull/64846#issuecomment-6225944661) **andrewbranch** apologized for clicking the wrong button and noted that Jake's response time was faster
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64847](https://github.com/microsoft/TypeScript/pull/64847) (Open, `For Uncommitted Bug`)

**Check referenced project sources before probing their declaration outputs**

*Prioritize referenced project source files before checking built declaration outputs to eliminate redundant filesystem lookups.*

 * created by **guru-irl**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64847#issuecomment-6223607821) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64848](https://github.com/microsoft/TypeScript/issues/64848) (Open, `Domain: Performance`, `Possible Improvement`)

**TypeScript 7\.1 regression: quadratic root scanning in settled no\-op builds**

*TypeScript 7.1 regression causes no-op build performance degradation by quadratically scanning roots during up-to-date checks*

 * created by **turadg**

### [Issue microsoft/TypeScript#64849](https://github.com/microsoft/TypeScript/issues/64849) (Open)

**\[ServerErrors\]\[JavaScript\] main**

*The main JavaScript pipeline run analyzing 300 TypeScript repositories reported server errors, timeouts, and unknown failures.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/64849#issuecomment-6226256542) **typescript-automation[bot]** reported a debug failure panic during textDocument/formatting and included the stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/64849#issuecomment-6226257102) **typescript-automation[bot]** reported a panic handling request for textDocument/diagnostic with stack trace and artifact links
 * [today](https://github.com/microsoft/TypeScript/issues/64849#issuecomment-6226257651) **typescript-automation[bot]** reported a panic during cross-project handling due to slice bounds out of range
 * [today](https://github.com/microsoft/TypeScript/issues/64849#issuecomment-6226258189) **typescript-automation[bot]** reported a server connection closed prematurely error for apache/pouchdb and included affected repo details and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64849#issuecomment-6226258746) **typescript-automation[bot]** reported a server connection closed prematurely error and provided affected repo details, logs, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64849#issuecomment-6226259334) **typescript-automation[bot]** logged a panic handling a textDocument/diagnostic request and reported flaky diagnostics with stack trace for chartjs/Chart.js

### [PR microsoft/TypeScript#64850](https://github.com/microsoft/TypeScript/pull/64850) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Reduce the last ~2 years of uncovered top1000 repo failures into local tests**

*Use Copilot to extract uncovered test failures from the top1000 repositories over the past two years into local test cases.*

 * created by **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/64850#issuecomment-6226697082) **jakebailey** said "Given the port was 2 years, I bet there's more juicy stuff earlier."
 * [today](https://github.com/microsoft/TypeScript/pull/64850#issuecomment-6227785078) **RyanCavanaugh** said "For posterity - https://gist.github.com/RyanCavanaugh/0acf47a3fe9df7d07035216ff4dac14e"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64851](https://github.com/microsoft/TypeScript/issues/64851) (Open)

**\[ServerErrors\]\[TypeScript\] main**

*The TypeScript main Azure pipeline run encountered errors, timeouts, and clone failures analyzing 300 GitHub repos, completing 133 analyses.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/64851#issuecomment-6227406949) **typescript-automation[bot]** reported a runtime panic error during textDocument/codeAction handling
 * [today](https://github.com/microsoft/TypeScript/issues/64851#issuecomment-6227407511) **typescript-automation[bot]** reported a server connection closed prematurely error and provided affected repo details, error artifacts, replay commands, recent request logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64851#issuecomment-6227408044) **typescript-automation[bot]** reported server connection closed prematurely and provided repro steps

