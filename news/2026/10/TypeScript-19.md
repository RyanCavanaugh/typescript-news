# Report for 2026-10-19 (Monday, October 19th, 2026)

22 different users commented on 50 different issues.

## Recommended Actions

 * Moderation
    * @frivanco97-cmd posted unclear or off-topic content in [microsoft/TypeScript#64880](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6280682950)
 * Response Recommended
    * @erlichmen asked when the beta would be published or if a manual build from the release-7.1 branch is required in [microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6285163659)
    * @adilalperenciftci asked for another review and workflow approval in [microsoft/TypeScript#64360](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6289784750)
    * @smg99 asked for review from @jakebailey in [microsoft/TypeScript#64743](https://github.com/microsoft/TypeScript/pull/64743#issuecomment-6283523879)
    * @NullVoxPopuli-ai-agent provided repro steps as requested in [microsoft/TypeScript#64828](https://github.com/microsoft/TypeScript/issues/64828#issuecomment-6276004130)
    * @sunny-kavixo asked whether a maintainer could triage the issue and add it to the Backlog milestone in [microsoft/TypeScript#64875](https://github.com/microsoft/TypeScript/issues/64875#issuecomment-6283506910)
    * @dotnetCarpenter provided repro steps as requested in [microsoft/TypeScript#64881](https://github.com/microsoft/TypeScript/issues/64881#issuecomment-6285040519)

## Activity Summary

### [Issue microsoft/TypeScript#35909](https://github.com/microsoft/TypeScript/issues/35909) (Open, `Suggestion`, `Awaiting More Feedback`)

**Can't evaluate equality of symbols made by Symbol\.for**

*TypeScript treats Symbol.for calls as distinct types, causing erroneous type errors on equality comparisons and assignments.*

 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-1159692746) **pjeby** described a use case for interop using Symbol.for() and explained TypeScript's limitation without global symbol syntax
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-2585209754) **yuhr** reposted an excerpt from issue #60944 explaining the use-case for non-unique symbol keys to support multiple library versions and the compile-time issues with string keys
 * [19 weeks ago](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-4626919034) **lygstate** said "It's a bug, can it fixed? As Symbol.for("literal") basically act like "literal" with symbol attribute"
 * [today](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-6277055373) **michaelfig** encouraged people following the issue to review PR #64451 and provide feedback

### [Issue microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703) (Open, `Planning`)

**TypeScript 7\.1 Iteration Plan**

*Roadmap for TypeScript 7.1 detailing milestones and features across compiler, editor productivity, and performance enhancements.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6208709487) **typescript-automation[bot]** said "Hey, @DanielRosenwasser! I've created release-7.1 with version 7.1.0-beta for you."
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6209347620) **DanielRosenwasser** said "This must be that agentic coding thing everyone's been talking about."
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6209379214) **Smrtnyk** said "Can we expect beta blogpost soon?"
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6276784242) **DanielRosenwasser** said "Yes, hopefully tomorrow. Sorry everyone!"
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6276785916) **DanielRosenwasser** said "@typescript-bot sync release-7.1"
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6276787389) **typescript-automation[bot]** provided build status update
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6276993692) **typescript-automation[bot]** said "Hey, @DanielRosenwasser! I've pulled main into release-7.1 for you."
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6285163659) **erlichmen** asked when the 7.1.0-beta artifacts would be published and if users needed to build from the release-7.1 branch

### [PR microsoft/TypeScript#64360](https://github.com/microsoft/TypeScript/pull/64360) (Open, `For Backlog Bug`)

**Fix union overload signature ordering instability**

*Ensure consistent union overload resolution by ordering synthesized candidates based on each constituent’s signature precedence.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6096350640) **adilalperenciftci** followed up on the PR, stated the branch was rebased cleanly on main with no conflicts, and asked for a review of the revised getUnionSignatures approach
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6154780445) **jakebailey** said "I don't think this PR is right but can't put my finger on why. Figuring out why it feels wrong probably means I have to figure out a fix myself, which defeats the purpose a bit."
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6186149807) **adilalperenciftci** removed the exact-arity signature expansion, preserved union-signature matching by using constituents’ reorderCandidates precedence, and reported successful test and build validation
 * [later](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6289784750) **adilalperenciftci** updated the PR description and asked for another review and approval of pending workflows

### [PR microsoft/TypeScript#64376](https://github.com/microsoft/TypeScript/pull/64376) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Change the meaning of \`{}\` to \`unknown & not null & not undefined\`**

*Redefine {} as non-null unknown instead of unknown, null, or undefined and enhance type-origin tracking for literal unions.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-5765207254) **typescript-automation[bot]** said "Hey @weswigham, this PR changed while I was preparing the test run. Please try again."
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-5781570769) **weswigham** said "@typescript-bot test top1000"
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-5781572035) **typescript-automation[bot]** announced that jobs had started and test top1000 build had begun with updates to follow
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-6272165576) **weswigham** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-6272167221) **typescript-automation[bot]** reported build jobs started and provided status and result links for test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-6272738846) **typescript-automation[bot]** posted the requested performance run results including a comparison report of baseline versus PR metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-6278060293) **typescript-automation[bot]** notified that the DT test run failed and asked to check the log

### [PR microsoft/TypeScript#64411](https://github.com/microsoft/TypeScript/pull/64411) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Preserve primitive literal union origins without special intersections**

*Preserve literal union origins for string, number, and bigint in completions and quick info without special intersections.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6047591133) **typescript-automation[bot]** reported that test results comparing baseline and PR looked good
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6048381655) **typescript-automation[bot]** reported build results for the top 400 repos comparing baseline and PR and highlighted failures in pixijs
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6065878245) **weswigham** explained that test failures were expected follow-ons from removing mapped type behavior and suggested rewriting code to avoid denormalized union behavior
 * **weswigham** added to milestone `TypeScript 7.2.0 Beta`
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6273627260) **weswigham** assumed the change wouldn't be included in 7.1 post-beta, moved the PR to the 7.2 milestone, and requested eventual reviews and removal of the analogous change from #64376

### [Issue microsoft/TypeScript#64532](https://github.com/microsoft/TypeScript/issues/64532) (Open, `Needs Investigation`, **andrewbranch**)

**\[API\] \`getImmediateAliasedSymbol\` returns a different symbol than classic \`tsc\`**

*getImmediateAliasedSymbol for namespace imports in TypeScript 7 returns a cloned symbol instead of the original file symbol when a module has a default export.*

 * (2 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64532#issuecomment-6151189735) **andrewbranch** said "We have checker.getTargetSymbol(symbol). Does that not address this?"
 * [today](https://github.com/microsoft/TypeScript/issues/64532#issuecomment-6271815914) **dragomirtitian** said "@andrewbranch Does not seem to. getTargetSymbol returns the same symbol. "

### [PR microsoft/TypeScript#64659](https://github.com/microsoft/TypeScript/pull/64659) (Open, `For Uncommitted Bug`, **johnfav03**)

**Compute signatures of dependent files in parallel on incremental rebuilds**

*Declaration signatures for files dependent on an edited file are now computed in parallel during incremental rebuilds to significantly reduce build times.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6025077510) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** assigned to **johnfav03**
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6067067676) **resure** described changes to NewWorkGroup API by replacing singleThreaded with concurrency, removed the semaphore, applied limits per group, and reported unchanged performance
 * [today](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6272272305) **typescript-automation[bot]** reported build jobs starting and their result statuses
 * [today](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6272850835) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6272927629) **typescript-automation[bot]** provided the results of the performance run with a detailed comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6273501427) **typescript-automation[bot]** reported that test results comparing baseline and PR looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6274117618) **typescript-automation[bot]** reported that tsc runs on the top 400 repos comparing baseline and pr succeeded

### [PR microsoft/TypeScript#64679](https://github.com/microsoft/TypeScript/pull/64679) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add snapshot\.rebase\(newBaseSnapshot, changes\)**

*Add snapshot.rebase(newBaseSnapshot, changes) to overlay synthetic filesystem changes from an old snapshot onto a new one.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6279317955) **andrewbranch** suggested renaming the API to use snapshot.update({ fileSystem: ... }) with createFileSystemWithBase for layering synthetic file system updates

### [PR microsoft/TypeScript#64695](https://github.com/microsoft/TypeScript/pull/64695) (Open, `For Milestone Bug`, **ahejlsberg**)

**\[experiment\] Skip incompatible discriminants when inferring**

*Experimentally skip incompatible discriminant properties during TypeScript union type inference to reduce workload and validate via tests.*

 * **typescript-automation[bot]** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6269790663) **weswigham** noted a neutral to +8% performance impact, suggested caching discriminable item results or re-adding an optional prop fast path to improve performance, and asked for test cases demonstrating improved inference results, referencing a prior PR
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6270098644) **Andarist** mentioned having implemented the optional prop fast path locally and planning to push it and request a fresh rerun; noted having some test cases and intending to push them later this week; said they would review the linked PR and its tests
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6272440480) **jakebailey** said "I'd hope we can make the perf better still? I really hope to not make us slower if we can avoid it"

### [PR microsoft/TypeScript#64743](https://github.com/microsoft/TypeScript/pull/64743) (Open, `For Backlog Bug`)

**Fix enum crash when namespace and enum share a name**

*Guard enum value computation and treat ModuleBlock as a member container to prevent compiler panic when a namespace and enum share the same name.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64743#issuecomment-6140953790) **jakebailey** said "If you're not a person who can sign a CLA, I don't think you should be sending PRs"
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64743#issuecomment-6143495673) **smg99** said "@microsoft-github-policy-service agree"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64743#issuecomment-6207033948) **smg99** clarified that they were submitting the PR as an independent contributor, offered to sign the Microsoft CLA individually if needed, asked if any contributor verification was outstanding, and noted that the earlier AST MemberList review finding was addressed in commit d064a4c4
 * [today](https://github.com/microsoft/TypeScript/pull/64743#issuecomment-6283523879) **smg99** clarified that they had signed the LCA and requested a review from @jakebailey

### [PR microsoft/TypeScript#64750](https://github.com/microsoft/TypeScript/pull/64750) (Open, `For Uncommitted Bug`)

**Add support for Jujutsu conflict markers**

*Extend TypeScript’s conflict marker detection to support Jujutsu-style markers using %, \ and + separators.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6150291835) **RyanCavanaugh** inquired if opening an issue was mandatory or optional and suggested using an issue to discuss conflict marker forms
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6159916825) **rf-** said "Good points, thanks @jakebailey! Apologies for not covering all of the possible formats, it definitely makes sense to do them all at once. I'll open an issue to ref in the PR."
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6237153149) **rf-** questioned whether the couldStartTrivia function was vestigial dead code in Go and suggested its removal
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6278628845) **jakebailey** said "I think we can probably just do the simple easy version of this and it be sufficient; this is a best effort recovery after all so I think that's ok."

### [PR microsoft/TypeScript#64823](https://github.com/microsoft/TypeScript/pull/64823) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Client performance optimizations**

*Six independent client performance optimizations reduce processing time, memory allocations, and improve symbol lookup benchmark speeds.*

 * (5 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64823#issuecomment-6278993230) **andrewbranch** said "@typescript-bot perf test api"
 * [today](https://github.com/microsoft/TypeScript/pull/64823#issuecomment-6278994430) **typescript-automation[bot]** reported that the perf test api build started and provided status links
 * (today) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64823#issuecomment-6279330552) **typescript-automation[bot]** said "@andrewbranch, the perf run you requested failed. You can check the log here."

### [Issue microsoft/TypeScript#64828](https://github.com/microsoft/TypeScript/issues/64828) (Open, `Needs Investigation`, **andrewbranch**)

**Content mappers: go\-to\-definition on an module specifier returns nothing when the target file has more than one span\-map segment**

*Go-to-definition on module specifiers no longer finds .gts files containing multiple span-map segments after content mapper updates.*

 * (4 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * **andrewbranch** added to milestone `TypeScript 7.1.1 RC`
 * [today](https://github.com/microsoft/TypeScript/issues/64828#issuecomment-6276004130) **NullVoxPopuli-ai-agent** provided a minimal reproduction without Ember or Glint, corrected the trigger to export-from statements, and showed span-mapping outputs across TypeScript versions

### [PR microsoft/TypeScript#64834](https://github.com/microsoft/TypeScript/pull/64834) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**, **johnfav03**)

**Always cache \`getTypeOfSymbol\` and handle circularities**

*Unify caching and circularity handling in getTypeOfSymbol to fix flaky resolutions and inconsistent return types.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64834#issuecomment-6200956272) **typescript-automation[bot]** posted the requested perf run results comparing baseline and PR metrics
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64834#issuecomment-6200969765) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64834#issuecomment-6202184254) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [today](https://github.com/microsoft/TypeScript/pull/64834#issuecomment-6277006501) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64834#issuecomment-6277008424) **typescript-automation[bot]** reported that CI jobs started with status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64834#issuecomment-6277586469) **typescript-automation[bot]** provided the requested performance run results

### [PR microsoft/TypeScript#64837](https://github.com/microsoft/TypeScript/pull/64837) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Make LSP server load content mappers only from node\_modules inside workspace folders**

*Restrict TypeScript LSP server to load content mappers only from node_modules within workspace folders to prevent loading from untrusted directories.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64837#issuecomment-6203631315) **jakebailey** said "For that last commit, why can't we check this after tsoptions is done instead of having to reintroduce the config host?"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64837#issuecomment-6203732837) **andrewbranch** explained why performing the check during parsing was preferable, citing consistency with other diagnostics, ability to return a zero manifest, and prevention of unauthorized execution
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64837#issuecomment-6203852216) **jakebailey** said "That's fair, just lamenting a bit reintroducing that layer when I just got rid of it 😄 "
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64848](https://github.com/microsoft/TypeScript/issues/64848) (Open, `Domain: Performance`, `Possible Improvement`)

**TypeScript 7\.1 regression: quadratic root scanning in settled no\-op builds**

*TypeScript 7.1 regression causes no-op build performance degradation by quadratically scanning roots during up-to-date checks*

 * created by **turadg**
 * [today](https://github.com/microsoft/TypeScript/issues/64848#issuecomment-6277974971) **sunny-kavixo** thanked the previous commenter and stated an intention to independently verify the regression and share any findings

### [Issue microsoft/TypeScript#64852](https://github.com/microsoft/TypeScript/issues/64852) (Open, `Possible Improvement`)

**Support Jujutsu conflict markers**

*Add parsing support for Jujutsu's custom conflict marker syntax to prevent spurious TypeScript errors*

 * created by **rf-**
 * [today](https://github.com/microsoft/TypeScript/issues/64852#issuecomment-6278616021) **jakebailey** said "I think we can just do the simple version and it would probably be sufficient."

### [Issue microsoft/TypeScript#64855](https://github.com/microsoft/TypeScript/issues/64855) (Closed, `Design Limitation`)

**"This expression is not callable\." false positive on union of generic functions where the call is valid for all types in the union**

*TypeScript reports a false "not callable" error when calling a union of compatible generic functions.*

 * created by **DetachHead**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64855#issuecomment-6251795447) **jcalz** described known limitation of union call signatures allowing at most one overloaded and one generic member and noted that two generic members prevent unification
 * **RyanCavanaugh** added label `Design Limitation`
 * [today](https://github.com/microsoft/TypeScript/issues/64855#issuecomment-6275255340) **RyanCavanaugh** explained that there was no sound and performant fix, that the signature reduction rule didn’t apply, and that they wouldn’t add iterative mechanics due to potential exponential checking complexity

### [Issue microsoft/TypeScript#64864](https://github.com/microsoft/TypeScript/issues/64864) (Open, **andrewbranch**, **Copilot**)

**Some JS API types don't match their runtime values**

*Several TypeScript JS API type definitions in the sync and AST packages misrepresent actual runtime property types, causing mismatches.*

 * created by **auvred**
 * **jakebailey** assigned to **andrewbranch**

### [PR microsoft/TypeScript#64866](https://github.com/microsoft/TypeScript/pull/64866) (Closed, `Author: Team`, `For Uncommitted Bug`, **joj**)

**Use supported MicroBuild source\-analysis pool**

*Change sdl.sourceAnalysisPool from VSEngSS-MicroBuild2022-1ES to VSEng-MicroBuildVSStable in TypeScript and VSCode pipeline YAMLs.*

 * created by **joj**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **joj**
 * [today](https://github.com/microsoft/TypeScript/pull/64866#issuecomment-6271834331) **jakebailey** said "This is one file but that same pool is used in multiple different pipelines and they all need to be fixed."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64867](https://github.com/microsoft/TypeScript/pull/64867) (Open, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Restore behavior of getImmediateAliasedSymbol**

*Restore getImmediateAliasedSymbol’s previous behavior to ensure consistent TypeScript 6 API semantics.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64868](https://github.com/microsoft/TypeScript/pull/64868) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compare names before symbols when matching flow references**

*Compare declaration and reference names before symbol lookup to reduce analysis overhead and improve performance.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64868#issuecomment-6272836805) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64868#issuecomment-6272839100) **typescript-automation[bot]** started performance tests and posted links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64868#issuecomment-6273381312) **typescript-automation[bot]** provided the requested performance run results

### [PR microsoft/TypeScript#64869](https://github.com/microsoft/TypeScript/pull/64869) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Store merged symbols in a paged symbol link store**

*Use a paged symbol link store indexed by dense symbol IDs to avoid getMergedSymbol map misses and improve performance.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64869#issuecomment-6273344912) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64869#issuecomment-6273347159) **typescript-automation[bot]** started build jobs and posted status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64869#issuecomment-6274004601) **typescript-automation[bot]** posted the requested performance run results including a comparison report of tsc metrics such as errors, symbols, types, memory used, and memory allocations

### [PR microsoft/TypeScript#64870](https://github.com/microsoft/TypeScript/pull/64870) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Checker affinity tweaks**

*Tweak checker affinity settings to optimize resource allocation and improve performance*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6273341235) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6273343183) **typescript-automation[bot]** reported that performance tests started and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6273868261) **typescript-automation[bot]** posted the requested perf run results
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6275528700) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6275530895) **typescript-automation[bot]** announced that performance tests had started and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6276045335) **typescript-automation[bot]** posted the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6276396799) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6276398446) **typescript-automation[bot]** started build jobs and posted their initial status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6276934321) **typescript-automation[bot]** posted the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6281774913) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6281776110) **typescript-automation[bot]** started performance test jobs and posted build status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6282118799) **typescript-automation[bot]** provided the requested performance run results in a detailed report
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6283574843) **jakebailey** said "vscode is really sensitive to checker assignment, they have one file that takes a lot more time than otherwise, and benchmarks run unpinned and therefore we see noise"
 * [later](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6286028333) **jakebailey** explained why the bot regression on vscode and mui-docs occurred due to grouping files by directory and cost estimate inaccuracies, and outlined eight attempted scheduling variants
 * [later](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6286227764) **jakebailey** said "@typescript-bot perf test"
 * [later](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6286229347) **typescript-automation[bot]** reported start of perf test build jobs and provided status and results links
 * [later](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6286762401) **typescript-automation[bot]** reported the results of the requested performance run

### [PR microsoft/TypeScript#64871](https://github.com/microsoft/TypeScript/pull/64871) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid hashing keys in active mapper instantiation caches**

*Avoid hashing 128-bit keys for active mapper instantiations and instead use only the type ID when probing the cache.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6273514770) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6273516583) **typescript-automation[bot]** posted automated build status update
 * [today](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6274131092) **typescript-automation[bot]** posted perf run results for baseline..pr including metrics for compiler unions - native scenario such as errors, symbols, types, memory usage, and memory allocations

### [PR microsoft/TypeScript#64872](https://github.com/microsoft/TypeScript/pull/64872) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use paged link stores for all symbol links**

*Use paged link stores for all symbol link types to reduce map lookups and improve performance at minimal memory cost.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64872#issuecomment-6273530369) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64872#issuecomment-6273532095) **typescript-automation[bot]** started CI jobs and provided a status table
 * [today](https://github.com/microsoft/TypeScript/pull/64872#issuecomment-6274246320) **typescript-automation[bot]** reported the results of the requested perf run

### [PR microsoft/TypeScript#64873](https://github.com/microsoft/TypeScript/pull/64873) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Don't resolve mapped type members to find their signatures**

*Avoid resolving mapped type members for signature checks to prevent unnecessary property building and improve compiler performance.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6273551956) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6273553933) **typescript-automation[bot]** announced that performance tests had started and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6274310316) **typescript-automation[bot]** posted the requested perf run results including a comparison report and detailed metrics

### [PR microsoft/TypeScript#64874](https://github.com/microsoft/TypeScript/pull/64874) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Update CI workflow to include 'weswigham/\*' branches**

*Include 'weswigham/*' branches in the CI workflow so that stacked pull requests always trigger CI on push.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64875](https://github.com/microsoft/TypeScript/issues/64875) (Open, `Bug`, `Crash`, `Domain: tsc: --incremental`)

**Incremental compile panics on a failed output write, or never retries it**

*TypeScript incremental compilation panics on failed file writes when declarations are enabled and never retries writes otherwise.*

 * created by **YevheniiKotyrlo**
 * [today](https://github.com/microsoft/TypeScript/issues/64875#issuecomment-6275917842) **sunny-kavixo** thanked the reporter and said they started investigating the incremental compilation failures, planned to reproduce the issue, explore a minimal fix with regression tests, and prepare a PR if successful
 * [today](https://github.com/microsoft/TypeScript/issues/64875#issuecomment-6277364909) **YevheniiKotyrlo** said "Love it! Thank You @sunny-kavixo!"
 * [today](https://github.com/microsoft/TypeScript/issues/64875#issuecomment-6277558110) **sunny-kavixo** thanked @YevheniiKotyrlo and reported reproducing both behaviors, said they were working on a minimal fix and regression tests, and promised to share an update once validated
 * [today](https://github.com/microsoft/TypeScript/issues/64875#issuecomment-6283506910) **sunny-kavixo** completed a focused fix for issue #64875 addressing nil-pointer panic and output-write retries, passed regression and validation tests, and requested a maintainer to triage the associated issue and add it to the Backlog milestone

### [PR microsoft/TypeScript#64876](https://github.com/microsoft/TypeScript/pull/64876) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Count intersection property names with a plain map and slice**

*Count intersection property names using a plain map and slice, benchmark performance differences, and note conflict with issue #64815.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64876#issuecomment-6274666942) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64876#issuecomment-6274668722) **typescript-automation[bot]** reported that the 'perf test this faster' job had started with links to build and results
 * [today](https://github.com/microsoft/TypeScript/pull/64876#issuecomment-6275219511) **typescript-automation[bot]** reported requested performance run results

### [PR microsoft/TypeScript#64877](https://github.com/microsoft/TypeScript/pull/64877) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**LSP perf optimizations**

*LSP performance optimizations in the TypeScript compiler reduce time, memory, and allocations in VSCode benchmarks by up to 43%.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6275193723) **andrewbranch** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6275195944) **typescript-automation[bot]** reported start of performance tests and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6275829124) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6277582400) **andrewbranch** said "@typescript-bot perf test"
 * [today](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6277584246) **typescript-automation[bot]** reported that CI jobs for perf test started and provided links to build results
 * [today](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6278207578) **typescript-automation[bot]** posted the requested performance run results

### [PR microsoft/TypeScript#64878](https://github.com/microsoft/TypeScript/pull/64878) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Skip assignments when narrowing identifiers**

*Skip assignment operations during identifier narrowing to improve filtering accuracy.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64878#issuecomment-6276912429) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64878#issuecomment-6276914193) **typescript-automation[bot]** posted automated build start status for `perf test this faster` command
 * [today](https://github.com/microsoft/TypeScript/pull/64878#issuecomment-6277464418) **typescript-automation[bot]** reported the requested perf run results including a baseline vs PR comparison table

### [PR microsoft/TypeScript#64879](https://github.com/microsoft/TypeScript/pull/64879) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Remove package\.json "imports"**

*Remove package.json imports to support direct CDN loading and output enums in a top-level distribution folder*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64879#issuecomment-6278891207) **andrewbranch** said "Actually, I guess we could just put the enums in some other top-level directory besides dist, similar to vendor"

### [PR microsoft/TypeScript#64880](https://github.com/microsoft/TypeScript/pull/64880) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Memoize repeated inference walks**

*Implement memoization to cache and reuse results of repeated inference walks for performance improvement.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6279374891) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6279376021) **typescript-automation[bot]** reported that performance tests started and provided links for build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6279767469) **typescript-automation[bot]** provided the performance run results requested by @jakebailey
 * [today](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6280682950) **frivanco97-cmd** said "Repositorios.. "

### [Issue microsoft/TypeScript#64881](https://github.com/microsoft/TypeScript/issues/64881) (Closed)

**Missing Iterator Helper Methods on Generators in Vanilla JS using @ts\-check**

*TypeScript @ts-check doesn’t recognize iterator helper methods like reduce on generator and IteratorObject return types.*

 * created by **dotnetCarpenter**
 * [today](https://github.com/microsoft/TypeScript/issues/64881#issuecomment-6282435230) **bakkot** advised to set the target to ES2025 or later and provided a playground link
 * [today](https://github.com/microsoft/TypeScript/issues/64881#issuecomment-6285040519) **dotnetCarpenter** provided a jsconfig.json configuration with target set to es2025 and noted that VSCode 1.142.0 defaults to ES2024
 * (today) **dotnetCarpenter** closed the issue

### [Issue microsoft/TypeScript#64882](https://github.com/microsoft/TypeScript/issues/64882) (Open, `Bug`, **RyanCavanaugh**, **gabritto**, **Copilot**)

**7\.1 regression: import resolving to a non\-module file falls back to a pattern ambient module instead of TS2306**

*TypeScript 7.1 incorrectly applies a pattern ambient module for imports resolving to non-module files instead of reporting TS2306.*

 * created by **harshmandan**

### [Issue microsoft/TypeScript#64883](https://github.com/microsoft/TypeScript/issues/64883) (Open, `Bug`, `Domain: Parser`)

**Escaped \`in\` / \`instanceof\` after a class field initializer is parsed as a binary operator instead of a new member**

*TypeScript treats Unicode-escaped identifiers matching 'in' and 'instanceof' after class field initializers as binary operators, triggering errors.*

 * created by **JLHwung**

### [PR microsoft/TypeScript#64884](https://github.com/microsoft/TypeScript/pull/64884) (Open, `For Uncommitted Bug`)

**Preserve non\-module errors for imports without attributes**

*Ensure imports without attributes still produce non-module errors and avoid unintended ambient module resolution*

 * created by **Andarist**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#64885](https://github.com/microsoft/TypeScript/pull/64885) (Open, `For Backlog Bug`)

**fix\(64883\): fix asi before escaped keyword class members**

*Adjust automatic semicolon insertion behavior to correctly handle escaped keyword names in class members.*

 * created by **a-tarasyuk**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

