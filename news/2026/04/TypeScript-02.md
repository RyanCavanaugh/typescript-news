# Report for 2026-04-02 (Thursday, April 2nd, 2026)

13 different users commented on 52 different issues.

## Recommended Actions

 * Response Recommended
    * @james-pre provided a patch for v6.0.2 in [microsoft/TypeScript#63008](https://github.com/microsoft/TypeScript/pull/63008#issuecomment-4180765961)
    * @TomStrepsil asked whether they should re-raise the issue at microsoft/typescript-go in [microsoft/TypeScript#63281](https://github.com/microsoft/TypeScript/issues/63281#issuecomment-4182597488)
    * @D2758695161 claimed the issue and is working on a PR in [microsoft/TypeScript#63325](https://github.com/microsoft/TypeScript/issues/63325#issuecomment-4180655477)
    * @bwalter007 asked if a maintainer could run baseline-accept or advise on local configuration in [microsoft/TypeScript#63344](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4180919755)
    * @bwalter007 asked if something was missing in the local setup after encountering ENOENT during npm test in [microsoft/TypeScript#63344](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4180995565)
    * @microsoft-github-policy-service requested CLA agreement in [microsoft/TypeScript#63344](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4183215229)

## Activity Summary

### [Issue microsoft/TypeScript#60591](https://github.com/microsoft/TypeScript/issues/60591) (Closed, `Bug`, `Help Wanted`, `Domain: Declaration Emit`)

**JSDoc implements with imported types**

*JSDoc @implements of an imported type in JS causes a private name error during declaration emit, unlike TypeScript files.*

 * (1.3 years ago) **RyanCavanaugh** added label `Domain: Declaration Emit`, and set milestone to `Backlog`
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/60591#issuecomment-4158335455) **apendua** said "FYI, it looks like this issue is now resolved in typescript-go."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63008](https://github.com/microsoft/TypeScript/pull/63008) (Closed, `For Uncommitted Bug`)

**Add support for importing JSON modules "as const"**

*Add opt-in importJsonAsConst compiler option to import JSON modules with 'as const' literal typing.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/63008#issuecomment-3765756808) **james-pre** provided a patch to backport the feature to Typescript v5.9.3
 * (1 week ago) **typescript-bot** closed the issue
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63008#issuecomment-4121468891) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates
 * [today](https://github.com/microsoft/TypeScript/pull/63008#issuecomment-4180765961) **james-pre** said "Patch for v6.0.2: typescript+6.0.2.patch"

### [Issue microsoft/TypeScript#63281](https://github.com/microsoft/TypeScript/issues/63281) (Open, `Suggestion`, `Awaiting More Feedback`)

**RegExpIndicesArray \- Named group indices can be undefined**

*TypeScript’s RegExpIndicesArray incorrectly assumes named regex group index arrays are always defined, missing errors for undefined groups.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63281#issuecomment-4113654374) **TomStrepsil** clarified that strong key typing for named capture groups is a larger change and unrelated to the undefined value issue
 * (1 week ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [later](https://github.com/microsoft/TypeScript/issues/63281#issuecomment-4182597488) **TomStrepsil** questioned whether their fix qualified under the contribution guide, asked if they should re-raise the issue in microsoft/typescript-go, and suggested adding | undefined for a quick win

### [Issue microsoft/TypeScript#63325](https://github.com/microsoft/TypeScript/issues/63325) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**\`lib\.dom\.d\.ts\`: Keyframe interface should allow CSS Typed Object Model objects like CSSTransformValue, etc**

*The Keyframe interface in lib.dom.d.ts should accept CSS Typed Object Model types such as CSSTransformValue.*

 * (2 days ago) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, `Domain: lib.d.ts`
 * [today](https://github.com/microsoft/TypeScript/issues/63325#issuecomment-4180655477) **D2758695161** claimed the issue and proposed updating the Keyframe interface in lib.dom.d.ts to accept CSS Typed OM objects and stated work on a PR

### [PR microsoft/TypeScript#63328](https://github.com/microsoft/TypeScript/pull/63328) (Closed)

**Backport tsgo PR 3301 for testing**

*Backport TypeScript-Go pull request 3301 to evaluate its performance.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4164657534) **typescript-bot** provided the requested performance run results in a detailed table
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4164789350) **typescript-bot** reported build results for the top 400 repos comparing main with the pull request, highlighted new TS2722 and TS2349 errors in Inquirer.js, and asked for review
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4165397001) **RyanCavanaugh** provided a reduced TypeScript example from the repository demonstrating the issue
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63332](https://github.com/microsoft/TypeScript/issues/63332) (Open, `Duplicate`)

**instanceof narrowing should respect type parameter bounds for covariant types**

*TypeScript’s instanceof narrowing of generic covariant classes defaults type parameters to any instead of their bounded unions*

 * created by **ethanresnick**
 * [today](https://github.com/microsoft/TypeScript/issues/63332#issuecomment-4179453589) **MartinJohns** said "Duplicate of #17473."
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#63333](https://github.com/microsoft/TypeScript/issues/63333) (Open, `Duplicate`)

**JSON\.stringify should disallow BigInt value**

*Restrict JSON.stringify’s parameter type to disallow BigInt values and prevent runtime errors.*

 * created by **wyattscarpenter**
 * [today](https://github.com/microsoft/TypeScript/issues/63333#issuecomment-4176413347) **nmain** inquired what type the argument to JSON.stringify would have and referenced issues #1897 and #4196
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#63334](https://github.com/microsoft/TypeScript/issues/63334) (Open)

**Playground typing issue**

*Importing from @octokit/core/types in the TypeScript Playground results in any types and stale diagnostic errors.*

 * created by **BrandonStudio**
 * [today](https://github.com/microsoft/TypeScript/issues/63334#issuecomment-4179530261) **RyanCavanaugh** listed similar issues in an auto-generated analysis

### [Issue microsoft/TypeScript#63339](https://github.com/microsoft/TypeScript/issues/63339) (Closed)

**"Find All References" does not show all sources when the same property is contributed by multiple \`declare module\` augmentations**

*Find All References only lists the first declare module augmentation for a merged interface property, omitting additional declarations.*

 * created by **GuichiZhao**
 * [today](https://github.com/microsoft/TypeScript/issues/63339#issuecomment-4176716230) **GuichiZhao** traced through the TypeScript source, identified that definitionToReferencedSymbolDefinitionInfo used firstOrUndefined to drop merged declarations, and suggested iterating over symbol.declarations to include all declaration sites
 * [today](https://github.com/microsoft/TypeScript/issues/63339#issuecomment-4178882796) **RyanCavanaugh** said "See https://github.com/microsoft/TypeScript/issues/62827, we are not making further changes to the TS 6 language service."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63340](https://github.com/microsoft/TypeScript/issues/63340) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Redundant leading apostrophe in the ts1344 diagnostic**

*TypeScript diagnostic ts1344 incorrectly includes a redundant leading apostrophe in its error message.*

 * created by **JLHwung**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63341](https://github.com/microsoft/TypeScript/pull/63341) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix redundant leading apostrophe in TS1344 diagnostic message**

*Remove the redundant leading apostrophe in the TS1344 diagnostic message and update baseline tests accordingly*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/63341#issuecomment-4179103357) **Copilot** reverted all changes under /src/loc and stored a memory to never edit those files in future PRs
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63342](https://github.com/microsoft/TypeScript/issues/63342) (Open)

**type checking complexity with multiple template literals in unions**

*TypeScript’s type checking time scales exponentially with unions of template literal types in dynamic route definitions.*

 * created by **eps1lon**
 * [today](https://github.com/microsoft/TypeScript/issues/63342#issuecomment-4180241279) **jakebailey** said "I'm pretty sure I tried this (no pun intended) in https://github.com/microsoft/TypeScript/pull/59759"
 * [today](https://github.com/microsoft/TypeScript/issues/63342#issuecomment-4180398717) **eps1lon** asked what the conclusion was after discussions fizzled over memory concerns and offered to investigate the benchmarks further
 * [today](https://github.com/microsoft/TypeScript/issues/63342#issuecomment-4180447400) **jakebailey** said "The conclusion was "we didn't come to a conclusion before this codebase became closed to new PRs": https://github.com/microsoft/TypeScript#contribute"

### [PR microsoft/TypeScript#63343](https://github.com/microsoft/TypeScript/pull/63343) (Open)

**Use trie for removeStringLiteralsMatchedByTemplateLiterals**

*Optimize removeStringLiteralsMatchedByTemplateLiterals by building a prefix trie for efficient template literal matching*

 * created by **eps1lon**
 * [today](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4180238308) **jakebailey** said "Is this different than https://github.com/microsoft/TypeScript/pull/59759?"
 * [today](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4180269841) **eps1lon** said "Looks like the same at a glance. Yours is already doing some size estimation it seems. I haven't accounted for opting out of trie-based search for small types."

### [PR microsoft/TypeScript#63344](https://github.com/microsoft/TypeScript/pull/63344) (Open)

**Document charCodeAt edge case behavior in first line**

*Update charCodeAt JSDoc to mention NaN return edge case in the main description line.*

 * created by **bwalter007**
 * [today](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4180847265) **RyanCavanaugh** said "You need to run hereby runtests-parallel then hereby baseline-accept then commit that diff"
 * [today](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4180919755) **bwalter007** asked for maintainer to run baseline-accept or advise on local test configuration
 * [today](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4180926787) **jakebailey** said "Just do npm test, it'll do everything for you in the right order."
 * [today](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4180995565) **bwalter007** reported that running npm test still yielded an ENOENT error before tests ran and asked if something was missing in the local setup
 * [today](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4181033803) **RyanCavanaugh** said "I don't know what's going on; never heard of this happening before. Even after running git clean -xdf, npm ci + npm test is sufficient on my machine."
 * [later](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4183215229) **microsoft-github-policy-service[bot]** requested the contributor to agree to the CLA by replying with the appropriate command and company information

### [PR microsoft/TypeScript#63345](https://github.com/microsoft/TypeScript/pull/63345) (Closed)

**fix\(lib\.dom\.d\.ts\): Keyframe interface supports CSS Typed OM objects**

*Add CSSStyleValue support to TypeScript's lib.dom.d.ts keyframe interfaces to enable CSS Typed OM objects in animations.*

 * created by **D2758695161**
 * [today](https://github.com/microsoft/TypeScript/pull/63345#issuecomment-4180804123) **jakebailey** said "you added a 45k long file, which is certainly wrong, and even so, these types are not handwritten, they are generated in https://github.com/microsoft/TypeScript-DOM-lib-generator."
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63345#issuecomment-4180805728) **RyanCavanaugh** said "Your bot is lost"

### [Issue microsoft/TypeScript#63346](https://github.com/microsoft/TypeScript/issues/63346) (Open)

**Experimental \(deprecated\) decorators are included by default**

*The ESNext library includes legacy experimental decorator types by default, causing conflicts with new decorator definitions.*

 * created by **OldStarchy**

### [Issue microsoft/TypeScript#63347](https://github.com/microsoft/TypeScript/issues/63347) (Open)

**Minor performance issue when using HTMLElementTagNameMap**

*TypeScript 6.0’s overload resolution for HTMLElementTagNameMap has regressed, causing slower type-checking and minor performance issues on Linux*

 * created by **jasonlyu123**

### [Issue microsoft/TypeScript#63348](https://github.com/microsoft/TypeScript/issues/63348) (Open)

**Inference is not working properly**

*TypeScript fails to infer the path generic type in useStoreByPath from its string argument.*

 * created by **eduardocque**

