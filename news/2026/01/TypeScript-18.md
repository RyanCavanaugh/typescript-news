# Report for 2026-01-18 (Sunday, January 18th, 2026)

8 different users commented on 15 different issues.

## Recommended Actions

 * Response Recommended
    * @devanshj asked for feedback on the PR in [microsoft/TypeScript#14466](https://github.com/microsoft/TypeScript/issues/14466#issuecomment-3768593626)
    * @james-pre provided a workaround patch for TS v5.9.3 in [microsoft/TypeScript#32063](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-3765755361)
    * @janhesters reported a recurrence of the crash and provided reproduction setup in [microsoft/TypeScript#61524](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-3765704531)
    * @james-pre provided a patch to enable the feature on v5.9.3 in [microsoft/TypeScript#63008](https://github.com/microsoft/TypeScript/pull/63008#issuecomment-3765756808)

## Activity Summary

### [Issue microsoft/TypeScript#14466](https://github.com/microsoft/TypeScript/issues/14466) (Open, `Suggestion`, `In Discussion`)

**Existential type?**

*Add existential type parameters in TypeScript definitions to avoid propagating generics for Binding and Scheduler constructors.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/14466#issuecomment-2509495772) **HansBrende** described how existential types could enable a typesafe Integer type in TypeScript
 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/14466#issuecomment-3194192650) **barasztamas** presented a common TypeScript use case example and expressed reluctance to use advanced TS solutions
 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/14466#issuecomment-3194224590) **MoritzR** suggested using a simpler function type returning Promise<void> and explained how to handle intermediate null values
 * [later](https://github.com/microsoft/TypeScript/issues/14466#issuecomment-3768593626) **devanshj** offered a PR for experimenting with existential types, showed screenshots of its behavior on two comments, and welcomed feedback

### [Issue microsoft/TypeScript#32063](https://github.com/microsoft/TypeScript/issues/32063) (Open, `Suggestion`, `Awaiting More Feedback`)

**import ConstJson from '\./config\.json' as const;**

*Allow importing a JSON config file with a const modifier to infer literal union types for its values.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-3320534310) **thw0rted** described an approach using class-validator and class-validator-jsonschema to generate shared type declarations, use the decorated class for runtime validation, and compile JSON schemas for distribution and validation with ajv
 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-3320861920) **TechQuery** suggested using decorated classes for front-end data validation with Decorator stage-2 or a future Parameter Decorator proposal and referenced their MobX-RESTful library
 * [yesterday](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-3764534135) **james-pre** implemented the feature in the TS compiler and opened a Go compiler pull request
 * [today](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-3765755361) **james-pre** shared a patch for TS v5.9.3 that applies the feature from #63008 via patch-package, corrected gist metadata, and noted tsc works but VS Code intellisense is broken

### [Issue microsoft/TypeScript#61524](https://github.com/microsoft/TypeScript/issues/61524) (Open, `Bug`, `Help Wanted`, `Domain: check: Variance Relationships`, `Fix Available`)

**Error: Debug Failure\. No error for last overload signature**

*TypeScript nightly v5.9.0-dev crashes with "Debug Failure. No error for last overload signature" during overload resolution in a generic function.*

 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-2780342066) **Andarist** described that relateVariances behaves differently on reportErrors leading to inconsistent results and noted that PR #55222 would fix it
 * **RyanCavanaugh** added label `Domain: Variance Relationships`
 * **typescript-bot** added label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-3765704531) **janhesters** reported seeing the Debug Failure crash on TypeScript 5.9.3 in a project with heavy generated types and provided detailed reproduction steps

### [PR microsoft/TypeScript#62918](https://github.com/microsoft/TypeScript/pull/62918) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.31\.8 to 4\.31\.9 in the github\-actions group**

*Bump github/codeql-action in the GitHub Actions group from v4.31.8 to v4.31.9 with no user-facing changes.*

 * (1 month ago) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62918#issuecomment-3765988918) **dependabot[bot]** said "Looks like github/codeql-action is updatable in another way, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript#63008](https://github.com/microsoft/TypeScript/pull/63008) (Open, `For Uncommitted Bug`)

**Add support for importing JSON modules "as const"**

*Add opt-in importJsonAsConst compiler option to import JSON modules with 'as const' literal typing.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63008#issuecomment-3764855551) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #32063. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63008#issuecomment-3764855552) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #32063. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63008#issuecomment-3764872636) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/63008#issuecomment-3765756808) **james-pre** provided a patch to backport the feature to Typescript v5.9.3

### [Issue microsoft/TypeScript#63011](https://github.com/microsoft/TypeScript/issues/63011) (Closed)

**\> Nic nie ciekawi mnie bardziej niż zimna myszka\.**

*User remarks that nothing interests them more than a cold mouse.*

 * created by **mekrix777mekort-ops**

### [Issue microsoft/TypeScript#63012](https://github.com/microsoft/TypeScript/issues/63012) (Closed)

**Type Narrowing in Discriminated Unions**

*Extend TypeScript control flow analysis to narrow destructured discriminated union types based on non-discriminant properties.*

 * created by **GermanJablo**
 * [today](https://github.com/microsoft/TypeScript/issues/63012#issuecomment-3766083042) **MartinJohns** pointed out that checking `!data` can mis-narrow types when `data` is falsy (e.g., an empty string)
 * [later](https://github.com/microsoft/TypeScript/issues/63012#issuecomment-3767454772) **GermanJablo** said "I can’t believe I didn’t catch that! Thanks!"
 * (later) **GermanJablo** closed the issue

### [PR microsoft/TypeScript#63013](https://github.com/microsoft/TypeScript/pull/63013) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 3 updates**

*Bump actions/setup-node to v6.2.0 and update actions/cache and github/codeql-action in the root directory*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63014](https://github.com/microsoft/TypeScript/pull/63014) (Open, `For Backlog Bug`)

**Fixes crash when inferring constrained variadic tuple types when source has insufficient fixed elements**

*A compiler crash occurs when inferring constrained variadic tuple types from a source tuple with insufficient fixed elements.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`

