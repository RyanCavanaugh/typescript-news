# Report for 2026-07-02 (Thursday, July 2nd, 2026)

11 different users commented on 31 different issues.

## Recommended Actions

 * Moderation
    * @KostyaTretyak posted unrelated content in [microsoft/TypeScript-go#4520](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4868442056)
 * Response Recommended
    * @typescript-automation[bot] provided requested performance results in [microsoft/TypeScript-go#3362](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4870283060)
    * @KostyaTretyak provided memory usage output in [microsoft/TypeScript-go#4520](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4867769184)
    * @KostyaTretyak provided filesystem type information in [microsoft/TypeScript-go#4520](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4868195100)
    * @KostyaTretyak provided requested arcstat and arcstats outputs in [microsoft/TypeScript-go#4520](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4868427022)
    * @KostyaTretyak provided additional repro clarification in [microsoft/TypeScript-go#4520](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4869357111)
    * @KostyaTretyak confirmed no memory leak occurs when moving the folder to a directory without other git repositories and suggested neighboring repositories may be misdetected as part of the monorepo in [microsoft/TypeScript-go#4520](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4869534469)

## Activity Summary

### [PR microsoft/TypeScript-go#1301](https://github.com/microsoft/TypeScript-go/pull/1301) (Closed)

**Enable pre/post emit diagnostic consistency tests**

*Enable pre/post emit diagnostic consistency tests after triaging newly surfaced test failures.*

 * created by **weswigham**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/1301#issuecomment-4870876843) **weswigham** said "Superseded by #4526"
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3362](https://github.com/microsoft/TypeScript-go/pull/3362) (Open)

**Replace most ID usage with pointers**

*Propose replacing most ID fields with pointers in Go to leverage pointer comparability and reduce overhead.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4735127438) **typescript-automation[bot]** announced the start of the perf test job and provided status and result links
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4735426623) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4735830791) **typescript-automation[bot]** posted the requested perf run results for jakebailey including comparison metrics
 * [today](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4870099786) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4870100315) **typescript-automation[bot]** reported that performance tests had started and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4870283060) **typescript-automation[bot]** reported the performance comparison results for the requested perf run

### [Issue microsoft/TypeScript-go#3508](https://github.com/microsoft/TypeScript-go/issues/3508) (Closed, `Needs Investigation`)

**Corsa no longer emits the TS\-1 internal diagnostic about pre\-emit/post\-emit diagnostic count mismatches**

*Corsa no longer emits TS-1 diagnostics for mismatched pre-emit and post-emit diagnostic counts in certain test files.*

 * (7 weeks ago) **RyanCavanaugh** set milestone to `Possible Improvement`, and unassigned **gabritto**, **Copilot**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3733](https://github.com/microsoft/TypeScript-go/issues/3733) (Closed, `Domain: Editor`, `Needs More Info`)

**No autocomplete for local symbols and some global types when creating a new file**

*VS Code fails to autocomplete or auto-import local symbols and ESNext types like Temporal in new TypeScript files until restart.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3733#issuecomment-4460635515) **jansedlon** provided a partial repro showing that the Temporal namespace was not recognized initially when typing 'type A = Temporal.' in a new file and noted inability to reproduce the local exports issue
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3733#issuecomment-4481422378) **RyanCavanaugh** asked which aspect (12,000 files, monorepo, tsconfig, etc.) was causing the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/3733#issuecomment-4877704092) **jansedlon** said "@RyanCavanaugh Sorry it took me so long to get back to it. PR here #4529 "

### [PR microsoft/TypeScript-go#3738](https://github.com/microsoft/TypeScript-go/pull/3738) (Closed, **gabritto**, **Copilot**)

**Implement pre\-emit/post\-emit diagnostic count mismatch detection \(TS\-1\)**

*Implement TS-1 diagnostic in Go test harness to detect and report mismatches between pre-emit and post-emit diagnostic counts.*

 * **Copilot** assigned to **gabritto**
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3738#issuecomment-4400192625) **jakebailey** said "I think this is technically a dupe of #1301 but it's been a while so I think we don't need some of the fixes in that PR?"
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3738#issuecomment-4870864259) **jakebailey** said "#4526"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4408](https://github.com/microsoft/TypeScript-go/issues/4408) (Open, `Needs More Info`)

**Regression: recursive conditional\+mapped "serialize" type no longer proves \`Transform\<X\>\` assignable to \`X\` on deeply\-nested compound types \(native\-preview; works in tsc\)**

*A regression in @typescript/native-preview fails to prove recursive mapped serialize types as identity for deeply nested compound types.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/4408#issuecomment-4867217257) **jakebailey** provided a more minimal TypeScript example demonstrating the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4408#issuecomment-4867414171) **jakebailey** said "@ahejlsberg Is this exactly like #4451?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4408#issuecomment-4867661889) **jakebailey** said "Thinking harder, I'm 99% percent certain it's exactly the same and this is working as intended."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4408#issuecomment-4869655798) **ahejlsberg** said "Agree, this seems exactly like #4451. And thus working as intended."

### [PR microsoft/TypeScript-go#4483](https://github.com/microsoft/TypeScript-go/pull/4483) (Closed)

**Handle unloaded projects in API snapshot responses**

*Prevent nil pointer panics in updateSnapshot by properly handling unloaded ancestor tsconfig projects lacking command line data.*

 * created by **ulitink**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4483#issuecomment-4842344803) **ulitink** said "@microsoft-github-policy-service agree company="JetBrains""
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4486](https://github.com/microsoft/TypeScript-go/pull/4486) (Closed)

**Use workspace/diagnostics for global diagnostics**

*Using workspace/diagnostics to work around VS Code diagnostic naming problems triggers repeated diagnostic request loops.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4486#issuecomment-4868887020) **jakebailey** said "The spam apparently can be handled by basically doing old school HTTP-style long-polling. But, the other PR to rename the collection was enough, so I'm just going to close this."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4511](https://github.com/microsoft/TypeScript-go/pull/4511) (Closed)

**Set allowJs in fourslash tests**

*A JS test crashes without allowJs while enabling it breaks others, indicating a need for additional project inference.*

 * created by **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4511#issuecomment-4859960767) **jakebailey** said "#3432 is related"
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4512](https://github.com/microsoft/TypeScript-go/pull/4512) (Closed)

**\[api\] Add option to collect timing info**

*Implement an API option to enable and retrieve detailed request timing and data usage metrics.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4512#issuecomment-4860808150) **andrewbranch** mentioned that changing the JSON-RPC message shape worked despite misgivings and stated plans to eventually replace JSON-RPC due to base64 overhead
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4512#issuecomment-4860819088) **andrewbranch** said "I think your suggestion is ultimately simpler, though probably a slight increase in LOC. Let me try it and see."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4512#issuecomment-4867506701) **andrewbranch** said "I had the idea this morning to add some client-side timing info on cumulative RemoteNode materialization from source file buffers, so I'm throwing that together."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4512#issuecomment-4868325067) **andrewbranch** observed that per-node materialization was too fast to measure, but metrics showed how many source files were fetched, how many nodes that represented, and how many of those nodes were materialized
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4520](https://github.com/microsoft/TypeScript-go/issues/4520) (Open, `Domain: Editor`)

**Bug Report: Severe memory leak triggered by "TypeScript \(Native Preview\)" extension**

*Enabling the TypeScript Native Preview extension in an empty folder without package.json causes a persistent memory leak until VS Code is closed.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4867681424) **jakebailey** said "I am fairly confused; in that screenshot, I do not see anything using 14GB? Am I missing something?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4867700307) **KostyaTretyak** said "I'm not a system administrator, so I can't answer your question. Another strange thing is how the memory cache changes."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4867717299) **jakebailey** clarified that cache memory is just available for processes and showed free -h output, questioned if the user was using gnome-system-monitor, and suggested using htop to identify processes
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4867769184) **KostyaTretyak** reported that even after 11 minutes available memory remained low at 2.4Gi and provided free -h output
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4867777764) **KostyaTretyak** said ""
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4867799905) **jakebailey** said "Can you sort by memory? I would also go into F2 > Display options > Hide userland process threads and see which specific process is to blame."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4867804155) **jakebailey** said "I'll note that in that htop screenshot, only 4.2GB are used, which was your baseline, the rest is "cached". (unused ram is wasted ram!)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4867851417) **KostyaTretyak** said ""
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4868195100) **KostyaTretyak** reported that their system is running on a ZFS root filesystem instead of ext4 and provided the output of df -T /
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4868427022) **KostyaTretyak** provided arcstat and proc spl kstat zfs arcstats outputs as advised by Gemini
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4868437817) **jakebailey** asked who had been advised and expressed confusion about followup screenshots not indicating anything particular
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4868442056) **KostyaTretyak** said "Google Gemini =)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4869357111) **KostyaTretyak** clarified that adding a default package.json with npm init -y prevented the memory leak and suggested a nearby service might be scanning git repositories
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4869534469) **KostyaTretyak** confirmed no memory leak when moving folder to a directory without other git repositories and suggested a service might misdetect neighboring repositories as part of the monorepo

### [Issue microsoft/TypeScript-go#4521](https://github.com/microsoft/TypeScript-go/issues/4521) (Open, `Domain: API and Extensibility`)

**SourceFile text does not include BOM**

*SourceFile.getText and getFullText omit the UTF-8 BOM while node start and end positions include it, causing misaligned text slices.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/4521#issuecomment-4867432365) **jakebailey** said "In a way this implies we should also be BOM stripping when creating source files too, though reasonably the only time this would happen is for the UTF-8 BOM when manually constructed like this?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4521#issuecomment-4867571296) **acutmore** noted BOM stripping in ts-blank-space tests and pointed out a technical difference from Strada's behavior
 * [today](https://github.com/microsoft/TypeScript-go/issues/4521#issuecomment-4867639424) **jakebailey** assumed that reading via ts.sys.readFile removed the BOM and suggested dropping the BOM elsewhere
 * **DanielRosenwasser** added label `Domain: API and Extensibility`

### [PR microsoft/TypeScript-go#4523](https://github.com/microsoft/TypeScript-go/pull/4523) (Closed)

**Move ID error to favor class expression inference failure when present**

*Remove an unused baseline diff and repurpose the special class expression inference failure error.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4524](https://github.com/microsoft/TypeScript-go/pull/4524) (Closed)

**Move last diff in ID triaged category to accepted**

*Reclassify the final diff in the ID triaged category to accepted to leverage more informative Corsa error reporting*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4525](https://github.com/microsoft/TypeScript-go/issues/4525) (Open)

**Follow\-up on issues/4254: \`typeof\` emit does not happen in \`export const { \.\.\. } = default\`**

*tsgo’s declaration emitter incorrectly inlines function signatures instead of using typeof when destructuring and exporting properties from a default export.*

 * created by **hkleungai**

### [PR microsoft/TypeScript-go#4526](https://github.com/microsoft/TypeScript-go/pull/4526) (Closed)

**Unconditionally reenable pre/post\-emit diagnostic consistency checking**

*Reenable diagnostic consistency checking around emit unconditionally and address multiple check-order and identifier resolution bugs.*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4526#issuecomment-4870817595) **weswigham** said "cc @gabritto Honestly, with fixes for what I saw as the top 3 built in to this PR, there aren't too many distinct issues left to look into, I think."
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4527](https://github.com/microsoft/TypeScript-go/issues/4527) (Open, `bug`, `meta-issue`)

**Investigate inconsistent diagnostic output in baselines & make builds with inconsistent diagnostic output fail tests**

*Investigate inconsistent diagnostic outputs in baselines caused by checker order dependence and enforce build failures on detection.*

 * created by **weswigham**
 * (today) **weswigham** added labels `bug`, `meta-issue`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4527#issuecomment-4870977001) **weswigham** mentioned that strada also contained TS-1 diagnostics in three additional baselines and proposed making TS-1 errors fail the build as the issue's completion criteria

### [Issue microsoft/TypeScript-go#4528](https://github.com/microsoft/TypeScript-go/issues/4528) (Open, `Domain: Type Checking`, `Type Ordering`)

**tsgo appears to loop until OOM on three/tsl Fn callback that TypeScript accepts**

*tsgo enters an infinite type-checking loop and exhausts memory when processing a three/tsl Fn callback that tsc accepts*

 * created by **hsheth2**

### [PR microsoft/TypeScript-go#4529](https://github.com/microsoft/TypeScript-go/pull/4529) (Closed)

**Fix wildcard directories being dropped for "\./"\-prefixed includes with dot\-directory excludes**

*Wildcard directories defined by './'-prefixed include patterns are incorrectly dropped when dot-directory excludes are present, preventing new file detection.*

 * created by **jansedlon**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4529#issuecomment-4874013472) **jansedlon** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4529#issuecomment-4877759536) **jakebailey** said "Can you point to the Strada code, if this is just a porting bug?"

### [PR microsoft/TypeScript-go#4530](https://github.com/microsoft/TypeScript-go/pull/4530) (Open)

**Fix: Correctly flag always\-truthy exported and imported enum conditions \(ts2845\)**

*Fix ts2845 by ensuring always-truthy enum conditions are flagged for exported and imported enums*

 * created by **iapoorv01**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4530#issuecomment-4874825598) **iapoorv01** described the Contributor License Agreement and prompted sign-off via the microsoft-github-policy-service agree command

### [PR microsoft/TypeScript-go#4531](https://github.com/microsoft/TypeScript-go/pull/4531) (Closed)

**Preserve original source text of negative numeric literals in declaration emit \(issue \#4116\)**

*Preserve original negative numeric literal text in declaration emit to avoid normalized outputs like -Infinity.*

 * created by **DrSmoothl**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4531#issuecomment-4875323045) **DrSmoothl** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4531#issuecomment-4877742896) **jakebailey** noted that an existing AI pull request (#4158) already addressed the same changes as its first commit
 * [later](https://github.com/microsoft/TypeScript-go/pull/4531#issuecomment-4877797163) **DrSmoothl** mentioned agreement with the agent on the fix and apologized for the noise
 * (later) **DrSmoothl** closed the issue

