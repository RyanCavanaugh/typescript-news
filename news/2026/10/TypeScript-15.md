# Report for 2026-10-15 (Wednesday, October 14th, 2026)

17 different users commented on 45 different issues.

## Recommended Actions

 * Response Recommended
    * @sindresorhus asked if it would be possible to fallback to the original type alias in [microsoft/TypeScript#60913](https://github.com/microsoft/TypeScript/issues/60913#issuecomment-6175793428)
    * @louisscruz asked about optional Yarn PnP support and path to package map support in [microsoft/TypeScript#63919](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-6182431945)
    * @MARCROCK22 suggested closing the issue in [microsoft/TypeScript#64807](https://github.com/microsoft/TypeScript/issues/64807#issuecomment-6177387309)

## Activity Summary

### [Issue microsoft/TypeScript#38385](https://github.com/microsoft/TypeScript/issues/38385) (Open, `Suggestion`, `Awaiting More Feedback`)

**RFC: Support \_\_proto\_\_ literal in object initializers**

*Support __proto__ literals in object initializers so TypeScript correctly infers prototype properties, enforces valid values, and distinguishes computed __proto__ assignments.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/38385#issuecomment-2241524475) **mkermani144** described a workaround using a withProto wrapper function and noted it was a pain point
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/38385#issuecomment-2571385406) **HansBrende** noted that objects created with __proto__: null should not implicitly inherit Object properties and illustrated how toString() throws a TypeError unless __proto__ inherits Object properties or is absent
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/38385#issuecomment-3149651389) **DominoPivot** provided a TypeScript utility function to recursively infer types across an object's prototype chain and demonstrated its usage
 * [today](https://github.com/microsoft/TypeScript/issues/38385#issuecomment-6175448748) **0f-0b** pointed out that null-prototype objects natively support JSON serialization and that parsing support is in the proposal process

### [Issue microsoft/TypeScript#60913](https://github.com/microsoft/TypeScript/issues/60913) (Open, `Needs Investigation`, **weswigham**)

**\`\./\*\.d\.ts\` required in \`exports\` to avoid \`Cannot be named without a reference to\.\.\. not portable\.\.\.\`**

*Requiring explicit .d.ts exports in package.json to prevent TS 'not portable' errors inadvertently exposes declaration files.*

 * [52 weeks ago](https://github.com/microsoft/TypeScript/issues/60913#issuecomment-3387749485) **ethanresnick** noted that errors can appear suddenly due to TypeScript’s reduction behavior and suggested fallback processing for more stable output, illustrating with a reduced Tag<"bar", never> example
 * [52 weeks ago](https://github.com/microsoft/TypeScript/issues/60913#issuecomment-3391374216) **weswigham** explained that TypeScript reduces some types when not visible but treats distributive types like mapped and conditional types as irreducible, so inlining can change behavior and supporting a loosening carve-out is complex
 * [52 weeks ago](https://github.com/microsoft/TypeScript/issues/60913#issuecomment-3392515574) **ethanresnick** asked about the difference between irreducible and not inlinable types and why TS didn’t fully evaluate bound types before declaration emit
 * [today](https://github.com/microsoft/TypeScript/issues/60913#issuecomment-6175793428) **sindresorhus** explained a minimal reproduction of a TypeScript type alias loss issue from a library author perspective and asked if a fallback could preserve the original alias

### [Issue microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703) (Open, `Planning`)

**TypeScript 7\.1 Iteration Plan**

*Roadmap for TypeScript 7.1 detailing milestones and features across compiler, editor productivity, and performance enhancements.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5553473110) **jakebailey** said "Please file an issue if you have something that reproduces."
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5554066590) **earthboundkid** reminded participants to keep comments on-topic and focus on 7.1 progress
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6005102141) **DanielRosenwasser** said "Due to a lot of infrastructure issues, we'll be at least a few days late on beta."
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6180900245) **DanielRosenwasser** said "@typescript-bot create release-7.1"
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6180949387) **DanielRosenwasser** said "\more loudly and audibly annoyed\ I said, @typescript-bot create release-7.1"
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6180990822) **DanielRosenwasser** said "@typescript-bot create release-7.1"

### [PR microsoft/TypeScript#63919](https://github.com/microsoft/TypeScript/pull/63919) (Open, `For Uncommitted Bug`)

**Add Yarn PnP module resolution support**

*Add native Yarn Plug’n’Play module resolution support to TypeScript Go, including PnP VFS, API, and manifest handling.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5908981564) **futursolo** suggested supporting the Node.js loader API as a pathway to support PnP with smaller modifications and noted that package maps lack many PnP benefits
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5915375074) **jakebailey** explained that using the JS API would require executing content mappers and handling zip files, offering no advantage over package maps
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5928111641) **futursolo** suggested using the Node.js API's resolve source code content feature to avoid implementing zip file system
 * [today](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-6182431945) **louisscruz** asked about optional Yarn PnP support via a compiler flag and asked @arcanis for a path to Yarn + TypeScript package map support
 * [later](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-6186919893) **arcanis** opened issue #64827 to start a discussion about package map support in Yarn + TypeScript

### [Issue microsoft/TypeScript#64058](https://github.com/microsoft/TypeScript/issues/64058) (Closed, `Bug`)

**TS7: \`@extends\` is ignored when the heritage is a call expression \(Base\.extend\(\)\)**

*TypeScript 7’s JSDoc @extends tag is ignored for classes extending via call expressions (Base.extend()), causing unexpected type argument errors.*

 * created by **NullVoxPopuli**
 * (6 weeks ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64072](https://github.com/microsoft/TypeScript/pull/64072) (Closed, `For Backlog Bug`)

**fix\(64058\): fix reparse jsdoc @extends type arguments for call expressions**

*Corrects the re-parsing of JSDoc @extends type arguments in call expressions.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64072#issuecomment-6154904228) **jakebailey** revisited the implementation and requested two tweaks, supplying a test case
 * [today](https://github.com/microsoft/TypeScript/pull/64072#issuecomment-6171794220) **jakebailey** pointed out that extends null now gets type arguments and asked to skip KindNullKeyword in the reparser and add a test
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64360](https://github.com/microsoft/TypeScript/pull/64360) (Open, `For Backlog Bug`)

**Fix union overload signature ordering instability**

*Ensure consistent union overload resolution by ordering synthesized candidates based on each constituent’s signature precedence.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5843031820) **adilalperenciftci** rebased cleanly on current main and asked if the revised getUnionSignatures arity expansion was preferable or if union overload matching should be handled differently
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6096350640) **adilalperenciftci** followed up on the PR, stated the branch was rebased cleanly on main with no conflicts, and asked for a review of the revised getUnionSignatures approach
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6154780445) **jakebailey** said "I don't think this PR is right but can't put my finger on why. Figuring out why it feels wrong probably means I have to figure out a fix myself, which defeats the purpose a bit."
 * [today](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6186149807) **adilalperenciftci** removed the exact-arity signature expansion, preserved union-signature matching by using constituents’ reorderCandidates precedence, and reported successful test and build validation

### [PR microsoft/TypeScript#64551](https://github.com/microsoft/TypeScript/pull/64551) (Closed, `For Uncommitted Bug`)

**perf\(checker\): fast\-path compareNodes for identical AST parent containers and use cmp\.Compare**

*Introduces a fast-path compareNodes for identical AST parents and uses cmp.Compare to prevent 64-bit symbol ID overflow.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-6157165515) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-6157166753) **typescript-automation[bot]** reported initiation of perf test jobs and provided status links
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-6157530877) **typescript-automation[bot]** provided the requested performance run results
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64734](https://github.com/microsoft/TypeScript/pull/64734) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Various memory optimizations**

*Combined memory optimizations reduce memory usage by 22–29% and allocation counts by 3.6–16.6% across nine test scenarios.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6134654273) **jakebailey** removed changes from PR #64735 while retaining issue #64063 and requested performance tests
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6134655235) **typescript-automation[bot]** initiated performance test builds and provided status and results links
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6134989198) **typescript-automation[bot]** provided the performance run results with a comparison report for tsc metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6173691806) **jakebailey** said "The remaining work is now in independent PRs: #64775, #64781, #64788, #64789, #64791, #64815."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64742](https://github.com/microsoft/TypeScript/issues/64742) (Open, `Bug`)

**Language server \(tsc \-\-lsp\) exits with code 1 after \`shutdown\` and \`exit\`**

*TypeScript 7's LSP server unexpectedly exits with code 1 after receiving shutdown and exit notifications*

 * created by **creasty**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64760](https://github.com/microsoft/TypeScript/issues/64760) (Open, `Bug`, **weswigham**)

**Declaration emit writes = Infinity initializers for overflowing number literals \(invalid \.d\.ts, TS1254\)**

*TypeScript's declaration emit incorrectly uses Infinity and -Infinity initializers for overflowing numeric literals in .d.ts files, causing TS1254 errors.*

 * created by **sidcraftscode**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript#64763](https://github.com/microsoft/TypeScript/issues/64763) (Closed, `Won't Fix`)

**Parser: exponential time and memory on nested \`a \< \(b = …\)\` \(failed type argument speculation is retried\)**

*Nested 'a < (b = …)' expressions trigger exponential parsing time and memory growth in TypeScript due to retrying failed type argument speculation.*

 * created by **moznion**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64763#issuecomment-6139366580) **moznion** said "I’ve already prepared a patch in https://github.com/microsoft/TypeScript/compare/main...moznion:TypeScript:fix/parser-type-arguments-retry, so I’d be happy to submit a pull request to fix this issue."
 * [today](https://github.com/microsoft/TypeScript/issues/64763#issuecomment-6174547190) **RyanCavanaugh** mentioned receiving flack for memory usage and stated that increasing memory for degenerate code wasn't a good trade-off and they'd reevaluate if it had a legitimate use case
 * **RyanCavanaugh** added label `Won't Fix`

### [PR microsoft/TypeScript#64764](https://github.com/microsoft/TypeScript/pull/64764) (Closed, `For Uncommitted Bug`)

**Update localization files**

*Update localization files and regenerate corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64765](https://github.com/microsoft/TypeScript/pull/64765) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Resolve class and interface members through shared layouts**

*Introduce shared member layouts and lazy resolution for class and interface instantiations to significantly reduce memory usage and symbol creation.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6142771607) **typescript-automation[bot]** announced the requested performance run results with a detailed comparison report
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6142780972) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6143576591) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6174724968) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6174726844) **typescript-automation[bot]** started performance test jobs and posted status table
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6175347381) **typescript-automation[bot]** reported performance run results for the requested comparison between baseline and PR, including metrics for errors, symbols, types, and memory usage
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6179791206) **jakebailey** requested tests be run by the TypeScript bot
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6179792417) **typescript-automation[bot]** said "Hey @jakebailey, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6180066521) **jakebailey** requested tests be run by the TypeScript bot
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6180067808) **typescript-automation[bot]** announced build jobs starting and provided status and results links for commands 'user test this' and 'test top1000'
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6180447586) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6181783359) **typescript-automation[bot]** reported test results for the top 1000 repositories and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6184734512) **jakebailey** requested tests from the typescript-bot
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6184735630) **typescript-automation[bot]** updated build job statuses
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6185076229) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6187294341) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6187296535) **typescript-automation[bot]** reported starting the perf test job and provided status and result links
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6187748114) **typescript-automation[bot]** provided performance run results for tsc comparing baseline to PR

### [PR microsoft/TypeScript#64775](https://github.com/microsoft/TypeScript/pull/64775) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compress paged link\-store references**

*Convert pointer-sized page entries in dense checker link stores to four-byte arena indexes, halving storage and eliminating pointers.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (yesterday) **jakebailey** closed the issue
 * (yesterday) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64775#issuecomment-6174009534) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64775#issuecomment-6174011605) **typescript-automation[bot]** reported that performance tests started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64775#issuecomment-6174935260) **typescript-automation[bot]** provided perf run results as requested
 * [today](https://github.com/microsoft/TypeScript/pull/64775#issuecomment-6175006477) **jakebailey** said "This one's a bit pitiful. Basically the strategy is to make stores hold indexes into a dense array instead of always placing in sparse. But it's more complicated."

### [PR microsoft/TypeScript#64781](https://github.com/microsoft/TypeScript/pull/64781) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Index checker members without redundant symbol maps**

*Use ordered property lists and pointer-free integer slots instead of redundant symbol maps, decreasing heap retention and GC scanning.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64781#issuecomment-6174010155) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64781#issuecomment-6174012515) **typescript-automation[bot]** announced that the perf test build started and provided links to its status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64781#issuecomment-6174536401) **typescript-automation[bot]** posted performance results for the requested perf run

### [PR microsoft/TypeScript#64788](https://github.com/microsoft/TypeScript/pull/64788) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Store ordinary relationship keys as exact type ID pairs**

*Store ordinary comparison keys as 64-bit type ID pairs instead of 128-bit hashes, improving memory usage.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64788#issuecomment-6174010677) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64788#issuecomment-6174013513) **typescript-automation[bot]** provided an update that the performance test had started with links to build and results
 * [today](https://github.com/microsoft/TypeScript/pull/64788#issuecomment-6174651792) **typescript-automation[bot]** posted requested performance run results

### [PR microsoft/TypeScript#64789](https://github.com/microsoft/TypeScript/pull/64789) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Share complete union and intersection property cache entries**

*Share complete property cache entries between augmented and non-augmented lookups to reduce duplicate entries, memory usage, and GC scanning overhead.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64789#issuecomment-6174011075) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64789#issuecomment-6174014470) **typescript-automation[bot]** reported build jobs started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64789#issuecomment-6174849745) **typescript-automation[bot]** provided the requested performance run results

### [PR microsoft/TypeScript#64801](https://github.com/microsoft/TypeScript/pull/64801) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep optional type\-node and signature state out of hot records**

*Relocate optional outer type parameters and signature state out of hot records to reduce memory usage.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64802](https://github.com/microsoft/TypeScript/pull/64802) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Bound arena retention by bytes instead of object count**

*Use 512-byte arena chunks instead of fixed object counts to reduce memory retention and GC at cost of more allocations.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64803](https://github.com/microsoft/TypeScript/pull/64803) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use paged indexes for type\-node and signature caches**

*Replace AST pointer maps with paged indexes keyed by stable node IDs for type-node and signature caches to reduce memory usage.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64804](https://github.com/microsoft/TypeScript/pull/64804) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reuse ordered property counts during intersection reduction**

*Reuse bounded, checker-local property-count tables in intersection reduction to reduce allocated memory by 26.6%, allocations by 7.6%, and CLI instructions by 8.9%.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64804#issuecomment-6162382028) **DanielRosenwasser** said "Weird that we need a free list. Maybe it's worth exploring a pool of 16, a bitset that indicates which one is currently in use, and just allocates if they're all occupied."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64807](https://github.com/microsoft/TypeScript/issues/64807) (Closed, `Working as Intended`)

**\`\-\-stableTypeOrdering\`: \`unknown \|\| {}\` is assignable to \`Record\<string, T\>\` in 6\.0\.3 with the option, and not in 7\.0\.2 nor in 6\.0\.3 without it**

*With --stableTypeOrdering, TS 6.0.3 allows unknown||{} to be assigned to Record<string, number>, unlike TS 6.0.3 without it and TS 7.0.2.*

 * created by **MARCROCK22**
 * [today](https://github.com/microsoft/TypeScript/issues/64807#issuecomment-6166781526) **Andarist** said "FWIW, the diff between TS 6 and TS 7 is this: https://github.com/microsoft/typescript-go/pull/1603 and it's an intended change. It was just not backported to TS 6 (and my bet is that it won't be)."
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/64807#issuecomment-6177387309) **MARCROCK22** said "I guess this issue should be closed then"

### [Issue microsoft/TypeScript#64809](https://github.com/microsoft/TypeScript/issues/64809) (Closed, `Declined`)

**TS 7: backport typescript\-go\#4665 to a 7\.0\.x patch release; the same bug also drops declaration emit**

*Dependent .d.ts files aren’t re-emitted in TypeScript 7.0.2’s isolatedModules incremental build after global-scope changes, so microsoft/typescript-go#4665 must be backported to a 7.0.x patch release.*

 * created by **Nabil372**
 * [today](https://github.com/microsoft/TypeScript/issues/64809#issuecomment-6174584122) **RyanCavanaugh** said "We don't backport fixes of this nature - only critical security or stability issues."
 * **RyanCavanaugh** added label `Declined`
 * [today](https://github.com/microsoft/TypeScript/issues/64809#issuecomment-6178719017) **Nabil372** thanked the maintainer and expressed eagerness for the 7.1 release
 * (today) **Nabil372** closed the issue

### [PR microsoft/TypeScript#64815](https://github.com/microsoft/TypeScript/pull/64815) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid short\-lived allocations in union and intersection property handling**

*Optimize union and intersection property enumeration by eliminating short-lived allocations, reducing memory usage and improving performance.*

 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64815#issuecomment-6174011628) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64815#issuecomment-6174015419) **typescript-automation[bot]** indicated the start of performance test jobs and provided links to the build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64815#issuecomment-6174755572) **typescript-automation[bot]** posted the requested perf run results for tsc comparing baseline and PR

### [PR microsoft/TypeScript#64816](https://github.com/microsoft/TypeScript/pull/64816) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use small slices for union and intersection property sources**

*Use plain slices for union and intersection properties until a size threshold to reduce allocations and memory usage.*

 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64816#issuecomment-6173689076) **jakebailey** said "Folded into #64815."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64817](https://github.com/microsoft/TypeScript/pull/64817) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reuse name sets when enumerating union and intersection properties**

*Reuse name sets from a per-checker free list for union and intersection enumeration, cutting allocated bytes 6.76% and allocations 0.60%.*

 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64817#issuecomment-6173690613) **jakebailey** said "Folded into #64815."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64818](https://github.com/microsoft/TypeScript/pull/64818) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Fix named pipe / UDS creation**

*Use secure temporary directories with restrictive permissions for Unix domain sockets and random Windows pipe names for API clients.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64818#issuecomment-6180210854) **andrewbranch** said "@typescript-bot cherry-pick this to release-7.0"
 * [today](https://github.com/microsoft/TypeScript/pull/64818#issuecomment-6180211937) **typescript-automation[bot]** started jobs and posted build status for cherry-pick to release-7.0
 * [today](https://github.com/microsoft/TypeScript/pull/64818#issuecomment-6180234331) **typescript-automation[bot]** reported inability to cherry-pick the PR and pointed to logs

### [PR microsoft/TypeScript#64819](https://github.com/microsoft/TypeScript/pull/64819) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Recycle type checkers under a configurable memory budget**

*Introduce an opt-in maxMemory option to recycle type checkers and cap memory usage during non-incremental type checking*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64819#issuecomment-6179426965) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64819#issuecomment-6179428536) **typescript-automation[bot]** said "Hey @DanielRosenwasser, this PR was updated less than two minutes before this command. Please wait until it has been unchanged for two minutes and try again."

### [Issue microsoft/TypeScript#64820](https://github.com/microsoft/TypeScript/issues/64820) (Open)

**Changing importModuleSpecifier or importModuleSpecifierEnding does not update auto\-import specifiers in open files**

*Changing importModuleSpecifier or importModuleSpecifierEnding preferences does not update auto-import suggestions in already open files until they are reopened.*

 * created by **lsh4711**

### [PR microsoft/TypeScript#64821](https://github.com/microsoft/TypeScript/pull/64821) (Open, `For Uncommitted Bug`)

**Clear auto\-import specifier cache when module specifier preferences change**

*Clear auto-import specifier cache on any module specifier preference change to ensure updated import suggestions for open files.*

 * created by **lsh4711**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#64822](https://github.com/microsoft/TypeScript/pull/64822) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Cherry\-pick \#64818 into release\-7\.0**

*Cherry-pick pull request 64818 into the release-7.0 branch.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64823](https://github.com/microsoft/TypeScript/pull/64823) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Client performance optimizations**

*Six independent client performance optimizations reduce processing time, memory allocations, and improve symbol lookup benchmark speeds.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64824](https://github.com/microsoft/TypeScript/issues/64824) (Open)

**\[api\] createSnapshot panics opening a project that extends into a circular extends chain**

*createSnapshot panics when opening a second TypeScript project that extends into a circular configuration chain*

 * created by **cplieger**

### [PR microsoft/TypeScript#64825](https://github.com/microsoft/TypeScript/pull/64825) (Open, `For Uncommitted Bug`)

**\[api\] Reparse extended configs cached under another resolution stack**

*Extended config cache wrongly reuses entries from circular tsconfig chains, causing snapshot panics or hangs without proper resolution stack context.*

 * created by **cplieger**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64826](https://github.com/microsoft/TypeScript/pull/64826) (Open, `Author: Team`, `For Uncommitted Bug`)

**Update localization files**

*Update localization files and regenerate corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64827](https://github.com/microsoft/TypeScript/issues/64827) (Open)

**Support package maps**

*Support Node.js experimental package maps in TypeScript with a new compiler option for module resolution.*

 * created by **arcanis**

### [Issue microsoft/TypeScript#64828](https://github.com/microsoft/TypeScript/issues/64828) (Open, `Needs Investigation`, **andrewbranch**)

**Content mappers: go\-to\-definition on an module specifier returns nothing when the target file has more than one span\-map segment**

*Go-to-definition on module specifiers no longer finds .gts files containing multiple span-map segments after content mapper updates.*

 * created by **NullVoxPopuli**

### [Issue microsoft/TypeScript#64829](https://github.com/microsoft/TypeScript/issues/64829) (Closed)

**\[api\] WeakSet in generator execution causes significant slow down\.**

*Using a WeakSet to track generator usage in batch execution significantly slows performance compared to a symbol-based approach.*

 * created by **dragomirtitian**

### [PR microsoft/TypeScript#64830](https://github.com/microsoft/TypeScript/pull/64830) (Closed, `For Uncommitted Bug`)

**Avoid weakset for executed generators**

*Replace WeakSet with a global symbol marker to track executed generators and prevent their reuse*

 * created by **dragomirtitian**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

