# Report for 2026-11-04 (Wednesday, November 4th, 2026)

18 different users commented on 62 different issues.

## Recommended Actions

 * Moderation
    * @Program-creator122 posted spam content in [microsoft/TypeScript#65100](https://github.com/microsoft/TypeScript/issues/65100#issuecomment-6649860494)
 * Response Recommended
    * @JemmyIndex provided detailed analysis and closed the PR, requesting maintainers to decide on printer behavior in [microsoft/TypeScript#65148](https://github.com/microsoft/TypeScript/issues/65148#issuecomment-6650867501)

## Activity Summary

### [Issue microsoft/TypeScript#202](https://github.com/microsoft/TypeScript/issues/202) (Open, `Suggestion`, `In Discussion`)

**Support some non\-structural \(nominal\) type matching**

*Introduce nominal typing in TypeScript to distinguish structurally identical types and prevent unintended type mixing.*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/202#issuecomment-2868870489) **emilioplatzer** shared a workaround with example repository and Playground link and explained a typing-by-example approach using string literal types
 * [23 weeks ago](https://github.com/microsoft/TypeScript/issues/202#issuecomment-4549960682) **bluepnume** described how they currently simulate opaque types with intersection types and custom tooling, illustrated how native opaque types and operator overloading would improve their workflow, linked to issue #42218, and expressed strong support
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/202#issuecomment-5432665580) **irfanstract** proposed allowing interfaces to extend union types to create preserved nominal types and suggested introducing an `Opaque` marker type for distinct opaque types
 * [later](https://github.com/microsoft/TypeScript/issues/202#issuecomment-6654116521) **Shinigami92** described working on a prototype for nominal type aliases with @claude, linking the commit and noting they had read the contributing guidelines and had not created a PR to avoid being blocked by Microsoft

### [Issue microsoft/TypeScript#58540](https://github.com/microsoft/TypeScript/issues/58540) (Open, `Bug`, `Help Wanted`, `Domain: Comment Emit`)

**duplicate comments on decorated fields**

*Using decorators on class fields causes duplicate comments for those fields in the transpiled output.*

 * (2.4 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Comment Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/58540#issuecomment-6645770704) **TimonGaertner** offered to work on the issue and reported that on version 7.1.0-dev.20261104.1 the JSDoc comment of the field following a decorated field was emitted twice

### [Issue microsoft/TypeScript#61783](https://github.com/microsoft/TypeScript/issues/61783) (Closed, `Help Wanted`, `Domain: Error Messages`, `Possible Improvement`)

**Function implementation name must be \.\.\. \(2389\) when abstract method is declared again later**

*TypeScript wrongly flags a concrete method name error instead of reporting the duplicate abstract method declaration.*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/61783#issuecomment-2927097644) **scusc** asked whether the declaration order requirement should be modified to accept unordered implementation methods
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/61783#issuecomment-2928374371) **loucadufault** agreed that the issue is broader than abstract methods, noted that non-abstract classes produced a clearer error on the second func1, and suggested improving the error messaging
 * **RyanCavanaugh** added label `Domain: Error Messages`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62436](https://github.com/microsoft/TypeScript/issues/62436) (Closed, **andrewbranch**)

**"This import path is unsafe to rewrite because it resolves to another project" missing an error location**

*The compiler error for unsafe import path rewrites across projects omits file and location information.*

 * created by **andrewbranch**
 * **andrewbranch** assigned to **andrewbranch**
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/62436#issuecomment-3282382485) **andrewbranch** stated that the issue was caused by tsbuildinfo state and that after cleaning and rebuilding they could not reproduce or craft a failing test
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64046](https://github.com/microsoft/TypeScript/pull/64046) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Flip files from CRLF to LF**

*Convert the remaining CRLF line endings in public API code and miscellaneous files to LF for consistency.*

 * (9 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64193](https://github.com/microsoft/TypeScript/pull/64193) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**fix\(tsoptions\): don't mutate ParsedCommandLine errors when computing CommonSourceDirectory**

*Fix CommonSourceDirectory to no longer mutate ParsedCommandLine errors by omitting source file path checks.*

 * created by **erantianantha**
 * (8 weeks ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64193#issuecomment-6637128808) **andrewbranch** said "Hey, sorry I forgot about this fix. If you want to fix the merge conflict, this looks correct to me and we can merge."
 * [today](https://github.com/microsoft/TypeScript/pull/64193#issuecomment-6638480064) **erantianantha** thanked the reviewer, merged main to resolve conflicts, and updated the test to include a file outside rootDir so it fails properly
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64910](https://github.com/microsoft/TypeScript/pull/64910) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid unnecessary localization branch rebases**

*Prevent rebasing the localization branch when its files are unchanged to avoid unnecessary commits and review churn.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64988](https://github.com/microsoft/TypeScript/pull/64988) (Open, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**Add missing Program and Project Methods**

*Add several missing Program API methods (for counts, diagnostics and references) and Project API methods for file and configuration access.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript/pull/64988#issuecomment-6648961939) **iisaduan** removed GetResolvedProjectReferences to rethink its implementation later and referenced relevant comments

### [PR microsoft/TypeScript#64989](https://github.com/microsoft/TypeScript/pull/64989) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Check ASCII identifier bytes with a lookup table**

*A lookup table for ASCII identifier checks speeds BenchmarkParse by 1-3% on M1 and yields larger gains for longer identifiers.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64989#issuecomment-6466038314) **typescript-automation[bot]** reported CI jobs start and linked build results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64989#issuecomment-6466967535) **typescript-automation[bot]** provided the requested performance run results for tsc, including a provisional hosted-runner comparison table indicating no significant changes
 * **jakebailey** added label `Domain: Performance`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65028](https://github.com/microsoft/TypeScript/pull/65028) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reuse scratch node lists in the parser**

*Reuse parser scratch buffers for nested list parsing to minimize heap allocations and memory garbage.*

 * **jakebailey** added label `Domain: Performance`
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/65028#issuecomment-6508835852) **typescript-automation[bot]** provided the performance run results requested by the user
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/65028#issuecomment-6508863691) **jakebailey** said "Hm, no great effect."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65032](https://github.com/microsoft/TypeScript/pull/65032) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Speed up keyword lookup, identifier scanning, and whitespace skipping in the scanner**

*Optimize the scanner’s performance by improving keyword lookup, identifier scanning, and whitespace skipping.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/65032#issuecomment-6508851917) **jakebailey** said "@typescript-bot perf test this faster"
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/65032#issuecomment-6508853497) **typescript-automation[bot]** announced that performance test jobs started and provided links to build status and results
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/65032#issuecomment-6510095162) **typescript-automation[bot]** provided the requested performance run results including detailed metrics for errors, symbols, types, and memory usage
 * [today](https://github.com/microsoft/TypeScript/pull/65032#issuecomment-6638440929) **RyanCavanaugh** said "Looks like this one is fully represented elsewhere and is conflicted now anyway"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65033](https://github.com/microsoft/TypeScript/pull/65033) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Speed up union construction with sorted\-run merging and cheaper membership check**

*Introduce sorted-run merging and cheaper membership checks to improve union construction performance.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/65033#issuecomment-6508406394) **typescript-automation[bot]** posted CI status update with build start and results links
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/65033#issuecomment-6509471610) **typescript-automation[bot]** provided perf run results in a comparison report
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/65033#issuecomment-6524379365) **RyanCavanaugh** said "Not sure if this one is worth it if it's only 1% on compiler-unions"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65037](https://github.com/microsoft/TypeScript/pull/65037) (Closed, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**Adds missing methods from checker api **

*Add missing Checker API methods for various type queries and remove the deprecated getAugmentedPropertiesOfType.*

 * (6 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **iisaduan**
 * (today) **iisaduan** closed the issue

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*Make the type checker fully order independent by replacing ID-based caching with content-based memos and order-variant tests.*

 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6626572032) **typescript-automation[bot]** reported new TypeScript errors in user tests comparing baseline and pr and asked for review
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6626808573) **typescript-automation[bot]** shared the perf run results requested by @jakebailey
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6628509191) **typescript-automation[bot]** reported tsc comparison results on the top 1000 repos, noted build failures in OmniRoute and PeerTube, and asked to review an interesting change
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6645914146) **jakebailey** requested the TypeScript bot to run various tests
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6645915754) **typescript-automation[bot]** reported CI jobs starting and linked to their results
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6646507823) **typescript-automation[bot]** reported DT tests results with compile errors in the d3-selection package
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6646564190) **typescript-automation[bot]** reported new TypeScript errors when comparing baseline and pr
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6646681758) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6648209501) **typescript-automation[bot]** ran type-checking on the top 1000 repos comparing baseline and pr and reported build failures in multiple projects, including Chocobozzz/PeerTube and cloudflare/cloudflare-os
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6651189560) **jakebailey** requested various tests from the typescript-bot
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6651190926) **typescript-automation[bot]** reported that build jobs started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6651763674) **typescript-automation[bot]** reported DT tests results showing compile errors in ember/v2 array-proxy tests
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6651765074) **typescript-automation[bot]** reported new TypeScript errors for implicitly any return types in SchemaAST.ts and requested review
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6652030784) **typescript-automation[bot]** reported the requested performance run results comparing baseline to pr including errors, symbols, types, memory usage, and other metrics
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6653582736) **typescript-automation[bot]** reported tsc run results for top 1000 repos comparing baseline and pr and noted failures
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6656960458) **jakebailey** requested various tests from the typescript-bot
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6656962581) **typescript-automation[bot]** reported build jobs starting and provided status and results links for each command
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6657641344) **typescript-automation[bot]** reported branch-only DT test errors for d3-selection
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6657696352) **typescript-automation[bot]** reported new TypeScript errors TS7023 for implicit any return types in SchemaAST functions
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6657976465) **typescript-automation[bot]** posted the requested perf run results comparing baseline to PR
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6659932668) **typescript-automation[bot]** reported tsc results for the top 1000 repos and highlighted changed build failures in specific projects

### [Issue microsoft/TypeScript#65090](https://github.com/microsoft/TypeScript/issues/65090) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Native compiler API resolves a default\-parameter reference to a body function binding**

*The TypeScript native compiler API incorrectly resolves default parameter references to an inner function declaration instead of the outer variable.*

 * (yesterday) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65092](https://github.com/microsoft/TypeScript/issues/65092) (Open, `Suggestion`, `Declined`)

**Feature Request: Allow Content Mappers to opt\-in to transforming files end in built\-in extensions**

*Enable content mappers to opt in to transforming built-in TypeScript/JavaScript file extensions with scoped applicability and avoid duplicate LSP registrations.*

 * **RyanCavanaugh** added label `Declined`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65092#issuecomment-6590654364) **loopingz** noted that in version 7.1.0-dev.20260929.1 additional SQL validation was possible and suggested leaving the decision to the user
 * [yesterday](https://github.com/microsoft/TypeScript/issues/65092#issuecomment-6616085979) **RyanCavanaugh** explained why failing to block wouldn't work and listed issues with outputExtensions, refactorings, and multiple CMs for .ts files
 * [later](https://github.com/microsoft/TypeScript/issues/65092#issuecomment-6659529647) **DetachHead** suggested applying the built-in JSON content mapper only when resolveJsonModule was false so users could override it with custom mappers

### [Issue microsoft/TypeScript#65096](https://github.com/microsoft/TypeScript/issues/65096) (Closed, `Question`)

**Clarify EULA and Background Sync provenance in TypeScript 5\.9\.3 third\-party notices**

*Clarify the applicable EULA for the DefinitelyTyped entry and the provenance, coverage, and licensing of the Web Background Synchronization notice in TypeScript 5.9.3’s third-party notices.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65096#issuecomment-6588107945) **RyanCavanaugh** said "I don't have authoritative answers off the top of my head for those questions. I can forward to our Legal to ask, but they'll likely ask what you're trying to determine before giving an answer."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65096#issuecomment-6589431877) **beefstew** thanked maintainers and described running ORT on his app, noting unresolved license compliance questions
 * **RyanCavanaugh** added label `Question`
 * [today](https://github.com/microsoft/TypeScript/issues/65096#issuecomment-6646803677) **typescript-automation[bot]** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#65099](https://github.com/microsoft/TypeScript/pull/65099) (Closed, `For Backlog Bug`)

**Report TS2516 for non\-consecutive abstract method declarations**

*Skip misnamed implementation checks for abstract methods so TS2516 is reported when their declarations are non-consecutive.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65099#issuecomment-6576739844) **Shadow0Bit** said "@microsoft-github-policy-service agree"
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65099#issuecomment-6589221073) **jakebailey** suggested splitting the changes into two commits for easier review
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65099#issuecomment-6623279107) **Shadow0Bit** said "Sure thing, I've split it into two commits."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65100](https://github.com/microsoft/TypeScript/issues/65100) (Closed)

**getting started**

*Guidance request for getting started with blocks, tools, and framework, seeking collaboration and freelancing opportunities.*

 * created by **Program-creator122**
 * (2 days ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/65100#issuecomment-6649860494) **Program-creator122** asked if there was any front-end programming service for gaming and simulation

### [Issue microsoft/TypeScript#65101](https://github.com/microsoft/TypeScript/issues/65101) (Closed, `Duplicate`)

**Can you please add some new features for types: string length getter \(currently \`number\`\), string getter by index \(currently \`string\`\), array multiple spreads \(currently gives the error of type\)**

*Support exact string literal length, precise character indexing types, and multiple tuple spread elements in TypeScript.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65101#issuecomment-6581326118) **nmain** suggested searching for each issue independently and identified the first idea as a duplicate of issue #34692
 * **RyanCavanaugh** added label `Duplicate`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65101#issuecomment-6582413326) **RyanCavanaugh** said "The third is #48992"
 * [today](https://github.com/microsoft/TypeScript/issues/65101#issuecomment-6646802638) **typescript-automation[bot]** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#65148](https://github.com/microsoft/TypeScript/issues/65148) (Open, `Bug`)

**Native printer: \`new \(C?\.\(\)\.D\)\` emits as \`new \(C?\.\(\)\)\.D\` \(optional call trips hasUnparenthesizedCall\)**

*The TypeScript native printer misparenthesizes new expressions with optional call and member chains, printing new (C?.()).D() instead of new (C?.().D)().*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/65148#issuecomment-6599096865) **timurzvural** described that same-precedence bail affected as/satisfies in member chains and gave an example of printing discrepancy
 * (yesterday) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/65148#issuecomment-6650867501) **JemmyIndex** investigated the issue, determined the current printer behavior was intentional to avoid a semantic regression, closed the related PR, and offered to revisit if maintainers prefer treating synthetic chains as optional

### [Issue microsoft/TypeScript#65170](https://github.com/microsoft/TypeScript/issues/65170) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Erasing \`as\` or \`satisfies\` can expose an invalid left operand of \`\*\*\`**

*Under erasableSyntaxOnly mode, erasing 'as' or 'satisfies' assertions can expose unparenthesized operands for '**', resulting in invalid JavaScript without diagnostics.*

 * (yesterday) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/65170#issuecomment-6627538836) **magic-akari** said "What is the intended direction for fixing this? Should these expressions be rejected only with erasableSyntaxOnly, or should they be rejected in all configurations?"
 * [today](https://github.com/microsoft/TypeScript/issues/65170#issuecomment-6640343299) **RyanCavanaugh** said "The best precedent here is https://github.com/microsoft/TypeScript/issues/63533, where the treatment of 1 + 2 as any / 3 was discussed. So I think this is an error regardless of ESO."
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65299](https://github.com/microsoft/TypeScript/pull/65299) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Respect parameter\-initializer scope for body function declarations**

*Include function declarations in parameter-initializer scope checks to prevent inner functions from shadowing outer bindings during type checking.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65299#issuecomment-6620312943) **typescript-automation[bot]** reported that everything looked good after running user tests with tsc comparing baseline and pr
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65299#issuecomment-6620501535) **typescript-automation[bot]** reported the perf run results for the requested comparison
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65299#issuecomment-6621052262) **typescript-automation[bot]** reported that the tsc comparison of the top 400 repos between baseline and PR showed no issues
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65305](https://github.com/microsoft/TypeScript/pull/65305) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**API: poll briefly before blocking on the sync channel**

*API sync channel now briefly spin-polls incoming messages before blocking reads, reducing OS wake-up overhead and speeding execution.*

 * created by **WinterYukky**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#65308](https://github.com/microsoft/TypeScript/pull/65308) (Open, `Domain: Performance`, `For Backlog Bug`)

**Stop unbounded memory growth after type complexity limits are hit**

*Improve TypeScript checker to stop unbounded memory growth by halting expensive type expansions after reporting complexity-limit errors.*

 * created by **1-DARK**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#65309](https://github.com/microsoft/TypeScript/issues/65309) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**TS1450 \(wrong number of \`import\(\)\` arguments\) is reported with category "message" instead of "error"**

*The wrong number of import() arguments triggers TS1450 diagnostics with category message rather than error, misleading editors and tools.*

 * created by **trackoor**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/issues/65309#issuecomment-6635945208) **RyanCavanaugh** said "Linked PR is good but we should have had an assert that catches this earlier too"
 * **RyanCavanaugh** added to milestone `Backlog`

### [Issue microsoft/TypeScript#65311](https://github.com/microsoft/TypeScript/issues/65311) (Open, `Bug`)

**\`in\` inside an array literal in a \`for\` initializer is a syntax error \(\`for \(let i = 0, a = \[k in o\]; …\)\`\)**

*TypeScript incorrectly treats ‘in’ inside array literals within for-loop initializers as syntax errors, unlike similar contexts.*

 * created by **trackoor**
 * [today](https://github.com/microsoft/TypeScript/issues/65311#issuecomment-6629428265) **MartinJohns** said "Why would you ever write code like this?"
 * [today](https://github.com/microsoft/TypeScript/issues/65311#issuecomment-6637234888) **trackoor** explained finding the code pattern while comparing their parser against their own implementation and test262, noting it was an uncommon pattern

### [PR microsoft/TypeScript#65312](https://github.com/microsoft/TypeScript/pull/65312) (Closed, `For Milestone Bug`, **RyanCavanaugh**)

**Report an error when erasing as/satisfies exposes an invalid left operand of \*\***

*Report errors when using as/satisfies to wrap unary, await, or type assertions as the left operand of exponentiation.*

 * created by **0xABCD01**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed labels `For Backlog Bug`, `For Backlog Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/65312#issuecomment-6646449905) **RyanCavanaugh** said "Closing in favor of the other one"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65317](https://github.com/microsoft/TypeScript/pull/65317) (Closed, `For Milestone Bug`, **RyanCavanaugh**)

**Fix TS1450 diagnostic severity for invalid dynamic imports**

*Adjust TS1450 severity to error for invalid dynamic import() calls and regenerate diagnostic definitions and baselines.*

 * created by **OKAN-SOFTWARE**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **RyanCavanaugh**

### [PR microsoft/TypeScript#65318](https://github.com/microsoft/TypeScript/pull/65318) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Assert checker errors cannot use the Message diagnostic category**

*Reject Message-category diagnostics in Checker.addDiagnostic to ensure errors use the correct diagnostic category.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#65319](https://github.com/microsoft/TypeScript/pull/65319) (Open, `Author: Team`, `For Milestone Bug`, **gabritto**)

**Adjust folding range's end line only if closing bracket followed by non\-trivia**

*Modify TypeScript folding range end adjustment to only recede when closing brackets precede non-trivia or mapped content.*

 * created by **gabritto**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **gabritto**

### [PR microsoft/TypeScript#65320](https://github.com/microsoft/TypeScript/pull/65320) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add CRLF to LF conversion to \.git\-blame\-ignore\-revs**

*Add CRLF-to-LF conversion support in .git-blame-ignore-revs to correctly ignore line ending changes.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65321](https://github.com/microsoft/TypeScript/pull/65321) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Don't run go\-test\-wasm in merge queue CI**

*Disable go-test-wasm in merge queue CI to speed up merge validations.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65322](https://github.com/microsoft/TypeScript/pull/65322) (Open, `For Uncommitted Bug`)

**Honor VS Code language\-override precedence in configuration middleware**

*configurationMiddleware.ts ignores language-specific overrides and misorders settings, causing inconsistency with VS Code precedence and the built-in TypeScript extension*

 * created by **GoodForOneFare**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65322#issuecomment-6638833398) **GoodForOneFare** agreed with microsoft-github-policy-service on behalf of Shopify
 * [today](https://github.com/microsoft/TypeScript/pull/65322#issuecomment-6638841879) **GoodForOneFare** said "@microsoft-github-policy-service agree company=Shopify"
 * [today](https://github.com/microsoft/TypeScript/pull/65322#issuecomment-6639972717) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#65323](https://github.com/microsoft/TypeScript/pull/65323) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Reject unary exponentiation operands hidden by assertions**

*Reject unparenthesized unary or await expressions hidden by type assertions as exponentiation operands to prevent invalid JavaScript.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65323#issuecomment-6641528106) **RyanCavanaugh** said "@copilot+gpt-6.1-sol:xhigh ; expected is an unsatisfactory error message here, we should be issuing the same error for -n as any * 2 as if you had written -n * 2"
 * [today](https://github.com/microsoft/TypeScript/pull/65323#issuecomment-6642096105) **Copilot** addressed error reporting for bare and assertion-wrapped operands in commit b64beb298
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65324](https://github.com/microsoft/TypeScript/pull/65324) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Cherry\-pick tsgo PR 4661 to release\-7\.0**

*Cherry-pick microsoft/typescript-go PR 4661 into the release-7.0 branch to fix issues #63646 and #63678.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65325](https://github.com/microsoft/TypeScript/pull/65325) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fall back to inotify when fanotify rejects mounts with EXDEV**

*Fall back to inotify file monitoring when fanotify rejects mount events with EXDEV errors.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#65326](https://github.com/microsoft/TypeScript/issues/65326) (Open)

**Allow to influence trigger characters for files with content\-mappers**

*Allow content mappers to specify custom trigger characters for code completions in mapped files*

 * created by **dummdidumm**

### [PR microsoft/TypeScript#65327](https://github.com/microsoft/TypeScript/pull/65327) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reset pooled relaters in place**

*Resetting pooled relater fields individually instead of bulk copying reduces GC barrier overhead and cuts CPU usage from 0.7% to 0.06%.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65327#issuecomment-6647726556) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65327#issuecomment-6647727959) **typescript-automation[bot]** announced that performance test jobs had started and provided status and results links
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65327#issuecomment-6648506327) **typescript-automation[bot]** provided performance run results for baseline vs PR

### [PR microsoft/TypeScript#65328](https://github.com/microsoft/TypeScript/pull/65328) (Closed, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**add parseConfigFileTextToJson**

*Introduce parseConfigFileTextToJson function to parse TypeScript configuration file text into JSON*

 * created by **iisaduan**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **iisaduan**

### [PR microsoft/TypeScript#65329](https://github.com/microsoft/TypeScript/pull/65329) (Closed, `For Backlog Bug`)

**Fix printer: parenthesize member chains starting with an optional chain as callee of \`new\`**

*Parenthesize member chains starting with optional chains when printing new expressions to avoid mis-association in synthetic ASTs.*

 * created by **JemmyIndex**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65329#issuecomment-6650570361) **JemmyIndex** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/65329#issuecomment-6650861194) **JemmyIndex** closed the PR after finding that the existing behavior is intentional and changes would regress semantics; noted a transform invariant issue instead
 * (today) **JemmyIndex** closed the issue

### [PR microsoft/TypeScript#65330](https://github.com/microsoft/TypeScript/pull/65330) (Open, `For Uncommitted Bug`)

**fix\(parser\): allow \`in\` in array literals in a \`for\` statement initializer**

*Allow 'in' expressions inside array literals in for-statement initializers by clearing the DisallowInContext parsing flag.*

 * created by **JemmyIndex**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65331](https://github.com/microsoft/TypeScript/issues/65331) (Closed, `Working as Intended`)

**7\.1\.0\-beta reports TS5088 for a self\-referential const that 7\.0\.2 emits cleanly, including under \-\-noEmit**

*TypeScript 7.1.0-beta incorrectly reports TS5088 on a self-referential const during declaration emit even with --noEmit, whereas 7.0.2 emits cleanly.*

 * created by **donut-wenzhang**

### [PR microsoft/TypeScript#65332](https://github.com/microsoft/TypeScript/pull/65332) (Open, `For Backlog Bug`)

**Report JS diagnostics at missing nodes without skipping trivia**

*Use the parser’s getErrorSpanForNode for missing JavaScript nodes to correct diagnostic positions and prevent panics.*

 * created by **JemmyIndex**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#65333](https://github.com/microsoft/TypeScript/issues/65333) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**Downlevel \`this\.\#x &&= v\` / \`\|\|=\` / \`??=\` on a private accessor always calls the setter**

*TypeScript downlevel compilation of private accessor logical assignments (&&=, ||=, ??=) incorrectly always invokes the setter instead of short-circuiting.*

 * created by **trackoor**

### [Issue microsoft/TypeScript#65334](https://github.com/microsoft/TypeScript/issues/65334) (Closed, `Bug`, `External`, **RyanCavanaugh**, **Copilot**)

**Content mappers affected by node execve environment\-dropping bug**

*Content mappers fail to initialize on certain Node.js versions because process.execve drops environment variables and PATH entries, preventing executables like node from being found.*

 * created by **privatenumber**

