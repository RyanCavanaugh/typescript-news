# Report for 2026-01-10 (Saturday, January 10th, 2026)

5 different users commented on 6 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#41173](https://github.com/microsoft/TypeScript/issues/41173) (Open, `Suggestion`, `Awaiting More Feedback`)

**Accept de\-structured elements in type predicates**

*Allow destructured parameters in TypeScript type predicate functions to enable more concise and readable type checks.*

 * [46 weeks ago](https://github.com/microsoft/TypeScript/issues/41173#issuecomment-2668226289) **aleksei-minkin-webcom** said "This seems like a good feature, any news on this?"
 * [42 weeks ago](https://github.com/microsoft/TypeScript/issues/41173#issuecomment-2740322844) **mariusaarsnes** said "Any updates here?"
 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/41173#issuecomment-2750780227) **adam-marshall** said "Any news?"
 * [today](https://github.com/microsoft/TypeScript/issues/41173#issuecomment-3733647068) **ljharb** expressed frustration that TypeScript required literal argument names and prevented destructuring

### [Issue microsoft/TypeScript#59497](https://github.com/microsoft/TypeScript/issues/59497) (Open, `Suggestion`, `Awaiting More Feedback`)

**functions with destructuring parameters are not inferred as type predicate correctly**

*Filter callbacks using destructured parameters do not infer type predicates correctly, causing type narrowing errors.*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/59497#issuecomment-2285083397) **miguel-leon** suggested using a type guard predicate in the filter to narrow items to type 'A'
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/59497#issuecomment-2285669097) **Andarist** noted that making it a valid type predicate currently errors and raises new design questions
 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/59497#issuecomment-3418772759) **Ragnar-Oock** asked whether using the parameter name as the identifier would be valid under the stated goal and requested information about the “reuse as much as possible from the source file” goal
 * [today](https://github.com/microsoft/TypeScript/issues/59497#issuecomment-3733647201) **ljharb** expressed frustration at TypeScript requiring literal argument names for type-related functionality

### [Issue microsoft/TypeScript#62972](https://github.com/microsoft/TypeScript/issues/62972) (Closed, `Not a Defect`)

**\`errorType\` does not propagate with non\-distributive conditional types**

*Non-distributive conditional types in TypeScript fail to propagate errorType, unlike distributive conditional types.*

 * created by **mizdra**

### [PR microsoft/TypeScript#62973](https://github.com/microsoft/TypeScript/pull/62973) (Open, `For Uncommitted Bug`)

**Add explicit type variance specifiers to Promise, Map, Set**

*Add explicit type variance specifiers to Promise, Map, and Set to potentially improve type checking performance.*

 * created by **akaltar**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3733279171) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #62954. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [today](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3733280151) **akaltar** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#62974](https://github.com/microsoft/TypeScript/issues/62974) (Open, `Bug`, `Help Wanted`, `Domain: Crashes`)

**Crash: TypeError: Cannot read properties of undefined \(reading 'flags'\) in isFreshLiteralType during recursive tuple expansion with unresolved identifiers**

*TypeScript compiler crashes with a TypeError reading 'flags' in isFreshLiteralType during recursive tuple expansion with unresolved identifiers*

 * created by **na7ure-a**

