# Report for 2026-08-04 (Tuesday, August 4th, 2026)

9 different users commented on 28 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#63533](https://github.com/microsoft/TypeScript/issues/63533) (Closed, `Design Notes`)

**Design Meeting Notes, 2026\-06\-04**

*Ban unparenthesized type assertions and satisfies with binary operators under erasableSyntaxOnly to preserve source maps and prevent ambiguous precedence.*

 * **RyanCavanaugh** added label `Design Notes`
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63533#issuecomment-4633821401) **jcalz** suggested that issue #34692 might mitigate a possible downside with template literals and Unicode
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63533#issuecomment-4634309789) **RyanCavanaugh** said "This didn't make it into the notes, but I'm actually very glad we didn't add length as a property. It's not really clear what you would even do with it under the proposed 7.0 behavior."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63677](https://github.com/microsoft/TypeScript/issues/63677) (Open, `Bug`, `Domain: check: Variance Relationships`)

**type parameter variance in generic call signature is incorrectly bivariant**

*TypeScript incorrectly allows bivariant assignments for invariant generic call signatures, resulting in unsound type checking.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63677#issuecomment-5133861386) **ayishaatwork** offered to work on the issue, reproduce the behavior, trace the compiler's assignability handling for generic function signatures, identify the unsound variance check, and share findings before opening a PR
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63677#issuecomment-5152761234) **ahmedajiz629** noted that intersecting a generic type T with D is equivalent to using a constraint <T extends D> and suggested D be contravariant
 * **RyanCavanaugh** added label `Domain: check: Variance Relationships`

### [Issue microsoft/TypeScript#63705](https://github.com/microsoft/TypeScript/issues/63705) (Closed, `Needs Investigation`, **weswigham**)

**TypeScript 7 declaration emit reuses an unrelated JSDoc import and generates an invalid type reference**

*TypeScript 7's declaration emit incorrectly reuses a private JSDoc import alias, producing invalid type references in declarations.*

 * (4 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **weswigham**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63705#issuecomment-5153126629) **platypii** provided context as maintainer of hyparquet and hyparquet-writer and described a type error that surfaced after regenerating types with TypeScript 7 due to a dependency on SchemaElement
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#63709](https://github.com/microsoft/TypeScript/issues/63709) (Open, `Fix Available`, `Cursed?`, `Possible Improvement`)

**Property lookups on arguments to type parameters constrained by string index signatures can violate other constraints because undefined is included for optional properties**

*Property lookups on generics constrained by string index signatures include undefined for optional properties, allowing type constraint violations to go undetected.*

 * created by **aweebit**
 * [today](https://github.com/microsoft/TypeScript/issues/63709#issuecomment-5182712235) **RyanCavanaugh** said "I don't see a fix here that wouldn't make a lot of very "this code is fine" examples start complaining. If you have one I'm all ears, but this particular cure seems worse than the current disease."
 * (today) **RyanCavanaugh** added labels `Cursed?`, `Possible Improvement`, and set milestone to `Dormant`
 * **typescript-automation[bot]** added label `Fix Available`

### [Issue microsoft/TypeScript#63714](https://github.com/microsoft/TypeScript/issues/63714) (Closed, `Design Limitation`, **RyanCavanaugh**, **Copilot**)

**Typescript still checks return type in a lamba that calls a function returning 'never'**

*TypeScript lambda with declared number return type errors for missing return when calling a never-returning method.*

 * created by **kwasimensah**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63714#issuecomment-5173766276) **MartinJohns** explained that the behavior matched the specification from issue #32695, detailing the conditions for assertion or never-returning calls
 * [today](https://github.com/microsoft/TypeScript/issues/63714#issuecomment-5179477257) **jcalz** explained how to ensure control flow analysis by explicitly typing the impl variable and provided a code example
 * (today) **RyanCavanaugh** added label `Design Limitation`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/issues/63714#issuecomment-5181997167) **RyanCavanaugh** said "Added https://github.com/microsoft/TypeScript/wiki/FAQ#calls-to-cfa-affecting-require-explicitly-typed-names-to-affect-control-flow"

### [Issue microsoft/TypeScript#63715](https://github.com/microsoft/TypeScript/issues/63715) (Closed, `Duplicate`)

**Implicitly typed type guard does not guard**

*TypeScript does not narrow union types when a never-returning guard function is implicitly typed as () => void, unlike when explicitly typed as () => never.*

 * [today](https://github.com/microsoft/TypeScript/issues/63715#issuecomment-5176541355) **OldStarchy** noted the complexity of type inference, suggested supporting never-returning methods for simpler use cases, and provided a code example with a workaround
 * [today](https://github.com/microsoft/TypeScript/issues/63715#issuecomment-5177240623) **MartinJohns** reiterated that they didn’t know the details and pointed to related issues, noted the team’s awareness of the restriction and suggested that Ryan address it when labeling or closing the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63715#issuecomment-5179494056) **jcalz** said "As a feature request, this would duplicate #45385 (which is a good read for people who run into this situation)."
 * [today](https://github.com/microsoft/TypeScript/issues/63715#issuecomment-5182474408) **RyanCavanaugh** argued that type circularities frequently arise from added features and illustrated with an example why enforcing annotations on CFA-affecting symbols reduces user burden
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#63716](https://github.com/microsoft/TypeScript/pull/63716) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Document control\-flow requirements for \`never\`\-returning calls**

*Document that calls to never-returning methods require explicit type annotations on their receivers to satisfy circular control-flow analysis constraints.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63717](https://github.com/microsoft/TypeScript/pull/63717) (Open, `For Uncommitted Bug`, `Voight-Kampff Anomaly`)

**Pin GitHub Actions to full\-length commit SHAs**

*Pin GitHub Actions workflows to immutable full-length commit SHAs and set a 7-day Dependabot cooldown for improved security and reproducibility.*

 * created by **OssSecurityBot**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63717#issuecomment-5181808795) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63717#issuecomment-5181808821) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`

### [Issue microsoft/TypeScript#63718](https://github.com/microsoft/TypeScript/issues/63718) (Open, `Bug`, `Help Wanted`)

**TS1518 depends on operand order in negated v\-mode class unions**

*TS1518 detection for negated v-mode RegExp character class unions is order-dependent, failing to flag invalid patterns when the string-pattern operand is second.*

 * created by **mohsen1**

### [Issue microsoft/TypeScript#63719](https://github.com/microsoft/TypeScript/issues/63719) (Closed, `Not a Defect`)

**ReDoS via typesMap\.json regex injection in loadTypesMap\(\)**

*Unsanitized regex patterns in typesMap.json cause ReDoS in the TypeScript language server.*

 * created by **bolverk**
 * [today](https://github.com/microsoft/TypeScript/issues/63719#issuecomment-5187697061) **MartinJohns** argued that the described vulnerability was a non-issue because a supply chain compromise posed a greater risk than regex exhaustion

### [Issue microsoft/TypeScript#63720](https://github.com/microsoft/TypeScript/issues/63720) (Closed)

**ReDoS via autoImportFileExcludePatterns in stringToRegex\(\)**

*Unsanitized regex patterns in TypeScript autoImportFileExcludePatterns enable ReDoS catastrophically hanging the language server during auto-import resolution.*

 * created by **bolverk**
 * [today](https://github.com/microsoft/TypeScript/issues/63720#issuecomment-5187214833) **bolverk** said "Closing — this issue has an incorrect setting name. The vulnerable setting is , not . Filing a corrected issue."
 * (today) **bolverk** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63720#issuecomment-5187386738) **MartinJohns** said "You do know that you can edit issues, right?"

### [Issue microsoft/TypeScript#63721](https://github.com/microsoft/TypeScript/issues/63721) (Closed)

**ReDoS via autoImportSpecifierExcludeRegexes in stringToRegex\(\)**

*User regex patterns in autoImportSpecifierExcludeRegexes are passed unsanitized to new RegExp, causing ReDoS and hanging the TypeScript language server.*

 * created by **bolverk**
 * [later](https://github.com/microsoft/TypeScript/issues/63721#issuecomment-5191792705) **nmain** noted that the Go rewrite uses RE2-based regex immune to ReDoS and mentioned that the AI thought the issue was already fixed

### [Issue microsoft/TypeScript#63722](https://github.com/microsoft/TypeScript/issues/63722) (Open, `Help Wanted`, `Domain: lib.d.ts`)

**\`Array\.prototype\.at\` docs use "code unit" instead of "item"**

*Array.prototype.at documentation mistakenly uses 'code unit' instead of 'item' or 'element' terminology.*

 * created by **grundb**

