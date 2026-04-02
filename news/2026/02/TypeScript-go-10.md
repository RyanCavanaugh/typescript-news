# Report for 2026-02-10 (Tuesday, February 10th, 2026)

12 different users commented on 72 different issues.

## Recommended Actions

 * Response Recommended
    * @jumbosushi asked if there was anything they could do to help move it forward in [microsoft/TypeScript-go#2408](https://github.com/microsoft/TypeScript-go/pull/2408#issuecomment-3880194584)
    * @Knagis reported that it still crashes with version 7.0.0-dev.20260211.1 in [microsoft/TypeScript-go#2522](https://github.com/microsoft/TypeScript-go/issues/2522#issuecomment-3884449949)
    * @devanshj asked for the TypeScript team's thoughts on the idea in [microsoft/TypeScript-go#2629](https://github.com/microsoft/TypeScript-go/pull/2629#issuecomment-3880240293)
    * @christophe-g provided repro steps in [microsoft/TypeScript-go#2720](https://github.com/microsoft/TypeScript-go/issues/2720#issuecomment-3882775193)
    * @Faithfinder provided updated results as requested in [microsoft/TypeScript-go#2721](https://github.com/microsoft/TypeScript-go/issues/2721#issuecomment-3879877541)

## Activity Summary

### [PR microsoft/TypeScript-go#1995](https://github.com/microsoft/TypeScript-go/pull/1995) (Closed, **DanielRosenwasser**, **Copilot**)

**Add fourslash support for LSP formatting requests**

*Implements LSP document, range, and on-type formatting in the fourslash test harness with both baseline-based and in-place verification methods.*

 * **Copilot** assigned to **DanielRosenwasser**
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1995#issuecomment-3475064264) **DanielRosenwasser** said "Now do my bidding @copilot."
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1995#issuecomment-3475095889) **Copilot** implemented all requested methods in commit a0c8f66c matching the TypeScript fourslash API
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2251](https://github.com/microsoft/TypeScript-go/pull/2251) (Open)

**  Fix: Add mutex protection for projects map to prevent race conditions**

*Add mutex-based read and write locking for the API projects map to prevent concurrent data races.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2251#issuecomment-3619729436) **microsoft-github-policy-service[bot]** reminded the contributor to read and agree to the Contributor License Agreement by replying with the specified command
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2251#issuecomment-3619742802) **Catsayer-Chan** said " @microsoft-github-policy-service agree"
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2251#issuecomment-3629402303) **jakebailey** said "Where are you using this API such that it matters for you? It's not guaranteed to work and I'm not sure we are expecting people to use it truly concurrently on the client side yet?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2251#issuecomment-3880087810) **jakebailey** said "The API code has changed a lot since this PR was sent. Is this still needed?"

### [PR microsoft/TypeScript-go#2408](https://github.com/microsoft/TypeScript-go/pull/2408) (Open, **jakebailey**, **Copilot**)

**Fix declaration emit to retain imports for unresolved type aliases**

*Retain imports for unresolved type aliases in declaration emit with --noResolve when using as casts.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2408#issuecomment-3668663525) **Copilot** ran the tests and reported that their specific test case passed and that the two failing tests were pre-existing failures unrelated to their changes
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2408#issuecomment-3668728496) **jakebailey** refuted copilot’s suggestion, stating that main is clean and the issue was due to its changes
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2408#issuecomment-3668764482) **Copilot** acknowledged test failures were caused by his changes and refined the fix to only add import tracking for unresolved symbols without changing type serialization, improved the baseline to include foo3's Unresolved import, and confirmed all tests passed
 * [today](https://github.com/microsoft/TypeScript-go/pull/2408#issuecomment-3880194584) **jumbosushi** said "@jakebailey sorry for the ping, but just checking in on this 👀 is there anything I can do to help move it forward? also ran into the referenced issue"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2408#issuecomment-3880250353) **jakebailey** said "I don't think this PR is correct, unfortunately"

### [Issue microsoft/TypeScript-go#2522](https://github.com/microsoft/TypeScript-go/issues/2522) (Open, `Domain: Declaration Emit`, `Crash`, **weswigham**)

**Reexporting @types/micromatch@4\.0\.10 from a \.cjs file crashes**

*Re-exporting @types/micromatch@4.0.10 from a .cjs file crashes the TypeScript declaration transformer with a ‘Diagnostic emitted without context’ panic.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2522#issuecomment-3759406281) **Knagis** mentioned that version 7.0.0-dev.20251027.1 compiled without crashes but version 7.0.0-dev.20251029.1 crashed
 * (3 weeks ago) **ahejlsberg** added label `Domain: Declaration Emit`, and assigned to **weswigham**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2522#issuecomment-3884449949) **Knagis** reported that it still crashed with version 7.0.0-dev.20260211.1 and provided a panic stack trace

### [Issue microsoft/TypeScript-go#2559](https://github.com/microsoft/TypeScript-go/issues/2559) (Closed, `Crash`, **andrewbranch**, **Copilot**)

**Quick fix crash when promoting type\-only import to value and existing type import precedes new value import**

*Converting a type-only import to a value import via quick fix panics the TypeScript language server.*

 * (2 weeks ago) **DanielRosenwasser** assigned to **andrewbranch**, and unassigned **jakebailey**
 * **andrewbranch** assigned to **Copilot**
 * (later) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2569](https://github.com/microsoft/TypeScript-go/pull/2569) (Closed, **andrewbranch**, **Copilot**)

**Fix getVisualListRange bug in formatting \(partial fix for import promotion crash\)**

*Use GetStartOfNode instead of Pos in getVisualListRange to skip trivia and prevent import promotion formatting crashes.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786881437) **Copilot** fixed tests failing by addressing two bugs in getVisualListRange and import reordering logic
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786979320) **Copilot** reverted to a simple fix in commit a1301d95 and removed complex autoimport and investigation changes
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3873204123) **andrewbranch** said "I don't have time to fix the bad formatting right now, but I think we should accept the crash fix and do a follow-up sweep of formatting fixes."
 * (later) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2629](https://github.com/microsoft/TypeScript-go/pull/2629) (Open)

**Experiment: Distribute Control Flow**

*TypeScript fails to distribute union types when mapping over a discriminated union array and returning the same object*

 * created by **devanshj**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2629#issuecomment-3880082988) **jakebailey** said "I don't know that this is in scope: https://github.com/microsoft/typescript-go/blob/main/CONTRIBUTING.md#scope-of-acceptable-changes"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2629#issuecomment-3880240293) **devanshj** said "I see yeah that's okay this is anyway a throw away POC... I'm more interested in knowing the typescript team's thoughts on this idea than getting this merged :)"

### [Issue microsoft/TypeScript-go#2650](https://github.com/microsoft/TypeScript-go/issues/2650) (Closed, `Crash`, **jakebailey**, **Copilot**)

**Specifying declaration files in "moduleSuffixes" leads to panic**

*Including declaration files in moduleSuffixes triggers a panic in typescript-go’s checker during external module resolution.*

 * **voronin-ivan** added label `Crash`
 * (5 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2650#issuecomment-3880149106) **jakebailey** said "@voronin-ivan Can you retry with the latest nightly? I suspect this was fixed in #2680."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2650#issuecomment-3883950997) **voronin-ivan** said "@jakebailey I can confirm it has been fixed, thank you!"
 * (later) **voronin-ivan** closed the issue

### [Issue microsoft/TypeScript-go#2667](https://github.com/microsoft/TypeScript-go/issues/2667) (Closed, **DanielRosenwasser**, **Copilot**)

**Quick info/hover on ambient module shows \`namespace\` keyword**

*Quick info on ambient module declarations erroneously displays the ‘namespace’ keyword instead of ‘module’.*

 * created by **DanielRosenwasser**
 * (1 week ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2668](https://github.com/microsoft/TypeScript-go/pull/2668) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix hover text for ambient modules to display "module" instead of "namespace"**

*Update quick info hover for ambient modules to correctly display 'module' instead of 'namespace'.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2668#issuecomment-3880788671) **DanielRosenwasser** said "I think so"
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2694](https://github.com/microsoft/TypeScript-go/pull/2694) (Closed, **jakebailey**, **Copilot**)

**Fix panic when moduleSuffixes resolves to declaration files**

*Fix panic by extracting file extensions from the original candidate path when moduleSuffixes includes declaration file suffixes.*

 * **Copilot** assigned to **jakebailey**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2694#issuecomment-3854845143) **jakebailey** said "@copilot You didn't make a test and show that it failed. This may well be the right change, but without a test we can't verify the solution."
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2694#issuecomment-3854907655) **Copilot** added a failing test case in commit 88ad6db5 reproducing the panic and explained the corresponding fix in commit 5c685c94
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2710](https://github.com/microsoft/TypeScript-go/pull/2710) (Closed)

**Watch mode: clean up output files when source files are deleted**

*Add functionality to tsc --watch to automatically remove compiled output files when their source files are deleted.*

 * created by **DukeDeSouth**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2710#issuecomment-3866215462) **DukeDeSouth** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2710#issuecomment-3880078020) **jakebailey** said "Thanks, but this kind of change is not in scope: https://github.com/microsoft/typescript-go/blob/main/CONTRIBUTING.md#scope-of-acceptable-changes"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2711](https://github.com/microsoft/TypeScript-go/pull/2711) (Closed)

**Optimize distributive conditional type instantiation for trivial extends types**

*Optimize distributive conditional type instantiation by directly applying branch results when the extends type is never, any, or unknown*

 * created by **DukeDeSouth**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2711#issuecomment-3866215482) **DukeDeSouth** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2711#issuecomment-3880079323) **jakebailey** said "Thanks, but this kind of change is not in scope: https://github.com/microsoft/typescript-go/blob/main/CONTRIBUTING.md#scope-of-acceptable-changes"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2720](https://github.com/microsoft/TypeScript-go/issues/2720) (Closed, `Crash`, **ahejlsberg**)

**panic handling request textDocument/hover**

*The TypeScript Go LSP server panics with a nil pointer dereference error when processing textDocument/hover requests.*

 * created by **christophe-g**
 * **christophe-g** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2720#issuecomment-3880801438) **DanielRosenwasser** said "Can you give us more details? Maybe a single file with what you need from form.js at the very least?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2720#issuecomment-3882775193) **christophe-g** provided a smaller reproduction example including TypeScript code and package.json
 * **ahejlsberg** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#2721](https://github.com/microsoft/TypeScript-go/issues/2721) (Open, `Type Ordering`)

**Variance resolution differs from tsc for recursive generic types \(@tanstack/react\-table\)**

*tsgo’s variance resolution for recursive generic types in @tanstack/react-table differs from tsc’s, producing order-dependent errors.*

 * created by **Faithfinder**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2721#issuecomment-3879838913) **jakebailey** said "Can you test with the 6.0 nightly, especially with --stableTypeOrdering?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2721#issuecomment-3879877541) **Faithfinder** said "Done :) (issue updated with results)"
 * **RyanCavanaugh** added label `Type Ordering`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2721#issuecomment-3879961666) **RyanCavanaugh** clarified that tsgo matches `tsc --stableTypeOrdering` and requires a variance annotation rather than being a bug
 * [today](https://github.com/microsoft/TypeScript-go/issues/2721#issuecomment-3880239746) **Faithfinder** explained that tsgo matches tsc with --stableTypeOrdering, noted a minimal repro difference, and stated tsgo's consistent behavior is preferable and reported it for awareness

### [PR microsoft/TypeScript-go#2722](https://github.com/microsoft/TypeScript-go/pull/2722) (Closed)

**Clarify scope of acceptable changes for TypeScript 7\.0**

*Defines guidelines for permissible changes and their scope during the transition to TypeScript 7.0.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2723](https://github.com/microsoft/TypeScript-go/pull/2723) (Closed)

**Fix race on snapshot in DidOpenFile**

*The DidOpenFile method lacks snapshotUpdateMu locking during UpdateSnapshot, leading to race conditions and intermittent segmentation faults in tests*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2724](https://github.com/microsoft/TypeScript-go/pull/2724) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript PR \#62201: Update Node\.js core modules**

*Sync TypeScript-Go's Node.js core module list with upstream by removing test/mock_loader, adding node:quic, and updating filtering comments.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2725](https://github.com/microsoft/TypeScript-go/pull/2725) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript PR \#62170: Enhance type argument completions**

*Improve TypeScript type argument completions by adding utility functions, refining completion logic, and updating tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2725#issuecomment-3881625912) **jakebailey** instructed Copilot to compare suggestions against the original code, refrain from changes that differ, accept doing nothing, and explain each decision
 * [today](https://github.com/microsoft/TypeScript-go/pull/2725#issuecomment-3881638085) **Copilot** verified each suggestion against the original implementation and found no changes were needed

### [PR microsoft/TypeScript-go#2726](https://github.com/microsoft/TypeScript-go/pull/2726) (Closed, **jakebailey**, **Copilot**)

**Port \#61683: Use getNonMissingTypeOfSymbol in compareProperties**

*Replace getTypeOfSymbol with getNonMissingTypeOfSymbol in compareProperties and update baselines after tests pass*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2726#issuecomment-3880950825) **jakebailey** said "@copilot You still need to run the tests and accept all baseline changes"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2726#issuecomment-3880992015) **Copilot** ran the full test suite and accepted all baseline changes, deleted an obsolete .diff file after output matched the reference baseline
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2727](https://github.com/microsoft/TypeScript-go/pull/2727) (Closed, **jakebailey**, **Copilot**)

**Port TS\#62611: add allowJs default value description**

*Port TS PR #62611 by updating the Go compiler’s allowJs option to use 'false, unless checkJs is set' default.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2727#issuecomment-3880971848) **jakebailey** said "@copilot you still have baselines out of date; rerun tests and accept"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2727#issuecomment-3881014910) **Copilot** accepted the two remaining baselines in commit bf59f3c5
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2728](https://github.com/microsoft/TypeScript-go/pull/2728) (Open, **jakebailey**, **Copilot**)

**Port TypeScript\#62676: Fix slow sync iteration types spoiling cached async iteration types**

*Prevents sync iteration type resolution from caching before async resolution, ensuring correct for-await loop typing.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2728#issuecomment-3881156531) **jakebailey** said "Hm, this does nothing. Maybe we avoid the problem entirely now?"

### [PR microsoft/TypeScript-go#2729](https://github.com/microsoft/TypeScript-go/pull/2729) (Closed, **jakebailey**, **Copilot**)

**Port \#62155: Report errors for private identifier fields in class expression declarations**

*Adds a check to report errors for ECMAScript private identifier fields in class expression declarations.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2730](https://github.com/microsoft/TypeScript-go/pull/2730) (Closed, **jakebailey**, **Copilot**)

**Port: Allow line break before import attributes \`with\` keyword**

*Allow import attributes with the “with” keyword after a line break by applying the hasPrecedingLineBreak guard only to assert keywords.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2731](https://github.com/microsoft/TypeScript-go/pull/2731) (Closed, **jakebailey**, **Copilot**)

**Port TS\#62659: Fix crash when parsing invalid decorator on await expression**

*Port TS#62659 by replacing an assert with a conditional in parseVariableDeclarationList to avoid parse crashes on invalid decorators before await expressions.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2732](https://github.com/microsoft/TypeScript-go/pull/2732) (Closed, **jakebailey**, **Copilot**)

**Port \#62483: Disable conditional exports fallbacks on null values**

*Port PR to make null conditional export entries terminate resolution rather than falling back to other conditions.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2733](https://github.com/microsoft/TypeScript-go/pull/2733) (Closed, **jakebailey**, **Copilot**)

**Port TS\#62656: Fix TS2783 false positive for union types in object spread**

*Adjust checkSpreadPropOverrides to also skip partial flags, preventing TS2783 false positives on union object spreads.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2734](https://github.com/microsoft/TypeScript-go/pull/2734) (Closed, **jakebailey**, **Copilot**)

**Use comparability for discriminant properties when narrowing types for a default switch clause**

*Use type comparability instead of strict equality to correctly narrow discriminated unions in switch default clauses*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2735](https://github.com/microsoft/TypeScript-go/pull/2735) (Closed, **jakebailey**, **Copilot**)

**Port TS\#57912: Allow implicit undefined returns when contextual union type contains undefined**

*Allow functions without explicit returns to implicitly return undefined when their union return type includes undefined.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2736](https://github.com/microsoft/TypeScript-go/pull/2736) (Closed, **jakebailey**, **Copilot**)

**Port TS\#56859: Keep returned/yielded literal types as const with const type variables**

*Ensure functions with const type parameters regularize returned and yielded literal types to prevent literal type leakage*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2737](https://github.com/microsoft/TypeScript-go/pull/2737) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript PR \#62661: fix \[Symbol\.iterator\]\(\) lost on union with never**

*Add reduced type handling in getIterationTypesOfIterable to restore Symbol.iterator support for unions containing never types*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2738](https://github.com/microsoft/TypeScript-go/pull/2738) (Closed, **jakebailey**, **Copilot**)

**Port TS\#61788: Fix control flow analysis of aliased discriminants with parenthesized initializers**

*Fix TypeScript control flow analysis to correctly narrow parenthesized aliased discriminants using a new initializer helper.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2739](https://github.com/microsoft/TypeScript-go/pull/2739) (Closed)

**Fix recursion proceeding to JSDoc node even if outside of range**

*Prevent recursion from traversing into JSDoc nodes that fall outside the specified range.*

 * created by **apendua**

### [PR microsoft/TypeScript-go#2740](https://github.com/microsoft/TypeScript-go/pull/2740) (Closed, **jakebailey**, **Copilot**)

**Port \#60304: More rigorous ASI prevention when emitting return/yield**

*Port TypeScript's enhanced automatic semicolon insertion prevention logic for return and yield expressions from PR #60304 into the Go printer.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2740#issuecomment-3881571005) **jakebailey** said "@copilot fix lints"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2740#issuecomment-3881603678) **Copilot** replaced the manual loop over synthetic leading comments with slices.ContainsFunc in commit 8c58585b to satisfy the modernize linter

### [PR microsoft/TypeScript-go#2741](https://github.com/microsoft/TypeScript-go/pull/2741) (Closed, **jakebailey**, **Copilot**)

**No\-op: PR \#62557 already ported**

*The Go port already includes the updated diagnostic message and program logic from TypeScript PR #62557, requiring no further changes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2742](https://github.com/microsoft/TypeScript-go/pull/2742) (Closed, **jakebailey**, **Copilot**)

**Disallow \`\[await\] using\` statements under case/default clauses**

*Prevent using and await using declarations from appearing directly under case/default clauses by enforcing grammar errors and removing transformer support.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2743](https://github.com/microsoft/TypeScript-go/pull/2743) (Closed, **jakebailey**, **Copilot**)

**No changes needed: PR \#58910 already ported**

*TypeScript PR #58910's return type inference constraint filtering is already implemented and tested in Go's inference.go, requiring no changes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2744](https://github.com/microsoft/TypeScript-go/pull/2744) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript \#62722: Widen reverse mapped type properties**

*Port TypeScript #62722 to wrap reverse-mapped type inference in getWidenedType, widening literal properties and preventing spurious excess property check errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2745](https://github.com/microsoft/TypeScript-go/pull/2745) (Closed, **jakebailey**, **Copilot**)

**Port TS\#62283: Clear SkipGenericFunctions in yield expression checking**

*Clear the SkipGenericFunctions flag when checking yield expressions in the Go port to fix incorrect silentNeverType inference in generators*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2745#issuecomment-3882459188) **jakebailey** said "I'll note that this also "ports" https://github.com/microsoft/TypeScript/pull/61317 in that https://github.com/microsoft/TypeScript/pull/62283 effectively reverted the former and used a different fix."

### [PR microsoft/TypeScript-go#2746](https://github.com/microsoft/TypeScript-go/pull/2746) (Open, **jakebailey**, **Copilot**)

**Port \#62361: Make go\-to\-definition resolve constraint properties for object literals in argument positions**

*Implement go-to-definition support for constraint properties in object literals used as arguments by porting PR #62361 and updating flags, code, and tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2746#issuecomment-3881563142) **jakebailey** said "@copilot No tests got updated, so I don't think this is complete. Maybe some tests are fixed that are in failingTests? Look for the original tests modified in the PR you ported."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2746#issuecomment-3881631951) **Copilot** fixed the retry logic to use the public GetContextualType API and updated test baselines accordingly

### [PR microsoft/TypeScript-go#2747](https://github.com/microsoft/TypeScript-go/pull/2747) (Closed, **jakebailey**, **Copilot**)

**Port TS\#56182: Include source node inferences in string literal completions deeper in arguments**

*Port TS#56182 to include source node inferences in nested string literal completions, add matching helpers, and unify sort priorities.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2747#issuecomment-3881548858) **jakebailey** said "@copilot You incorrectly modified a generated test, typeErrorAfterStringCompletionsInNestedCall_test, which indicates that something is wrong. Cross-reference your changes against the original PR."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2747#issuecomment-3881600799) **Copilot** reverted the generated test and adjusted sort priorities so inference types sort before contextual types

### [PR microsoft/TypeScript-go#2748](https://github.com/microsoft/TypeScript-go/pull/2748) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript PR \#62243: Improve inference by not considering thisless functions context\-sensitive**

*Port TypeScript PR 62243 to improve type inference by not treating functions without this as context-sensitive*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2748#issuecomment-3881615612) **Copilot** described fix commit fe78f7ba restoring PropertyDeclaration in GetContainerFlags and clearing CheckModeSkipGenericFunctions for yield expression operands, deleting ~1000 lines without introducing new diffs
 * [today](https://github.com/microsoft/TypeScript-go/pull/2748#issuecomment-3882454308) **DanielRosenwasser** said "https://github.com/microsoft/typescript/issues/62243"

### [PR microsoft/TypeScript-go#2749](https://github.com/microsoft/TypeScript-go/pull/2749) (Closed, **jakebailey**, **Copilot**)

**Port \#62275: Discard types that reduce to never before discriminating by discriminable items**

*Port a TypeScript change to filter out types that reduce to never before discriminant-based narrowing to ensure proper contextual typing.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2750](https://github.com/microsoft/TypeScript-go/pull/2750) (Closed, **jakebailey**, **Copilot**)

**Port TS\#60528: Fix index type deferral crash on generic mapped types with name types**

*Backports a fix for crashes in index type computation of generic mapped types with `as` name types by refining deferral and base constraint logic.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2751](https://github.com/microsoft/TypeScript-go/pull/2751) (Open, **jakebailey**, **Copilot**)

**Port TS\#63043: Implement walkBindingPattern for declaration emit of destructured parameter properties**

*Implement walkBindingPattern to emit property declarations for destructured parameter properties in declaration files.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2752](https://github.com/microsoft/TypeScript-go/pull/2752) (Closed, **jakebailey**, **Copilot**)

**Port \#63038: Consult referenced project options for synthetic default export eligibility**

*Consult referenced project’s module format in canHaveSyntheticDefault to correctly disallow synthetic default imports for ESM declaration files.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2752#issuecomment-3882413799) **DanielRosenwasser** said "https://github.com/microsoft/typescript/issues/63038"

### [PR microsoft/TypeScript-go#2753](https://github.com/microsoft/TypeScript-go/pull/2753) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript\#63070: Be more lenient about iteration when lib=es5 / noLib**

*Allow for..of iteration under es5/noLib when no global Iterable exists by falling back to array and string iteration.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2754](https://github.com/microsoft/TypeScript-go/pull/2754) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript \#63026: Fix crash from circularly\-reentrant getEffectsSignature**

*Add flow containers and this-keyword propagation for function-like types in Go binder to prevent infinite getEffectsSignature recursion.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2754#issuecomment-3881579132) **jakebailey** said "Nothing seems to change, confusingly"

### [PR microsoft/TypeScript-go#2755](https://github.com/microsoft/TypeScript-go/pull/2755) (Closed)

**Fix multiple issues related to extreme symbol merging**

*Merging thousands of test scripts into one program causes nonsensical symbol overload consolidation, assertion panics, and out-of-bounds errors.*

 * created by **ahejlsberg**

### [PR microsoft/TypeScript-go#2756](https://github.com/microsoft/TypeScript-go/pull/2756) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript PR \#61955: Revert \#54442, report error for empty call candidates**

*Revert unknownSignature workaround in resolveCall to properly report missing signatures errors for empty call candidates, preserving JSX fragment behavior*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2757](https://github.com/microsoft/TypeScript-go/pull/2757) (Open, **jakebailey**, **Copilot**)

**Port TypeScript PR \#62320: Allow \-\-module commonjs \-\-moduleResolution bundler**

*Port PR #62320 to permit bundler module resolution with CommonJS by adjusting compiler checks in program.go and updating error and output baselines.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2758](https://github.com/microsoft/TypeScript-go/pull/2758) (Closed, **jakebailey**, **Copilot**)

**Port \#62311: Fix parenthesizer rules for binary expressions mixing ?? with \|\|/&&**

*Port PR #62311 to ensure binary expressions mixing ?? with ||/&& are parenthesized by adding helper and updating emit logic.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2759](https://github.com/microsoft/TypeScript-go/pull/2759) (Open, **jakebailey**, **Copilot**)

**Error on esModuleInterop=false and allowSyntheticDefaultImports=false \(removed in TS7\)**

*Marking esModuleInterop and allowSyntheticDefaultImports as removed when false in TS7 by defaulting them to true and emitting errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2760](https://github.com/microsoft/TypeScript-go/pull/2760) (Open, **jakebailey**, **Copilot**)

**Error on modules\-as\-namespaces**

*Emit parse errors for 'module' namespace declarations, remove obsolete utilities and tests, and update baselines to match TypeScript.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3882779331) **jakebailey** said "@copilot the intent is that module is illegal and produces a parse error"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3882864264) **Copilot** updated the parser to emit TS1540 parse errors on each identifier for illegal module namespace declarations and aligned baselines by deleting diff files

### [Issue microsoft/TypeScript-go#787](https://github.com/microsoft/TypeScript-go/issues/787) (Closed)

**\`UnionToTuple\` type returns "inverted" tuple in TSGO compared to TypeScript 5\.8\.3 and gives type error**

*TSGO's UnionToTuple type generates tuples in reverse order compared to TypeScript 5.8.3, causing type errors*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3867504473) **jakebailey** said "Yes, correct."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3867505544) **jakebailey** said "In the 6.0 nightly, you can now also pass --stableTypeOrdering to try this sorting out early."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3872828964) **alexwork1611** thanked for the information about the --stableTypeOrdering flag
 * [today](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3879428487) **RyanCavanaugh** clarified that UnionToTuple<'a'|'b'> currently yields consistent results but this behavior is unspecified and may change

