# Report for 2026-07-08 (Wednesday, July 8th, 2026)

13 different users commented on 12 different issues.

## Recommended Actions

 * Response Recommended
    * @jonkoops opened a pull request fixing the documentation website in [microsoft/TypeScript#63330](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4924067216)
    * @ZuBB asked if their interpretation of the typescript aliasing snippet was correct in [microsoft/TypeScript#63601](https://github.com/microsoft/TypeScript/issues/63601#issuecomment-4916804847)
    * @igordanchenko provided detailed investigation and workaround for the tsc bin collision issue in [microsoft/TypeScript#63634](https://github.com/microsoft/TypeScript/issues/63634#issuecomment-4919175665)
    * @hyunbinseo asked about migration plans or interim configuration in [microsoft/TypeScript#63637](https://github.com/microsoft/TypeScript/issues/63637#issuecomment-4923612893)

## Activity Summary

### [Issue microsoft/TypeScript#10570](https://github.com/microsoft/TypeScript/issues/10570) (Open, `Suggestion`, `In Discussion`)

**Inherited typing for class property initializers**

*When a class property initializer is {} [] null or undefined, inherit its type from the base class*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/10570#issuecomment-1979034603) **aikhan** checked in after eight years and tagged RyanCavanaugh
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/10570#issuecomment-1979103178) **jonlepage** checked in after eight years, pinged RyanCavanaugh, and noted that they were in discussions
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/10570#issuecomment-2695740930) **xorweak** said "bump dump pump and dumppp"
 * [later](https://github.com/microsoft/TypeScript/issues/10570#issuecomment-4924034871) **jbjhjm** checked in to plan the 10-year issue anniversary party and said they would search for a workaround

### [Issue microsoft/TypeScript#63330](https://github.com/microsoft/TypeScript/issues/63330) (Open, `Docs`, **DanielRosenwasser**)

**\[V6\] \`module\` defaults is not \`esnext\`**

*TypeScript 6.0 incorrectly defaults the module option to ES2015 instead of ESNext, causing import attributes errors.*

 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4245384683) **mkantor** pointed out that the announcement post incorrectly stated that --outFile was removed in TypeScript 6.0 instead of deprecated and suggested it should reference 7.0
 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4491058453) **matthewbordas** reported seeing related compiler behavior issues, linked detailed notes, and noted that documentation defaults appear unsynchronized across core pages
 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4491128744) **mkantor** said "Yeah,  is in need of updates (perhaps other documentation pages too). See #63392."
 * [later](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4924067216) **jonkoops** opened a PR to update the documented default for module in tsconfigRules.ts to reflect current computation logic

### [Issue microsoft/TypeScript#63392](https://github.com/microsoft/TypeScript/issues/63392) (Open, `Docs`, **RyanCavanaugh**)

**Review/update https://typescriptlang\.org/tsconfig for TS 6\.0**

*The TypeScript tsconfig documentation is outdated for version 6.0, showing incorrect defaults and options for target, types, paths, rootDir, and module.*

 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4244991841) **RyanCavanaugh** said "I started this at https://github.com/RyanCavanaugh/schemastore/pull/1 but haven't had time to get it over the finish line. Feel free to doublecheck this; it's not fully vetted yet."
 * **RyanCavanaugh** assigned to **RyanCavanaugh**
 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4245971467) **mkantor** asked if the tsconfig descriptions need separate updates in the TypeScript-Website repository
 * [later](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4924067326) **jonkoops** opened two PRs on the TypeScript-Website repo to fix the module and moduleResolution defaults in tsconfigRules.ts

### [Issue microsoft/TypeScript#63601](https://github.com/microsoft/TypeScript/issues/63601) (Closed, `Needs Investigation`, **jakebailey**)

**@typescript/typescript6 does not have all versions that regular v6 branch has**

*The @typescript/typescript6 npm package lags behind the regular typescript v6 branch, missing versions like 6.0.3.*

 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **jakebailey**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63601#issuecomment-4894812442) **jakebailey** said "Why? The version you place there will have no impact on what version of TS your package manager selects to be reexported."
 * [today](https://github.com/microsoft/TypeScript/issues/63601#issuecomment-4916804847) **ZuBB** interpreted that the snippet caused imports of 'typescript' to resolve to version 6 by default, locking NestJS users to that version
 * [today](https://github.com/microsoft/TypeScript/issues/63601#issuecomment-4916820320) **jakebailey** said "But that has nothing to do the version of the shim package, which just depend on any v6?"
 * [today](https://github.com/microsoft/TypeScript/issues/63601#issuecomment-4916871012) **ZuBB** acknowledged that typescript6 is a proxy for the regular package and apologized for the confusion
 * (today) **ZuBB** closed the issue

### [Issue microsoft/TypeScript#63627](https://github.com/microsoft/TypeScript/issues/63627) (Open, `Needs Investigation`, **ahejlsberg**)

**\`NoInfer\` changes behavior for type matching on spread**

*Applying NoInfer to spread types unexpectedly produces type errors whereas equivalent spreads without NoInfer succeed*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63627#issuecomment-4909504855) **RyanCavanaugh** said "Why do you have NoInfer there either? e.g. what's a sample call that it fixes?"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63627#issuecomment-4909777910) **upsuper** explained that NoInfer allows a function to have fewer parameters than A and illustrated inference errors without it using a TypeScript example
 * **RyanCavanaugh** removed label `Not a Defect`
 * (later) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#63634](https://github.com/microsoft/TypeScript/issues/63634) (Closed)

**\`tsc\` incorrectly points to v6 rather than v7**

*Following the TypeScript 7 announcement’s alias instructions causes the tsc binary to default to version 6 instead of version 7.*

 * created by **abrahamguo**
 * [today](https://github.com/microsoft/TypeScript/issues/63634#issuecomment-4919175665) **igordanchenko** detailed the root cause of a conflicting tsc bin resolution between TypeScript 6 and 7 and provided a postinstall/prepare rebuild workaround
 * [today](https://github.com/microsoft/TypeScript/issues/63634#issuecomment-4919621853) **RyanCavanaugh** said "See https://github.com/microsoft/typescript-go/issues/4567#issuecomment-4919083741"
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63635](https://github.com/microsoft/TypeScript/issues/63635) (Closed, `Question`)

**Question: should \(type\) assertion functions be "if\-and\-only\-if" or just "only if"**

*Question whether TypeScript assertion functions using asserts can safely implement one-way type predicates without requiring their converse*

 * created by **kirkwaiblinger**
 * [today](https://github.com/microsoft/TypeScript/issues/63635#issuecomment-4919684518) **kirkwaiblinger** elaborated on the Node case by demonstrating how assertStrictEqual narrows types with example code, argued it belongs more to issue #15048 than to asserts semantics, and noted that typescript-eslint incorrectly flags a related corollary as unnecessary, linking to a playground
 * [today](https://github.com/microsoft/TypeScript/issues/63635#issuecomment-4919791837) **MartinJohns** said "Not a team member, but IMO assertion functions should behave the same as type predicates. Anything else would be confusing."
 * [today](https://github.com/microsoft/TypeScript/issues/63635#issuecomment-4920013911) **RyanCavanaugh** explained that assertion functions share predicate semantics, that assertIsLuckyNumber is not well-formed, and that assertStrictEqual’s signature can’t enforce its type checks
 * **RyanCavanaugh** added label `Question`
 * (today) **kirkwaiblinger** closed the issue

### [Issue microsoft/TypeScript#63636](https://github.com/microsoft/TypeScript/issues/63636) (Closed)

**Undocumented incompatibilities in TypeScript 7**

*TypeScript 7 introduced undocumented breaking changes that remove the typescript.sys export, causing typescript.sys to be undefined.*

 * created by **Vessel9817**
 * [today](https://github.com/microsoft/TypeScript/issues/63636#issuecomment-4921046408) **MartinJohns** provided documentation link and noted that TypeScript 7+ is written in Go and not directly usable in JavaScript projects
 * [later](https://github.com/microsoft/TypeScript/issues/63636#issuecomment-4923549862) **jakebailey** referenced a blog post stating that there is no API and provided the link
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63637](https://github.com/microsoft/TypeScript/issues/63637) (Closed, `Question`)

**v7 missing GitHub releases**

*TypeScript v7.0.2 is missing from the main repository's GitHub releases page and appears only under typescript-go.*

 * created by **hyunbinseo**
 * [later](https://github.com/microsoft/TypeScript/issues/63637#issuecomment-4923537904) **jakebailey** explained that the tag was in the other repository pending a codebase move and history replay, linking to the v7.0.2 release
 * [later](https://github.com/microsoft/TypeScript/issues/63637#issuecomment-4923612893) **hyunbinseo** asked about migration plans or interim package.json configuration
 * [later](https://github.com/microsoft/TypeScript/issues/63637#issuecomment-4923638845) **jakebailey** said "Bugs are fine to file here and that's the main place the project lives; is this causing a problem for you in some way?"
 * [later](https://github.com/microsoft/TypeScript/issues/63637#issuecomment-4923690763) **hyunbinseo** mentioned confusion about how to follow up with the v7 release and updated the issue body with a tl;dr section

### [PR microsoft/TypeScript#63638](https://github.com/microsoft/TypeScript/pull/63638) (Closed, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Fix inconsistent \`typeof this\` when \`this\` parameter comes from a contextual signature \(\#63616\)**

*TypeScript incorrectly resolves typeof this as the enclosing type instead of the contextual this in type queries.*

 * created by **AmariahAK**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63638#issuecomment-4924177988) **AmariahAK** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#63639](https://github.com/microsoft/TypeScript/issues/63639) (Closed, `Duplicate`)

**Consistent Typechecking Mode**

*Add a TypeScript compiler option enabling consistent typechecking by treating missing object keys as never or unknown.*

 * created by **p-98**
 * [later](https://github.com/microsoft/TypeScript/issues/63639#issuecomment-4925849782) **MartinJohns** said "Essentially you want #12936."
 * **RyanCavanaugh** added label `Duplicate`

