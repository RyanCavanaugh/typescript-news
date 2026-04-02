# Report for 2026-03-25 (Wednesday, March 25th, 2026)

14 different users commented on 56 different issues.

## Recommended Actions

 * Response Recommended
    * @rubenferreira97 provided confirmation that the issue is resolved in the tested version in [microsoft/TypeScript-go#3040](https://github.com/microsoft/TypeScript-go/issues/3040#issuecomment-4130633015)
    * @gary-donut provided an example showing vague error messages via this['faa'] in [microsoft/TypeScript-go#3220](https://github.com/microsoft/TypeScript-go/pull/3220#issuecomment-4131552782)

## Activity Summary

### [Issue microsoft/TypeScript-go#2081](https://github.com/microsoft/TypeScript-go/issues/2081) (Closed, `bug`, **RyanCavanaugh**, **Copilot**)

**Missing error when reference directive file path doesn't exist**

*tsgo fails to report an error for a nonexistent reference directive file path, unlike tsc which raises TS6053.*

 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2081#issuecomment-3533996173) **jakebailey** said "Bug, there should be an error; some code is just not ported."
 * (1 week ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2108](https://github.com/microsoft/TypeScript-go/issues/2108) (Closed)

**Import containing a dot give an error**

*Importing from 'socket.io/dist/namespace' works in TypeScript 5.8 but causes TS2307 'cannot find module' errors in tsgo.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2108#issuecomment-3599008290) **RyanCavanaugh** noted that a deprecated compiler option was being used and showed the resulting error message
 * **RyanCavanaugh** removed label `Needs More Info`
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2108#issuecomment-3599030621) **jakebailey** said "Yeah, unfortunately we are not yet hard erroring in tsgo on node10."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2244](https://github.com/microsoft/TypeScript-go/issues/2244) (Open, `Domain: Editor`, **gabritto**)

**Port \`update imports on file rename/move\` support**

*Request to port support for automatically updating imports when files are renamed or relocated*

 * **jakebailey** added label `Domain: Editor`
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2244#issuecomment-3633217310) **GitMurf** asked if there was a discussion on how tsgo will implement file rename LSP methods and offered to help test from a Neovim perspective
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2244#issuecomment-3633225247) **jakebailey** said "I assume we'd do it the same way as VS Code, just over LSP (which LSP is mostly a thin wrapper over)."
 * **RyanCavanaugh** assigned to **gabritto**

### [PR microsoft/TypeScript-go#2407](https://github.com/microsoft/TypeScript-go/pull/2407) (Closed)

**Rewrite matchFiles to not use regexp2, remove other regexp uses**

*Rewrites matchFiles to remove regexp2 and minimize regex usage, achieving significant performance gains.*

 * created by **jakebailey**
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2407#issuecomment-3741353531) **jakebailey** said "This needs more work, unfortunately."
 * [later](https://github.com/microsoft/TypeScript-go/pull/2407#issuecomment-4135895201) **jakebailey** tested a Copilot-based reimplementation, noted negligible practical differences from the old regex version, and offered to remove the old implementation due to improved design and performance

### [PR microsoft/TypeScript-go#2817](https://github.com/microsoft/TypeScript-go/pull/2817) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript PR \#62338: Deprecate \-\-moduleResolution node10**

*Port TypeScript PR #62338 to Go to deprecate --moduleResolution node10, enhance require resolution utilities, and update tests.*

 * created by **Copilot**
 * (5 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2818](https://github.com/microsoft/TypeScript-go/pull/2818) (Closed, **jakebailey**, **Copilot**)

**Port TS PR \#62669: Deprecate \-\-module amd, umd, system, none; \-\-moduleResolution classic**

*Port deprecation of amd, umd, system, and none module options and classic module resolution removal diagnostic to the Go port.*

 * created by **Copilot**
 * (5 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2988](https://github.com/microsoft/TypeScript-go/issues/2988) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[TypeScript\] main vs **

*TypeScript main pipeline encountered server errors in 62 of 300 repos and detected 163 interesting changes among the 238 analyzed.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4006497130) **gabritto** summarized issues found by PR and request with panic messages and links
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4007294528) **gabritto** listed occurrences of 'Token end is child end' errors by node kind with counts and links
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4008560677) **Andarist** noted that most issues referred to range formatting and likely would be fixed by PR 3000, and said they would still investigate the JsxAttribute issue
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3012](https://github.com/microsoft/TypeScript-go/issues/3012) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The main branch Azure pipeline reported clone failures, timeouts, and server errors during analysis of 300 TypeScript repositories, yielding 53 significant changes.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173799) **typescript-bot** reported a panic handling textDocument/formatting request due to a debug failure: Token end is child end
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173817) **typescript-bot** reported a panic in textDocument/formatting due to a false expression 'Token end is child end' with a stack trace
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4068851896) **gabritto** provided a table summarizing error messages, stack trace links, comment counts, affected repositories, and related pull requests
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3015](https://github.com/microsoft/TypeScript-go/issues/3015) (Open, `Crash`, **johnfav03**)

**panic on \`\-\-watch\` and \`\-\-explainFiles\`**

*Using tsgo with --watch and --explainFiles flags triggers a nil pointer dereference panic.*

 * created by **DanielRosenwasser**
 * (2 weeks ago) **DanielRosenwasser** added labels `Crash`, `Crash`
 * **RyanCavanaugh** assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#3025](https://github.com/microsoft/TypeScript-go/issues/3025) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*An Azure Pipeline run on the TypeScript main branch encountered server errors and mixed results across 300 popular GitHub repositories.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210395) **typescript-bot** reported a server connection closing prematurely with undefined and provided affected repos and reproduction steps
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210407) **typescript-bot** reported a panic handling textDocument/rangeFormatting due to a debug failure
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4068930190) **gabritto** listed five error messages with stack trace links, comment counts, and affected repositories
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3040](https://github.com/microsoft/TypeScript-go/issues/3040) (Closed, `Domain: Declaration Emit`, **weswigham**)

**\`TS7056\` for exported generic arrow function with return type \(arrow\-only\)**

*Exporting a generic arrow function with a complex return type triggers TS7056 serialization errors under tsgo but not in TypeScript 6.0 or for function declarations.*

 * created by **rubenferreira97**
 * (2 weeks ago) **ahejlsberg** added label `Domain: Declaration Emit`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3040#issuecomment-4130633015) **rubenferreira97** said "I'm not sure exactly which version fixed this, but I can confirm it's resolved when testing on 7.0.0-dev.20260325.1."
 * (today) **rubenferreira97** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3040#issuecomment-4130635972) **jakebailey** said "Would have been #2459, I'm sure."

### [Issue microsoft/TypeScript-go#3097](https://github.com/microsoft/TypeScript-go/issues/3097) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The main branch TypeScript error pipeline analyzed 300 repositories, finding 32 changes, 191 unchanged, 6 clone failures, 69 timeouts, and 2 unknown failures.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022754) **typescript-bot** reported a server connection closed prematurely error
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022812) **typescript-bot** reported a server connection closed prematurely with undefined error for babel/babel and provided repro steps
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022941) **typescript-bot** reported a server connection closed prematurely error and provided error logs, last requests, and repro steps for n8n-io/n8n
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3099](https://github.com/microsoft/TypeScript-go/issues/3099) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch error-delta pipeline processed 300 repos, encountering server errors, analyzing 220 and reporting interesting changes, failures, timeouts.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180394) **typescript-bot** reported that the server connection closed prematurely and provided affected repos, last requests, and repro steps
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180414) **typescript-bot** reported server connection closed prematurely on colinhacks/zod with error logs
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180435) **typescript-bot** reported server connection closed prematurely and provided repro steps
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3126](https://github.com/microsoft/TypeScript-go/pull/3126) (Closed, **RyanCavanaugh**, **Copilot**)

**Emit TS6053 error for missing reference directive files**

*Emit TS6053 error for missing triple-slash reference files in the Go compiler, align noResolve behavior, and update baselines.*

 * **Copilot** assigned to **RyanCavanaugh**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3126#issuecomment-4099495030) **Copilot** skipped referenced files and type reference directive processing when noResolve was set
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3126#issuecomment-4099873499) **Copilot** addressed the code review comment in commit f224b98e, updating the File_0_not_found diagnostic to use the original reference directive string instead of the resolved absolute path, matching TypeScript's output
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3176](https://github.com/microsoft/TypeScript-go/pull/3176) (Closed)

**Fix ref count cache inconsistencies**

*Revert cache ref-count simplification so parse cache entries start with refCount 1 and prevent premature deletion.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4121907291) **andrewbranch** said "I can't get the flaky test to fail on my machine 😕 "
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4121947181) **jakebailey** said "I've been trying to get get a failing run of TestDuplicatePackageServices_fileChanges for what feels like months now, it's almost certainly nothing related to this PR."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4121984148) **andrewbranch** said "Oh, geez, I didn't know that and this PR did touch duplicate file stuff, so I thought it was my fault."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4130474601) **andrewbranch** said "@gabritto and/or @iisaduan was looking into running the fuzzer against this to hopefully get some extra validation before merging."

### [Issue microsoft/TypeScript-go#3187](https://github.com/microsoft/TypeScript-go/issues/3187) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch pipeline analyzed 262 of 300 repositories, reporting 23 changes, timeouts, clone failures, and unknown errors.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731479) **typescript-bot** reported a premature server connection closure error and provided affected repo, raw error logs, replay commands, last requests, and repro steps
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731569) **typescript-bot** reported a panic during cross-project handling of textDocument/implementation due to invalid memory address or nil pointer dereference
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731639) **typescript-bot** reported a panic handling request textDocument/implementation caused by invalid memory address or nil pointer dereference
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3195](https://github.com/microsoft/TypeScript-go/pull/3195) (Open)

**API encode/decode fixes**

*Fixed API encoder/decoder by adding missing node properties, assigning a HeritageClause token type, and extending isTypeNode to recognize type keywords.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4104786681) **virtulis** agreed with microsoft-github-policy-service
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4113515688) **virtulis** agreed that encoder changes were unnecessary and only the properties getter was needed, suggested adding a flag for getNamedChild to handle non-optional properties, proposed tests for round-trip consistency, and declined to commit due to CLA restrictions
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4113555719) **virtulis** suggested generating a full list of properties with the generateFactory script and using defineProperty to dynamically define getters on RemoteNode to avoid manual listings and solve the optional vs empty NodeList issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4129065241) **virtulis** said "Added the roundtrip test, made it go through everything and print each error since there's multiple different failures present."

### [Issue microsoft/TypeScript-go#3202](https://github.com/microsoft/TypeScript-go/issues/3202) (Closed, `Crash`, **andrewbranch**, **jakebailey**, **Copilot**)

**Panic in \`20260321\.1\` release**

*Updating to the 20260321.1 release triggers a nil pointer panic in tsgo type checking, unlike 20260320.1.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3202#issuecomment-4118780990) **walkerdb** provided a minimal repro including code files and tsconfig
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3202#issuecomment-4119188813) **walkerdb** said "hmm actually the above is a panic, but I think it's a different panic than the one originally reported. I'll keep iterating.."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3202#issuecomment-4119423916) **walkerdb** provided a repro for the original panic with code samples and noted it was fixed in PR #3203
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3205](https://github.com/microsoft/TypeScript-go/pull/3205) (Closed)

**Don’t try to create invalid type/symbol merges**

*Prevent invalid merges between type and value symbols by updating the merging logic and diff handling.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3205#issuecomment-4127758976) **jakebailey** tried applying the proposed merge code approach but found it unhelpful and shared a diff illustrating the changes
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3206](https://github.com/microsoft/TypeScript-go/pull/3206) (Closed)

**Report "File not found" for missing tripleslash path references**

*Report 'File not found' errors when triple-slash directive path references are missing.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3206#issuecomment-4119973682) **jakebailey** said "On face, does seem like it covers more stuff, yeah. You can probably say "Fixes #2081"."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3206#issuecomment-4120023176) **Andarist** asked whether the PR duplicated microsoft/typescript-go#3126 and mentioned having started work over a week ago without reviewing existing PRs/issues
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3206#issuecomment-4122135853) **jakebailey** provided an unsolicited patch adding isSupportedExtension method and refactoring extension checks in fileloader.go
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3207](https://github.com/microsoft/TypeScript-go/issues/3207) (Closed, **weswigham**)

**\`isolatedDeclarations\` false positive TS9013 on arrow functions with default parameters and \`as const\` objects**

*Enabling isolatedDeclarations in tsgo triggers false-positive TS9013 errors on arrow functions with default parameters and as const objects.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3207#issuecomment-4120895556) **hkleungai** mentioned that tsgo behaved unexpectedly with `as const` and nested object/array literals under the isolatedDeclarations flag and referenced a related issue
 * **jakebailey** assigned to **weswigham**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3207#issuecomment-4122814850) **jakebailey** said "The first is is an easy fix. I have not looked at the latter."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3213](https://github.com/microsoft/TypeScript-go/pull/3213) (Closed)

**Remove nondeterminism in container generation**

*Eliminate nondeterministic global symbol traversal by implementing stable sorting to ensure consistent container generation and measurable performance.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3213#issuecomment-4121061795) **ahejlsberg** explained that using insertion-order sorted symbol tables was too costly due to performance and memory overhead
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3213#issuecomment-4121088253) **ahejlsberg** asked how often the bottom part of getWithAlternativeContainers executes and expressed concern about its performance cost
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3213#issuecomment-4121177006) **weswigham** explained that declaration emit historically made cached type comparisons free, noted a potential alternative for current emit model, and reported that removing the style container lookup would affect 61 test baselines
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3217](https://github.com/microsoft/TypeScript-go/pull/3217) (Open)

**Watch cli efficiency update**

*Watch CLI efficiency improvements implement debouncing, configuration caching, and dependency parsing to avoid unnecessary recompilations.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4127784005) **andrewbranch** highlighted missing include wildcard handling and proposed decoupling watcher logic from build logic for LSP integration
 * [today](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4129133587) **johnfav03** described implementing the change by separating file tracking into a FileWatcher struct with a callback linked to doCycle while keeping caches, program construction, and emitting logic in the Watcher wrapper

### [PR microsoft/TypeScript-go#3218](https://github.com/microsoft/TypeScript-go/pull/3218) (Closed)

**Port PR 61392 \- Fix serialization of accessor types in declaration files**

*Port PR 61392 to address incorrect serialization of accessor types in TypeScript declaration files.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3219](https://github.com/microsoft/TypeScript-go/pull/3219) (Closed)

**Use isOptionalParameter from checker to check param optional\-ness**

*Use isOptionalParameter from the checker to accurately detect parameter optionality instead of relying solely on isOptionalDeclaration’s question-node check.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3219#issuecomment-4129651300) **jakebailey** said "Yeah, I started with a syntactic one only, but that didn't work in many cases..."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3220](https://github.com/microsoft/TypeScript-go/pull/3220) (Open)

**Preserve error elaboration for indexed access type assignments**

*Improve TypeScript diagnostic messages by preserving specific error details for assignments to indexed access types.*

 * created by **WhiteMinds**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3220#issuecomment-4127991153) **jakebailey** said "Maybe I don't have context here, but, I don't find the new messages more helpful than the existing one..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3220#issuecomment-4131552782) **gary-donut** provided an example demonstrating that assignment via this['faa'] yields less precise error messages than direct assignment

### [PR microsoft/TypeScript-go#3221](https://github.com/microsoft/TypeScript-go/pull/3221) (Closed)

**Fix ProbablyUsesSemicolons threshold comparison \(integer division\)**

*Replace the flawed integer division threshold in ProbablyUsesSemicolons with a multiplication-based inequality to fix zero-valued comparisons.*

 * created by **cuiweixie**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3221#issuecomment-4126082963) **cuiweixie** said "@microsoft-github-policy-service agree"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3222](https://github.com/microsoft/TypeScript-go/pull/3222) (Closed)

**Fix getPossibleTypeArgumentsInfo balance for \>\> and \>\>\>**

*Fix getPossibleTypeArgumentsInfo to increment balance by 2 and 3 for >> and >>> instead of resetting it.*

 * created by **cuiweixie**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3223](https://github.com/microsoft/TypeScript-go/pull/3223) (Closed)

**Fix signature help label for multiple type parameters**

*Format multiple generic type parameters in signature help with commas and spaces between names.*

 * created by **cuiweixie**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3225](https://github.com/microsoft/TypeScript-go/pull/3225) (Closed)

**adding prefix/postfix unary operator fix**

*Serialize prefix and postfix unary operators in the TypeScript-Go binary AST protocol by encoding their SyntaxKind bits.*

 * created by **navya9singh**
 * (today) **navya9singh** closed the issue

### [PR microsoft/TypeScript-go#3226](https://github.com/microsoft/TypeScript-go/pull/3226) (Closed)

**Add lint rule forbidding \.Parent accesses in transformers**

*Implement a lint rule banning .Parent accesses in transformers and address or exempt current references*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3227](https://github.com/microsoft/TypeScript-go/issues/3227) (Open, `possible improvement`, **DanielRosenwasser**, **Copilot**)

**Track file type or extension for failing requests**

*Track file extensions for failing requests to aid in reproducing crashes and identifying language-specific issues.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3228](https://github.com/microsoft/TypeScript-go/pull/3228) (Open, **DanielRosenwasser**, **Copilot**)

**Track file extension in LSP request failure telemetry**

*Include an optional fileExtension field in LSP request failure telemetry to capture the affected file type.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3229](https://github.com/microsoft/TypeScript-go/pull/3229) (Closed)

**Check pointer equality of getRegularTypeOfLiteralType in pseudoTypeEquivalentToType**

*Add pointer equality check in pseudoTypeEquivalentToType for getRegularTypeOfLiteralType to fix literal type comparison.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3230](https://github.com/microsoft/TypeScript-go/pull/3230) (Closed)

**Fix class field super access checks**

*Refine class field super access checks to align test baselines and disallow uninitialized expando declarations.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3231](https://github.com/microsoft/TypeScript-go/pull/3231) (Closed)

**Organize CI checks into groups by name**

*Group GitHub Actions CI checks by name and rename them for clearer UI organization.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3231#issuecomment-4129084217) **jakebailey** noted that the proposed solution did not work and provided a screenshot
 * [today](https://github.com/microsoft/TypeScript-go/pull/3231#issuecomment-4129088937) **jakebailey** said "I guess I was bamboozled by some sort of reusable workflow feature. Sigh."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3232](https://github.com/microsoft/TypeScript-go/pull/3232) (Open)

**Speed up lookupSymbolChain**

*Optimize lookupSymbolChain by caching alias-only symbol lists per table and refining iteration logic, reducing CPU time by 61%.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3232#issuecomment-4129832914) **jakebailey** said "Unfortunately it seems like if I remove these fast paths (which presumably are iffy), and then restrict to just globals, it goes back to having the same perf..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3232#issuecomment-4129842233) **jakebailey** drafted a comment admitting overexcitement and lamenting the lack of tests to prove the change wrong

### [PR microsoft/TypeScript-go#3233](https://github.com/microsoft/TypeScript-go/pull/3233) (Closed)

**adding to isTypeNode\(\)**

*Extend isTypeNode to include keyword, expression, and JSDoc type nodes, preventing visitEachChild assertion failures.*

 * created by **navya9singh**

### [PR microsoft/TypeScript-go#3234](https://github.com/microsoft/TypeScript-go/pull/3234) (Closed, **andrewbranch**, **Copilot**)

**Add diagnostic API methods**

*Add API methods for syntactic, semantic, suggestion, config file parsing, and declaration diagnostics with async server calls and range-based tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**

### [PR microsoft/TypeScript-go#3235](https://github.com/microsoft/TypeScript-go/pull/3235) (Closed)

**Add project info, progress indicators**

*Port project info features from the old TypeScript extension and add progress indicators for project loading and ATA operations.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3236](https://github.com/microsoft/TypeScript-go/pull/3236) (Closed)

**Use an empty NoParams type instead of any for no param messages**

*Use an empty NoParams struct instead of any for no-parameter messages to remove any(nil) from generated LSP types.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3237](https://github.com/microsoft/TypeScript-go/pull/3237) (Closed)

**Lint when t\.Cleanup closes over t**

*Introduce a lint rule to detect closures capturing t in t.Cleanup and automatically fix the identified case.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3238](https://github.com/microsoft/TypeScript-go/issues/3238) (Closed)

**Consider using \`process\.execve\` in tsgo\.js ?**

*Proposes using experimental process.execve instead of execFileSync in tsgo.js to avoid spawning extra Node processes.*

 * created by **kanashimia**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3238#issuecomment-4135945340) **jakebailey** said "Yes, we'd totally accept a PR for this."

### [PR microsoft/TypeScript-go#3239](https://github.com/microsoft/TypeScript-go/pull/3239) (Closed)

**Accept baseline differences**

*Integrate the first batch of approved baseline differences into the project’s testing baseline.*

 * created by **ahejlsberg**

### [Issue microsoft/TypeScript-go#3240](https://github.com/microsoft/TypeScript-go/issues/3240) (Closed)

**Parser: postfix \`\!\` \(NonNullExpression\) parsed as prefix \`\!\` \(PrefixUnaryExpression\)**

*tsgo parser misparses the postfix non-null assertion operator '!' as a prefix logical-not, producing two statements instead of one.*

 * created by **RealColdFry**

### [Issue microsoft/TypeScript-go#787](https://github.com/microsoft/TypeScript-go/issues/787) (Closed)

**\`UnionToTuple\` type returns "inverted" tuple in TSGO compared to TypeScript 5\.8\.3 and gives type error**

*TSGO's UnionToTuple type generates tuples in reverse order compared to TypeScript 5.8.3, causing type errors*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-4119936148) **jakebailey** said "I don't understand the question; I was just pointing out that you could test this more easily with that flag (the code for this had been backported for a while, just not shipped)."
 * [today](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-4125698998) **alexwork1611** said "Another way to ask would be, would you say this specific issue helped inform the design or the priority of the new --stableTypeOrdering flag in TS 6.0?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-4127370402) **RyanCavanaugh** explained that the design and implementation of STO predates the issue and TS7 and that this issue was one of many confirming the need for STO since TS6
 * [today](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-4132153061) **alexwork1611** said "I really appreciate that clarification, @RyanCavanaugh. I'm glad I could contribute with something, though!"

