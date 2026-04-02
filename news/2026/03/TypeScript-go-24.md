# Report for 2026-03-24 (Tuesday, March 24th, 2026)

18 different users commented on 58 different issues.

## Recommended Actions

 * Response Recommended
    * @alexwork1611 asked how the issue contributed to the creation of the --stableTypeOrdering flag in [microsoft/TypeScript-go#787](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-4119913898)
    * @alexwork1611 asked whether this issue informed the design or priority of the --stableTypeOrdering flag in TS 6.0 in [microsoft/TypeScript-go#787](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-4125698998)

## Activity Summary

### [Issue microsoft/TypeScript-go#1317](https://github.com/microsoft/TypeScript-go/issues/1317) (Open, `Domain: CLI`, `Domain: Performance`, **johnfav03**)

**High CPU usage with \-\-watch when idling on MacOS**

*Running tsgo in watch mode on MacOS consumes abnormally high CPU (120–170%) even when idle, unlike tsc -w.*

 * [34 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1317#issuecomment-3114860336) **sheetalkamat** said "@tmm1 please open new issue, providing repro steps to investigate the crash."
 * **jakebailey** added label `Domain: Performance`
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/1317#issuecomment-3928808922) **nfarina** suggested adding fsevents support and a custom watcher.go to improve watch mode CPU usage by building a local tsgo binary
 * [later](https://github.com/microsoft/TypeScript-go/issues/1317#issuecomment-4124796852) **alexswan93** reported similar idle CPU usage on Windows in watch mode with @typescript/native-preview v7.0.0-dev.20260324.1 and noted using tsgo as a workaround

### [Issue microsoft/TypeScript-go#1637](https://github.com/microsoft/TypeScript-go/issues/1637) (Closed, `wontfix`)

**Limitation on union of mapped types \(25 members\)**

*tsgo fails to compile unions of mapped types exceeding 25 members due to TypeScript’s internal limit and requests configurability*

 * [29 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1637#issuecomment-3232333969) **nicooprat** suggested making the feature configurable as a compromise
 * [29 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1637#issuecomment-3234122207) **RyanCavanaugh** warned that configurability on type relations could cause mysterious failures when libraries and consumers used different Max Combinatorial Explosion settings
 * **jakebailey** added label `wontfix`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2020](https://github.com/microsoft/TypeScript-go/pull/2020) (Closed)

**Support for custom configurations**

*Enable passing custom tsconfig file names to the tsgo LSP to support solution-style repository configurations.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-4065010535) **sspencer-canva** mentioned that the issue had been on hold for three weeks and asked if there was anything they could do to help
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-4084912118) **jakebailey** stated that the PR needed a merge from main, that they couldn’t explain the behavior seen in testing, and that they were attempting to write a test
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-4085003788) **jakebailey** said "I think I have a test and a fix. Will push it to the PR so we can get this moving."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2503](https://github.com/microsoft/TypeScript-go/issues/2503) (Closed, **gabritto**)

**Autocomplete and auto\-import is slower in JSX context**

*JSX tag autocomplete and auto-import in TypeScript monorepos remains slow (~1s vs ~100ms) due to expensive contextual type computation.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3752145034) **gabritto** requested a repro project or CPU profile log to investigate JSX completions slowness
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3784284733) **jansedlon** said "Hey grabritto, sorry for the delay. I tried it today and for some reason it worked fine. When it happens again, i will take a cpu profile and send it to you"
 * **gabritto** assigned to **gabritto**
 * (later) **jansedlon** closed the issue

### [Issue microsoft/TypeScript-go#2655](https://github.com/microsoft/TypeScript-go/issues/2655) (Closed, `wontfix`)

**Incorrect type error when assigning to an index in a \`{}\[\]\`\-typed field where the index is any\-typed and field is defined in a base class in a JS file**

*tsgo wrongly reports type errors when assigning to an any-indexed element of a {}[] field in a JS base class.*

 * created by **peetklecha**
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2655#issuecomment-3861558989) **ahejlsberg** explained that the error was intended, clarifying that the {} in the inferred {}[] type represented the internal anyFunctionType wildcard, described tsgo's stricter subtype rules, and noted that a recent PR would cause the example to error in TS 6.0 with inferred (() => void)[], aligning tsgo behavior
 * **ahejlsberg** added label `wontfix`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2757](https://github.com/microsoft/TypeScript-go/pull/2757) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript PR \#62320: Allow \-\-module commonjs \-\-moduleResolution bundler**

*Port PR #62320 to permit bundler module resolution with CommonJS by adjusting compiler checks in program.go and updating error and output baselines.*

 * (5 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2757#issuecomment-3987516677) **jakebailey** said "Going to wait to merge this around the same time as the node10 deprecation error."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2984](https://github.com/microsoft/TypeScript-go/issues/2984) (Closed, `Domain: Editor`)

**Auto\-import with subpath imports always prioritizes relative imports**

*VSCode TypeScript auto-import suggestions ignore package.json subpath mappings and default to relative paths even when configured for shortest or non-relative imports*

 * created by **danilofuchs**
 * **danilofuchs** added label `Domain: Editor`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2984#issuecomment-4004322347) **psznm** suggested that moduleResolution nodenext might cause node imports to be looked up in the build directory and asked if the build/* did not contain the import, linking to a related issue
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3085](https://github.com/microsoft/TypeScript-go/pull/3085) (Closed)

**API: Small bug fixes**

*Fixed three bugs causing panics: empty array truthy check, RemoteNode.getNamedChild crash on no children, and arrow function printing nil check.*

 * created by **navya9singh**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3085#issuecomment-4053358530) **navya9singh** said "@copilot format"
 * (today) **navya9singh** closed the issue

### [PR microsoft/TypeScript-go#3117](https://github.com/microsoft/TypeScript-go/pull/3117) (Closed)

**Don't use parent pointer in classfields\.go visitPrivateIdentifier**

*Handle private identifier visits in classfields.go at a higher level to avoid dubious parent pointer usage.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3123](https://github.com/microsoft/TypeScript-go/pull/3123) (Closed)

**Fix auto\-import of subpath imports starting with \`\#/\` in supported module resolution modes**

*Update auto-import handling to recognize subpath imports beginning with '#/' in all supported resolution modes.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139) (Open, `Needs More Info`)

**runtime: failed to create new OS thread**

*Running tsgo on a large macFUSE-mounted TypeScript project exhausts OS threads and crashes the Go runtime.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4089048689) **vetptzru** described that running with the --singleThreaded flag prevented crashes, mentioned currently building with that flag in VS Code and asked how to pass it there, and stated that they were not using --watch
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4089083039) **vetptzru** provided screenshots showing the peak thread count the tsgo process reached before crashing
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4096913604) **vetptzru** said "@DanielRosenwasser do you need any more information from me, or is this enough?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4123683587) **jakebailey** expressed uncertainty about reproducing the issue, suggested runtime tracing might help, and asked why the issue had so many reactions

### [PR microsoft/TypeScript-go#3145](https://github.com/microsoft/TypeScript-go/pull/3145) (Closed)

**Refactor debug package to be inlinable, always enabled**

*Refactor Go debug package to always enable inlined debug asserts by eliminating reflect, interface indirection, and un-inlinable tests.*

 * created by **jakebailey**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3145#issuecomment-4092317917) **jakebailey** said "I'm refactoring this package even more, down to just having Assert as a boolean taking function. And, just deleting nodebug now."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3146](https://github.com/microsoft/TypeScript-go/issues/3146) (Closed, `bug`, `Domain: Emit`, **jakebailey**, **Copilot**)

**experimentalDecorators renames enum accesses with same name as class**

*experimentalDecorators causes enum member accesses sharing a class name to be incorrectly renamed in emitted code*

 * (6 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3146#issuecomment-4108755647) **ejekanshjain** demonstrated that with typeorm decorators and tsgo ^7.0.0-dev.20260312.1+, the emitted js code used ItemType.Product_1 instead of ItemType.Product and provided code examples
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3147](https://github.com/microsoft/TypeScript-go/pull/3147) (Closed, **jakebailey**, **Copilot**)

**Fix property access name substitution in decorator and class field transformers**

*Add explicit property access expression visitors in decorator and class-field transformers to prevent misrenaming property names that match class identifiers.*

 * **Copilot** assigned to **jakebailey**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3147#issuecomment-4084588388) **jakebailey** asked for a slew of tests to cover potential bugs in ES decorators, class fields, and similar cases
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3147#issuecomment-4084713463) **Copilot** confirmed the bug in the class fields transformer, fixed it in commit bd33135f, and added tests covering legacy decorators, class fields (including private fields), and ES decorators
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3150](https://github.com/microsoft/TypeScript-go/pull/3150) (Closed)

**Add bitclear analyzer to suggest \`&^= A\` instead of \`&= ^A\`**

*Add an analyzer to identify &= ^A bit-clearing patterns and automatically replace them with the &^= operator.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3176](https://github.com/microsoft/TypeScript-go/pull/3176) (Closed)

**Fix ref count cache inconsistencies**

*Revert cache ref-count simplification so parse cache entries start with refCount 1 and prevent premature deletion.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4101015139) **andrewbranch** clarified UpdateProgram’s file acquisition and cloning behavior and explained the missing deref caused a memory leak, exemplifying why building programs without reffing then reffing at the end is easier
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4101228488) **gabritto** explained the UpdateProgram file acquisition logic and acknowledged that there was no ideal solution
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4101468121) **andrewbranch** expressed frustration and suggested reverting to snapshot ref counts while noting that some complications would remain
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4120165292) **andrewbranch** proposed restoring ref counts on snapshots with automatic releasing by callbacks and asked whether to include it in the current PR or address it in a follow-up
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4120197934) **jakebailey** said "However you want to do it; I think if there's a final state you want it'd be good to jump to straight to it in case there's a delay? But maybe this PR is fine on its own. Up to you."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4121907291) **andrewbranch** said "I can't get the flaky test to fail on my machine 😕 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4121947181) **jakebailey** said "I've been trying to get get a failing run of TestDuplicatePackageServices_fileChanges for what feels like months now, it's almost certainly nothing related to this PR."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4121984148) **andrewbranch** said "Oh, geez, I didn't know that and this PR did touch duplicate file stuff, so I thought it was my fault."

### [PR microsoft/TypeScript-go#3184](https://github.com/microsoft/TypeScript-go/pull/3184) (Closed)

**Use NodeIsMissing in typeeraser\.go where Strada did**

*Implement NodeIsMissing error handling in typeeraser.go to match Strada's implementation.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3185](https://github.com/microsoft/TypeScript-go/pull/3185) (Closed)

**Ensure tsconfig is passed to dts emit compile tests**

*Pass the TypeScript configuration to dts emit compile tests to prevent detached errors.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3186](https://github.com/microsoft/TypeScript-go/pull/3186) (Closed)

**Accept changes solely due to \_jsxFileName**

*Inconsistent absolute paths in _jsxFileName cause spurious test diffs that should be accepted as non-functional changes.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3186#issuecomment-4120730150) **DanielRosenwasser** said "Do the devtools that actually use this information still function correctly?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3186#issuecomment-4120739749) **jakebailey** said "I don't know, but I'll note that I checked other transformers like babel and they all emit absolute paths too."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3186#issuecomment-4120744824) **jakebailey** said "Er, well, I think babel just uses the filename it's given, so, that depends."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3188](https://github.com/microsoft/TypeScript-go/pull/3188) (Closed)

**Fix identifier unicode escaping for parameter props**

*Properly parent cloned identifier nodes for parameter properties to fix unicode escaping*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3190](https://github.com/microsoft/TypeScript-go/pull/3190) (Closed)

**Use iter\.Seq for GetSpellingSuggestion**

*Optimize GetSpellingSuggestion by using iterator-based sequence traversal to avoid sorting large symbol tables and improve performance.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3191](https://github.com/microsoft/TypeScript-go/pull/3191) (Closed)

**Reuse fileloader task data when atomic store fails**

*Reuse file loader task data via a global pool after atomic store failures to reduce memory allocations by about 80%.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3192](https://github.com/microsoft/TypeScript-go/issues/3192) (Closed, **weswigham**, **jakebailey**, **Copilot**)

**0320 vs 0321**

*The workglow build fails when using tsgo 7.0.0-dev.20260321.1 but succeeds with the previous day's 20260320.1 version.*

 * **jakebailey** assigned to **jakebailey**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4106574091) **jakebailey** asked which behavior was correct regarding the referenced issues
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4106654378) **Andarist** confirmed the issue was real and referenced Anders’ PR and a follow-up test-only PR
 * [today](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4120953583) **jakebailey** expressed that they did not know how to fix the incompatibility introduced by the PR, stating that 'as const' behavior was fundamentally incompatible with the ID-style emit
 * **jakebailey** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4121065100) **weswigham** explained that extending const type parameters to `as const satisfies` broke isolated-declarations inference because `as const` implies a fully const tree, noted that strada’s typeFromArrayLiteral never wraps tuples in `readonly`, and mentioned a drive-by fix in corsa
 * [today](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4121941514) **Andarist** noted an extra note from old design meeting notes and mentioned that although `satisfies` composes better, it’s not ID-friendly

### [Issue microsoft/TypeScript-go#3193](https://github.com/microsoft/TypeScript-go/issues/3193) (Closed)

**isolatedDeclarations does not flag potential type predicate funcs**

*Functions resembling type predicates, such as isString returning boolean, are not flagged as errors when isolatedDeclarations and declaration are enabled.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3194](https://github.com/microsoft/TypeScript-go/pull/3194) (Closed)

**Report inferred type predicate inference fallback**

*Enable error reporting for inferred type predicates while reusing AST nodes from explicitly annotated predicates*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3196](https://github.com/microsoft/TypeScript-go/pull/3196) (Open, **gabritto**)

**Fixes a crash when renaming import path of a JSON file**

*Renaming a JSON file’s import path causes the compiler to crash in TypeScript-Go and Strada.*

 * created by **Andarist**
 * **gabritto** assigned to **gabritto**

### [PR microsoft/TypeScript-go#3197](https://github.com/microsoft/TypeScript-go/pull/3197) (Closed)

**Fixed a go\-to\-implementations crash related to reexported type\-only namespace**

*Fixes go-to-implementations crash when navigating reexported type-only namespaces.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3201](https://github.com/microsoft/TypeScript-go/pull/3201) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 2 directories with 3 updates**

*Update three GitHub Actions dependencies across the root and setup-go directories, bumping codecov-action to v5.5.3, github/codeql-action, and actions/cache.*

 * (yesterday) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3204](https://github.com/microsoft/TypeScript-go/issues/3204) (Closed, `Crash`, **DanielRosenwasser**, **jakebailey**, **Copilot**)

**Panic with \`declarationMap\` in version 7\.0\.0\-dev\.20260323\.1**

*typescript-go 7.0.0-dev.20260323.1 panics with a slice bounds out of range error in scanner.SkipTriviaEx while generating declarationMap*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4114621338) **DanielRosenwasser** noted that @jakebailey had a separate branch with declaration emit fixes and provided a TypeScript repro demonstrating the slice bounds out-of-range crash
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4114866426) **faradaytrs** said "The same error for me since version 0320"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4115293270) **RohinBhargava** provided another repro link for tsgo-repro-3202
 * [today](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4120631561) **DanielRosenwasser** said "You can temporarily turn declarationMap off if you want to unblock yourself until we have a fix."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4120992116) **RohinBhargava** said "Yeah, unfortunately I need it on right now, but downgrading is fine for me right now!"

### [PR microsoft/TypeScript-go#3205](https://github.com/microsoft/TypeScript-go/pull/3205) (Closed)

**Don’t try to create invalid type/symbol merges**

*Prevent invalid merges between type and value symbols by updating the merging logic and diff handling.*

 * created by **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3205#issuecomment-4127758976) **jakebailey** tried applying the proposed merge code approach but found it unhelpful and shared a diff illustrating the changes

### [PR microsoft/TypeScript-go#3206](https://github.com/microsoft/TypeScript-go/pull/3206) (Closed)

**Report "File not found" for missing tripleslash path references**

*Report 'File not found' errors when triple-slash directive path references are missing.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3206#issuecomment-4119939224) **jakebailey** said "Is this just #3126? (Perhaps this PR is better, I have not yet looked)"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3206#issuecomment-4119973682) **jakebailey** said "On face, does seem like it covers more stuff, yeah. You can probably say "Fixes #2081"."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3206#issuecomment-4120023176) **Andarist** asked whether the PR duplicated microsoft/typescript-go#3126 and mentioned having started work over a week ago without reviewing existing PRs/issues
 * [today](https://github.com/microsoft/TypeScript-go/pull/3206#issuecomment-4122135853) **jakebailey** provided an unsolicited patch adding isSupportedExtension method and refactoring extension checks in fileloader.go

### [Issue microsoft/TypeScript-go#3207](https://github.com/microsoft/TypeScript-go/issues/3207) (Closed, **weswigham**)

**\`isolatedDeclarations\` false positive TS9013 on arrow functions with default parameters and \`as const\` objects**

*Enabling isolatedDeclarations in tsgo triggers false-positive TS9013 errors on arrow functions with default parameters and as const objects.*

 * created by **jakeboone02**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3207#issuecomment-4120895556) **hkleungai** mentioned that tsgo behaved unexpectedly with `as const` and nested object/array literals under the isolatedDeclarations flag and referenced a related issue
 * **jakebailey** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3207#issuecomment-4122814850) **jakebailey** said "The first is is an easy fix. I have not looked at the latter."

### [PR microsoft/TypeScript-go#3208](https://github.com/microsoft/TypeScript-go/pull/3208) (Closed)

**\[API\] Formatting bug fixes**

*Add PrintNodeOptions support to API and Go printer with emitter.withOptions, fix emitLiteral handling for terminateUnterminatedLiterals, and add related tests.*

 * created by **navya9singh**

### [PR microsoft/TypeScript-go#3209](https://github.com/microsoft/TypeScript-go/pull/3209) (Closed)

**\[API\] Session bug fix**

*resolveNodeHandle now walks up parent AST nodes when innermost matches fail, ensuring correct node resolution and type annotations.*

 * created by **navya9singh**
 * (today) **navya9singh** closed the issue

### [PR microsoft/TypeScript-go#3210](https://github.com/microsoft/TypeScript-go/pull/3210) (Closed)

**Disable nil\-context type\-node reuse**

*Prevent type-node reuse when context is nil to avoid inconsistent type information.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3211](https://github.com/microsoft/TypeScript-go/pull/3211) (Open)

**Fix typo in README definitions section**

*Correct the typo in the definitions section of the README.*

 * created by **colin99d**

### [PR microsoft/TypeScript-go#3212](https://github.com/microsoft/TypeScript-go/pull/3212) (Open)

**Fix error spans for \`@satisfies\`**

*Fix error span calculation for @satisfies to ensure accurate error highlighting.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3213](https://github.com/microsoft/TypeScript-go/pull/3213) (Closed)

**Remove nondeterminism in container generation**

*Eliminate nondeterministic global symbol traversal by implementing stable sorting to ensure consistent container generation and measurable performance.*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3213#issuecomment-4120769274) **jakebailey** suggested caching the deferred-sorted globals list with sync.Once and questioned if the current PR is the best solution
 * [today](https://github.com/microsoft/TypeScript-go/pull/3213#issuecomment-4120835880) **weswigham** described the need for special-casing globals for on-demand sorting, suggested using insertion-order symbol tables consistently, and explained difficulties with preserving symbol reverse mappings due to nuanced parent-child contexts
 * [today](https://github.com/microsoft/TypeScript-go/pull/3213#issuecomment-4121061795) **ahejlsberg** explained that using insertion-order sorted symbol tables was too costly due to performance and memory overhead
 * [today](https://github.com/microsoft/TypeScript-go/pull/3213#issuecomment-4121088253) **ahejlsberg** asked how often the bottom part of getWithAlternativeContainers executes and expressed concern about its performance cost
 * [today](https://github.com/microsoft/TypeScript-go/pull/3213#issuecomment-4121177006) **weswigham** explained that declaration emit historically made cached type comparisons free, noted a potential alternative for current emit model, and reported that removing the style container lookup would affect 61 test baselines

### [PR microsoft/TypeScript-go#3214](https://github.com/microsoft/TypeScript-go/pull/3214) (Closed)

**Disable nil\-context type\-node reuse in \`serializeReturnTypeForSignature\`**

*Disable reuse of nil-context type-node instances in serializeReturnTypeForSignature to ensure correct type serialization.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3215](https://github.com/microsoft/TypeScript-go/pull/3215) (Closed)

**Commit buffered iteration diagnostics when iterable recovery succeeds**

*Ensure buffered iteration diagnostics are committed when iterable recovery succeeds.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3216](https://github.com/microsoft/TypeScript-go/pull/3216) (Open)

**fix: clean up failed pprof startup files**

*Use a start hook to remove partially created CPU profile files on BeginProfiling failures, adding a unit test for cleanup.*

 * created by **buley**

### [PR microsoft/TypeScript-go#3217](https://github.com/microsoft/TypeScript-go/pull/3217) (Open)

**Watch cli efficiency update**

*Watch CLI efficiency improvements implement debouncing, configuration caching, and dependency parsing to avoid unnecessary recompilations.*

 * created by **johnfav03**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4127784005) **andrewbranch** highlighted missing include wildcard handling and proposed decoupling watcher logic from build logic for LSP integration

### [PR microsoft/TypeScript-go#3218](https://github.com/microsoft/TypeScript-go/pull/3218) (Closed)

**Port PR 61392 \- Fix serialization of accessor types in declaration files**

*Port PR 61392 to address incorrect serialization of accessor types in TypeScript declaration files.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3219](https://github.com/microsoft/TypeScript-go/pull/3219) (Closed)

**Use isOptionalParameter from checker to check param optional\-ness**

*Use isOptionalParameter from the checker to accurately detect parameter optionality instead of relying solely on isOptionalDeclaration’s question-node check.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3220](https://github.com/microsoft/TypeScript-go/pull/3220) (Open)

**Preserve error elaboration for indexed access type assignments**

*Improve TypeScript diagnostic messages by preserving specific error details for assignments to indexed access types.*

 * created by **WhiteMinds**

### [PR microsoft/TypeScript-go#3221](https://github.com/microsoft/TypeScript-go/pull/3221) (Closed)

**Fix ProbablyUsesSemicolons threshold comparison \(integer division\)**

*Replace the flawed integer division threshold in ProbablyUsesSemicolons with a multiplication-based inequality to fix zero-valued comparisons.*

 * created by **cuiweixie**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3221#issuecomment-4126082963) **cuiweixie** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#3222](https://github.com/microsoft/TypeScript-go/pull/3222) (Closed)

**Fix getPossibleTypeArgumentsInfo balance for \>\> and \>\>\>**

*Fix getPossibleTypeArgumentsInfo to increment balance by 2 and 3 for >> and >>> instead of resetting it.*

 * created by **cuiweixie**

### [PR microsoft/TypeScript-go#3223](https://github.com/microsoft/TypeScript-go/pull/3223) (Closed)

**Fix signature help label for multiple type parameters**

*Format multiple generic type parameters in signature help with commas and spaces between names.*

 * created by **cuiweixie**

### [PR microsoft/TypeScript-go#3224](https://github.com/microsoft/TypeScript-go/pull/3224) (Closed)

**Don't run release\-build job in merge queue checks**

*Exclude the release-build job from merge queue checks to prevent it from blocking the merge queue.*

 * created by **jakebailey**
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#787](https://github.com/microsoft/TypeScript-go/issues/787) (Closed)

**\`UnionToTuple\` type returns "inverted" tuple in TSGO compared to TypeScript 5\.8\.3 and gives type error**

*TSGO's UnionToTuple type generates tuples in reverse order compared to TypeScript 5.8.3, causing type errors*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3872828964) **alexwork1611** thanked for the information about the --stableTypeOrdering flag
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3879428487) **RyanCavanaugh** clarified that UnionToTuple<'a'|'b'> currently yields consistent results but this behavior is unspecified and may change
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3912876412) **alexwork1611** appreciated the clarification from Ryan
 * [today](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-4119913898) **alexwork1611** asked how the issue contributed to the creation of the --stableTypeOrdering flag
 * [today](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-4119936148) **jakebailey** said "I don't understand the question; I was just pointing out that you could test this more easily with that flag (the code for this had been backported for a while, just not shipped)."
 * [later](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-4125698998) **alexwork1611** said "Another way to ask would be, would you say this specific issue helped inform the design or the priority of the new --stableTypeOrdering flag in TS 6.0?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-4127370402) **RyanCavanaugh** explained that the design and implementation of STO predates the issue and TS7 and that this issue was one of many confirming the need for STO since TS6

