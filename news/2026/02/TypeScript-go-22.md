# Report for 2026-02-22 (Sunday, February 22nd, 2026)

14 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @justinsmid provided memory usage stats and a heap profile in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3943840500)
    * @evsasse provided profiling and log files in [microsoft/TypeScript-go#2859](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-3944449861)
    * @Meligy reported that .scss imports broke even with fake modules in [microsoft/TypeScript-go#2864](https://github.com/microsoft/TypeScript-go/pull/2864#issuecomment-3942566068)
    * @pedro757 confirmed it breaks css imports in [microsoft/TypeScript-go#2864](https://github.com/microsoft/TypeScript-go/pull/2864#issuecomment-3944772586)
    * @siphosenkosindhlovu confirmed that the issue occurs in playwright-core@1.55.0 in [microsoft/TypeScript-go#2873](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3942883536)
    * @AntonOfTheWoods asked if deprecation should be considered a syntax error in [microsoft/TypeScript-go#2873](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3942915711)

## Activity Summary

### [Issue microsoft/TypeScript-go#2285](https://github.com/microsoft/TypeScript-go/issues/2285) (Closed, `Domain: Editor`)

**Backticked JSDOC \`{@link}\`s in tagless descriptions docblocks are broken**

*Backticked JSDoc {@link} tags in tagless description comments fail to render properly in VS Code hover tooltips.*

 * (10 weeks ago) **mjbvz** removed labels `bug`, `javascript`
 * **jakebailey** added label `Domain: Editor`
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo takes forever to compile, 325seconds vs typescript 42seconds**

*tsgo watch compilation takes 325s versus TypeScript’s 42s, and the reporter requests help diagnosing and resolving the slowdown.*

 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3940694707) **jogibear9988** identified a performance bottleneck in GetECMALineAndCharacterOfPosition due to O(n²) rune counting and proposed caching rune-to-byte offsets for O(1) character queries
 * [today](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3941359888) **jakebailey** stated that the previous analysis added nothing new and encouraged a fix submission while noting the issue's complexity due to emit phase line map changes
 * [today](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3941829062) **jogibear9988** apologized for distracting and mentioned asking Copilot to explain why it works in JS but not in Go
 * [today](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3941938891) **jakebailey** said "Try #2872 to see if it fixes your case."

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3931736730) **shinichy** said "@neo773 Are you able to reproduce this issue in https://github.com/twentyhq/twenty/? I couldn't reproduce this issue in the repo."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3936503506) **andrewbranch** said "@shinichy could you try out #2855 and see if that improves things for you?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3940248161) **shinichy** reported that the memory leak slowed but persisted, that the tsgo LSP process still hung and memory usage hit ~30GB, traced the hang to extractFromFile(entrypoint), and shared an AI-generated explanation of unbounded work per entrypoint and lack of cancellation
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3941537584) **andrewbranch** asked for the package or file causing the issue and requested debug details and dependency files to reproduce
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3942722362) **shinichy** mentioned inability to share code from private repo, noted that bucket.DependencyNames was nil and len(bucket.Paths) was 0, and offered to create a public repo to reproduce the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3943840500) **justinsmid** reported experiencing excessive memory usage and provided cache stats and a heap profile, noting the project was private but accessible to Jake Bailey

### [PR microsoft/TypeScript-go#2821](https://github.com/microsoft/TypeScript-go/pull/2821) (Closed)

**Remove redundant JSDoc flag checks**

*Remove redundant flag checks in JSDoc and EagerJSDoc since both already perform this check and return nil.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2859](https://github.com/microsoft/TypeScript-go/issues/2859) (Open)

**\`gql\.tada\` performing better with \`\-\-singleThreaded\` than without it**

*tsgo without --singleThreaded runs significantly slower than with it when generating gql.tada types due to union caching inefficiencies.*

 * created by **evsasse**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-3937207873) **jakebailey** said "I would suggest using --pprofDir . and upload those profiles."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-3937281866) **ahejlsberg** noted that expensive type instantiations jumped from 32M in single-threaded mode to 125M in concurrent mode, indicating each of the four type checkers repeated the same work
 * [later](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-3944449861) **evsasse** attached profiling and log files for default and single-threaded runs and offered to provide additional information

### [PR microsoft/TypeScript-go#2864](https://github.com/microsoft/TypeScript-go/pull/2864) (Closed)

**Enable \`noUncheckedSideEffectImports\` by default**

*Port PR 62443 to enable the noUncheckedSideEffectImports compiler option by default.*

 * (2 days ago) **jakebailey** closed the issue
 * (2 days ago) **jakebailey** reopened the issue
 * (yesterday) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2864#issuecomment-3942566068) **Meligy** said "This breaks .scss imports even when you have fake modules for them."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2864#issuecomment-3942792030) **jakebailey** said "Please file an issue with a repro. That should not be the case https://devblogs.microsoft.com/typescript/announcing-typescript-5-6/#the---nouncheckedsideeffectimports-option"
 * [later](https://github.com/microsoft/TypeScript-go/pull/2864#issuecomment-3944772586) **pedro757** said "I can confirm this breaks css imports"
 * [later](https://github.com/microsoft/TypeScript-go/pull/2864#issuecomment-3944805108) **Andarist** said "Please open a new issue with the repro steps included. Ideally, one that would showcase the difference between typescript@next and tsgo"

### [PR microsoft/TypeScript-go#2868](https://github.com/microsoft/TypeScript-go/pull/2868) (Closed)

**Don't process \`@link\` JSDoc tags inside backticks**

*Prevent processing of @link JSDoc tags inside backticks.*

 * created by **ahejlsberg**
 * (2 days ago) **jakebailey** closed the issue
 * (2 days ago) **jakebailey** reopened the issue
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2870](https://github.com/microsoft/TypeScript-go/pull/2870) (Closed)

**2x speedup of binary AST encoding**

*Directly appending uint32 instead of using a runtime type switch doubles binary AST encoding performance.*

 * created by **auvred**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2870#issuecomment-3941383597) **jakebailey** said "FWIW I would recommend using https://pkg.go.dev/golang.org/x/perf/cmd/benchstat to test your changes, e.g.: https://pkg.go.dev/golang.org/x/perf/cmd/benchstat#hdr-Example"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2871](https://github.com/microsoft/TypeScript-go/issues/2871) (Open)

**\[ServerErrors\]\[TypeScript\] linux\-x64\-7\.0\.0\-dev\.20260222\.1 vs **

*The linux-x64 TypeScript 7.0.0-dev pipeline run encountered multiple errors—including timeouts, clone failures, and unknown failures—while analyzing popular repositories.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2871#issuecomment-3941898703) **typescript-bot** reported a runtime panic in the textDocument/completion handler due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/2871#issuecomment-3941898733) **typescript-bot** reported that the server connection closed prematurely for the elastic/kibana repo and provided repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/2871#issuecomment-3941898753) **typescript-bot** reported a server connection closed prematurely error and provided affected repos, artifact links, request logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/2871#issuecomment-3941898776) **typescript-bot** reported a premature server connection closure error and supplied reproduction steps for the HumanSignal/label-studio repo
 * [today](https://github.com/microsoft/TypeScript-go/issues/2871#issuecomment-3941898803) **typescript-bot** reported that the server connection closed prematurely with undefined and listed affected repos and logs

### [PR microsoft/TypeScript-go#2872](https://github.com/microsoft/TypeScript-go/pull/2872) (Closed)

**Speed up source map emit with printer\-local monotomic cache**

*Introducing a printer-local monotonic cache for source map emission achieves up to 230× speedup and cuts memory allocations.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2873](https://github.com/microsoft/TypeScript-go/issues/2873) (Closed)

**dexie validation 7\.0\.0\-dev\.20260219\.1 works, 7\.0\.0\-dev\.20260222\.1 fails**

*Updating to dexie 7.0.0-dev.20260222.1 triggers a TS1540 'namespace' declaration error in dexie.d.ts that was not present in 7.0.0-dev.20260219.1*

 * created by **AntonOfTheWoods**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3942772816) **jakebailey** clarified that the deprecation messages are intentional, can be silenced in TS 6.0 but will be hard errors in TS 7.0, and linked issue #2760 and PR #62876
 * [today](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3942779567) **jakebailey** questioned the safety of doing this in declaration files, noted that Dexie.js used a handwritten .d.ts on TypeScript 5.6, and suggested patching the dependency
 * [today](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3942883536) **siphosenkosindhlovu** said "I can confirm this also happens for playwright-core@1.55.0"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3942907832) **jakebailey** said "Playwright already fixed this, in https://github.com/microsoft/playwright/pull/38558, released in v1.58."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3942915711) **AntonOfTheWoods** noted the README claim wasn't strictly true, asked if deprecation counts as an error, and offered to submit a fix to dexie
 * (today) **AntonOfTheWoods** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3942921426) **siphosenkosindhlovu** acknowledged missing the fix and thanked the contributor
 * [today](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3942927604) **jakebailey** acknowledged that the readme claim about parsing/scanning matching TS 6.0 wasn't strictly true when being pedantic
 * [today](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3943016313) **AntonOfTheWoods** mentioned that pedantry is typically beneficial in programming contexts

### [PR microsoft/TypeScript-go#2874](https://github.com/microsoft/TypeScript-go/pull/2874) (Open, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.32\.3 to 4\.32\.4 in the github\-actions group across 1 directory**

*Bump github/codeql-action from 4.32.3 to 4.32.4 to update the default CodeQL bundle and enhance proxy certificate handling and diagnostics.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [Issue microsoft/TypeScript-go#2875](https://github.com/microsoft/TypeScript-go/issues/2875) (Open, `Crash`)

**Occasional error invalid memory address/nil pointer dereference \- codeAction failed**

*TypeScript-Go LSP server intermittently panics with a nil pointer dereference when handling textDocument/codeAction requests.*

 * created by **lukpsaxo**
 * **lukpsaxo** added label `Crash`

