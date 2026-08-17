# Report for 2026-08-14 (Friday, August 14th, 2026)

8 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @irfanstract asked why const enum is allowed in [microsoft/TypeScript#31670](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5299225184)
    * @tejash5489-lang suggested relabeling or splitting the issue to avoid duplication in [microsoft/TypeScript#37782](https://github.com/microsoft/TypeScript/issues/37782#issuecomment-5301387045)
    * @patrickswedish asked whether to reopen/retarget #63729 or create a fresh rebased PR in [microsoft/TypeScript#63728](https://github.com/microsoft/TypeScript/issues/63728#issuecomment-5301776601)

## Activity Summary

### [Issue microsoft/TypeScript#31670](https://github.com/microsoft/TypeScript/issues/31670) (Closed, `Discussion`)

**The future of the "private" keyword**

*Discussion of TypeScript’s plan to retain its existing private keyword while supporting new JavaScript private fields (#fields) and associated rules.*

 * [42 weeks ago](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-3436325273) **ArrayIterator** mentioned that the private visibility modifier could be dangerous as it might be exposed when objects are stringified
 * [21 weeks ago](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-4088397826) **Finesse** asked about using a TypeScript flag to prepend '#' to private fields for minification benefits and inquired why const enum emit is allowed
 * [21 weeks ago](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-4090013416) **snarbles2** explained that transpiling private to # is not simple due to semantic differences, backward-compatibility concerns, and potential confusion, and clarified that const enums are permitted because they are grandfathered from before TypeScript's type-directed emit stance
 * [today](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5299225184) **irfanstract** warned that the private visibility modifier can be dangerous and suggested migrating to ES Private Fields; asked why const enum is allowed, speculating that some transpilers might drop const

### [Issue microsoft/TypeScript#37782](https://github.com/microsoft/TypeScript/issues/37782) (Open, `Suggestion`, `Help Wanted`, `Good First Issue`)

**'declare method' quick fix for adding a private method**

*Request a quick fix feature to declare missing private methods in classes, similar to the existing private property quick fix.*

 * [50 weeks ago](https://github.com/microsoft/TypeScript/issues/37782#issuecomment-3233122916) **kamolovd** said "This is my first investment in outsourcing, can I start with this? @mjbvz "
 * [44 weeks ago](https://github.com/microsoft/TypeScript/issues/37782#issuecomment-3375208607) **tysoncung** suggested checking the error logs and asked for environment details to help investigate the issue
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/37782#issuecomment-3707833723) **oppong07** announced plans to implement the "declare method" quick fix, add tests, open a PR, and asked whether maintainers prefer submission to microsoft/typescript-go
 * [later](https://github.com/microsoft/TypeScript/issues/37782#issuecomment-5301387045) **tejash5489-lang** noted that the originally reported case was already resolved by a merged PR, described the remaining follow-up tracked in another issue, and suggested relabeling or splitting the issue

### [Issue microsoft/TypeScript#47595](https://github.com/microsoft/TypeScript/issues/47595) (Closed, `Suggestion`, `Help Wanted`, `Experience Enhancement`)

**Inability to use typeof on an ES private property**

*TypeScript prevents using typeof on ES private class properties even within their defining class.*

 * (4.2 years ago) **jakebailey** reopened the issue
 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/47595#issuecomment-1118033008) **jakebailey** said "I've now reverted #47696 in #48959, reopening this issue."
 * [33 weeks ago](https://github.com/microsoft/TypeScript/issues/47595#issuecomment-3674421455) **grundb** pointed out that the suggested support for typeof this.#p wouldn't allow using typeof on static private elements in non-static methods
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#61706](https://github.com/microsoft/TypeScript/issues/61706) (Open, `Suggestion`, `Awaiting More Feedback`)

**\`Object\.groupBy\` should not return \`Partial\<Record\<string, T\>\>\` or \`Partial\<Record\<number, T\>\>\`**

*Object.groupBy's type definitions unnecessarily return Partial<Record<string|number, T>> for unrestricted keys, causing false undefined errors.*

 * [42 weeks ago](https://github.com/microsoft/TypeScript/issues/61706#issuecomment-3431185657) **TiAlRo** proposed adjusting groupBy’s return type to Record<K, T[]> and modifying Record for union-literal keys to permit omitted keys at runtime with T | undefined while preserving autocompletion and existing string-key behavior
 * [42 weeks ago](https://github.com/microsoft/TypeScript/issues/61706#issuecomment-3432033532) **TiAlRo** said "Additionally, the type Partial> should be assignable to the type Record because there is no difference."
 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/61706#issuecomment-3962612851) **DominoPivot** corrected the example by noting Object.groupBy returns a null-prototype object, explained TypeScript optional index signature issue, and suggested using Map.groupBy
 * [today](https://github.com/microsoft/TypeScript/issues/61706#issuecomment-5297545787) **erictheswift** described how optionality leaks into enumeration with Object.groupBy and Object.values causing spurious undefined errors, and proposed a conditional GroupByResult type to distinguish bounded key unions from wide index-signature keys to preserve correct optionality
 * [today](https://github.com/microsoft/TypeScript/issues/61706#issuecomment-5297554213) **erictheswift** said "Map.groupBy is a good workaround. I guess even superior one so we may consider current api as an implicit nudge towards it ;) "

### [Issue microsoft/TypeScript#63173](https://github.com/microsoft/TypeScript/issues/63173) (Closed, `Bug`, `Help Wanted`, `Domain: Crashes`)

**Crash: Maximum call stack size exceeded when declare const enum has a computed property named \[object\] followed by an object member**

*The compiler overflows the call stack when a const enum has a computed [object] member followed by an object member.*

 * (24 weeks ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Crashes`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63661](https://github.com/microsoft/TypeScript/issues/63661) (Closed, `Bug`, `Domain: Parser`)

**\`as\`/\`satisfies\` between exponentiation operators cannot be safely erased**

*Removing 'as' or 'satisfies' assertions between exponentiation operators in TypeScript changes operator grouping without errors.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Bug`, `Domain: Parser`, and set milestone to `Backlog`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63696](https://github.com/microsoft/TypeScript/issues/63696) (Closed, `Bug`, `Help Wanted`, `Domain: ES Modules`)

**False positive on destructured \`require\` is \`verbatimModuleSyntax\` and \`module\` is \`preserve\`**

*TypeScript incorrectly rejects destructured CommonJS require calls when verbatimModuleSyntax is enabled and module is preserve.*

 * **RyanCavanaugh** added label `Help Wanted`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63696#issuecomment-5134707373) **Samyra312007** said "Thanks for sharing."
 * **RyanCavanaugh** added label `Domain: ES Modules`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63728](https://github.com/microsoft/TypeScript/issues/63728) (Open, `Bug`, `Help Wanted`, `Domain: tslib and Helper Functions`)

**\`importHelpers\` incorrectly requires \`tslib\` for native \`\#private\` class members at every dated \`target\` \(ES2022–ES2025\), even though no helper is ever emitted**

*TypeScript’s importHelpers option wrongly requires tslib for native private class fields when targeting ES2022–ES2025 despite no helper emission*

 * (3 days ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: tslib and Helper Functions`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/63728#issuecomment-5301776601) **patrickswedish** noticed the issue remained marked Help Wanted after #63729 was closed, reviewed the issue and prepared a rebased version with updated compiler baselines and validation, and asked whether to reopen/retarget #63729 against main or submit a fresh rebased PR

### [PR microsoft/TypeScript#63738](https://github.com/microsoft/TypeScript/pull/63738) (Closed, `For Uncommitted Bug`)

**lib: document remaining ProxyHandler trap parameters**

*Document missing ProxyHandler trap parameters and rename setPrototypeOf’s v parameter to newPrototype to align JSDoc with code*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63738#issuecomment-5237173780) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63738#issuecomment-5237173801) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63738#issuecomment-5296055304) **RyanCavanaugh** said "This seems like make-work PR activity; no one is confused about whether argArray is the arguments array."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63749](https://github.com/microsoft/TypeScript/issues/63749) (Open, `Bug`)

**\[7\.0\] Can't access field if it is protected in one constituent of an intersection \(type order dependent\)**

*TypeScript 7 erroneously prevents accessing a property protected in one part of an intersection type when constituent order differs.*

 * created by **dragomirtitian**
 * [today](https://github.com/microsoft/TypeScript/issues/63749#issuecomment-5292998642) **nmain** said "This repros in 6.0 if stableTypeOrdering is used."
 * [today](https://github.com/microsoft/TypeScript/issues/63749#issuecomment-5295663639) **RyanCavanaugh** clarified that intersections are order-dependent and proposed allowing access if any constituent is public
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63750](https://github.com/microsoft/TypeScript/issues/63750) (Open, `Bug`, `Fix Available`)

**tsgo: parser nil\-pointer panic when a JSDoc @overload tags an anonymous default\-export function**

*tsgo’s parser crashes with a nil-pointer panic when a JSDoc @overload tags an anonymous default-export function*

 * created by **johnsoncodehk**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`

### [PR microsoft/TypeScript#63751](https://github.com/microsoft/TypeScript/pull/63751) (Closed, `For Backlog Bug`)

**fix: remove false tslib requirement for native \#private fields at ES2022\+**

*Removes unnecessary tslib dependency for native #private fields in ES2022+ in favor of the Go-based fix.*

 * [today](https://github.com/microsoft/TypeScript/pull/63751#issuecomment-5295063528) **ErfanBagheri404** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63751#issuecomment-5295079421) **RyanCavanaugh** informed that the TypeScript repo was closed for development and directed the PR to the typescript-go repo referencing CONTRIBUTING.md and issue #62963
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63751#issuecomment-5295656014) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#63752](https://github.com/microsoft/TypeScript/issues/63752) (Closed)

**extraFileExtensions cannot declare an extension as TypeScript, so TS\-flavoured files are charged to maxProgramSizeForNonTsFiles**

*extraFileExtensions files are not recognized as TypeScript and thus are measured against maxProgramSizeForNonTsFiles, disabling them when large*

 * created by **wagenet**
 * [today](https://github.com/microsoft/TypeScript/issues/63752#issuecomment-5299504677) **wagenet** explained a workaround shipping in the Ember parser that lies to ts.sys.getFileSize by reporting .gts files as zero bytes and stated a preference for extraFileExtensions
 * [today](https://github.com/microsoft/TypeScript/issues/63752#issuecomment-5300461978) **MartinJohns** noted that the suggested fix applied to nonexistent files and cautioned against trusting the AI given that TypeScript 5.7 is almost two years old

