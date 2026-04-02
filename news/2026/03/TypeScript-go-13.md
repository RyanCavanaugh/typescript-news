# Report for 2026-03-13 (Friday, March 13th, 2026)

9 different users commented on 35 different issues.

## Recommended Actions

 * Response Recommended
    * @shahmir-oscilar reported TS2615 errors under multi-threaded build after applying PR #3093 in [microsoft/TypeScript-go#3081](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4056943184)
    * @shahmir-oscilar provided typing info examples in [microsoft/TypeScript-go#3081](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4057021615)
    * @shahmir-oscilar provided updates indicating the issue is resolved and suggested closing the issue in [microsoft/TypeScript-go#3081](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4059658320)

## Activity Summary

### [Issue microsoft/TypeScript-go#2117](https://github.com/microsoft/TypeScript-go/issues/2117) (Closed)

**jsnum\.Remainder and others may not behave correctly**

*Potential incorrect behavior in jsnum.Remainder and related numeric functions*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2322](https://github.com/microsoft/TypeScript-go/pull/2322) (Open)

**Remove GetOptionsDiagnostics**

*Remove GetOptionsDiagnostics and replace it with separate GetConfigFileParsingDiagnostics and GetGlobalDiagnostics to prevent redundant diagnostic aggregation.*

 * created by **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2322#issuecomment-4049204728) **andrewbranch** asked if some diagnostics were generated during checker initialization due to symbol table merging and suggested distinguishing initialization diagnostics
 * [today](https://github.com/microsoft/TypeScript-go/pull/2322#issuecomment-4057133072) **jakebailey** said "Yes, there are diagnostics that are generated without a location, so can't be exposed any other way."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2322#issuecomment-4057861525) **andrewbranch** asked whether diagnostic location presence was orthogonal to file check-in order dependency
 * [today](https://github.com/microsoft/TypeScript-go/pull/2322#issuecomment-4057866971) **jakebailey** said "Ah. I think we still can report global diagnostics on things like "Iterable is missing", which only happens when you finally ask for it somewhere. Would need to recheck."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2322#issuecomment-4057914264) **andrewbranch** suggested having a diagnostics bucket for checker initialization, noted that the change was fine as-is, clarified the scope of global diagnostics in the LSP, and offered approval once undrafted

### [Issue microsoft/TypeScript-go#2576](https://github.com/microsoft/TypeScript-go/issues/2576) (Closed, **andrewbranch**, **Copilot**)

**Autocompletions and quick fix suggestions try to import from "@types" packages**

*tsgo quick fixes and autocompletions wrongly import from @types packages instead of real modules*

 * created by **kyle-sawatsky**
 * **andrewbranch** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2576#issuecomment-4054083735) **dan-proudfoot-bots** said "Still noticing this as of today - it makes suggestions for external packages basically useless"
 * **andrewbranch** assigned to **Copilot**

### [Issue microsoft/TypeScript-go#2859](https://github.com/microsoft/TypeScript-go/issues/2859) (Open)

**\`gql\.tada\` performing better with \`\-\-singleThreaded\` than without it**

*tsgo without --singleThreaded runs significantly slower than with it when generating gql.tada types due to union caching inefficiencies.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-3937207873) **jakebailey** said "I would suggest using --pprofDir . and upload those profiles."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-3937281866) **ahejlsberg** noted that expensive type instantiations jumped from 32M in single-threaded mode to 125M in concurrent mode, indicating each of the four type checkers repeated the same work
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-3944449861) **evsasse** attached profiling and log files for default and single-threaded runs and offered to provide additional information
 * [today](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-4058286993) **ahejlsberg** analyzed fragment file dependencies, measured command performance, and concluded that tsgo is ~6x faster than tsc and behaves as expected
 * [later](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-4060416384) **evsasse** thanked Anders and said they would refine the minimal reproduction while noting unexpected compiler performance differences

### [Issue microsoft/TypeScript-go#2993](https://github.com/microsoft/TypeScript-go/issues/2993) (Closed, `bug`, `Domain: Editor`, **andrewbranch**, **iisaduan**, **Copilot**)

**Auto import does not get its own line**

*Auto-importing readFileSync inserts its import on the same line as the previous import instead of a new line.*

 * (1 week ago) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, and assigned to **iisaduan**
 * (today) **andrewbranch** assigned to **Copilot**, **andrewbranch**

### [PR microsoft/TypeScript-go#2999](https://github.com/microsoft/TypeScript-go/pull/2999) (Closed, **jakebailey**, **Copilot**)

**\[WIP\] Fix issue preventing renaming of keywords in TS\-go**

*Add early prepareRename validation in TS-go to prevent renaming of keywords and punctuation tokens*

 * (1 week ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2999#issuecomment-4009883793) **jakebailey** said "@copilot+claude-opus-4.6 something bad happened. Look at all of my comments and try again"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2999#issuecomment-4059307149) **jakebailey** said "@copilot+claude-opus-4.6 something bad happened. Look at all of my comments and try again"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3009](https://github.com/microsoft/TypeScript-go/pull/3009) (Closed)

**Remove some unused / noop emit flags**

*Remove unused or no-op compiler emit flags rendered redundant by dropping ES5 support and restructuring imports*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3021](https://github.com/microsoft/TypeScript-go/pull/3021) (Closed)

**Fixed a format selection crash in reparsed JSDoc nodes**

*Fixed a crash triggered by format selection in reparsed JSDoc nodes.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3024](https://github.com/microsoft/TypeScript-go/pull/3024) (Closed)

**Fixes a crash when requesting implementations for a module referenced by a tripleslash directive**

*Fix crash when requesting implementations for modules referenced by triple-slash directives.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3033](https://github.com/microsoft/TypeScript-go/pull/3033) (Closed)

**Fixed a formatting crash caused by misinterpretation of tokens in reparsed node lists**

*A formatting crash caused by misinterpreting tokens in reparsed node lists has been fixed.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3060](https://github.com/microsoft/TypeScript-go/pull/3060) (Closed)

**Fix jsnum's Remainder and Exponentiate funcs**

*Update jsnum’s remainder function to handle rounding correctly and refine exponentiation accuracy with Node.js tests.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3064](https://github.com/microsoft/TypeScript-go/pull/3064) (Closed)

**Don't use our parser in bundled/generate\.go**

*Replace the custom JSONC parser in bundled/generate.go with simple comment stripping and the standard json package.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3067](https://github.com/microsoft/TypeScript-go/pull/3067) (Closed)

**Avoid constructing unused transformers**

*Skip constructing transformers for high targets and eliminate the now-unnecessary internal checks.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3074](https://github.com/microsoft/TypeScript-go/pull/3074) (Closed)

**Preserve detached comment separator after unterminated block comments**

*Preserve detached comment separators after unterminated block comments to eliminate unnecessary diffs.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3076](https://github.com/microsoft/TypeScript-go/pull/3076) (Closed)

**Align enum emit with Strada, fix inlining of imported enum members**

*Resolve imported enum member values during transformation so generated enum emit matches Strada's output.*

 * (yesterday) **jakebailey** reopened the issue
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3076#issuecomment-4048031606) **jakebailey** expressed a desire to keep the issue open and acknowledged misunderstanding about the crash
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3076#issuecomment-4048057332) **AlCalzone** said "Right, I didn't explicitly say so - my bad. The import is elided, but still used in the enum definition."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3076#issuecomment-4056722113) **jakebailey** said "I compared the two, and my change had a few more changes that would have been required, so I've just opened #3092."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3081](https://github.com/microsoft/TypeScript-go/issues/3081) (Open)

**Stack overflow in multi\-threaded mode during type instantiation**

*tsgo 7.0.0-dev encounters a goroutine stack overflow in multi-threaded type instantiation on a large React/TypeScript codebase, while single-threaded mode works.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4050894285) **ahejlsberg** said "Hmm, the checker.(*NodeBuilderImpl) on the stack means we're serializing something, probably because we're building a diagnostic message. Can you post the bottom 100 and top 100 frames of the stack?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4052970423) **shahmir-oscilar** shared the entire stack trace in an attached file
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4055740225) **ahejlsberg** identified a circularity error in getTypeOfMappedSymbol and asked for a repro
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4056827274) **shahmir-oscilar** said "Sorry, wasn't able to find root cause / come up with a sharable repro, but totally willing to try out any fixes y'all do to verify that it's fixed."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4056838816) **jakebailey** said "If you're willing to build from source, can you try #3093?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4056943184) **shahmir-oscilar** tried building from source with PR #3093 and reported that --singleThreaded produced no errors but multi-threaded build now showed TS2615 circular reference errors
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4057021615) **shahmir-oscilar** provided typing information including OmitStrict, IntegrationFormData, SchemaFieldAO, and SchemaAO definitions
 * (today) **ahejlsberg** closed the issue
 * (today) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4057291353) **ahejlsberg** explained that concurrent checking can cause differences and asked for a repro
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4059658320) **shahmir-oscilar** found that the error was due to an older react-hook-form version, recommended upgrading to the latest version, and suggested the issue could be closed
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4059818295) **jakebailey** suggested running TypeScript 6.0 with --stableTypeOrdering to reveal the circular error

### [PR microsoft/TypeScript-go#3083](https://github.com/microsoft/TypeScript-go/pull/3083) (Closed)

**Remove JSDocParsingMode from API scanner**

*Remove the obsolete JSDocParsingMode option from the API scanner since it predates the #2801 port.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3087](https://github.com/microsoft/TypeScript-go/issues/3087) (Closed, `Crash`)

**panic handling request textDocument/documentHighlight: runtime error: invalid memory address or nil pointer dereference**

*The TypeScript-Go LSP server panics with a nil pointer dereference during textDocument/documentHighlight requests.*

 * created by **Zzzen**
 * **Zzzen** added label `Crash`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3088](https://github.com/microsoft/TypeScript-go/pull/3088) (Closed)

**fix\(checker\): add nil guard for thisType in getThisType**

*Add a nil guard in getThisType to prevent errors when thisType is nil.*

 * created by **Zzzen**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3088#issuecomment-4056302012) **Zzzen** noted that the assertion was too optimistic and asked why Strada didn't show a crash popup
 * [today](https://github.com/microsoft/TypeScript-go/pull/3088#issuecomment-4056403882) **jakebailey** noted that Strada didn't report errors and that they now let the VS Code LSP client show errors loudly
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3089](https://github.com/microsoft/TypeScript-go/pull/3089) (Closed, **andrewbranch**, **Copilot**)

**Fix auto\-import suggesting "@types" package specifiers instead of real package names**

*Update auto-import logic to favor actual package names over @types specifiers when both are installed*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3089#issuecomment-4056790526) **andrewbranch** questioned whether the original bug was reproduced or a different bug was fixed, noting that “no suggestions” and “incorrect @types/react specifiers” are distinct behaviors
 * [today](https://github.com/microsoft/TypeScript-go/pull/3089#issuecomment-4057007192) **Copilot** clarified the distinction between no suggestions and incorrect `@types` specifiers, reproduced the incorrect specifier case in updated tests, and explained the normalization fix

### [PR microsoft/TypeScript-go#3090](https://github.com/microsoft/TypeScript-go/pull/3090) (Closed, **andrewbranch**, **Copilot**)

**Fix auto import not getting its own line**

*Ensure auto-imports are inserted with a trailing newline and preserve header comments when added before existing imports.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**

### [PR microsoft/TypeScript-go#3091](https://github.com/microsoft/TypeScript-go/pull/3091) (Closed)

**Drop scriptKind out of scanner entirely**

*Remove the obsolete scriptKind functionality from the scanner now that JSDocParsingMode support has been eliminated.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3092](https://github.com/microsoft/TypeScript-go/pull/3092) (Closed)

**Rework enums back into a more Strada\-like form**

*Restore enum emission to the previous Strada-like approach by removing custom checker-less code and reinstating the emit resolver.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3093](https://github.com/microsoft/TypeScript-go/pull/3093) (Closed)

**Record resolved error type before reporting circularity error**

*Record the resolved error type for mapped type element symbols before reporting circularity errors to avoid infinite recursion in TypeToString.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3094](https://github.com/microsoft/TypeScript-go/issues/3094) (Open, `bug`, **weswigham**)

**Declaration emit proceeds in the presence of TS7056**

*TypeScript emits declarations despite TS7056 errors caused by deeply nested conditional and tag-branded utility types.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript-go#3095](https://github.com/microsoft/TypeScript-go/pull/3095) (Closed)

**Watch directories and react to symlink directory creation**

*Enhance directory watcher to detect symlink directory creation and handle directory deletion events*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#3096](https://github.com/microsoft/TypeScript-go/pull/3096) (Closed)

**Hide skipped tests in CI too**

*Suppress skipped tests in CI output to streamline logs and quickly locate test failures.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3097](https://github.com/microsoft/TypeScript-go/issues/3097) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*The main branch TypeScript error pipeline analyzed 300 repositories, finding 32 changes, 191 unchanged, 6 clone failures, 69 timeouts, and 2 unknown failures.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022203) **typescript-bot** reported a panic in the textDocument/formatting handler with a debug failure
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022226) **typescript-bot** reported a panic during rangeFormatting and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022246) **typescript-bot** reported a panic in textDocument/implementation during cross-project handling
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022278) **typescript-bot** reported a panic due to invalid memory address or nil pointer dereference in textDocument/implementation
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022304) **typescript-bot** reported a panic in textDocument/implementation due to an invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022334) **typescript-bot** reported a panic in textDocument/implementation cross-project handling due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022367) **typescript-bot** reported a panic with stack trace during textDocument/implementation request
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022390) **typescript-bot** reported a panic during textDocument/implementation handling due to invalid memory address or nil pointer dereference with stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022436) **typescript-bot** reported a panic in textDocument/formatting due to debug failure "False expression: Token end is child end" and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022467) **typescript-bot** reported a panic handling textDocument/signatureHelp due to debug failure "Expected 3 < 1"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022491) **typescript-bot** reported a server connection closed prematurely error with details of affected repos and recent requests
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022523) **typescript-bot** reported server connection closed prematurely with raw error details, affected repository information, recent requests, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022557) **typescript-bot** reported a server connection closed prematurely error including affected repos and request logs
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022670) **typescript-bot** reported that the server connection closed prematurely and provided repro steps and error details for directus/directus
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022754) **typescript-bot** reported a server connection closed prematurely error
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022812) **typescript-bot** reported a server connection closed prematurely with undefined error for babel/babel and provided repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3097#issuecomment-4059022941) **typescript-bot** reported a server connection closed prematurely error and provided error logs, last requests, and repro steps for n8n-io/n8n

