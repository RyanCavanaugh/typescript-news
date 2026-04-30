# Report for 2026-04-27 (Monday, April 27th, 2026)

7 different users commented on 16 different issues.

## Recommended Actions

 * Response Recommended
    * @natsuki-engr asked if there's a path forward to formalize @local in [microsoft/TypeScript#46011](https://github.com/microsoft/TypeScript/issues/46011#issuecomment-4332923366)
    * @linnbenton asked whether the baseUrl deprecation warning behavior is intended for TS7 or if migration strategy for monorepos is still evolving in [microsoft/TypeScript#62508](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4331983425)
    * @Bertie690 asked what the quoted Ezra Koenig quote was in [microsoft/TypeScript#63432](https://github.com/microsoft/TypeScript/issues/63432#issuecomment-4329067421)
    * @creazyfrog asked whether pull requests created with AI agents are accepted and when the 6.0 patch will be released in [microsoft/TypeScript#63439](https://github.com/microsoft/TypeScript/pull/63439#issuecomment-4328732077)

## Activity Summary

### [Issue microsoft/TypeScript#46011](https://github.com/microsoft/TypeScript/issues/46011) (Open, `Suggestion`, `Needs Proposal`, `In Discussion`)

**Support for opting out of jsdoc @typedef exports**

*Allow disabling automatic export of root-scope @typedef declarations in JSDoc.*

 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/46011#issuecomment-2137950809) **ljharb** explained that renaming an exported type constitutes a semver-major change and is as dangerous as renaming a variable because it can break CI pipelines and is often propagated via editor autocompletion
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/46011#issuecomment-2137964557) **stoicbuddha** mentioned that editor autocompletion pollution could justify file-specific usage and noted potential annoyance; observed a potential disagreement on definitions of danger but deemed it unimportant to solving the overall issue
 * [28 weeks ago](https://github.com/microsoft/TypeScript/issues/46011#issuecomment-3395687680) **mhofman** described encountering the need to define a local module type for implementation details without exporting it
 * [today](https://github.com/microsoft/TypeScript/issues/46011#issuecomment-4332923366) **natsuki-engr** outlined the issue of unwanted @typedef exports, compared opt-out tag proposals, and asked if there was a path to formalize @local

### [Issue microsoft/TypeScript#62508](https://github.com/microsoft/TypeScript/issues/62508) (Open, `Discussion`)

**6\.0 Migration Guide**

*Placeholder issue for drafting and publishing the migration guide for version 6.0.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4152939556) **cscnk52** provided guidance on using node16/nodenext/bundler for moduleResolution and linked to the TypeScript docs
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4153001690) **dskloetc** thanked cscnk52 for the information and mentioned that the error message could have been more helpful
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4228915356) **Kimxons** noted that the solution worked okay
 * [today](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4331983425) **linnbenton** highlighted inconsistent baseUrl deprecation warnings in TS 6+ monorepo setups and asked whether this is intended as an early signal for TS 7 or if the migration strategy for monorepos is still evolving

### [Issue microsoft/TypeScript#63432](https://github.com/microsoft/TypeScript/issues/63432) (Closed, `Possible Improvement`)

**\`Math\.sign\` JSDoc comment has grammatical typo**

*Fix JSDoc comment in Math.sign for grammar by changing “the x” to “x”.*

 * [today](https://github.com/microsoft/TypeScript/issues/63432#issuecomment-4328388994) **RyanCavanaugh** said "To quote Ezra Koenig,"
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63432#issuecomment-4329067421) **Bertie690** asked what the quoted Ezra Koenig quote was and whether they were missing a joke
 * [today](https://github.com/microsoft/TypeScript/issues/63432#issuecomment-4329106507) **RyanCavanaugh** said "https://en.wikipedia.org/wiki/Oxford_Comma_(song)"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63433](https://github.com/microsoft/TypeScript/pull/63433) (Closed, `For Backlog Bug`)

**docs: improve Math\.sign JSDoc grammar and clarity**

*Updated Math.sign JSDoc in es2015.core.d.ts to correct phrasing and add missing comma for consistency.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63433#issuecomment-4318410016) **MartinJohns** cited the pull request template discouraging typo-only fixes
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63439](https://github.com/microsoft/TypeScript/pull/63439) (Closed, `For Backlog Bug`)

**fix\(completions\): sort JSDoc @param suggestions by declaration order**

*Add parameter index to completion sortText so JSDoc @param suggestions appear in declaration order rather than alphabetically.*

 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63439#issuecomment-4328336816) **RyanCavanaugh** stated that the PR didn't meet the bar for a 6.0 patch and asked whether the agent correctly prompted that the PR wouldn't be accepted
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63439#issuecomment-4328732077) **creazyfrog** asked whether PRs created with AI agents were accepted and when the 6.0 patch was planned for release
 * [today](https://github.com/microsoft/TypeScript/pull/63439#issuecomment-4328766437) **RyanCavanaugh** thanked and pointed to the AGENTS.md document regarding AI-assisted PR acceptance and patching policy for critical issues in 6.0

### [Issue microsoft/TypeScript#63441](https://github.com/microsoft/TypeScript/issues/63441) (Open, `Bug`, `Domain: check: Type Circularity`)

**\`symbolToNode\` stack overflow when using recursive types and functions with type parameters**

*Recursive generic functions and types cause TypeScript's symbolToNode to exceed the maximum call stack size.*

 * created by **StyleShit**
 * [today](https://github.com/microsoft/TypeScript/issues/63441#issuecomment-4328571967) **RyanCavanaugh** provided an automated list of similar issues

### [Issue microsoft/TypeScript#63442](https://github.com/microsoft/TypeScript/issues/63442) (Closed)

**Formatting fails for entire file when a line contains only whitespace between two comments**

*A line containing only whitespace between two single-line comments prevents VS Code from formatting the entire TypeScript or JavaScript file.*

 * created by **glitcher255**
 * [today](https://github.com/microsoft/TypeScript/issues/63442#issuecomment-4328536465) **RyanCavanaugh** said "This doesn't meet the 6.0 patch bar. Please log an issue in the typescript-go repo if this repros in the native language service. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63446](https://github.com/microsoft/TypeScript/pull/63446) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Redirect Claude Code to read AGENTS\.md**

*Enable Claude Code to read and process AGENTS.md, which it currently ignores.*

 * created by **RyanCavanaugh**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63447](https://github.com/microsoft/TypeScript/issues/63447) (Open, `Duplicate`)

**5\.9 regression: Union types served by mutually exclusive function overloads not working**

*TypeScript 5.9 fails to apply mutually exclusive overloads for functions accepting ArrayBuffer or Uint8Array.*

 * created by **hyperair**
 * [later](https://github.com/microsoft/TypeScript/issues/63447#issuecomment-4333882436) **hyperair** provided a workaround by checking if data was a Uint8Array before calling bar
 * [later](https://github.com/microsoft/TypeScript/issues/63447#issuecomment-4333955742) **MartinJohns** explained that the behavior change was due to type narrowing changes in TypeScript 5.9 and recommended removing the overload in favor of a union type parameter

