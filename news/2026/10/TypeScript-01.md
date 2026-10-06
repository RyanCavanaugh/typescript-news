# Report for 2026-10-01 (Thursday, October 1st, 2026)

19 different users commented on 48 different issues.

## Recommended Actions

 * Moderation
    * @skywalkersPadawan posted automated policy text in [microsoft/TypeScript#64587](https://github.com/microsoft/TypeScript/pull/64587#issuecomment-5950585432)
 * Response Recommended
    * @jedwards1211 asked about exporting both named types and a CJS default export from the same file in [microsoft/TypeScript#64249](https://github.com/microsoft/TypeScript/issues/64249#issuecomment-5938446060)
    * @jedwards1211 asked for suggestions on dual CJS/ESM package strategies in [microsoft/TypeScript#64249](https://github.com/microsoft/TypeScript/issues/64249#issuecomment-5940951185)
    * @leonidaz suggested skipping extensions that registered content mappers to avoid warnings and noted a timing detail for re-running the check in [microsoft/TypeScript#64356](https://github.com/microsoft/TypeScript/issues/64356#issuecomment-5936832948)
    * @skywalkersPadawan asked if the issue needs to be linked or triaged differently in [microsoft/TypeScript#64450](https://github.com/microsoft/TypeScript/issues/64450#issuecomment-5950681585)
    * @microsoft-github-policy-service asked the contributor to agree to the CLA in [microsoft/TypeScript#64575](https://github.com/microsoft/TypeScript/pull/64575#issuecomment-5937084410)

## Activity Summary

### [Issue microsoft/TypeScript#54192](https://github.com/microsoft/TypeScript/issues/54192) (Closed, `Suggestion`, `Awaiting More Feedback`)

**Add JSON schema to the \`typescript\` package for \`tsconfig\.json\` and \`jsconfig\.json\`**

*Add maintained JSON schemas for tsconfig.json and jsconfig.json to the TypeScript package for version alignment and offline support.*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/54192#issuecomment-1823064129) **terenc3** said "I agree. A local schema file is better. compodoc is doing it also this way, see [FEATURE] Provide a JSON Schema for JSON Configuration File. #577"
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/54192#issuecomment-3232744406) **jonasgeiler** said "Biome.js has also started doing this and it's very convenient: https://biomejs.dev/reference/configuration/#schema"
 * [44 weeks ago](https://github.com/microsoft/TypeScript/issues/54192#issuecomment-3580656475) **XantreDev** said "Should we open a PR with a copy of json file from https://json.schemastore.org/tsconfig xD? "
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62239](https://github.com/microsoft/TypeScript/issues/62239) (Closed, `Help Wanted`, `Domain: ES Modules`, `Possible Improvement`)

**\`verbatimModuleSyntax\` leaves empty curly brackets in the JS output**

*With verbatimModuleSyntax enabled, TypeScript emits import statements with unnecessary empty braces after removing type-only imports.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/62239#issuecomment-3232681463) **codenamenam** explained the principle of verbatimModuleSyntax, described the assumption about type-only named imports, and adjusted the code to remove empty braces only when a default import was present
 * **RyanCavanaugh** added label `Domain: ES Modules`
 * [today](https://github.com/microsoft/TypeScript/issues/62239#issuecomment-5942142617) **jakebailey** said "A long time on and I believe that this was misclassified; import { type Foo } from "foo" means to elide Foo, not the import, and that's what type stripping, esbuild, etc, all do."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63701](https://github.com/microsoft/TypeScript/issues/63701) (Closed, `Suggestion`, `Committed`, `Domain: lib.d.ts`)

**Support \`Promise\.allKeyed\`/\`Promise\.allSettledKeyed\` methods in \`esnext\` \(eventually \`es2027\`\)**

*Add support for Promise.allKeyed and Promise.allSettledKeyed in TypeScript 7.1’s esnext library to implement the stage 3 await dictionary proposal.*

 * (8 weeks ago) **DanielRosenwasser** added label `Domain: lib.d.ts`, and removed labels `Fix Available`, `lib update`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63825](https://github.com/microsoft/TypeScript/issues/63825) (Closed, `Needs More Info`, `Needs Investigation`, `Domain: Declaration Emit`)

**\`DeepCloneNode\` allocation runaway \(44 GB / 308 s\) for recursive tagged\-tuple type alias**

*tsgo’s DeepCloneNode allocation spikes (44 GB over 308 s) when type-checking a recursive variadic tuple alias with a .tsbuildinfo file.*

 * (19 weeks ago) **weswigham** added labels `Domain: Declaration Emit`, `Needs More Info`, `Needs Investigation`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64093](https://github.com/microsoft/TypeScript/pull/64093) (Closed, `For Milestone Bug`)

**feat: add Promise\.allKeyed and Promise\.allSettledKeyed to esnext**

*Add Promise.allKeyed and Promise.allSettledKeyed methods to the ESNext Promise API.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Milestone Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64093#issuecomment-5876580113) **DanielRosenwasser** said "After the merge conflicts we can get it in. Thanks for the patience here!"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64249](https://github.com/microsoft/TypeScript/issues/64249) (Closed, `Needs Investigation`, **weswigham**)

**Spurious TS4094 "exported anonymous class type may not be private" error after upgrading from TS6 to TS7**

*Upgrading from TypeScript 6 to 7 causes TS4094 errors on exported anonymous ZodRoute instances due to private class properties.*

 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/issues/64249#issuecomment-5936794340) **weswigham** described an error in the zod-route-schemas declaration file on TS versions before 7, explained the undefined behavior and new TS7 merge-aliasing rules, and opened issue #64573 with a fix
 * [today](https://github.com/microsoft/TypeScript/issues/64249#issuecomment-5938446060) **jedwards1211** asked whether there was any valid way to export both named types and a CJS default export from the same file and criticized the limitation
 * [today](https://github.com/microsoft/TypeScript/issues/64249#issuecomment-5939320315) **weswigham** demonstrated merging a namespace with a class to export both named types and a CJS default export
 * [today](https://github.com/microsoft/TypeScript/issues/64249#issuecomment-5939360279) **weswigham** clarified that the source uses export default rather than export= and therefore doesn’t require export=
 * (today) **weswigham** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/64249#issuecomment-5940951185) **jedwards1211** expressed surprise at namespace import behavior, explained transpiling the same source to both CJS and ESM with associated drawbacks, and asked for better approaches

### [Issue microsoft/TypeScript#64271](https://github.com/microsoft/TypeScript/issues/64271) (Closed)

**CSOAI — TypeScript AI governance**

*The CSOAI TypeScript AI governance proposal has been withdrawn with no further action required.*

 * created by **CSOAI-ORG**
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64271#issuecomment-5674854371) **MartinJohns** said "Even more AI spam, lovely."
 * (today) **CSOAI-ORG** closed the issue

### [Issue microsoft/TypeScript#64356](https://github.com/microsoft/TypeScript/issues/64356) (Open, `Needs Investigation`, `Domain: Content Mappers`, **andrewbranch**)

**TypeScript 7 VS Code extension: let extensions that serve their language through content mappers opt out of the tsserver\-plugin warning**

*Enable extensions using TypeScript 7 content mappers to suppress tsserver-plugin warnings via a declarative flag*

 * (1 week ago) **RyanCavanaugh** added labels `Needs Investigation`, `Domain: Content Mappers`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/64356#issuecomment-5936832948) **leonidaz** suggested using registered content mappers to skip tsserver plugin warnings instead of requiring manifest flags and noted a timing detail about re-running the check after registration

### [Issue microsoft/TypeScript#64450](https://github.com/microsoft/TypeScript/issues/64450) (Closed, `Needs Investigation`, **johnfav03**)

**createWatchProgram\(\)\.close\(\) does not cancel the pending program update timer**

*close() does not cancel the pending program update timer in createWatchProgram, causing updates to run after closure and preventing process exit.*

 * created by **sdjayna**
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**
 * [later](https://github.com/microsoft/TypeScript/issues/64450#issuecomment-5950681585) **skywalkersPadawan** opened PR #64587 targeting release-6.0 that cleared the pending timerToUpdateProgram in createWatchProgram().close with a regression test and asked if the issue needs linking or different triage

### [PR microsoft/TypeScript#64457](https://github.com/microsoft/TypeScript/pull/64457) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Generate compiler option definitions, create JSON schema**

*Generate compiler option metadata to code-generate Go and TypeScript bindings and include a JSON schema in the package*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64457#issuecomment-5900957359) **andrewbranch** mentioned that he moved user preferences generation to JSON because Go's type system is less expressive than TypeScript's
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64457#issuecomment-5914329460) **weswigham** suggested generating the CompilerOptions interface in generate-options.ts and updating gen-proto to import the generated type to remove sequencing-reliant codegen
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64457#issuecomment-5915118799) **jakebailey** offered to fix the sequencing-reliant codegen dependency
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64536](https://github.com/microsoft/TypeScript/pull/64536) (Closed, `For Backlog Bug`)

**Fix Array\.at documentation: change 'code unit' to 'item'**

*Updated Array.at and TypedArray.at documentation to replace 'code unit' with 'item' in index parameter descriptions.*

 * (2 days ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64536#issuecomment-5900379984) **RyanCavanaugh** said "This is good to go but I can't merge it until the CLA is signed"
 * [later](https://github.com/microsoft/TypeScript/pull/64536#issuecomment-5948397985) **iamawanishmaurya** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64539](https://github.com/microsoft/TypeScript/pull/64539) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fuse local syntax lowerings into one traversal**

*Combining local syntax lowerings into one transformer traversal to boost performance and reduce memory usage pending benchmarks.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5896681435) **typescript-automation[bot]** reported CI build jobs start and provided status table with result links
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5897198748) **typescript-automation[bot]** provided the requested perf run results
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5897621618) **jakebailey** said "No change???"
 * [today](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5937115274) **weswigham** described his plan to update transformers.Chain to track the full transform stack during traversal and perform walk-fusion

### [PR microsoft/TypeScript#64544](https://github.com/microsoft/TypeScript/pull/64544) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Typed path prep bugfixes**

*Pulled out typed path preparation bugfixes from PR 64159 for separate early review and merge.*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64556](https://github.com/microsoft/TypeScript/pull/64556) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Detect cycles while serializing array and tuple types**

*Handle deferred references in the node builder to detect cycles and prevent infinite recursion during array and tuple type serialization.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64556#issuecomment-5916394736) **typescript-automation[bot]** reported that user tests with tsc comparing main and refs/pull/64556/merge looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64556#issuecomment-5917145787) **typescript-automation[bot]** reported that comparing tsc runs on the top 400 repos between main and the PR merge showed no issues
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64556#issuecomment-5925279660) **jakebailey** said "Yeah, I agree. I pushed up a new version that tries to do what you suggested. It got funky because it turns out that these do not play well with caching if they actually make it there..."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64561](https://github.com/microsoft/TypeScript/pull/64561) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**\[release\-7\.0\] Stabilize merged declaration diagnostics**

*Stabilize merged declaration diagnostics in release-7.0 to ensure deterministic reporting during DT runs.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64564](https://github.com/microsoft/TypeScript/issues/64564) (Closed, `Domain: Content Mappers`, **andrewbranch**)

**TypeScript 7 VS Code extension: closing JSX tags are not inserted in content\-mapped files, although tsc \-\-lsp provides them**

*The VS Code TypeScript 7 extension omits on-auto-insert for closing JSX tags in content-mapped files despite language server support.*

 * created by **leonidaz**
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#64566](https://github.com/microsoft/TypeScript/pull/64566) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Stabilize merged declaration diagnostic ownership**

*Stabilize merged declaration diagnostic ownership to eliminate nondeterministic diagnostic reporting in DT 7.0.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64566#issuecomment-5925240251) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64566#issuecomment-5925313131) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64566#issuecomment-5926316929) **typescript-automation[bot]** reported test results for the top 1000 repositories and confirmed everything looked good
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64569](https://github.com/microsoft/TypeScript/issues/64569) (Closed, `Bug`, **weswigham**)

**The with statement causes a panic in CommonJS\.**

*A with statement in a CommonJS module triggers a nil pointer dereference panic in the TypeScript compiler.*

 * created by **luchenxu73**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/issues/64569#issuecomment-5936145861) **RyanCavanaugh** said "Not quite sure about that fix - @weswigham ?"
 * **RyanCavanaugh** added to milestone `Backlog`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64571](https://github.com/microsoft/TypeScript/pull/64571) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add \`getSymbol\(decl\)\`**

*Add API method getSymbol(decl) to retrieve unmerged, binder-produced symbols directly from declarations without requiring a type checker.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64572](https://github.com/microsoft/TypeScript/pull/64572) (Closed, `For Uncommitted Bug`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**Enable JSX auto\-insert in content\-mapped files**

*Enable JSX closing tag auto-insertion in content-mapped files by extending auto-insert registration and updating event listeners.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64572#issuecomment-5939616122) **jakebailey** said "This seems like a good fix but I'm a bit confused how it fixes the linked issue."

### [PR microsoft/TypeScript#64573](https://github.com/microsoft/TypeScript/pull/64573) (Closed, `Author: Team`, `For Milestone Bug`, **weswigham**)

**Fix export= class visibility alongside top\-level export type**

*Fix visibility of export= class declarations merged with a top-level export type through recursive alias resolution.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64574](https://github.com/microsoft/TypeScript/pull/64574) (Closed, `For Milestone Bug`, **weswigham**)

**fix with statement crash**

*Compiler crash occurs when processing with statements in TypeScript code.*

 * created by **luchenxu73**
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64575](https://github.com/microsoft/TypeScript/pull/64575) (Open, `For Uncommitted Bug`)

**Add regression test for jsxImportSource in non\-module files**

*Add regression test ensuring jsxImportSource resolution works in non-module script files as in modules.*

 * created by **pmudassir**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64575#issuecomment-5937084410) **microsoft-github-policy-service[bot]** prompted the user to agree to the Contributor License Agreement and reply with a formatted confirmation

### [Issue microsoft/TypeScript#64576](https://github.com/microsoft/TypeScript/issues/64576) (Open)

**TypeScript 7 VS Code extension: Go to Source Definition does not run in content\-mapped files, although tsc \-\-lsp answers for them**

*Go to Source Definition fails for content-mapped files in the TypeScript 7 VS Code extension due to language ID filtering despite LSP support.*

 * created by **leonidaz**

### [PR microsoft/TypeScript#64577](https://github.com/microsoft/TypeScript/pull/64577) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Update Security Information**

*Clarify the meaning of the workspace trust dialog to address remote code execution concerns.*

 * created by **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64577#issuecomment-5940574365) **RyanCavanaugh** explained that people were running dumb scanners and recommended they run a smarter checker instead

### [PR microsoft/TypeScript#64578](https://github.com/microsoft/TypeScript/pull/64578) (Closed, `For Backlog Bug`)

**Elide empty named imports next to a default import under verbatimModuleSyntax**

*With verbatimModuleSyntax enabled, TypeScript now omits empty named-import braces following a default import when all named imports are type-only.*

 * created by **maksim-romanov**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64578#issuecomment-5940476678) **maksim-romanov** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64578#issuecomment-5941616550) **jakebailey** said "I thought this behavior was intentional? @andrewbranch "
 * [today](https://github.com/microsoft/TypeScript/pull/64578#issuecomment-5942005562) **maksim-romanov** said "Ryan marked #62239 Help Wanted and approved the same fix in #62349. import { type T } still emits import {}, only the default import case changes."
 * [today](https://github.com/microsoft/TypeScript/pull/64578#issuecomment-5942032746) **jakebailey** said "Yes, because import { type Foo } from "foo" means "erase Foo", which nets import {} from "foo". This is also how erasable types works in Node, 99% sure."
 * [today](https://github.com/microsoft/TypeScript/pull/64578#issuecomment-5942122247) **maksim-romanov** said "Makes sense. Node's type stripping, ts-blank-space and esbuild all keep the {} too, so the current output is the consistent one. Closing."
 * (today) **maksim-romanov** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64578#issuecomment-5942236674) **jakebailey** said "Sorry, I misread the issue; I didn't realize that the first default import was not also a type import. I think eliding the {} is fine so long as default is not a type import."
 * (today) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64578#issuecomment-5942274796) **jakebailey** said "import type A1, { type T } is illegal already, because we smartly realized this would be ambiguous 🤦 "
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64579](https://github.com/microsoft/TypeScript/issues/64579) (Open)

**Content mappers: let a mapper opt out of formatting, so tsc \-\-lsp does not offer a formatter that returns no edits**

*Allow mappers to disable formatting registrations in tsc --lsp so editors no longer list ineffective TypeScript formatter*

 * created by **leonidaz**

### [Issue microsoft/TypeScript#64580](https://github.com/microsoft/TypeScript/issues/64580) (Open)

**TypeScript 7 VS Code extension: let other extensions send requests to tsc \-\-lsp, like typescript\.tsserverRequest**

*Add support in the TypeScript 7 VS Code extension for other extensions to send tsc --lsp requests for content-mapped languages.*

 * created by **leonidaz**

### [PR microsoft/TypeScript#64581](https://github.com/microsoft/TypeScript/pull/64581) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Add content mapper output extensions**

*Add support for specifying content mapper output file extension mappings in TypeScript configs and package manifests.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64582](https://github.com/microsoft/TypeScript/issues/64582) (Open, `Possible Improvement`)

**Info missing when hover on a proptery compare to TS6**

*TS7 hover on an index-signature property shows only its base type instead of the full index signature info from TS6.*

 * created by **Withered-Flower-0422**

### [PR microsoft/TypeScript#64583](https://github.com/microsoft/TypeScript/pull/64583) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Allow other VS Code extensions to install LSP middleware on language feature responses**

*Enable third-party VS Code extensions to register custom LSP middleware for TypeScript language feature responses*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64584](https://github.com/microsoft/TypeScript/pull/64584) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Stop dropping dispose Promises in the async API**

*Fix async API to use Symbol.asyncDispose instead of Symbol.dispose to preserve disposal promises and update diagnostics.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64585](https://github.com/microsoft/TypeScript/issues/64585) (Open)

**TS Symbol typing clashes with standard, idiomatic JS**

*TypeScript’s symbol typing model conflicts with JavaScript’s native Symbol behavior, hindering idiomatic JS symbol usage.*

 * created by **michaelfig**

### [PR microsoft/TypeScript#64586](https://github.com/microsoft/TypeScript/pull/64586) (Open, `For Backlog Bug`)

**Restore index signature details in property hovers**

*Restore index signature details in TypeScript property hover tooltips to show key and value type information.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64587](https://github.com/microsoft/TypeScript/pull/64587) (Closed, `For Uncommitted Bug`)

**fix\(64450\): clear the pending program update timer when a watch program is closed**

*Clear the pending program update timer when a watch program is closed to prevent lingering watchers and process hangs.*

 * created by **skywalkersPadawan**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64587#issuecomment-5950280054) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64587#issuecomment-5950585432) **skywalkersPadawan** pasted the Contributor License Agreement instructions
 * (later) **skywalkersPadawan** closed the issue
 * (later) **skywalkersPadawan** reopened the issue
 * [later](https://github.com/microsoft/TypeScript/pull/64587#issuecomment-5950617247) **skywalkersPadawan** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64588](https://github.com/microsoft/TypeScript/pull/64588) (Open, `For Uncommitted Bug`)

**Restore symbol names in JSX import action titles**

*Restores symbol names in JSX import action titles by porting Strada’s logic and fixes two skipped tests.*

 * created by **Andarist**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64588#issuecomment-5953399343) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64589](https://github.com/microsoft/TypeScript/issues/64589) (Closed, `Bug`, **ahejlsberg**)

**TS 7: declaration emit prints union members in a different order from run to run**

*TS 7’s declaration emitter produces union types with non-deterministic member ordering across runs, causing unstable declaration files.*

 * created by **kristojorg**
 * (later) **ahejlsberg** added label `Bug`, set milestone to `TypeScript 7.1.0 Beta`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#64590](https://github.com/microsoft/TypeScript/issues/64590) (Open)

**Declaration emit writes an import the file cannot resolve when the package has \`exports\`; no TS2883**

*TypeScript’s declaration emit generates unresolved imports for packages with an exports map in pnpm layouts without emitting TS2883 errors*

 * created by **kristojorg**

### [Issue microsoft/TypeScript#64591](https://github.com/microsoft/TypeScript/issues/64591) (Open)

**\`tsc \-b\`: incremental build keeps a declaration that names a removed re\-export, and passes a program a clean build rejects**

*An incremental TypeScript build retains stale declarations for a removed re-export, causing inconsistent successes compared to a clean build.*

 * created by **kristojorg**

### [PR microsoft/TypeScript#64592](https://github.com/microsoft/TypeScript/pull/64592) (Open, `For Uncommitted Bug`)

**Use numeric literal source text when formatting property access**

*Format property access expressions using the original numeric literal source text rather than a reformatted value.*

 * created by **Andarist**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64592#issuecomment-5954642319) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64593](https://github.com/microsoft/TypeScript/issues/64593) (Open)

**Reverse\-mapped inference exposes private members as public; since \#63932 this rejects \`f\<T\>\(\) as C\`**

*Since PR #63932, reverse-mapped type inference exposes private members as public, causing errors when casting Readonly<Account & T> to Account.*

 * created by **kirkouimet**

### [PR microsoft/TypeScript#64594](https://github.com/microsoft/TypeScript/pull/64594) (Open, `For Uncommitted Bug`)

**Skip non\-public members when resolving reverse\-mapped types**

*Skip non-public class members when resolving reverse-mapped types to prevent them from becoming erroneously public.*

 * created by **kirkouimet**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64594#issuecomment-5956190388) **kirkouimet** said "@microsoft-github-policy-service agree"

