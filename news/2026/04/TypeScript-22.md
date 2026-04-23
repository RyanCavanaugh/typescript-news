# Report for 2026-04-22 (Wednesday, April 22nd, 2026)

13 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @Misha327 asked for a workaround to prevent imports from being reordered on save when organizeImports is enabled in [microsoft/TypeScript#57157](https://github.com/microsoft/TypeScript/issues/57157#issuecomment-4304321407)
    * @3ru offered to help split out smaller follow-up PRs in [microsoft/TypeScript#58084](https://github.com/microsoft/TypeScript/pull/58084#issuecomment-4302383505)
    * @ilyash-b asked whether to update the handbook or close the issue in [microsoft/TypeScript#63421](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4303181436)

## Activity Summary

### [Issue microsoft/TypeScript#57157](https://github.com/microsoft/TypeScript/issues/57157) (Closed, `Needs More Info`)

**Allow indentation option for organizeImports**

*Provide an indent configuration option for TypeScript’s organizeImports feature to control import formatting indentation.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/57157#issuecomment-1910575998) **RyanCavanaugh** said "I can't repro the described behavior of two tabs - can you clarify?"
 * **RyanCavanaugh** added label `Needs More Info`
 * (1.7 years ago) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/57157#issuecomment-4304321407) **Misha327** described that when organizeImports was enabled on save the issue occurred and that he could not find a workaround

### [PR microsoft/TypeScript#58084](https://github.com/microsoft/TypeScript/pull/58084) (Closed, `For Uncommitted Bug`, **sandersn**)

**intl\.d\.ts: cleanup, add missing features, fix library discrepancies**

*Clean up and align TypeScript’s intl.d.ts with the ECMA-402 spec, fixing inconsistencies, adding missing features, and unifying type names.*

 * [1.7 years ago](https://github.com/microsoft/TypeScript/pull/58084#issuecomment-2225504323) **Renegade334** explained that the change was intentional to maintain consistency and suggested using `as const`, a `satisfies` clause, or explicit typing
 * (1 month ago) **typescript-bot** closed the issue
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/58084#issuecomment-4121434443) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates
 * [later](https://github.com/microsoft/TypeScript/pull/58084#issuecomment-4302383505) **3ru** offered to help split out smaller follow-up PRs and upstream remaining Intl API work
 * [later](https://github.com/microsoft/TypeScript/pull/58084#issuecomment-4302428124) **Renegade334** said "All yours. 🫡"

### [Issue microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **andrewbranch**, **Copilot**)

**Deprecate, remove support for \`baseUrl\`**

*TypeScript 6.0 will deprecate baseUrl support and require explicit prefixes in paths mappings.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4220113144) **Jasper-Nelligan** reported that adding a catch-all paths entry caused VSCode to auto-suggest imports from node_modules and asked if anyone else was facing the issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4288080930) **ruizmarc** confirmed experiencing the same issue where autoimports start with node_modules/ instead of the library name
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4293131060) **li-zck** affirmed encountering the issue and asked for a workaround
 * [today](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4298121028) **RyanCavanaugh** requested posting a new issue with a reproduction so the team could investigate

### [Issue microsoft/TypeScript#62905](https://github.com/microsoft/TypeScript/issues/62905) (Open, `Suggestion`, `Awaiting More Feedback`)

**Provide a new, simple 'browser' moduleResolution mode for Browser, ESM\-based, non\-bundled projects\.**

*Add a TypeScript Browser moduleResolution mode for ESM projects that only resolves relative and tsconfig-mapped paths and errors otherwise.*

 * [17 weeks ago](https://github.com/microsoft/TypeScript/issues/62905#issuecomment-3676611464) **HolgerJeromin** expressed surprise that the browser native approach was poorly supported and noted they could not find an eslint rule to catch incorrect auto imports without file extensions
 * (15 weeks ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/62905#issuecomment-4300077048) **jeseibel** agreed that a feature for deploying transpiled files would be helpful and described use cases involving browser handling, hybrid Maui Blazor apps, and embedded software

### [Issue microsoft/TypeScript#63420](https://github.com/microsoft/TypeScript/issues/63420) (Open, `Bug`, `Domain: Intersection`)

**union of pattern template literals intersected with optional brand mutually assignable to one with incompatible brand**

*TypeScript incorrectly allows mutual assignment between unions of template literal types intersected with incompatible optional brand properties.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63420#issuecomment-4290418908) **RyanCavanaugh** provided an automated analysis of why the two branded types are structurally assignable and linked relevant FAQs and issues
 * (yesterday) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Intersection`

### [Issue microsoft/TypeScript#63421](https://github.com/microsoft/TypeScript/issues/63421) (Open, `Not a Defect`)

**"Using type predicates" documentation promotes lying to the type system**

*The TypeScript documentation's type predicate example encourages misuse of 'as' assertions, undermining type safety.*

 * created by **ilyash-b**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4293448864) **MartinJohns** explained that type assertions bypass compiler checks and require 'lying' to the compiler
 * [today](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4296729187) **jcalz** explained that using type assertions in type predicate functions can mislead the type system, illustrated pitfalls with examples of ‘lying’ predicates, proposed stricter type definitions to avoid unsoundness, and agreed that the handbook guidance is sufficient
 * [today](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4297927428) **RyanCavanaugh** provided an automated analysis and guidance on implementing user-defined type guards including relevant FAQs
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4298029720) **RyanCavanaugh** argued that there’s usually no perfect way to write a type predicate function because built-in narrowing suffices and noted that using ‘in’ loses type safety on the key
 * [later](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4303181436) **ilyash-b** asked whether to comment on this in the handbook or close the issue, noting that 'in' is not a clear winner over 'as'

### [Issue microsoft/TypeScript#63422](https://github.com/microsoft/TypeScript/issues/63422) (Open)

**@typescript/typescript6 does not proxy subpath imports**

*@typescript/typescript6@6.0.0 omits a subpath exports map and tsserverlibrary file, so requiring typescript/lib/tsserverlibrary fails.*

 * created by **christopher-buss**
 * [today](https://github.com/microsoft/TypeScript/issues/63422#issuecomment-4297927484) **RyanCavanaugh** provided an auto-generated list of similar issues and suggested closing duplicates

### [PR microsoft/TypeScript#63423](https://github.com/microsoft/TypeScript/pull/63423) (Open, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump fast\-xml\-parser from 5\.5\.9 to 5\.7\.0**

*Upgrade fast-xml-parser dependency from 5.5.9 to 5.7.0 to leverage updated entity replacement and performance enhancements.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`
 * (today) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#63424](https://github.com/microsoft/TypeScript/pull/63424) (Open, `For Uncommitted Bug`)

**Add \`Intl\.PluralRules\.selectRange\` typing to es2023\.intl**

*Add the missing Intl.PluralRules.selectRange type definition to ES2023 Intl declarations in TypeScript.*

 * created by **3ru**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63424#issuecomment-4302615156) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63424#issuecomment-4302615177) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#63425](https://github.com/microsoft/TypeScript/issues/63425) (Open)

**Hover display for non\-homomorphic mapped types renders numeric\-string keys indistinguishably from numeric keys**

*TypeScript's hover display omits quotes for numeric-string keys in non-homomorphic mapped types, making them appear as numeric keys.*

 * created by **codpro2005**
 * [later](https://github.com/microsoft/TypeScript/issues/63425#issuecomment-4304286820) **mkantor** explained that JavaScript property keys are always strings or symbols and that TypeScript normalizes numeric keys, noted differences with keyof and referenced issue #47214
 * [later](https://github.com/microsoft/TypeScript/issues/63425#issuecomment-4304393568) **mkantor** rephrased the issue by explaining that B is displayed as a valid but observably-distinct type, which may confuse users copying it
 * [later](https://github.com/microsoft/TypeScript/issues/63425#issuecomment-4304396986) **codpro2005** acknowledged the oversight and explained scoping the issue to the hover inconsistency

### [Issue microsoft/TypeScript#63426](https://github.com/microsoft/TypeScript/issues/63426) (Open)

**Incorrect TS18047 Error \-\-\> "variable is possibly null"**

*TypeScript incorrectly flags the selection variable as possibly null even after an explicit null check in v6.0.3.*

 * created by **PoseidonEnergy**
 * [later](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4305049124) **MartinJohns** said "Another duplicate of #9998."
 * [later](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4305301332) **PoseidonEnergy** said "Wow. There are hundreds of posts describing #9998 dating all the way back to 2016. This is an obvious bug, it's unfortunate it still exists."

### [Issue microsoft/TypeScript#63427](https://github.com/microsoft/TypeScript/issues/63427) (Open)

**Add type definition for Math\.sumPrecise \(ES2025 / TC39 proposal\)**

*TypeScript 6.x lacks built-in type definitions for the new ES2025 Math.sumPrecise API, causing compile errors without manual augmentation.*

 * created by **827652549**

