# Report for 2026-03-11 (Wednesday, March 11th, 2026)

12 different users commented on 37 different issues.

## Recommended Actions

 * Response Recommended
    * @graphemecluster asked if the issue was closed in favor of #3061 in [microsoft/TypeScript-go#2026](https://github.com/microsoft/TypeScript-go/pull/2026#issuecomment-4046590806)
    * @dbrxnds reported that the issue persisted after initial improvement in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4047475814)
    * @camchenry asked whether cache invalidation is needed for long-running processes in [microsoft/TypeScript-go#3070](https://github.com/microsoft/TypeScript-go/pull/3070#issuecomment-4043364505)

## Activity Summary

### [PR microsoft/TypeScript-go#2026](https://github.com/microsoft/TypeScript-go/pull/2026) (Closed)

**Implement regexp literal syntax checking**

*Move regexp literal syntax checks into the grammar checking phase to unify ASTs and improve Unicode offset handling*

 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2026#issuecomment-3554866023) **jakebailey** thanked the reviewer, noted his approach duplicated scanner functionality requiring code relocation, and said he needed time to rethink it
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2026#issuecomment-3560078395) **graphemecluster** explained that CharacterEscape and EscapeSequence are separate productions, noted that only HexEscapeSequence and LegacyOctalEscapeSequence overlap, questioned the value of abstracting the method, and acknowledged their large share in scanEscapeSequence
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2026#issuecomment-3567273094) **graphemecluster** explained that RegExpIdentifierName and IdentifierName are distinct productions and suggested moving surrogate-pair utils to core or a standalone text manipulation folder
 * (today) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/2026#issuecomment-4046590806) **graphemecluster** said "Just to be sure, did you close this in favor of #3061?"
 * [later](https://github.com/microsoft/TypeScript-go/pull/2026#issuecomment-4047211371) **jakebailey** said "Yes, correct."

### [Issue microsoft/TypeScript-go#2354](https://github.com/microsoft/TypeScript-go/issues/2354) (Closed, `Domain: Emit`)

**Implement esnext\-\>es2022 transformer \(ES decorators, \`using\` declarations\)**

*Implement ES decorator transformations to enable --target es2022 support in the esnext->es2022 transformer.*

 * created by **DanielRosenwasser**
 * **jakebailey** added label `Domain: Emit`
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2354#issuecomment-3736508508) **rektide** requested implementation of the decorator transform in tsgo, loosening of decorator type‐signature restrictions, and more granular control such as enabling decorators with newer ES targets
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4006434882) **andrewbranch** described different causes for high memory usage, mentioned a pending PR with optimizations, and asked @shinichy about signing an NDA and sharing their repo for offline debugging
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4009619194) **shinichy** said "@andrewbranch I'm not sure if an NDA is possible at my company, but I'll look into it. I'll send an email anyway. Thanks for your help!"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4018362467) **shinichy** described that a generated re-export file with many subpath exports caused checker.getExportsOfModuleWorker to recurse deeply, and asked how to skip visiting the generated export and why the Strada language service didn’t exhibit the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4047475814) **dbrxnds** said "Update: Unfortunately I just seemed to have gotten last time when I said things improved. These past 2 days have been the same as before."

### [PR microsoft/TypeScript-go#3013](https://github.com/microsoft/TypeScript-go/pull/3013) (Closed)

**Report errors on unsupported CJS constructs in declaration emit**

*Generate errors during declaration file emission for multiple or nested CommonJS exports and defineProperty calls.*

 * created by **ahejlsberg**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3013#issuecomment-4016612558) **ahejlsberg** explained that the only change in the symbol tracker was the addition of two error reporting methods, serving as the conduit for error reporting in the declaration transformer
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3022](https://github.com/microsoft/TypeScript-go/pull/3022) (Closed)

**Provide type\-based quick info on symbol\-less nodes**

*Enable quick info tooltips showing inferred type information for code nodes without associated symbols.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3022#issuecomment-4025483658) **ahejlsberg** explained that the current fix approach was incorrect and that existing infrastructure for synthetic symbols wasn’t working properly, and said he would submit a PR to fix it
 * [today](https://github.com/microsoft/TypeScript-go/pull/3022#issuecomment-4039906916) **jakebailey** said "is this still needed after #3018?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3022#issuecomment-4040054101) **Andarist** described the branch as a pure port from Strada, removed failingTests, and noted it was based on issue #3018 so the diff was current
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3022#issuecomment-4040722300) **ahejlsberg** questioned changing quick info on an error location from displaying nothing to 'any' and asked how that was better
 * [today](https://github.com/microsoft/TypeScript-go/pull/3022#issuecomment-4040744728) **Andarist** said "As a user, that displayed any is what I expect - it might be an acquired expectation but now it would feel slightly off to me if those wouldn't display anything. "
 * [today](https://github.com/microsoft/TypeScript-go/pull/3022#issuecomment-4040754380) **jakebailey** said "Yes, I would tend to agree, that if we are hovering on an identifier-y thing, we need to display something..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3022#issuecomment-4040826352) **ahejlsberg** disagreed that displaying `any` helps when `GetTypeAtLocation` returns the error type because it is indistinguishable from a real `any`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3022#issuecomment-4040951595) **Andarist** demonstrated cross-location consistency using a TypeScript code example

### [PR microsoft/TypeScript-go#3037](https://github.com/microsoft/TypeScript-go/pull/3037) (Closed)

**Move extension status entirely into language status bar, drop warning color**

*Integrate extension status into the language status bar without warning color, but struggle with default pinning and visibility.*

 * created by **jakebailey**
 * (yesterday) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3037#issuecomment-4040020713) **jakebailey** admitted should have tested with a real version and noted the result looked bad
 * [today](https://github.com/microsoft/TypeScript-go/pull/3037#issuecomment-4040622765) **jakebailey** admitted forgetting to update

### [PR microsoft/TypeScript-go#3045](https://github.com/microsoft/TypeScript-go/pull/3045) (Closed, **RyanCavanaugh**, **Copilot**)

**Port scanRegularExpressionWorker to enable regex body validation**

*Port TypeScript's scanRegularExpressionWorker into the Go scanner to enable comprehensive regex literal structural validation and flag error reporting.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3055](https://github.com/microsoft/TypeScript-go/pull/3055) (Closed)

**Fix JSX runtime indirect calls**

*Update the JSX runtime to correctly mark indirect calls for proper handling.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3056](https://github.com/microsoft/TypeScript-go/pull/3056) (Closed)

**Replace const with var in CJS emit**

*visitTopLevelExportDeclaration in CJS emit always uses var declarations instead of const, causing inconsistency with other emit paths*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3058](https://github.com/microsoft/TypeScript-go/issues/3058) (Closed)

**panic: program not found in counter**

*A panic occurs in programCounter.Deref with 'program not found in counter' when running internal fourslash manual tests*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3058#issuecomment-4036481076) **jakebailey** said "go test -count=100 ./internal/fourslash/tests/manual repros it for me fairly consistently."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3058#issuecomment-4036554520) **jakebailey** used GODEBUG to generate a stack trace showing a panic ‘program not found in counter’
 * [today](https://github.com/microsoft/TypeScript-go/issues/3058#issuecomment-4036953105) **jakebailey** said "I have a very complicated fix"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3058#issuecomment-4041991276) **jakebailey** said "Fixed by #3062"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3059](https://github.com/microsoft/TypeScript-go/pull/3059) (Closed)

**Fix double deref, races**

*Lock reference counting and snapshot retrieval to prevent races, ensure proper ref/unref handling, and add negative count assertions.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3059#issuecomment-4040288586) **andrewbranch** suggested simplifying ref counting by only referencing the current snapshot since old snapshots aren’t used
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3061](https://github.com/microsoft/TypeScript-go/pull/3061) (Closed)

**Port Regular Expressions checking**

*Introduce a faithful port of the existing regular expression checking code.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3061#issuecomment-4040639738) **jakebailey** said "Can you see if this works with the tests added in #2107?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3061#issuecomment-4040726976) **Andarist** said "It doesn't report the exact same errors as that PR in the regularExpressionDuplicateCapturingGroupName test - but what it does report is consistent with Strada"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3061#issuecomment-4042850773) **jakebailey** said "Okay. Strada alignment is of course good 😄 "

### [PR microsoft/TypeScript-go#3062](https://github.com/microsoft/TypeScript-go/pull/3062) (Closed)

**Remove snapshot ref counting**

*Remove snapshot reference counting from the parse cache since it’s unused and adds unnecessary complexity.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3063](https://github.com/microsoft/TypeScript-go/pull/3063) (Closed, **RyanCavanaugh**, **Copilot**)

**Parenthesize typeof in postfix type contexts**

*Adjust Go AST printer to parenthesize typeof expressions in postfix contexts, producing (typeof C)[] instead of typeof C[].*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3064](https://github.com/microsoft/TypeScript-go/pull/3064) (Closed)

**Don't use our parser in bundled/generate\.go**

*Replace the custom JSONC parser in bundled/generate.go with simple comment stripping and the standard json package.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3065](https://github.com/microsoft/TypeScript-go/pull/3065) (Closed)

**Set GODEBUG=tracebackancestors in testing**

*Enable GODEBUG=tracebackancestors during testing to capture more comprehensive goroutine stack traces including originating test contexts at negligible performance cost.*

 * created by **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3065#issuecomment-4047842062) **gabritto** said "Could this be any helpful for when people show up reporting crashes with just a stack trace?"

### [PR microsoft/TypeScript-go#3066](https://github.com/microsoft/TypeScript-go/pull/3066) (Closed)

**Fixed encoding bug in sourcemaps by fixing \`EncodeURI\`**

*Update to EncodeURI function to correct character encoding errors in generated sourcemaps.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3067](https://github.com/microsoft/TypeScript-go/pull/3067) (Closed)

**Avoid constructing unused transformers**

*Skip constructing transformers for high targets and eliminate the now-unnecessary internal checks.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3068](https://github.com/microsoft/TypeScript-go/pull/3068) (Closed)

**Preserve comments in empty JSX expressions during JSX emit**

*Ensure comments within empty JSX expressions are preserved when emitting JSX output.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3069](https://github.com/microsoft/TypeScript-go/pull/3069) (Closed)

**Improve snapshotFSBuilder FileExists and reloadEntryIfNeeded performance**

*Optimized snapshotFSBuilder by improving FileExists and reducing lock contention, resulting in a 32% speedup on large codebases.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3069#issuecomment-4043073344) **andrewbranch** said "whoa, preexisting race must have been coincidentally prevented by accidental contention!"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3069#issuecomment-4043148535) **andrewbranch** said "sorry, one more"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3070](https://github.com/microsoft/TypeScript-go/pull/3070) (Closed)

**Add per\-directory module resolution cache**

*Add per-directory module resolution caching to reduce lock contention and improve performance, demonstrating up to 1.25x speedups in large projects.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3070#issuecomment-4043364505) **camchenry** thanked maintainers and asked whether cache invalidation is needed for long-running processes
 * [today](https://github.com/microsoft/TypeScript-go/pull/3070#issuecomment-4043378431) **andrewbranch** explained that module resolution rebuilt programs from scratch due to immutability, sometimes using minimal clones, and noted that Strada’s cache reuse logic was too complex
 * [today](https://github.com/microsoft/TypeScript-go/pull/3070#issuecomment-4043468391) **camchenry** thanked for the explanation and noted that building from scratch was sensible for future optimizations

### [PR microsoft/TypeScript-go#3071](https://github.com/microsoft/TypeScript-go/pull/3071) (Closed)

**Fix \`"use strict"\` emit, again**

*Update the 'use strict' directive emission logic to ensure it matches Strada behavior.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3072](https://github.com/microsoft/TypeScript-go/issues/3072) (Open)

**getTargetOfType panics on non\-generic types via the api server**

*getTargetOfType panics on intersection or union types instead of returning null as expected*

 * created by **souporserious**

### [PR microsoft/TypeScript-go#3073](https://github.com/microsoft/TypeScript-go/pull/3073) (Closed)

**Port missing \_\_makeTemplateObject transform, fix octal scanning**

*Add the missing __makeTemplateObject transform to handle ES2018+ template literal escapes with subtree optimization and correct octal scanning.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3074](https://github.com/microsoft/TypeScript-go/pull/3074) (Closed)

**Preserve detached comment separator after unterminated block comments**

*Preserve detached comment separators after unterminated block comments to eliminate unnecessary diffs.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3075](https://github.com/microsoft/TypeScript-go/pull/3075) (Closed)

**Avoid duplicating comments in empty lists**

*Prevent duplicated comment entries from appearing in initially empty lists.*

 * created by **Andarist**
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3076](https://github.com/microsoft/TypeScript-go/pull/3076) (Closed)

**Align enum emit with Strada, fix inlining of imported enum members**

*Resolve imported enum member values during transformation so generated enum emit matches Strada's output.*

 * created by **AlCalzone**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3076#issuecomment-4045824917) **AlCalzone** said "After rebasing I realized there are many more differences in enum emit. The most recent commit fixes those diffs."
 * [later](https://github.com/microsoft/TypeScript-go/pull/3076#issuecomment-4047411373) **jakebailey** mentioned working on a related branch that removed the ability to emit enums without consulting the type checker, suggested discussing resolver usage in a design meeting, and noted possible further deletions not included in the PR

### [PR microsoft/TypeScript-go#3077](https://github.com/microsoft/TypeScript-go/pull/3077) (Closed)

**Preserve declaration comments on list elements and JSDoc type assertions**

*Comments on list element declarations and JSDoc type assertions should be preserved during code transformations.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3078](https://github.com/microsoft/TypeScript-go/pull/3078) (Closed)

**add nil guard for \`getTypeOfSymbol\` in checker**

*Add nil guard to getTypeOfSymbol so unbound synthetic nodes return unknownType instead of causing a panic.*

 * created by **sczesny**

