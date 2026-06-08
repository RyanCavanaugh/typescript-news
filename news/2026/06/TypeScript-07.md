# Report for 2026-06-07 (Sunday, June 7th, 2026)

3 different users commented on 23 different issues.

## Recommended Actions

 * Response Recommended
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

### [Issue microsoft/TypeScript#63531](https://github.com/microsoft/TypeScript/issues/63531) (Closed, `Help Wanted`, `Docs`)

**Markdown heading level bug in Narrowing documentation**

*The 'Truthiness narrowing' heading in the TypeScript Narrowing documentation is formatted as H1 instead of H2, causing subsequent sections to be incorrectly nested under it in the table of contents.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63531#issuecomment-4625038495) **RyanCavanaugh** said "Weird, the accessibility scan is supposed to yell at us when this happens"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63531#issuecomment-4630156658) **MannXo** said "I'll take this if no one's working on it yet."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63531#issuecomment-4630477675) **MartinJohns** said "@MannXo There are already open PR to address this issue. Generally, the TypeScript team does not assign issues to users. You're free to just work on issues labelled as "Help wanted" and issue PRs."
 * (later) **mzleman** closed the issue

### [PR microsoft/TypeScript#63543](https://github.com/microsoft/TypeScript/pull/63543) (Open, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Fix wildcard export target containment in auto\-imports**

*Apply containment validation to wildcard export targets in auto-imports to prevent out-of-package file enumeration*

 * created by **scarab-systems**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63543#issuecomment-4644002105) **scarab-systems** expressed agreement with microsoft-github-policy-service
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * [today](https://github.com/microsoft/TypeScript/pull/63543#issuecomment-4645878227) **scarab-systems** updated the PR to address review feedback, force-pushed an amended commit, reviewed changes, reran validation tests locally, and offered to make further adjustments

