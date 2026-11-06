# Report for 2026-11-05 (Thursday, November 5th, 2026)

29 different users commented on 163 different issues.

## Recommended Actions

 * Response Recommended
    * @MartinFerret asked whether the plan sounds right and if the name ErrorConstructorStatics is acceptable in [microsoft/TypeScript#61460](https://github.com/microsoft/TypeScript/issues/61460#issuecomment-6683539096)
    * @MartinFerret asked if the proposed trade-off was acceptable to proceed with updates and tests in [microsoft/TypeScript#61680](https://github.com/microsoft/TypeScript/issues/61680#issuecomment-6687246214)
    * @dummdidumm asked whether content mappers could be configured to exclude node_modules in [microsoft/TypeScript#64362](https://github.com/microsoft/TypeScript/issues/64362#issuecomment-6671076292)

## Activity Summary

### [Issue microsoft/TypeScript#61460](https://github.com/microsoft/TypeScript/issues/61460) (Open, `Help Wanted`, `Domain: lib.d.ts`, `Possible Improvement`)

**\`InstanceType\` and constructor return type inference doesn’t work for built‑in subtypes of \`ErrorConstructor\`**

*TypeScript's InstanceType returns Error for all built-in ErrorConstructor subtypes rather than their specific types.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/61460#issuecomment-2744724958) **ExE-Boss** proposed filtering out inherited overloads that were wholly subsumed by subinterface overloads to simplify overload resolution in ReturnType/InstanceType
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [later](https://github.com/microsoft/TypeScript/issues/61460#issuecomment-6683539096) **MartinFerret** proposed splitting ErrorConstructorStatics into a shared interface for ErrorConstructor and its subtypes, outlined compatibility considerations with @types/node, and asked for confirmation on the plan and name
 * [later](https://github.com/microsoft/TypeScript/issues/61460#issuecomment-6684715829) **ExE-Boss** said "I’d rather this get fixed on the overload resolution side, like what I proposed in May last year: "
 * [later](https://github.com/microsoft/TypeScript/issues/61460#issuecomment-6686499304) **MartinFerret** mentioned that the approach would avoid lib-side breakage but broaden inference design, and expressed openness to either direction

### [Issue microsoft/TypeScript#61680](https://github.com/microsoft/TypeScript/issues/61680) (Open, `Help Wanted`, `Domain: lib.d.ts`, `Possible Improvement`)

**Generic TypedArray constructors have only one overload**

*Using generic TypedArray constructors only exposes the ArrayBuffer overload, preventing valid TypedArray-to-TypedArray copies.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/61680#issuecomment-2946015973) **RyanCavanaugh** said "We can try a PR and this seems OK as long as it doesn't break something else"
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [later](https://github.com/microsoft/TypeScript/issues/61680#issuecomment-6687246214) **MartinFerret** offered two overload implementations for Uint8Array, described their trade-offs, and asked if the first solution trade-off was acceptable to proceed with updates and tests

### [PR microsoft/TypeScript#63904](https://github.com/microsoft/TypeScript/pull/63904) (Closed, `Domain: Performance`, `For Uncommitted Bug`, **andrewbranch**)

**Add batched version for the several API**

*Add batched versions of the getDeclaredTypeOfSymbol, getAliasedSymbol, getImmediateAliasedSymbol, getExportsOfModule, and getMemberInModuleExports API methods.*

 * **typescript-automation[bot]** assigned to **andrewbranch**
 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/63904#issuecomment-5425245595) **dragomirtitian** said "Fixed by https://github.com/microsoft/TypeScript/pull/63937"
 * (10 weeks ago) **dragomirtitian** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#63908](https://github.com/microsoft/TypeScript/pull/63908) (Closed, `Domain: Performance`, `For Backlog Bug`)

**Deduplicate repeated declarations on union/intersection properties**

*Deduplicate redundant property declarations in union and intersection types to prevent repeated members.*

 * [11 weeks ago](https://github.com/microsoft/TypeScript/pull/63908#issuecomment-5365073207) **typescript-automation[bot]** reported that the perf test build started and provided links to the build and results
 * [11 weeks ago](https://github.com/microsoft/TypeScript/pull/63908#issuecomment-5365255753) **typescript-automation[bot]** posted the requested perf run results with detailed tsc comparison metrics
 * (10 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#63918](https://github.com/microsoft/TypeScript/pull/63918) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Add some methods from Type to Checker\.**

*Add specific methods from Type to Checker to enable batched operations*

 * (11 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (2 weeks ago) **dragomirtitian** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#63934](https://github.com/microsoft/TypeScript/pull/63934) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Optimize LSP discriminated union decoding**

*Optimize LSP discriminated union decoding by bypassing buffering and using streaming when the discriminator is first for faster performance.*

 * (11 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (6 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#63937](https://github.com/microsoft/TypeScript/pull/63937) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**, **andrewbranch**)

**Add arbitrary API request batching**

*Add a batchRequests method and tick-based auto-batching with manual batchContext support for async API clients*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/63937#issuecomment-5396890510) **dragomirtitian** suggested that the PR looked promising and asked for public exposure of batched requests, describing their internal yield*-based batching library
 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/63937#issuecomment-5399409788) **weswigham** described a follow-up plan to add an API output that maps async function input into generators and a sync API driver for batching
 * (10 weeks ago) **weswigham** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#63969](https://github.com/microsoft/TypeScript/pull/63969) (Closed, `Domain: Performance`, `For Backlog Bug`)

**Avoid cloning cached declaration types after truncation**

*Prevent cloning of cached declaration type nodes after truncation threshold is reached, drastically improving compile performance.*

 * (5 weeks ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (5 weeks ago) **weswigham** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#63977](https://github.com/microsoft/TypeScript/pull/63977) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Avoid allocations when checking project reference declaration directories**

*Replace allocation-heavy project reference directory checks with ContainsPath to eliminate allocations and improve textDocument/references performance.*

 * created by **auvred**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (10 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#63983](https://github.com/microsoft/TypeScript/pull/63983) (Closed, `Domain: Performance`)

**Speed up CI with more jobs, less work**

*Propose parallelizing CI tests and disabling coverage in merge queues to reduce merge queue time by 40%.*

 * created by **jakebailey**
 * (10 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#63996](https://github.com/microsoft/TypeScript/pull/63996) (Closed, `Domain: Performance`, `For Backlog Bug`)

**Fix scanning issues related to Unicode escapes in RegExp group names and refactor identifier scanning**

*Refactor identifier scanning to correctly parse and normalize Unicode escapes and surrogate pairs in RegExp group names, preventing TS1514 errors.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432686256) **typescript-automation[bot]** provided the results of the requested performance run
 * (9 weeks ago) **jakebailey** closed the issue
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#63998](https://github.com/microsoft/TypeScript/pull/63998) (Closed, `Domain: Performance`)

**Reduce path\-mapping cache memory usage for projects with many paths**

*Move immutable parsed path-mapping patterns into a shared Resolver cache to reduce memory usage and improve module resolution performance.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/63998#issuecomment-5415767739) **DanielRosenwasser** asked how the issue arises, whether from multiple threads doing independent work on resolution or from multi-project setups
 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/63998#issuecomment-5418453342) **DanielRosenwasser** asked for clarification on how multiple paths would come into play when only grabbing paths once per tsconfig
 * (10 weeks ago) **andrewbranch** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64009](https://github.com/microsoft/TypeScript/pull/64009) (Closed, `Domain: Performance`)

**Don't depend on vfstest for transpile**

*Replace the transpile package’s dependence on vfstest’s test VFS with a local filesystem to reduce binary size by about 100KB.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/64009#issuecomment-5415531238) **andrewbranch** mentioned having a local fix that was broader than necessary and offered to address module resolution in a follow-up after Copilot comments were fixed
 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/64009#issuecomment-5415969655) **jakebailey** said "Fixed them, with tests"
 * (10 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64010](https://github.com/microsoft/TypeScript/pull/64010) (Closed, `Domain: Performance`)

**Remove free\-disk\-space step from CI**

*Remove the free-disk-space step from regular CI since it’s no longer needed outside copilot setup.*

 * created by **jakebailey**
 * (10 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64023](https://github.com/microsoft/TypeScript/pull/64023) (Closed, `Domain: Performance`)

**Additional generator\-based sync API methods**

*Add strongly-typed generator-based synchronous API methods to facilitate request batching parallel to the async API*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/64023#issuecomment-5428495821) **weswigham** described that api.batch is equivalent to runBatch, noted tests are missing and promised to add them along with a Promise.all helper
 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/64023#issuecomment-5429110699) **weswigham** extracted the 'all' equivalent helper from the generator-running logic and exported it in the sync API, tested user-composed generator functions, added batch-flattening to the 'all' batch request builder, and removed the API-level 'batchRequests' helper from API and moved it to Client
 * (10 weeks ago) **weswigham** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64024](https://github.com/microsoft/TypeScript/pull/64024) (Closed, `Domain: Performance`)

**Fix transpileModule/transpileDeclaration bugs**

*Skip module resolver functionality during transpileModule and transpileDeclaration to fix existing bugs and add corresponding tests.*

 * (10 weeks ago) **andrewbranch** closed the issue
 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/64024#issuecomment-5427586198) **johnnyreilly** said "Nice work @andrewbranch! I'll see if I can try this out on https://github.com/TypeStrong/ts-loader/pull/1704 this weekend. Thanks!"
 * [9 weeks ago](https://github.com/microsoft/TypeScript/pull/64024#issuecomment-5461369414) **johnnyreilly** reported removing workarounds from ts-loader after the change landed and linked to the relevant PR changes
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64063](https://github.com/microsoft/TypeScript/pull/64063) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Ditch nodeData interface in favor of generated accessors**

*Replace dynamic nodeData interface with generated accessors to reduce binary size, cut AST symbols, and improve compile performance.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-6026643943) **typescript-automation[bot]** provided the results of the requested performance run
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-6151517581) **jakebailey** said "Superseded by #64773, the bottom of the stack summarized in #64734."
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64159](https://github.com/microsoft/TypeScript/pull/64159) (Closed, `Domain: Performance`, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Strongly type file paths**

*Add branded types for absolute, normalized file and directory paths to enforce path invariants and reduce normalization overhead.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64159#issuecomment-5702887286) **jakebailey** said "I guess I can try and flip the API side back to strings, but there's a bunch of conversions we get to skip because of it, and some of the bugs found were on the API side outside the Go code."
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64159#issuecomment-5961659959) **andrewbranch** said "(not that the conflict-free state is going to survive the stuff already enabled to auto-merge)"
 * (1 month ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64194](https://github.com/microsoft/TypeScript/pull/64194) (Closed, `Domain: Performance`, `For Backlog Bug`)

**fix\(checker\): cap template literal type size to avoid unbounded growth**

*Cap template literal type size with character and placeholder limits to prevent infinite type instantiation and memory exhaustion.*

 * created by **ekalinin**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (5 weeks ago) **ahejlsberg** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64206](https://github.com/microsoft/TypeScript/pull/64206) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Benchmark generator API, fix performance of nested \`all\` calls**

*Deferring nested `all` calls to the host executor eliminates their performance overhead and stabilizes benchmark generator execution.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [8 weeks ago](https://github.com/microsoft/TypeScript/pull/64206#issuecomment-5593558675) **weswigham** apologized to @andrewbranch and described finding modest but meaningful performance gains by using a class implementing the iterator protocol over a native generator for hoisted messages
 * (8 weeks ago) **weswigham** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64220](https://github.com/microsoft/TypeScript/pull/64220) (Closed, `Domain: Performance`, `For Milestone Bug`, **johnfav03**)

**Schedule tsc \-b projects by dependency depth to reduce builder idle time on upstream projects**

*Sort topologically built TypeScript projects by dependency depth rather than references-first to reduce builder idle time and speed up large monorepo builds.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5749572773) **Freakazo** tested the branch on a large monorepo and observed performance gains (median 38.24s to 28.39s) with increased memory usage (~5.4GB to ~6.9GB), and noted most benchmarks don’t use the -b flag
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5766071230) **jakebailey** clarified that only the xstate benchmark used -b, where the optimization had the biggest impact
 * (6 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64305](https://github.com/microsoft/TypeScript/pull/64305) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**perf: avoid duplicate symbol link lookup in \`GetNameTypeOfSymbol\`**

*Remove redundant TryGet call in GetNameTypeOfSymbol to avoid duplicate symbol link lookup and improve performance.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64305#issuecomment-5709911469) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (7 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64306](https://github.com/microsoft/TypeScript/pull/64306) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**perf: preallocate instantiated symbol table**

*Preallocate the instantiated symbol table to its known size to avoid intermediate reallocations.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64306#issuecomment-5710355492) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (7 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64331](https://github.com/microsoft/TypeScript/pull/64331) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Make all the codegen we do incremental**

*Add incremental caching to all repository code generation tasks to reduce generate subtasks runtime by up to 80%.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64331#issuecomment-5766922572) **weswigham** said "That's pretty fair - the logging got simplified as I merged helpers from the first version and it got a wee bit too simple."
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64331#issuecomment-5767488842) **weswigham** said "@jakebailey There ya go, output of the cache layer's a bit more verbose."
 * (6 weeks ago) **weswigham** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#64362](https://github.com/microsoft/TypeScript/issues/64362) (Open, `Needs Investigation`, `Domain: Content Mappers`, **andrewbranch**)

**Content mappers: more granular resolution, and default extensions in the manifest**

*Enhance content mappers to support regex-style filters or dynamic on-register claims for file-specific mapping beyond simple extensions.*

 * (6 weeks ago) **RyanCavanaugh** added labels `Needs Investigation`, `Domain: Content Mappers`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/64362#issuecomment-6671076292) **dummdidumm** proposed excluding node_modules from content mappers to solve Svelte package type-definition resolution issues

### [PR microsoft/TypeScript#64371](https://github.com/microsoft/TypeScript/pull/64371) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**parser: bound recursion depth to avoid stack overflow on deeply nested input**

*Bound parser recursion with a 40000-depth limit and new TS1700 diagnostic to prevent stack overflows on deeply nested input.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64371#issuecomment-5763762546) **jakebailey** rejected setting an arbitrary maximum as a fix and noted upcoming parser restructuring changes to reduce recursion
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64371#issuecomment-5768190783) **RyanCavanaugh** said "Closing per linked discussion; this PR attempts to enforce an invariant that is documented as explicitly not existing."
 * (6 weeks ago) **RyanCavanaugh** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64379](https://github.com/microsoft/TypeScript/pull/64379) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add the \`concurrency\` option to node tests**

*Introduce a concurrency option to Node tests to improve performance of filtered runs without impacting full-suite execution.*

 * (6 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (6 weeks ago) **weswigham** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64388](https://github.com/microsoft/TypeScript/pull/64388) (Closed, `Domain: Performance`, `For Backlog Bug`)

**\[perf\]\[experiment\] fix\(64378\): add a cache to avoid repeated type arg inference**

*Introduce a cache for type argument inference to eliminate repeated inference and significantly improve performance.*

 * (6 weeks ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (1 month ago) **a-tarasyuk** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64392](https://github.com/microsoft/TypeScript/pull/64392) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Onboard loc and vendoring to code generation caching**

*Onboard loc and vendoring to code generation caching by sharing file fingerprints to avoid duplicate hashing and reduce generate time from 10s to 4s*

 * (6 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (6 weeks ago) **weswigham** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64393](https://github.com/microsoft/TypeScript/pull/64393) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Just check package\.json for vendor code up\-to\-date\-ness**

*Simplify vendor dependency updates by verifying their versions in package.json instead of inspecting node_modules.*

 * (6 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (6 weeks ago) **weswigham** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64402](https://github.com/microsoft/TypeScript/pull/64402) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use lazy map for diagnostic keyToMessage, speeding up go build**

*Optimize diagnostic keyToMessage by using a lazy map to reduce Go build time and improve startup performance.*

 * (6 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (6 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64408](https://github.com/microsoft/TypeScript/pull/64408) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Fix a couple type cache issues**

*Resolve two type cache bugs in the API to comply with the guidelines introduced in #64397.*

 * (6 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (6 weeks ago) **andrewbranch** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64409](https://github.com/microsoft/TypeScript/pull/64409) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Onboard the \`lib\` task to code generation caching and include it in \`generate\`**

*Integrate the lib task into code generation caching and the generate command to prevent missing diffs in CI.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64409#issuecomment-5803155730) **jakebailey** explained that there is no code generation beyond copying from the DOM lib generator and questioned if this process qualifies as codegen since other generators produce committed artifacts
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64409#issuecomment-5818725139) **weswigham** said "Alright, we can just leave it as-is, not like it saves any real amount time to make a basic copy option incremental anyway."
 * (6 weeks ago) **weswigham** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64434](https://github.com/microsoft/TypeScript/pull/64434) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Give standalone created files a tracked identity and incorporate with the parse cache**

*Modify createSourceFile API to use a global parse cache and return disposable leases for identity consistency.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64434#issuecomment-5823204073) **andrewbranch** said "Then using it or otherwise dispose it when you're ready to throw it away, or don't and it will get released when you close the API"
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64434#issuecomment-5823240240) **andrewbranch** described that binder symbol follow-up creates a confusing bifurcation because untracked throwaway SourceFiles cannot fetch or assign binder symbols using server identity methods
 * (6 weeks ago) **andrewbranch** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64466](https://github.com/microsoft/TypeScript/pull/64466) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Fix language server retaining pre\-edit program and its checkers after program clone**

*Prevent TypeScript language server cloned programs from retaining previous program checker pools to reduce memory leaks.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64466#issuecomment-5850307599) **jakebailey** said "I think there's actually another one of these in ReuseProgram via processedFiles."
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64466#issuecomment-5880715981) **jakebailey** said "I think this PR is in itself fine, but I'm going to try and put together a very invasive version which prevents us from making this mistake in the future."
 * (5 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64469](https://github.com/microsoft/TypeScript/pull/64469) (Closed, `Domain: Performance`, `For Uncommitted Bug`, **johnfav03**)

**Index re\-exporting modules for declaration emit**

*Optimize TypeScript’s declaration emit performance by caching an export-to-module index to avoid repeated scans during incremental rebuilds*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-6046261147) **weswigham** observed no performance regression and asked for a large public repository demonstrating the fixed performance issue to add to the perf test suite
 * (1 month ago) **weswigham** closed the issue
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-6062593250) **resure** provided Spotify's Backstage as a large public repo example and benchmarked performance improvements with metrics
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64476](https://github.com/microsoft/TypeScript/pull/64476) (Closed, `Domain: Performance`, `For Milestone Bug`, **ahejlsberg**)

**only build intersection props that can reduce it to never**

*Modify TypeScript’s intersection type reduction to skip creating properties that cannot reduce to never, reducing memory and improving performance.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64476#issuecomment-5878048790) **maschwenk** said "@ahejlsberg shall I close this out?"
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64476#issuecomment-5878420125) **ahejlsberg** confirmed that #64499 was already in main
 * (5 weeks ago) **maschwenk** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64491](https://github.com/microsoft/TypeScript/pull/64491) (Closed, `Domain: Performance`, `For Backlog Bug`)

**Match Strada and don't resolve imports of ambient modules declared in the same file**

*Do not resolve imports of ambient modules declared in the same file to external typings, preventing excessive type instantiations.*

 * (5 weeks ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (3 weeks ago) **andrewbranch** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64499](https://github.com/microsoft/TypeScript/pull/64499) (Closed, `Domain: Performance`, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Only check properties with multiple declarations for never\-reduction**

*Optimize getReducedType by limiting never-type reduction checks to properties declared in multiple intersection constituents.*

 * (5 weeks ago) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * (5 weeks ago) **ahejlsberg** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64518](https://github.com/microsoft/TypeScript/pull/64518) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Make binder\-produced symbols owned by SourceFiles in the client, like the server and 6\.0**

*Cache binder-produced symbols in client SourceFiles to maintain symbol identity across snapshots and enable context-independent symbol retrieval.*

 * (5 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (5 weeks ago) **andrewbranch** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64519](https://github.com/microsoft/TypeScript/pull/64519) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Better manage Program options lifetimes**

*Refactor ProgramOptions into separate Config, Hosts, and Factories components to properly manage lifetimes and prevent stale state.*

 * (5 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (5 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64526](https://github.com/microsoft/TypeScript/pull/64526) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**build members of keyof mapped types lazily**

*Implement lazy member tables for keyof mapped types to defer property symbol creation and enhance performance*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64526#issuecomment-6022090808) **maschwenk** closed the PR due to minimal heap savings and required rework atop future changes
 * (1 month ago) **maschwenk** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64551](https://github.com/microsoft/TypeScript/pull/64551) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**perf\(checker\): fast\-path compareNodes for identical AST parent containers and use cmp\.Compare**

*Introduces a fast-path compareNodes for identical AST parents and uses cmp.Compare to prevent 64-bit symbol ID overflow.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-6157166753) **typescript-automation[bot]** reported initiation of perf test jobs and provided status links
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-6157530877) **typescript-automation[bot]** provided the requested performance run results
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64553](https://github.com/microsoft/TypeScript/pull/64553) (Closed, `Domain: Performance`, `Author: Team`, `For Backlog Bug`, **ahejlsberg**)

**Cache inferences made from type arguments**

*Cache type argument inferences in the existing invokeOnce infrastructure and include variance states to prevent false matches*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5919122764) **typescript-automation[bot]** provided the requested perf run results in a comparison report
 * (5 weeks ago) **ahejlsberg** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64563](https://github.com/microsoft/TypeScript/pull/64563) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Build all platforms in parallel in release pipeline**

*Build all platforms concurrently in the release pipeline to accelerate full release builds.*

 * (5 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#64565](https://github.com/microsoft/TypeScript/issues/64565) (Closed, `Needs Investigation`, **jakebailey**)

**TypeScript 7 VS Code extension: a workspace "typescript" 7\.x package is not detected, only "@typescript/native\-preview", which is no longer published**

*The TypeScript 7 VS Code extension fails to detect standard typescript@7 in workspace, using its bundled compiler instead.*

 * (1 month ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **jakebailey**
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64565#issuecomment-6322494161) **insilications** said "It seems that using the nightly extension, TypeScriptTeam.vscode-typescript-nightly, is now only working if one sets "js/ts.tsdk.path": "node_modules/typescript""
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64600](https://github.com/microsoft/TypeScript/pull/64600) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**don't copy union and intersection properties into the augmented property cache**

*Prevent unnecessary copying of union and intersection properties into the augmented property cache and defer cache map allocation to reduce memory overhead.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64600#issuecomment-5963635621) **maschwenk** said "Withdrawing this one: the gain is too small to be worth reviewer time on its own. The larger change is #64475 / #64526."
 * (1 month ago) **maschwenk** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64601](https://github.com/microsoft/TypeScript/pull/64601) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**instantiate conditional types without a combined mapper for the cache lookup**

*Optimize conditional type instantiation to bypass composite mapper creation for cache lookups, saving millions of allocations.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64601#issuecomment-5963635944) **maschwenk** said "Withdrawing this one: the gain is too small to be worth reviewer time on its own. The larger change is #64475 / #64526."
 * (1 month ago) **maschwenk** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64615](https://github.com/microsoft/TypeScript/pull/64615) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Restore dependency\-depth build scheduling**

*Restore the dependency-depth-based build scheduling functionality removed by PR #64158 that regressed PR #64220.*

 * (1 month ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64624](https://github.com/microsoft/TypeScript/pull/64624) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix idle cache clean timer never being stored on Session**

*The idle cache clean timer isn't saved to session, so cancelIdleCacheClean can't stop it and Close blocks until it fires.*

 * (1 month ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (1 month ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#64634](https://github.com/microsoft/TypeScript/issues/64634) (Closed, `Needs Investigation`, **iisaduan**)

**\[api\] Add \`parseConfigFileTextToJson\(\)\` helper**

*Add a parseConfigFileTextToJson() helper to enable consistent diagnostics when parsing JSON config strings.*

 * created by **mrazauskas**
 * (1 month ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **iisaduan**
 * (today) **iisaduan** closed the issue

### [PR microsoft/TypeScript#64648](https://github.com/microsoft/TypeScript/pull/64648) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Add cache to \`getSimplifiedConditionalType\`**

*Add caching for conditional types in getSimplifiedType to improve performance and ensure consistency.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64648#issuecomment-6002735350) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64648#issuecomment-6004798872) **ahejlsberg** said "No measurable effect on perf tests, likely because we don't have react tests which is where it's supposed to help."
 * (3 weeks ago) **ahejlsberg** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64649](https://github.com/microsoft/TypeScript/pull/64649) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Cache one nodebuilder per emit resolver, make emit resolver emit context scoped**

*Cache one NodeBuilder per emit resolver and scope each emit resolver to its specific emit context.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64649#issuecomment-6023272670) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64649#issuecomment-6024002969) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * (1 month ago) **weswigham** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64675](https://github.com/microsoft/TypeScript/pull/64675) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Try to filter go compiler test files before reading them and building compiler tests**

*Filter Go compiler test files by name or regex before loading to reduce IO and speed up Windows test runs.*

 * (1 month ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (1 month ago) **weswigham** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64679](https://github.com/microsoft/TypeScript/pull/64679) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add createFileSystemFromSnapshot\(oldSnapshot, extraFSLayer\)**

*Implement createFileSystemFromSnapshot to reapply a previous snapshot’s synthetic file system onto a new snapshot with optional layering.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6347271080) **weswigham** realized that the FS structure only reused the final state rather than replaying all intermediate snapshots and proposed renaming the API and updating the PR
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6348197362) **weswigham** said "@andrewbranch does createFileSystemFromSnapshot like this work for you? Makes sense to me."
 * (1 week ago) **weswigham** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64691](https://github.com/microsoft/TypeScript/pull/64691) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Shared data symbols**

*Splitting Symbol into separate header and shared data parts in the checker reduces instantiated symbol size from 96 to 24 bytes.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64691#issuecomment-6065021531) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64691#issuecomment-6066086195) **ahejlsberg** said "Looks like 5-7% savings in memory overhead."
 * (1 month ago) **ahejlsberg** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64695](https://github.com/microsoft/TypeScript/pull/64695) (Open, `Domain: Performance`, `For Milestone Bug`, `For Backlog Bug`, **ahejlsberg**)

**\[experiment\] Skip incompatible discriminants when inferring**

*Add experimental logic to skip incompatible discriminants during discriminated union type inference to reduce inference work.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6588948856) **typescript-automation[bot]** reported the performance comparison results between baseline and PR as requested
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6598167877) **Andarist** noted that the table results were skewed by the inclusion of another optimization in the PR
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6666346894) **weswigham** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6666349655) **typescript-automation[bot]** noted that perf test job started and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6667475727) **typescript-automation[bot]** provided performance run results with metrics for errors, symbols, types, and memory usage

### [PR microsoft/TypeScript#64711](https://github.com/microsoft/TypeScript/pull/64711) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Dense link stores**

*Switching paged link stores to dense allocation cuts wasted storage and memory usage by up to 9% in multi-checker compilations.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64711#issuecomment-6091080523) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * (3 weeks ago) **ahejlsberg** closed the issue
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64711#issuecomment-6091297926) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64723](https://github.com/microsoft/TypeScript/pull/64723) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Create declaration emit diagnostic selectors on demand**

*Delay creation of symbol accessibility diagnostic selectors until needed during declaration file emission to eliminate unnecessary allocations and improve performance.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64723#issuecomment-6295599026) **gwkline** said "Withdrawing: the time win is too small to justify reviewer attention on its own. Keeping #64722, which is the change that actually moves check time."
 * (2 weeks ago) **gwkline** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64724](https://github.com/microsoft/TypeScript/pull/64724) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Cache exports lookups and path patterns in module specifier generation**

*Cache exports and paths lookups in the module specifier generator to reduce redundant resolution work.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64724#issuecomment-6295599958) **gwkline** said "Withdrawing to keep the review queue focused on #64722. The emit-side caching here is a larger host/interface change than the win warrants right now."
 * (2 weeks ago) **gwkline** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64734](https://github.com/microsoft/TypeScript/pull/64734) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Various memory optimizations**

*Combined memory optimizations reduce memory usage by 22–29% and allocation counts by 3.6–16.6% across nine test scenarios.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6134989198) **typescript-automation[bot]** provided the performance run results with a comparison report for tsc metrics
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6173691806) **jakebailey** said "The remaining work is now in independent PRs: #64775, #64781, #64788, #64789, #64791, #64815."
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64735](https://github.com/microsoft/TypeScript/pull/64735) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Resolve instantiated object members through a shared worker**

*Allow instantiated object members to be resolved properly when used inside shared workers.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6129638105) **typescript-automation[bot]** posted the requested perf run results comparing baseline and PR, showing symbol count reduction and memory usage improvements
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6151656466) **jakebailey** said "Superseded by #64765."
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64739](https://github.com/microsoft/TypeScript/pull/64739) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Shrink \`ValueSymbolLinks\` by 16 bytes**

*Relocating a boolean into a separate set reduces ValueSymbolLinks memory by 16 bytes (1%) when compiling VS Code.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64739#issuecomment-6115562754) **typescript-automation[bot]** indicated that the performance test job started and provided status and results links
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64739#issuecomment-6115800643) **typescript-automation[bot]** posted performance run results for the requested comparison on the PR
 * (3 weeks ago) **ahejlsberg** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64762](https://github.com/microsoft/TypeScript/pull/64762) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix symbol table kind mask**

*Restore alias caching and the members fast path by ensuring the symbol table kind mask includes all three kind bits.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64762#issuecomment-6138957785) **typescript-automation[bot]** reported build status for performance test and provided results link
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64762#issuecomment-6139283586) **typescript-automation[bot]** posted the requested perf run results
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64765](https://github.com/microsoft/TypeScript/pull/64765) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Resolve class and interface members through shared layouts**

*Introduce shared member layouts and lazy resolution for class and interface instantiations to significantly reduce memory usage and symbol creation.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6329170294) **typescript-automation[bot]** reported that perf test jobs started and shared links to status and results
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6329797206) **typescript-automation[bot]** provided the performance run results as requested
 * (1 week ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64773](https://github.com/microsoft/TypeScript/pull/64773) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Replace nodeData interface with generated AST accessors**

*Replace the dynamic nodeData interface with generated AST kind-switch accessors, reducing code size and improving compile performance.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64774](https://github.com/microsoft/TypeScript/pull/64774) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compact checker type metadata**

*Replace self-referential type metadata with a compact kind tag to save 16 bytes per type and remove GC pointer storage.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64776](https://github.com/microsoft/TypeScript/pull/64776) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Batch allocations of common checker types**

*Use typed arenas to batch allocate common checker type records, reducing small-object heap allocation overhead while enabling independent block collection.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64777](https://github.com/microsoft/TypeScript/pull/64777) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Presize checker type\-list cache keys**

*Reserve the encoded size upfront for type-list cache keys to minimize temporary hash buffer allocations.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64778](https://github.com/microsoft/TypeScript/pull/64778) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid allocating normalized types on interning cache hits**

*Reuse cached union and intersection types during normalization to avoid temporary allocations and improve memory efficiency.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64779](https://github.com/microsoft/TypeScript/pull/64779) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compact type mappers and coallocate inference mapper storage**

*Compact type mappers by replacing interfaces with a concrete header and coallocating two inference mappers, reducing allocations by 3.90%.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64780](https://github.com/microsoft/TypeScript/pull/64780) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Move cold value\-symbol links out of the hot records**

*Move optional value-symbol link fields into a sidecar structure to shrink hot records and improve memory usage*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64782](https://github.com/microsoft/TypeScript/pull/64782) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Recover concrete AST nodes from their embedded headers**

*Recover AST nodes from embedded headers at offset zero with kind-checked casts to shrink header size and reduce memory usage*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64783](https://github.com/microsoft/TypeScript/pull/64783) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep optional symbol tables out of hot symbol records**

*Optional symbol tables are relocated to arena-batched metadata, shrinking symbol records and reducing memory usage.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64784](https://github.com/microsoft/TypeScript/pull/64784) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Move optional structured type shape into cold storage**

*Move unused StructuredType fields into optional storage to shrink its size and cut memory and GC overhead.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64785](https://github.com/microsoft/TypeScript/pull/64785) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep optional type\-node and signature state out of hot records**

*Reduce TypeScript compiler memory usage by extracting optional type-node parameters and signature state from hot record structures.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64786](https://github.com/microsoft/TypeScript/pull/64786) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Bound arena retention by bytes instead of object count**

*Bound arena chunk size by 512 bytes instead of object count to reduce heap retention and GC work.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64787](https://github.com/microsoft/TypeScript/pull/64787) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use paged indexes for type\-node and signature caches**

*Type-node and signature caches are migrated from AST pointer maps to paged indexes using existing node-link stores, reducing heap usage, GC scanning, and allocations.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64790](https://github.com/microsoft/TypeScript/pull/64790) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reuse ordered property counts during intersection reduction**

*Reuse bounded, checker-local property-count tables during intersection reduction to reduce allocated memory by around 27% and allocations by about 8%.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64793](https://github.com/microsoft/TypeScript/pull/64793) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Batch allocations of common checker types**

*Use typed arenas to batch-allocate common checker types, reducing small-object allocation overhead and preserving independent block collection.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64794](https://github.com/microsoft/TypeScript/pull/64794) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Presize checker type\-list cache keys**

*Reserve known encoded size for checker type-list cache keys to reduce temporary hash buffer allocations and improve memory efficiency.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64795](https://github.com/microsoft/TypeScript/pull/64795) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid allocating normalized types on interning cache hits**

*Eliminate unnecessary allocations in union and intersection normalization by reusing cached equivalent types to reduce memory usage.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **ahejlsberg** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64796](https://github.com/microsoft/TypeScript/pull/64796) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compact type mappers and coallocate inference mapper storage**

*Replace mapper interfaces with concrete kind headers and coallocate inference context’s two mappers to reduce allocations.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **ahejlsberg** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64797](https://github.com/microsoft/TypeScript/pull/64797) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Move cold value\-symbol links out of the hot records**

*Relocate cold value-symbol link fields into an optional arena-backed sidecar to shrink hot records and reduce memory usage.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **ahejlsberg** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64798](https://github.com/microsoft/TypeScript/pull/64798) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Recover concrete AST nodes from their embedded headers**

*Embed AST node headers at offset zero with kind checks to shrink header size, boost memory efficiency, and omit non-debug DWARF.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **ahejlsberg** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64799](https://github.com/microsoft/TypeScript/pull/64799) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep optional symbol tables out of hot symbol records**

*Move optional symbol tables into arena-batched metadata to shrink symbol records and lower heap and GC overhead*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **ahejlsberg** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64800](https://github.com/microsoft/TypeScript/pull/64800) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Move optional structured type shape into cold storage**

*Move optional type metadata into cold storage to reduce StructuredType memory footprint and improve GC performance.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **ahejlsberg** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64801](https://github.com/microsoft/TypeScript/pull/64801) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep optional type\-node and signature state out of hot records**

*Relocate optional outer type parameters and signature state out of hot records to reduce memory usage.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64802](https://github.com/microsoft/TypeScript/pull/64802) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Bound arena retention by bytes instead of object count**

*Use 512-byte arena chunks instead of fixed object counts to reduce memory retention and GC at cost of more allocations.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64803](https://github.com/microsoft/TypeScript/pull/64803) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use paged indexes for type\-node and signature caches**

*Replace AST pointer maps with paged indexes keyed by stable node IDs for type-node and signature caches to reduce memory usage.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64804](https://github.com/microsoft/TypeScript/pull/64804) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reuse ordered property counts during intersection reduction**

*Reuse bounded, checker-local property-count tables in intersection reduction to reduce allocated memory by 26.6%, allocations by 7.6%, and CLI instructions by 8.9%.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64804#issuecomment-6162382028) **DanielRosenwasser** said "Weird that we need a free list. Maybe it's worth exploring a pool of 16, a bitset that indicates which one is currently in use, and just allocates if they're all occupied."
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64816](https://github.com/microsoft/TypeScript/pull/64816) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use small slices for union and intersection property sources**

*Use plain slices for union and intersection properties until a size threshold to reduce allocations and memory usage.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64816#issuecomment-6173689076) **jakebailey** said "Folded into #64815."
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64817](https://github.com/microsoft/TypeScript/pull/64817) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reuse name sets when enumerating union and intersection properties**

*Reuse name sets from a per-checker free list for union and intersection enumeration, cutting allocated bytes 6.76% and allocations 0.60%.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64817#issuecomment-6173690613) **jakebailey** said "Folded into #64815."
 * (3 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64823](https://github.com/microsoft/TypeScript/pull/64823) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Client performance optimizations**

*Six independent client performance optimizations reduce processing time, memory allocations, and improve symbol lookup benchmark speeds.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64823#issuecomment-6278994430) **typescript-automation[bot]** reported that the perf test api build started and provided status links
 * (2 weeks ago) **andrewbranch** closed the issue
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64823#issuecomment-6279330552) **typescript-automation[bot]** said "@andrewbranch, the perf run you requested failed. You can check the log here."
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64830](https://github.com/microsoft/TypeScript/pull/64830) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Avoid weakset for executed generators**

*Replace WeakSet with a global symbol marker to track executed generators and prevent their reuse*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64830#issuecomment-6197412104) **dragomirtitian** agreed to remove the check, stating no use case and willingness to add it back if needed
 * (3 weeks ago) **weswigham** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64872](https://github.com/microsoft/TypeScript/pull/64872) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use paged link stores for all symbol links**

*Use paged link stores for all symbol link types to reduce map lookups and improve performance at minimal memory cost.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64872#issuecomment-6274246320) **typescript-automation[bot]** reported the results of the requested perf run
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64872#issuecomment-6413051384) **jakebailey** said "Closing; perf results don't justify it."
 * (1 week ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64873](https://github.com/microsoft/TypeScript/pull/64873) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Don't resolve mapped type members to find their signatures**

*Avoid resolving mapped type members for signature checks to prevent unnecessary property building and improve compiler performance.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6376752833) **typescript-automation[bot]** started the perf test job and posted links to build status and results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6377132981) **typescript-automation[bot]** posted the performance run results including a detailed comparison report
 * (1 week ago) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64877](https://github.com/microsoft/TypeScript/pull/64877) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**LSP perf optimizations**

*LSP performance optimizations in the TypeScript compiler reduce time, memory, and allocations in VSCode benchmarks by up to 43%.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6277584246) **typescript-automation[bot]** reported that CI jobs for perf test started and provided links to build results
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6278207578) **typescript-automation[bot]** posted the requested performance run results
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6666502037) **andrewbranch** said "@typescript-bot perf test"
 * [today](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6666504476) **typescript-automation[bot]** announced the start of CI jobs and provided build and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6667834432) **typescript-automation[bot]** reported performance results for the requested perf run
 * (today) **andrewbranch** closed the issue

