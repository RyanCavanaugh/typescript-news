# Report for 2026-03-30 (Monday, March 30th, 2026)

14 different users commented on 67 different issues.

## Recommended Actions

 * Response Recommended
    * @rubenferreira97 provided a minimal reproduction repository as requested in [microsoft/TypeScript-go#2666](https://github.com/microsoft/TypeScript-go/issues/2666#issuecomment-4161580561)
    * @ozyx offered to gather debug info in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4158120316)
    * @rubenferreira97 asked if the PR could be merged for testing in [microsoft/TypeScript-go#3243](https://github.com/microsoft/TypeScript-go/issues/3243#issuecomment-4161321466)

## Activity Summary

### [Issue microsoft/TypeScript-go#1032](https://github.com/microsoft/TypeScript-go/issues/1032) (Closed, `Domain: Type Checking`, `Type Ordering`)

**Change in inference from tuple to array**

*tsgo 7.0.0-dev changes tuple inference so Object.entries mapping yields string[][] instead of [string,string][], causing TS2345 type errors.*

 * **ahejlsberg** added label `Type Ordering`
 * [40 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1032#issuecomment-2994223243) **ahejlsberg** explained that the type inference failure was caused by picking the first candidate and proposed using InferencePriorityReturnType to produce a union type, and stated intent to create a PR
 * **jakebailey** removed label `wontfix`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1057](https://github.com/microsoft/TypeScript-go/issues/1057) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**, **Copilot**)

**Inconsistency involving discriminated union and flatMap**

*flatMap callback returning either InputOp[] or remove-only arrays causes a TypeScript discriminated union inference error*

 * **jakebailey** added label `Domain: Type Checking`
 * [42 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1057#issuecomment-2955800228) **ahejlsberg** explained that type inference for the arrow return in `flatMap` chose the first of two non-strict-supertype candidates due to union ordering differences, suggested using assignability as a tiebreaker or adding a type assertion as a workaround
 * **ahejlsberg** added label `Type Ordering`
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#1317](https://github.com/microsoft/TypeScript-go/issues/1317) (Open, `Domain: CLI`, `Domain: Performance`, **johnfav03**)

**High CPU usage with \-\-watch when idling on MacOS**

*Running tsgo in watch mode on MacOS consumes abnormally high CPU (120–170%) even when idle, unlike tsc -w.*

 * **jakebailey** added label `Domain: Performance`
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1317#issuecomment-3928808922) **nfarina** suggested adding fsevents support and a custom watcher.go to improve watch mode CPU usage by building a local tsgo binary
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/1317#issuecomment-4124796852) **alexswan93** reported similar idle CPU usage on Windows in watch mode with @typescript/native-preview v7.0.0-dev.20260324.1 and noted using tsgo as a workaround
 * **RyanCavanaugh** assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#136](https://github.com/microsoft/TypeScript-go/issues/136) (Closed, `Domain: Parser`)

**Import assertions parse incorrectly as ImportAttributes**

*Import assertions are incorrectly parsed as ImportAttributes because the import assertion feature has not yet been implemented.*

 * created by **sandersn**
 * **jakebailey** added label `Domain: Parser`
 * [today](https://github.com/microsoft/TypeScript-go/issues/136#issuecomment-4157823853) **RyanCavanaugh** said "This is fixed"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#137](https://github.com/microsoft/TypeScript-go/issues/137) (Closed, `Domain: Parser`)

**Incorrect, stray hashes parse differently than tsc**

*Stray hash characters in private class member names are parsed differently than in the TypeScript compiler.*

 * created by **sandersn**
 * **jakebailey** added label `Domain: Parser`
 * [today](https://github.com/microsoft/TypeScript-go/issues/137#issuecomment-4157822266) **RyanCavanaugh** said "Won't fix, not an invariant"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#141](https://github.com/microsoft/TypeScript-go/issues/141) (Closed, `Domain: Parser`)

**Invalid JSX parses more JSXSelfClosingTags than tsc**

*The parser incorrectly recognizes more self-closing JSX tags than the TypeScript compiler when handling invalid JSX constructs.*

 * created by **sandersn**
 * **jakebailey** added label `Domain: Parser`
 * [today](https://github.com/microsoft/TypeScript-go/issues/141#issuecomment-4157974402) **RyanCavanaugh** said "Won't fix"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1570](https://github.com/microsoft/TypeScript-go/issues/1570) (Open, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Nondeterministic declaration emit in test nodeModulesExportsSourceTs**

*The nodeModulesExportsSourceTs (nodenext) test’s baseline comparison is failing due to nondeterministic declaration file emits that omit inner module .d.ts files.*

 * created by **jakebailey**
 * (32 weeks ago) **jakebailey** added labels `bug`, `Domain: Declaration Emit`
 * **RyanCavanaugh** assigned to **weswigham**

### [Issue microsoft/TypeScript-go#2115](https://github.com/microsoft/TypeScript-go/issues/2115) (Open, `possible improvement`)

**Refactor checker pool to limit checker creation for foreground tasks, segment diagnostic checkers**

*Refactor the checker pool to separate foreground and diagnostic tasks, minimizing redundant checker creation and resource usage*

 * created by **jakebailey**
 * **RyanCavanaugh** added label `possible improvement`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#2125](https://github.com/microsoft/TypeScript-go/issues/2125) (Open, `possible improvement`)

**Unbounded memory consumption with recursive conditional types causes compilation OOM**

*Recursive conditional types on large numeric and string unions lead the TypeScript compiler to run out of memory and crash.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4011601474) **jakebailey** said "Editor growth is probably unrelated, and if you have a repro that would be very appreciated in a new issue."
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4012842570) **caomingpei** noted that the tsgo process triggered by VS Code consumed 20–30+ GB of memory causing unresponsiveness, suggested constraining editor/plugin integrations with explicit resource limits or startup parameters, and highlighted a difference between tsc and ts-go default behaviors
 * **RyanCavanaugh** added label `possible improvement`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#2186](https://github.com/microsoft/TypeScript-go/issues/2186) (Open, `bug`, **gabritto**)

**Broken assignability and quick info due to erroneously deferring keyof T since \#51621**

*Erroneously deferring keyof T since PR 51621 causes unsimplified quick info and invalid type assignments.*

 * created by **LukeAbby**
 * **RyanCavanaugh** added label `bug`
 * **RyanCavanaugh** assigned to **gabritto**

### [PR microsoft/TypeScript-go#2322](https://github.com/microsoft/TypeScript-go/pull/2322) (Closed)

**Remove GetOptionsDiagnostics, expose global diags in LSP**

*Remove the redundant GetOptionsDiagnostics API, expose separate config file parsing and real-time global diagnostics in the LSP.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2322#issuecomment-4057861525) **andrewbranch** asked whether diagnostic location presence was orthogonal to file check-in order dependency
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2322#issuecomment-4057866971) **jakebailey** said "Ah. I think we still can report global diagnostics on things like "Iterable is missing", which only happens when you finally ask for it somewhere. Would need to recheck."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2322#issuecomment-4057914264) **andrewbranch** suggested having a diagnostics bucket for checker initialization, noted that the change was fine as-is, clarified the scope of global diagnostics in the LSP, and offered approval once undrafted
 * [today](https://github.com/microsoft/TypeScript-go/pull/2322#issuecomment-4158591198) **jakebailey** said "Probably should just take #3285"

### [Issue microsoft/TypeScript-go#2364](https://github.com/microsoft/TypeScript-go/issues/2364) (Open, `possible improvement`)

**Provide document links in tsconfig/jsconfig files**

*Enable TypeScript to provide document links for extends, files, and references in tsconfig/jsconfig to improve IntelliSense consistency and reduce bugs.*

 * created by **mjbvz**
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2364#issuecomment-3647749264) **jakebailey** suggested adding JSON file patterns to the document selector to limit tsconfig JSON files
 * **RyanCavanaugh** added label `possible improvement`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#2384](https://github.com/microsoft/TypeScript-go/issues/2384) (Closed, `question`)

**slow Code Completion with use valibot schema define**

*TypeScript code completion becomes significantly slow when using Valibot to define large schemas.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2384#issuecomment-3672670301) **wszgrcy** thanked the maintainer, provided a link to the type file, and asked for modification suggestions to reduce type computation costs
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2384#issuecomment-3706542883) **fabian-hiller** suggested that the pipe function's 20 overload signatures may be causing the slowdown due to missing generic-related optimizations and provided a simplified example signature
 * **RyanCavanaugh** added label `question`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2384#issuecomment-4157809308) **RyanCavanaugh** said "Closing since this isn't a bug vis a vis the JS implementation."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2394](https://github.com/microsoft/TypeScript-go/issues/2394) (Open, `possible improvement`)

**Enable IntelliSense in staged files**

*Enable IntelliSense features like go-to-definition and document outline for staged files opened from the source control view.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2394#issuecomment-3662496414) **mjbvz** mentioned that git: files were ignored due to non-file URI challenges and suggested TS-go add basic support for other virtual file system schemes
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2394#issuecomment-3662503421) **jakebailey** said "Ah, so this is a feature request, not a bug report?"
 * **RyanCavanaugh** added label `possible improvement`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#2420](https://github.com/microsoft/TypeScript-go/issues/2420) (Open, `Crash`, **iisaduan**)

**vscode extension crashes on start**

*The TypeScript native-preview VSCode extension fails to initialize due to write EPIPE errors and an unterminated quoted string syntax error.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2420#issuecomment-3685399582) **Bashamega** said "I think these versions are buggy, because version 0.20251204.2 works fine, try upgrading"
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2420#issuecomment-3685539027) **PinkaminaDianePie** said "@Bashamega i don't even see such a version here https://marketplace.visualstudio.com/items?itemName=TypeScriptTeam.native-preview&ssr=false#version-history"
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2420#issuecomment-3685558502) **Bashamega** said "I am using cursor that uses vsx"
 * **RyanCavanaugh** assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#2424](https://github.com/microsoft/TypeScript-go/issues/2424) (Open, `possible improvement`)

**Request for support for additional architectures**

*Support and a roadmap are requested for riscv64, ppc64le, and loong64 architectures in typescript-go.*

 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-3720653589) **jakebailey** noted that esbuild builds all variants without testing and cautioned about the signing overhead with many optional dependencies
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-3721623829) **darkyzhou** clarified whether the concern about adding more architectures was mainly about increased CI running time and proposed starting support for riscv64, loong64, ppc64le, and s390x on Linux
 * **RyanCavanaugh** added label `possible improvement`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#2501](https://github.com/microsoft/TypeScript-go/issues/2501) (Open, `Crash`, **iisaduan**)

**textDocument/completion: runtime error: slice bounds out of range \[:2615\] with length 2590**

*The TypeScript-Go language server panics with a slice bounds out of range error during textDocument/completion requests.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2501#issuecomment-3747026777) **rubenferreira97** reported experiencing the error but was unable to reproduce it
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2501#issuecomment-3829141424) **frodi-karlsson** suggested adding bounds checking to LineAndCharacterToPosition to prevent panics when positions exceed text length
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2501#issuecomment-3829229887) **jakebailey** expressed concern that having them elsewhere could introduce mismatches and break things, and that this shouldn't be inevitable
 * **RyanCavanaugh** assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#2561](https://github.com/microsoft/TypeScript-go/issues/2561) (Open, `Crash`, **iisaduan**)

**v0\.20260119\.1 crashes ts server for large project, v0\.20260116\.1 works**

*TypeScript Native Preview v0.20260119.1 crashes the TS server on large, high-memory projects, whereas v0.20260116.1 works.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3791552923) **Titozzz** said "Seems like 0.20260122.4  is better, will report if issue rises again"
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3791740211) **austinfennacy** described memory usage issues across versions, noted a crash on version 0.20260119, observed fluctuating memory on 0.20260122.4, and indicated intent to keep auto-update enabled while leaving the issue open
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3791903072) **DanielRosenwasser** announced that the issue was solved by PR #2553, noted version 0.20260122.4 as a last-known-good release, and recommended against pinning to a specific extension version
 * **RyanCavanaugh** assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#2666](https://github.com/microsoft/TypeScript-go/issues/2666) (Open, `Needs Investigation`, **johnfav03**)

**\`tsgo \-\-build\` fails to invalidate incremental cache after dependency update**

*tsgo's --build incremental cache does not detect updated dependency types and ignores resulting type errors.*

 * created by **rubenferreira97**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2666#issuecomment-4161580561) **rubenferreira97** provided a minimal reproduction repository for the build bug using local dependencies

### [Issue microsoft/TypeScript-go#2683](https://github.com/microsoft/TypeScript-go/issues/2683) (Open, `bug`, **gabritto**)

**TS2590: "Expression produces a union type that is too complex to represent" on generics types**

*A generic type union in the @regle monorepo triggers TS2590 errors due to overly complex inferred types in newer TypeScript versions*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2683#issuecomment-3905132004) **victorgarciaesgi** described narrowing down the issue to a recursive type and fixing it with additional isAny and isUnknown checks, noted a crash in one package and inconsistent tsconfig include behavior, and said they would open another issue
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2683#issuecomment-3908046091) **victorgarciaesgi** found that the type helper crashed when augmenting a tuple with an optional first parameter and provided working and crashing examples
 * **RyanCavanaugh** added label `bug`
 * **RyanCavanaugh** assigned to **gabritto**

### [Issue microsoft/TypeScript-go#272](https://github.com/microsoft/TypeScript-go/issues/272) (Closed, `Domain: Porting Meta`)

**\`System\` vs \`Host\` vs \`Program\` layering**

*Clarify distribution of CompilerOptions subsets among System, Host, and Program layers for clearer architecture.*

 * created by **iisaduan**
 * **jakebailey** added label `Domain: Porting Meta`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4009619194) **shinichy** said "@andrewbranch I'm not sure if an NDA is possible at my company, but I'll look into it. I'll send an email anyway. Thanks for your help!"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4018362467) **shinichy** described that a generated re-export file with many subpath exports caused checker.getExportsOfModuleWorker to recurse deeply, and asked how to skip visiting the generated export and why the Strada language service didn’t exhibit the issue
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4047475814) **dbrxnds** said "Update: Unfortunately I just seemed to have gotten last time when I said things improved. These past 2 days have been the same as before."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4158120316) **ozyx** reported experiencing a massive memory leak in a large pnpm monorepo when using tsgo and offered to gather debug info

### [Issue microsoft/TypeScript-go#2791](https://github.com/microsoft/TypeScript-go/issues/2791) (Open, `possible improvement`)

**\[Feature Request\] Static C library**

*Enable tsgo distribution as a static and/or dynamic C library for embedding in native applications such as Rust.*

 * created by **alshdavid**
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2791#issuecomment-3906042750) **jakebailey** referred to a discussion link, noted it may be possible with caveats, and asked whether IPC or Wasm would work for the use case
 * **RyanCavanaugh** added label `possible improvement`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#2825](https://github.com/microsoft/TypeScript-go/issues/2825) (Closed, `question`)

**How will native library dependencies's CVEs be handled?**

*How can pnpm audit expose CVEs in native Go module dependencies and help downstream users identify related supply-chain vulnerabilities?*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2825#issuecomment-3923737892) **DanielRosenwasser** stated that they would publish an appropriate patch if a dependency had a CVE, report risks with the prior version, and involve @jakebailey's input
 * **DanielRosenwasser** added label `question`
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2825#issuecomment-3923751113) **jakebailey** noted encoding/json/v2 upcoming change, explained scanner over-reporting issues and govulncheck's advantages, and stated that forced rebuilds may be needed albeit unlikely given the small dependency set
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2836](https://github.com/microsoft/TypeScript-go/issues/2836) (Open, `possible improvement`)

**Cache \`getExePath\(\)\` for performance reasons**

*Cache getExePath results to avoid redundant lookups and improve tsgo invocation performance.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-3928400257) **jakebailey** questioned where caching would occur and explained why postinstall is avoided and no slowdown seems to come from platform checks
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-3928421769) **jakebailey** said "If the import is that slow, we could switch to using plain FS lookups, since peer deps must be "peers" in a parent dir..."
 * **RyanCavanaugh** added label `possible improvement`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#2875](https://github.com/microsoft/TypeScript-go/issues/2875) (Open, `Crash`, **iisaduan**)

**Occasional error invalid memory address/nil pointer dereference \- codeAction failed**

*TypeScript-Go LSP server intermittently panics with a nil pointer dereference when handling textDocument/codeAction requests.*

 * created by **lukpsaxo**
 * **lukpsaxo** added label `Crash`
 * **RyanCavanaugh** assigned to **iisaduan**

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*Add draft formatting tests to validate and troubleshoot the repository’s testing pipelines.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4148801620) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4152659049) **typescript-bot** provided the requested perf run results
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4152679800) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4158591248) **iisaduan** said "@typescript-bot test top100"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4158591498) **typescript-bot** said "Hey @iisaduan, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4158631456) **iisaduan** said "@typescript-bot test top100"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4158631722) **typescript-bot** reported that the test top100 build failed due to validation errors or warnings
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4158701169) **typescript-bot** provided the requested perf run results to @iisaduan
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4158717642) **gabritto** said "@typescript-bot test tsserver top10"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4158717868) **typescript-bot** reported that the test tsserver top10 job failed to queue due to validation errors or warnings
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4158719196) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."

### [Issue microsoft/TypeScript-go#2959](https://github.com/microsoft/TypeScript-go/issues/2959) (Open, `Crash`, **iisaduan**)

**panic handling request textDocument/definition: bad line number**

*The TypeScript Go LSP server panics in textDocument/definition when an out-of-range line number is passed to the line-and-character to position converter.*

 * created by **Zzzen**
 * **Zzzen** added label `Crash`
 * **RyanCavanaugh** assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#3027](https://github.com/microsoft/TypeScript-go/issues/3027) (Closed)

**New TS2883 "\.\.\. cannot be named \.\.\." error exporting an arrow function\.**

*Arrow-exported functions with CSSProperties['cursor'] return types trigger TS2883 in TS 7.0 preview due to unnamed csstype dependencies, unlike function declarations.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3027#issuecomment-4021083531) **simonbuchan** said "Those are TS4023 and TS4053 so they are at least hitting a different code path, but there does seem to be some relation."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3027#issuecomment-4155024237) **RyanCavanaugh** reported that nightly now emitted the foo and bar declarations without error
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3027#issuecomment-4157257550) **simonbuchan** said "Awesome! I'll fire it up again when I get in today, see if there's anything else that was buried by these."

### [Issue microsoft/TypeScript-go#3072](https://github.com/microsoft/TypeScript-go/issues/3072) (Closed)

**getTargetOfType panics on non\-generic types via the api server**

*getTargetOfType panics on intersection or union types instead of returning null as expected*

 * [today](https://github.com/microsoft/TypeScript-go/issues/3072#issuecomment-4154998438) **RyanCavanaugh** disagreed with the assessment that returning an error rather than null is semantically correct, argued that returning null implies a successful operation and conflates illegal and legal nil targets
 * [today](https://github.com/microsoft/TypeScript-go/issues/3072#issuecomment-4156038896) **RyanCavanaugh** noted that the TS API restricts calls to legal types, so this case is analogous to other malformed requests triggering asserts
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3072#issuecomment-4156415096) **souporserious** acknowledged the explanation and explained they were parsing the AST binary themselves for lower-level access in Go

### [Issue microsoft/TypeScript-go#3094](https://github.com/microsoft/TypeScript-go/issues/3094) (Open, `bug`, **weswigham**)

**Declaration emit proceeds in the presence of TS7056**

*TypeScript emits declarations despite TS7056 errors caused by deeply nested conditional and tag-branded utility types.*

 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3094#issuecomment-4068324272) **hkleungai** noted that the TS4053 error resembled a previously reported issue, argued that ts6 and ts7 should resolve the type reference without error, and referenced related issues #2504 and #3027
 * [today](https://github.com/microsoft/TypeScript-go/issues/3094#issuecomment-4158824453) **weswigham** provided a status update on declaration emit behaviour in corsa versus strada, mentioned a 4-line diff to align implementations, and noted ongoing debugging of -b unit test failures

### [PR microsoft/TypeScript-go#3118](https://github.com/microsoft/TypeScript-go/pull/3118) (Closed)

**Fix difference between checker and binder resolvers**

*Re-align checker and binder resolvers by restoring getReferencedValueOrAliasSymbol and replacing obsolete symbol resolution functions.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3118#issuecomment-4144324035) **weswigham** discussed the potential for an emit checker mode, noted that PR #1301 addressed some checker-versus-emit issues but introduced regressions, restored getReferencedValueOrAliasSymbol to align with Strada, and asked whether this change regressed VSCode nocheck emit performance or required further fixes
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3118#issuecomment-4144343140) **jakebailey** said "I forgot to mention it, but I did check, and it still seems fast. I will recheck."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3118#issuecomment-4145012454) **jakebailey** compared performance metrics of the tsgo binary before #2396, on main, and in this PR using a quick bash script on VSCode
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3120](https://github.com/microsoft/TypeScript-go/issues/3120) (Open, `Crash`, **iisaduan**)

**thread exhaustion \- program exceeds 10000\-thread limit \- one off error**

*An unreproducible Go runtime crash arises when the program exceeds the 10000-thread limit.*

 * created by **lukpsaxo**
 * **lukpsaxo** added label `Crash`
 * **RyanCavanaugh** assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#313](https://github.com/microsoft/TypeScript-go/issues/313) (Closed, `Domain: Binder`)

**binder: expando declarations don't show up on symbol**

*Expando declarations are not emitted on default exports, interface merges, overloaded functions, keyword-named expandos, or element accesses.*

 * [1 year ago](https://github.com/microsoft/TypeScript-go/issues/313#issuecomment-2669908966) **sandersn** described the discrepancy in namespace declarations for `Point` between Strada and Corsa and proposed a synthetic JS-only namespace feature for `Point.zero`, outlining binder, checker, and language service requirements
 * **jakebailey** added label `Domain: Binder`
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/313#issuecomment-3923610589) **ahejlsberg** noted that the binder was working as intended, pointed out remaining declaration emit differences captured in baselines, and asked to close the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/313#issuecomment-4157998166) **sandersn** said "Sounds like the baselines diffs are gone except for declaration emit, so I think this is OK to close."
 * (today) **sandersn** closed the issue

### [PR microsoft/TypeScript-go#3228](https://github.com/microsoft/TypeScript-go/pull/3228) (Open, **DanielRosenwasser**, **Copilot**)

**Track file extension in LSP request failure telemetry**

*Include an optional fileExtension field in LSP request failure telemetry to capture the affected file type.*

 * created by **Copilot**
 * (5 days ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3228#issuecomment-4156546121) **DanielRosenwasser** said "@copilot+claude-sonnet-4.6 merge from main and resolve conflicts"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3228#issuecomment-4156638191) **Copilot** merged from main and resolved two conflicts in server.go

### [PR microsoft/TypeScript-go#3234](https://github.com/microsoft/TypeScript-go/pull/3234) (Closed, **andrewbranch**, **Copilot**)

**Add diagnostic API methods**

*Add API methods for syntactic, semantic, suggestion, config file parsing, and declaration diagnostics with async server calls and range-based tests.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3234#issuecomment-4136298113) **Copilot** removed omitempty from reportsUnnecessary and reportsDeprecated, ran the formatter, and noted retention of the getGlobalDiagnostics test due to a pre-existing type assertion bug
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3234#issuecomment-4136624785) **andrewbranch** said "@copilot just remove getGlobalDiagnostics from the API for now."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3234#issuecomment-4136685418) **Copilot** removed getGlobalDiagnostics from the Go protocol, session handler, and TypeScript Program class along with its tests in both async and sync suites
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3243](https://github.com/microsoft/TypeScript-go/issues/3243) (Closed, `Domain: Editor`, **andrewbranch**, **Copilot**)

**Auto\-import adds type to value import instead of using existing import type \(Follow\-up to PR \#2978\)**

*Auto-import adds type specifiers to value import statements instead of merging them into existing type-only import blocks.*

 * (4 days ago) **andrewbranch** added label `Domain: Editor`, and assigned to **Copilot**, **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3243#issuecomment-4161321466) **rubenferreira97** noted that Copilot didn't link PR #3244 to the issue and asked if it could be merged for a test run
 * (later) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3244](https://github.com/microsoft/TypeScript-go/pull/3244) (Closed, **andrewbranch**, **Copilot**)

**Fix auto\-import to prefer existing \`import type\` declarations**

*Modify auto-import logic to prefer merging type imports into existing `import type` declarations instead of adding inline type modifiers on value imports.*

 * **Copilot** assigned to **andrewbranch**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3244#issuecomment-4137439470) **andrewbranch** said "@copilot+claude-opus-4.6 since this causes existing tests to be removed from the failing list, you can delete your new test."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3244#issuecomment-4137493300) **Copilot** removed the new test file because existing tests already covered it
 * (later) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3249](https://github.com/microsoft/TypeScript-go/issues/3249) (Open, `possible improvement`)

**Report perf measurements from extension**

*Collect and report performance metrics for language service operations in the extension to track regressions and improvements.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added to milestone `TypeScript 7.0 RC`
 * **RyanCavanaugh** added label `possible improvement`
 * (today) **RyanCavanaugh** set milestone to `Possible Improvement`, and removed from milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3259](https://github.com/microsoft/TypeScript-go/issues/3259) (Open, `possible improvement`)

**Proposal: Flatten the AST to speed up tsgo**

*Proposes flattening tsgo’s AST into a flat array to reduce garbage collection scanning overhead and improve performance.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3259#issuecomment-4144353592) **DanielRosenwasser** explained that replacing pointers with indexes would complicate API by requiring arena context and noted that slimming down nodeData was risky with minimal savings
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3259#issuecomment-4144699877) **ahejlsberg** suggested disabling GC for command-line compiles due to minimal GC-eligible allocations
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3259#issuecomment-4147318834) **no-yan** clarified that the goal was reducing GC scan cost rather than DoD/locality, explained that GC still scans contiguous nodes containing pointers, suggested making large pointer-free regions to avoid scanning, and recommended disabling or tuning GC for command-line compiles
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3263](https://github.com/microsoft/TypeScript-go/pull/3263) (Open)

**Preserve original comments on params in dts generated by pseudo type node builder under \`removeComments: false\`**

*Declaration files generated by the pseudo type node builder with removeComments disabled fail to preserve original parameter comments.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3263#issuecomment-4156791336) **jakebailey** said "At some level, I wonder if this is even worth it."

### [PR microsoft/TypeScript-go#3265](https://github.com/microsoft/TypeScript-go/pull/3265) (Closed)

**Fix dts emit for type params for object methods in const context**

*Correct generation of d.ts definitions for type parameters of object methods declared in const contexts.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3278](https://github.com/microsoft/TypeScript-go/issues/3278) (Closed, `Domain: Editor`, **jakebailey**)

**Add one\-time prompt to enable extension**

*Add a one-time prompt to enable the native preview language server when the extension is first activated.*

 * created by **DanielRosenwasser**
 * (3 days ago) **DanielRosenwasser** added label `Domain: Editor`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3279](https://github.com/microsoft/TypeScript-go/pull/3279) (Closed)

**Set js/ts\.experimental\.useTsgo on first run**

*Automatically enable the js/ts.experimental.useTsgo setting on first activation when unset.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3282](https://github.com/microsoft/TypeScript-go/pull/3282) (Closed)

**Don't send progress reports for very short spans**

*Add a 250ms delay before sending progress tokens to prevent excessive reporting for very short spans.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3293](https://github.com/microsoft/TypeScript-go/pull/3293) (Closed)

**Accept baseline diffs, round 2**

*Accepts a second batch of baseline diffs to update the project’s accepted baselines.*

 * created by **ahejlsberg**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3299](https://github.com/microsoft/TypeScript-go/pull/3299) (Closed)

**Refactor and improve generated LSP code**

*Refactor the generated LSP protocol code to eliminate redundant JSON decoding by improving union discrimination and registration option typing.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3300](https://github.com/microsoft/TypeScript-go/pull/3300) (Open)

**Rename core\.Pool to core\.Arena**

*Propose renaming core.Pool to core.Arena to accurately reflect its bump allocator functionality.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3301](https://github.com/microsoft/TypeScript-go/pull/3301) (Open, **RyanCavanaugh**, **Copilot**)

**Fix type inference ordering inconsistency with discriminated unions and flatMap**

*Replace subtype-based tiebreaker with asymmetric assignability to fix inconsistent discriminated union inference in flatMap.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3302](https://github.com/microsoft/TypeScript-go/issues/3302) (Closed, `Needs More Info`)

**panic crash**

*The TypeScript-Go language server panics with a slice bounds out of range error when processing hover requests.*

 * created by **ShenHongFei**

### [Issue microsoft/TypeScript-go#460](https://github.com/microsoft/TypeScript-go/issues/460) (Open, `Domain: API and Extensibility`)

**Yarn PnP**

*Add native Yarn PnP support to experimental TypeScript via a static resolution map to enhance stability and security.*

 * [1 year ago](https://github.com/microsoft/TypeScript-go/issues/460#issuecomment-2715637998) **jakebailey** mentioned that implementing this feature could be technically better in Go due to built-in zip support and FS wrapper, and suggested exploring it
 * [44 weeks ago](https://github.com/microsoft/TypeScript-go/issues/460#issuecomment-2907325842) **pauldraper** expressed support for compatibility between Yarn PnP and typescript-go and lamented potential inability to use both together
 * **jakebailey** added label `Domain: API and Extensibility`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#464](https://github.com/microsoft/TypeScript-go/issues/464) (Closed, `Domain: API and Extensibility`)

**jest**

*Requesting instructions on how to integrate and use this library with Jest.*

 * created by **createthis**
 * [1 year ago](https://github.com/microsoft/TypeScript-go/issues/464#issuecomment-2715103936) **RyanCavanaugh** said "Not yet? 🙂"
 * **jakebailey** added label `Domain: API and Extensibility`
 * [today](https://github.com/microsoft/TypeScript-go/issues/464#issuecomment-4157986068) **RyanCavanaugh** expressed uncertainty about the requested feature and clarified that on-the-fly transpilers support tsgo syntax and an official API scenario is planned post-7.0
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#504](https://github.com/microsoft/TypeScript-go/issues/504) (Open, `Domain: API and Extensibility`)

**Feature Suggestion: Static Indexing Format for Compiler**

*Propose adding a static code indexing export format from the TypeScript compiler to enable offline, language-agnostic type-aware tools.*

 * [1 year ago](https://github.com/microsoft/TypeScript-go/issues/504#issuecomment-2717520803) **jakebailey** noted that issue #514 addresses the topic, expressed confusion about performance numbers, recommended posting testing methodology there, and pointed out that concurrency is incorrectly enabled in WASM by default, deeming this thread off-topic
 * [1 year ago](https://github.com/microsoft/TypeScript-go/issues/504#issuecomment-2717525805) **jakebailey** noted they were working on API support and that NAPI was infeasible for Go because multiple Go libraries cannot be loaded into the same process safely
 * **jakebailey** added label `Domain: API and Extensibility`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#648](https://github.com/microsoft/TypeScript-go/issues/648) (Open, `Domain: API and Extensibility`)

**Support embedded JavaScript/TypeScript**

*Enable built-in handling of embedded JavaScript/TypeScript in languages such as MDX, Vue, Svelte, Astro, and Markdown in the Go rewrite.*

 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3699085966) **auvred** suggested that a unified plugin architecture could allow language extensions to run in separate processes and be written in any language and noted that tsgo would be a nicer plugin host
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3928741504) **andrewbranch** opened a related issue (#2824) and requested expert feedback
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3935957954) **silverwind** noted community projects emerging to fill missing embedded language support in tsgo
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#657](https://github.com/microsoft/TypeScript-go/issues/657) (Open, `Domain: Porting Meta`, `Domain: Performance`, `possible improvement`)

**Use Profile\-Guided Optimization \(PGO\) for the compiler itself**

*Incorporate Profile-Guided Optimization into the Go-based TypeScript compiler via benchmarks, build scripts, and CI integration.*

 * [1 year ago](https://github.com/microsoft/TypeScript-go/issues/657#issuecomment-2735299840) **jakebailey** explained that they needed to run the benchmark on a dedicated performance machine configured to use a single physical core, and that they must find a new approach now that they have more cores
 * (42 weeks ago) **jakebailey** added labels `Domain: Porting Meta`, `Domain: Performance`
 * (today) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`

### [Issue microsoft/TypeScript-go#759](https://github.com/microsoft/TypeScript-go/issues/759) (Closed, `Domain: Porting Meta`)

**Is there any reason to sort named member symbols in structured type properties?**

*Proposal to limit sorting of structured type properties to error message formatting to reduce tsgo --noEmit execution time*

 * [51 weeks ago](https://github.com/microsoft/TypeScript-go/issues/759#issuecomment-2783987271) **auvred** reported that the percentage decreased from 2.6% to 2.2% on microsoft/vscode
 * [51 weeks ago](https://github.com/microsoft/TypeScript-go/issues/759#issuecomment-2783995201) **jakebailey** said "Interesting, given the original trace was about the same length of time, but GetSourceFileOfNode was not a big factor there. Definitely, better, though."
 * **jakebailey** added label `Domain: Porting Meta`
 * [today](https://github.com/microsoft/TypeScript-go/issues/759#issuecomment-4158107490) **RyanCavanaugh** said "Order of property enumeration, internally, definitely matters. If someone can prove that moving that sort to a different codepath is better we would look at that PR, but it's not for nothing."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#771](https://github.com/microsoft/TypeScript-go/issues/771) (Closed, `Domain: Porting Meta`, `Domain: Performance`)

**Benchmark suggestion, power usage**

*Propose measuring and benchmarking power usage to evaluate energy efficiency improvements in the Go-based compiler variant.*

 * created by **jaenster**
 * (42 weeks ago) **jakebailey** added labels `Domain: Porting Meta`, `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript-go/issues/771#issuecomment-4158046829) **RyanCavanaugh** said "I don't really know any off-the-shelf tools for doing this. It'd be a great blog post for a community member, maybe someone wants to look into it?"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#974](https://github.com/microsoft/TypeScript-go/issues/974) (Closed, `Domain: Module Resolution`, `node10 resolution`)

**Import behavior mismatch from typescript 5 \(bwip\-js\)**

*tsgo cannot find module 'bwip-js' import that tsc accepts, causing a TS2307 error.*

 * [39 weeks ago](https://github.com/microsoft/TypeScript-go/issues/974#issuecomment-3010389752) **jakebailey** apologized for not noticing the original issue filer, explained that using moduleResolution: Node (implying CommonJS) is unsupported by tsgo, and recommended switching to nodenext resolution to fix compilation
 * [39 weeks ago](https://github.com/microsoft/TypeScript-go/issues/974#issuecomment-3010396150) **jakebailey** said "See also: https://www.typescriptlang.org/docs/handbook/modules/guides/choosing-compiler-options.html"
 * **jakebailey** added label `node10 resolution`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#988](https://github.com/microsoft/TypeScript-go/issues/988) (Open, `Domain: Type Checking`, `Type Ordering`, `Domain: Performance`, **jakebailey**)

**tsgo "Type instantiation is excessively deep and possibly infinite" error when using react\-hook\-form**

*tsgo reports excessively deep type instantiation errors on two react-hook-form forms when spreading useForm into FormProvider, unlike tsc.*

 * [37 weeks ago](https://github.com/microsoft/TypeScript-go/issues/988#issuecomment-3050601116) **jakebailey** investigated memory allocation during error printing, identified type ordering and ts-expect-error filters as potential causes, and planned further diagnostics focusing on getTypeNamesForErrorDisplay
 * (33 weeks ago) **jakebailey** added labels `Domain: Performance`, `Type Ordering`
 * **RyanCavanaugh** assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/988#issuecomment-4158122110) **jakebailey** said "@justinsmid I haven't looked at this in a while; with #2459 merged it's possible this won't happen anymore. Have you used tsgo recently?"

