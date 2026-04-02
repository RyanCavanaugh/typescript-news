# Report for 2026-01-17 (Saturday, January 17th, 2026)

10 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @danilofuchs asked whether noUncheckedIndexAccess will be turned on by default in strict mode in [microsoft/TypeScript#54500](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3764353180)

## Activity Summary

### [Issue microsoft/TypeScript#32063](https://github.com/microsoft/TypeScript/issues/32063) (Open, `Suggestion`, `Awaiting More Feedback`)

**import ConstJson from '\./config\.json' as const;**

*Allow importing a JSON config file with a const modifier to infer literal union types for its values.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-3319118377) **Tom-de-Boer** said "I could also very much use this. I am trying to create types from a json-schema."
 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-3320534310) **thw0rted** described an approach using class-validator and class-validator-jsonschema to generate shared type declarations, use the decorated class for runtime validation, and compile JSON schemas for distribution and validation with ajv
 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-3320861920) **TechQuery** suggested using decorated classes for front-end data validation with Decorator stage-2 or a future Parameter Decorator proposal and referenced their MobX-RESTful library
 * [today](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-3764534135) **james-pre** implemented the feature in the TS compiler and opened a Go compiler pull request

### [Issue microsoft/TypeScript#37681](https://github.com/microsoft/TypeScript/issues/37681) (Open, `Suggestion`, `In Discussion`)

**Asynchronous type guards and assertion signatures**

*Support asynchronous custom type guards and assertion signatures returning Promise<value is Type> and Promise<asserts value is Type>.*

 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/37681#issuecomment-1221530302) **avin-kavish** requested support for async type guards and provided a code example showing the guard breaking when awaited
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/37681#issuecomment-1650605236) **steveluscher** asked for support for async assertion functions using SubtleCrypto#verify and shared example code
 * [52 weeks ago](https://github.com/microsoft/TypeScript/issues/37681#issuecomment-2597158467) **dgca** demonstrated a workaround using discriminated unions and an async utility to narrow promise return types and sketched a generic factory for async type checkers
 * [later](https://github.com/microsoft/TypeScript/issues/37681#issuecomment-3765217938) **orimay** said "It's crazy this is not yet implemented"

### [Issue microsoft/TypeScript#45537](https://github.com/microsoft/TypeScript/issues/45537) (Closed, `Help Wanted`, `Domain: API`)

**resolvedTrueType and resolvedFalseType of conditionType are not resolved when used in the compiler api**

*resolvedTrueType and resolvedFalseType on compiler API ConditionalType return unresolved when accessed via ts-morph.*

 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/45537#issuecomment-917586599) **jbrown16** offered a draft PR purportedly fixing the issue and asked for feedback on its adequacy
 * (4.3 years ago) **andrewbranch** closed the issue
 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/45537#issuecomment-921051349) **andrewbranch** invited opening a new issue to request exposing getTrueTypeFromConditionalType/getFalseTypeFromConditionalType and noted uncertainty about acceptance
 * [today](https://github.com/microsoft/TypeScript/issues/45537#issuecomment-3764345069) **olsonpm** asked for a recommended way to resolve conditional types without functions, then noted the discussion became obsolete due to API freezing

### [Issue microsoft/TypeScript#54500](https://github.com/microsoft/TypeScript/issues/54500) (Open, `Discussion`, `Fix Available`)

**6\.0 Deprecation Candidates**

*Deprecation proposals for TypeScript 6.0 include removal of legacy compiler flags and updates to modern defaults*

 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3531830683) **fry69** clarified that allowSyntheticDefaultExports did not exist, provided the correct compiler option allowSyntheticDefaultImports, and explained the origin of the typo in the TS 6 deprecation candidates issue
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3604830790) **michael-small** asked what the scope of `useDefineForClassFields` was in v6/v7 and referenced the proposed deprecation plan in issue #60284
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3745453163) **RyanCavanaugh** explained that useDefineForClassFields would remain supported in v6/v7 due to widespread dependencies and migration difficulty
 * [today](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3764353180) **danilofuchs** asked whether noUncheckedIndexAccess would be enabled by default in strict mode

### [PR microsoft/TypeScript#61265](https://github.com/microsoft/TypeScript/pull/61265) (Open, `For Backlog Bug`)

**Fixed an issue with \`ReduceLabel\` flows spoiling node reachability cache**

*Corrects ReduceLabel flow processing to prevent spoiling of the node reachability cache.*

 * created by **Andarist**
 * **typescript-bot** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#63002](https://github.com/microsoft/TypeScript/issues/63002) (Open, `Suggestion`, `Too Complex`)

**create primitive to prevent one folder from importing from another**

*Add a tsconfig.json setting to prevent imports between designated folders.*

 * created by **ORESoftware**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63002#issuecomment-3762617606) **MartinJohns** said "https://eslint.org/docs/latest/rules/no-restricted-imports"
 * [today](https://github.com/microsoft/TypeScript/issues/63002#issuecomment-3764521009) **ORESoftware** said "I think building into TS compiler instead of just ESLint might make a lot of sense though - seems like small cost and big win"

### [Issue microsoft/TypeScript#63003](https://github.com/microsoft/TypeScript/issues/63003) (Closed, `Bug`, `Domain: lib.d.ts`)

**\[Typo\] Possible typo in JSDoc string for \`Math\.trunc\(…\)\` function \(lib\.es2015\.core\.d\.ts\)**

*The JSDoc comment for Math.trunc in lib.es2015.core.d.ts contains a typo with an extra 'the' before 'a numeric expression'.*

 * created by **MichaelZalla**
 * [later](https://github.com/microsoft/TypeScript/issues/63003#issuecomment-3765303007) **Yashxp1** said "Yeah, I think it's a typo since x refers to a specific parameter, it should be “the numeric expression x” instead of “a numeric expression, x""

### [Issue microsoft/TypeScript#63004](https://github.com/microsoft/TypeScript/issues/63004) (Open, `Bug`)

**Explicit \`never\` return type in \`catch\` block & condition in \`finally\` marks the whole \`finally\` block as unreachable**

*TypeScript incorrectly flags a conditional finally block as unreachable when a catch handler calls a function declared to return never.*

 * created by **d-fischer**
 * [later](https://github.com/microsoft/TypeScript/issues/63004#issuecomment-3765286934) **Andarist** said "https://github.com/microsoft/TypeScript/pull/61265 fixes this too"

### [PR microsoft/TypeScript#63006](https://github.com/microsoft/TypeScript/pull/63006) (Open, `For Milestone Bug`, **RyanCavanaugh**)

**Don't try to narrow type of a symbol within RHS of its declaration**

*Prevent TypeScript from narrowing a symbol’s type within the right-hand side of its own declaration.*

 * created by **Andarist**
 * (today) **typescript-bot** added label `For Milestone Bug`, and assigned to **RyanCavanaugh**

### [Issue microsoft/TypeScript#63007](https://github.com/microsoft/TypeScript/issues/63007) (Open, `Duplicate`)

**"Conditionally optional" type works for concrete parameter but not generic**

*Conditional optional types work for concrete types but not when used with generics in TypeScript.*

 * created by **ianroberts**
 * [today](https://github.com/microsoft/TypeScript/issues/63007#issuecomment-3764420109) **MartinJohns** explained that resolution of conditional types involving unbound generic types is deferred and marked the issue as a duplicate of #52144

### [PR microsoft/TypeScript#63008](https://github.com/microsoft/TypeScript/pull/63008) (Open, `For Uncommitted Bug`)

**Add support for importing JSON modules "as const"**

*Add opt-in importJsonAsConst compiler option to import JSON modules with 'as const' literal typing.*

 * created by **james-pre**
 * (today) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63008#issuecomment-3764855551) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #32063. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [today](https://github.com/microsoft/TypeScript/pull/63008#issuecomment-3764855552) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #32063. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [today](https://github.com/microsoft/TypeScript/pull/63008#issuecomment-3764872636) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh

### [PR microsoft/TypeScript#63009](https://github.com/microsoft/TypeScript/pull/63009) (Open, `For Backlog Bug`)

**Tweak \`isValidHeritageClauseObjectLiteral\`**

*Update isValidHeritageClauseObjectLiteral to more accurately validate heritage clause object literals*

 * created by **Andarist**
 * **typescript-bot** added label `For Backlog Bug`

### [PR microsoft/TypeScript#63010](https://github.com/microsoft/TypeScript/pull/63010) (Open, `For Uncommitted Bug`)

**Don't error on \`this\` in arrows referencing explicit \`typeof globalThis\` annotation in parent this container**

*Allow arrow functions to reference this without errors in functions annotated with typeof globalThis*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`

