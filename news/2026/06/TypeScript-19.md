# Report for 2026-06-19 (Friday, June 19th, 2026)

7 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @neoneye reported that they tried multiple fixes including clearing caches but still couldn't get quicklook working and may need assistance in [microsoft/TypeScript#25945](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-4757554749)

## Activity Summary

### [Issue microsoft/TypeScript#25945](https://github.com/microsoft/TypeScript/issues/25945) (Closed, `External`)

**macOS considers typescript files to be MPEG\-2 Transport Stream \- QuickLook and Spotlight do not work**

*macOS incorrectly identifies TypeScript (.ts) files as MPEG-2 transport streams, breaking QuickLook and Spotlight functionality.*

 * [33 weeks ago](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-3463523226) **cryptolit0** mocked the project as being sponsored by Microsoft
 * [26 weeks ago](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-3649797068) **qgustavor** described that the .ts extension issue arose from a lack of file extension standardization across operating systems, noted that renaming the extension was impractical, and proposed future OS heuristics to distinguish file types
 * [17 weeks ago](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-3916884301) **qgustavor** suggested adopting .cts and .mts over .ts to avoid conflicts and provided a migration guide
 * [later](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-4757554749) **neoneye** said "Just wasted 1 hour on trying to resolve this issue with Claude, making all kinds of changes to my mac, clearing caches. No luck getting quicklook working for ts files."

### [Issue microsoft/TypeScript#56235](https://github.com/microsoft/TypeScript/issues/56235) (Open, `Suggestion`, `Awaiting More Feedback`)

**Safe type assertion \(upcast / widening\) operator**

*Introduce a safe `as!` type assertion operator that only permits casting to a wider type without altering runtime behavior.*

 * [46 weeks ago](https://github.com/microsoft/TypeScript/issues/56235#issuecomment-3141256372) **jcalz** cross-linked `satisfiesas`, `satisfias`, and `sassafras` with two issue comments
 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/56235#issuecomment-4145657649) **5cover** asked whether the operator model type annotation would mirror standard type annotation semantics including assignability and excess property checks, and suggested syntax variants like 'ascribe', 'be', and 'to'.
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/56235#issuecomment-4533848101) **mkantor** suggested using 'x satisfies as T' syntax and explained its benefits
 * [later](https://github.com/microsoft/TypeScript/issues/56235#issuecomment-4757663281) **michaelboyles** argued that using 'is' for this feature provided symmetry with type guards, was shorter and more readable, and that tooling could mitigate its visual similarity to 'as'.

### [Issue microsoft/TypeScript#63566](https://github.com/microsoft/TypeScript/issues/63566) (Open, `Working as Intended`)

**TypeScript doesn't consider contravariance in member functions even with strictFunctionTypes**

*TypeScript ignores contravariance in function-typed object members, allowing unsafe assignments even with strictFunctionTypes.*

 * created by **alecov**

### [PR microsoft/TypeScript#63567](https://github.com/microsoft/TypeScript/pull/63567) (Closed, `For Backlog Bug`)

**fix\(checker\): avoid stack overflow for self\-referential computed enum member names**

*Fix stack overflow crashes by treating self-referential computed enum member names as non-bindable during name resolution.*

 * created by **yen0304**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#63568](https://github.com/microsoft/TypeScript/issues/63568) (Open)

**Regression: 7\.0\.1\-RC Unable to Satisfy Recursive Mapped Type Constraint**

*TypeScript 7.0.1-RC fails to satisfy recursive mapped type constraints that worked in earlier releases.*

 * created by **sinclairzx81**

### [Issue microsoft/TypeScript#63569](https://github.com/microsoft/TypeScript/issues/63569) (Closed, `Suggestion`, `Out of Scope`)

**Switch Expression**

*Add C#-style switch expression syntax to TypeScript for concise inline value mappings*

 * created by **Lenmint**
 * [later](https://github.com/microsoft/TypeScript/issues/63569#issuecomment-4757274226) **MartinJohns** pointed out that the proposal was out of scope for TypeScript and the viability checklist item was checked mistakenly

