# Report for 2026-05-18 (Monday, May 18th, 2026)

12 different users commented on 56 different issues.

## Recommended Actions

 * Response Recommended
    * @Zelys-DFKH provided the root cause and announced a fix with an incoming PR in [microsoft/TypeScript-go#3976](https://github.com/microsoft/TypeScript-go/issues/3976#issuecomment-4482730647)
    * @danyalahmed1995 provided repro steps as requested in [microsoft/TypeScript-go#3983](https://github.com/microsoft/TypeScript-go/issues/3983#issuecomment-4488712247)

## Activity Summary

### [PR microsoft/TypeScript-go#3159](https://github.com/microsoft/TypeScript-go/pull/3159) (Open, **jakebailey**, **Copilot**)

**Fix format selection deleting comments when selection ends inside comment trivia**

*A format selection operation that ends within a comment in JS/TS code deletes the comment.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3159#issuecomment-4195608650) **jakebailey** said "@copilot address review comments"
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3159#issuecomment-4195634797) **Copilot** addressed all three review comments in commit 11fd998d by fixing misleading position comments, renaming the test description, and replacing loose assertions with exact checks
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3159#issuecomment-4479867256) **jakebailey** said "@copilot+gpt-5.5 merge main and fix the issues"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3159#issuecomment-4480080104) **Copilot** merged origin/main, fixed format settings API issues, verified build, test, and lint passed, reported format failure due to plugins.dprint.dev DNS block, and suggested updating Actions setup or allowlist

### [PR microsoft/TypeScript-go#3495](https://github.com/microsoft/TypeScript-go/pull/3495) (Open)

**Use JS\-compatible Unicode casing for intrinsic string mappings**

*Implement JavaScript-compatible Unicode casing rules in TypeScript’s intrinsic string mapping functions.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4476496557) **Andarist** explained that using Go's unicode ranges wasn't possible, added a code comment, and implemented a commitable code generator to keep the output file up to date
 * [today](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4478753309) **jakebailey** said "See also https://github.com/microsoft/typescript-go/pull/3930 which uses x/text for this, though I'm wary of that too..."
 * [later](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4486782037) **Andarist** mentioned having used AI assistance to draft an uncommitted audit script for js casing and shared its code
 * [later](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4488896476) **jakebailey** said "What were the results of the analysis? What is the difference?"

### [Issue microsoft/TypeScript-go#3612](https://github.com/microsoft/TypeScript-go/issues/3612) (Closed, `Needs More Info`)

**Intermittent tsgo build failures with incorrect inferences**

*tsgo intermittently misinfers arktype-inferred referenced types as empty objects, causing build failures in incremental builds*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4392365318) **kwonoj** acknowledged difficulty diagnosing without a repro and asked if there were diagnostic logs to collect
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4392876439) **RyanCavanaugh** suggested setting a coding agent to produce a minimal shareable version and linked a relevant TypeScript Maintainer Skills resource
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4392883922) **kwonoj** said "Build time is somewhat larger, but I can spin a remote box to keep spinning. Thanks for the suggestion, will give it a go and come back later."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4481350945) **RyanCavanaugh** said "Closing due to lack of repro. Please open a new issue if one is found or constructed. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3692](https://github.com/microsoft/TypeScript-go/issues/3692) (Closed)

**Excessive CPU usage**

*WebStorm’s ts-go server often consumes 80-100% CPU when adding new imports in a monorepo frontend until restarted.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4425907817) **AndrewSouthpaw** asked what diagnostic information could be collected to help investigate tsgo's high CPU usage
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4426707829) **andrewbranch** asked whether the reporter was using WebStorm, suggested reproducing the issue in VS Code and using TypeScript Native Preview commands to gather logs and CPU profiles, and recommended collecting logs and CPU profiles when reproducing in WebStorm
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4463720030) **Jelcoo** noted that WebStorm had no built-in CPU profiling and that using lsp4ij caused issues and failed to initialize the project
 * **RyanCavanaugh** removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4481357962) **RyanCavanaugh** said "Lacking concrete info, we have to consider this external for now. Please open a new issue if a supported repro is found or constructed. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3733](https://github.com/microsoft/TypeScript-go/issues/3733) (Open, `Domain: Editor`, `Needs More Info`)

**No autocomplete for local symbols and some global types when creating a new file**

*VS Code fails to autocomplete or auto-import local symbols and ESNext types like Temporal in new TypeScript files until restart.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3733#issuecomment-4408882714) **RyanCavanaugh** said "We really need concrete file contents in order to investigate these kinds of things."
 * **RyanCavanaugh** added label `Needs More Info`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3733#issuecomment-4460635515) **jansedlon** provided a partial repro showing that the Temporal namespace was not recognized initially when typing 'type A = Temporal.' in a new file and noted inability to reproduce the local exports issue
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3733#issuecomment-4481422378) **RyanCavanaugh** asked which aspect (12,000 files, monorepo, tsconfig, etc.) was causing the issue

### [PR microsoft/TypeScript-go#3798](https://github.com/microsoft/TypeScript-go/pull/3798) (Closed, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.35\.2 to 4\.35\.4 in the github\-actions group across 1 directory**

*Bump github/codeql-action from version 4.35.2 to 4.35.4 to update the default CodeQL bundle to v2.25.4.*

 * (1 week ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3798#issuecomment-4481324846) **dependabot[bot]** said "Looks like github/codeql-action is updatable in another way, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript-go#3814](https://github.com/microsoft/TypeScript-go/issues/3814) (Closed, `wontfix`)

**\`skipLibCheck\` does not suppress TS2430 for interface merging errors originating in user code**

*Using skipLibCheck with tsgo fails to suppress TS2430 interface merging errors in user code.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3814#issuecomment-4433187187) **RyanCavanaugh** said "This seems like a bug in 6.0 more than anything. It's super weird that you could put an invalid declaration in user code and not get an error just because skipLibCheck is on."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3814#issuecomment-4433206174) **jakebailey** said "This is definitely an intentional change, because we issue the errors on whichever thing we see first and therefore this is not deterministic, so we issue it everywhere"
 * **RyanCavanaugh** added label `wontfix`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3815](https://github.com/microsoft/TypeScript-go/issues/3815) (Closed, `wontfix`)

**\`skipLibCheck\` does not suppress TS2320 when module augmentation in \`\.ts\` triggers interface merging conflict from \`\.d\.ts\`**

*skipLibCheck doesn't suppress TS2320 error caused by module augmentation in .ts exposing conflicting check signatures from .d.ts*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4433834754) **jfirebaugh** said "It repros without = any."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4456030799) **Okanlawon2259** said "It's just any seem others are perfect "
 * **RyanCavanaugh** added label `wontfix`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3876](https://github.com/microsoft/TypeScript-go/issues/3876) (Closed, `bug`, `Domain: Editor`, `Crash`, **DanielRosenwasser**, **Copilot**)

**Error when retrieving diagnostics**

*Retrieving diagnostics in the TypeScript language server fails due to an error parsing object literal expressions.*

 * (3 days ago) **DanielRosenwasser** added label `bug`, and assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3877](https://github.com/microsoft/TypeScript-go/pull/3877) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix panic in getTsConfigObjectLiteralExpression for malformed tsconfig**

*getTsConfigObjectLiteralExpression now checks for object literals to avoid panicking on malformed tsconfig.json values, and a test case was added.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3877#issuecomment-4465771376) **DanielRosenwasser** said "@copilot fix it"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3877#issuecomment-4465830661) **Copilot** acknowledged that the original test didn’t exercise the diagnostic explanation code and updated the test to use an array-literal tsconfig to trigger the crash path
 * [today](https://github.com/microsoft/TypeScript-go/pull/3877#issuecomment-4479412000) **RyanCavanaugh** updated the test to use a specific compilerOptions types array and confirmed that this triggers the tsgo cmdline crash
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3879](https://github.com/microsoft/TypeScript-go/pull/3879) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil dereference in resolveHelpersModule via checkExternalEmitHelpers**

*Prevent nil dereference in resolveHelpersModule by falling back to file.AsNode when checkExternalEmitHelpers runs without an import specifier.*

 * created by **Copilot**
 * (3 days ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3879#issuecomment-4480157845) **DanielRosenwasser** said "@copilot I don't see a panic from that test locally."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3879#issuecomment-4480319374) **Copilot** verified that tests did not panic without the fix, proposed a theory regarding project references with differing importHelpers settings, removed irrelevant tests, retained the defensive nil check, and offered to add a proper test if provided with a repro case

### [Issue microsoft/TypeScript-go#3883](https://github.com/microsoft/TypeScript-go/issues/3883) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when inferring \[\.\.\.rest, \.\.\.T\] from a tuple shorter than fixed\-arity constraint**

*tsgo panics from slice bounds error when inferring rest and generic types from too-short tuples*

 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3883#issuecomment-4467960569) **jakebailey** said "I think this effectively https://github.com/microsoft/typescript-go/pull/2928, https://github.com/microsoft/TypeScript/issues/63199"
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3886](https://github.com/microsoft/TypeScript-go/issues/3886) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo printer panics when emitting declarations for CommonJS files with numeric export names**

*tsgo printer panics when emitting declarations for CommonJS files with numeric export names*

 * **mariusschulz** added label `Crash`
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3891](https://github.com/microsoft/TypeScript-go/issues/3891) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when an anonymous class declaration has a member decorator when downleveling to ES2022**

*tsgo panics with a debug assertion failure when downleveling anonymous classes with member decorators to ES2022*

 * **mariusschulz** added label `Crash`
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3894](https://github.com/microsoft/TypeScript-go/issues/3894) (Closed, **jakebailey**, **Copilot**)

**tsgo JSX entity decoder skips entities that follow a non\-entity ampersand**

*tsgo’s JSX entity decoder fails to decode valid entities immediately following a standalone ampersand, resulting in literal entity strings in the output.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3894#issuecomment-4467303139) **jakebailey** said "Could be my code was wrong in https://github.com/microsoft/typescript-go/pull/2510"
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3897](https://github.com/microsoft/TypeScript-go/pull/3897) (Closed, **jakebailey**, **Copilot**)

**Fix JSX entity decoder skipping entities after non\-entity ampersand**

*Update JSX entity decoder to skip intervening non-entity ampersands and correctly decode entities.*

 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3897#issuecomment-4474627711) **jakebailey** said "@copilot+claude-opus-4.6 address comments"
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3898](https://github.com/microsoft/TypeScript-go/issues/3898) (Closed, **jakebailey**, **Copilot**)

**tsgo creates a distinct enum literal type for each NaN\-valued enum member**

*tsgo treats NaN-valued enum members as distinct literal types, causing assignment errors between them*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3898#issuecomment-4467309242) **jakebailey** said "That or NaN is not NaN and is being keyed somewhere (Go maps hash every NaN as new items)"
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3906](https://github.com/microsoft/TypeScript-go/issues/3906) (Closed, **jakebailey**, **Copilot**)

**tsgo emits incorrect string value when encountering a backslash before a non\-special character**

*tsgo emits invalid Unicode escape sequences for enum string values containing backslashes before non-special characters.*

 * created by **mariusschulz**
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3911](https://github.com/microsoft/TypeScript-go/pull/3911) (Closed, **jakebailey**, **Copilot**)

**Fix scanEscapeSequence for multi\-byte UTF\-8 characters after backslash**

*Fix scanEscapeSequence to correctly decode multi-byte UTF-8 escape sequences including U+2028/U+2029 and set containsNonASCII=true.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3912](https://github.com/microsoft/TypeScript-go/pull/3912) (Open, **jakebailey**, **Copilot**)

**Fix type soundness for lone\-surrogate string literals**

*Ensure lone-surrogate string literals are encoded and compared distinctly to maintain type soundness and correctness.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3912#issuecomment-4481020164) **DanielRosenwasser** pointed out that other code paths rely on string text and may need adjustment
 * [today](https://github.com/microsoft/TypeScript-go/pull/3912#issuecomment-4481127125) **jakebailey** said "@copilot apply changes based on the comments in this thread"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3912#issuecomment-4481339817) **Copilot** fixed CompareStringsCaseInsensitive to use decodeCESU8OrUTF8 and applied extended escape surrogate handling with tests in commit ef2a8254
 * [today](https://github.com/microsoft/TypeScript-go/pull/3912#issuecomment-4481362050) **jakebailey** noted that the situation seemed spooky and suggested consistent use of WTF-8 everywhere

### [PR microsoft/TypeScript-go#3917](https://github.com/microsoft/TypeScript-go/pull/3917) (Closed, **jakebailey**, **Copilot**)

**Fix panic when inferring \[\.\.\.rest, \.\.\.T\] from tuple shorter than fixed\-arity constraint**

*Slice indices in [...rest, ...T] inference go negative and panic when the source tuple is shorter than the arity constraint.*

 * **Copilot** assigned to **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3917#issuecomment-4470720336) **ahejlsberg** said "@copilot resolve the merge conflicts in this pull request"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3917#issuecomment-4470768518) **Copilot** resolved the merge conflict in internal/checker/inference.go and combined the bounds check with the restType guard
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3919](https://github.com/microsoft/TypeScript-go/pull/3919) (Closed, **jakebailey**, **Copilot**)

**Handle numeric literal export names in declaration emit**

*Fix declaration emit to convert numeric export names to string literals, preventing printer panics and invalid syntax.*

 * **Copilot** assigned to **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3919#issuecomment-4470587854) **ahejlsberg** said "@copilot Please make the requested changes."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3919#issuecomment-4470705583) **ahejlsberg** agreed that converting numeric literals to string literals was best and contrasted with Strada's approach
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3926](https://github.com/microsoft/TypeScript-go/pull/3926) (Closed, **jakebailey**, **Copilot**)

**Fix panic on anonymous class declaration with decorator targeting ES2022**

*Prevent panic on anonymous class decorators targeting ES2022 by naming classes, optimizing traversal, adding tests, and enabling experimental decorators.*

 * **Copilot** assigned to **jakebailey**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3926#issuecomment-4468394332) **jakebailey** said "@copilot apply changes based on the comments in this thread"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3926#issuecomment-4468420316) **Copilot** applied both requested changes: short-circuited ChildIsDecorated behind name == nil and replaced hardcoded false with tx.compilerOptions.ExperimentalDecorators.IsTrue()
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3931](https://github.com/microsoft/TypeScript-go/pull/3931) (Open, **jakebailey**, **Copilot**)

**Fix \-NaN emission for enum members in declaration output**

*Fix -NaN emission for enum members in declaration output by adding explicit NaN and Infinity checks*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3931#issuecomment-4482202170) **jakebailey** said "@copilot+gpt-5.5 merge main and update baselines"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3931#issuecomment-4482377077) **Copilot** merged latest main and updated affected enum NaN baseline, then reported that build, test, lint, format, and validation checks passed

### [PR microsoft/TypeScript-go#3932](https://github.com/microsoft/TypeScript-go/pull/3932) (Closed, **jakebailey**, **Copilot**)

**Fix NaN\-valued enum members creating distinct literal types**

*Add specialized handling to ensure NaN-valued enum members share the same literal type within an enum but remain distinct across different enums.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3943](https://github.com/microsoft/TypeScript-go/pull/3943) (Open)

**Fix crash inferring constrained variadic tuples with optional elements**

*Fix compiler crash during inference of constrained variadic tuples with optional elements*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3943#issuecomment-4479716867) **jakebailey** said "We have a couple of PRs touching this same code, e.g. #3917, #2928; I feel a little unclear what combo is correct in all of these"

### [Issue microsoft/TypeScript-go#3957](https://github.com/microsoft/TypeScript-go/issues/3957) (Open, `possible improvement`, **jakebailey**, **Copilot**)

**Property names are quoted one level deep in inferred type**

*tsgo preserves quotes on one-level-deep property names in inferred types, unlike TypeScript 6.0 which strips them.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/3957#issuecomment-4479189689) **jakebailey** said "Ah, I see what you mean."
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`

### [Issue microsoft/TypeScript-go#3961](https://github.com/microsoft/TypeScript-go/issues/3961) (Closed, **jakebailey**, **Copilot**)

**Parentheses always added around \`typeof\` type expression**

*tsgo adds redundant parentheses around typeof type expressions in type aliases, altering the original code formatting.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/3961#issuecomment-4479155423) **dragomirtitian** noted that adding parentheses to user code for declaration files seemed strange and asked if it could be avoided
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3964](https://github.com/microsoft/TypeScript-go/pull/3964) (Closed, **jakebailey**, **Copilot**)

**Preserve parsed \`typeof X\` in postfix type contexts**

*Declaration emit now preserves parsed typeof expressions without parentheses in array, indexed access, and optional type contexts.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3964#issuecomment-4479605991) **jakebailey** said "@copilot apply changes based on the comments in this thread"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3964#issuecomment-4479702790) **Copilot** addressed reviewer comments by fixing a doc comment parameter name and expanding tests to cover emitArrayType and emitOptionalType paths
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3966](https://github.com/microsoft/TypeScript-go/issues/3966) (Closed, **jakebailey**, **Copilot**)

**Emojis from inferred types are written as unicode escapes in declaration files**

*Declaration files emit emojis as Unicode escape sequences instead of preserving the original emoji characters.*

 * created by **dragomirtitian**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3967](https://github.com/microsoft/TypeScript-go/pull/3967) (Closed, **jakebailey**, **Copilot**)

**Preserve non\-ASCII characters in declaration emit for string literal types**

*Preserve non-ASCII characters in string literal types in emitted declaration files by applying the no-ASCII-escaping printer flag to reused nodes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3971](https://github.com/microsoft/TypeScript-go/issues/3971) (Closed, **jakebailey**, **Copilot**)

**Assertion in JSX spread causes missing newline in JS output**

*A type assertion in a JSX spread property causes the emitted JavaScript to remove surrounding newlines when transpiled with tsgo.*

 * created by **dragomirtitian**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3972](https://github.com/microsoft/TypeScript-go/pull/3972) (Closed, **jakebailey**, **Copilot**)

**Preserve source newlines around transformer\-updated object literal properties**

*Preserve newlines around transformer-updated type-asserted object literal properties in JSX spreads by comparing original nodes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3972#issuecomment-4482971407) **jakebailey** said "If it changed, it would be in the PR; accepting a baseline does not delete it."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3973](https://github.com/microsoft/TypeScript-go/issues/3973) (Open, `Type Ordering`, **ahejlsberg**)

**Variance check skipped on union of intersections when one branch's recursive cycle goes through a covariant \`TValue\`**

*TypeScript skips variance checking on a union of intersections with a covariant recursive branch, missing type errors.*

 * created by **IanVS**
 * (today) **RyanCavanaugh** added label `Type Ordering`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3973#issuecomment-4484334937) **RyanCavanaugh** described an analogous variance-cycle issue in tsgo and explained how renaming affected error reporting

### [PR microsoft/TypeScript-go#3974](https://github.com/microsoft/TypeScript-go/pull/3974) (Open)

**fix\(checker\): check type expressions on unmatched JSDoc @param tags**

*Enable checking of type expressions on unmatched JSDoc @param tags in JavaScript files to ensure generic type errors are reported.*

 * created by **Zelys-DFKH**

### [PR microsoft/TypeScript-go#3975](https://github.com/microsoft/TypeScript-go/pull/3975) (Open, `dependencies`, `javascript`)

**Bump brace\-expansion from 5\.0\.5 to 5\.0\.6**

*Bump brace-expansion dependency from version 5.0.5 to 5.0.6.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`

### [Issue microsoft/TypeScript-go#3976](https://github.com/microsoft/TypeScript-go/issues/3976) (Open, **ahejlsberg**)

**tsgo does not correctly infer array type assignment on callable type with fields since 20260503\.1**

*Since 20260503.1 tsgo incorrectly rejects assigning [] to a callable type’s array field due to broken inference.*

 * created by **chriskrycho**
 * **jakebailey** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3976#issuecomment-4482730647) **Zelys-DFKH** pointed out the root cause was a circular type resolution path that settled [] as never[] before the annotation check and announced a tested fix with a forthcoming PR

### [PR microsoft/TypeScript-go#3977](https://github.com/microsoft/TypeScript-go/pull/3977) (Open)

**Emit publish\-order\.json with per\-package npm dist\-tag**

*Emit publish-order.json with per-package npm dist-tag entries to enable custom publisher tagging.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3978](https://github.com/microsoft/TypeScript-go/pull/3978) (Open, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Bump codecov/codecov-action from 6.0.0 to 6.0.1 and update github/codeql-action in the repository root.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [PR microsoft/TypeScript-go#3979](https://github.com/microsoft/TypeScript-go/pull/3979) (Open)

**fix\(checker\): suppress false TS7008 for empty array assigned to annotated expando property**

*Suppress the TS7008 "implicitly has any[]" error for empty array assignments to explicitly annotated expando properties on callable types.*

 * created by **Zelys-DFKH**

### [PR microsoft/TypeScript-go#3980](https://github.com/microsoft/TypeScript-go/pull/3980) (Open)

**Add \`fswatch\` package, ported from \`@parcel/watcher\` with heavy modification**

*Port @parcel/watcher to Go as fswatch, providing only Update/Delete events, non-recursive watching, and ignore support.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3980#issuecomment-4482921293) **jakebailey** said "Oh great, I forgot to check linting when I moved the code over, sigh"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3980#issuecomment-4483773513) **jakebailey** said "macOS is flaky, despite my best efforts ☹️ "

### [Issue microsoft/TypeScript-go#3981](https://github.com/microsoft/TypeScript-go/issues/3981) (Open, `bug`, `Domain: Editor`, **gabritto**)

**Excess path components suggested in completions**

*Import path completions for @typescript/native-preview/unstable repeatedly include existing segments, duplicating folder names and causing imports like unstable/unstable/ast.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, and assigned to **gabritto**

### [PR microsoft/TypeScript-go#3982](https://github.com/microsoft/TypeScript-go/pull/3982) (Open)

**Fix repeated path component in exports completions after directory separator**

*Export path completions incorrectly repeat the last directory for trailing slashes, so the fix strips the typed fragment.*

 * created by **Zelys-DFKH**

### [Issue microsoft/TypeScript-go#3983](https://github.com/microsoft/TypeScript-go/issues/3983) (Open)

**Declaration emit leaks namespace declarations for \`@internal\` functions with static property assignments**

*tsgo includes namespace declarations for internal functions with static property assignments in .d.ts files even when stripInternal is enabled*

 * created by **MgmClientGuy**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3983#issuecomment-4488712247) **danyalahmed1995** reproduced the stripInternal issue and observed that TS 6.0.3 omits the merged namespace while TS 7 native preview still emits it, indicating a declaration emit parity gap

### [Issue microsoft/TypeScript-go#3984](https://github.com/microsoft/TypeScript-go/issues/3984) (Open)

**Bloomberg feedback for 7\.0 beta**

*Bloomberg feedback highlights tsgo vs tsc declaration emit and type-checking discrepancies in the 7.0 beta, most fixed or minor.*

 * created by **dragomirtitian**

