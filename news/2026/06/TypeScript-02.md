# Report for 2026-06-02 (Tuesday, June 2nd, 2026)

7 different users commented on 33 different issues.

## Recommended Actions

 * Response Recommended
    * @umenosuke reported a potential bug where the compiler accepted incorrect types via index signatures under strict mode in [microsoft/TypeScript#27144](https://github.com/microsoft/TypeScript/issues/27144#issuecomment-4614095827)

## Activity Summary

### [Issue microsoft/TypeScript#27144](https://github.com/microsoft/TypeScript/issues/27144) (Open, `Bug`, `Domain: Index Types`)

**Index signature is assignable to weak type whose properties don't match the signature type**

*TypeScript allows assigning a string-indexed number type to an interface with an optional string property without error.*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/27144#issuecomment-2487564210) **umenosuke** reported having trouble and provided a playground link
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/27144#issuecomment-2825552889) **jthemphill** explained that all file properties being optional means any object matches the type and suggested making size non-optional, providing a playground link
 * **RyanCavanaugh** added label `Domain: Index Types`
 * [later](https://github.com/microsoft/TypeScript/issues/27144#issuecomment-4614095827) **umenosuke** demonstrated that boolean values were accepted for an optional string property via an index signature without strict mode errors

### [Issue microsoft/TypeScript#63498](https://github.com/microsoft/TypeScript/issues/63498) (Open, `Needs Investigation`)

**\`js/ts\.preferences\.autoImportFileExcludePatterns\` is not reflected promptly in IntelliSense suggestions**

*Changes to js/ts.preferences.autoImportFileExcludePatterns are not promptly reflected in IntelliSense import suggestions*

 * created by **heroboy**
 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/63498#issuecomment-4612318584) **jakebailey** said "This is more or less mooted by the new language server, no? I don't think we have this problem there."

### [PR microsoft/TypeScript#63502](https://github.com/microsoft/TypeScript/pull/63502) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 6 updates**

*Update six GitHub Actions in the repository root to their latest patch and minor versions.*

 * (1 week ago) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63502#issuecomment-4605737454) **dependabot[bot]** said "Looks like these dependencies are updatable in another way, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript#63514](https://github.com/microsoft/TypeScript/issues/63514) (Closed, `Not a Defect`)

**Reassigning of inferred \`object\` with Indexed access value does not widen it's type**

*Reassigning an inferred object via indexed access in TypeScript fails to widen its type beyond object.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4575968627) **nmain** said "https://typescript-eslint.io/rules/no-unsafe-member-access/ handles an any indexer but not a never indexer."
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4577327383) **svenvandescheur** explained that never is a valid keyof and that any opts out of type checks, referenced related issues, and noted that defaulting to any and never feels counterintuitive versus using unknown or treating never as a noop
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4577403452) **nmain** explained that the `never` type contains no values, thus satisfies all predicates, and that asserting a value as `never` implies unreachable code
 * [today](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4605191004) **RyanCavanaugh** explained that never must always be a valid keyof object using logical arguments
 * **RyanCavanaugh** added label `Not a Defect`

### [Issue microsoft/TypeScript#63522](https://github.com/microsoft/TypeScript/issues/63522) (Open, `Bug`, `Domain: JS Emit`)

**Declarations that shadow global \`Symbol\`  break emit for \`using\` declarations**

*Declaring a local Symbol class that shadows the global Symbol breaks using declaration emissions and leads to runtime Symbol.dispose errors.*

 * created by **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63522#issuecomment-4592215906) **nmain** said "Similar to https://github.com/microsoft/TypeScript/issues/61150."
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: JS Emit`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63523](https://github.com/microsoft/TypeScript/issues/63523) (Closed, `Working as Intended`)

**tsc may fail to report error when \`file\.js\` & \`file\.d\.ts\` coexist, even when \`@ts\-check\` is added on \`file\.js\`\.**

*After TypeScript 4.5 update, JavaScript files with @ts-check ignore errors if a corresponding .d.ts file is present.*

 * created by **hkleungai**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63523#issuecomment-4591680219) **MartinJohns** explained that .d.ts files took priority over .js files and suggested enabling --skipLibCheck or generating .d.ts from .js
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63523#issuecomment-4592123266) **hkleungai** noted skipLibCheck was enabled but the bug persisted, questioned that .d.ts files took priority over .js files, and suggested documentation clarification, highlighting a tsc ordering inconsistency
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63523#issuecomment-4605129005) **RyanCavanaugh** noted that automatically ingesting both would cause duplicate identifier errors and suggested it was a configuration error

### [PR microsoft/TypeScript#63525](https://github.com/microsoft/TypeScript/pull/63525) (Closed, `For Uncommitted Bug`)

**Fix JSDoc grammar typo: 'returns a undefined' → 'returns undefined'**

*Grammar typo corrected in JSDoc for SymbolConstructor.keyFor by changing '@returns a undefined' to '@returns undefined'*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63525#issuecomment-4599055168) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63525#issuecomment-4599055185) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63525#issuecomment-4599055199) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **RyanCavanaugh** closed the issue
 * (today) **RyanCavanaugh** reopened the issue

### [PR microsoft/TypeScript#63526](https://github.com/microsoft/TypeScript/pull/63526) (Closed, `For Backlog Bug`)

**Allow element access on enum as computed property name in type literal**

*Permit using enum members with non-identifier names as computed property keys in type literals by treating bracket access expressions as late-bindable.*

 * created by **driphtyio**
 * (yesterday) **typescript-bot** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63526#issuecomment-4605326192) **RyanCavanaugh** said "This doesn't meet the 6.0 patch bar https://github.com/microsoft/TypeScript/issues/62963#issuecomment-4100336368"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63527](https://github.com/microsoft/TypeScript/issues/63527) (Closed, `Needs Investigation`, **ahejlsberg**)

**\`erasableSyntaxOnly\` should error on unerasable \`as\`/\`satisfies\`**

*ErasableSyntaxOnly should report errors for as or satisfies expressions that cannot be safely removed.*

 * [today](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4602727661) **ritschwumm** expressed surprise at the `as` operator precedence and wondered where it was documented
 * [today](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4603029422) **snarbles2** mentioned inability to find documentation for the `as` operator precedence and asked whether “erasable syntax only” implies “blankable” or if that was merely assumed
 * [today](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4603595943) **acutmore** questioned whether “erasable syntax only” implies “blankable” and referenced a precedent banning old `<Type>val` assertion syntax with an example illustrating the need for parentheses
 * [today](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4605100332) **RyanCavanaugh** questioned whether erasable syntax only implied blankability and noted that blanking-only was a retrospective outcome rather than an initial design goal for ESO
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4606483396) **RyanCavanaugh** summarized key takeaways about erasableSyntaxOnly, questioned shipped precedence rules, and proposed testing top1000 code to determine if a precedence error could be introduced in TS 7.0

### [PR microsoft/TypeScript#63528](https://github.com/microsoft/TypeScript/pull/63528) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Delete browser\-integration job from ci\.yml**

*Remove browser-integration job from CI workflow due to persistent external failures and discontinue its maintenance*

 * created by **RyanCavanaugh**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63529](https://github.com/microsoft/TypeScript/pull/63529) (Open, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 7 updates**

*Bump seven GitHub Actions dependencies in the root directory to their latest versions.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63530](https://github.com/microsoft/TypeScript/pull/63530) (Closed, `For Uncommitted Bug`)

**Fix typo in es5\.d\.ts JSDoc: 'paramater' \-\> 'parameter'**

*A typo in the Array.prototype.splice JSDoc comment in src/lib/es5.d.ts is corrected from 'paramater' to 'parameter'.*

 * created by **driphtyio**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63530#issuecomment-4607074332) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63530#issuecomment-4607074337) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63530#issuecomment-4609279991) **MartinJohns** said "This has to be another AI spam bot."

