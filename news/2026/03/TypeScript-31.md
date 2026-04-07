# Report for 2026-03-31 (Tuesday, March 31st, 2026)

11 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @denis-migdal asked about redefining cloneNode for improved typing in [microsoft/TypeScript#283](https://github.com/microsoft/TypeScript/issues/283#issuecomment-4169322887)
    * @denis-migdal suggested changing the function signature to require the optional parameter when the generic parameter is incompatible in [microsoft/TypeScript#58977](https://github.com/microsoft/TypeScript/issues/58977#issuecomment-4171035844)
    * @trevorade asked for a timeline for tsc 6.0.3 in [microsoft/TypeScript#63309](https://github.com/microsoft/TypeScript/issues/63309#issuecomment-4164294071)
    * @GertSallaerts asked where the documentation could go in [microsoft/TypeScript#63320](https://github.com/microsoft/TypeScript/issues/63320#issuecomment-4164347860)

## Activity Summary

### [Issue microsoft/TypeScript#283](https://github.com/microsoft/TypeScript/issues/283) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**cloneNode should return sub type, not Node**

*cloneNode currently returns a generic Node type instead of preserving the actual element subtype*

 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/283#issuecomment-1290875359) **clshortfuse** noted that `typeof this` sounds the same but differs and said there wasn't enough information to assess its performance impact
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/283#issuecomment-2026808489) **callionica** asked for a reassessment of fixing the cloneNode issue and suggested adding specific overloads for Element and HTMLElement
 * [50 weeks ago](https://github.com/microsoft/TypeScript/issues/283#issuecomment-2802350962) **miss-programgamer** proposed using 'typeof class' to express the type of the current class or its subtypes and asked if implicit conversion to this would cause issues
 * [later](https://github.com/microsoft/TypeScript/issues/283#issuecomment-4169322887) **denis-migdal** suggested redefining cloneNode at least for DocumentFragment and HTMLElement using interface augmentation for better typing

### [Issue microsoft/TypeScript#58977](https://github.com/microsoft/TypeScript/issues/58977) (Open, `Suggestion`, `Experimentation Needed`)

**Allow defering type check of default value for generic\-typed function parameter until instantiation**

*Propose deferring the default value type check for generic function parameters until instantiation to avoid spurious TS2322 errors.*

 * (1.7 years ago) **RyanCavanaugh** added label `Experimentation Needed`, and removed label `In Discussion`
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/58977#issuecomment-2192561969) **RyanCavanaugh** described challenges of deferring default parameter checks to call sites due to parity requirements with .d.ts files, complex evaluation scenarios, and broad system impacts, and concluded that a PR would be too invasive unless a simpler solution emerged
 * [later](https://github.com/microsoft/TypeScript/issues/58977#issuecomment-4171035844) **denis-migdal** suggested changing the function signature to require the optional parameter when the generic parameter is incompatible

### [Issue microsoft/TypeScript#63309](https://github.com/microsoft/TypeScript/issues/63309) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Regression in 6\.0: type inferred from const with broader type is too narrow**

*TypeScript 6.0 mistakenly narrows a class property initialized from a union-typed constant to a single literal value.*

 * (4 days ago) **RyanCavanaugh** added label `Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63309#issuecomment-4164294071) **trevorade** thanked for fixing and asked for a timeline for tsc 6.0.3
 * [today](https://github.com/microsoft/TypeScript/issues/63309#issuecomment-4164904964) **RyanCavanaugh** said "Likely in the next week or so, we're going to want to see if any other patch-worthy bugs come in"

### [PR microsoft/TypeScript#63310](https://github.com/microsoft/TypeScript/pull/63310) (Closed, **RyanCavanaugh**, **Copilot**)

**Mark class property initializers as outside of CFA containers**

*Restore PropertyDeclaration as a control flow container to isolate class property initializer type inference and prevent module-level narrowing leaks*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4148850455) **typescript-bot** posted performance run results as requested
 * **RyanCavanaugh** added to milestone `TypeScript 6.0.2`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4163848637) **jakebailey** said "@typescript-bot cherry-pick this to release-6.0"
 * [today](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4163849118) **typescript-bot** posted a status update about CI jobs starting and linking to results
 * [today](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4163862108) **typescript-bot** said "Hey, @jakebailey! I've created #63327 for you."

### [Issue microsoft/TypeScript#63320](https://github.com/microsoft/TypeScript/issues/63320) (Open, `Suggestion`, `Awaiting More Feedback`)

**importModuleSpecifier "shortest" does not choose shortest result among multiple matching paths aliases**

*TypeScript’s auto-import ‘shortest’ setting ignores path length and picks the first matching alias instead of the shortest.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63320#issuecomment-4154429746) **RyanCavanaugh** stated that the issue was uncommon, the workaround was reasonable, and a fix was unwarranted due to performance concerns
 * (yesterday) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63320#issuecomment-4164347860) **GertSallaerts** said "Agree that it's probably pretty uncommon. Might be interesting to have this documented though I'm having a hard time figuring out where exactly that could go."

### [Issue microsoft/TypeScript#63325](https://github.com/microsoft/TypeScript/issues/63325) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**\`lib\.dom\.d\.ts\`: Keyframe interface should allow CSS Typed Object Model objects like CSSTransformValue, etc**

*The Keyframe interface in lib.dom.d.ts should accept CSS Typed Object Model types such as CSSTransformValue.*

 * created by **zardalt**
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, `Domain: lib.d.ts`

### [PR microsoft/TypeScript#63327](https://github.com/microsoft/TypeScript/pull/63327) (Closed, **DanielRosenwasser**)

**🤖 Pick PR \#63310 \(Mark class property initializers as\.\.\.\) into release\-6\.0**

*Cherry-pick PR #63310 marking class property initializers into the release-6.0 branch for review and merge*

 * created by **typescript-bot**
 * **typescript-bot** assigned to **DanielRosenwasser**

### [PR microsoft/TypeScript#63328](https://github.com/microsoft/TypeScript/pull/63328) (Closed)

**Backport tsgo PR 3301 for testing**

*Backport TypeScript-Go pull request 3301 to evaluate its performance.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4164331898) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4164332339) **typescript-bot** posted CI build statuses for four jobs: test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4164483692) **typescript-bot** noted that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4164502658) **typescript-bot** ran user tests comparing main and the PR merge and reported one infrastructure failure but otherwise everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4164657534) **typescript-bot** provided the requested performance run results in a detailed table
 * [today](https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4164789350) **typescript-bot** reported build results for the top 400 repos comparing main with the pull request, highlighted new TS2722 and TS2349 errors in Inquirer.js, and asked for review
 * [today](https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4165397001) **RyanCavanaugh** provided a reduced TypeScript example from the repository demonstrating the issue

### [PR microsoft/TypeScript#63329](https://github.com/microsoft/TypeScript/pull/63329) (Closed)

**fix: add parameterized queries in configurePrerelease\.mjs \(utils\.cust\.\.\.**

*Added parameterized queries to configurePrerelease.mjs to address a high-severity SQL injection vulnerability detected by semgrep.*

 * created by **orbisai0security**
 * [later](https://github.com/microsoft/TypeScript/pull/63329#issuecomment-4168152144) **jakebailey** said "There is no vulnerability here."
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63330](https://github.com/microsoft/TypeScript/issues/63330) (Open, `Docs`, **DanielRosenwasser**)

**\[V6\] \`module\` defaults is not \`esnext\`**

*TypeScript 6.0 incorrectly defaults the module option to ES2015 instead of ESNext, causing import attributes errors.*

 * created by **regseb**
 * [later](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4169933585) **mkantor** explained that module defaulted to es2022 due to ScriptTarget.LatestStandard being es2025 and confirmed the same error with --module es2022
 * [later](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4169953503) **mkantor** noticed that the documentation for the default value of `target` was incorrect and that `ES3` was still mentioned as allowed though no longer supported
 * [later](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4169983541) **mkantor** questioned the repeated phrasing in the announcement post and asked if it was a typo

### [Issue microsoft/TypeScript#63331](https://github.com/microsoft/TypeScript/issues/63331) (Closed)

**Admin Dashboard Implementation Progress Update**

*The admin dashboard tRPC backend is now 75% complete with all procedures implemented and ready for frontend integration.*

 * created by **rrader26**
 * [later](https://github.com/microsoft/TypeScript/issues/63331#issuecomment-4168993162) **MartinJohns** said "You seem to be lost. Which repository were you looking for?"

