# Report for 2026-08-13 (Thursday, August 13th, 2026)

17 different users commented on 40 different issues.

## Recommended Actions

 * Response Recommended
    * @safal207 provided source-level verification results as requested in [microsoft/TypeScript-go#1493](https://github.com/microsoft/TypeScript-go/issues/1493#issuecomment-5288572532)
    * @robertkirkman provided confirmation of testing results in [microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5288657980)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4903](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5290957829)
    * @typescript-automation provided perf results as requested in [microsoft/TypeScript-go#4903](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5293644618)

## Activity Summary

### [Issue microsoft/TypeScript-go#1493](https://github.com/microsoft/TypeScript-go/issues/1493) (Closed, `Domain: CLI`, **jakebailey**, **Copilot**)

**Exit code for type error is incorrect starting from \`7\.0\.0\-dev\.20250724\.1\`**

*tsgo in @typescript/native-preview@7.0.0-dev.20250724.1 returns exit code 1 for type errors instead of the expected code 2.*

 * (5 weeks ago) **jakebailey** set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 Stable`
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/1493#issuecomment-4944032445) **safal207** reported that the exit-status difference still reproduces with TypeScript 7.0.2 on all GitHub-hosted OS and provided detailed environment, test profile, and evidence confirming stability for issue #4407
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/1493#issuecomment-5288572532) **safal207** verified post-fix behavior on Ubuntu, Windows, and macOS using the merged commit, observed TS2322 errors with exit code 2, and provided evidence links

### [PR microsoft/TypeScript-go#3627](https://github.com/microsoft/TypeScript-go/pull/3627) (Closed, `No linked issue`)

**Runtime tracing, flight recording**

*Integrate Go runtime/trace support and flight recording into the VS Code extension similarly to pprof profiling.*

 * created by **jakebailey**
 * (12 weeks ago) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3627#issuecomment-5286871794) **jakebailey** said "This is not going to happen before the repo move, closing an will do another day."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3880](https://github.com/microsoft/TypeScript-go/pull/3880) (Closed)

**Re\-add diagnostics consistency check**

*Re-add diagnostics consistency check after resolving emit errors and symbol lookup issues, dropping redundant diagnostics.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#4218](https://github.com/microsoft/TypeScript-go/pull/4218) (Closed, `Voight-Kampff Anomaly`)

**Allow lone & in Unicode sets regexp classes**

*Update native scanner to allow lone & in Unicode Set regex character classes while preserving && intersections.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4796094461) **graphemecluster** noted the small fix looked fine but mentioned preferring to port PR #62716 if its scope met expectations
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4969251422) **Ijtihed** said "so what's the consensus here? :) I can close if needed"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-5104213104) **Ijtihed** asked if there was anything left for them to do
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4313](https://github.com/microsoft/TypeScript-go/pull/4313) (Closed)

**Assign files to checkers using balanced import affinity**

*A FENNEL-based balanced import affinity algorithm replaces round-robin checker assignment to boost checking performance and reduce memory usage by 10%.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5254846282) **RyanCavanaugh** suggested giving a parameter sweep for the remaining constant factor and said the code looked good
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5271320890) **jakebailey** said "It did actually sweep that; I did just have it retry and 100 is still the best in what projects I have."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5271326245) **jakebailey** said "I will let it update some comments afterward, though, so will probably push soon when it's done benchmarking"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4407](https://github.com/microsoft/TypeScript-go/pull/4407) (Closed, **jakebailey**, **Copilot**)

**Restore tsgo noEmit exit status semantics**

*Restore tsgo’s noEmit exit status semantics by porting tsc’s handleNoEmitOptions logic to ensure exit code 2 for type errors*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5270347126) **jakebailey** said "Nope, they flipped the author order in the commits so now it doesn't think you pushed it"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5270391379) **Copilot** updated the native-preview `noEmit` expectations to match upstream `emitSkipped: false` semantics and confirmed that tests passed
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5270480799) **jakebailey** said "Ah, but it finished and then rerequested a review, invalidating it"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Open)

**Content mappers**

*Support external content mappers in tsconfig to transform and map unsupported file types into valid TypeScript*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5274755525) **andrewbranch** said "I’ve somewhat reluctantly added a way to support ` and explained why it can’t just translate into // @ts-expect-error`."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5275507907) **andrewbranch** benchmarked a Copilot-generated content mapper against vue-tsc on 222 fixtures, found it 2.4× faster with 24% less memory, noted scaffolding parse and type errors, and shared a branch for reference
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5279235915) **remcohaszing** suggested adding logging support via a `tsc --verbose` flag and LSP `log` notifications for both editor and CLI
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5287957894) **andrewbranch** said "Bikeshed request: I don’t love the name "tsContentMapper" for the mapper package.json key. Any better ideas?"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5290710912) **remcohaszing** suggested using a JSONC snippet with a typescript.contentMapper namespace for future reuse

### [PR microsoft/TypeScript-go#4714](https://github.com/microsoft/TypeScript-go/pull/4714) (Closed, **andrewbranch**)

**feat\(47595\): allow using private fields in type queries**

*Enable referencing private class fields in TypeScript type queries.*

 * created by **a-tarasyuk**
 * **RyanCavanaugh** assigned to **andrewbranch**
 * (today) **a-tarasyuk** closed the issue

### [PR microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734) (Open)

**Add Android ARM64 release target**

*Add Android ARM64 release target to the build configuration*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5268571846) **jakebailey** clarified that the previous remark sounded like a complaint and explained he found the termux case simpler but hadn’t tested the PR since returning from a conference
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5270017668) **dlecan** referenced similar PRs in the Node ecosystem and suggested focusing on Android because Node apps run slowly on Proot
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5271186367) **sylirre** said "https://github.com/microsoft/typescript-go/issues/4718 will be resolved on the proot side in pending release."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5287189401) **jakebailey** said "Ok, I have this PR where I want it, besides the artifact uploading. If you can, please test it before I remove the artifact stuff and go for a merge."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5288657980) **robertkirkman** said "I have tested this again, and it continues to work as expected in both F-Droid Termux and Google Play Termux."

### [Issue microsoft/TypeScript-go#4752](https://github.com/microsoft/TypeScript-go/issues/4752) (Closed, `Crash`, **jakebailey**, **Copilot**)

**\`tsconfig\.json\`: \`{"" }\` causes a panic, and more TS errors than v6**

*An empty tsconfig.json literal {} crashes the compiler with a 'negative Repeat count' panic and produces more errors than TypeScript v6.*

 * (2 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4762](https://github.com/microsoft/TypeScript-go/pull/4762) (Closed, **jakebailey**, **Copilot**)

**Prevent panic and duplicate diagnostics for malformed tsconfig properties**

*Normalized recovered JSON node spans and suppressed redundant diagnostics to prevent panics and duplicate errors from malformed tsconfig properties.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4809](https://github.com/microsoft/TypeScript-go/issues/4809) (Closed, `Crash`, **jakebailey**, **Copilot**)

**LSP exits when parent process PID is not found**

*LSP’s parent-PID watchdog terminates the server when the PID can’t be found in Docker, with a CLI flag to disable it.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5222278230) **jakebailey** said "How does that help your case? If you're launching in docker, how would you know the PID ahead of time if it's inside a container or something?"
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5233282616) **mj026** explained that the real parent process isn't visible in a container and demonstrated that the init process appears as PID 1
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5243409670) **jakebailey** said "Given https://github.com/microsoft/vscode-languageserver-node/blob/0b6b07cdbed310771ac26267109c1db22ee62a2b/client/src/node/main.ts#L375 we can probably just use this flag, yeah"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4828](https://github.com/microsoft/TypeScript-go/pull/4828) (Closed, `dependencies`, `javascript`)

**Bump undici from 7\.28\.0 to 7\.29\.0**

*Upgrade undici from 7.28.0 to 7.29.0 to address high and medium severity security vulnerabilities.*

 * (1 week ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4828#issuecomment-5287421493) **dependabot[bot]** explained how to ignore dependency update notifications or reopen the PR to resolve conflicts

### [PR microsoft/TypeScript-go#4833](https://github.com/microsoft/TypeScript-go/pull/4833) (Closed, `dependencies`, `javascript`)

**Bump fast\-uri from 3\.1\.2 to 3\.1\.5**

*Bump fast-uri from 3.1.2 to 3.1.5 to apply critical security fixes.*

 * (1 week ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4833#issuecomment-5287421582) **dependabot[bot]** explained how to ignore dependency update notifications or reopen the PR to resolve conflicts

### [PR microsoft/TypeScript-go#4840](https://github.com/microsoft/TypeScript-go/pull/4840) (Closed)

**WIP**

*A work-in-progress placeholder issue created without any accompanying details.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#4847](https://github.com/microsoft/TypeScript-go/pull/4847) (Open, `Voight-Kampff Anomaly`, **weswigham**)

**fix: allow destructured require under module preserve \+ verbatimModuleSyntax**

*Allow destructured require calls in CommonJS modules under --module preserve and --verbatimModuleSyntax by adjusting alias checks to prevent TS1293 errors.*

 * created by **sankalpsthakur**
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * **RyanCavanaugh** assigned to **weswigham**

### [Issue microsoft/TypeScript-go#4861](https://github.com/microsoft/TypeScript-go/issues/4861) (Open, `Working As Intended`, **ahejlsberg**)

**Assignment to an \`any\`\-parameterised generic rejected by tsgo, accepted by tsc 6\.0\.3**

*tsgo rejects assigning a typed ObjectSchema<FormData> to AnyObjectSchema while tsc 6.0.3 accepts it.*

 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4861#issuecomment-5291939916) **ahejlsberg** explained that the behavior was working as intended due to issue #3445 enabling deeper analysis and revealing that Shape<any, any> wasn’t assignable to Shape<FormData, AnyObject>
 * (later) **ahejlsberg** added label `Working As Intended`, and removed label `Needs Investigation`

### [PR microsoft/TypeScript-go#4866](https://github.com/microsoft/TypeScript-go/pull/4866) (Closed)

**Add \`\-\-clientProcessId\` like reference LSP server**

*Add a --clientProcessId flag to allow overriding the parent process ID in LSP server initialization.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4875](https://github.com/microsoft/TypeScript-go/issues/4875) (Open, `Needs Investigation`, **weswigham**, **Copilot**)

**\`@augments\` JSDoc tag causes compilation error in generated declaration file**

*A JSDoc @augments tag mismatched with the extends clause in generated declaration files triggers ts(8023) errors under tsgo.*

 * **weswigham** assigned to **Copilot**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4875#issuecomment-5272301744) **jakebailey** said "I don't even know why this is happening in .ts files at all?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4875#issuecomment-5272315368) **weswigham** said "Also a good point! Honestly, I don't know why we're checking this at all! This is, AFAIK, a lint-consistency level error, at most."
 * [later](https://github.com/microsoft/TypeScript-go/issues/4875#issuecomment-5292276241) **dragomirtitian** noted that jsdoc checks in ts files were unexpected and suggested it was only a lint-consistency level error

### [Issue microsoft/TypeScript-go#4876](https://github.com/microsoft/TypeScript-go/issues/4876) (Open)

**Impending Repo Move**

*TypeScript development will consolidate in the microsoft/TypeScript repo, briefly locking activity and migrating all issues and PRs.*

 * created by **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4876#issuecomment-5284335831) **RyanCavanaugh** noted that issue and PR creation were disabled due to an upcoming repo move and instructed users to file bugs in the TypeScript repo and hold off on PRs

### [PR microsoft/TypeScript-go#4882](https://github.com/microsoft/TypeScript-go/pull/4882) (Closed, `dependencies`, `javascript`)

**Bump js\-yaml from 4\.2\.0 to 4\.3\.1**

*Upgrade js-yaml to 4.3.1 to patch a quadratic complexity vulnerability in !!omap and add a key limit option.*

 * (2 days ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4882#issuecomment-5284348245) **dependabot[bot]** explained how to ignore dependency update notifications or reopen the PR to resolve conflicts

### [PR microsoft/TypeScript-go#4883](https://github.com/microsoft/TypeScript-go/pull/4883) (Closed, `dependencies`, `go`)

**Bump go\.mongodb\.org/mongo\-driver from 1\.17\.6 to 1\.17\.7**

*Upgrade go.mongodb.org/mongo-driver to v1.17.7 to fix GSSAPI buffer handling and remove deprecation notices.*

 * (2 days ago) **dependabot[bot]** added labels `go`, `dependencies`, `go`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4883#issuecomment-5284348263) **dependabot[bot]** explained how to ignore dependency update notifications or reopen the PR to resolve conflicts

### [PR microsoft/TypeScript-go#4884](https://github.com/microsoft/TypeScript-go/pull/4884) (Closed, `dependencies`, `go`)

**Bump github\.com/aws/aws\-sdk\-go\-v2/service/s3 from 1\.96\.2 to 1\.97\.3**

*Bump AWS SDK Go v2 service/s3 dependency from version 1.96.2 to 1.97.3*

 * (2 days ago) **dependabot[bot]** added labels `go`, `dependencies`, `go`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4884#issuecomment-5284348403) **dependabot[bot]** explained how to ignore dependency update notifications or reopen the PR to resolve conflicts

### [PR microsoft/TypeScript-go#4885](https://github.com/microsoft/TypeScript-go/pull/4885) (Closed, `dependencies`, `go`)

**Bump github\.com/aws/aws\-sdk\-go\-v2/aws/protocol/eventstream from 1\.7\.5 to 1\.7\.8**

*Upgrade AWS SDK Go v2 eventstream protocol module from v1.7.5 to v1.7.8*

 * created by **dependabot[bot]**
 * (2 days ago) **dependabot[bot]** added labels `dependencies`, `go`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4885#issuecomment-5284348542) **dependabot[bot]** explained how to ignore dependency update notifications or reopen the PR to resolve conflicts

### [PR microsoft/TypeScript-go#4887](https://github.com/microsoft/TypeScript-go/pull/4887) (Closed)

**Make \`NodeHandle\` generic and generate \.Handle members of is\-guards for guarding node handles \(sync and async\)**

*Enable generic NodeHandle support and generate .Handle members on sync and async is-guards to narrow node handles.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4888](https://github.com/microsoft/TypeScript-go/pull/4888) (Closed)

**Port \`parseCommandLine\`, \`readConfigFile\`, and \`parseJsonConfigFileContent\`**

*Expose the parseCommandLine, readConfigFile, and parseJsonConfigFileContent functions in the TypeScript API.*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4889](https://github.com/microsoft/TypeScript-go/pull/4889) (Open, **weswigham**, **Copilot**)

**Use semantic type identity for JSDoc augments checks**

*Use semantic type identity for JSDoc @augments checks to avoid false mismatches when extending through aliases.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4889#issuecomment-5286070875) **weswigham** said "Actually @copilot also limit the check to JS files only - we shouldn't be issuing this (lint?) in .d.ts or .ts files at all anyway."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4889#issuecomment-5286284754) **Copilot** implemented augments/extends mismatch validation to apply only to JavaScript source files

### [Issue microsoft/TypeScript-go#4892](https://github.com/microsoft/TypeScript-go/issues/4892) (Open)

**textDocument/diagnostic on the first\-opened file in a session can silently omit real errors**

*The first diagnostic request in a new tsgo LSP session can silently omit real errors until another file is queried.*

 * created by **cheruvian**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4892#issuecomment-5286468698) **jakebailey** said "I think I might have regressed this in #4825, though you haven't mentioned that it's a regression. I that what you're seeing, or was this always a problem?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4892#issuecomment-5286515231) **jakebailey** said "I have not found a test for this, I'm only speculating."

### [PR microsoft/TypeScript-go#4893](https://github.com/microsoft/TypeScript-go/pull/4893) (Closed)

**\[api\] Move language service methods into dedicated namespace**

*Move language service methods into a dedicated namespace to restore intended grouping and support programs without LanguageServices*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4893#issuecomment-5283189199) **andrewbranch** said "@navya9singh @piotrtomiak, methods you rely on are moving. I left deprecated aliases in for use in nightlies for now, but will be removed before the 7.1 release."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4894](https://github.com/microsoft/TypeScript-go/pull/4894) (Open)

**Fix hover for merged generic namespace exports**

*Hover resolution crashes when merging a generic interface with a self-re-exported namespace sharing the same name.*

 * created by **johnfav03**

### [Issue microsoft/TypeScript-go#4895](https://github.com/microsoft/TypeScript-go/issues/4895) (Closed)

**tsc colours diagnostics when stdout is not a TTY, splitting "error TS2304" and breaking output parsing \(regressed in 6\.0\)**

*TypeScript CLI regressed in v6 by emitting ANSI escapes on non-TTY stdout, splitting "error TS2304" and preventing error detection.*

 * created by **leo-heath**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4895#issuecomment-5285322360) **jakebailey** clarified that FORCE_COLOR forces color unconditionally, asked if the user meant NO_COLOR and if FORCE_COLOR was overriding TTY detection
 * [today](https://github.com/microsoft/TypeScript-go/issues/4895#issuecomment-5285735626) **leo-heath** explained that FORCE_COLOR=0 was automatically set, confirmed TTY detection worked correctly across versions, and closed the issue after apologizing for the detour
 * (today) **leo-heath** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4895#issuecomment-5286256121) **jakebailey** mentioned that FORCE_COLOR handling was inconsistent and suggested copying chalk or Node’s behavior

### [PR microsoft/TypeScript-go#4896](https://github.com/microsoft/TypeScript-go/pull/4896) (Closed)

**Keep LSP server alive after response marshal failures**

*Log and respond to JSON serialization failures in LSP writeLoop instead of terminating the server connection.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4896#issuecomment-5284667208) **jakebailey** said "Handling this is good, but, I am worried about the root problem here; we should attempt to handle the nested case too."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4896#issuecomment-5285617717) **johnfav03** proposed a cap of 1000 for selection-range parent chains to maintain nesting within limits and requested feedback
 * [today](https://github.com/microsoft/TypeScript-go/pull/4896#issuecomment-5285738932) **gabritto** implemented a cap of 1000 for selection-range parent chains and asked what file or AST caused such a deep chain
 * [today](https://github.com/microsoft/TypeScript-go/pull/4896#issuecomment-5285901999) **johnfav03** explained that a missing comma in a large generated array of ~50K entries led the parser to create deep nested AST nodes (~18K parents)
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4897](https://github.com/microsoft/TypeScript-go/pull/4897) (Closed, **andrewbranch**, **Copilot**)

**Add checker\.getSymbolsInScope to native\-preview API**

*Expose checker.getSymbolsInScope in the native-preview API to retrieve symbols visible at a given location with a specified meaning.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4898](https://github.com/microsoft/TypeScript-go/pull/4898) (Open)

**Parse dotted private names in type queries, forbid in declaration emit**

*Enable parsing of dotted private names in type queries but prevent them in declaration file output.*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4898#issuecomment-5286753073) **a-tarasyuk** noted that this revived the previous approach while fixing the AST issue and asked whether the approach from the linked issue comment still made sense
 * [today](https://github.com/microsoft/TypeScript-go/pull/4898#issuecomment-5287295294) **weswigham** explained that private names only appeared in dotted expression-like positions and expressed reluctance to change that or conflict with potential future expression syntax

### [Issue microsoft/TypeScript-go#4899](https://github.com/microsoft/TypeScript-go/issues/4899) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Crash at \`GetSourceFilePathInNewDir\`**

*TypeScript 7.0.2 unexpectedly crashes in GetSourceFilePathInNewDir during program creation with no reproducible steps.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4900](https://github.com/microsoft/TypeScript-go/pull/4900) (Open, **DanielRosenwasser**, **Copilot**)

**Prevent crash when computing emit output paths**

*Prevent panics in computing emit output paths by delegating to a canonical prefix-based worker and removing invalid containment checks*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4901](https://github.com/microsoft/TypeScript-go/pull/4901) (Closed)

**Fix diagnostics lookup across source file replacements**

*Use file path keys instead of SourceFile objects in diagnostics lookup to avoid retaining outdated source files on program reuse.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4902](https://github.com/microsoft/TypeScript-go/pull/4902) (Open)

**Fix transpile test diffs**

*Urgently fix the newly introduced transpile test diffs before they are deleted.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#4903](https://github.com/microsoft/TypeScript-go/pull/4903) (Open)

**Remove AST node self pointers**

*Remove self-referencing pointers from AST nodes now that unsafe code is confined to generated code.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5290293010) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5290293731) **typescript-automation[bot]** reported that build jobs started and provided links to status and results
 * [later](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5290536962) **typescript-automation[bot]** reported the requested perf run results including a metrics comparison between baseline and pr
 * [later](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5290715464) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5290716030) **typescript-automation[bot]** started performance test job and posted status and results links
 * [later](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5290957829) **typescript-automation[bot]** provided the requested performance run results
 * [later](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5291168257) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5291168946) **typescript-automation[bot]** posted a build status update with links to the started performance test jobs
 * [later](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5291450290) **typescript-automation[bot]** posted the requested performance run results
 * [later](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5293362138) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5293362765) **typescript-automation[bot]** notified that performance tests started and provided status and results links
 * [later](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5293644618) **typescript-automation[bot]** provided the requested performance run results

