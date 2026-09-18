# Report for 2026-09-12 (Saturday, September 12th, 2026)

5 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @Ichi075 asked if their proposed direction for investigating inference improvements is reasonable in [microsoft/TypeScript#63019](https://github.com/microsoft/TypeScript/issues/63019#issuecomment-5652264608)

## Activity Summary

### [Issue microsoft/TypeScript#63019](https://github.com/microsoft/TypeScript/issues/63019) (Open, `Help Wanted`, `Domain: check: Type Inference`, `Possible Improvement`)

**Regression: Generic function returning union of tuples is not assignable to identical type since v4\.2**

*TypeScript 4.2 regression incorrectly widens generics causing identical generic functions returning unions of tuples to be unassignable.*

 * (31 weeks ago) **RyanCavanaugh** added labels `Possible Improvement`, `Domain: check: Type Inference`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/63019#issuecomment-5652264608) **Ichi075** asked whether investigating discriminated union matching during type inference is reasonable and noted reproduction versions for tuple and object forms

### [Issue microsoft/TypeScript#64168](https://github.com/microsoft/TypeScript/issues/64168) (Open, `Bug`)

**\`getChildren\(\)\` drops the \`\<\` token of a type argument list when immediately followed by another \`\<\`**

*getChildren() removes the first '<' in a '<<' type argument list, causing a gap in AST children*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64168#issuecomment-5543643908) **RyanCavanaugh** said "We're not making fixes to the TS6 API, but based on the linked PR it looks like there's a TS7 equivalent problem"
 * (1 week ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/64168#issuecomment-5650107944) **irfanstract** said "related to #63850 (with getText() or getFullText())"

### [PR microsoft/TypeScript#64243](https://github.com/microsoft/TypeScript/pull/64243) (Open, `For Uncommitted Bug`)

**fix: disallow NoSubstitutionTemplate in module import attribute types**

*Enforce rejecting empty template literals in module import attribute types by requiring quoted string literals.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5633219206) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5638319287) **DanielRosenwasser** appreciated test coverage and asked if there are tests for template string types with interpolations, requesting their addition if missing
 * [today](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5647642629) **camc314** explained that requiring quoted string literals is better design due to spec distinctions and consistency; noted the downstream tool impact and that it can change since unreleased; added a test case for template string types with interpolations

### [Issue microsoft/TypeScript#64244](https://github.com/microsoft/TypeScript/issues/64244) (Closed, `Working as Intended`)

**The isFinite\(\) type declaration doesn't specify the right type**

*The TypeScript declaration for global isFinite incorrectly specifies its parameter as number instead of any.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5640638046) **SetTrend** suggested adding a link to the TypeScript FAQ in the lib declaration to reduce confusion about isFinite usage
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5640766744) **RyanCavanaugh** noted that the library typing was intentional and cited MDN's warning against using isFinite due to coercion
 * [today](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5645885126) **SetTrend** suggested considering MDN documentation users in the JsDoc docs for isFinite instead of expecting them to refer to the wiki
 * [later](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5652715247) **MartinJohns** said "See his StackOverflow response: https://stackoverflow.com/a/41750391"

### [PR microsoft/TypeScript#64254](https://github.com/microsoft/TypeScript/pull/64254) (Open, `For Backlog Bug`)

**fix\(checker\): emit TS2845 for exported enum member truthiness checks \(\#63565\)**

*Fix truthiness checks on exported enum members to emit TS2845 by evaluating constant initializers in the checker.*

 * created by **vaibhavsrv**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`

### [PR microsoft/TypeScript#64255](https://github.com/microsoft/TypeScript/pull/64255) (Closed, `For Backlog Bug`)

**test: add regression coverage for await in computed member names of namespace classes \(\#63712\)**

*Adds regression tests verifying TS1308 diagnostics for await in computed member names of exported and unexported namespace classes.*

 * created by **vaibhavsrv**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64255#issuecomment-5651907568) **vaibhavsrv** said "Closing PR as issue #63712 already has existing test coverage in awaitInNamespaceExportedClassComputedProperty.ts."
 * (later) **vaibhavsrv** closed the issue

