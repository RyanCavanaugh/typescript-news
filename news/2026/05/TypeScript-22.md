# Report for 2026-05-22 (Friday, May 22nd, 2026)

9 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @heroboy asked if the issue was fixed in version 6.0.3 in [microsoft/TypeScript#41548](https://github.com/microsoft/TypeScript/issues/41548#issuecomment-4524987622)
    * @Derugon provided a code suggestion for matches() overloads in [microsoft/TypeScript#63497](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4520380563)
    * @zainnadeem786 asked if the proposed fix direction for wildcard export validation aligns with the intended design in [microsoft/TypeScript#63499](https://github.com/microsoft/TypeScript/issues/63499#issuecomment-4522920279)

## Activity Summary

### [Issue microsoft/TypeScript#39459](https://github.com/microsoft/TypeScript/issues/39459) (Closed, `Suggestion`, `Committed`, `Domain: LS: TSServer`, **jakebailey**)

**tsserver should implement the Language Server Protocol **

*Enable tsserver to natively support the Language Server Protocol for broader TypeScript IDE integration.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/39459#issuecomment-2716008345) **halfnibble** expressed excitement about TypeScript and Go and nostalgia for Microsoft
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/39459#issuecomment-2716113639) **0xdevalias** provided a direct link to the TypeScript-Go LSP prototype
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/39459#issuecomment-2742724777) **mickaelistria** said "I'd be delighted to give it a try in eg Eclipse IDE one of these days. Is there a place where one can access some snapshot builds of tsgo already to start having fun with it?"
 * [today](https://github.com/microsoft/TypeScript/issues/39459#issuecomment-4524226998) **jakebailey** closed the issue, mentioned TS 7.0 nearing completion, and shared a preview link
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#41548](https://github.com/microsoft/TypeScript/issues/41548) (Open, `Bug`, `Fix Available`, `Domain: check: Excess Property Checking`, `Has Repro`, **Copilot**)

**Compile error if I named last array destructuring element\.**

*TypeScript incorrectly flags an excess property error for objects passed to a generic function when using array destructuring that binds only the last element.*

 * (42 weeks ago) **typescript-bot** added labels `Fix Available`, `Fix Available`
 * **RyanCavanaugh** added label `Domain: Excess Property Checking`
 * [later](https://github.com/microsoft/TypeScript/issues/41548#issuecomment-4524987622) **heroboy** observed that the code had no errors in version 6.0.3 and asked if the issue was fixed

### [Issue microsoft/TypeScript#51011](https://github.com/microsoft/TypeScript/issues/51011) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow circular constraints**

*Allow immediate circular generic constraints in TypeScript so types can extend themselves without errors.*

 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/51011#issuecomment-1754634794) **brad-jones** explained difficulty with TypeScript type algebra while designing a type-safe DSL for DAGs and showed several code attempts
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/51011#issuecomment-1788481941) **devanshj** provided a TypeScript code example implementing Dagfile and DagDSL
 * [yesterday](https://github.com/microsoft/TypeScript/issues/51011#issuecomment-4513832492) **jcalz** asked why F-bounded generic circularity is problematic and what scenarios cause real issues
 * [today](https://github.com/microsoft/TypeScript/issues/51011#issuecomment-4520708589) **RyanCavanaugh** explained that failed inference didn't trigger an error, provided an example of circular constraints, and noted that the error exists to prevent stack overflows
 * [today](https://github.com/microsoft/TypeScript/issues/51011#issuecomment-4520951615) **jcalz** asked where a stack overflow could occur given recursive constraint inference fallback to unknown
 * [today](https://github.com/microsoft/TypeScript/issues/51011#issuecomment-4521608458) **RyanCavanaugh** noted that they would also try it themselves to answer the question

### [Issue microsoft/TypeScript#58692](https://github.com/microsoft/TypeScript/issues/58692) (Open, `Suggestion`, `Awaiting More Feedback`)

**\[isolatedDeclarations\] An option like disableSourceOfProjectReferenceRedirect, but configurable on the referenced project's end**

*Add a per-project compiler option to disable source-based project reference redirects for isolatedDeclarations-enabled projects to improve responsiveness.*

 * (1.9 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/58692#issuecomment-4518295031) **maxired** reported that tsc -b reported errors not shown in VSCode due to project reference redirect behavior in a TypeScript monorepo
 * [today](https://github.com/microsoft/TypeScript/issues/58692#issuecomment-4521402353) **RyanCavanaugh** explained that project references require consistent compiler options across analysis units and that differing settings necessitate using .d.ts files

### [Issue microsoft/TypeScript#63219](https://github.com/microsoft/TypeScript/issues/63219) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow primitive LHS to \`instanceof\` operator if RHS is a custom \`hasInstance\`**

*Enable using instanceof with primitive left-hand values when the right-hand side defines a custom Symbol.hasInstance method.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/63219#issuecomment-4016296812) **MartinJohns** said "Duplicate of #59492."
 * (10 weeks ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63219#issuecomment-4524126711) **nuckolp-amzn** demonstrated a sample use case by defining a StringEnum helper in TypeScript and provided a playground link

### [PR microsoft/TypeScript#63489](https://github.com/microsoft/TypeScript/pull/63489) (Closed, `For Uncommitted Bug`)

**Fix \`es2020\.intl\.d\.ts\` formatting**

*Correct inconsistent formatting in the es2020.intl.d.ts TypeScript declaration file.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/63489#issuecomment-4472153592) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/63489#issuecomment-4472153608) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63497](https://github.com/microsoft/TypeScript/issues/63497) (Open, `Help Wanted`, `Domain: lib.d.ts`)

**DOM: \`Element\#matches\(\)\` incorrectly narrows types**

*Using Element.matches with a specific tag name inside a negated condition incorrectly narrows the element's type to never.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4505625574) **Derugon** suggested a proper fix for element.matches narrowing issues and provided test cases with playground links
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4513118282) **voxpelli** asked when the issues were encountered in practice and provided a working example link
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4514725394) **MartinJohns** noted that the example worked only because of the null-conditional operator and would fail if the value were non-null or explicitly checked for null
 * [today](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4520366278) **voxpelli** refocused on the change’s intent and noted that instanceof-based type deduction only works for tags with a 1:1 class relationship
 * [today](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4520380563) **Derugon** suggested using PickExtends and PickExtendsStrict to refine Element.matches overloads and adding an extra overload for literal tag names

### [Issue microsoft/TypeScript#63499](https://github.com/microsoft/TypeScript/issues/63499) (Open, `Bug`, `Domain: LS: Auto-import`)

**Wildcard package\.json exports auto\-import path does not apply traversal containment checks**

*tsserver auto-import provider ignores traversal containment in wildcard package.json exports and indexes files outside package.*

 * created by **zainnadeem786**
 * [today](https://github.com/microsoft/TypeScript/issues/63499#issuecomment-4521547487) **RyanCavanaugh** said "Who exactly is able to read a file they couldn't already read in this setup?"
 * [today](https://github.com/microsoft/TypeScript/issues/63499#issuecomment-4521569247) **zainnadeem786** explained concerns about inconsistent containment enforcement between normal module resolution and tsserver package-json auto-import indexing, noting that wildcard export targets with traversal segments can still enumerate out-of-package files and justifying reporting it as a hardening issue
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: LS: Auto-import`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63499#issuecomment-4522920279) **zainnadeem786** suggested that the wildcard branch needed traversal validation like non-wildcard paths and offered to implement a fix pending confirmation

### [PR microsoft/TypeScript#63500](https://github.com/microsoft/TypeScript/pull/63500) (Open, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump qs from 6\.15\.0 to 6\.15\.2**

*Update qs dependency from version 6.15.0 to 6.15.2 to incorporate multiple stringify and parse fixes.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`
 * **typescript-bot** added label `For Uncommitted Bug`

