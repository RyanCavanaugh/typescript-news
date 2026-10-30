# Report for 2026-10-24 (Saturday, October 24th, 2026)

11 different users commented on 16 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#46532](https://github.com/microsoft/TypeScript/issues/46532) (Open, `Suggestion`, `Awaiting More Feedback`)

**support "star projections" in generics**

*Add star projection (*) support in TypeScript generics to omit unspecified type arguments like in Kotlin.*

 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/46532#issuecomment-1025473635) **blutorange** explained that when a type parameter is invariant you cannot use unknown or never and must use any or make the function generic, which can be cumbersome
 * [3.2 years ago](https://github.com/microsoft/TypeScript/issues/46532#issuecomment-1659893745) **wakaztahir** posted TypeScript code defining generic BlockModel and Block interfaces, concrete Paragraph and List implementations, and a blocks mapping
 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/46532#issuecomment-1787127427) **Schahen** provided another example illustrating how generic type annotations become redundant and suggested that star syntax could reduce the verbosity
 * [today](https://github.com/microsoft/TypeScript/issues/46532#issuecomment-6394624703) **DetachHead** said "an alternative solution would be to implement "top types" or "existential types", see discussion in https://github.com/facebook/pyrefly/issues/3736"

### [Issue microsoft/TypeScript#63979](https://github.com/microsoft/TypeScript/issues/63979) (Closed, `Out of Scope`, `Docs`)

**Official guidelines to build complex types**

*Proposal to add official TypeScript guidelines detailing supported tips, patterns, and pitfalls for constructing complex type definitions.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5457409158) **RyanCavanaugh** said "Regardless, the scope of the project is not really something you're going to change by commenting on an issue whether it's closed or open"
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5566337634) **denis-migdal** proposed collecting TypeScript tips and suggested using interfaces instead of concrete types, defining capacity-based interfaces, and employing symbols to hide internal data
 * [today](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-6382208348) **denis-migdal** provided several TypeScript tricks and tips including type assertions, casting avoidance, static hooks, and parameter bags
 * [later](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-6396284363) **denis-migdal** explained how to declare and export a type and value with the same name, including usage for classes and factories and how to re-export when importing the type from another file

### [PR microsoft/TypeScript#64781](https://github.com/microsoft/TypeScript/pull/64781) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Index structured type members without redundant symbol maps**

*Remove redundant name-to-symbol maps for resolved object types by using property lists and indexed slots, reducing memory usage.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64781#issuecomment-6174010155) **jakebailey** said "@typescript-bot perf test this faster"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64781#issuecomment-6174012515) **typescript-automation[bot]** announced that the perf test build started and provided links to its status and results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64781#issuecomment-6174536401) **typescript-automation[bot]** posted performance results for the requested perf run
 * [today](https://github.com/microsoft/TypeScript/pull/64781#issuecomment-6391335368) **jakebailey** said "@typescript-bot perf test"
 * [today](https://github.com/microsoft/TypeScript/pull/64781#issuecomment-6391336124) **typescript-automation[bot]** started perf test jobs and provided status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64781#issuecomment-6391649443) **typescript-automation[bot]** provided the performance run results

### [PR microsoft/TypeScript#64841](https://github.com/microsoft/TypeScript/pull/64841) (Open, `For Backlog Bug`)

**Invalidate declaration state when linked packages change**

*Store signatures of symlinked package directories and package.json entry fields to force declaration rebuilds when linked packages change.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64841#issuecomment-6210106648) **jackeddisciple** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64841#issuecomment-6384522466) **jasonkuhrt** thanked maintainers, described a stale declaration case involving nested package.json files, and asked whether including nested manifests in the PR signature would be appropriate while offering to add a test case
 * [today](https://github.com/microsoft/TypeScript/pull/64841#issuecomment-6384595844) **jackeddisciple** acknowledged the missing nested manifest case and said they would investigate how to include relevant manifests and add a regression test
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64841#issuecomment-6388350463) **jackeddisciple** described how the signature now tracks every package.json through linked packages and node_modules lookups, added dependencyUpdate tests for the reported case under incremental and watch, and confirmed the issue is fixed
 * [today](https://github.com/microsoft/TypeScript/pull/64841#issuecomment-6389040021) **jasonkuhrt** confirmed that on head commit aa080c4 tsc incremental builds matched forced builds across multiple repro cases, resolving stale errors present on base commit 8a62bbe

### [PR microsoft/TypeScript#64873](https://github.com/microsoft/TypeScript/pull/64873) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Don't resolve mapped type members to find their signatures**

*Avoid resolving mapped type members for signature checks to prevent unnecessary property building and improve compiler performance.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6376751550) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6376752833) **typescript-automation[bot]** started the perf test job and posted links to build status and results
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6377132981) **typescript-automation[bot]** posted the performance run results including a detailed comparison report
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64876](https://github.com/microsoft/TypeScript/pull/64876) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Count intersection property names with a plain map and slice**

*Count intersection property names using a plain map and slice, benchmark performance differences, and note conflict with issue #64815.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64876#issuecomment-6274666942) **jakebailey** said "@typescript-bot perf test this faster"
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64876#issuecomment-6274668722) **typescript-automation[bot]** reported that the 'perf test this faster' job had started with links to build and results
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64876#issuecomment-6275219511) **typescript-automation[bot]** reported requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64876#issuecomment-6391181434) **jakebailey** said "@typescript-bot perf test"
 * [today](https://github.com/microsoft/TypeScript/pull/64876#issuecomment-6391182586) **typescript-automation[bot]** announced that the perf test build job started and linked to its status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64876#issuecomment-6391487648) **typescript-automation[bot]** posted performance run results including a detailed comparison report of compiler metrics between baseline and pr

### [PR microsoft/TypeScript#64880](https://github.com/microsoft/TypeScript/pull/64880) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Memoize repeated inference walks**

*Implement memoization to cache and reuse results of repeated inference walks for performance improvement.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6279376021) **typescript-automation[bot]** reported that performance tests started and provided links for build status and results
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6279767469) **typescript-automation[bot]** provided the performance run results requested by @jakebailey
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6280682950) **frivanco97-cmd** said "Repositorios.. "
 * [today](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6391181190) **jakebailey** said "@typescript-bot perf test"
 * [today](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6391182173) **typescript-automation[bot]** reported that performance test jobs started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6391679634) **typescript-automation[bot]** provided the requested performance run results in a detailed comparison report

### [PR microsoft/TypeScript#64935](https://github.com/microsoft/TypeScript/pull/64935) (Open, `For Backlog Bug`)

**Don't measure type parameters as independent through circular variance lookups**

*Correct circular variance computation to disallow incompatible assignments between mutually recursive type aliases.*

 * [today](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6386179655) **typescript-automation[bot]** reported DT test results and branch-only TypeScript compile errors for react-relay
 * [today](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6386240501) **typescript-automation[bot]** provided perf run results for @ahejlsberg
 * [today](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6386252039) **typescript-automation[bot]** reported differences in user test results comparing baseline and PR and requested review
 * [today](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6386813789) **typescript-automation[bot]** reported build errors for DIYgod/RSSHub and every-app/open-seo when comparing baseline and pr

### [Issue microsoft/TypeScript#64953](https://github.com/microsoft/TypeScript/issues/64953) (Closed, `Bug`)

**Unsaved export not offered for auto\-import after reopening the importing file**

*TypeScript does not offer auto-import suggestions or import edits for functions defined in unsaved files when reopening the importing file.*

 * created by **johnsoncodehk**

### [Issue microsoft/TypeScript#64954](https://github.com/microsoft/TypeScript/issues/64954) (Open, `Bug`)

**Type annotations cause contextual \`this\` in object literal returned from an async function to be inferred as \`Promise\<This\> \| This\`**

*Async function type annotations cause object methods’ this to be inferred as a union with PromiseLike instead of the object type.*

 * created by **kanashimia**

### [Issue microsoft/TypeScript#64955](https://github.com/microsoft/TypeScript/issues/64955) (Closed, `Won't Fix`)

**Checking deeply nested array/object literals is quadratic and can hang in TS7**

*TypeScript 7’s checker exhibits quadratic time complexity for deeply nested array or object literals, causing compiler hangs on large depths.*

 * created by **qiyuhuating**

### [PR microsoft/TypeScript#64956](https://github.com/microsoft/TypeScript/pull/64956) (Closed, `For Uncommitted Bug`)

**Fix quadratic const\-context checking for deeply nested literals**

*Add per-node caching to Checker.isConstContext to change deeply nested literal const-context checks from quadratic time to linear time.*

 * created by **qiyuhuating**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64956#issuecomment-6394506819) **qiyuhuating** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64957](https://github.com/microsoft/TypeScript/issues/64957) (Closed, `Question`)

**type Exclude on class hierarchy resolves to never**

*Excluding a subclass from a union of structurally identical classes unexpectedly resolves to never in TypeScript.*

 * created by **xtnw**
 * [later](https://github.com/microsoft/TypeScript/issues/64957#issuecomment-6398117465) **jcalz** explained that TypeScript uses structural typing, linked to the handbook, and stated that the observed behavior is intentional and not a bug

