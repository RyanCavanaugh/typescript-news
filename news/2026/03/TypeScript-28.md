# Report for 2026-03-28 (Saturday, March 28th, 2026)

7 different users commented on 9 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#63299](https://github.com/microsoft/TypeScript/issues/63299) (Closed, `Working as Intended`)

**AsyncDisposable should allow non\-Promise returning implementations**

*Permit AsyncDisposable implementations to return void or PromiseLike<void> from Symbol.asyncDispose.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63299#issuecomment-4129520096) **RyanCavanaugh** said "What are real disposable objects out there that only sometimes return a Promise?"
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63299#issuecomment-4129628037) **RyanCavanaugh** showed a motivating example of a class implementing AsyncDisposable that forgot to call or await its disposer
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63299#issuecomment-4149197302) **typescript-bot** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63308](https://github.com/microsoft/TypeScript/issues/63308) (Closed, `Not a Defect`)

**\`let a = {}\` infers \`{}\` instead of \`object\`, which seems too wide for the initializer**

*Inferring an empty object literal as {} allows primitive assignments instead of preserving its object type*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63308#issuecomment-4144459355) **RyanCavanaugh** explained that determining the correct amount of type widening for mutable declarations is heuristic, illustrating with examples let a = {} and let a = 10
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63308#issuecomment-4144510902) **5cover** asked why {} literals are widened to {} instead of object and whether the widening heuristic should avoid crossing typeof categories
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63308#issuecomment-4144527119) **RyanCavanaugh** argued that the previous inference was begging the question and would introduce a variance discontinuity
 * [later](https://github.com/microsoft/TypeScript/issues/63308#issuecomment-4150108229) **5cover** explained that inferring {} for primitives is correct because primitives are treated structurally and runtime typeof changes shouldn’t require stricter inference semantics
 * (later) **5cover** closed the issue

### [PR microsoft/TypeScript#63310](https://github.com/microsoft/TypeScript/pull/63310) (Closed, **RyanCavanaugh**, **Copilot**)

**Mark class property initializers as outside of CFA containers**

*Restore PropertyDeclaration as a control flow container to isolate class property initializer type inference and prevent module-level narrowing leaks*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4148334091) **RyanCavanaugh** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4148334230) **typescript-bot** posted CI status updates including commands, statuses, and result links
 * [today](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4148372510) **typescript-bot** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4148381148) **typescript-bot** reported results of user tests comparing main and the PR merge, noting one Git clone failure but otherwise everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4148456905) **typescript-bot** reported successful test results from running the top 400 repos with tsc comparing main and PR merge
 * [today](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4148850455) **typescript-bot** posted performance run results as requested

### [Issue microsoft/TypeScript#63311](https://github.com/microsoft/TypeScript/issues/63311) (Closed, `Not a Defect`)

**\`typescript\.d\.ts\` uses ES2015\+ globals \(\`Map\`, \`ReadonlyMap\`\) without \`/// \<reference lib\>\` directive**

*typescript.d.ts uses ES2015 Map and ReadonlyMap without a /// <reference lib='es2015' /> directive, causing type errors outside ES2015 contexts.*

 * created by **baraknaveh**
 * [later](https://github.com/microsoft/TypeScript/issues/63311#issuecomment-4149633663) **jakebailey** argued that libraries typically omit references for builtins, explained directive preservation behavior, stated compiler errors clearly instruct fixes, and noted default target is ES2025

### [Issue microsoft/TypeScript#63314](https://github.com/microsoft/TypeScript/issues/63314) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow structural typing of prototypes**

*Add structural prototype typing to TypeScript so that prototype chain properties are recognized in type checking.*

 * created by **5cover**
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#63315](https://github.com/microsoft/TypeScript/issues/63315) (Closed, `Duplicate`)

**Error type constructor**

*Provide a type error constructor in TypeScript to allow explicit type-level errors instead of fallback to never.*

 * created by **masaeedu**
 * [today](https://github.com/microsoft/TypeScript/issues/63315#issuecomment-4148730562) **MartinJohns** said "Duplicate of #23689."

### [PR microsoft/TypeScript#63316](https://github.com/microsoft/TypeScript/pull/63316) (Closed)

**Port tsgo PR 3276 for testing**

*Port tsgo PR 3276 to test how PR 3288 impacts the extended tests.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63316#issuecomment-4149386870) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63316#issuecomment-4149386968) **typescript-bot** reported CI status updates for test top400, user test this, run dt, and perf test this faster with links to build results
 * [today](https://github.com/microsoft/TypeScript/pull/63316#issuecomment-4149415079) **typescript-bot** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/63316#issuecomment-4149420877) **typescript-bot** reported that user tests had one infrastructure failure but otherwise passed
 * [today](https://github.com/microsoft/TypeScript/pull/63316#issuecomment-4149451937) **typescript-bot** provided the performance run results requested by @jakebailey
 * [today](https://github.com/microsoft/TypeScript/pull/63316#issuecomment-4149477524) **typescript-bot** reported that compilation results for the top 400 repos looked good
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63317](https://github.com/microsoft/TypeScript/pull/63317) (Closed)

**docs: Add Chinese README**

*Add a Chinese version of the project’s README to the documentation directory.*

 * created by **CJstate**
 * [later](https://github.com/microsoft/TypeScript/pull/63317#issuecomment-4150260532) **MartinJohns** said "This doesn't seem to serve any purpose."

