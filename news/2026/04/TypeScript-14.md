# Report for 2026-04-14 (Tuesday, April 14th, 2026)

18 different users commented on 45 different issues.

## Recommended Actions

 * Moderation
    * @alisa-xh posted spam offering services in [microsoft/TypeScript#29707](https://github.com/microsoft/TypeScript/issues/29707#issuecomment-4248128808)
    * @alisa-xh posted spam offering services in [microsoft/TypeScript#63206](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-4248127704)
 * Response Recommended
    * @freshp86 asked if the issue was still relevant in [microsoft/TypeScript#13569](https://github.com/microsoft/TypeScript/issues/13569#issuecomment-4247506804)
    * @everett1992 provided repro steps for .d.ts files referencing .ts extensions causing TS errors in [microsoft/TypeScript#61037](https://github.com/microsoft/TypeScript/issues/61037#issuecomment-4248673137)
    * @Bodlux asked for a preferred security contact for responsible disclosure in [microsoft/TypeScript#63404](https://github.com/microsoft/TypeScript/pull/63404#issuecomment-4247956854)
    * @hikeeba reported experiencing the same error on a fresh Vite project with MUI in [microsoft/TypeScript#63405](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253248545)
    * @hikeeba reported that it filled up 3GB of RAM and crashed repeatedly on a fresh VSCode install in [microsoft/TypeScript#63405](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253305882)
    * @himhimlo reported the issue occurred on both MacBook Pro and Windows 11 laptop, indicating it wasn't machine-specific in [microsoft/TypeScript#63405](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253355220)
    * @nmain asked about intention behind comma operator vs semicolon in [microsoft/TypeScript#63406](https://github.com/microsoft/TypeScript/issues/63406#issuecomment-4252782247)
    * @dangreen requested to transpile to ES2021 in [microsoft/TypeScript#63406](https://github.com/microsoft/TypeScript/issues/63406#issuecomment-4252904980)

## Activity Summary

### [Issue microsoft/TypeScript#13569](https://github.com/microsoft/TypeScript/issues/13569) (Closed, `Suggestion`, `Revisit`, `Domain: lib.d.ts`)

**DOM: Font Loading API**

*Developer requests inclusion of FontFace, FontFaceSet and document.fonts typings for the CSS Font Loading API in TypeScript.*

 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/13569#issuecomment-770420210) **arcanis** noted that font faces had been a Candidate Recommendation since September 2018 and had 98% support
 * [5 years ago](https://github.com/microsoft/TypeScript/issues/13569#issuecomment-802591857) **wereHamster** noted that the CSS side had reached Candidate Recommendation while the JS API remained a Working Draft and shared relevant links
 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/13569#issuecomment-913143701) **s-h-a-d-o-w** noted that draft status hasn’t prevented including types by comparing web audio and font APIs and pointed out 96% JS API support via caniuse.com
 * [today](https://github.com/microsoft/TypeScript/issues/13569#issuecomment-4247506804) **freshp86** said "Is this still relevant? Looking at node_modules/typescript/lib/lib.dom.d.ts it seems to already include some of the APIs that were previously missing (for example FontFace#load)."

### [Issue microsoft/TypeScript#17253](https://github.com/microsoft/TypeScript/issues/17253) (Open, `Domain: check: Control Flow`, `Possible Improvement`)

**Properties of instances of anonymous classes have type \<any\> after an instanceof guard\.**

*TypeScript fails to enforce generic property types on instances of anonymous classes after an instanceof check.*

 * (today) **ahejlsberg** added label `Possible Improvement`, and removed label `Bug`
 * [today](https://github.com/microsoft/TypeScript/issues/17253#issuecomment-4244726458) **ahejlsberg** changed the label from "bug" to "possible improvement" and suggested substituting `unknown` instead of `any` for type parameters with `instanceof`, noting it’s safer for covariant but still unsound for contravariant positions
 * [today](https://github.com/microsoft/TypeScript/issues/17253#issuecomment-4247857718) **kljnepk** provided additional signals from local type checks to narrow the search space for instanceof narrowing issues

### [Issue microsoft/TypeScript#29707](https://github.com/microsoft/TypeScript/issues/29707) (Open, `Bug`, `Help Wanted`, `Good First Issue`, `Domain: classes`)

**TS is overly picky when declaring a class constructor type**

*TypeScript rejects generic class constructors declared with unknown[] signatures as valid constructor types*

 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/29707#issuecomment-1193043857) **jszopi** explained that function types are contravariant in their parameters, causing unknown to be restrictive and leading to never[] for rest parameters; shared using never[] for instanceof operands and noted mixins require any
 * [27 weeks ago](https://github.com/microsoft/TypeScript/issues/29707#issuecomment-3375208966) **tysoncung** said "I'm interested in working on this issue. Could you provide more context about what you're looking for? Any additional details about requirements or constraints would be helpful."
 * **RyanCavanaugh** added label `Domain: classes`
 * [today](https://github.com/microsoft/TypeScript/issues/29707#issuecomment-4248128808) **alisa-xh** offered professional development services and asked to connect on WeChat
 * [later](https://github.com/microsoft/TypeScript/issues/29707#issuecomment-4253541609) **RyanCavanaugh** said "@snarbles2 I'm tempted to set up a script to auto-ban anyone who gets a 🚀 reaction from you 😅"

### [Issue microsoft/TypeScript#46005](https://github.com/microsoft/TypeScript/issues/46005) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow specifying exclude as a command line option**

*Add a --exclude command line option to the TypeScript compiler mirroring tsconfig.json’s exclude setting.*

 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/46005#issuecomment-3005327993) **jstevej** said "Needed this today. Ended up here. 😔"
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/46005#issuecomment-3254146131) **liunice** said "I also needed this!"
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/46005#issuecomment-3414281558) **zanminkian** described a tsc wrapper named tscx that supports the requested feature and provided a usage example
 * [today](https://github.com/microsoft/TypeScript/issues/46005#issuecomment-4245659380) **VillainsRule** said "+1; following"

### [Issue microsoft/TypeScript#61037](https://github.com/microsoft/TypeScript/issues/61037) (Open, `Suggestion`, `Help Wanted`, `Experience Enhancement`)

**rewriteRelativeImportExtensions: tsc doesn't rewrite extensions in emitted declaration files**

*TypeScript’s rewriteRelativeImportExtensions setting rewrites .ts to .js in emitted JavaScript files but not in generated declaration files.*

 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/61037#issuecomment-3140846857) **imcotton** said "Since the ticket has the Help Wanted label, what is the correct spell to summon the copilot for the help?"
 * [20 weeks ago](https://github.com/microsoft/TypeScript/issues/61037#issuecomment-3572855999) **paulmillr** said "User encountered TS2691 in Angular/Ionic/Capacitor because of this."
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/61037#issuecomment-3695019834) **stevenvachon** lamented that a year later there was still no progress, suggested Flow over TypeScript, and shared a workaround using tsc-alias
 * [today](https://github.com/microsoft/TypeScript/issues/61037#issuecomment-4248673137) **everett1992** described encountering TypeScript errors when .d.ts files referenced .ts extensions after compiling with tsc --rewriteRelativeImportExtensions

### [Issue microsoft/TypeScript#63206](https://github.com/microsoft/TypeScript/issues/63206) (Open, `Bug`, `Help Wanted`, `Domain: Error Messages`)

**Confusing error message \(2322\), should use \(2741\) and \(2322\) error message when this\["XXX"\] = {\.\.\.} has a missing \(or mispelled\) key or an incompatible value\.**

*Improve TypeScript error messaging for this['XXX'] assignments by distinguishing missing property errors (2741) from type mismatches (2322).*

 * **RyanCavanaugh** added label `Domain: Error Messages`
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3995817875) **denis-migdal** asked whether TypeScript could enforce explicit casts to signal intent for potentially unsafe assignments
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-4102579315) **WhiteMinds** traced the root cause and identified that reportRelationError discarded error elaboration for indexed access types, and proposed preserving errorInfo in that case (PR #63278)
 * [today](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-4248127704) **alisa-xh** offered professional development services and asked to connect on WeChat

### [Issue microsoft/TypeScript#63330](https://github.com/microsoft/TypeScript/issues/63330) (Open, `Docs`, **DanielRosenwasser**)

**\[V6\] \`module\` defaults is not \`esnext\`**

*TypeScript 6.0 incorrectly defaults the module option to ES2015 instead of ESNext, causing import attributes errors.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4169983541) **mkantor** questioned the repeated phrasing in the announcement post and asked if it was a typo
 * (1 week ago) **RyanCavanaugh** added label `Docs`, and assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4245384683) **mkantor** pointed out that the announcement post incorrectly stated that --outFile was removed in TypeScript 6.0 instead of deprecated and suggested it should reference 7.0

### [Issue microsoft/TypeScript#63334](https://github.com/microsoft/TypeScript/issues/63334) (Open, `Website`)

**Playground typing issue**

*Importing from @octokit/core/types in the TypeScript Playground results in any types and stale diagnostic errors.*

 * created by **BrandonStudio**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63334#issuecomment-4179530261) **RyanCavanaugh** listed similar issues in an auto-generated analysis
 * **RyanCavanaugh** added label `Website`

### [Issue microsoft/TypeScript#63373](https://github.com/microsoft/TypeScript/issues/63373) (Closed, `External`)

**tsserver hangs in Yarn PnP projects — incorrect directory watcher due to unchecked indexOf returning \-1**

*tsserver in Yarn PnP projects hangs because unchecked indexOf on non-node_modules paths produces incorrect directory watcher paths.*

 * created by **sebaspf**
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63373#issuecomment-4208290436) **RyanCavanaugh** provided an auto-generated analysis listing similar issues to help get started
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63373#issuecomment-4217077271) **jakebailey** said "This is out of our control; this is a patch and we do not maintain it."
 * **RyanCavanaugh** added label `External`

### [Issue microsoft/TypeScript#63377](https://github.com/microsoft/TypeScript/issues/63377) (Closed, `Question`)

**TS doesn't properly infer generic callback \`\<T\>\(x: X\<T\>\) =\> T\` when providing \`\(x\) =\> new T\(\)\` \(parameter defined without type\)**

*TypeScript does not infer a generic callback’s type when its parameter is untyped, resulting in any instead.*

 * **RyanCavanaugh** added label `Question`
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63377#issuecomment-4221303828) **denis-migdal** thanked for the answer, described two possible inference results for createViewClass2, and asked if using a const generic parameter would select the more precise inference
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63377#issuecomment-4231435840) **denis-migdal** described that defaulting a generic type parameter can cause lazy inference and suggested removing the default as a workaround
 * [today](https://github.com/microsoft/TypeScript/issues/63377#issuecomment-4248795382) **typescript-bot** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63378](https://github.com/microsoft/TypeScript/issues/63378) (Open, `Domain: check: Type Inference`, `Possible Improvement`)

**Object properties are inferred in the wrong order: should infer properties with \`NoInfer\<T\>\` AFTER properties with \`T\`**

*TypeScript infers object properties with NoInfer<T> before plain generics rather than after, causing inconsistent inference order.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63378#issuecomment-4216001335) **denis-migdal** clarified their issue is a specific subcase of #47599 and described the observed inference behavior with and without attachController
 * (5 days ago) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: check: Type Inference`

### [Issue microsoft/TypeScript#63380](https://github.com/microsoft/TypeScript/issues/63380) (Open, `Bug`, `Domain: check: Type Inference`)

**Wrong inference for defaulted generic in nested call**

*TypeScript fails to infer the correct return type for nested calls to a generic function with a default type parameter.*

 * created by **TurtIeSocks**
 * (5 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: check: Type Inference`

### [Issue microsoft/TypeScript#63382](https://github.com/microsoft/TypeScript/issues/63382) (Open, **mjbvz**)

**Typescript Server syntax highlighting bug: introduced by recent update**

*The latest VS Code update causes the TypeScript server to ignore custom global types, resulting in red syntax errors.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63382#issuecomment-4218277248) **RedCMD** said "typeRoots or types?"
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63382#issuecomment-4218277267) **kidCaulfield** clarified that typeRoots includes the global types folder, explained the docs distinction with types, and reported that switching to types reintroduced the VS Code syntax highlighting issue after restarting the TS server
 * [today](https://github.com/microsoft/TypeScript/issues/63382#issuecomment-4245536013) **RyanCavanaugh** provided automated suggestions for including declaration files and linking to relevant FAQs and similar issues

### [Issue microsoft/TypeScript#63385](https://github.com/microsoft/TypeScript/issues/63385) (Closed, `Design Limitation`)

**\`null\`/\`undefined\` guards sometimes adds \`& \({} \| undefined\`/\`& \({} \| null\` \(out of nowhere\) to the tested variable\.**

*Null guards in generic functions introduce an unintended intersection with {} | null or undefined into the variable's type.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4236078898) **mkantor** praised the AnyX workaround, suggested using type parameter defaults and infer to extract constraints, endorsed the '?' proposal as lower priority, recommended aligning its syntax with partial type argument inference and HKT proposals, and advised opening or finding an existing issue to pitch it
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4236340685) **denis-migdal** noted that many people use X<any> without noticing its dangers and described his surprise at how the any constraint behaved, mentioned he found no existing issues on the topic, and stated he would wait for Ryan before opening a suggestion issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4236655344) **denis-migdal** suggested a fourth workaround using an Ensure<T, U> type with example and linked to a Playground; noted uncertainty about inference in complex cases and preference for variance keywords
 * [today](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4245536168) **RyanCavanaugh** provided auto-generated analysis with links to similar issues and explained type guard behavior in generics
 * [today](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4245586969) **denis-migdal** pointed out that GetHooks<WithHooks<any>> resolved to any despite constraints and said they would read related issues and propose a more secure way to express T<any>.
 * (today) **RyanCavanaugh** added labels `Not a Defect`, `Design Limitation`, and removed label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4246755155) **RyanCavanaugh** said "I don't really see a way to fix this without breaking other CFA scenarios at the moment."

### [PR microsoft/TypeScript#63386](https://github.com/microsoft/TypeScript/pull/63386) (Open)

**Document charAt edge case behavior**

*Document that String.charAt returns an empty string for indexes outside the valid range to ensure consistency.*

 * created by **bwalter007**
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63386#issuecomment-4229758174) **afurm** acknowledged the clarification and asked whether charCodeAt, codePointAt, and substring out-of-bounds behaviors are documented and if documentation updates are needed
 * [today](https://github.com/microsoft/TypeScript/pull/63386#issuecomment-4245703846) **RyanCavanaugh** said "https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4180847265"

### [PR microsoft/TypeScript#63389](https://github.com/microsoft/TypeScript/pull/63389) (Closed)

**fix\(lib\): correct typo in es5\.d\.ts — paramater \-\> parameter**

*Corrects a typo in the es5.d.ts JSDoc comment for Array.prototype.splice, changing 'paramater' to 'parameter'.*

 * created by **hijingsong**
 * [today](https://github.com/microsoft/TypeScript/pull/63389#issuecomment-4245706598) **RyanCavanaugh** closed the PR to save CI time due to a shortage of runners
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63390](https://github.com/microsoft/TypeScript/pull/63390) (Closed, `For Uncommitted Bug`)

**feat: Higher\-Kinded Types prototype \(parser \+ RFC\)**

*Prototype parser support for higher-kinded types with an accompanying RFC outlining phased syntax, kind inference, and future checker integration.*

 * created by **SAY-5**
 * [today](https://github.com/microsoft/TypeScript/pull/63390#issuecomment-4245698097) **RyanCavanaugh** noted that the repo was closed to development and linked to the AI assistance section of the contribution guidelines
 * (today) **RyanCavanaugh** closed the issue
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63390#issuecomment-4247258973) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63390#issuecomment-4247929135) **SAY-5** said "Understood. Apologies for not reading the contributing guidelines properly."

### [Issue microsoft/TypeScript#63391](https://github.com/microsoft/TypeScript/issues/63391) (Open, `Bug`, `Domain: JS Emit`, `Fix Available`)

**The module namespace object returned by \_\_importStar is not the same when import the same module multiple times**

*TypeScript’s compiled CommonJS __importStar helper creates separate namespace objects for repeated imports of the same module.*

 * **RyanCavanaugh** added label `Bug`
 * [today](https://github.com/microsoft/TypeScript/issues/63391#issuecomment-4245031560) **RyanCavanaugh** noted that there was no reasonable space for runtime helpers to stash a global lookup table and questioned why the user was using commonjs instead of a modern target
 * **RyanCavanaugh** added to milestone `Dormant`
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: JS Emit`

### [Issue microsoft/TypeScript#63392](https://github.com/microsoft/TypeScript/issues/63392) (Open, `Docs`, **RyanCavanaugh**)

**Review/update https://typescriptlang\.org/tsconfig for TS 6\.0**

*The TypeScript tsconfig documentation is outdated for version 6.0, showing incorrect defaults and options for target, types, paths, rootDir, and module.*

 * **RyanCavanaugh** added label `Docs`
 * [today](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4244991841) **RyanCavanaugh** said "I started this at https://github.com/RyanCavanaugh/schemastore/pull/1 but haven't had time to get it over the finish line. Feel free to doublecheck this; it's not fully vetted yet."
 * **RyanCavanaugh** assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4245971467) **mkantor** asked if the tsconfig descriptions need separate updates in the TypeScript-Website repository

### [PR microsoft/TypeScript#63395](https://github.com/microsoft/TypeScript/pull/63395) (Closed, `For Backlog Bug`)

**Fix MIDIMessageEvent\.data incorrectly typed as nullable**

*Update the MIDIMessageEvent.data definition to remove its erroneous nullability and match the Web MIDI API spec.*

 * created by **Nedunchezhiyan-M**
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63395#issuecomment-4232364942) **typescript-bot** notified that the pull request updated generated DOM declaration files which should not be edited and that the PR would be closed
 * (2 days ago) **typescript-bot** closed the issue
 * **typescript-bot** added label `For Backlog Bug`

### [PR microsoft/TypeScript#63396](https://github.com/microsoft/TypeScript/pull/63396) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 2 updates**

*Update GitHub Actions group by bumping actions/upload-artifact to v7.0.1 and actions/github-script.*

 * (2 days ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63397](https://github.com/microsoft/TypeScript/issues/63397) (Open, `Suggestion`, `Needs Proposal`)

**skipLibChecks specificity**

*Enable skipLibCheck to accept glob patterns for selectively skipping type checking on specified declaration files.*

 * created by **dragomirtitian**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63397#issuecomment-4237637681) **dragomirtitian** said "This  is similar to https://github.com/microsoft/TypeScript/issues/30511 but that issue is specifically for just node_modules"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63397#issuecomment-4238179681) **guillaumebrunerie** suggested using regular .ts files with declare global blocks instead of handwritten .d.ts files to ensure proper type checking even with skipLibCheck
 * [today](https://github.com/microsoft/TypeScript/issues/63397#issuecomment-4245489788) **RyanCavanaugh** explained that skipLibCheck is a special case of a 2x2 .ts/.d.ts and checked/unchecked matrix, and observed that representing the user configuration is the main challenge
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Needs Proposal`
 * [today](https://github.com/microsoft/TypeScript/issues/63397#issuecomment-4245515366) **jakebailey** proposed introducing a new split for `.d.ts` file checking using existing root file rules

### [PR microsoft/TypeScript#63401](https://github.com/microsoft/TypeScript/pull/63401) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Also check package name validity in InstallPackageRequest**

*Add package name validation to the InstallPackageRequest code action, extending previous checks without altering security boundaries.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#63402](https://github.com/microsoft/TypeScript/pull/63402) (Closed, `For Uncommitted Bug`)

**fix: update engine requirements for Node 14 compatibility check**

*Update engine requirements to include a compatibility check for Node.js 14*

 * created by **Bodlux**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63402#issuecomment-4247711116) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63403](https://github.com/microsoft/TypeScript/issues/63403) (Closed)

**Array\.indexOf/lastIndexOf JSDoc missing \-1 return behavior**

*Array.indexOf and lastIndexOf JSDoc omit the '-1 if not found' clause, creating inconsistency with ReadonlyArray and TypedArray documentation.*

 * created by **Bodlux**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63404](https://github.com/microsoft/TypeScript/pull/63404) (Closed, `For Uncommitted Bug`)

**fix\(lib\): add missing \-1 return documentation for Array indexOf/lastIndexOf**

*Add missing JSDoc clause stating Array.indexOf and lastIndexOf return -1 when the element is not found*

 * created by **Bodlux**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63404#issuecomment-4247876497) **RyanCavanaugh** said "@bodlux you can engage with us on security in a disclosed and responsible manner, or do it the other way. Let me know which you're going for."
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63404#issuecomment-4247886110) **DanielRosenwasser** said "Context is https://github.com/microsoft/TypeScript/pull/63402"
 * [today](https://github.com/microsoft/TypeScript/pull/63404#issuecomment-4247956854) **Bodlux** asked for preferred security contact to share details of a potential CI security concern
 * [today](https://github.com/microsoft/TypeScript/pull/63404#issuecomment-4248030953) **RyanCavanaugh** said "Please consult SECURITY.md"

### [Issue microsoft/TypeScript#63405](https://github.com/microsoft/TypeScript/issues/63405) (Closed, `Question`)

**VSCode's TypeScript Language Server Keeps Crashing on a Project**

*VSCode's TypeScript server repeatedly crashes with “TSServer exited. Code: 134” when opening a basic Vite React MUI project.*

 * created by **matthew-lo-housing**
 * [later](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253248545) **hikeeba** said "Getting the exact same error on a freshly set up vite project w/ MUI and no other custom code added."
 * [later](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253249507) **RyanCavanaugh** reported that it worked fine for them and noted that the issue is unlikely to meet the servicing bar if it is machine-specific
 * (later) **RyanCavanaugh** added labels `7.0 LS Migration`, `Won't Fix`
 * [later](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253305882) **hikeeba** said "It will work for a couple of minutes, but eventually it will fill up 3GB of RAM and crash and then do that forever. I have a fresh install of VSCode."
 * [later](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253355220) **himhimlo** said "And I have the issue on both my MacBook Pro and win11 laptop. It doesn't like a very machine-specific issue."
 * **RyanCavanaugh** removed label `Won't Fix`
 * [later](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253390323) **hikeeba** stated that they tested on a Windows 11 laptop, offered to try on other machines later, and guessed that the previous test either didn’t wait long enough or didn’t include MUI lib usage
 * [later](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253431817) **RyanCavanaugh** said "Yeah, I forgot I had the TypeScript-go LS (7.0) enabled. In 6.0 I'm seeing tsserver repeatedly spawn and exit, but I'm also seeing this in TypeScript 5.9. What changed for y'all?"
 * [later](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253505723) **hikeeba** said "Unfortunately I don't have anything to point to here as for what changed. I have older projects that work, but I haven't spun up any new ones in a while until just now."

### [Issue microsoft/TypeScript#63406](https://github.com/microsoft/TypeScript/issues/63406) (Closed, `Not a Defect`)

**TS incorrectly downgrades class fields**

*TypeScript compiler incorrectly hoists class field initializations before the super call, violating subclass initialization order.*

 * created by **dangreen**
 * [later](https://github.com/microsoft/TypeScript/issues/63406#issuecomment-4252782247) **nmain** noted that the playground example gave an error and asked whether the comma operator was added intentionally or if semantics were expected to change
 * [later](https://github.com/microsoft/TypeScript/issues/63406#issuecomment-4252853758) **dangreen** noted that a type-correct example could be created but the issue would persist, and that they were using lexical@0.43.0 with ES2021 target causing the bundle to contain super(t), this.offset = e;
 * [later](https://github.com/microsoft/TypeScript/issues/63406#issuecomment-4252871588) **dangreen** acknowledged inability to create a type-correct example and noted that the issue wasn’t about types
 * [later](https://github.com/microsoft/TypeScript/issues/63406#issuecomment-4252886046) **dangreen** stated that they fixed the comma operator output issue
 * [later](https://github.com/microsoft/TypeScript/issues/63406#issuecomment-4252896319) **mkantor** said "Why are you running https://app.unpkg.com/lexical@0.43.0/files/Lexical.prod.mjs through tsc in the first place? That file is already valid JavaScript and it has no type annotations."
 * [later](https://github.com/microsoft/TypeScript/issues/63406#issuecomment-4252904980) **dangreen** said "@mkantor we want to transpile it to es2021 "
 * **RyanCavanaugh** added label `Not a Defect`
 * [later](https://github.com/microsoft/TypeScript/issues/63406#issuecomment-4253193942) **RyanCavanaugh** noted limitations in the downleveler and suggested using other tools for downleveling arbitrary third-party code

