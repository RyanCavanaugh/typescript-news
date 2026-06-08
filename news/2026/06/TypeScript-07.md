# Report for 2026-06-07 (Sunday, June 7th, 2026)

5 different users commented on 27 different issues.

## Recommended Actions

 * Response Recommended
    * @iroquoispliskin2 asked if they could work on the open issue in [microsoft/TypeScript#63090](https://github.com/microsoft/TypeScript/issues/63090#issuecomment-4650612002)
    * @scarab-systems provided requested test results and update after review in [microsoft/TypeScript#63543](https://github.com/microsoft/TypeScript/pull/63543#issuecomment-4645878227)

## Activity Summary

### [Issue microsoft/TypeScript#34692](https://github.com/microsoft/TypeScript/issues/34692) (Open, `Suggestion`, `Awaiting More Feedback`)

**Enhance members of literal type like const array type \(e\.g\. string literal types should have literal length property\)**

*Request to improve string literal types by inferring exact length and character literal types for indexed access similar to const arrays.*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/34692#issuecomment-2286102351) **castarco** critiqued proposals for introducing new intrinsic types as against guidelines and lacking broad usefulness
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/34692#issuecomment-2286898441) **augustobmoura** discussed adding literal string length metadata, provided example implementations, and asked how to store the length value and define literal types
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/34692#issuecomment-2543328551) **HansBrende** argued that supporting length on string literals would simplify useful type patterns and provided examples using index signatures or existential types
 * [today](https://github.com/microsoft/TypeScript/issues/34692#issuecomment-4644344222) **jcalz** shared a recursive TypeScript utility type for determining string literal lengths, working up to length 8191, and linked to a playground

### [Issue microsoft/TypeScript#41952](https://github.com/microsoft/TypeScript/issues/41952) (Open, `Docs`)

**Document File name has a '\.js' extension \- stripping it**

*Document TypeScript's process of stripping .js and .jsx extensions and subsequent module lookup behavior.*

 * created by **sguillia**
 * **RyanCavanaugh** added label `Docs`
 * [today](https://github.com/microsoft/TypeScript/issues/41952#issuecomment-4644017200) **EECOLOR** pointed to the TypeScript documentation on file extension substitution

### [Issue microsoft/TypeScript#63090](https://github.com/microsoft/TypeScript/issues/63090) (Open, `Bug`, `Help Wanted`, `Domain: check: Type Circularity`)

**Crash: RangeError: Maximum call stack size exceeded during type serialization of recursive distributive mapped types**

*Recursive distributive mapped types trigger a compiler stack overflow error in TypeScript 5.7.3 and later.*

 * (16 weeks ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: check: Type Circularity`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/63090#issuecomment-4650612002) **iroquoispliskin2** said "Hey, if the issue is still open, would you mind I give it a shot?"

### [Issue microsoft/TypeScript#63531](https://github.com/microsoft/TypeScript/issues/63531) (Closed, `Help Wanted`, `Docs`)

**Markdown heading level bug in Narrowing documentation**

*The 'Truthiness narrowing' heading in the TypeScript Narrowing documentation is formatted as H1 instead of H2, causing subsequent sections to be incorrectly nested under it in the table of contents.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63531#issuecomment-4625038495) **RyanCavanaugh** said "Weird, the accessibility scan is supposed to yell at us when this happens"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63531#issuecomment-4630156658) **MannXo** said "I'll take this if no one's working on it yet."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63531#issuecomment-4630477675) **MartinJohns** said "@MannXo There are already open PR to address this issue. Generally, the TypeScript team does not assign issues to users. You're free to just work on issues labelled as "Help wanted" and issue PRs."
 * (later) **mzleman** closed the issue

### [Issue microsoft/TypeScript#63540](https://github.com/microsoft/TypeScript/issues/63540) (Open, `Suggestion`, `Needs Proposal`)

**Better ownership lint to eliminate ownership chaos for generated code**

*Add a TypeScript ownership lint enforcing explicit resource management to avoid disposal-related crashes in generated code.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63540#issuecomment-4638502645) **MartinJohns** said "This has absolutely nothing to do with AI. Same code can be written by humans. Better Code can be written by AI."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63540#issuecomment-4638663487) **loynoir** noted that AI could write better code but might introduce double free issues and suggested adopting a stricter type system like Rust's
 * [today](https://github.com/microsoft/TypeScript/issues/63540#issuecomment-4642992017) **loynoir** reaffirmed that humans are humans regardless of skin color or wealth, and that AI is AI regardless of nationality or performance or price, and updated the title to generated code as @MartinJohns suggested
 * (later) **RyanCavanaugh** added labels `Suggestion`, `Needs Proposal`
 * [later](https://github.com/microsoft/TypeScript/issues/63540#issuecomment-4650789043) **RyanCavanaugh** said "Not sure how we'd possibly do this if even the API authors can't agree on what the ownership semantics are."

### [PR microsoft/TypeScript#63541](https://github.com/microsoft/TypeScript/pull/63541) (Closed, `For Backlog Bug`)

**Fix using declarations when Symbol is shadowed**

*Fix using and await using emit to reference the global Symbol constructor via globalThis when local Symbols shadow it*

 * (2 days ago) **typescript-bot** added labels `For Backlog Bug`, `For Backlog Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63541#issuecomment-4637418778) **xsourabhsharma** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/63541#issuecomment-4650819787) **RyanCavanaugh** said "This doesn't meet the 6.0 patch bar, see #62963. New development should generally happen in the typescript-go repo right now."
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63542](https://github.com/microsoft/TypeScript/pull/63542) (Closed, `For Backlog Bug`)

**fix jsx error location when empty JsxExpression precedes failing child**

*Skip empty JSX expressions when locating error nodes so type mismatches highlight the correct expression instead of comments.*

 * created by **harsha-cpp**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63542#issuecomment-4650816067) **RyanCavanaugh** said "This doesn't meet the 6.0 patch bar, see #62963. New development should generally happen in the typescript-go repo right now."
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63543](https://github.com/microsoft/TypeScript/pull/63543) (Closed, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Fix wildcard export target containment in auto\-imports**

*Apply containment validation to wildcard export targets in auto-imports to prevent out-of-package file enumeration*

 * created by **scarab-systems**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63543#issuecomment-4644002105) **scarab-systems** expressed agreement with microsoft-github-policy-service
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * [today](https://github.com/microsoft/TypeScript/pull/63543#issuecomment-4645878227) **scarab-systems** updated the PR to address review feedback, force-pushed an amended commit, reviewed changes, reran validation tests locally, and offered to make further adjustments
 * [later](https://github.com/microsoft/TypeScript/pull/63543#issuecomment-4650804019) **RyanCavanaugh** said "Thanks for the disclosures. Honestly, I'm not sure how to be more clear that this repo isn't accepting new dev contributions unless they meet the 6.0 critical patch bar. Any ideas?"

