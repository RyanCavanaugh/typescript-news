# Report for 2026-09-30 (Wednesday, September 30th, 2026)

24 different users commented on 50 different issues.

## Recommended Actions

 * Response Recommended
    * @csvn asked if there has been any internal discussion on this issue in [microsoft/TypeScript#60948](https://github.com/microsoft/TypeScript/issues/60948#issuecomment-5932695631)
    * @unrevised6419 reported that the docs still describe `extends` as a string only in [microsoft/TypeScript#62915](https://github.com/microsoft/TypeScript/issues/62915#issuecomment-5921269382)
    * @VedantMadane asked whether es2025.json is still desired given earlier feedback in [microsoft/TypeScript#63248](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-5927679800)
    * @futursolo asked if the Node.js API's resolve source code content feature could avoid implementing zip file system in [microsoft/TypeScript#63919](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5928111641)
    * @hardikkaurani provided implementation updates and updated regression tests as requested in [microsoft/TypeScript#64527](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5917608212)
    * @hardikkaurani asked if the implementation aligns with intended behavior and if any further changes were needed in [microsoft/TypeScript#64527](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5924505152)
    * @hardikkaurani asked for intended compatibility semantics for wildcard resolution in [microsoft/TypeScript#64527](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5926959590)
    * @leonidaz filed a new issue with a suggestion and proposed closing the current issue in favor of #64560 in [microsoft/TypeScript#64548](https://github.com/microsoft/TypeScript/issues/64548#issuecomment-5916751267)
    * @KostyaTretyak reported the issue still persists in VS Code v1.140.0 and provided environment details in [microsoft/TypeScript#64568](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-5931170276)

## Activity Summary

### [Issue microsoft/TypeScript#29400](https://github.com/microsoft/TypeScript/issues/29400) (Open, `Suggestion`, `Needs Proposal`, `Domain: check: Type Inference`)

**generic function parameter infers boolean as true**

*A generic function with a boolean-defaulted parameter using T|false erroneously infers T as true instead of boolean.*

 * (7.7 years ago) **weswigham** added labels `Suggestion`, `Needs Proposal`, `Domain: Type Inference`
 * [today](https://github.com/microsoft/TypeScript/issues/29400#issuecomment-5917114435) **GrantGryczan** said "While I don't like it in this case, this behavior is intentional as per #10676."

### [Issue microsoft/TypeScript#59271](https://github.com/microsoft/TypeScript/issues/59271) (Closed, `Bug`, `Help Wanted`, `Domain: check: Type Circularity`)

**\[Regression\] Circular reference error when passing a class expression with non\-primitive static properties to a generic function**

*TypeScript 4.1.5 regresses by inferring “any” and throwing circular reference errors on non-primitive static class properties in generic functions.*

 * (2.2 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Type Circularity`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#60948](https://github.com/microsoft/TypeScript/issues/60948) (Open, `Needs More Info`)

**'identity' modifier to indicate a function's parameter\-less returns should be narrowed like a value**

*Add an identity modifier to TypeScript to mark parameterless functions as returning stable cached values so their results can be type-narrowed.*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/60948#issuecomment-2637387587) **andreialecu** suggested reviving and fast-tracking the Declarations-in-Conditionals proposal
 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/60948#issuecomment-2637764912) **shicks** suggested explicitly tagging methods as `mutating` to manage signal mutations and improve developer experience
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/60948#issuecomment-2714362449) **JeanMeche** asked what the next steps for the discussion were and whether more feedback was expected
 * [later](https://github.com/microsoft/TypeScript/issues/60948#issuecomment-5932695631) **csvn** asked whether there had been internal discussion on the issue of param-less getter function narrowing in switch patterns

### [Issue microsoft/TypeScript#61216](https://github.com/microsoft/TypeScript/issues/61216) (Closed, `Suggestion`, `Help Wanted`, `Committed`)

**Support source phase imports**

*Enable TC39 source phase imports in TypeScript to allow importing raw WebAssembly modules directly.*

 * **jakebailey** removed label `Fix Available`
 * (5 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.1`, and removed from milestone `TypeScript 5.9.0`
 * [today](https://github.com/microsoft/TypeScript/issues/61216#issuecomment-5914953287) **RyanCavanaugh** described offline discussion and proposed a minimal implementation for source-phase imports in 7.1

### [Issue microsoft/TypeScript#62552](https://github.com/microsoft/TypeScript/issues/62552) (Closed, `Help Wanted`, `Domain: check: Type Inference`, `Possible Improvement`)

**Incorrect report of self\-referencing type for static fields**

*TypeScript erroneously reports TS7022 for static fields initialized via a generic identity function in classes wrapped by id.*

 * (51 weeks ago) **RyanCavanaugh** added labels `Possible Improvement`, `Domain: Type Inference`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62915](https://github.com/microsoft/TypeScript/issues/62915) (Open, `Help Wanted`, `Docs`)

**Document that compiler\.extends can be an array**

*Update tsconfig.json documentation to indicate that the compiler.extends option can accept an array of configurations.*

 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/62915#issuecomment-3723285450) **aaron-seq** announced intent to create a PR updating the TypeScript-Website documentation to clarify that `extends` can accept an array of configuration files
 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/62915#issuecomment-3745705505) **saksham-sankhla04** said "Hi, I would Like to work on this"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62915#issuecomment-5661966799) **anbv29** said "hey, can i be assigned this issue? I would love to work on it."
 * [today](https://github.com/microsoft/TypeScript/issues/62915#issuecomment-5921269382) **unrevised6419** listed open and closed PRs addressing a change and noted that the docs still describe `extends` as a string only

### [PR microsoft/TypeScript#63248](https://github.com/microsoft/TypeScript/pull/63248) (Closed, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Add lib types for JSON\.rawJSON, JSON\.isRawJSON, and reviver context**

*Add ES2025 JSON lib type definitions for JSON.rawJSON, JSON.isRawJSON, and JSON.parse reviver context support.*

 * [22 weeks ago](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-4346296546) **MulverineX** said "@RyanCavanaugh the commandLineParser.ts has since been removed, is there a reason this PR is not proceeding?"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-5398875333) **MulverineX** said "Even if this is a bot this is still something that needs to get implemented, its pretty annoying to have to vendor these types in"
 * (later) **VedantMadane** closed the issue
 * (later) **VedantMadane** reopened the issue
 * [later](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-5927679800) **VedantMadane** rebased onto main and resolved merge conflicts, regenerated embedded files, kept es2025 JSON typings, and called for a maintainer decision on retaining es2025.json

### [PR microsoft/TypeScript#63919](https://github.com/microsoft/TypeScript/pull/63919) (Open, `For Uncommitted Bug`)

**Add Yarn PnP module resolution support**

*Add native Yarn Plug’n’Play module resolution support to TypeScript Go, including PnP VFS, API, and manifest handling.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5898089808) **jakebailey** expressed reservations about the current PnP implementation’s design, its reliance on globals, unclear JS API integration, and uncertain ecosystem adoption
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5901034425) **arcanis** explained that Node 26+ package maps could be seen as the standard successor to PnP, shipping since Node v26.4, supported by Yarn, pnpm, and soon Vite, and compatible with node_modules installs unlike PnP
 * [today](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5908981564) **futursolo** suggested supporting the Node.js loader API as a pathway to support PnP with smaller modifications and noted that package maps lack many PnP benefits
 * [today](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5915375074) **jakebailey** explained that using the JS API would require executing content mappers and handling zip files, offering no advantage over package maps
 * [later](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5928111641) **futursolo** suggested using the Node.js API's resolve source code content feature to avoid implementing zip file system

### [Issue microsoft/TypeScript#64094](https://github.com/microsoft/TypeScript/issues/64094) (Open, `Suggestion`)

**typescript\-language\-server does not work with @typescript/typescript6**

*typescript-language-server is incompatible with @typescript/typescript6 due to a missing tsserver.js wrapper in its lib directory.*

 * created by **guillaumebrunerie**
 * **RyanCavanaugh** added label `Suggestion`

### [PR microsoft/TypeScript#64243](https://github.com/microsoft/TypeScript/pull/64243) (Closed, `For Uncommitted Bug`)

**fix: disallow NoSubstitutionTemplate in module import attribute types**

*Enforce rejecting empty template literals in module import attribute types by requiring quoted string literals.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5638319287) **DanielRosenwasser** appreciated test coverage and asked if there are tests for template string types with interpolations, requesting their addition if missing
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5647642629) **camc314** explained that requiring quoted string literals is better design due to spec distinctions and consistency; noted the downstream tool impact and that it can change since unreleased; added a test case for template string types with interpolations
 * [today](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5909635356) **camc314** pinged maintainers for clarity before the 7.1 beta to avoid blocking user adoption
 * [today](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5915402698) **camc314** said "Thanks Ryan!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64300](https://github.com/microsoft/TypeScript/issues/64300) (Open, `Needs Investigation`, **jakebailey**)

**\[TS7 LSP\] Panic on document URI "file://" \(empty path\): vfs: path "tsconfig\.json" is not absolute**

*TypeScript 7 Go LSP panics on a 'file://' URI with an empty path because it expects an absolute tsconfig.json path.*

 * created by **chenxin-yan**
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64300#issuecomment-5706934663) **jakebailey** said "How did you find this? (I can't imagine any client trying to use an empty file URI?)"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64300#issuecomment-5707036878) **chenxin-yan** described using tsc lsp with Neovim and how vim.lsp.enable auto-attached to buffers with empty names causing the error
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#64351](https://github.com/microsoft/TypeScript/issues/64351) (Closed, `Bug`, **jakebailey**)

**tsc \-\-watch never recompiles on macOS since 7\.1\.0\-dev\.20260811\.1**

*On macOS with TypeScript 7.1.0-dev.20260811.1 and later nightly builds, tsc --watch stops detecting file changes and never recompiles.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64351#issuecomment-5784637279) **jakebailey** said "Thanks. I'm scoping #64210 specifically down to the other issue, but I should be able to send a different Pr to fix this one."
 * (1 week ago) **RyanCavanaugh** added label `Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/issues/64351#issuecomment-5919941863) **leonidaz** confirmed that nightly builds after 7.1.0-dev.20260922.1 recompiled on edit, thanked @jakebailey, and closed the issue
 * (today) **leonidaz** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/64351#issuecomment-5919957433) **jakebailey** said "Oh, what? That PR was enough?"
 * [today](https://github.com/microsoft/TypeScript/issues/64351#issuecomment-5920190312) **leonidaz** said "I mean, we tried out the latest nightlies and saw both of your pr's merged and it's working now. 🤷‍♂️ "

### [Issue microsoft/TypeScript#64378](https://github.com/microsoft/TypeScript/issues/64378) (Closed, `Possible Improvement`)

**Performance: exponential check time as a chain of generic calls grows \(index signature in the inferred spec type\)**

*A string index signature in a generic command spec type causes exponentially slower TypeScript checks for long call chains.*

 * (1 week ago) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64378#issuecomment-5780416195) **RyanCavanaugh** said "@ahejlsberg maybe worth looking at"
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64457](https://github.com/microsoft/TypeScript/pull/64457) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Generate compiler option definitions, create JSON schema**

*Generate compiler option metadata to code-generate Go and TypeScript bindings and include a JSON schema in the package*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64457#issuecomment-5896253300) **jakebailey** explained that most of the content was data not types and that the AST was generated from a JSON file with a TS script, and that using a TS file made diagnostic declarations easier than a Go implementation would
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64457#issuecomment-5900957359) **andrewbranch** mentioned that he moved user preferences generation to JSON because Go's type system is less expressive than TypeScript's
 * [today](https://github.com/microsoft/TypeScript/pull/64457#issuecomment-5914329460) **weswigham** suggested generating the CompilerOptions interface in generate-options.ts and updating gen-proto to import the generated type to remove sequencing-reliant codegen
 * [today](https://github.com/microsoft/TypeScript/pull/64457#issuecomment-5915118799) **jakebailey** offered to fix the sequencing-reliant codegen dependency

### [PR microsoft/TypeScript#64461](https://github.com/microsoft/TypeScript/pull/64461) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Report cyclic structures and truncation during declaration emit**

*Enhance declaration emit to detect and report cyclic type structures and truncation instead of silently returning elided anys*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5901111734) **typescript-automation[bot]** started jobs and provided an initial status table
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5901344302) **typescript-automation[bot]** reported main-only DT test errors for wicg-task-scheduling due to incompatible scheduler type
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5901446288) **jakebailey** said "Exciting, the new DT run found a flake in main."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64475](https://github.com/microsoft/TypeScript/pull/64475) (Open, `For Uncommitted Bug`, **ahejlsberg**)

**build member tables of instantiated classes/interfaces lazily**

*Implement lazy construction of class and interface member tables to avoid unneeded instantiations and improve performance and memory usage.*

 * (2 days ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64475#issuecomment-5885611567) **maschwenk** thanked the maintainer for landing the PR and reported code size reductions and performance improvements across various projects, noted non-determinism in the never-reduction check and submitted a fix via PR #64521
 * [today](https://github.com/microsoft/TypeScript/pull/64475#issuecomment-5918854781) **ahejlsberg** thanked @maschwenk for the research, acknowledged potential wins from selective member resolution, and suggested combining the disparate code paths into a single implementation
 * [today](https://github.com/microsoft/TypeScript/pull/64475#issuecomment-5918890839) **maschwenk** said "@ahejlsberg totally understand! thank you! was just making sure it didn't drop off notifications ❤️ "

### [Issue microsoft/TypeScript#64478](https://github.com/microsoft/TypeScript/issues/64478) (Open, `Suggestion`)

**An \`internal\` property modifier as an alternative to \`protected\`**

*Introduce an internal modifier that keeps properties visible in type definitions but accessible only within class methods.*

 * **RyanCavanaugh** added label `Suggestion`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5894466979) **RyanCavanaugh** said "Even a single code example of how you'd expect this to be used would be illuminating. Honestly I'm still not understanding what the goal of this is."
 * [today](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5908822519) **denis-migdal** provided sample code illustrating possible use cases for an `internal` modifier and described current workarounds for friend functions, class implementation, and interface definitions
 * [today](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5915192668) **RyanCavanaugh** asked why the type assertion was considered safe given 'as' allows downcasting
 * [today](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5915734706) **denis-migdal** explained that casting T into Internals<T> was always correct by construction but that using 'as' directly was unsafe and a generic helper function should be used for safety

### [Issue microsoft/TypeScript#64490](https://github.com/microsoft/TypeScript/issues/64490) (Closed, `Unactionable`)

**TypeScript 7\.0\.2 scanner does not advance on bare hash**

*TypeScript 7.0.2 scanner gets stuck on a bare '#' and repeatedly returns the same token without advancing.*

 * created by **yum45f**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64490#issuecomment-5873676173) **RyanCavanaugh** said "Just calling scan in a loop isn't going to give you anything meaningful; this isn't how to use that function"
 * **RyanCavanaugh** added label `Unactionable`
 * [today](https://github.com/microsoft/TypeScript/issues/64490#issuecomment-5923007045) **typescript-automation[bot]** said "This issue has been marked as "Unactionable" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#64498](https://github.com/microsoft/TypeScript/issues/64498) (Open, `Bug`, **andrewbranch**)

**Program\.emitToString\(\) silently omits real files due to nondeterministic isSourceFileFromExternalLibrary\(\) misclassification**

*TypeScript’s Program.emitToString sometimes excludes real source files because isSourceFileFromExternalLibrary nondeterministically marks them as external library files.*

 * created by **jelical**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/64498#issuecomment-5916667448) **RyanCavanaugh** said "@jelical we're interested in how to streamline AI-assisted bug reports like this one. Can you walk me through the human-side workflow that you went through to get to this spot?"

### [PR microsoft/TypeScript#64522](https://github.com/microsoft/TypeScript/pull/64522) (Closed, `For Uncommitted Bug`)

**Fix moduleResolution \-\> customConditions test to actually apply both conditions**

*CustomConditions test in moduleResolution fails to trim whitespace on comma-separated values, resulting in only the first condition applying.*

 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64522#issuecomment-5886317751) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64525](https://github.com/microsoft/TypeScript/pull/64525) (Closed, `For Backlog Bug`)

**Avoid contextually typing static properties by their own class to prevent spurious circularities**

*Modify TypeScript’s type checker to prevent contextually typing a class’s static properties with the class itself, avoiding spurious circularities.*

 * [today](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5906028905) **typescript-automation[bot]** reported that build jobs started and provided status updates with result links
 * [today](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5906108130) **Andarist** said "Hm, ok - then that's confusing. I'll wait for the re-run results and dig into this again."
 * [today](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5906420781) **typescript-automation[bot]** reported that user tests comparison between main and the pull request merge looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64525#issuecomment-5915498915) **jakebailey** said "Ugh. I forgot that this infra is not like the benchmarker and compares against main directly instead of using the generated merge commit. I'll fix that. Carry on!"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64527](https://github.com/microsoft/TypeScript/pull/64527) (Open, `For Uncommitted Bug`)

**Fix checkJs behavior for \.mjs and \.cjs files next to declarations**

*Remove legacy wildcard exception to ensure wildcard include consistently prefers declaration files over .js, .mjs, and .cjs implementations.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5905678191) **ljharb** said "@weswigham i intentionally include a .js and .d.ts in all of my typed npm packages, and intend to continue to do so. That's the only way to write typed JS (without writing TS) that I'm aware of."
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5908105828) **hardikkaurani** thanked ljharb for context, proposed preserving the companion .js/.d.ts pattern for .mjs and .cjs files, and asked if maintainers would proceed with the current approach
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5914546447) **weswigham** rejected preserving side-by-side .js and .d.ts files and argued for aligning include behavior with modern extensions and using JSDoc-annotated JS for typing
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5917608212) **hardikkaurani** revised implementation to remove the legacy .js exception from extension priority logic and updated regression tests to assert consistent skipping of .js, .mjs, and .cjs when higher-priority .d.ts variants are present
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5923217419) **ljharb** said "I'm confused what's a footgun about the .js behavior? The footgun I see is that adding one file can cause another to silently become unchecked. I don't see why how common it is is relevant at all?"
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5924505152) **hardikkaurani** clarified that the change removed the legacy .js wildcard-resolution special-case, updated regression coverage to skip .js/.mjs/.cjs when corresponding declarations exist, and requested confirmation that this aligns with intended include-resolution behavior
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5925515517) **ljharb** said "ok but that's worse - because it indeed is silently skipping a file solely because i created another one, without any config changes. That should never be the case."
 * [later](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5926959590) **hardikkaurani** thanked ljharb for clarifying the compatibility concern and asked weswigham to clarify the intended compatibility semantics for wildcard resolution

### [Issue microsoft/TypeScript#64529](https://github.com/microsoft/TypeScript/issues/64529) (Closed, `Needs Investigation`, **ahejlsberg**)

**Type parameter escapes its constraint in a recursive call resolution**

*Recursive resolution of object calls leaks the type parameter P outside its constraint, causing incorrect inference.*

 * created by **colinhacks**
 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64530](https://github.com/microsoft/TypeScript/pull/64530) (Closed, `For Uncommitted Bug`, **ahejlsberg**)

**Keep a pure return type inference filtered by its constraint in a recursive call resolution**

*Restore constraint filtering for pure return type inferences during recursive call resolution to prevent invalid type arguments*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64530#issuecomment-5892953821) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64548](https://github.com/microsoft/TypeScript/issues/64548) (Closed, `Working as Intended`)

**Content mappers: \`moduleSuffixes\` probes \`card\.foo\.web\` instead of \`card\.web\.foo\` for a registered extension**

*When using moduleSuffixes with a registered content mapper, a fully specified import probes the suffix after the custom extension (card.foo.web) instead of before (card.web.foo), resolving to the wrong file.*

 * created by **leonidaz**
 * [today](https://github.com/microsoft/TypeScript/issues/64548#issuecomment-5915868733) **RyanCavanaugh** clarified that content mappers do not change moduleSuffixes behavior and that import specifiers must include the mapper's extension
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/64548#issuecomment-5916751267) **leonidaz** filed issue #64560 suggesting an optional moduleSuffixes list on contentMappers entries and offered to close this issue in favor of it

### [Issue microsoft/TypeScript#64549](https://github.com/microsoft/TypeScript/issues/64549) (Open, `Suggestion`)

**Content mappers: let registered extensions take part in extensionless module lookup**

*Enable TypeScript to include contentMappers’ registered custom extensions in extensionless module import resolution for bundler and Node modes*

 * created by **leonidaz**
 * [today](https://github.com/microsoft/TypeScript/issues/64549#issuecomment-5912337356) **aleclarson** described a concrete use case for cross-platform file variants with .tsrx extensions, explained the current shim workaround and its drawbacks, mentioned a one-line patch enabling resolveHiddenExtensions in TS5/Volar, and offered to share a resolution fixture
 * **RyanCavanaugh** added label `Suggestion`

### [PR microsoft/TypeScript#64551](https://github.com/microsoft/TypeScript/pull/64551) (Open, `For Uncommitted Bug`)

**perf\(checker\): fast\-path compareNodes for identical AST parent containers and use cmp\.Compare**

*Introduces a fast-path compareNodes for identical AST parents and uses cmp.Compare to prevent 64-bit symbol ID overflow.*

 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5914036976) **jakebailey** criticicized that the PR contained unrelated changes and needed splitting, and noted that increasing GOGC would increase memory footprint
 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5914567421) **hazyhaar** reduced the PR to only checker optimizations, implemented a fast-path in compareNodes for same-parent nodes, switched to cmp.Compare for SymbolId fallback, removed 32-bit ID narrowing, dropped GOGC tuning, and withdrew SIMD kernels
 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5914905234) **jakebailey** said "The PR description is still describing the original state."
 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5915554577) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5915556271) **typescript-automation[bot]** posted an automated CI status update indicating the perf test had started and linking to results
 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5915967988) **typescript-automation[bot]** said "@DanielRosenwasser, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5916078411) **jakebailey** said "mui is broken because they're using pnpm 12 which segfaults 😢 "
 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5916572770) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5916574307) **typescript-automation[bot]** posted automated build status update
 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5917030053) **typescript-automation[bot]** reported the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64551#issuecomment-5917132564) **jakebailey** suggested checking additional parent nodes and considering a more clever parent traversal to optimize comparisons

### [Issue microsoft/TypeScript#64552](https://github.com/microsoft/TypeScript/issues/64552) (Open, `Needs Investigation`, **johnfav03**)

**\`\-\-incremental\` keeps stale diagnostics after \`lib\` or \`target\` changes in tsconfig\.json \(7\.0\.2, regression from 6\.0\.3\)**

*TypeScript 7.0.2’s --incremental compiler retains stale diagnostics after toggling tsconfig.json lib or target settings.*

 * created by **valeralebedz**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**

### [PR microsoft/TypeScript#64553](https://github.com/microsoft/TypeScript/pull/64553) (Closed, `Author: Team`, `For Backlog Bug`, **ahejlsberg**)

**Cache inferences made from type arguments**

*Cache type argument inferences in the existing invokeOnce infrastructure and include variance states to prevent false matches*

 * [today](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5914522225) **ahejlsberg** asked the contributor to describe what happens in the test after manually verifying its effect on check times
 * [today](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5914537348) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5914538753) **typescript-automation[bot]** reported CI job statuses and result links for various test commands
 * [today](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5914960731) **typescript-automation[bot]** said "@ahejlsberg, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5915037001) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5915065196) **typescript-automation[bot]** provided results of running user tests comparing main and refs/pull/64553/merge and reported new type errors in webpack
 * [today](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5915827880) **typescript-automation[bot]** reported results of running the top 400 repos with tsc comparing main and the PR merge and noted everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5918651771) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5918653160) **typescript-automation[bot]** started CI jobs and displayed build status
 * [today](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5918715773) **ahejlsberg** explained that the webpack user test changes were due to different type inferences and that the resulting errors stemmed from requiring explicit typeof operators in version 7.0
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64553#issuecomment-5919122764) **typescript-automation[bot]** provided the requested perf run results in a comparison report
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64554](https://github.com/microsoft/TypeScript/pull/64554) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Ensure completion symbols returned to API always come from the current snapshot**

*Ensure completion symbols returned by the API originate from the current snapshot and allow configuring auto-import behavior.*

 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64554#issuecomment-5919622558) **andrewbranch** admitted using regex for code analysis and reported a TypeScript build error about external imports in .d.ts files
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64555](https://github.com/microsoft/TypeScript/pull/64555) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Switch signing command to msbuild**

*Switch the signing command to msbuild to remove .NET Core 3.1 from the pipeline and consolidate signing credentials.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64556](https://github.com/microsoft/TypeScript/pull/64556) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Detect cycles while serializing array and tuple types**

*Handle deferred references in the node builder to detect cycles and prevent infinite recursion during array and tuple type serialization.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64556#issuecomment-5915881475) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64556#issuecomment-5915883065) **typescript-automation[bot]** posted CI job status updates indicating start and completion statuses for test top400, user test this, run dt, and perf test this faster, with one failure
 * [today](https://github.com/microsoft/TypeScript/pull/64556#issuecomment-5916298621) **typescript-automation[bot]** reported that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64556#issuecomment-5916321649) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64556#issuecomment-5916394736) **typescript-automation[bot]** reported that user tests with tsc comparing main and refs/pull/64556/merge looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64556#issuecomment-5917145787) **typescript-automation[bot]** reported that comparing tsc runs on the top 400 repos between main and the PR merge showed no issues
 * [today](https://github.com/microsoft/TypeScript/pull/64556#issuecomment-5925279660) **jakebailey** said "Yeah, I agree. I pushed up a new version that tries to do what you suggested. It got funky because it turns out that these do not play well with caching if they actually make it there..."

### [PR microsoft/TypeScript#64558](https://github.com/microsoft/TypeScript/pull/64558) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Preserve reverse mapped types in declaration emit**

*Preserve reverse mapped types during declaration emission to eliminate silently elided anys.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64558#issuecomment-5920835235) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64558#issuecomment-5920836317) **typescript-automation[bot]** reported CI job statuses with start and result links for test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/64558#issuecomment-5921100472) **typescript-automation[bot]** reported that the DT test results were ready and everything looked the same
 * [today](https://github.com/microsoft/TypeScript/pull/64558#issuecomment-5921158049) **typescript-automation[bot]** reported that tsc user tests comparing commit 792ffccb90f548cd3bdd7fc0b44f0ca9e1b169a7 and the pull request merge passed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/64558#issuecomment-5921164862) **typescript-automation[bot]** reported the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64558#issuecomment-5921737566) **typescript-automation[bot]** reported that running tsc on the top 400 repos between the two commits succeeded without issues
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64559](https://github.com/microsoft/TypeScript/pull/64559) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Disable publish template steps for VSIX publish jobs**

*Disable publish template steps for VSIX publish jobs to prevent unnecessary ESRP signing setup.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64560](https://github.com/microsoft/TypeScript/issues/64560) (Open, `Suggestion`)

**Content mappers: a \`moduleSuffixes\` list on a \`contentMappers\` entry**

*Add an optional moduleSuffixes list to content mappers to control platform-specific file resolution order.*

 * created by **leonidaz**
 * **RyanCavanaugh** added label `Suggestion`

### [PR microsoft/TypeScript#64561](https://github.com/microsoft/TypeScript/pull/64561) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**\[release\-7\.0\] Stabilize merged declaration diagnostics**

*Stabilize merged declaration diagnostics in release-7.0 to ensure deterministic reporting during DT runs.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64562](https://github.com/microsoft/TypeScript/pull/64562) (Closed, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump brace\-expansion from 5\.0\.9 to 5\.0\.12**

*Update brace-expansion dependency from version 5.0.9 to 5.0.12.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64563](https://github.com/microsoft/TypeScript/pull/64563) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Build all platforms in parallel in release pipeline**

*Build all platforms concurrently in the release pipeline to accelerate full release builds.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#64564](https://github.com/microsoft/TypeScript/issues/64564) (Closed, `Domain: Content Mappers`, **andrewbranch**)

**TypeScript 7 VS Code extension: closing JSX tags are not inserted in content\-mapped files, although tsc \-\-lsp provides them**

*The VS Code TypeScript 7 extension omits on-auto-insert for closing JSX tags in content-mapped files despite language server support.*

 * created by **leonidaz**

### [Issue microsoft/TypeScript#64565](https://github.com/microsoft/TypeScript/issues/64565) (Open)

**TypeScript 7 VS Code extension: a workspace "typescript" 7\.x package is not detected, only "@typescript/native\-preview", which is no longer published**

*The TypeScript 7 VS Code extension fails to detect standard typescript@7 in workspace, using its bundled compiler instead.*

 * created by **leonidaz**

### [PR microsoft/TypeScript#64566](https://github.com/microsoft/TypeScript/pull/64566) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Stabilize merged declaration diagnostic ownership**

*Stabilize merged declaration diagnostic ownership to eliminate nondeterministic diagnostic reporting in DT 7.0.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64566#issuecomment-5925006446) **jakebailey** requested typescript-bot to run tests for top1000, user test, and dt
 * [today](https://github.com/microsoft/TypeScript/pull/64566#issuecomment-5925007348) **typescript-automation[bot]** posted automated build status updates for test top1000, user test this, and run dt jobs with start and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64566#issuecomment-5925240251) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64566#issuecomment-5925313131) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64566#issuecomment-5926316929) **typescript-automation[bot]** reported test results for the top 1000 repositories and confirmed everything looked good

### [PR microsoft/TypeScript#64567](https://github.com/microsoft/TypeScript/pull/64567) (Open, `For Uncommitted Bug`)

**Fix TypeScript 7 workspace package detection**

*Enhance VS Code TypeScript extension to detect TypeScript 7 installations in node_modules/typescript as well as legacy @typescript/native-preview packages.*

 * created by **Nanditha264**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64567#issuecomment-5925914328) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64567#issuecomment-5925919680) **microsoft-github-policy-service[bot]** prompted the user to agree to the Contributor License Agreement by replying with a formatted agree command

### [Issue microsoft/TypeScript#64568](https://github.com/microsoft/TypeScript/issues/64568) (Open, **dbaeumer**)

**Bug Report: Severe memory leak triggered by "TypeScript \(Native Preview\)" extension**

*Enabling the TypeScript Native Preview extension causes a memory leak when opening a TS file in a folder without package.json.*

 * created by **KostyaTretyak**
 * [today](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-5931170063) **RyanCavanaugh** said "Moving to VS Code since this repros even with the TS extension disabled"
 * [today](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-5931170176) **vs-code-engineering[bot]** thanked the user and advised updating VS Code to the latest stable release to check if the issue remained
 * **vs-code-engineering[bot]** assigned to **dbaeumer**
 * [today](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-5931170276) **KostyaTretyak** reported that the issue still persisted in VS Code v1.140.0, suspected a memory leak related to improper reading of neighboring projects, and noted using a ZFS root filesystem
 * [later](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-5931170354) **dbaeumer** said "@lszomoru since this seems to be related to having git repositories as siblings does this ring a bell for you?"
 * [later](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-5931170441) **dbaeumer** said "@lszomoru forget my last comment."
 * [later](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-5931170553) **dbaeumer** reproduced the issue using GPT-6 Astra and identified that TypeScript requests an overly broad recursive file watcher when package.json is absent, analysed the cause in watch-root calculation and parcel watcher behavior, provided memory evidence suggesting ZFS ARC fill rather than a heap leak, and requested trace-level log entries for further comparison
 * [later](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-5931170686) **dbaeumer** said "Moving back to the TS team based on the above analysis."

### [Issue microsoft/TypeScript#64569](https://github.com/microsoft/TypeScript/issues/64569) (Closed, `Bug`, **weswigham**)

**The with statement causes a panic in CommonJS\.**

*A with statement in a CommonJS module triggers a nil pointer dereference panic in the TypeScript compiler.*

 * created by **luchenxu73**

