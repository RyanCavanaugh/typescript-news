# Report for 2026-07-26 (Sunday, July 26th, 2026)

6 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @rekha0suthar volunteered to work on the issue in [microsoft/TypeScript#63606](https://github.com/microsoft/TypeScript/issues/63606#issuecomment-5088590324)
    * @droooney provided a code example demonstrating the issue with enums in [microsoft/TypeScript#63655](https://github.com/microsoft/TypeScript/issues/63655#issuecomment-5089560131)

## Activity Summary

### [Issue microsoft/TypeScript#55538](https://github.com/microsoft/TypeScript/issues/55538) (Closed, `Suggestion`, `Awaiting More Feedback`)

**When using disposable, typescript should never report the variable as unused**

*TypeScript should not flag variables declared with using as unused since they are implicitly used for disposal.*

 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/55538#issuecomment-1948309886) **KristjanTammekivi** referenced the discard-binding proposal and remarked that they had to wait for it
 * (2.4 years ago) **KristjanTammekivi** closed the issue
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/55538#issuecomment-5069593738) **matthieusieben** suggested reconsidering the issue due to growing support for using, described a workaround for non-disposable dependencies, and noted that the error message was misleading because variables were used implicitly
 * [later](https://github.com/microsoft/TypeScript/issues/55538#issuecomment-5091870984) **snarbles2** stated that the error message was accurate and clear and argued that no action was needed due to the void-binding proposal and the underscore workaround

### [Issue microsoft/TypeScript#63606](https://github.com/microsoft/TypeScript/issues/63606) (Closed, `Bug`, `Domain: lib.d.ts`)

**Intl\.PluralRules constructor should not be callable without new**

*The TypeScript lib.es2020.intl.d.ts incorrectly allows calling Intl.PluralRules without new, contrary to the ECMA-402 specification.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Bug`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/63606#issuecomment-5088590324) **rekha0suthar** said "I'd like to work on this — starting now."

### [Issue microsoft/TypeScript#63655](https://github.com/microsoft/TypeScript/issues/63655) (Closed, `Duplicate`)

**No type mismatch for records with enum keys inside object literal with dynamic key**

*TypeScript fails to flag a type mismatch when assigning a string to a number-valued Record property via a dynamic key.*

 * **RyanCavanaugh** added label `Duplicate`
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63655#issuecomment-5053380531) **typescript-automation[bot]** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (4 days ago) **typescript-automation[bot]** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63655#issuecomment-5089560131) **droooney** acknowledged the mix-up between enum and union types and provided a code example showing the same issue with enums

### [Issue microsoft/TypeScript#63666](https://github.com/microsoft/TypeScript/issues/63666) (Open, `Bug`, `Domain: check: Type Inference`)

**\[5\.9 regression\] as const readonly tuple inferred as mutable through a nested generic call under a conditional\-type circular constraint**

*TypeScript 5.9 regression infers readonly 'as const' tuples as mutable in nested generic circular conditional types.*

 * created by **xkatianx**
 * (4 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: check: Type Inference`

### [Issue microsoft/TypeScript#63671](https://github.com/microsoft/TypeScript/issues/63671) (Open, `Needs Investigation`, `Fix Available`, **andrewbranch**)

**Module value in TSConfig does not enforce ModuleResolution value**

*TypeScript allows a tsconfig module value of nodenext with a moduleResolution of node16 instead of enforcing nodenext resolution as documented.*

 * created by **yohny**
 * (later) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Backlog`, and assigned to **andrewbranch**
 * **typescript-automation[bot]** added label `Fix Available`

### [Issue microsoft/TypeScript#63677](https://github.com/microsoft/TypeScript/issues/63677) (Open, `Bug`)

**type parameter variance in generic call signature is incorrectly bivariant**

*TypeScript incorrectly allows bivariant assignments for invariant generic call signatures, resulting in unsound type checking.*

 * created by **ahmedajiz629**
 * (later) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63678](https://github.com/microsoft/TypeScript/issues/63678) (Open, `Needs Investigation`, **johnfav03**)

**tsc \-\-watch doesn't work on NTFS partitions on Linux**

*After upgrading to TypeScript 7, tsc --watch fails on Linux NTFS partitions due to fanotify_mark no such device errors.*

 * created by **bt7s7k7**
 * (later) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript#63679](https://github.com/microsoft/TypeScript/issues/63679) (Open, `Bug`, `Help Wanted`)

**Should not allow \`import\.defer?\.\('x'\)\`**

*Prevent optional chaining calls on import.defer so import.defer?.('x') is correctly rejected.*

 * created by **fisker**
 * (later) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63680](https://github.com/microsoft/TypeScript/pull/63680) (Open, `dependencies`, `github_actions`)

**Bump the github\-actions group with 8 updates**

*Upgrade eight GitHub Actions dependencies including checkout, setup-node, cache, CodeQL actions, and scorecard to their latest versions.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [Issue microsoft/TypeScript#63681](https://github.com/microsoft/TypeScript/issues/63681) (Open, `Suggestion`, `Awaiting More Feedback`)

**Proposal: \`unstable\` and \`volatile\` control\-flow analysis modifiers**

*Add erasable ‘unstable’ and ‘volatile’ declaration modifiers to disable TypeScript’s optimistic control-flow narrowing for specific variables and properties.*

 * created by **5cover**
 * (later) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#63682](https://github.com/microsoft/TypeScript/issues/63682) (Open, `Bug`, `Help Wanted`)

**ES2025 regex syntax \(duplicate named groups, pattern modifiers\) is not gated by \`target\`**

*TypeScript does not enforce target-based errors for ES2025 regex features such as duplicate named groups and pattern modifiers.*

 * created by **dayongkr**

