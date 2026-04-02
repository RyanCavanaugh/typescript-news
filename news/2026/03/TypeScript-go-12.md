# Report for 2026-03-12 (Thursday, March 12th, 2026)

12 different users commented on 21 different issues.

## Recommended Actions

 * Response Recommended
    * @dan-proudfoot-bots reported that the issue still occurred and made suggestions for external packages useless in [microsoft/TypeScript-go#2576](https://github.com/microsoft/TypeScript-go/issues/2576#issuecomment-4054083735)
    * @shahmir-oscilar asked which fix was referred to in [microsoft/TypeScript-go#3081](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4050109362)
    * @shahmir-oscilar provided the entire stack trace as requested in [microsoft/TypeScript-go#3081](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4052970423)

## Activity Summary

### [PR microsoft/TypeScript-go#2322](https://github.com/microsoft/TypeScript-go/pull/2322) (Open)

**Remove GetOptionsDiagnostics**

*Remove GetOptionsDiagnostics and replace it with separate GetConfigFileParsingDiagnostics and GetGlobalDiagnostics to prevent redundant diagnostic aggregation.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2322#issuecomment-4049204728) **andrewbranch** asked if some diagnostics were generated during checker initialization due to symbol table merging and suggested distinguishing initialization diagnostics

### [Issue microsoft/TypeScript-go#2576](https://github.com/microsoft/TypeScript-go/issues/2576) (Closed, **andrewbranch**, **Copilot**)

**Autocompletions and quick fix suggestions try to import from "@types" packages**

*tsgo quick fixes and autocompletions wrongly import from @types packages instead of real modules*

 * created by **kyle-sawatsky**
 * **andrewbranch** assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2576#issuecomment-4054083735) **dan-proudfoot-bots** said "Still noticing this as of today - it makes suggestions for external packages basically useless"

### [PR microsoft/TypeScript-go#2978](https://github.com/microsoft/TypeScript-go/pull/2978) (Open, **andrewbranch**, **Copilot**)

**Fix auto\-import type modifier and formatting issues in type\-only import statements**

*Fix inline type modifiers, formatting, indentation, token handling, and import ordering in type-only import statements.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4025888666) **Copilot** fixed merge conflict and addressed feedback by deduplicating functions, adding TS comments, and updating failingTests.txt
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4025894963) **andrewbranch** said "@copilot+claude-opus-4.6 you messed up the merge, there's still a conflict and this PR now shows a massive diff from the merge commit 😠 "
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4025998453) **Copilot** fixed the merge by reverting the bad single-parent commit and re-merging origin/main with a proper two-parent merge, resulting in the PR diff showing only the intended 18 changed files
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4049675258) **jakebailey** said "Needs a merge from main and update, it seems"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4049824447) **andrewbranch** said "I wasn't ready yet!"

### [PR microsoft/TypeScript-go#3039](https://github.com/microsoft/TypeScript-go/pull/3039) (Closed)

**\[@typescript/api\] Codegen node visitor**

*Implement code generation support for the TypeScript API node visitor to automate visitor scaffolding.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3061](https://github.com/microsoft/TypeScript-go/pull/3061) (Closed)

**Port Regular Expressions checking**

*Introduce a faithful port of the existing regular expression checking code.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3061#issuecomment-4040639738) **jakebailey** said "Can you see if this works with the tests added in #2107?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3061#issuecomment-4040726976) **Andarist** said "It doesn't report the exact same errors as that PR in the regularExpressionDuplicateCapturingGroupName test - but what it does report is consistent with Strada"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3061#issuecomment-4042850773) **jakebailey** said "Okay. Strada alignment is of course good 😄 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/3061#issuecomment-4050922704) **jakebailey** said "In general, I would recheck that all of the comments are present too."

### [PR microsoft/TypeScript-go#3065](https://github.com/microsoft/TypeScript-go/pull/3065) (Closed)

**Set GODEBUG=tracebackancestors in testing**

*Enable GODEBUG=tracebackancestors during testing to capture more comprehensive goroutine stack traces including originating test contexts at negligible performance cost.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3065#issuecomment-4047842062) **gabritto** said "Could this be any helpful for when people show up reporting crashes with just a stack trace?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3065#issuecomment-4047931558) **jakebailey** considered limiting the setting to testing, potentially only for concurrent multiproject cases
 * [today](https://github.com/microsoft/TypeScript-go/pull/3065#issuecomment-4047966384) **jakebailey** said "Reverted the cmd/tsgo change, and upped the number to 10 for testing, since there's testing infra overhead."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3068](https://github.com/microsoft/TypeScript-go/pull/3068) (Closed)

**Preserve comments in empty JSX expressions during JSX emit**

*Ensure comments within empty JSX expressions are preserved when emitting JSX output.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3071](https://github.com/microsoft/TypeScript-go/pull/3071) (Closed)

**Fix \`"use strict"\` emit, again**

*Update the 'use strict' directive emission logic to ensure it matches Strada behavior.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3076](https://github.com/microsoft/TypeScript-go/pull/3076) (Closed)

**Align enum emit with Strada, fix inlining of imported enum members**

*Resolve imported enum member values during transformation so generated enum emit matches Strada's output.*

 * created by **AlCalzone**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3076#issuecomment-4045824917) **AlCalzone** said "After rebasing I realized there are many more differences in enum emit. The most recent commit fixes those diffs."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3076#issuecomment-4047411373) **jakebailey** mentioned working on a related branch that removed the ability to emit enums without consulting the type checker, suggested discussing resolver usage in a design meeting, and noted possible further deletions not included in the PR
 * [today](https://github.com/microsoft/TypeScript-go/pull/3076#issuecomment-4048018358) **AlCalzone** offered to close the issue and noted that the only remaining diff between Strada and Corsa caused a runtime error
 * (today) **AlCalzone** closed the issue
 * (today) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3076#issuecomment-4048031606) **jakebailey** expressed a desire to keep the issue open and acknowledged misunderstanding about the crash
 * [today](https://github.com/microsoft/TypeScript-go/pull/3076#issuecomment-4048057332) **AlCalzone** said "Right, I didn't explicitly say so - my bad. The import is elided, but still used in the enum definition."

### [PR microsoft/TypeScript-go#3077](https://github.com/microsoft/TypeScript-go/pull/3077) (Closed)

**Preserve declaration comments on list elements and JSDoc type assertions**

*Comments on list element declarations and JSDoc type assertions should be preserved during code transformations.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3078](https://github.com/microsoft/TypeScript-go/pull/3078) (Closed)

**add nil guard for \`getTypeOfSymbol\` in checker**

*Add nil guard to getTypeOfSymbol so unbound synthetic nodes return unknownType instead of causing a panic.*

 * created by **sczesny**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3078#issuecomment-4048080631) **ahejlsberg** said "@sczesny Can we get a repro for the issue?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3078#issuecomment-4048514845) **sczesny** explained that they had mistakenly modified their own Transformer, noted that adding a nil check fixed the issue, and apologized for wasting time
 * (today) **sczesny** closed the issue

### [PR microsoft/TypeScript-go#3079](https://github.com/microsoft/TypeScript-go/pull/3079) (Closed)

**Fix issues in Quick Info for symbol\-less nodes**

*Adds missing non-null assertion and refactors Quick Info logic to handle all symbol-less declaration nodes without a position parameter.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3080](https://github.com/microsoft/TypeScript-go/pull/3080) (Closed)

**Fixing encoder/decoder bugs**

*Decode this, super, and import keywords as KeywordExpression nodes and preserve const/let flags in binary AST encode/decode.*

 * created by **navya9singh**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3081](https://github.com/microsoft/TypeScript-go/issues/3081) (Open)

**Stack overflow in multi\-threaded mode during type instantiation**

*tsgo 7.0.0-dev encounters a goroutine stack overflow in multi-threaded type instantiation on a large React/TypeScript codebase, while single-threaded mode works.*

 * created by **shahmir-oscilar**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4049976723) **jakebailey** asked which fix was being referred to
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4050109362) **shahmir-oscilar** asked which fix was referred to and reported that version 7.0.0-dev.20260309.1 produced namespace errors in node_modules while 20260310.1 singleThreaded did not, and noted removing singleThreaded causes a reproducible stack overflow
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4050199939) **jakebailey** said "Yes, we got rid of that error. I don't think that's related."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4050894285) **ahejlsberg** said "Hmm, the checker.(*NodeBuilderImpl) on the stack means we're serializing something, probably because we're building a diagnostic message. Can you post the bottom 100 and top 100 frames of the stack?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4052970423) **shahmir-oscilar** shared the entire stack trace in an attached file
 * [later](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4055740225) **ahejlsberg** identified a circularity error in getTypeOfMappedSymbol and asked for a repro

### [PR microsoft/TypeScript-go#3082](https://github.com/microsoft/TypeScript-go/pull/3082) (Closed, **andrewbranch**, **Copilot**)

**API: Add modifierFlags, getResolvedSymbol, fix BlockScoped flags and empty NodeList mask encoding**

*Implements modifierFlags and getResolvedSymbol in the TypeScript API and fixes block-scoped flags and empty NodeList mask encoding in the binary protocol*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4050735968) **Copilot** described reverting encoding changes and implementing client-side computation of modifierFlags and getResolvedSymbol to match existing server-side logic
 * [today](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4050828232) **Copilot** added ModifierFlags to enumDefs, auto-generated it from internal/ast/modifierflags.go, and imported and re-exported it for both async and sync APIs
 * [today](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4051023204) **Copilot** listed the commits containing tests and described their coverage across async and sync API suites
 * [today](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4051065262) **andrewbranch** said "@copilot format"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4051093786) **Copilot** formatted code in commit fa81eb8 and noted that dprint reformatted import ordering and switch-case style in node.ts

### [PR microsoft/TypeScript-go#3083](https://github.com/microsoft/TypeScript-go/pull/3083) (Closed)

**Remove JSDocParsingMode from API scanner**

*Remove the obsolete JSDocParsingMode option from the API scanner since it predates the #2801 port.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3084](https://github.com/microsoft/TypeScript-go/pull/3084) (Open)

**Port LSP update imports on file rename support**

*Adds support to update import paths via LSP when files are renamed or moved to ensure correct relative references.*

 * created by **anchmelev**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4052113218) **anchmelev** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#3085](https://github.com/microsoft/TypeScript-go/pull/3085) (Open)

**API: Small bug fixes**

*Fixed three bugs causing panics: empty array truthy check, RemoteNode.getNamedChild crash on no children, and arrow function printing nil check.*

 * created by **navya9singh**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3085#issuecomment-4053358530) **navya9singh** said "@copilot format"

### [Issue microsoft/TypeScript-go#3086](https://github.com/microsoft/TypeScript-go/issues/3086) (Open, `Crash`)

**panic: cache entry not found**

*Cloning a project snapshot panics due to a missing RefCountCache entry.*

 * created by **nnnnoel**
 * **nnnnoel** added label `Crash`

### [Issue microsoft/TypeScript-go#3087](https://github.com/microsoft/TypeScript-go/issues/3087) (Closed, `Crash`)

**panic handling request textDocument/documentHighlight: runtime error: invalid memory address or nil pointer dereference**

*The TypeScript-Go LSP server panics with a nil pointer dereference during textDocument/documentHighlight requests.*

 * created by **Zzzen**
 * **Zzzen** added label `Crash`

### [PR microsoft/TypeScript-go#3088](https://github.com/microsoft/TypeScript-go/pull/3088) (Closed)

**fix\(checker\): add nil guard for thisType in getThisType**

*Add a nil guard in getThisType to prevent errors when thisType is nil.*

 * created by **Zzzen**

