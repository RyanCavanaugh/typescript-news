# Report for 2026-09-01 (Tuesday, September 1st, 2026)

24 different users commented on 58 different issues.

## Recommended Actions

 * Response Recommended
    * @LukeAbby asked about handling of typeRelatedToDiscriminatedType special case in [microsoft/TypeScript#64113](https://github.com/microsoft/TypeScript/issues/64113#issuecomment-5504318190)
    * @LukeAbby asked about contextual typing of 'not' types in function parameters and returns in [microsoft/TypeScript#64113](https://github.com/microsoft/TypeScript/issues/64113#issuecomment-5504459251)

## Activity Summary

### [Issue microsoft/TypeScript#12936](https://github.com/microsoft/TypeScript/issues/12936) (Open, `Suggestion`, `Awaiting More Feedback`)

**Exact Types**

*Introduce an Exact<T> type (e.g. |T|) to enforce exact object types and disallow extra properties.*

 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5491147943) **codpro2005** provided a TypeScript Exact<T, TTarget> type guard and an 'exact' helper function to enforce exact object types, with accompanying playground examples
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5491383358) **ClementValot** criticized the practice of pasting untested AI-generated code, noted that the combination of wording, formatting, and opaque code caused concern, and suggested splitting the type into named types to improve performance and readability
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5491430359) **codpro2005** responded that they authored all code, kept the post compact to avoid pollution, noted playground links contain tests, and acknowledged feedback on readability, performance, and the proof-of-concept nature
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5499071549) **BinToss** suggested setting a recursion limit of ~16 for class inheritance to avoid TypeScript's infinite-recursion errors and mitigate performance issues in TS<6, and provided a link to an article

### [Issue microsoft/TypeScript#29112](https://github.com/microsoft/TypeScript/issues/29112) (Closed, `Bug`, `Fixed`, `Domain: Mapped Types`, `Needs Human Review`)

**Excessive stack depth comparing types with TS 3\.2 **

*TypeScript 3.2.2 fails to compile a generic function using lodash’s PartialDeep and pick due to an excessive stack depth comparing types error.*

 * [4.1 years ago](https://github.com/microsoft/TypeScript/issues/29112#issuecomment-1179243801) **AaravShah042** reported facing the same “Excessive stack depth comparing types” issue
 * [4 years ago](https://github.com/microsoft/TypeScript/issues/29112#issuecomment-1227460812) **Lyokolux** reported also facing the issue when comparing two arrays with Prisma CreateInput types
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/29112#issuecomment-2862709378) **oom-** described encountering an intermittent TS2321 excessive stack depth error with a custom type and suggested adding a --max-depth compilation flag
 * [today](https://github.com/microsoft/TypeScript/issues/29112#issuecomment-5497915189) **RyanCavanaugh** stated that a fix in PR #33144 addressed the recursive `PartialDeep` TS2321 error, included in TypeScript 3.7, and that it compiles in 3.7.2 and nightly but failed under `--strict` in 3.6.2
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#30176](https://github.com/microsoft/TypeScript/issues/30176) (Closed, `Bug`, `Domain: JSDoc`, `Needs Human Review`)

**JSDoc Class extending Array not supported \(?\)**

*VSCode fails to recognize JSDoc generics on a custom Array subclass, ignoring both element types and its methods.*

 * (7.5 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: JSDoc`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/30176#issuecomment-5498848809) **RyanCavanaugh** explained that FooArray.<XYZ> required a declared type parameter and provided a corrected JSDoc example for extending Array
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#30269](https://github.com/microsoft/TypeScript/issues/30269) (Closed, `Bug`, `Needs More Info`, `Crash`, `Domain: Crashes`)

**TypeError: Cannot read property 'kind' of undefined**

*Renaming a React component and dropping its interface props causes the TypeScript language server to throw a “Cannot read property 'kind' of undefined” error.*

 * (7.4 years ago) **RyanCavanaugh** added label `Domain: Crashes`, removed label `Needs Investigation`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/30269#issuecomment-5499453340) **RyanCavanaugh** asked for missing route declaration, React declarations, tsconfig settings, complete before-and-after file contents, cursor location, and editor action to reproduce signature help issue
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * (today) **pocesar** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#30451](https://github.com/microsoft/TypeScript/issues/30451) (Closed, `Bug`, `Domain: JSDoc`, `Needs Human Review`)

**Inconsistent error reporting for duplicate JSDoc tags**

*TypeScript only flags duplicate JSDoc tags within the same comment while ignoring redundancies across separate comments.*

 * (7.4 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: JSDoc`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/30451#issuecomment-5499716547) **RyanCavanaugh** stated that the issue was covered by #24996 requesting duplicate JSDoc diagnostics for annotations in separate locations and noted that the original example still lacked a diagnostic for v in TS 3.4.5 or 7.1.0-dev.20260901.1 while v2 reported TS1223
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#30669](https://github.com/microsoft/TypeScript/issues/30669) (Closed, `Bug`, `Domain: lib.d.ts`, `Needs Human Review`)

**event argument has no target\.result property on  IDBRequest: success event**

*TypeScript's IDBRequest event definitions omit the result property on event.target, causing errors in onsuccess handlers.*

 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/30669#issuecomment-762694955) **grzegorzjudas** said "Looks like this issue is still there. Have you been able to resolve it somehow?"
 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/30669#issuecomment-1396575573) **jibi966** said "Hi, is there any progress on this bug? I can't actually catch some DOM Exception due to this. (currently maintaining by @ts-ignore)"
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/30669#issuecomment-1913715395) **randomchars42** noted that the issue was related to #28293 and that a workaround was available
 * [today](https://github.com/microsoft/TypeScript/issues/30669#issuecomment-5500171093) **RyanCavanaugh** noted that the issue duplicated #28293 and reproduced TS2339 for event.target.result in TypeScript dev builds
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#30693](https://github.com/microsoft/TypeScript/issues/30693) (Closed, `Bug`, `Fixed`, `Domain: JS Emit`, `Needs Human Review`)

**If not all sources are under rootDir, you only get an error message when combined with outDir, not with outFile**

*Compiling with --outFile causes TypeScript to ignore rootDir and not error on files outside it, causing incorrect AMD outputs.*

 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/30693#issuecomment-1002083050) **antonio-rodrigues** explained that they needed to enable composite in tsconfig and add the dist folder to paths to make it work
 * [4 years ago](https://github.com/microsoft/TypeScript/issues/30693#issuecomment-1196868279) **xgqfrms** recommended using the exclude option in tsconfig to omit specified files and linked a StackOverflow solution
 * **RyanCavanaugh** added label `Domain: JS Emit`
 * [today](https://github.com/microsoft/TypeScript/issues/30693#issuecomment-5501494961) **RyanCavanaugh** described that TypeScript 4.3 began reporting TS6059 for AMD outFile inputs outside rootDir and clarified the misuse of the `includes` property
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#30708](https://github.com/microsoft/TypeScript/issues/30708) (Closed, `Bug`, `Fixed`, `Domain: Conditional Types`, `Needs Human Review`)

**Nested conditional type with generic tuple argument always expands to false branch\.**

*Generic nested conditional types comparing tuples in TypeScript 3.4 wrongly collapse to the false branch instead of preserving dependency.*

 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/30708#issuecomment-581049823) **sktw** described a bug where `IsOptional` incorrectly marked a potentially optional generic property as required and provided an alternative implementation that avoids the issue
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/30708#issuecomment-1977952037) **jcalz** asked if there was a general bug report and if they should close this issue and open a new one
 * **RyanCavanaugh** added label `Domain: Conditional Types`
 * [today](https://github.com/microsoft/TypeScript/issues/30708#issuecomment-5503640195) **RyanCavanaugh** noted that the issue was fixed and explained conditional type evaluation changes introduced by PR #42248
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#31066](https://github.com/microsoft/TypeScript/issues/31066) (Closed, `Bug`, `Fixed`, `Domain: lib.d.ts`, `Needs Human Review`)

**Compiling async/await to ES5 may fail to warn about missing Promise constructor**

*When targeting ES5, async/await compilation in TypeScript does not error for missing Promise constructor, causing runtime failures.*

 * [7.3 years ago](https://github.com/microsoft/TypeScript/issues/31066#issuecomment-485642145) **jwmerrill** expressed interest in the check to ensure code remains IE11-compatible and disallows async/await where forbidden
 * [6.3 years ago](https://github.com/microsoft/TypeScript/issues/31066#issuecomment-631029314) **aleksei-berezkin** asked for background on the commit that moved the Promise interface into lib.es5.d.ts and noted that Promise should be ES6-only
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [later](https://github.com/microsoft/TypeScript/issues/31066#issuecomment-5507768544) **RyanCavanaugh** noted that ES5 targeting was removed after TS 6.0.2, previews now raise TS5108 errors, and the async/await downlevel-ES5 scenario no longer applies in 7.1.0-dev
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#31426](https://github.com/microsoft/TypeScript/issues/31426) (Open, `Bug`, `Domain: classes`, `Needs Human Review`)

**\[3\.5\.0\-dev\.20190516\] Incorrect type error for mixin**

*Using interface-based mixin notation in TypeScript incorrectly reports type errors for property usage in mixin methods.*

 * (5.9 years ago) **RyanCavanaugh** added label `Domain: classes`, and set milestone to `Backlog`
 * **jakebailey** removed label `Fix Available`
 * [later](https://github.com/microsoft/TypeScript/issues/31426#issuecomment-5509068107) **RyanCavanaugh** explained that the TS2339 error no longer occurs in TypeScript 7.1.0-dev.20260902.1 and is replaced by TS7023 and TS2310 due to a circular Quark mixin declaration, and noted that circularity errors may occur
 * **RyanCavanaugh** added label `Needs Human Review`

### [Issue microsoft/TypeScript#31549](https://github.com/microsoft/TypeScript/issues/31549) (Open, `Bug`, `Domain: Indexed Access Types`, `Needs Human Review`)

**Regression: Type T\[K\] as an array when sliced loses its type**

*TypeScript 3.4.5 regresses by losing the specific T[K] type when slicing a generic array property.*

 * (7 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Indexed Access Types`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/31549#issuecomment-5509559852) **RyanCavanaugh** explained that the assignment is unsound because slice returns a plain U[] which may not satisfy the original T[K] subtype, referencing the generic-constraint rule and TS2322 diagnostic
 * **RyanCavanaugh** added label `Needs Human Review`

### [Issue microsoft/TypeScript#31613](https://github.com/microsoft/TypeScript/issues/31613) (Closed, `Bug`, `Needs Proposal`, `Domain: check: Control Flow`, `Needs Human Review`)

**Type narrowing not working for unions of tuples with object literals**

*TypeScript does not narrow unions of tuples containing object literals based on discriminant property checks.*

 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/31613#issuecomment-1162151385) **jtbandes** said "Possibly related: https://github.com/microsoft/TypeScript/issues/48378"
 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/31613#issuecomment-1162657933) **squidfunk** asked if the issue was dead after being repeatedly rescheduled and noted that a fix would improve expressivity
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/31613#issuecomment-2848783407) **rauschma** provided code examples showing that tuple union rest parameters didn’t work
 * [later](https://github.com/microsoft/TypeScript/issues/31613#issuecomment-5509999155) **RyanCavanaugh** marked the issue as a duplicate of #18758 and explained that tuple positions versus named outer properties do not affect the control-flow narrowing limitation for nested discriminants
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#31667](https://github.com/microsoft/TypeScript/issues/31667) (Open, `Bug`, `Needs More Info`, `Domain: JavaScript`, `Needs Human Review`)

**Type narrowing in checked JS in module scope doesn't work**

*In checked JavaScript module scope TypeScript doesn’t apply instanceof type narrowing for variables, although it works inside functions.*

 * (7.2 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: JavaScript`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/31667#issuecomment-5510264647) **RyanCavanaugh** couldn't reproduce the reported errors from the provided files and requested the tsconfig.json, any declarations or imports, the exact tsc command, and diagnostics on the guarded calls
 * (later) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#32111](https://github.com/microsoft/TypeScript/issues/32111) (Closed, `Bug`, `Needs More Info`, `Crash`, `Domain: Performance`, `Needs Human Review`)

**Language service OOM on lodash DT tests when batch compilation succeeds**

*Language service operations for lodash DefinitelyTyped tests cause out-of-memory errors even though batch compilation succeeds.*

 * (7.1 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Performance`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/32111#issuecomment-5511285423) **RyanCavanaugh** requested detailed repro information (source file, position, request type, and log or payload) to recreate the language-service request
 * (later) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#35942](https://github.com/microsoft/TypeScript/issues/35942) (Closed, `Bug`, `Domain: Parser`)

**Missing syntax error for destructuring with private names**

*TypeScript fails to report syntax errors for destructuring assignments using private class fields.*

 * (6.5 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Parser`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#46135](https://github.com/microsoft/TypeScript/issues/46135) (Closed, `Suggestion`, `Awaiting More Feedback`, **gabritto**)

**Ambient Module Declarations for Import Attributes \(formerly known as Import Assertions\)**

*Enable ambient module declarations based on import attributes to provide type definitions for CSS modules and asset URL imports.*

 * **gabritto** assigned to **gabritto**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-5479995982) **tomaswrobel** said "Will the issue be implemented in a way that "fit the merge criteria for post-6.0 patches"?"
 * (yesterday) **gabritto** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-5498379097) **jonathantneal** said "Thank you so incredibly much, @gabritto . 🙏❤️"
 * [today](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-5498844938) **RyanCavanaugh** stated that it will not be backported to 6.0

### [Issue microsoft/TypeScript#62179](https://github.com/microsoft/TypeScript/issues/62179) (Closed, `Bug`, `Help Wanted`, `Domain: ES Modules`)

**ImportType attributes can include JS expressions**

*TypeScript parser wrongly permits arbitrary JavaScript expressions in import type assertion attributes instead of only string literals or types.*

 * (1 year ago) **RyanCavanaugh** added label `Domain: ES Modules`, and set milestone to `Backlog`
 * [45 weeks ago](https://github.com/microsoft/TypeScript/issues/62179#issuecomment-3422857354) **sdotson** said "I'll give it a go: https://github.com/microsoft/TypeScript/pull/62638"
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703) (Open, `Planning`)

**TypeScript 7\.1 Iteration Plan**

*TypeScript 7.1 release plan outlining key milestones and proposed language, editor, and performance enhancements.*

 * **DanielRosenwasser** added label `Planning`
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5146188990) **dasa** said "2027, is that a typo?"
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5146248499) **DanielRosenwasser** said "Sure is! 🫠🤦‍♂️"
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5501016536) **DanielRosenwasser** announced that the beta release would be delayed by two weeks for additional API testing, with further details on RC and final release dates to follow

### [PR microsoft/TypeScript#63764](https://github.com/microsoft/TypeScript/pull/63764) (Closed, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump adm\-zip from 0\.5\.18 to 0\.6\.0**

*Upgrade adm-zip to v0.6.0 to fix a critical security vulnerability, add TypeScript types, and resolve several bugs*

 * (1 week ago) **dependabot[bot]** added labels `dependencies`, `javascript`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63764#issuecomment-5500297493) **dependabot[bot]** said "Looks like adm-zip is up-to-date now, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript#63873](https://github.com/microsoft/TypeScript/issues/63873) (Open, `Needs Investigation`, **andrewbranch**)

**Add batched assignability checks into the \`Checker API\`**

*Add batched type assignability checks and optional quantifiers to the Checker API for improved performance.*

 * created by **artem1458**
 * (1 month ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/63873#issuecomment-5504529919) **weswigham** said "Since https://github.com/microsoft/TypeScript/pull/63937 and https://github.com/microsoft/TypeScript/pull/64023 you should be able to batch up whatever API calls you want - that work well for you?"

### [Issue microsoft/TypeScript#63875](https://github.com/microsoft/TypeScript/issues/63875) (Open, `Suggestion`, `Committed`, **andrewbranch**)

**API feature roadmap**

*API feature roadmap for TypeScript 7.1 outlining plugin replacements and top-level utilities with rough cost estimates.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5429685565) **andrewbranch** explained that the necessary APIs already exist and detailed how to load the program, use AST, symbol, and checker APIs, modify files, and update snapshots, noting that content mappers are supported but recommending using APIs to build a custom CLI
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5437239627) **remojansen** thanked andrewbranch and reported initial PoC progress for ahead-of-time reflect metadata in TypeScript 7, injecting design:symbols and design:arguments at build time using types
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5482240339) **johnnyreilly** said "As discussed in https://github.com/microsoft/TypeScript/issues/64090, it would be handy to expose the path normalisation function."
 * [later](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5510502588) **johnnyreilly** shared a benchmark test pack and snapshot results comparing performance of the old and new TypeScript APIs in ts-loader

### [Issue microsoft/TypeScript#64025](https://github.com/microsoft/TypeScript/issues/64025) (Closed, `Bug`, **jakebailey**, **Copilot**)

**\`\-\-incremental\`: diagnostics caused by a JSON module are never cleared after the JSON file is fixed \(7\.0\.2\)**

*TypeScript 7.0.2’s incremental mode with resolveJsonModule fails to clear stale JSON import diagnostics after fixing the JSON file, requiring tsbuildinfo deletion to recover.*

 * **jakebailey** assigned to **jakebailey**
 * (6 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64026](https://github.com/microsoft/TypeScript/pull/64026) (Closed, `For Uncommitted Bug`, **jakebailey**, **Copilot**)

**Clear stale incremental diagnostics after JSON module changes**

*Use JSON file content version as its shape signature to invalidate stale incremental diagnostics after JSON module changes.*

 * (1 week ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64026#issuecomment-5498423232) **jakebailey** said "I added the comment so need a re-review."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64034](https://github.com/microsoft/TypeScript/issues/64034) (Open, `Needs More Info`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**Auto\-import prioritizes files alphabetically before index\.ts inside a folder, ignoring the barrel**

*VSCode’s TypeScript auto-import in version 7.0.2 prioritizes files by alphabetical order over index.ts barrels, leading to inconsistent import paths.*

 * (6 days ago) **andrewbranch** added label `Needs More Info`, and removed label `Bug`
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64034#issuecomment-5429857364) **alexicum** thanked the maintainer for clarification and provided repro steps along with expected behavior for consistent import suggestions
 * [today](https://github.com/microsoft/TypeScript/issues/64034#issuecomment-5497652884) **alexicum** said "Related issue #46134"

### [PR microsoft/TypeScript#64054](https://github.com/microsoft/TypeScript/pull/64054) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Bump and clean up deps, raise min local node version**

*Bump and clean dependencies, raise minimum Node version to 22.18, and replace several packages with built-in features.*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64061](https://github.com/microsoft/TypeScript/pull/64061) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add pagination of batch requests**

*Implement server-side pagination of batch API responses using maxResponseBytesPerPage to prevent JavaScript string size overflows and simplify encoding.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64061#issuecomment-5485942212) **andrewbranch** said "Are any of these copilot review comments valid?"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64061#issuecomment-5489578245) **weswigham** discussed using concat vs push(...) based on element count and asked whether continuation tokens should be scoped per API client
 * [today](https://github.com/microsoft/TypeScript/pull/64061#issuecomment-5497399283) **andrewbranch** said "It's fine if you want to resolve them as wontfix, I'm just looking for a signal of whether you've evaluated them. There's another one about slice cloning in there."
 * [today](https://github.com/microsoft/TypeScript/pull/64061#issuecomment-5498052776) **weswigham** synced main and made small edits, then explained the tradeoff between cloning slices and retaining storage for batch memory usage

### [Issue microsoft/TypeScript#64062](https://github.com/microsoft/TypeScript/issues/64062) (Closed, `External`)

**LSP causes client to watch thousands of files**

*TypeScript LSP server's file watcher registers a project-wide glob, watching thousands of files and exhausting file descriptors.*

 * (yesterday) **typescript-automation[bot]** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64062#issuecomment-5487841749) **CamJN** said "What the heck, bad bot."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64062#issuecomment-5489402209) **guillaumebrunerie** agreed that MacOS supports recursive directory watching and called the multiple-watcher behavior a bug in eglot or its dependencies
 * [today](https://github.com/microsoft/TypeScript/issues/64062#issuecomment-5498829498) **RyanCavanaugh** called the bot 'bad bot' and stated that closed is the correct state for an issue not in their control
 * [today](https://github.com/microsoft/TypeScript/issues/64062#issuecomment-5499073443) **CamJN** criticized the use of unreasonable file watches and suggested limiting watchers to tsconfig directories
 * [today](https://github.com/microsoft/TypeScript/issues/64062#issuecomment-5499679896) **RyanCavanaugh** described that watching only tsconfig directories was insufficient because module resolution can traverse above include and that watching the repo root is necessary to detect creation of node_modules

### [PR microsoft/TypeScript#64063](https://github.com/microsoft/TypeScript/pull/64063) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Ditch nodeData interface in favor of generated accessors**

*Replacing the dynamic nodeData interface with generated accessors reduces binary size, symbol count, and compile time.*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5499685436) **jakebailey** requested the typescript-bot to run perf tests faster after noting the change should be performance neutral
 * [today](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5499686412) **typescript-automation[bot]** announced that performance tests started and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5500018137) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5500189461) **jakebailey** said "Hm, there's something to this, I think, I need to investigate."

### [PR microsoft/TypeScript#64084](https://github.com/microsoft/TypeScript/pull/64084) (Closed, `For Backlog Bug`)

**Add diagnostic for private identifiers in destructuring patterns**

*Add diagnostic preventing use of private identifiers in destructuring patterns.*

 * created by **youngspe**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64099](https://github.com/microsoft/TypeScript/pull/64099) (Closed, `For Backlog Bug`)

**fix\(62179\): report non\-string\-literal values in import type attributes**

*Add diagnostics to report non-string-literal values in import type attributes.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64099#issuecomment-5498386524) **jakebailey** said "Seems like this needs a merge from main."
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64108](https://github.com/microsoft/TypeScript/pull/64108) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix call hierarchy file node paths**

*Display file basenames with project-relative directories in call hierarchy nodes instead of absolute file paths.*

 * (yesterday) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64108#issuecomment-5498368978) **jakebailey** mentioned that the old VS Code extension made paths relative to the workspace root and suggested plumbing that info from the init message

### [Issue microsoft/TypeScript#64111](https://github.com/microsoft/TypeScript/issues/64111) (Closed, `Bug`, `Domain: LS: Type Display`, `Crash`, **DanielRosenwasser**, **Copilot**)

**Nil dereference when printing back function that has mapped type with no mapped property type**

*Hovering over a mapped type with no property type causes a nil pointer dereference panic in the TypeScript-Go LSP server.*

 * (yesterday) **DanielRosenwasser** added labels `Bug`, `Domain: LS: Type Display`, `Crash`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#64112](https://github.com/microsoft/TypeScript/pull/64112) (Closed, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Fix mapped type hover nil dereference**

*Hovering mapped types without property types caused panics, so the printer now emits type annotations only when property types exist.*

 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript#64113](https://github.com/microsoft/TypeScript/issues/64113) (Open, `Design Notes`)

**Design Meeting Notes, 2026\-08\-27**

*Design notes on introducing contextual, use-site negated types in TypeScript to enhance control flow narrowing and exclusions.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Design Notes`
 * [today](https://github.com/microsoft/TypeScript/issues/64113#issuecomment-5497721368) **DanielRosenwasser** explained that an optional property in `{ a?: string }` can be viewed via De Morgan's law as `{ a: unknown } & not { a: string }`, meaning `a` must be present but not a string
 * [today](https://github.com/microsoft/TypeScript/issues/64113#issuecomment-5498011315) **DanielRosenwasser** suggested that 'not { a: string, b: number }' be consistent with 'not { a: string } | not { b: number }'
 * [today](https://github.com/microsoft/TypeScript/issues/64113#issuecomment-5498077810) **DanielRosenwasser** said "We nerd-sniped @RyanCavanaugh into talking about what the heck not void is."
 * [today](https://github.com/microsoft/TypeScript/issues/64113#issuecomment-5498154258) **RyanCavanaugh** provided an AI-generated summary of the design discussion on negated types in TypeScript, covering fresh object types, the proposed `not T` constructor, and practical use cases
 * [today](https://github.com/microsoft/TypeScript/issues/64113#issuecomment-5504318190) **LukeAbby** asked about the typeRelatedToDiscriminatedType special case and its assignability issue
 * [today](https://github.com/microsoft/TypeScript/issues/64113#issuecomment-5504459251) **LukeAbby** highlighted a bonus issue regarding fresh literal widening and asked if contextual typing should apply to 'not' types in function parameters and returns

### [PR microsoft/TypeScript#64115](https://github.com/microsoft/TypeScript/pull/64115) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add optional VFS parameters to updateSnapshot**

*Add optional VFS parameters to updateSnapshot with helpers for in-memory or layered file systems supporting fallback, symlinks, and removed paths.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5496806376) **andrewbranch** expressed excitement about the feature, questioned whether the complementary file system use case exists, and worried that multiple access methods could be confusing
 * [today](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5498184533) **weswigham** explained that file system layering can be implemented via callbacks and host fallback, recommending mounting `/project/node_modules` as a host mount into the in-memory VFS

### [Issue microsoft/TypeScript#64116](https://github.com/microsoft/TypeScript/issues/64116) (Closed)

**class doesn't inherit generic type paramater when inheriting from a variable/expression**

*Extending a generic class instantiated via a function expression fails to preserve its type parameters.*

 * created by **jasonlyu123**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64116#issuecomment-5489740913) **scs0209** offered to reproduce the bug locally and bisect nightly builds to add a regression test
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64117](https://github.com/microsoft/TypeScript/pull/64117) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Make the API disposable**

*Add Symbol.asyncDispose and Symbol.dispose methods for lexical API disposal and incorporate related disposal and initialization race condition fixes*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64122](https://github.com/microsoft/TypeScript/pull/64122) (Closed, `For Uncommitted Bug`)

**chore: remove \`outFile\`,\`module:amd\` config from test cases**

*Remove outFile and AMD module test configurations and harness logic to reinstate coverage for previously skipped error code tests.*

 * created by **camc314**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64122#issuecomment-5496947601) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64122#issuecomment-5496990552) **camc314** said "Hmm actually this makes sense to just remove outFile from all fixtures so that they can start to be tested - i'll update this PR."
 * [later](https://github.com/microsoft/TypeScript/pull/64122#issuecomment-5506628420) **camc314** described fixes for the legacy outFile fixture removal and expanded unsupported compiler option skipping to cover fourslash configs

### [PR microsoft/TypeScript#64123](https://github.com/microsoft/TypeScript/pull/64123) (Closed, `For Uncommitted Bug`)

**Keep instantiation expression symbols distinct and stable**

*Restore distinct and stable symbols for instantiation expressions to fix a regression introduced by the typescript-go pull request 4687.*

 * created by **Andarist**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64124](https://github.com/microsoft/TypeScript/pull/64124) (Closed, `For Uncommitted Bug`)

**Add intrinsic type \`ModuleReference\<T\>\`**

*Add a generic intrinsic type ModuleReference<T> to the language's type system.*

 * created by **hirehamir**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64124#issuecomment-5498458439) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #54022. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [today](https://github.com/microsoft/TypeScript/pull/64124#issuecomment-5499034973) **RyanCavanaugh** said "We don't review PRs for features that aren't approved for inclusion"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64125](https://github.com/microsoft/TypeScript/pull/64125) (Open, `For Uncommitted Bug`)

**Fix add missing JSDoc to ES2015 Collection Map and WeakMap**

*Add missing @param JSDoc comments to ES2015 Map and WeakMap methods in lib.es2015.collection.d.ts to improve IntelliSense documentation consistency.*

 * created by **vedanshshetti**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64125#issuecomment-5499356950) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64125#issuecomment-5499381170) **vedanshshetti** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64125#issuecomment-5499422757) **vedanshshetti** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64126](https://github.com/microsoft/TypeScript/issues/64126) (Open, `Domain: API`, **andrewbranch**)

**\`forEachChild\` is hard to use with async API**

*forEachChild’s synchronous traversal halts on any truthy Promise return, making it incompatible with async APIs and needing an async variant*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Domain: API`, set milestone to `TypeScript 7.1.0 Beta`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64127](https://github.com/microsoft/TypeScript/issues/64127) (Closed)

**Docs: Add missing JSDoc examples**

*Add missing JSDoc usage examples for public functions to enhance the developer experience for new users.*

 * created by **a18-n03**
 * [today](https://github.com/microsoft/TypeScript/issues/64127#issuecomment-5501671334) **RyanCavanaugh** said "Unactionable without specifics. Please use an issue template."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64128](https://github.com/microsoft/TypeScript/issues/64128) (Closed)

**Feature: Add built\-in rate limiting middleware**

*Add built-in rate limiting middleware to enhance developer experience*

 * created by **a18-n03**
 * [today](https://github.com/microsoft/TypeScript/issues/64128#issuecomment-5501663031) **RyanCavanaugh** said "Add to what where? Please use an issue template."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64129](https://github.com/microsoft/TypeScript/issues/64129) (Open, `Design Notes`)

**Design Meeting Notes, 2026\-09\-01**

*The proposal introduces fresh type parameters for each conditional type distribution in TypeScript to enforce constraints, acknowledging potential breaking changes.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Design Notes`

### [PR microsoft/TypeScript#64130](https://github.com/microsoft/TypeScript/pull/64130) (Open, `For Uncommitted Bug`)

**Implement workspace/diagnostics**

*Implement workspace/diagnostics in the language server with dynamic registration behind a feature flag to reduce IDE polling in large repositories.*

 * created by **eagarwal-notion**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64130#issuecomment-5501310074) **eagarwal-notion** said "@microsoft-github-policy-service agree company="Notion""

### [PR microsoft/TypeScript#64131](https://github.com/microsoft/TypeScript/pull/64131) (Closed, `For Backlog Bug`)

**Fixed \`anyFunctionType\` leak**

*Recreates the pull request to fix the anyFunctionType leak in TypeScript.*

 * created by **Andarist**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`

### [Issue microsoft/TypeScript#64132](https://github.com/microsoft/TypeScript/issues/64132) (Open)

**getCompletionsAtPosition in API throws "completion list needs auto imports"**

*Using getCompletionsAtPosition in TypeScript 7.0.2’s unstable sync API throws a “completion list needs auto imports” error.*

 * created by **auvred**

### [PR microsoft/TypeScript#64133](https://github.com/microsoft/TypeScript/pull/64133) (Open, `For Uncommitted Bug`)

**Add auto\-import retry to getCompletionsAtPosition in API**

*Implement a GetSnapshotWithAutoImports retry in getCompletionsAtPosition to improve auto-import completions*

 * created by **auvred**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64134](https://github.com/microsoft/TypeScript/issues/64134) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**\`sourceMap\` emit is disproportionately slow for files containing one very large object literal**

*Source map generation in TypeScript 7 is significantly slower than in TypeScript 6 for files with a large object literal.*

 * created by **ken7253**

### [Issue microsoft/TypeScript#64135](https://github.com/microsoft/TypeScript/issues/64135) (Open, **jakebailey**, **Copilot**)

**unstable/ast: scanJsDocToken infinite\-loops when a scan range ends on a trailing '\-' \(fix from \#63581 not carried into the AST scanner\)**

*scanJsDocToken in unstable/ast infinite-loops on trailing hyphens due to missing parentheses in its loop condition*

 * created by **nightcabin1**

### [Issue microsoft/TypeScript#64136](https://github.com/microsoft/TypeScript/issues/64136) (Open)

**Regression to \#35004**

*Assertion functions fail with wildcard destructuring imports after upgrading to TypeScript 7, triggering TS2775 errors.*

 * created by **valler**
 * [later](https://github.com/microsoft/TypeScript/issues/64136#issuecomment-5512454226) **MartinJohns** said "Your issue is the deconstruction, not the wildcard import."

