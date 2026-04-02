# Report for 2026-03-11 (Wednesday, March 11th, 2026)

21 different users commented on 28 different issues.

## Recommended Actions

 * Response Recommended
    * @yandodov suggested adding a cleaner satisfies feature to TypeScript in [microsoft/TypeScript#52222](https://github.com/microsoft/TypeScript/issues/52222#issuecomment-4046222921)
    * @jonathantneal asked if they could help move this along in [microsoft/TypeScript#63036](https://github.com/microsoft/TypeScript/pull/63036#issuecomment-4045738525)
    * @murataslan1 requested a review on a PR that sorts JSDoc @param completions by argument position in [microsoft/TypeScript#63079](https://github.com/microsoft/TypeScript/pull/63079#issuecomment-4040782543)
    * @juanjh1 provided repro steps as requested in [microsoft/TypeScript#63230](https://github.com/microsoft/TypeScript/issues/63230#issuecomment-4040793418)
    * @iluha168 suggested splitting PromiseLike.then into two overloads to preserve return type specificity in [microsoft/TypeScript#63244](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4047353571)

## Activity Summary

### [Issue microsoft/TypeScript#3841](https://github.com/microsoft/TypeScript/issues/3841) (Open, `Suggestion`, `In Discussion`)

**T\.constructor should be of type T**

*Suggest typing instance.constructor as the class type rather than Function to enable direct static property access without casting.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3613012288) **ExE-Boss** corrected the type of C.constructor by explaining it’s globalThis.Function and provided a correct TypeScript definition
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3831017529) **OldStarchy** explained that constructor signatures and call signatures cannot be inherited, suggested using static factory methods as a workaround, and demonstrated typing constructors by picking static members via Pick
 * [yesterday](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-4033575172) **ljharb** argued that static members were equally difficult to reason about because subclasses could avoid inheriting or shadow them
 * [today](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-4042966761) **OldStarchy** described TypeScript's lack of support for static members in interfaces and demonstrated a generic workaround using a custom constructor interface

### [Issue microsoft/TypeScript#43368](https://github.com/microsoft/TypeScript/issues/43368) (Open, `Suggestion`, `Awaiting More Feedback`)

**Suggestion: Allow getters to have predicate return types**

*Enable TypeScript class getters to have user-defined type predicate return types for type guards.*

 * [47 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-2797184331) **marijnh** mentioned running into situations where he needed to convert getters to methods to use them as type predicates despite conflicting with system conventions
 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-2993092726) **chespina** expressed frustration with the suggestion to use a method, noted it changed semantics and could introduce breaking changes, mentioned the issue dates back to 2016 and argued that a fundamental language feature is missing and should have higher priority
 * [27 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-3243558010) **qolity** described encountering incorrect type inference with a property-based isRight approach and explaining why the type predicate method, though accurate, is prone to accidental misuse
 * [later](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-4046270378) **alex-at-happening** said "That would be awesome to have it in TS"

### [Issue microsoft/TypeScript#52222](https://github.com/microsoft/TypeScript/issues/52222) (Open, `Suggestion`, `Awaiting More Feedback`)

**Support \`satisfies\` in type declaration**

*Add support for using the TypeScript `satisfies` operator in type alias declarations.*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/52222#issuecomment-2112167935) **mattidupre** added that this would help shimming utility types whose generics are not strict enough and demonstrated with TypeScript examples
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/52222#issuecomment-2632452441) **gggdomi** described using the 'satisfies' one-liner for value type assertions and expressed annoyance at not being able to apply it to types without ESLint errors
 * [35 weeks ago](https://github.com/microsoft/TypeScript/issues/52222#issuecomment-3053526286) **bwateratmsft** mentioned intention to use this in the Container Tools extension for VSCode and to assert a Disposable interface’s compatibility with both `@types/vscode` and `vscode-jsonrpc`
 * [later](https://github.com/microsoft/TypeScript/issues/52222#issuecomment-4046222921) **yandodov** demonstrated a hack to satisfy ESLint by using `void 0 as unknown as Satisfy<..., ...>` and suggested a built-in `satisfies` feature
 * [later](https://github.com/microsoft/TypeScript/issues/52222#issuecomment-4046297699) **yandodov** suggested support for type annotations in type definitions analogous to runtime variable annotations

### [Issue microsoft/TypeScript#61165](https://github.com/microsoft/TypeScript/issues/61165) (Open, `Bug`, `Help Wanted`, `Domain: JavaScript`)

**Object\.defineProperty\(variable\) does not error in \`\.js\` files if \`variable\` does not exist**

*TypeScript does not report missing variable errors for Object.defineProperty calls in JavaScript files.*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/61165#issuecomment-2683146141) **Andarist** said "@sandersn do u have an opinion on how this should work and how file.jsGlobalAugmentations should be utilized (should they perhaps depend on checkJs or something)?"
 * [47 weeks ago](https://github.com/microsoft/TypeScript/issues/61165#issuecomment-2803209841) **sandersn** noted that TS7 removed implicit namespace creation in JS, expressed uncertainty about Object.defineProperty special handling, and asserted that foo should error in the original example
 * **RyanCavanaugh** added label `Domain: JavaScript`
 * [later](https://github.com/microsoft/TypeScript/issues/61165#issuecomment-4044483018) **DetachHead** asked why x.prop implicitly created the parent x and asked if there was an option to disable that behavior

### [PR microsoft/TypeScript#63036](https://github.com/microsoft/TypeScript/pull/63036) (Open, `For Uncommitted Bug`)

**Add support for import attributes in ambient module declarations**

*Enable import attributes in ambient module declarations to ensure correct parsing, module resolution, type checking, and diagnostics.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/63036#issuecomment-3782583826) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/63036#issuecomment-3782584168) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/63036#issuecomment-3782592823) **jonathantneal** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/63036#issuecomment-4045738525) **jonathantneal** said "Anything I can do here to help this move along?"
 * [later](https://github.com/microsoft/TypeScript/pull/63036#issuecomment-4047519208) **jakebailey** said "The TS 6.0 RC is cut, so we are basically frozen until TS 7.0 or even TS 7.1 as the port proceeds. So I would not expect this (or effectively any other non-bugfix PRs) to be merged."

### [PR microsoft/TypeScript#63079](https://github.com/microsoft/TypeScript/pull/63079) (Open, `For Backlog Bug`)

**Sort JSDoc @param completions by argument position**

*Sort JSDoc @param completions by function parameter order instead of alphabetical order.*

 * created by **murataslan1**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63079#issuecomment-4040782543) **murataslan1** requested a review for a change that sorted JSDoc @param completions by argument position

### [Issue microsoft/TypeScript#63197](https://github.com/microsoft/TypeScript/issues/63197) (Closed, `Bug`, `Fixed`)

**Fatal OOM crash on recursive template literal type**

*A recursive template literal type definition causes a fatal out-of-memory crash in TypeScript versions 5.9.3 and 6.0.0-beta.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-3975896004) **james-pre** provided environment details, a CI reproduction link, an example type causing the crash, and the tsconfig configuration
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-3984559138) **mkantor** provided a minimized reproduction case demonstrating the crash
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-4010047218) **caomingpei** described that the issue related to typescript-go#2125 shared a root cause of unbounded recursive type expansion and suggested considering default compiler behavior in a future ts-go migration
 * [today](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-4040827985) **RyanCavanaugh** reported that nightly tsgo immediately issued an appropriate error
 * (today) **RyanCavanaugh** added labels `Bug`, `Fixed`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63207](https://github.com/microsoft/TypeScript/issues/63207) (Open, `Bug`, `Domain: check: Type Circularity`)

**tsserver hangs indefinitely when inferring return type of class method that passes this to a function with deeply nested conditional return type**

*tsserver hangs when inferring a class method’s return type using remeda.pick without an explicit annotation due to circular type inference*

 * created by **kkirby**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63207#issuecomment-3994012407) **RyanCavanaugh** explained that the hang was caused by an undetected type-checking cycle, linked to a relevant FAQ, and suggested annotating return types or using type assertions to unblock work
 * [today](https://github.com/microsoft/TypeScript/issues/63207#issuecomment-4040931836) **RyanCavanaugh** noted that tsgo finished in finite time, suggested tsc would finish in another 30 seconds, and listed TypeScript compilation errors and metrics
 * [today](https://github.com/microsoft/TypeScript/issues/63207#issuecomment-4040938729) **RyanCavanaugh** said "The emitted a.d.ts is 48 megabytes 🫨"

### [Issue microsoft/TypeScript#63216](https://github.com/microsoft/TypeScript/issues/63216) (Closed, `Duplicate`)

**\`keyof\` behaves differently with index signatures created using \`Record\`**

*The keyof operator returns string|number for an explicit {[x: string]: unknown} index signature but only string for Record<string, unknown> despite both supporting numeric indexing.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016764287) **MartinJohns** clarified that issue #45447 was not the same, explained that keyof {[x: string]: any} and keyof Record<string, any> return different results, and noted confusion due to a display issue
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4017187645) **jcalz** said "Duplicate #31013"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4025537931) **RyanCavanaugh** provided an automatically generated analysis and list of similar issues
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#63218](https://github.com/microsoft/TypeScript/issues/63218) (Open, `Suggestion`, `Awaiting More Feedback`)

**Error \(2320\) when extending interfaces where a property is both readonly and readwrite\.**

*Extending two interfaces that declare the same property as readonly and writable erroneously triggers a conflict error*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63218#issuecomment-4017183362) **denis-migdal** provided two code examples illustrating missing TypeScript errors for getter/setter implementations
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63218#issuecomment-4025537993) **RyanCavanaugh** provided an automated analysis listing similar issues
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63218#issuecomment-4025817238) **denis-migdal** compared proposed bugs against existing issues and found no clear duplicates while highlighting confusion around readonly behavior
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#63223](https://github.com/microsoft/TypeScript/issues/63223) (Open, `Bug`, `Domain: flag: isolatedDeclarations`)

**Toggling \`isolatedModules\` in \`tsconfig\.json\` while running the compiler in \`watch\` mode, doesn't re\-emit \`const enums\`, unlike toggling \`preserveConstEnums\`, which does**

*Unlike preserveConstEnums toggles, changing isolatedModules in watch mode does not re-emit const enums until a full rebuild.*

 * created by **rotemdan**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63223#issuecomment-4025538117) **RyanCavanaugh** provided an automated list of similar issues
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63225](https://github.com/microsoft/TypeScript/issues/63225) (Open, `Needs Investigation`)

**\`Omit\` causes function to lose contextual typing**

*Omitting keys from AssertableState<T> in TypeScript 6.0 causes function parameters to lose contextual typing and default to any.*

 * created by **dragomirtitian**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63225#issuecomment-4029620365) **Andarist** said "Bisects to https://github.com/microsoft/TypeScript/pull/60528 . I'll investigate it"
 * **RyanCavanaugh** added label `Needs Investigation`

### [Issue microsoft/TypeScript#63227](https://github.com/microsoft/TypeScript/issues/63227) (Open, `Needs Investigation`, **ahejlsberg**)

**Inference from result of generic function no longer produces a union**

*TypeScript 6 regression: deepEqual’s generic inference from compact fails to produce a union of optional and required properties.*

 * created by **dragomirtitian**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63227#issuecomment-4032636619) **Andarist** said "bisects to https://github.com/microsoft/TypeScript/pull/62502"
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#63228](https://github.com/microsoft/TypeScript/issues/63228) (Closed, `Needs Investigation`, **jakebailey**)

**TypeScript 6 API Bug \- \`isSourceFileDefaultLibrary\` false negative on program structure reuse**

*In TypeScript 6.0.0-beta, isSourceFileDefaultLibrary incorrectly returns false for default library files when reusing program structure.*

 * created by **StyleShit**
 * [today](https://github.com/microsoft/TypeScript/issues/63228#issuecomment-4040885719) **RyanCavanaugh** said "Huh, this is very weird. It seems like it'd have some obvious effects under watch mode."
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/issues/63228#issuecomment-4041547524) **jakebailey** said "@StyleShit I think https://github.com/microsoft/TypeScript/pull/63239#issuecomment-4041195460 should fix it."
 * [later](https://github.com/microsoft/TypeScript/issues/63228#issuecomment-4044993165) **StyleShit** said "@jakebailey works for me in the ts-eslint PR 👍 "
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63230](https://github.com/microsoft/TypeScript/issues/63230) (Open, `Bug`, `Domain: Crashes`)

**Compiler crash: Debug Failure in visitEachChildOfIndexSignatureDeclaration**

*TypeScript compiler crashes with a Debug Failure in visitEachChildOfIndexSignatureDeclaration when addInitializer uses an invalid index signature annotation*

 * created by **juanjh1**
 * [today](https://github.com/microsoft/TypeScript/issues/63230#issuecomment-4040587604) **RyanCavanaugh** provided a minimal reproduction and noted it didn't occur on TS7
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63230#issuecomment-4040769522) **Andarist** explained that Corsa did not crash because it did not assert on missing .type and allowed nil to propagate while Strada expected .type
 * [today](https://github.com/microsoft/TypeScript/issues/63230#issuecomment-4040793418) **juanjh1** provided a minimal repro snippet with TypeScript code and a screenshot

### [Issue microsoft/TypeScript#63231](https://github.com/microsoft/TypeScript/issues/63231) (Open, `Needs More Info`)

**exports subpath with array types is not autocompleting**

*VS Code’s JavaScript/TypeScript language server does not autocomplete import paths for subpaths when exports.types is defined as an array*

 * created by **unional**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/63231#issuecomment-4040628071) **RyanCavanaugh** said "@unional can you check this in TS 7 (native preview) and tell me if it still repros?"
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63231#issuecomment-4041227902) **unional** said "Hi @RyanCavanaugh, sure will give that a try when I get a chance to. "

### [Issue microsoft/TypeScript#63232](https://github.com/microsoft/TypeScript/issues/63232) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**exactOptionalPropertyTypes shows a warning when strict is undefined in TypeScript 6\.0**

*exactOptionalPropertyTypes emits a warning requiring strictNullChecks when strict is undefined in tsconfig, despite TypeScript 6.0 defaulting strict mode.*

 * created by **nishiikata**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/issues/63232#issuecomment-4040761236) **RyanCavanaugh** said "This is fixed in nightly"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63236](https://github.com/microsoft/TypeScript/issues/63236) (Closed)

**دمج**

*Request to merge the changes from commit fc13b0193ddb5857c2b805f13023ef893552b05c into the repository*

 * created by **asd585140-glitch**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63238](https://github.com/microsoft/TypeScript/pull/63238) (Closed, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix warning for exactOptionalPropertyTypes with undefined strict flag**

*Use effective strictPropertyInitialization value in verifyCompilerOptions to fix exactOptionalPropertyTypes warning when strict flag is unspecified*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63239](https://github.com/microsoft/TypeScript/pull/63239) (Closed)

**Fix missing lib files in reused programs**

*Reintroduce omitted library files in reused programs and cherry-pick the fix to the 6.0 branch.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63239#issuecomment-4041169166) **jakebailey** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/63239#issuecomment-4041169687) **typescript-bot** reported build job status and provided links to started and completed results
 * [today](https://github.com/microsoft/TypeScript/pull/63239#issuecomment-4041195460) **typescript-bot** provided installation instructions and testing links for the PR build
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63240](https://github.com/microsoft/TypeScript/issues/63240) (Open, `Bug`, `Domain: flag: exactOptionalPropertyTypes`)

**Error from \`exactOptionalPropertyTypes\` not reported when using object spread with a ternary and optional property acces**

*TypeScript's exactOptionalPropertyTypes fails to report an error when combining object spread, a ternary expression, and optional property access.*

 * created by **aswinsvijay**

### [Issue microsoft/TypeScript#63241](https://github.com/microsoft/TypeScript/issues/63241) (Closed)

**دمج**

*Request to merge the awesomeWM 4.3 release tag into the main codebase.*

 * created by **asd585140-glitch**

### [Issue microsoft/TypeScript#63242](https://github.com/microsoft/TypeScript/issues/63242) (Closed)

**04bea1e3cdab4cad52569b7995071a08ec267b12ضبط**

*A GitHub issue linking commit 1429c7e80cb9b2b00c426387db1ec24f7fb50e8e in TooTallNate/proxy-agents related to ضبط*

 * created by **asd585140-glitch**

### [Issue microsoft/TypeScript#63243](https://github.com/microsoft/TypeScript/issues/63243) (Closed, `Duplicate`)

**PromiseRejectedResut reason should be \`unknown\`**

*Require the PromiseRejectedResult.reason type in the es2020 promise library to be unknown instead of any*

 * created by **karlismelderis-mckinsey**
 * [later](https://github.com/microsoft/TypeScript/issues/63243#issuecomment-4045154423) **MartinJohns** said "Essentials a duplicate of #45602."

### [Issue microsoft/TypeScript#63244](https://github.com/microsoft/TypeScript/issues/63244) (Open, `Needs Proposal`)

**bug\(lib\): Explicitly stating wrong return type of \`Promise\.then\` without arguments results in no error**

*Current TypeScript versions fail to report a type mismatch when Promise<string> is assigned from Promise.resolve(1).then() with no arguments.*

 * created by **iluha168**
 * [later](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4046207682) **jcalz** suggested retyping Promise.then using the NoInfer utility type to improve typing
 * [later](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4047353571) **iluha168** suggested splitting the PromiseLike.then and Promise.then definitions into two overloads to avoid the NoInfer breaking change and maintain return type hints

### [Issue microsoft/TypeScript#63245](https://github.com/microsoft/TypeScript/issues/63245) (Open, `Discussion`)

**Bloomberg feedback for 6\.0**

*Bloomberg reports moderate impact from TypeScript 6.0 RC, citing deprecated node module resolution, type checking regressions, JS emit changes, and removed hasDefaultLib API.*

 * created by **dragomirtitian**
 * [later](https://github.com/microsoft/TypeScript/issues/63245#issuecomment-4045864995) **MartinJohns** expressed amazement that all projects used the node moduleResolution despite fewer than 1% of packages being affected
 * [later](https://github.com/microsoft/TypeScript/issues/63245#issuecomment-4046613300) **dragomirtitian** clarified that 100% of projects used node resolution but fewer than 1% experienced issues when moved to bundler

