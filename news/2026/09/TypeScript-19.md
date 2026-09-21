# Report for 2026-09-19 (Saturday, September 19th, 2026)

16 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @Freakazo reported performance gains and memory usage increase when testing the branch in [microsoft/TypeScript#64220](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5749572773)
    * @Ecco provided repro steps and screenshots in [microsoft/TypeScript#64228](https://github.com/microsoft/TypeScript/issues/64228#issuecomment-5746689139)
    * @Raxan7 provided detailed repro steps and offered to add a regression test or fix in [microsoft/TypeScript#64228](https://github.com/microsoft/TypeScript/issues/64228#issuecomment-5747747091)
    * @devanshj provided a patch fixing xstate type inference issues in [microsoft/TypeScript#64252](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5750754357)
    * @Sector6759 asked about improving the interface definition to prevent passing the timeZone option in [microsoft/TypeScript#64346](https://github.com/microsoft/TypeScript/pull/64346#issuecomment-5745662690)
    * @leonidaz reported that activation alone is insufficient and suggested pairing activation with project loading or syncing open mapped documents in [microsoft/TypeScript#64355](https://github.com/microsoft/TypeScript/issues/64355#issuecomment-5746828846)

## Activity Summary

### [PR microsoft/TypeScript#64220](https://github.com/microsoft/TypeScript/pull/64220) (Open, `For Milestone Bug`, **johnfav03**)

**Schedule tsc \-b projects by dependency depth so builders do not idle on upstream projects**

*Sort tsc -b build tasks by dependency depth instead of depth-first references to reduce idle time and speed up parallel builds.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5685828576) **jakebailey** said "@typescript-bot perf test this faster"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5685830448) **typescript-automation[bot]** reported build jobs starting and provided links to status and results
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5686328009) **typescript-automation[bot]** posted performance run results for tsc comparing baseline to pr
 * [later](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5749572773) **Freakazo** tested the branch on a large monorepo and observed performance gains (median 38.24s to 28.39s) with increased memory usage (~5.4GB to ~6.9GB), and noted most benchmarks don’t use the -b flag

### [Issue microsoft/TypeScript#64228](https://github.com/microsoft/TypeScript/issues/64228) (Open, `Needs More Info`)

**Incorrect TS1111 when using private generator function in JS**

*VSCode erroneously raises TS1111 error when invoking a private generator method on another instance within a class.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/64228#issuecomment-5666596178) **RyanCavanaugh** said "Same, please fill in the definitions of child and its #iterate"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64228#issuecomment-5734070632) **Raxan7** mentioned inability to reproduce TS1111 with various TypeScript versions and requested the child declaration, config, and a minimal reproduction
 * [today](https://github.com/microsoft/TypeScript/issues/64228#issuecomment-5746689139) **Ecco** described that the example code still triggered the error, provided screenshots of the error and TypeScript version selection, and noted that adding an explicit constructor resolves the error
 * [today](https://github.com/microsoft/TypeScript/issues/64228#issuecomment-5747747091) **Raxan7** reproduced the error in plain unchecked JavaScript, detailed reproduction steps across multiple TypeScript versions with control tests, and offered to add a regression test or fix

### [PR microsoft/TypeScript#64252](https://github.com/microsoft/TypeScript/pull/64252) (Open, `For Backlog Bug`)

**Fix reverse mapped type inference when all properties are context\-sensitive**

*Improve reverse mapped type inference to correctly handle scenarios where every property is context-sensitive.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5670695144) **typescript-automation[bot]** provided the perf run results for the requested comparison report
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5680822580) **devanshj** reported that xstate broke with 14 new errors and said they would investigate whether the break is acceptable or adjust the PR accordingly
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5684134246) **devanshj** provided a minimal TypeScript snippet that compiled in main but failed in the PR, and noted that removing a type constraint resolved the issue
 * [later](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5750754357) **devanshj** provided a patch that fixed xstate type inference by removing an unused invariant type parameter and making the assigner function bivariant

### [Issue microsoft/TypeScript#64308](https://github.com/microsoft/TypeScript/issues/64308) (Closed, `Working as Intended`)

**typescript version 7 complains about unused generic type even though version 6 does not**

*TypeScript 7 incorrectly reports an unused generic parameter error in overloaded createRef definitions under noUnusedParameters, unlike version 6.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64308#issuecomment-5715673074) **MartinJohns** said "But.. it is unused. So it's actually a bugfix."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64308#issuecomment-5716862153) **jakebailey** said "Yes, this is a bug that was noticed in the port."
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/64308#issuecomment-5746704149) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#64314](https://github.com/microsoft/TypeScript/issues/64314) (Closed, `Duplicate`)

**False\-positive \`unintentional comparison\` error with closures**

*TypeScript’s language service incorrectly flags valid comparisons on a union-typed variable as unintentional after the variable is updated within a closure.*

 * created by **e-kucheriavyi**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64314#issuecomment-5720680826) **MartinJohns** said "Duplicate of #9998."
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/64314#issuecomment-5746703838) **typescript-automation[bot]** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#64346](https://github.com/microsoft/TypeScript/pull/64346) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Reject timeZone in ZonedDateTime\.toLocaleString options**

*Remove the timeZone option from Temporal.ZonedDateTime.toLocaleString and error on its usage because the method always uses the receiver’s time zone.*

 * (yesterday) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64346#issuecomment-5745662690) **Sector6759** suggested defining the interface with timeZone?: never to prevent accidentally passing the timeZone option in non-literal options objects

### [PR microsoft/TypeScript#64352](https://github.com/microsoft/TypeScript/pull/64352) (Open, `For Backlog Bug`)

**Remove misplaced parameter description from RegExp\#source JSDoc**

*Remove the misplaced 'regExp' parameter description from the read-only RegExp.source JSDoc in lib.es5.d.ts*

 * created by **hikmetba-bit**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`

### [PR microsoft/TypeScript#64353](https://github.com/microsoft/TypeScript/pull/64353) (Open, `For Backlog Bug`)

**Fix invalid decorator examples in lib\.decorators\.d\.ts**

*Rewrite invalid decorator examples in lib.decorators.d.ts to use correct context types and fix syntax errors.*

 * created by **wfatih**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64353#issuecomment-5744120251) **wfatih** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64354](https://github.com/microsoft/TypeScript/issues/64354) (Closed)

**Burp Professional 2026**

*Propose implementing Burp Suite Professional 2026 support using the aanyapatels/Burpsuite-Professional repository.*

 * created by **aanyapatels**
 * [today](https://github.com/microsoft/TypeScript/issues/64354#issuecomment-5744806500) **MartinJohns** said "I will never understand how people think this is acceptable behavior."

### [Issue microsoft/TypeScript#64355](https://github.com/microsoft/TypeScript/issues/64355) (Open, `Working as Intended`)

**TypeScript 7 VS Code extension never activates for workspaces where only content\-mapped files are opened**

*The TypeScript 7 VS Code extension never activates for content-mapped file types unless a native TypeScript or JavaScript file is opened.*

 * created by **leonidaz**
 * [today](https://github.com/microsoft/TypeScript/issues/64355#issuecomment-5746828846) **leonidaz** described that activation alone was insufficient and suggested pairing activation with project loading or syncing already-open mapped documents

### [Issue microsoft/TypeScript#64356](https://github.com/microsoft/TypeScript/issues/64356) (Open)

**TypeScript 7 VS Code extension: let extensions that serve their language through content mappers opt out of the tsserver\-plugin warning**

*Enable extensions using TypeScript 7 content mappers to suppress tsserver-plugin warnings via a declarative flag*

 * created by **leonidaz**

### [PR microsoft/TypeScript#64357](https://github.com/microsoft/TypeScript/pull/64357) (Open, `For Uncommitted Bug`)

**Fix import statement completion filtering in tsgo**

*Use the generated import statement as filterText for tsgo import completions to fix filtering inside named imports.*

 * created by **yksr-melt**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64357#issuecomment-5747866962) **yksr-melt** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64358](https://github.com/microsoft/TypeScript/pull/64358) (Open, `For Backlog Bug`)

**Deprecate literal computed property names in enums**

*Deprecate string and template literal computed enum member names in TypeScript by providing deprecation warnings and quick fixes.*

 * created by **magic-akari**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64359](https://github.com/microsoft/TypeScript/pull/64359) (Open, `For Backlog Bug`)

**Respect quote preference for object property completions**

*Respect user quote style preferences for non-identifier property completions in object literals.*

 * created by **yksr-melt**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`

### [PR microsoft/TypeScript#64360](https://github.com/microsoft/TypeScript/pull/64360) (Open, `For Backlog Bug`)

**Fix union overload signature ordering instability**

*Modify TypeScript's union overload resolution to consistently prefer strictly more specific signatures over less specific ones.*

 * created by **adilalperenciftci**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5748296015) **adilalperenciftci** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64361](https://github.com/microsoft/TypeScript/pull/64361) (Open, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20260920092305213 to main**

*Merge localized lcls updates from branch lego/hb_5378966c-b857-470a-8675-daebef4a6da1_20260920092305213 into main.*

 * created by **csigs**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64362](https://github.com/microsoft/TypeScript/issues/64362) (Open)

**Content mappers: more granular resolution, and default extensions in the manifest**

*Enable regex-based and dynamic path matching for content mappers and default manifest extension support.*

 * created by **colinhacks**

### [PR microsoft/TypeScript#64363](https://github.com/microsoft/TypeScript/pull/64363) (Open, `For Backlog Bug`)

**Fix inlay hints for trailing required rest elements**

*Adjust inlay parameter name hint mapping for rest parameters with trailing required tuple elements and skip destructured parameters*

 * created by **yksr-melt**
 * **typescript-automation[bot]** added label `For Backlog Bug`

