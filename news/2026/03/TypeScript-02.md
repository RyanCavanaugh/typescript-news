# Report for 2026-03-02 (Monday, March 2nd, 2026)

14 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @juhort asked why variance-based check only occurred one way in the F<T> example in [microsoft/TypeScript#62798](https://github.com/microsoft/TypeScript/issues/62798#issuecomment-3986082804)
    * @connorshea suggested feature parity with TS7 in [microsoft/TypeScript#63163](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3988138981)
    * @denis-migdal asked if the this[XXX] case could have more explicit messages in [microsoft/TypeScript#63206](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3990552026)
    * @denis-migdal asked if old opened issues are still watched by the team in [microsoft/TypeScript#63209](https://github.com/microsoft/TypeScript/issues/63209#issuecomment-3991951606)

## Activity Summary

### [Issue microsoft/TypeScript#62798](https://github.com/microsoft/TypeScript/issues/62798) (Open, `Bug`, `Help Wanted`, `Domain: check: Variance Relationships`, `Cursed?`)

**Conditional type eagerly calculated to be invariant breaks referential transparency**

*Eager evaluation of conditional type F<T> as invariant breaks referential transparency, making F<{}> extends F<{a:string}> yield false instead of true*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/62798#issuecomment-3574814438) **Andarist** said "I can only confirm that F is measured to be invariant here and that the other example ends up comparing different type aliases so it goes straight~ to the structural comparison."
 * **RyanCavanaugh** added label `Domain: check: Variance Relationships`
 * [today](https://github.com/microsoft/TypeScript/issues/62798#issuecomment-3986082804) **juhort** demonstrated that variance-based checks occurred both ways in the BoxOfIsSupertypeOfString example but only one way in the F<T> example

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3944591376) **HolgerJeromin** noted that the PR also deprecated --module=none and questioned whether it is less-used in the wild
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3959254158) **erictheswift** asked about updates on the RC/test build arrival and whether an existing dev build could be considered test-quality
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3962487549) **DanielRosenwasser** apologized for the delay, said the release candidate should arrive within a week, and mentioned that dev and nightly builds are available via npm and the VS Code Marketplace
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3987763468) **DanielRosenwasser** said "@typescript-bot sync release-6.0"
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3987763667) **typescript-bot** reported that sync release-6.0 jobs had started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3987771165) **typescript-bot** said "Hey, @DanielRosenwasser! I've pulled main into release-6.0 for you."
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3987821803) **DanielRosenwasser** said "@typescript-bot bump release-6.0"
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3987822011) **typescript-bot** posted an automated build status update for bump release-6.0
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3987851804) **typescript-bot** said "Hey, @DanielRosenwasser! I've set the version of release-6.0 to 6.0.1-rc for you."

### [Issue microsoft/TypeScript#63143](https://github.com/microsoft/TypeScript/issues/63143) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add switch to disable \_var unused variable prevention**

*Add a tsconfig option to disable automatic ignoring of underscore-prefixed unused variables so the compiler still reports them to IDE.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3953666515) **ackvf** explained their confusion about eslint unused-variable settings and justified making IDE prefix handling configurable
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3957255323) **guillaumebrunerie** explained that TypeScript errors and ESLint warnings both appear and suggested disabling noUnusedLocals and noUnusedParameters to rely solely on ESLint for consistent styling
 * [today](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3983613552) **ackvf** asked how to configure the IDE to always dim unused variables regardless of disabled extensions or suppressed rules
 * [today](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3986970398) **RyanCavanaugh** explained that the behavior had existed for a long time and that there was little appetite for changing it because it suited the vast majority of users

### [PR microsoft/TypeScript#63156](https://github.com/microsoft/TypeScript/pull/63156) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update dependencies**

*Update dependencies to the latest ESLint version, remove eslint-autolinkable-stylish, and address some audit issues.*

 * (1 week ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63163](https://github.com/microsoft/TypeScript/pull/63163) (Closed, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Port anyFunctionType subtype fix and JSX children NonInferrableType propagation from typescript\-go**

*Port fixes from typescript-go to make anyFunctionType a proper function subtype and correctly propagate NonInferrableType for JSX children.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3936667089) **jakebailey** fixed DT and requested the typescript-bot to run dt
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3936667361) **typescript-bot** reported dt jobs start and completion status with result links
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3936759174) **typescript-bot** notified that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3988138981) **connorshea** said "Since I saw a ts6 rc may go out soon, figured I'd comment and note this would be good to have for parity with TS7 🙏 "
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3988146507) **jakebailey** said "Oops, this was meant to be merged "
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3988148952) **DanielRosenwasser** said "@typescript-bot cherry-pick this to release-6.0 and LKG"
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3988149337) **typescript-bot** updated CI job status for cherry-pick to release-6.0 and LKG
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3988154678) **connorshea** apologized for the misdirected comment and thanked the contributor for their work
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3988175602) **typescript-bot** said "Hey, @DanielRosenwasser! I've created #63208 for you."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#63172](https://github.com/microsoft/TypeScript/pull/63172) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Deprecate assert in import\(\)**

*Deprecate use of assert within dynamic import() calls due to its runtime interpretation, which was overlooked in #63077.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63172#issuecomment-3937632278) **DanielRosenwasser** said "We don't have a test with { assert: { type: json } }???"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63172#issuecomment-3937830272) **DanielRosenwasser** said "I assume we have tests for runtime import() calls as well."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63201](https://github.com/microsoft/TypeScript/pull/63201) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Revert "discrete pluralizer for lib\.esnext\.temporal unit unions"**

*Revert the discrete pluralizer addition for lib.esnext.temporal unit unions in TypeScript*

 * (3 days ago) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63201#issuecomment-3982486366) **justingrant** explained the rationale for accepting both singular and plural unit strings in certain Temporal API methods and for using a wrapper type in TypeScript definitions to improve IntelliSense
 * [today](https://github.com/microsoft/TypeScript/pull/63201#issuecomment-3986033596) **DanielRosenwasser** asked how common and easy it would be for APIs interfacing with Temporal to remember to reference the helper type
 * [today](https://github.com/microsoft/TypeScript/pull/63201#issuecomment-3986481893) **justingrant** described ideal TypeScript behavior for hiding deprecated types in IntelliSense, recalled deprecated plural values cluttering suggestions, proposed hiding deprecated options by default to improve DX, assessed that requiring a helper type is likely acceptable based on 5+ years of polyfill usage, and asked if there was a specific future-compatibility concern
 * [today](https://github.com/microsoft/TypeScript/pull/63201#issuecomment-3987134549) **DanielRosenwasser** mentioned that other APIs could accept `TimeUnit` and get everything working, but they’d often prefer it to be singular
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63202](https://github.com/microsoft/TypeScript/pull/63202) (Closed, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump minimatch from 3\.1\.2 to 3\.1\.5**

*Upgrade the minimatch dependency from version 3.1.2 to 3.1.5 to include ReDoS warnings, performance improvements, and bug fixes.*

 * **dependabot[bot]** added label `javascript`
 * (3 days ago) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63202#issuecomment-3987757347) **jakebailey** said "@dependabot recreate"
 * [today](https://github.com/microsoft/TypeScript/pull/63202#issuecomment-3987761497) **dependabot[bot]** said "Looks like minimatch is up-to-date now, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript#63203](https://github.com/microsoft/TypeScript/issues/63203) (Open, `Suggestion`, `Awaiting More Feedback`)

**Narrow a ternary expression to unique symbol type**

*Enable TypeScript to infer a unique symbol type from a ternary expression whose runtime result is constant.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-3977064991) **guillaumebrunerie** asked whether libraries depending on global state might break during Vite development and whether this is a Vite bug or a misunderstanding
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-3977083251) **mitar** explained that Vite optimized imports during development by duplicating and bundling them together, causing symbol identity mismatches when the same module was imported via different absolute or relative paths
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-3979903350) **mkantor** suggested using Symbol.for("none") unconditionally and asked if memory cost was a concern, then proposed a workaround switching symbols based on NODE_ENV
 * [today](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-3986114155) **RyanCavanaugh** explained that unique symbols are supposed to be unique but might not be when using Symbol.for and recommended using a cast
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-3986157126) **mitar** stated that exporting two unique symbols with Symbol.for or Symbol() did not produce errors, contradicting the earlier example that errors occur without a ternary expression

### [PR microsoft/TypeScript#63204](https://github.com/microsoft/TypeScript/pull/63204) (Closed, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump fast\-xml\-parser from 5\.3\.2 to 5\.3\.8**

*Upgrade fast-xml-parser dependency from v5.3.2 to v5.3.8 incorporating improved entity security, performance, XML builder support, and CJS typing fixes.*

 * (2 days ago) **dependabot[bot]** added labels `dependencies`, `javascript`
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63204#issuecomment-3986741829) **dependabot[bot]** said "Looks like fast-xml-parser is up-to-date now, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript#63205](https://github.com/microsoft/TypeScript/pull/63205) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Bump the github-actions group in the repository root by upgrading actions/upload-artifact to v7.0.0 and updating github/codeql-action.*

 * (yesterday) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63206](https://github.com/microsoft/TypeScript/issues/63206) (Open, `Bug`, `Help Wanted`, `Domain: Error Messages`)

**Confusing error message \(2322\), should use \(2741\) and \(2322\) error message when this\["XXX"\] = {\.\.\.} has a missing \(or mispelled\) key or an incompatible value\.**

*Improve TypeScript error messaging for this['XXX'] assignments by distinguishing missing property errors (2741) from type mismatches (2322).*

 * created by **denis-migdal**
 * [today](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3986762561) **nmain** explained that replacing this["faa"] with A["faa"] fixes the issue when not subclassing and clarified that subclassing leads to unresolved generic constraints so the errors are valid
 * [today](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3988965071) **denis-migdal** challenged the assertion that the TypeScript compiler cannot detect missing or incompatible object keys, provided examples demonstrating error detection, and discussed subclassing and input/output property distinctions
 * [today](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3989002108) **denis-migdal** demonstrated that TS handles this['faa'] changes in subclasses with example code
 * [today](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3989154726) **MartinJohns** demonstrated that subclasses could add properties and provide more specific types with a TypeScript example
 * [today](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3989336812) **denis-migdal** analyzed subclass property assignment under TS error 2322 and argued that no error should be raised
 * [later](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3990439265) **MartinJohns** explained that accepting 'this.foo' assignments is an intentional unsoundness in TypeScript's type system and clarified that type assertions serve as escape hatches for this limitation
 * [later](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3990552026) **denis-migdal** observed TS's differing treatment of the `this[XXX]` and generic cases and asked if the `this[XXX]` case could have more explicit messages

### [Issue microsoft/TypeScript#63207](https://github.com/microsoft/TypeScript/issues/63207) (Open)

**tsserver hangs indefinitely when inferring return type of class method that passes this to a function with deeply nested conditional return type**

*tsserver hangs when inferring a class method’s return type using remeda.pick without an explicit annotation due to circular type inference*

 * created by **kkirby**

### [PR microsoft/TypeScript#63208](https://github.com/microsoft/TypeScript/pull/63208) (Closed, **DanielRosenwasser**)

**🤖 Pick PR \#63163 \(Port anyFunctionType subtype fix an\.\.\.\) into release\-6\.0**

*Cherry-pick PR #63163, porting the anyFunctionType subtype fix, into the release-6.0 branch.*

 * created by **typescript-bot**
 * **typescript-bot** assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript#63209](https://github.com/microsoft/TypeScript/issues/63209) (Closed)

**Enable \`declare public readonly\` \+ \`protected\` declaration merge in classes**

*Enable `declare public readonly` + `protected` declaration merge in classes*

 * created by **denis-migdal**
 * [later](https://github.com/microsoft/TypeScript/issues/63209#issuecomment-3991896628) **MartinJohns** disputed mention of opening new issues for triage and noted duplicates remained open
 * [later](https://github.com/microsoft/TypeScript/issues/63209#issuecomment-3991951606) **denis-migdal** stated not having seen any mention of requiring new issues for triage, noted possibly seeing a pinned issue by Ryan, and asked if old open issues are still watched by the team

### [Issue microsoft/TypeScript#63210](https://github.com/microsoft/TypeScript/issues/63210) (Open, `Needs More Info`)

**6\.0\.20260301 Causing general instability and hanging operations**

*Updating to extension version 6.0.20260301 causes indefinite tsconfig initialization, hung TS Server commands, and file renaming failures in VS Code.*

 * created by **netjordanlee**

