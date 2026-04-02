# Report for 2026-01-13 (Tuesday, January 13th, 2026)

14 different users commented on 24 different issues.

## Recommended Actions

 * Response Recommended
    * @valler asked for clarification on how isolated declarations relate to class expressions and requested use cases in [microsoft/TypeScript#36060](https://github.com/microsoft/TypeScript/issues/36060#issuecomment-3745302728)
    * @justinfagnani asked if there is sufficient platform support to implement CSS modules with import attributes in TypeScript in [microsoft/TypeScript#46135](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3745345018)
    * @justinfagnani asked if Firefox 147 shipping CSS modules is sufficient to add it to the DOM lib in [microsoft/TypeScript#46689](https://github.com/microsoft/TypeScript/issues/46689#issuecomment-3745276561)
    * @saksham-sankhla04 offered to work on the issue in [microsoft/TypeScript#62915](https://github.com/microsoft/TypeScript/issues/62915#issuecomment-3745705505)

## Activity Summary

### [Issue microsoft/TypeScript#36060](https://github.com/microsoft/TypeScript/issues/36060) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow \.d\.ts files to represent anonymous class expressions with \`private\` members**

*Enable .d.ts declaration files to represent anonymous class expressions with private members.*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/36060#issuecomment-2132038130) **MichaelMitchell-at** suggested a syntax for anonymous class types to annotate computed properties under isolatedDeclarations to reduce verbosity
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/36060#issuecomment-3398475344) **trusktr** described a TypeScript mixin example in which private fields on exported anonymous classes caused a type error, noted that private hashtag syntax suppressed the type error but leads to runtime errors
 * [today](https://github.com/microsoft/TypeScript/issues/36060#issuecomment-3744808515) **valler** explained that private and protected members break with dynamically created classes, showed how One and Two must share the same mixin result for protected members to work, and suggested a cleaner class-based pattern with code examples
 * [today](https://github.com/microsoft/TypeScript/issues/36060#issuecomment-3745302728) **valler** asked for clarification on how isolated declarations relate to class expressions and requested use cases
 * [today](https://github.com/microsoft/TypeScript/issues/36060#issuecomment-3745388037) **MichaelMitchell-at** said "Isolated declarations was later extended to support the case I brought up. My previous comment can be disregarded."
 * [today](https://github.com/microsoft/TypeScript/issues/36060#issuecomment-3745390489) **valler** suggested using top-level exported classes as a general workaround for the bug
 * [today](https://github.com/microsoft/TypeScript/issues/36060#issuecomment-3747185005) **valler** provided a TypeScript mixin example demonstrating private and protected members and noting the reduced complexity compared to the previous approach

### [Issue microsoft/TypeScript#46135](https://github.com/microsoft/TypeScript/issues/46135) (Open, `Suggestion`, `Awaiting More Feedback`)

**Ambient Module Declarations for Import Attributes \(formerly known as Import Assertions\)**

*Enable ambient module declarations based on import attributes to provide type definitions for CSS modules and asset URL imports.*

 * [21 weeks ago](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3198734819) **alii** asked what contributors could do to help land import bytes support in TypeScript
 * [17 weeks ago](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3284241553) **AFatNiBBa** said "Is there anything new on this?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3692946297) **otomad** suggested supporting the inline grab module type and provided a TypeScript code example
 * [today](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3745345018) **justinfagnani** noted that major browsers, Node, Deno, Bun, Rollup, and Webpack support CSS and JSON modules with import attributes, and asked if that provides enough platform support for TypeScript support

### [Issue microsoft/TypeScript#46689](https://github.com/microsoft/TypeScript/issues/46689) (Open, `Suggestion`, `Awaiting More Feedback`)

**CSS module support**

*Add TypeScript support for CSS modules import assertions, providing built-in typings and automatic CSS file copying.*

 * [42 weeks ago](https://github.com/microsoft/TypeScript/issues/46689#issuecomment-2738551364) **runarberg** mentioned having created a babel-plugin for this and provided its repository link
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/46689#issuecomment-3257073928) **justinfagnani** mentioned that Firefox was about to land CSS Modules and linked two Bugzilla issues for an implementation bug and a shipping bug
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/46689#issuecomment-3383035044) **jogibear9988** provided links to a babel-plugin and an esbuild addon implementation
 * [today](https://github.com/microsoft/TypeScript/issues/46689#issuecomment-3745276561) **justinfagnani** mentioned that Firefox 147 is now shipping CSS modules and asked if that is enough to add it to the DOM lib

### [Issue microsoft/TypeScript#54500](https://github.com/microsoft/TypeScript/issues/54500) (Open, `Discussion`, `Fix Available`)

**6\.0 Deprecation Candidates**

*Deprecation proposals for TypeScript 6.0 include removal of legacy compiler flags and updates to modern defaults*

 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3445167076) **jakebailey** said "I'm silly, that's clearly in #62196. Yay collapsed github threads"
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3531830683) **fry69** clarified that allowSyntheticDefaultExports did not exist, provided the correct compiler option allowSyntheticDefaultImports, and explained the origin of the typo in the TS 6 deprecation candidates issue
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3604830790) **michael-small** asked what the scope of `useDefineForClassFields` was in v6/v7 and referenced the proposed deprecation plan in issue #60284
 * [today](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3745453163) **RyanCavanaugh** explained that useDefineForClassFields would remain supported in v6/v7 due to widespread dependencies and migration difficulty

### [Issue microsoft/TypeScript#62256](https://github.com/microsoft/TypeScript/issues/62256) (Closed, `Help Wanted`, `Domain: check: Type Inference`, `Possible Improvement`)

**Typescript 5\.9 can no longer derive this type, becomes 'any' instead**

*TypeScript 5.9 no longer infers a React component callback parameter as { id: string } | null, defaulting to any.*

 * (20 weeks ago) **RyanCavanaugh** added labels `Possible Improvement`, `Domain: Type Inference`, and set milestone to `Backlog`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62275](https://github.com/microsoft/TypeScript/pull/62275) (Closed, `For Backlog Bug`)

**Discard types that reduce to \`never\` before discriminating by discriminable items**

*Filter out union types that resolve to never before performing discrimination based on discriminable properties.*

 * [20 weeks ago](https://github.com/microsoft/TypeScript/pull/62275#issuecomment-3208405622) **RyanCavanaugh** said "@ahejlsberg this one seems well-motivated. Can you take a look?"
 * (20 weeks ago) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62752](https://github.com/microsoft/TypeScript/issues/62752) (Open, `Suggestion`, `Awaiting More Feedback`)

**Strongly typed TypedArray values**

*Enable a generic element type parameter for TypedArrays to support stronger typing with unions or branded numbers.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/62752#issuecomment-3530777757) **Bertie690** chimed in to suggest adding these as TS native types behind a feature flag, shared a 500-line hand-rolled PartialInt16Array interface example, and noted needing @ts-expect-error for some overrides
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/62752#issuecomment-3581069609) **Renegade334** explained that TS 5.9's typed array interface changes and version discrepancies complicate type compatibility, argued that the suggested extra type parameter would worsen these headaches for library developers, and recommended handling it in userland
 * [today](https://github.com/microsoft/TypeScript/issues/62752#issuecomment-3746690050) **aapoalas** argued that adding a `Value extends number` type parameter would not bifurcate APIs or cause subtype variance issues and criticized pushing the solution to userland as it forces an ecosystem split

### [Issue microsoft/TypeScript#62915](https://github.com/microsoft/TypeScript/issues/62915) (Open, `Help Wanted`, `Docs`)

**Document that compiler\.extends can be an array**

*Update tsconfig.json documentation to indicate that the compiler.extends option can accept an array of configurations.*

 * (1 week ago) **RyanCavanaugh** added label `Docs`, and set milestone to `Backlog`
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62915#issuecomment-3723285450) **aaron-seq** announced intent to create a PR updating the TypeScript-Website documentation to clarify that `extends` can accept an array of configuration files
 * [today](https://github.com/microsoft/TypeScript/issues/62915#issuecomment-3745705505) **saksham-sankhla04** said "Hi, I would Like to work on this"

### [Issue microsoft/TypeScript#62965](https://github.com/microsoft/TypeScript/issues/62965) (Open, `Bug`, `Domain: LS: Type Display`)

**\`@deprecated\` on property getter and setters\.**

*Regression in TypeScript 5.1.6 causing @deprecated tags on property getters and setters to not be recognized consistently.*

 * created by **Danielku15**
 * [today](https://github.com/microsoft/TypeScript/issues/62965#issuecomment-3746633303) **RyanCavanaugh** noted that the issue was an unintended side effect of #41941 and repros in TS7
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: LS: Type Display`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/62965#issuecomment-3746763003) **a-tarasyuk** pointed out that the change applied only to completion items and explained that getters and setters share a symbol with two declarations requiring each declaration to be deprecated

### [Issue microsoft/TypeScript#62967](https://github.com/microsoft/TypeScript/issues/62967) (Open, `Suggestion`, `Help Wanted`, `Experience Enhancement`)

**JSDoc comments for async\_hooks are confusing/misleading**

*JSDoc comments in the async_hooks module misleadingly discourage its use while recommending AsyncLocalStorage, causing confusion in TypeScript.*

 * created by **a-non-a-mouse**
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Help Wanted`, `Experience Enhancement`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#62969](https://github.com/microsoft/TypeScript/pull/62969) (Closed, `For Uncommitted Bug`)

**Remove unnecessary type assertions**

*Remove unnecessary type assertions found during testing of the @typescript-eslint/no-unnecessary-type-assertion lint rule without affecting runtime or TS errors.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62969#issuecomment-3736259974) **jakebailey** expressed doubt that the changes would be merged because the TypeScript codebase is due to be overwritten soon
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62969#issuecomment-3740735228) **ulrichstark** thanked for feedback and offered to close the PR, noting it was a proof of concept for lint changes
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62970](https://github.com/microsoft/TypeScript/issues/62970) (Open, `Bug`, `Domain: lib.d.ts`)

**\`Intl\.CollatorOptions\['collation'\]\` is missing value \`'default'\`**

*TypeScript's Intl.CollatorOptions type omits the 'default' collation value.*

 * created by **quisido**
 * [today](https://github.com/microsoft/TypeScript/issues/62970#issuecomment-3745272686) **IllusionMH** asked whether the "default" collation value is meaningful or just a syntactic fallback
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: lib.d.ts`
 * [today](https://github.com/microsoft/TypeScript/issues/62970#issuecomment-3746083320) **RyanCavanaugh** clarified that passing default to Intl.Collator was sensible since resolvedOptions showed default
 * **RyanCavanaugh** added to milestone `Backlog`

### [PR microsoft/TypeScript#62971](https://github.com/microsoft/TypeScript/pull/62971) (Open, `For Backlog Bug`)

**add \`collation\` to \`Intl\.CollatorOptions\`**

*Add the collation property to Intl.CollatorOptions to enable specifying string comparison rules for different locales*

 * created by **quisido**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#62972](https://github.com/microsoft/TypeScript/issues/62972) (Closed, `Not a Defect`)

**\`errorType\` does not propagate with non\-distributive conditional types**

*Non-distributive conditional types in TypeScript fail to propagate errorType, unlike distributive conditional types.*

 * created by **mizdra**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62972#issuecomment-3737245693) **mizdra** questioned whether the behavior should be considered intended specification rather than a bug, reasoning that [ErrorType] extends [unknown] evaluates to true because arrays are of type Array
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62972#issuecomment-3737630505) **Andarist** clarified that eagerly reducing those constructs would degrade the in-IDE experience and compared { prop: ErrorType } to ErrorType
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/62972#issuecomment-3746022448) **RyanCavanaugh** clarified that the reported behavior should never occur and that no guarantees are made beyond the first line

### [Issue microsoft/TypeScript#62976](https://github.com/microsoft/TypeScript/issues/62976) (Closed, `Duplicate`)

**Nested Branded type does not error**

*TypeScript fails to enforce branded type distinctions in nested Records, allowing incompatible nested branded types to be assigned without error.*

 * created by **nitzcard**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62976#issuecomment-3739117679) **jcalz** said "Duplicate of or related to #43852 "
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#62980](https://github.com/microsoft/TypeScript/issues/62980) (Closed, `Bug`, `Breaking Change`, `Fix Available`)

**Deprecate, remove \`\-\-outFile\`**

*Deprecate and prepare removal of the `--outFile` compiler option in TypeScript 6.0 ahead of version 7.0.*

 * **typescript-bot** added label `Fix Available`
 * **DanielRosenwasser** removed label `Fix Available`
 * **typescript-bot** added label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/62980#issuecomment-3745437588) **RyanCavanaugh** said "ref #54500"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62981](https://github.com/microsoft/TypeScript/pull/62981) (Closed, `Author: Team`, `For Milestone Bug`, **RyanCavanaugh**)

**Deprecate \`\-\-outFile\`**

*Deprecate the --outFile compiler option as part of the fix for issue #62980.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/62981#issuecomment-3741283947) **typescript-bot** reported build start and completion statuses for the 'user test this' and 'test top800' commands
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62981#issuecomment-3741343885) **typescript-bot** reported user test comparisons between main and the merge pull request, noted infrastructure failures, and affirmed everything else looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62981#issuecomment-3741688191) **typescript-bot** reported that running tsc on the top 800 repos comparing main and the PR merge produced no issues
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62983](https://github.com/microsoft/TypeScript/pull/62983) (Open, `For Backlog Bug`)

**Fixed issues in relater related to tuples with variadic elements**

*Relater now correctly handles comparisons of tuple types containing variadic elements.*

 * created by **Andarist**
 * **typescript-bot** added label `For Backlog Bug`

### [PR microsoft/TypeScript#62984](https://github.com/microsoft/TypeScript/pull/62984) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**More strictness prep**

*Extends test coverage for various strict TypeScript compiler options including strictPropertyInitialization, useUnknownInCatchVariables, strictNullChecks, strictFunctionTypes, noImplicitAny, and decorator metadata serialization.*

 * created by **DanielRosenwasser**
 * (today) **typescript-bot** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript#62985](https://github.com/microsoft/TypeScript/issues/62985) (Closed, `Not a Defect`)

**Cannot extract base type from branded intersection**

*Request for a TypeScript mechanism to remove a branded intersection from a type and recover its base type.*

 * created by **shkumbinhasani**
 * [later](https://github.com/microsoft/TypeScript/issues/62985#issuecomment-3749270968) **mkantor** suggested using Error instead of any and noted uncertainty why any doesn't work

### [Issue microsoft/TypeScript#62986](https://github.com/microsoft/TypeScript/issues/62986) (Closed, `Duplicate`)

**Only the last overload of a function is considered while inferring**

*Inference for overloaded functions only uses the last signature when inferring return or parameter types instead of uniting all overloads*

 * created by **AFatNiBBa**
 * [later](https://github.com/microsoft/TypeScript/issues/62986#issuecomment-3750125156) **MartinJohns** explained that the behavior was working as intended and documented in the TypeScript handbook with a link to conditional types

