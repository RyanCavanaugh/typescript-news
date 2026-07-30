# Report for 2026-07-27 (Monday, July 27th, 2026)

9 different users commented on 12 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#43368](https://github.com/microsoft/TypeScript/issues/43368) (Open, `Suggestion`, `Awaiting More Feedback`)

**Suggestion: Allow getters to have predicate return types**

*Enable TypeScript class getters to have user-defined type predicate return types for type guards.*

 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-4410653140) **owenoak** said "+1 for this"
 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-4600711749) **MaestroDD0S** said "+1 "
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-5036153917) **merlinaudio** noted that methods have different semantics than getters, expressed a strong preference for getters, and gave a +1
 * [later](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-5101166181) **danieleloscozzese** mentioned having the same use case and argued that boolean checks should be getters rather than methods for ergonomic consistency

### [Issue microsoft/TypeScript#63598](https://github.com/microsoft/TypeScript/issues/63598) (Closed, `Bug`, `Domain: Formatter`, `Fix Available`, **gabritto**)

**"Token end is child end" when '= ${id}id' is used in a property annotation**

*Formatting a property annotation using a malformed template literal triggers a 'Token end is child end' debug failure in TypeScript.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * **typescript-automation[bot]** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: Formatter`
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript#63606](https://github.com/microsoft/TypeScript/issues/63606) (Closed, `Bug`, `Domain: lib.d.ts`)

**Intl\.PluralRules constructor should not be callable without new**

*The TypeScript lib.es2020.intl.d.ts incorrectly allows calling Intl.PluralRules without new, contrary to the ECMA-402 specification.*

 * (3 weeks ago) **RyanCavanaugh** added label `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63606#issuecomment-5088590324) **rekha0suthar** said "I'd like to work on this — starting now."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63608](https://github.com/microsoft/TypeScript/pull/63608) (Closed, `For Backlog Bug`)

**fix\(lib\): remove callable signature without new from Intl\.PluralRules…**

*Remove callable signature from Intl.PluralRules in type definitions to enforce constructor invocation with new.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/63608#issuecomment-4881716027) **SiddGud** said "@microsoft-github-policy-service agree"
 * (3 weeks ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63672](https://github.com/microsoft/TypeScript/issues/63672) (Closed, `Working as Intended`)

**showConfig CLI option no longer shows all the compilation options**

*After updating to TypeScript 6.0.3, the CLI option --showConfig no longer displays default compiler options.*

 * created by **yohny**
 * [today](https://github.com/microsoft/TypeScript/issues/63672#issuecomment-5094014249) **RyanCavanaugh** said "--showConfig intentionally doesn't show options which are not different from their defaults, and 6.0 changed the default values for the ones you see no longer listed."
 * **RyanCavanaugh** added label `Working as Intended`

### [Issue microsoft/TypeScript#63681](https://github.com/microsoft/TypeScript/issues/63681) (Open, `Suggestion`, `Awaiting More Feedback`)

**Proposal: \`unstable\` and \`volatile\` control\-flow analysis modifiers**

*Add erasable ‘unstable’ and ‘volatile’ declaration modifiers to disable TypeScript’s optimistic control-flow narrowing for specific variables and properties.*

 * created by **5cover**
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [later](https://github.com/microsoft/TypeScript/issues/63681#issuecomment-5104806304) **jcalz** said "cross-linking to #49669"

### [Issue microsoft/TypeScript#63682](https://github.com/microsoft/TypeScript/issues/63682) (Open, `Bug`, `Help Wanted`)

**ES2025 regex syntax \(duplicate named groups, pattern modifiers\) is not gated by \`target\`**

*TypeScript does not enforce target-based errors for ES2025 regex features such as duplicate named groups and pattern modifiers.*

 * created by **dayongkr**
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63683](https://github.com/microsoft/TypeScript/issues/63683) (Closed, `Working as Intended`)

**Retain key type in \`Object\.entries\(\)\`**

*Enhance TypeScript’s lib.es2017 Object.entries definition to preserve specific object key types rather than generic strings.*

 * created by **nickshanks**
 * [today](https://github.com/microsoft/TypeScript/issues/63683#issuecomment-5096252862) **MartinJohns** said "Try searching for Object.keys in this repository. This has been rejected over and over again."
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63683#issuecomment-5096497419) **RyanCavanaugh** said "entries is just keys + their values, so the same logic applies"

### [Issue microsoft/TypeScript#63684](https://github.com/microsoft/TypeScript/issues/63684) (Closed)

**كود**

*Submitted issue titled 'كود' containing only a link to the TypeScript issue creation page.*

 * created by **503badrr**

### [Issue microsoft/TypeScript#63685](https://github.com/microsoft/TypeScript/issues/63685) (Closed)

**JSDoc \`@type\` does not type a Promise in TypeScript Playground**

*JSDoc @type {Promise<number>} annotations in TypeScript Playground don’t infer the Promise’s resolved type, making .then callback argument unknown.*

 * created by **arka-prat-juno**
 * [later](https://github.com/microsoft/TypeScript/issues/63685#issuecomment-5103325944) **MartinJohns** reported inability to reproduce the issue after switching to JavaScript mode and removing TypeScript code, and noted that JSDoc typing does not work in TypeScript
 * [later](https://github.com/microsoft/TypeScript/issues/63685#issuecomment-5104862358) **jcalz** explained that the Playground file type must be set to JS instead of TS and provided a link

### [Issue microsoft/TypeScript#63686](https://github.com/microsoft/TypeScript/issues/63686) (Closed, `Question`)

**\`\!\` does not narrow discriminated unions when \`strict\` is \`false\`**

*Using !result.ok fails to narrow the discriminated union to the false branch when strict mode is disabled*

 * created by **LancesLance56**

### [Issue microsoft/TypeScript#63687](https://github.com/microsoft/TypeScript/issues/63687) (Closed)

**\[Bug\]: Control flow analysis fails to narrow Discriminated Union when destructuring in loop**

*TypeScript's control flow analysis fails to narrow destructured discriminated union elements inside a for...of loop*

 * created by **mahjandora**
 * [later](https://github.com/microsoft/TypeScript/issues/63687#issuecomment-5106298122) **mahjandora** acknowledged a known limitation where destructuring breaks control flow narrowing, noted that checking the parent object's discriminant resolved the issue, and apologized for duplicating the report
 * (later) **mahjandora** closed the issue

