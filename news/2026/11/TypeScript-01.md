# Report for 2026-11-01 (Sunday, November 1st, 2026)

16 different users commented on 29 different issues.

## Recommended Actions

 * Response Recommended
    * @mwaibel-go reported that the feature landed in type-fest and provided issue and implementation links in [microsoft/TypeScript#48992](https://github.com/microsoft/TypeScript/issues/48992#issuecomment-6576674715)
    * @saair-quaderi asked when the upgrade would be available in [microsoft/TypeScript#64318](https://github.com/microsoft/TypeScript/pull/64318#issuecomment-6572763966)
    * @GoodbyeNJN provided detailed findings about duplicate inlay hints and a confirmation of the root cause in [microsoft/TypeScript#65092](https://github.com/microsoft/TypeScript/issues/65092#issuecomment-6560928348)

## Activity Summary

### [Issue microsoft/TypeScript#48992](https://github.com/microsoft/TypeScript/issues/48992) (Open, `Suggestion`, `Awaiting More Feedback`)

**Operator to produce keys of a type where the properties of that type in those keys match some type**

*Add a KeysOfType<T, P> type operator to extract the keys of T whose property types extend P.*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/48992#issuecomment-1870978637) **somebody1234** pointed out that it didn’t work on the base class and provided a working example via a Playground link
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/48992#issuecomment-2065557699) **Howard-Lam-UnitedVanning** reported that in a generic test, the 'e' field was inferred as never instead of number
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/48992#issuecomment-2460844436) **jesseditson** asked if his type issue was the same as a previous discussion
 * [later](https://github.com/microsoft/TypeScript/issues/48992#issuecomment-6576674715) **mwaibel-go** noted that the feature landed in 'type-fest' with links to the issue and implementation

### [Issue microsoft/TypeScript#63555](https://github.com/microsoft/TypeScript/issues/63555) (Closed, `Domain: Performance`, `Possible Improvement`)

**Quadratic check time for diamond\-shaped interface inheritance graphs**

*TypeScript exhibits quadratic check time when traversing base types in diamond-shaped interface inheritance graphs.*

 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/63555#issuecomment-4781962281) **canonic-epicure** said "Its a valid program after all => should compile."
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/63555#issuecomment-4785188567) **RyanCavanaugh** said "A Turing-complete system that can produce correct outputs in finite and bounded time is going to be extremely useful 😉"
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/63555#issuecomment-4785835932) **canonic-epicure** said "I agree, definitely, its very important to apply a proper fix."
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64262](https://github.com/microsoft/TypeScript/issues/64262) (Closed, `Bug`, `Domain: tsc -b`, **jakebailey**)

**Port \`DirWatchSet\` over to TS7**

*Cherry-pick commit e05860d9328a894189b49d9c43fb8a52e6c6d5a2 implementing DirWatchSet into a new 7.0.x branch of the TypeScript repository.*

 * **DanielRosenwasser** added label `Domain: tsc -b`
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/64262#issuecomment-5891481987) **Emut** expressed satisfaction with the nightly version and asked whether a 7.0.3 release will be available or if they should wait for 7.1.0
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/64262#issuecomment-5891943211) **CSenshi** expressed support for including the fix in version 7.0.3 and noted that TypeScript compilation is slow in large repositories
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64318](https://github.com/microsoft/TypeScript/pull/64318) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Cherry\-pick tsgo PR 4658 into release\-7\.0**

*Cherry-pick PR 4658 from tsgo into the release-7.0 branch to resolve issue 64262.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`
 * (2 days ago) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript/pull/64318#issuecomment-6572763966) **saair-quaderi** said "Thanks so much for this! Do we know when this might be available to upgrade to?"

### [PR microsoft/TypeScript#64658](https://github.com/microsoft/TypeScript/pull/64658) (Open, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Fix Windows module resolution for reserved path segments**

*Use extended path namespaces to prevent Windows reserved device names like con from blocking module resolution.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6070384917) **DanielRosenwasser** requested Copilot address CI failures and provided continuous integration failure logs
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6070559076) **Copilot** fixed the Windows short-path expectation, removed t.Parallel() from the allocation test, and adjusted cleanup to satisfy custom lint
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6070609937) **jakebailey** said "I don't think you can just remove Parallel without a nolint directive that says why"
 * [later](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6572393641) **itrapashko** asked DanielRosenwasser to review the outstanding nolint directive note still affecting Windows

### [PR microsoft/TypeScript#64737](https://github.com/microsoft/TypeScript/pull/64737) (Closed, `Domain: Performance`, `For Backlog Bug`)

**Avoid exponential base type search in hasBaseType**

*Change hasBaseType to avoid exponential exploration of shared interface base types, reducing type-checking time on deep inheritance chains.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64737#issuecomment-6118739780) **typescript-automation[bot]** announced that performance test build jobs started and provided links to status and results
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64737#issuecomment-6119059459) **typescript-automation[bot]** provided the requested performance run results in a detailed comparison table
 * **jakebailey** added label `Domain: Performance`
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64912](https://github.com/microsoft/TypeScript/issues/64912) (Open, `Needs Investigation`, **andrewbranch**)

**Content mappers: pass an import's query or attributes to \`transform\`**

*Allow content mappers to opt in to receiving import query parameters or import attributes in their transform calls to handle module variants.*

 * created by **colinhacks**
 * (6 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript/issues/64912#issuecomment-6575275078) **Knagis** described using import attributes with type options for SVG, PNG, and CSS files, noted issues with go-to-definition when using ambient module declarations, and suggested that content mappers would improve the development experience
 * [later](https://github.com/microsoft/TypeScript/issues/64912#issuecomment-6575354926) **Knagis** suggested registering content mapper based on type attribute regardless of file extension

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*Make the type checker fully order independent by replacing ID-based caching with content-based memos and order-variant tests.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6551788903) **typescript-automation[bot]** reported new TS7023 errors for implicit any return types in SchemaAST.ts when comparing baseline and pr
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6551896318) **typescript-automation[bot]** informed @jakebailey of the requested performance run results and presented comparison metrics
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6552290072) **typescript-automation[bot]** reported tsc build results for the top 400 repos, noted an interesting change, and provided failure details for cheaper-inference/OmniRoute
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6566981308) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6566982516) **typescript-automation[bot]** reported the start of multiple CI jobs with links to their statuses and results
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6567417024) **typescript-automation[bot]** reported DT test results with branch-only errors in d3-selection due to TypeScript compile errors
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6567487859) **typescript-automation[bot]** reported new TypeScript errors for implicit any return types in functions _rebuild and recur during tsc comparison
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6567682690) **typescript-automation[bot]** provided the perf run results requested by @jakebailey
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6568122632) **typescript-automation[bot]** reported build comparison results for top 400 repos showing new TypeScript errors

### [PR microsoft/TypeScript#65091](https://github.com/microsoft/TypeScript/pull/65091) (Closed, `For Milestone Bug`, **RyanCavanaugh**)

**Fill the config cycle into the TS18000 circularity message**

*Include the chain of configuration file paths causing a circular extends error in the TS18000 diagnostic message*

 * created by **cplieger**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65091#issuecomment-6560560316) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#65092](https://github.com/microsoft/TypeScript/issues/65092) (Open, `Suggestion`, `Declined`)

**Feature Request: Allow Content Mappers to opt\-in to transforming files end in built\-in extensions**

*Enable content mappers to opt in to transforming built-in TypeScript/JavaScript file extensions with scoped applicability and avoid duplicate LSP registrations.*

 * created by **GoodbyeNJN**
 * [today](https://github.com/microsoft/TypeScript/issues/65092#issuecomment-6560928348) **GoodbyeNJN** described a local experiment bypassing extension checks that led to duplicate inlay hints for .ts files and confirmed the cause by filtering out built-in JS/TS extensions

### [PR microsoft/TypeScript#65093](https://github.com/microsoft/TypeScript/pull/65093) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Use SymbolTables instead of maps for member layouts**

*Replacing maps with SymbolTables for member layouts reduces memory usage and restores declared member ordering from TypeScript 6.0.*

 * created by **ahejlsberg**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6564034992) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6564036179) **typescript-automation[bot]** posted CI job status updates including build and result links
 * [today](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6564457609) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6564527141) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6564652774) **typescript-automation[bot]** reported the results of the requested perf run
 * [today](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6565124402) **typescript-automation[bot]** provided build comparison results for top 400 repos between baseline and PR and noted an interesting change

### [Issue microsoft/TypeScript#65094](https://github.com/microsoft/TypeScript/issues/65094) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**TS18000 circularity message prints its {0} placeholder instead of the config chain**

*The circular configuration error TS18000 in TypeScript 7.x prints its {0} placeholder instead of listing the tsconfig files in the cycle.*

 * created by **cplieger**

### [Issue microsoft/TypeScript#65095](https://github.com/microsoft/TypeScript/issues/65095) (Open, `Bug`)

**TypeScript 7 memory grows without bound on a next\-intl call with a missing namespace and ICU arguments \(6\.0 stays at 2\.5 GB\)**

*TypeScript 7.0.2's memory usage grows indefinitely when compiling next-intl with a missing namespace and ICU arguments, unlike versions 6.0.3 and 5.9.3.*

 * created by **jcoulaud**

### [Issue microsoft/TypeScript#65096](https://github.com/microsoft/TypeScript/issues/65096) (Closed, `Question`)

**Clarify EULA and Background Sync provenance in TypeScript 5\.9\.3 third\-party notices**

*Clarify the applicable EULA for the DefinitelyTyped entry and the provenance, coverage, and licensing of the Web Background Synchronization notice in TypeScript 5.9.3’s third-party notices.*

 * created by **beefstew**

### [Issue microsoft/TypeScript#65097](https://github.com/microsoft/TypeScript/issues/65097) (Closed, `Needs Investigation`, **andrewbranch**, **Copilot**)

**Content mappers: a relative \`package\` path loads the package\.json of the nearest folder with node\_modules**

*A relative contentMappers package path resolves unexpectedly to the nearest node_modules package.json rather than the target mapper folder.*

 * created by **onmax**

### [Issue microsoft/TypeScript#65098](https://github.com/microsoft/TypeScript/issues/65098) (Open)

**TS7\.1 importing \.json with type: something still parses the JSON file even though ambient module declaration is used**

*TypeScript 7.1 still parses JSON imports with with { type: 'text' } despite an ambient module declaration preventing parsing.*

 * created by **Knagis**

### [PR microsoft/TypeScript#65099](https://github.com/microsoft/TypeScript/pull/65099) (Closed, `For Backlog Bug`)

**Report TS2516 for non\-consecutive abstract method declarations**

*Skip misnamed implementation checks for abstract methods so TS2516 is reported when their declarations are non-consecutive.*

 * created by **Shadow0Bit**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65099#issuecomment-6576739844) **Shadow0Bit** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#65100](https://github.com/microsoft/TypeScript/issues/65100) (Closed)

**getting started**

*Guidance request for getting started with blocks, tools, and framework, seeking collaboration and freelancing opportunities.*

 * created by **Program-creator122**

### [Issue microsoft/TypeScript#65101](https://github.com/microsoft/TypeScript/issues/65101) (Closed, `Duplicate`)

**Can you please add some new features for types: string length getter \(currently \`number\`\), string getter by index \(currently \`string\`\), array multiple spreads \(currently gives the error of type\)**

*Support exact string literal length, precise character indexing types, and multiple tuple spread elements in TypeScript.*

 * created by **mark-sss-coder**
 * [later](https://github.com/microsoft/TypeScript/issues/65101#issuecomment-6581326118) **nmain** suggested searching for each issue independently and identified the first idea as a duplicate of issue #34692

