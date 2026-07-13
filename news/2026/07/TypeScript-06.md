# Report for 2026-07-06 (Monday, July 6th, 2026)

17 different users commented on 39 different issues.

## Recommended Actions

 * Moderation
    * @subweave-bot posted spam content in [microsoft/TypeScript#63343](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4903271233)
 * Response Recommended
    * @anderson-pete noted that the fix would break a lot of existing code in [microsoft/TypeScript#17002](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4896931936)
    * @tvogel asked for alternative ways to achieve the typing constraint without duplicating the type in [microsoft/TypeScript#47920](https://github.com/microsoft/TypeScript/issues/47920#issuecomment-4901884856)
    * @snarbles2 provided syntax correction advice in [microsoft/TypeScript#63628](https://github.com/microsoft/TypeScript/issues/63628#issuecomment-4903849625)

## Activity Summary

### [Issue microsoft/TypeScript#17002](https://github.com/microsoft/TypeScript/issues/17002) (Open, `Suggestion`, `In Discussion`, `Domain: lib.d.ts`, `Fix Available`)

**Array\.isArray type narrows to any\[\] for ReadonlyArray\<T\>**

*Array.isArray fails to correctly narrow a union including ReadonlyArray<T>, resulting in an any[] type instead of ReadonlyArray<T>.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4076378007) **slztfn** said "I believe @cahnory solution is the best one so far and it should be in the standard library"
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4080971605) **cahnory** described augmenting ArrayConstructor.isArray to use a readonly unknown[] type guard, compared approaches, noted a minor type-narrowing difference, and expressed a preference for a dedicated helper over standard-library augmentation
 * [yesterday](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4885934843) **daishuge** submitted a minimal fix in PR #63609 that added an overload in es5.d.ts to preserve readonly input types without affecting unknown narrowing
 * [today](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4896931936) **anderson-pete** noted that the proposed fix would break a lot of existing code

### [Issue microsoft/TypeScript#47920](https://github.com/microsoft/TypeScript/issues/47920) (Closed, `Suggestion`, `Fixed`, `Fix Available`)

**"satisfies" operator to ensure an expression matches some type \(feedback reset\)**

*Collecting feedback and refining scenarios for adding a TypeScript ‘satisfies’ operator that enforces type compatibility.*

 * [3.2 years ago](https://github.com/microsoft/TypeScript/issues/47920#issuecomment-1513473903) **RyanCavanaugh** linked to the TypeScript 4.9 announcement showing the 'satisfies' feature is available
 * [3.2 years ago](https://github.com/microsoft/TypeScript/issues/47920#issuecomment-1513479417) **BribeFromTheHive** expressed surprise that the fix existed and thanked the author for sharing because they couldn’t find any information elsewhere
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/47920#issuecomment-2198376324) **maksverver** indicated that the satisfies constraint works for function expressions but not declarations, and suggested adding syntax for function declarations
 * [later](https://github.com/microsoft/TypeScript/issues/47920#issuecomment-4901884856) **tvogel** described using satisfies to constrain nested object literal types and asked for alternative approaches without duplicating the type
 * [later](https://github.com/microsoft/TypeScript/issues/47920#issuecomment-4903238427) **Svish** recommended defining the object as Record<string, string | undefined> directly instead of using satisfies or as
 * [later](https://github.com/microsoft/TypeScript/issues/47920#issuecomment-4904748607) **c-harding** clarified that object literal syntax doesn't work for nested object parts and that the entire object must be defined that way

### [PR microsoft/TypeScript#63343](https://github.com/microsoft/TypeScript/pull/63343) (Open)

**Use trie for removeStringLiteralsMatchedByTemplateLiterals**

*Optimize removeStringLiteralsMatchedByTemplateLiterals by building a prefix trie for efficient template literal matching*

 * [13 weeks ago](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4180238308) **jakebailey** said "Is this different than https://github.com/microsoft/TypeScript/pull/59759?"
 * [13 weeks ago](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4180269841) **eps1lon** said "Looks like the same at a glance. Yours is already doing some size estimation it seems. I haven't accounted for opting out of trie-based search for small types."
 * [12 weeks ago](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4234453594) **afurm** asked whether the trie needed to index non-prefix segments too
 * [later](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4903271233) **subweave-bot** praised the trie-based matching as smart and fast and included a Subweave map link

### [PR microsoft/TypeScript#63593](https://github.com/microsoft/TypeScript/pull/63593) (Open, `For Uncommitted Bug`, `Voight-Kampff Anomaly`)

**ci: pin GitHub Actions to full commit SHAs**

*Pin GitHub Actions to specific commit SHAs to prevent supply-chain attacks while retaining version tags as comments.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63593#issuecomment-4824701768) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63593#issuecomment-4824701769) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`

### [PR microsoft/TypeScript#63594](https://github.com/microsoft/TypeScript/pull/63594) (Open, `For Uncommitted Bug`, `Voight-Kampff Anomaly`)

**ci: pin GitHub Actions to full commit SHAs**

*Pin GitHub Actions to specific commit SHAs to prevent supply-chain attacks while retaining version tags as comments.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63594#issuecomment-4824702512) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63594#issuecomment-4824702514) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`

### [Issue microsoft/TypeScript#63598](https://github.com/microsoft/TypeScript/issues/63598) (Open, `Bug`, `Domain: Formatter`, `Fix Available`, **gabritto**)

**"Token end is child end" when '= ${id}id' is used in a property annotation**

*Formatting a property annotation using a malformed template literal triggers a 'Token end is child end' debug failure in TypeScript.*

 * (today) **RyanCavanaugh** set milestone to `Backlog`, and assigned to **gabritto**
 * **typescript-automation[bot]** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: Formatter`

### [Issue microsoft/TypeScript#63603](https://github.com/microsoft/TypeScript/issues/63603) (Open, `Bug`, `Domain: LS: Completion Lists`)

**Issue: TypeScript autocomplete for template literal types ignores user's Quote Style preference**

*Autocomplete suggestions for template literal type keys always use double quotes, ignoring the user's configured quote style preference.*

 * created by **Gabilabrebi**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: LS: Completion Lists`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63606](https://github.com/microsoft/TypeScript/issues/63606) (Open, `Bug`, `Domain: lib.d.ts`)

**Intl\.PluralRules constructor should not be callable without new**

*The TypeScript lib.es2020.intl.d.ts incorrectly allows calling Intl.PluralRules without new, contrary to the ECMA-402 specification.*

 * created by **ptomato**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: lib.d.ts`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63608](https://github.com/microsoft/TypeScript/pull/63608) (Open, `For Backlog Bug`)

**fix\(lib\): remove callable signature without new from Intl\.PluralRules…**

*Remove callable signature from Intl.PluralRules in type definitions to enforce constructor invocation with new.*

 * (2 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63608#issuecomment-4881716027) **SiddGud** said "@microsoft-github-policy-service agree"
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63609](https://github.com/microsoft/TypeScript/pull/63609) (Closed, `For Uncommitted Bug`)

**fix\(lib\): preserve readonly narrowing in Array\.isArray type guard**

*Introduce a new overload for Array.isArray in es5.d.ts to correctly preserve readonly array types during type narrowing.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63609#issuecomment-4885475302) **daishuge** said "@microsoft-github-policy-service agree"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63609#issuecomment-4885496605) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #17002. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63609#issuecomment-4885496673) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #17002. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [today](https://github.com/microsoft/TypeScript/pull/63609#issuecomment-4896919593) **anderson-pete** explained that the first overload collapses to any, making it always chosen, and argued that stricter readonly typing, while correct, would break existing code

### [Issue microsoft/TypeScript#63616](https://github.com/microsoft/TypeScript/issues/63616) (Open, `Bug`, `Domain: This-Typing`)

**Inconsistent \`typeof this\` when the \`this\` parameter declared in the signature of a function parameter**

*Declaring a this parameter for callback functions leads to inconsistent inferred types for typeof this depending on whether this is used in the function body.*

 * created by **mpal9000**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: This-Typing`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63619](https://github.com/microsoft/TypeScript/issues/63619) (Open, `Fixed`)

**\`get self\(\): this\` in an interface crashes the checker \(6\.0 regression\)**

*Interface accessor declarations using a ‘this’ return type crash the TypeScript 6.0 checker, regressing from 5.9.*

 * created by **tonyboho**
 * [today](https://github.com/microsoft/TypeScript/issues/63619#issuecomment-4897160218) **RyanCavanaugh** marked the issue as fixed in 7.0 and suggested 'readonly self: this' as a 6.0 workaround
 * **RyanCavanaugh** added label `Fixed`

### [PR microsoft/TypeScript#63620](https://github.com/microsoft/TypeScript/pull/63620) (Closed, `For Uncommitted Bug`)

**Update and rename protocol\.ts to protocol\_print\.ts**

*Rename the protocol.ts file to protocol_print.ts and apply necessary updates according to TZAHAL 1165.*

 * created by **liu-idf18**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63620#issuecomment-4895906378) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63620#issuecomment-4895906397) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63621](https://github.com/microsoft/TypeScript/pull/63621) (Closed, `For Uncommitted Bug`)

**Atualização **

*Requesting status updates for cases TZAHAL 19715 and FOIA 151465.*

 * created by **liu-idf18**
 * [today](https://github.com/microsoft/TypeScript/pull/63621#issuecomment-4896025442) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63621#issuecomment-4896025454) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63622](https://github.com/microsoft/TypeScript/pull/63622) (Closed, `For Uncommitted Bug`)

**Update copilot\-setup\-steps\.yml**

*Align copilot-setup-steps.yml with TZAHAL-165 requirements*

 * created by **liu-idf18**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63622#issuecomment-4896177680) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63622#issuecomment-4896177684) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63623](https://github.com/microsoft/TypeScript/pull/63623) (Closed, `For Uncommitted Bug`)

**Update codeql\-configuration\.yml**

*Update codeql-configuration.yml to incorporate changes required by TZAHAL-165 and FOIA-151874.*

 * created by **liu-idf18**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63623#issuecomment-4896233862) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63623#issuecomment-4896233874) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63624](https://github.com/microsoft/TypeScript/pull/63624) (Closed, `For Uncommitted Bug`)

**gh pr checkout 63624 \- Atualização **

*Update pull request 63624 to incorporate the TZAHAL 165 changes.*

 * created by **liu-idf18**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63624#issuecomment-4896288678) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63624#issuecomment-4896335223) **MartinJohns** said "What's with the sudden increase of pull request spam?"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63625](https://github.com/microsoft/TypeScript/pull/63625) (Closed, `For Uncommitted Bug`)

**Atualização **

*Requesting an update on TZAHAL.*

 * created by **liu-idf18**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63625#issuecomment-4896388386) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63626](https://github.com/microsoft/TypeScript/issues/63626) (Open, `Fixed`)

**Support HTMLElement\.focus\(\) Option FocusVisible**

*Add FocusVisible to FocusOptions in TypeScript's HTMLElement.focus() definitions to match modern browser support.*

 * created by **larnett**
 * [today](https://github.com/microsoft/TypeScript/issues/63626#issuecomment-4897299647) **MartinJohns** mentioned that focusVisible is already supported and suggested adding the type definition via declaration merging
 * **RyanCavanaugh** added label `Fixed`

### [Issue microsoft/TypeScript#63627](https://github.com/microsoft/TypeScript/issues/63627) (Open, `Needs Investigation`, **ahejlsberg**)

**\`NoInfer\` changes behavior for type matching on spread**

*Applying NoInfer to spread types unexpectedly produces type errors whereas equivalent spreads without NoInfer succeed*

 * created by **upsuper**

### [Issue microsoft/TypeScript#63628](https://github.com/microsoft/TypeScript/issues/63628) (Open, `Bug`, `Domain: Error Messages`)

**Incorrect diagnostic message in TS2814**

*TS2814’s misleading error “Function with bodies can only merge with ambient classes” is shown when merging a body-less function declaration with a class.*

 * created by **bvanjoi**
 * [later](https://github.com/microsoft/TypeScript/issues/63628#issuecomment-4903849625) **snarbles2** clarified that `function Foo();` is invalid syntax, noted the need for the `declare` keyword and a return type under `noImplicitAny`, and mentioned that this fix did not address other errors

### [PR microsoft/TypeScript#63629](https://github.com/microsoft/TypeScript/pull/63629) (Closed, `For Milestone Bug`, `Voight-Kampff Anomaly`, **gabritto**)

**fix\(formatting\): recover from token spans outside property children**

*Recover from tokens overrunning node boundaries by fixing the formatting recursion guard in processChildNode and adding a regression test.*

 * created by **ahfoysal**
 * [later](https://github.com/microsoft/TypeScript/pull/63629#issuecomment-4901819030) **ahfoysal** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/63629#issuecomment-4903493769) **MartinJohns** said "@ahfoysal You should read this: https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * (later) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **gabritto**

### [PR microsoft/TypeScript#63630](https://github.com/microsoft/TypeScript/pull/63630) (Closed, `For Uncommitted Bug`)

**Create frontend change**

*Implement frontend changes according to contribution guidelines, keeping code up-to-date, passing all tests, and adding new unit tests.*

 * created by **AFJAL23**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63630#issuecomment-4904905880) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63630#issuecomment-4904905941) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63631](https://github.com/microsoft/TypeScript/pull/63631) (Closed, `For Backlog Bug`)

**fix\(2814\): correct misleading error message for functions without bodies**

*Remove 'with bodies' qualifier from TS2814 error to clarify merge restrictions apply to any function declaration.*

 * created by **Nabeel-akk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

