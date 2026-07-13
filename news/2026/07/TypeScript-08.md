# Report for 2026-07-08 (Tuesday, July 7th, 2026)

6 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @tonyboho asked if the change should be pinned with a test to avoid regressions in [microsoft/TypeScript#63619](https://github.com/microsoft/TypeScript/issues/63619#issuecomment-4907024735)
    * @upsuper provided repro steps as requested in [microsoft/TypeScript#63627](https://github.com/microsoft/TypeScript/issues/63627#issuecomment-4909418101)

## Activity Summary

### [Issue microsoft/TypeScript#47920](https://github.com/microsoft/TypeScript/issues/47920) (Closed, `Suggestion`, `Fixed`, `Fix Available`)

**"satisfies" operator to ensure an expression matches some type \(feedback reset\)**

*Collecting feedback and refining scenarios for adding a TypeScript ‘satisfies’ operator that enforces type compatibility.*

 * [today](https://github.com/microsoft/TypeScript/issues/47920#issuecomment-4901884856) **tvogel** described using satisfies to constrain nested object literal types and asked for alternative approaches without duplicating the type
 * [today](https://github.com/microsoft/TypeScript/issues/47920#issuecomment-4903238427) **Svish** recommended defining the object as Record<string, string | undefined> directly instead of using satisfies or as
 * [today](https://github.com/microsoft/TypeScript/issues/47920#issuecomment-4904748607) **c-harding** clarified that object literal syntax doesn't work for nested object parts and that the entire object must be defined that way
 * [today](https://github.com/microsoft/TypeScript/issues/47920#issuecomment-4909361174) **tvogel** clarified that the object literal workaround didn't work for nested object parts and suggested using separately typed consts or a check-and-bless operator for expressions

### [PR microsoft/TypeScript#63574](https://github.com/microsoft/TypeScript/pull/63574) (Closed, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump js\-yaml from 4\.1\.1 to 4\.2\.0**

*Upgrade js-yaml to version 4.2.0 from 4.1.1 to incorporate safety documentation, new loader options, and bug fixes.*

 * **dependabot[bot]** added label `javascript`
 * (2 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63574#issuecomment-4916588698) **dependabot[bot]** said "Superseded by #63633."
 * (later) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript#63609](https://github.com/microsoft/TypeScript/pull/63609) (Closed, `For Uncommitted Bug`)

**fix\(lib\): preserve readonly narrowing in Array\.isArray type guard**

*Introduce a new overload for Array.isArray in es5.d.ts to correctly preserve readonly array types during type narrowing.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63609#issuecomment-4885496605) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #17002. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63609#issuecomment-4885496673) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #17002. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63609#issuecomment-4896919593) **anderson-pete** explained that the first overload collapses to any, making it always chosen, and argued that stricter readonly typing, while correct, would break existing code
 * [today](https://github.com/microsoft/TypeScript/pull/63609#issuecomment-4906326308) **RyanCavanaugh** said "+1 to the above comment. The difficulties here have been discussed at length and the lack of a solution is not due to a lack of trying."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63619](https://github.com/microsoft/TypeScript/issues/63619) (Open, `Fixed`)

**\`get self\(\): this\` in an interface crashes the checker \(6\.0 regression\)**

*Interface accessor declarations using a ‘this’ return type crash the TypeScript 6.0 checker, regressing from 5.9.*

 * created by **tonyboho**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63619#issuecomment-4897160218) **RyanCavanaugh** marked the issue as fixed in 7.0 and suggested 'readonly self: this' as a 6.0 workaround
 * **RyanCavanaugh** added label `Fixed`
 * [today](https://github.com/microsoft/TypeScript/issues/63619#issuecomment-4907024735) **tonyboho** said "Shouldn't it be pinned with a test, to avoid regressions in the future?"
 * [today](https://github.com/microsoft/TypeScript/issues/63619#issuecomment-4909508046) **RyanCavanaugh** said "Feel free to send a PR with a test, no objections to that"

### [Issue microsoft/TypeScript#63627](https://github.com/microsoft/TypeScript/issues/63627) (Open, `Needs Investigation`, **ahejlsberg**)

**\`NoInfer\` changes behavior for type matching on spread**

*Applying NoInfer to spread types unexpectedly produces type errors whereas equivalent spreads without NoInfer succeed*

 * created by **upsuper**
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63627#issuecomment-4906525044) **RyanCavanaugh** said "Using NoInfer around a type expression with no type parameters doesn't make any sense. Don't do this."
 * [today](https://github.com/microsoft/TypeScript/issues/63627#issuecomment-4909418101) **upsuper** demonstrated that wrapping NoInfer around a type parameter triggered the same type inference error and presented a code example and error message
 * [today](https://github.com/microsoft/TypeScript/issues/63627#issuecomment-4909504855) **RyanCavanaugh** said "Why do you have NoInfer there either? e.g. what's a sample call that it fixes?"
 * [today](https://github.com/microsoft/TypeScript/issues/63627#issuecomment-4909777910) **upsuper** explained that NoInfer allows a function to have fewer parameters than A and illustrated inference errors without it using a TypeScript example
 * **RyanCavanaugh** removed label `Not a Defect`

### [Issue microsoft/TypeScript#63628](https://github.com/microsoft/TypeScript/issues/63628) (Open, `Bug`, `Domain: Error Messages`)

**Incorrect diagnostic message in TS2814**

*TS2814’s misleading error “Function with bodies can only merge with ambient classes” is shown when merging a body-less function declaration with a class.*

 * created by **bvanjoi**
 * [today](https://github.com/microsoft/TypeScript/issues/63628#issuecomment-4903849625) **snarbles2** clarified that `function Foo();` is invalid syntax, noted the need for the `declare` keyword and a return type under `noImplicitAny`, and mentioned that this fix did not address other errors
 * (today) **RyanCavanaugh** added labels `Not a Defect`, `Bug`, removed label `Not a Defect`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63631](https://github.com/microsoft/TypeScript/pull/63631) (Closed, `For Backlog Bug`)

**fix\(2814\): correct misleading error message for functions without bodies**

*Remove 'with bodies' qualifier from TS2814 error to clarify merge restrictions apply to any function declaration.*

 * created by **Nabeel-akk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63631#issuecomment-4906822128) **Nabeel-akk** said "Closing this - the message key change cascades to generated files. Will resubmit with a proper fix."
 * (today) **Nabeel-akk** closed the issue

### [Issue microsoft/TypeScript#63632](https://github.com/microsoft/TypeScript/issues/63632) (Open, `Suggestion`, `Awaiting More Feedback`)

**Feature request: machine\-readable \(JSONL\) diagnostics output**

*Add a JSONL output flag to the TypeScript compiler to provide machine-readable diagnostics in watch and noEmit modes.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63632#issuecomment-4906907307) **Alex-Bond** asked whether to move the feature request to the main TS repo and suggested creating adapters for customizable outputs while keeping current flags until 8.0
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63632#issuecomment-4906907326) **jakebailey** doubted that adapters would be supported or included in version 7.0 and suggested moving the feature while relying on the API
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63632#issuecomment-4906907350) **Alex-Bond** agreed to target the change for version 7.1 to avoid additional cleanup, acknowledged overengineering by considering SARIF, JSONL, and template outputs, and explained the adapter motivation
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [PR microsoft/TypeScript#63633](https://github.com/microsoft/TypeScript/pull/63633) (Open, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump js\-yaml from 4\.1\.1 to 4\.3\.0**

*Upgrade js-yaml dependency from version 4.1.1 to 4.3.0 for security fixes and new features.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `javascript`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

