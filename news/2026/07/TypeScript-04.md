# Report for 2026-07-04 (Saturday, July 4th, 2026)

3 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @daishuge provided implementation details in PR #63610 in [microsoft/TypeScript#44253](https://github.com/microsoft/TypeScript/issues/44253#issuecomment-4885934976)

## Activity Summary

### [Issue microsoft/TypeScript#17002](https://github.com/microsoft/TypeScript/issues/17002) (Open, `Suggestion`, `In Discussion`, `Domain: lib.d.ts`, `Fix Available`)

**Array\.isArray type narrows to any\[\] for ReadonlyArray\<T\>**

*Array.isArray fails to correctly narrow a union including ReadonlyArray<T>, resulting in an any[] type instead of ReadonlyArray<T>.*

 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-3958701606) **niklasholm** suggested using `unknown` and augmenting ArrayConstructor.isArray via global declaration to avoid `any` or type assertions
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4076378007) **slztfn** said "I believe @cahnory solution is the best one so far and it should be in the standard library"
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4080971605) **cahnory** described augmenting ArrayConstructor.isArray to use a readonly unknown[] type guard, compared approaches, noted a minor type-narrowing difference, and expressed a preference for a dedicated helper over standard-library augmentation
 * [later](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4885934843) **daishuge** submitted a minimal fix in PR #63609 that added an overload in es5.d.ts to preserve readonly input types without affecting unknown narrowing

### [Issue microsoft/TypeScript#44253](https://github.com/microsoft/TypeScript/issues/44253) (Open, `Suggestion`, `Domain: lib.d.ts`, `ES Next`)

**Support for \`Object\.hasOwn\` \(\`lib\.d\.ts\` and narrowing\)**

*Add stage 3 Object.hasOwn method definitions and type narrowing support in lib.d.ts.*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/44253#issuecomment-2614587657) **valler** added a test example linking to the TypeScript playground
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/44253#issuecomment-2616122986) **valler** described a third iteration of type definitions for ObjectConstructor.hasOwn with SimplifyIntersection and provided a Playground link for test cases
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/44253#issuecomment-2619832197) **valler** concluded they didn't need a fancier Object.hasOwn and provided a simplified TypeScript declaration along with a playground demo
 * [later](https://github.com/microsoft/TypeScript/issues/44253#issuecomment-4885934976) **daishuge** submitted an implementation in PR #63610 that detects Object.hasOwn and delegates to narrowTypeByInKeyword to implement same-branch narrowing with semantics identical to the `in` operator

### [PR microsoft/TypeScript#63604](https://github.com/microsoft/TypeScript/pull/63604) (Closed, `For Backlog Bug`)

**fix\(completions\): exclude \`default\` keyword from expression\-body arrow function completions**

*Exclude the default keyword from expression-bodied arrow function completions by modifying completion context detection and filters.*

 * created by **tsushanth**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63604#issuecomment-4869923852) **MartinJohns** said "@tsushanth You should read this: https://github.com/microsoft/TypeScript/issues/62963"
 * [today](https://github.com/microsoft/TypeScript/pull/63604#issuecomment-4884534330) **tsushanth** said "Thanks for the pointer — I see #62963. With the 6.0 merge criteria and the focus on TS7/Go rewrite this fix doesn't qualify. I'll close this out."
 * (today) **tsushanth** closed the issue

### [PR microsoft/TypeScript#63609](https://github.com/microsoft/TypeScript/pull/63609) (Open, `For Uncommitted Bug`)

**fix\(lib\): preserve readonly narrowing in Array\.isArray type guard**

*Introduce a new overload for Array.isArray in es5.d.ts to correctly preserve readonly array types during type narrowing.*

 * created by **daishuge**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63609#issuecomment-4885475302) **daishuge** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/63609#issuecomment-4885496605) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #17002. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [later](https://github.com/microsoft/TypeScript/pull/63609#issuecomment-4885496673) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #17002. If you can get it accepted, this PR will have a better chance of being reviewed."

### [PR microsoft/TypeScript#63610](https://github.com/microsoft/TypeScript/pull/63610) (Open, `For Uncommitted Bug`)

**feat\(checker\): add Object\.hasOwn\(\) type narrowing**

*Support type narrowing of object properties in Object.hasOwn() calls by leveraging existing in-operator logic.*

 * created by **daishuge**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63610#issuecomment-4885475416) **daishuge** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/63610#issuecomment-4885496751) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #44253. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [later](https://github.com/microsoft/TypeScript/pull/63610#issuecomment-4885496820) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #44253. If you can get it accepted, this PR will have a better chance of being reviewed."

