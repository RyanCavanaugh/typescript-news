# Report for 2026-08-19 (Wednesday, August 19th, 2026)

27 different users commented on 235 different issues.

## Recommended Actions

 * Response Recommended
    * @irfanstract asked for extending tsconfig's JSONC with extra features in [microsoft/TypeScript#30400](https://github.com/microsoft/TypeScript/issues/30400#issuecomment-5350493151)
    * @StyleShit asked if an API exists to check for recursive types to prevent overflow in [microsoft/TypeScript#63759](https://github.com/microsoft/TypeScript/issues/63759#issuecomment-5356535553)
    * @typescript-automation[bot] asked to document breaking changes on wiki and notify relevant maintainers in [microsoft/TypeScript#63763](https://github.com/microsoft/TypeScript/pull/63763#issuecomment-5349541636)
    * @typescript-automation[bot] asked to document breaking changes on wiki and notify relevant maintainers in [microsoft/TypeScript#63763](https://github.com/microsoft/TypeScript/pull/63763#issuecomment-5350134148)

## Activity Summary

### [Issue microsoft/TypeScript#14561](https://github.com/microsoft/TypeScript/issues/14561) (Closed, `Bug`, `Domain: JavaScript`)

**type information from referenced file not available\.**

*TypeScript in VS Code does not show type information or IntelliSense for types imported from a referenced JavaScript file.*

 * (7.7 years ago) **weswigham** removed labels `Salsa`, `Salsa`
 * **sandersn** unassigned **sandersn**
 * [today](https://github.com/microsoft/TypeScript/issues/14561#issuecomment-5346921479) **RyanCavanaugh** said "This is fixed now"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28635](https://github.com/microsoft/TypeScript/issues/28635) (Closed, `Bug`, `Domain: JSDoc`)

**Inconsistency of mapped type and \`Parameters\<T\>\` between TS and JS**

*JSDoc-based mapped types with Parameters<T> generate optional parameters in JavaScript unlike TypeScript's required ones.*

 * **RyanCavanaugh** unassigned **sandersn**
 * [7.3 years ago](https://github.com/microsoft/TypeScript/issues/28635#issuecomment-486741053) **niksajanjic** described encountering the same TS errors with Object.freeze and .map(Object.freeze) and provided code examples and a simple fix
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [today](https://github.com/microsoft/TypeScript/issues/28635#issuecomment-5346812072) **RyanCavanaugh** said "This is fixed"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28724](https://github.com/microsoft/TypeScript/issues/28724) (Closed, `Bug`, `Domain: JavaScript`)

**JSDoc @type for list of declarations**

*JSDoc @type annotation on an empty array only provides intellisense for the first of multiple variable declarations and not for subsequent ones.*

 * (7.4 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `TypeScript 3.4.0`
 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/28724#issuecomment-825354722) **Paril** said "Any news on this one? It's an old issue, but still quite relevant. Kind of similar to #43756 in terms of workarounds."
 * [today](https://github.com/microsoft/TypeScript/issues/28724#issuecomment-5346555716) **RyanCavanaugh** said "This got fixed in ~4.9 or so"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28953](https://github.com/microsoft/TypeScript/issues/28953) (Closed, `Bug`, `Domain: JSX/TSX`)

**JSX\.ElementChildrenAttribute values are never considered excess properties in JSX**

*TypeScript always allows children defined by JSX.ElementChildrenAttribute as excess properties, preventing excess property errors for undeclared children.*

 * (7.7 years ago) **weswigham** added labels `Bug`, `Domain: JSX/TSX`
 * **RyanCavanaugh** added to milestone `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/28953#issuecomment-5346538672) **RyanCavanaugh** said "This was fixed in TS 3.3"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#29622](https://github.com/microsoft/TypeScript/issues/29622) (Closed, `Bug`, `Domain: API`, `Crash`, `Domain: Binder`)

**Error: Debug Failure getDisplayName for babel project while getting program\.getTypeChecker\(\)**

*TypeScript 3.0.3 throws a Debug Failure in getDisplayName when creating a type checker for Babel code.*

 * **weswigham** added label `Crash`
 * (7.4 years ago) **RyanCavanaugh** added label `Domain: Binder`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/29622#issuecomment-5346531646) **RyanCavanaugh** reproduced the crash in TypeScript 3.0.3 with a minimal example and confirmed that it’s fixed in TypeScript 7.1.0-dev with correct diagnostics
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#29718](https://github.com/microsoft/TypeScript/issues/29718) (Closed, `Bug`, `Domain: Mapped Types`)

**Object non\-literal keys breaks parameter type guard in callback value**

*Non-literal object property keys prevent TypeScript from inferring callback parameter types and detecting duplicate keys.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/29718#issuecomment-752633944) **Zzzen** said "I think getC() should be recognized as "c", just like key can be inferred in obj[getC()] = key => key."
 * **RyanCavanaugh** added label `Domain: Mapped Types`
 * [today](https://github.com/microsoft/TypeScript/issues/29718#issuecomment-5346525346) **RyanCavanaugh** reported that the current nightly fixed the issue and demonstrated correct diagnostic behavior on a reduced code sample
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#29821](https://github.com/microsoft/TypeScript/issues/29821) (Closed, `Bug`, `Domain: Something Else`)

**TS doesn't see when we add symbol properties to functions\. **

*TypeScript incorrectly reports a missing symbol property on a function annotated with an interface requiring that property, even after assignment.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [3 years ago](https://github.com/microsoft/TypeScript/issues/29821#issuecomment-1676931339) **Andarist** noted that the issue was fixed by PR #54726, provided a fix in PR #55357, and recommended closing the issue
 * **RyanCavanaugh** added label `Domain: Something Else`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#30155](https://github.com/microsoft/TypeScript/issues/30155) (Closed, `Bug`, `Domain: JSDoc`, `Domain: JavaScript`)

**Inaccurate error or buggy behavior for JSDoc @typedef tags**

*JSDoc '@typedef' error message incorrectly flags valid @member annotations as missing type annotations*

 * [7.2 years ago](https://github.com/microsoft/TypeScript/issues/30155#issuecomment-493785321) **danvk** described encountering an error caused by using a Closure-style @typedef with a var outside the JSDoc comment instead of placing the type name inside the comment
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/30155#issuecomment-2701598703) **daviareias** described using ripgrep with a regex to locate TypeScript errors when the compiler didn’t show the error location
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/30155#issuecomment-3114538629) **RyanCavanaugh** said "Confirmed repro in 5.9. Maybe this is a Won't Fix."
 * [today](https://github.com/microsoft/TypeScript/issues/30155#issuecomment-5346506575) **RyanCavanaugh** said "This is fixed in 7"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#30400](https://github.com/microsoft/TypeScript/issues/30400) (Closed, `Suggestion`, `Too Complex`)

**Allow javascript \(or typescript\) config file**

*Support tsconfig.js or tsconfig.ts configuration files to allow comments and improved readability.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/30400#issuecomment-2078015952) **silverwind** said "https://github.com/microsoft/TypeScript/issues/57486 highlights the need for this. It tries to invent complex syntax for merging/extending when it could just be done by the user in a code config file."
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/30400#issuecomment-2397866299) **eXory2024** urged dynamic config support and admonished responsibility for preventing code from doing stupid things
 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/30400#issuecomment-2536535266) **kerryj89** suggested reconsidering allowing js config support for advanced monorepo use cases due to lack of merging in simple JSON configs
 * [today](https://github.com/microsoft/TypeScript/issues/30400#issuecomment-5349444914) **DanhezCode** said "now in 2026 ts.config.ts is a good standar"
 * [today](https://github.com/microsoft/TypeScript/issues/30400#issuecomment-5350493151) **irfanstract** said "I'd ask for extending tsconfig's JSONC with some extra stuff, like const variables and restricted methods (map, flatMap, filter, toSorted, and friends)."

### [Issue microsoft/TypeScript#31001](https://github.com/microsoft/TypeScript/issues/31001) (Closed, `Bug`, `Domain: Literal Types`)

**String literals widened to string when destructuring function return**

*Destructuring a generic function's returned string literal property immediately widens it to string instead of preserving its literal type*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/31001#issuecomment-847387317) **Tukajo** asked if there had been any progress on the bug about TypeScript not inferring string literal unions when spreading props
 * **RyanCavanaugh** added label `Domain: Literal Types`
 * [today](https://github.com/microsoft/TypeScript/issues/31001#issuecomment-5345984484) **RyanCavanaugh** said "This works as expected now"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#31172](https://github.com/microsoft/TypeScript/issues/31172) (Closed, `Bug`, `Domain: JavaScript`)

**Namespaced ES6 classes are not recognized as types**

*Namespaced ES6 class NS.T isn't recognized by VSCode's JavaScript type checker, defaulting its parameters to any.*

 * (7.3 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: JavaScript`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/31172#issuecomment-5345973626) **RyanCavanaugh** said "This was fixed in TS 4.5, and remains fixed in TS 7"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#31599](https://github.com/microsoft/TypeScript/issues/31599) (Closed, `Bug`, `Domain: JSDoc`)

**Arobases in an example section of a jsdoc is considered a jsdoc section**

*VS Code incorrectly parses the @ symbol in module import paths within a jsdoc @example block as jsdoc tags.*

 * (7.2 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: JSDoc`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/31599#issuecomment-5345962579) **RyanCavanaugh** said "Fixed in TS 7 (probably much earlier but that's what I checked)"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#50466](https://github.com/microsoft/TypeScript/issues/50466) (Closed, `Needs Investigation`, **weswigham**)

**NodeNext resolution failed to resolve dual\-package correctly**

*NodeNext resolution incorrectly resolves a dual-package by selecting the CommonJS export instead of the type definitions, causing a TS2349 error.*

 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/50466#issuecomment-1880582216) **kerambit** mentioned encountering the same problem, referenced a linked solution, and noted that consumer code must use CJS although docs recommend nodenext
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/50466#issuecomment-5172407186) **miami-man** said "Has this been resolved yet? I've been using a command line tool to automate this process for a few years now, so have lost track of status. "
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/50466#issuecomment-5195005662) **andrewbranch** said "I don’t know why this wasn’t closed as “Working as Intended.”"
 * [today](https://github.com/microsoft/TypeScript/issues/50466#issuecomment-5345433417) **weswigham** clarified that the issue was only a reminder to remove a bad example sharing a `.d.ts` file and noted that the handbook and blog posts had already been corrected, so the issue was unrelated
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#55486](https://github.com/microsoft/TypeScript/issues/55486) (Closed, `Planning`)

**TypeScript 5\.3 Iteration Plan**

*The plan outlines the timeline and key compiler and language service features scheduled for TypeScript 5.3.*

 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/55486#issuecomment-1861971770) **laterdayi** said "https://github.com/microsoft/TypeScript/issues/47663      Several years later, the problem still persists"
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/55486#issuecomment-1876506578) **jogibear9988** asked if issue #42048 was an option when parsing jsdoc in TS files
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/55486#issuecomment-1877660194) **DanielRosenwasser** said "The 5.4 iteration plan is now available here."
 * [today](https://github.com/microsoft/TypeScript/issues/55486#issuecomment-5351770237) **spartanatreyu** said "This issue should probably be closed"
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#61216](https://github.com/microsoft/TypeScript/issues/61216) (Open, `Suggestion`, `Help Wanted`, `Committed`)

**Support source phase imports**

*Enable TC39 source phase imports in TypeScript to allow importing raw WebAssembly modules directly.*

 * (1.4 years ago) **RyanCavanaugh** added labels `Committed`, `Help Wanted`, and set milestone to `TypeScript 5.9.0`
 * **typescript-automation[bot]** added label `Fix Available`

### [Issue microsoft/TypeScript#62963](https://github.com/microsoft/TypeScript/issues/62963) (Closed, `Meta-Issue`)

**Transition to 6\.0 Maintenance Mode**

*TypeScript 6.0 is now in maintenance mode, accepting only regression, deprecation, and crash fixes while the team prioritizes TypeScript 7.0.*

 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3940657202) **jogibear9988** asked whether there was a plan for a WASM version of TypeScript 7.0 and how it would integrate into the Monaco editor or client-side websites
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3956082889) **RyanCavanaugh** said "WASM is definitely possible. The perf today is not super -- about on par with the JS codebase -- but it would hopefully get better over time as Go and/or browsers get better at it."
 * [21 weeks ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-4100336368) **RyanCavanaugh** enumerated PR merge criteria for post-6.0 changes
 * [today](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-5351858114) **jakebailey** stated that the repo is now targeting TS7 and referenced issue #63763
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63342](https://github.com/microsoft/TypeScript/issues/63342) (Open, `Experimentation Needed`, `Domain: check: Big Unions`, `Possible Improvement`)

**type checking complexity with multiple template literals in unions**

*TypeScript’s type checking time scales exponentially with unions of template literal types in dynamic route definitions.*

 * (19 weeks ago) **RyanCavanaugh** added labels `Experimentation Needed`, `Possible Improvement`, `Domain: check: Big Unions`
 * (later) **eps1lon** closed the issue
 * (later) **eps1lon** reopened the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63342#issuecomment-5353671888) **eps1lon** said "Go port filed against this repo in https://github.com/microsoft/TypeScript/pull/63900"

### [PR microsoft/TypeScript#63343](https://github.com/microsoft/TypeScript/pull/63343) (Closed)

**Use trie for removeStringLiteralsMatchedByTemplateLiterals**

*Optimize removeStringLiteralsMatchedByTemplateLiterals by building a prefix trie for efficient template literal matching*

 * [19 weeks ago](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4180269841) **eps1lon** said "Looks like the same at a glance. Yours is already doing some size estimation it seems. I haven't accounted for opting out of trie-based search for small types."
 * [18 weeks ago](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4234453594) **afurm** asked whether the trie needed to index non-prefix segments too
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4903271233) **subweave-bot** praised the trie-based matching as smart and fast and included a Subweave map link
 * [later](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-5353645289) **eps1lon** said "JS implementation is obsolete. Replaced by Go implementation in https://github.com/microsoft/TypeScript/pull/63900"
 * (later) **eps1lon** closed the issue

### [PR microsoft/TypeScript#63688](https://github.com/microsoft/TypeScript/pull/63688) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove see/link special casing entirely in TS files**

*Eliminate all special casing of see/link tags in TypeScript files to test the effect.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/63688#issuecomment-5110420222) **jakebailey** said "@typescript-bot test top999"
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/63688#issuecomment-5110420906) **typescript-automation[bot]** started CI jobs and posted a status table with result links
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/63688#issuecomment-5111330274) **typescript-automation[bot]** provided TypeScript build comparison results between main and the PR merge and noted unused variable errors in compiler-explorer and Effect-TS/effect
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63755](https://github.com/microsoft/TypeScript/issues/63755) (Closed, `Suggestion`, `Awaiting More Feedback`)

**Contextually type \`this\` inside \`function\*\` from a leading thisArg**

*Implement contextual this typing for generator function expressions based on a leading thisArg to infer the enclosing instance type.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63755#issuecomment-5320745088) **RyanCavanaugh** said "I'm a little surprised this doesn't work already. If it's a ~one-line fix we should just do it; maybe there were unforeseen complications originally"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63755#issuecomment-5324016464) **bun-unsafe** clarified that contextual `this` works for plain functions but not for generator functions and requested applying the existing contextual-`this` rule to function* expressions
 * [today](https://github.com/microsoft/TypeScript/issues/63755#issuecomment-5344505069) **Andarist** asked to share the repro case as a TS playground after verifying that the provided code snippets worked
 * [later](https://github.com/microsoft/TypeScript/issues/63755#issuecomment-5358390609) **bun-unsafe** rechecked the snippet in TS 6.0.3 and 7.0.2, confirmed no TS2683 error, explained the actual error in app code, apologized for the noise and closed the issue as not a TypeScript gap
 * (later) **bun-unsafe** closed the issue

### [Issue microsoft/TypeScript#63757](https://github.com/microsoft/TypeScript/issues/63757) (Open)

**\[7\.0 API\] \- Accessing name on a jsdoc link that does not have a valid name produces sibling node**

*In TypeScript 7.0’s API, invalid JSDoc link names produce a sibling node instead of undefined.*

 * created by **dragomirtitian**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63757#issuecomment-5338133199) **MartinJohns** said "Am I missing something? 7.0 doesn't have an API."
 * [later](https://github.com/microsoft/TypeScript/issues/63757#issuecomment-5354498996) **dragomirtitian** mentioned that 7.0 has an unstable nightly API

### [Issue microsoft/TypeScript#63759](https://github.com/microsoft/TypeScript/issues/63759) (Closed, `External`)

**\`getReturnType\` stack overflow when using recursive generic function with accumulated type argument**

*getReturnType causes stack overflow when inferring return types for recursive generic functions with accumulated type arguments*

 * created by **StyleShit**
 * [today](https://github.com/microsoft/TypeScript/issues/63759#issuecomment-5347131432) **RyanCavanaugh** pointed out that the bug was in the user's recurse function and provided stack growth logs
 * **RyanCavanaugh** added label `External`
 * [later](https://github.com/microsoft/TypeScript/issues/63759#issuecomment-5356535553) **StyleShit** asked if an API existed to check whether a type is recursive to prevent overflow

### [Issue microsoft/TypeScript#63760](https://github.com/microsoft/TypeScript/issues/63760) (Open, `Not a Defect`)

**Improve tsdoc for sort\(\)**

*Update the TSDoc example for sort() in es5.d.ts to include the returned sorted array output.*

 * created by **advinans-dennis**
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63760#issuecomment-5346949701) **RyanCavanaugh** said "This doesn't seem necessary."

### [Issue microsoft/TypeScript#63762](https://github.com/microsoft/TypeScript/issues/63762) (Open, `Bug`, `Domain: LS: Symbol Navigation`)

**Go\-to\-type definition does not work on aliases to tuple types**

*Go-to-type definition fails on aliases to tuple types in TypeScript.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Bug`, `Domain: LS: Symbol Navigation`, and set milestone to `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`

### [PR microsoft/TypeScript#63763](https://github.com/microsoft/TypeScript/pull/63763) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Migrate repo to TypeScript 7**

*Migrate the repository to TypeScript 7 by replaying typescript-go commit history into a nested tsc module and preserving git history.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63763#issuecomment-5349541560) **typescript-automation[bot]** thanked the contributor, reminded them to ensure TSServer protocol changes don’t break the current API, and pinged additional reviewers
 * [today](https://github.com/microsoft/TypeScript/pull/63763#issuecomment-5349541636) **typescript-automation[bot]** instructed to document breaking changes on the API Breaking Changes wiki page and to notify @DanielRosenwasser and @RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/63763#issuecomment-5349598752) **github-advanced-security[bot]** explained that GitHub Code Scanning was set up and described its features and where to view results
 * [today](https://github.com/microsoft/TypeScript/pull/63763#issuecomment-5350133999) **typescript-automation[bot]** thanked the contributor, reminded them to ensure TSServer protocol changes don’t break the current API, and pinged additional reviewers
 * [today](https://github.com/microsoft/TypeScript/pull/63763#issuecomment-5350134148) **typescript-automation[bot]** instructed to document breaking changes on the API Breaking Changes wiki page and to notify @DanielRosenwasser and @RyanCavanaugh
 * (today) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript/pull/63763#issuecomment-5356050731) **ashlynorsomethin-hub** said "yo huge w"

### [PR microsoft/TypeScript#63764](https://github.com/microsoft/TypeScript/pull/63764) (Open, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump adm\-zip from 0\.5\.18 to 0\.6\.0**

*Upgrade adm-zip to v0.6.0 to fix a critical security vulnerability, add TypeScript types, and resolve several bugs*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63765](https://github.com/microsoft/TypeScript/pull/63765) (Open, `For Uncommitted Bug`, `dependencies`, `go`)

**Bump go\.mongodb\.org/mongo\-driver from 1\.17\.6 to 1\.17\.7 in /tools**

*Upgrade the MongoDB Go driver in /tools from v1.17.6 to v1.17.7 to include bug fixes and deprecation updates*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `go`
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#63766](https://github.com/microsoft/TypeScript/pull/63766) (Open, `For Uncommitted Bug`, `dependencies`, `go`)

**Bump software\.sslmate\.com/src/go\-pkcs12 from 0\.7\.0 to 0\.7\.2 in /tools**

*Update the go-pkcs12 dependency in the tools directory from version 0.7.0 to 0.7.2.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `go`, `dependencies`, `go`
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#63767](https://github.com/microsoft/TypeScript/pull/63767) (Open, `For Uncommitted Bug`, `dependencies`, `go`)

**Bump github\.com/aws/aws\-sdk\-go\-v2/service/s3 from 1\.96\.2 to 1\.97\.3 in /tools**

*Update AWS SDK Go v2 S3 service dependency in the tools directory from version 1.96.2 to 1.97.3.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `go`, `dependencies`, `go`
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#63768](https://github.com/microsoft/TypeScript/pull/63768) (Open, `For Uncommitted Bug`, `dependencies`, `go`)

**Bump github\.com/aws/aws\-sdk\-go\-v2/aws/protocol/eventstream from 1\.7\.5 to 1\.7\.8 in /tools**

*Upgrade aws-sdk-go-v2 eventstream protocol dependency from version 1.7.5 to 1.7.8 in tools*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `go`, `dependencies`, `go`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

