# Report for 2026-07-16 (Thursday, July 16th, 2026)

9 different users commented on 22 different issues.

## Recommended Actions

 * Response Recommended
    * @denis-migdal asked if more information was needed about the regression in [microsoft/TypeScript#63644](https://github.com/microsoft/TypeScript/issues/63644#issuecomment-4995087715)
    * @Alex-Bond suggested rolling back the new file-watching system or adding a flag to use the old one in [microsoft/TypeScript#63646](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-4995708261)
    * @Alex-Bond provided additional details about environment and observed behavior in [microsoft/TypeScript#63646](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-4996371305)

## Activity Summary

### [Issue microsoft/TypeScript#63579](https://github.com/microsoft/TypeScript/issues/63579) (Closed, `Needs Investigation`, **johnfav03**)

**tsc \-\-build false negative through export star facade project**

*Incremental tsc --build with composite projects using export * facades fails to detect downstream type changes, resulting in stale declarations.*

 * **RyanCavanaugh** added label `Needs Investigation`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63579#issuecomment-4846863745) **jakebailey** said "@jasonkuhrt @johnfav03 Is this a 7.0 regression? Or does this reproduce in 6.0?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63579#issuecomment-4846969089) **johnfav03** clarified that the issue was not a 7.0 regression and that it reproduced in 6.0
 * [today](https://github.com/microsoft/TypeScript/issues/63579#issuecomment-4997279541) **johnfav03** said "Fixed in #4301"
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript#63643](https://github.com/microsoft/TypeScript/issues/63643) (Closed, `Duplicate`)

**Reusable callbacks: When destructuring, missing properties should be excluded from the infered type\.**

*TypeScript should infer destructured callback parameters using only the referenced properties instead of requiring the entire type.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4971877503) **denis-migdal** questioned how the proposed inference would increase type problems, explained that it would solve type issues when reusing callbacks, and illustrated how to force type parameters with alternative generic definitions
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4972289232) **RyanCavanaugh** provided a code snippet demonstrating a unit mismatch that crashed the Mars probe
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4972686606) **denis-migdal** argued that the type definition of bindings, not the suggestion, caused the issue and illustrated with example code
 * [today](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4996142542) **RyanCavanaugh** clarified that destructuring is an internal implementation detail that should not change the function's external behavior or signature
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63644](https://github.com/microsoft/TypeScript/issues/63644) (Open, `Needs More Info`)

**In a class, an unique symbol attribute is sometime lost during incremental build**

*Incremental builds with interface declaration merging sometimes lose a class's unique symbol property, leading to TS7053 errors.*

 * created by **denis-migdal**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63644#issuecomment-4983168816) **RyanCavanaugh** said "What's the behavior in TS 7?"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63644#issuecomment-4985411150) **denis-migdal** reported TS7 errors after modifying files and suggested more concise, two-line error summaries to improve readability
 * [today](https://github.com/microsoft/TypeScript/issues/63644#issuecomment-4994650165) **RyanCavanaugh** said "What exactly is the defect, in TS7, that you are reporting?"
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63644#issuecomment-4995087715) **denis-migdal** reported three issues with the incremental build, a regression in TS 7.0.2, and hard-to-read error messages, and assumed more information was wanted about the regression
 * [today](https://github.com/microsoft/TypeScript/issues/63644#issuecomment-4995302238) **denis-migdal** said "Note: If you want to explore it, theses are the types from chart.js@4.5.1."

### [Issue microsoft/TypeScript#63646](https://github.com/microsoft/TypeScript/issues/63646) (Open, `Needs Investigation`, **johnfav03**)

**tsc \-\-watch does not work in docker**

*tsc --watch fails to detect file changes in Docker bind-mounted workspaces on macOS after upgrading to version 7.0.2.*

 * created by **laverdet**
 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-4995708261) **Alex-Bond** reported a similar problem on MacOS where the new TS watch system exhausted system resources and suggested rolling back or adding a flag to use the old file-watching system
 * [today](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-4996181046) **johnfav03** asked if the issue also involved docker or was a separate issue with running watchers in parallel
 * [today](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-4996371305) **Alex-Bond** reported that the issue occurred on a native system where circular symlinks in node_modules overwhelmed the watcher, causing it to start listening but never receive updates
 * [today](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-4999890598) **jakebailey** advised the user to file a separate issue for the MacOS problem and clarified that TS7 has no toggle to revert to NodeJS behavior

### [Issue microsoft/TypeScript#63648](https://github.com/microsoft/TypeScript/issues/63648) (Open, `Suggestion`, `Awaiting More Feedback`)

**Some colors make error messages hard to read on white backgrounds\.**

*Diagnosticwriter’s forced bright ANSI color codes make error messages illegible on white backgrounds and should use default colors instead.*

 * created by **ayosec**
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63648#issuecomment-4985206698) **jakebailey** questioned whether the issue was new in v7 and linked to existing code
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63648#issuecomment-4985206740) **ayosec** noted that the issue also existed in the original compiler and asked if it should be moved to the microsoft/TypeScript repository
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#63651](https://github.com/microsoft/TypeScript/issues/63651) (Closed)

**Ternary operator narrows down types when they are subsets of each other**

*TypeScript’s ternary operator narrows an object type to the subset shared by both branches, dropping extra properties.*

 * created by **Quacken8**
 * [today](https://github.com/microsoft/TypeScript/issues/63651#issuecomment-4993406096) **MartinJohns** said "Duplicate of #46449. You are a victim of subtype reduction. Do you wish to join the self-support group?"
 * (today) **Quacken8** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63651#issuecomment-4994648414) **Quacken8** said "It's a sign of a good feature that it keeps getting reported as a bug"

### [Issue microsoft/TypeScript#63652](https://github.com/microsoft/TypeScript/issues/63652) (Closed)

**Files changed**

*Report indicating that files in the repository have been modified.*

 * created by **fernandoesteban2408-ux**
 * [today](https://github.com/microsoft/TypeScript/issues/63652#issuecomment-4994654827) **RyanCavanaugh** said "Indeed they did"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63653](https://github.com/microsoft/TypeScript/issues/63653) (Open, `Needs Investigation`, **ahejlsberg**)

**Template literal union type\-checking is exponentially slower when type is explicitly annotated vs inferred**

*TypeScript’s type-checker experiences exponential slowdown when checking large template literal union types on explicitly annotated variables compared to inferred ones.*

 * created by **LangLangBart**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/issues/63653#issuecomment-4997425821) **RyanCavanaugh** said "This might not be a bug; // repro-inferred.ts really does have to do less work than // repro.ts - the latter has to do an assignability check, the former does not."

### [PR microsoft/TypeScript#63654](https://github.com/microsoft/TypeScript/pull/63654) (Closed, `For Backlog Bug`)

**lib\.es5\.d\.ts: accept array\-likes \(arguments, typed arrays, DOM collections\) as the second argument of Function\.prototype\.apply**

*Add an overload to lib.es5.d.ts so Function.prototype.apply accepts any array-like object per ECMAScript spec*

 * created by **KAMRONBEK**
 * **typescript-automation[bot]** added label `For Backlog Bug`

