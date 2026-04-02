# Report for 2026-01-12 (Monday, January 12th, 2026)

17 different users commented on 22 different issues.

## Recommended Actions

 * Response Recommended
    * @OldStarchy provided reproduction steps and code for diagnosing type conflicts in [microsoft/TypeScript#16132](https://github.com/microsoft/TypeScript/issues/16132#issuecomment-3743922773)
    * @cleversonferreira asked about when the PR would be published in [microsoft/TypeScript#62887](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3739775406)
    * @wparad asked for reference docs explaining the configuration in [microsoft/TypeScript#62975](https://github.com/microsoft/TypeScript/issues/62975#issuecomment-3740376562)
    * @heathdutton asked for confirmation before making changes in [microsoft/TypeScript#62979](https://github.com/microsoft/TypeScript/pull/62979#issuecomment-3745118718)

## Activity Summary

### [Issue microsoft/TypeScript#16132](https://github.com/microsoft/TypeScript/issues/16132) (Closed, `Discussion`)

**es5\.d\.ts lib does not match the ECMAScript 5\.1 Spec**

*The es5.d.ts lib file incorrectly includes non-ES5.1 types such as Promise, ArrayBuffer, and decorators.*

 * [4 years ago](https://github.com/microsoft/TypeScript/issues/16132#issuecomment-995247582) **RyanCavanaugh** stated that concerns were based on technical purity but that ES3 runtimes were outdated, and declared no action planned
 * (4 years ago) **RyanCavanaugh** closed the issue
 * [4 years ago](https://github.com/microsoft/TypeScript/issues/16132#issuecomment-995251606) **ericdrobinson** disagreed that the concerns were solely based on technical purity, argued against consolidating everything into a core ES library, acknowledged ES3 runtimes were nearly obsolete, and agreed with leaving things as-is
 * [later](https://github.com/microsoft/TypeScript/issues/16132#issuecomment-3743922773) **OldStarchy** described declaring a custom ClassDecorator in types.d.ts to match new decorator types and noted a conflict with legacy decorator types from es5 via esnext causing type errors

### [Issue microsoft/TypeScript#27273](https://github.com/microsoft/TypeScript/issues/27273) (Open, `Suggestion`, `In Discussion`)

**Object spread drops index signature**

*TypeScript object spreads lose index signatures when merging Record<string,string> with other properties.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/27273#issuecomment-1814952500) **bmillwood** clarified that the example illustrated a type unsoundness rather than inconvenience, since the record type falsely claims only strings but contains a number
 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/27273#issuecomment-1814962470) **fatcerberus** said "@bmillwood I was talking specifically about the example in the OP (the original bug report).  Your example is covered by #56431, and I agree it is incorrect."
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/27273#issuecomment-2221153341) **vincerubinetti** questioned the inconsistency between Object.assign and spread regarding typing behavior
 * [later](https://github.com/microsoft/TypeScript/issues/27273#issuecomment-3743368168) **som-sm** demonstrated that Object.assign also produces incorrect merged types and introduced an ObjectMerge utility type in type-fest to handle various edge cases correctly

### [Issue microsoft/TypeScript#36060](https://github.com/microsoft/TypeScript/issues/36060) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow \.d\.ts files to represent anonymous class expressions with \`private\` members**

*Enable .d.ts declaration files to represent anonymous class expressions with private members.*

 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/36060#issuecomment-1229422816) **RonnieLincoln** asked if there was any process and mentioned encountering the issue when using the Builder Pattern
 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/36060#issuecomment-2132038130) **MichaelMitchell-at** suggested a syntax for anonymous class types to annotate computed properties under isolatedDeclarations to reduce verbosity
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/36060#issuecomment-3398475344) **trusktr** described a TypeScript mixin example in which private fields on exported anonymous classes caused a type error, noted that private hashtag syntax suppressed the type error but leads to runtime errors
 * [later](https://github.com/microsoft/TypeScript/issues/36060#issuecomment-3744808515) **valler** explained that private and protected members break with dynamically created classes, showed how One and Two must share the same mixin result for protected members to work, and suggested a cleaner class-based pattern with code examples

### [Issue microsoft/TypeScript#62887](https://github.com/microsoft/TypeScript/issues/62887) (Closed, `Needs Investigation`, **sheetalkamat**)

**TS Server Crash Loop: Copilot Chat virtual files \('vscode\-chat\-code\-block'\) trigger infinite Directory Watcher recursion on InferredProject**

*Copilot Chat’s virtual “vscode-chat-code-block” files cause the TypeScript server to enter infinite directory watcher recursion, spike CPU, and crash repeatedly.*

 * (1 month ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **sheetalkamat**
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3649495289) **code-forge-temple** identified the bug's introduction around mid-May 2025 and recommended reviewing changes from that period; criticized Microsoft for ignoring critical bugs and expressed intent to cancel Copilot subscription due to corporate priorities
 * [today](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3739775406) **cleversonferreira** asked about when the PR with the bug fix would be published

### [Issue microsoft/TypeScript#62948](https://github.com/microsoft/TypeScript/issues/62948) (Closed, `Needs Investigation`, **joj**)

**TypeScript MSBuild Target named GetTypeScriptOutputForPublishing should not include the removed Content files**

*The GetTypeScriptOutputForPublishing MSBuild target ignores Content Remove directives and re-includes generated .js and .d.ts files in the package.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3721396672) **joj** noted that the TypeScript NuGet package runs tsc directly and suggested adding an MSBuild target before CoreCompile, then asked if the user needs JavaScript files and is deploying them
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3721793580) **marqdouj** clarified that they only needed the JavaScript for WebPack bundling and did not want to distribute the TypeScript output, and asked if the other participant had reviewed the previously posted source code link to understand their intentions
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3723673201) **marqdouj** outlined a process to use TypeScript, WebPack, and MSBuild targets to build, bundle, and exclude tsgen files before packaging
 * [today](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3741818215) **marqdouj** stated that their configuration worked and that they would close the issue, and thanked @joj
 * (today) **marqdouj** closed the issue

### [Issue microsoft/TypeScript#62960](https://github.com/microsoft/TypeScript/issues/62960) (Open, `Needs More Info`)

**Initializing tsconfig\.json hangs**

*VS Code hangs indefinitely initializing tsconfig.json for Vue projects on network shares, disabling IntelliSense and error reporting.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62960#issuecomment-3720609065) **uli-a** said "Yes, it does. Not if .vue files are opened, but for .ts files the same issue occurs."
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62960#issuecomment-3720726879) **RyanCavanaugh** noted that without knowing network and OS performance it's hard to determine if this is a defect, explained that watches are required for editor functionality, and suggested configuring watch differently with a link to the docs
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62960#issuecomment-3720924568) **uli-a** tried changing the watch configuration but observed no improvement; described the network and hardware environment and ruled out performance issues; asked how to determine what tsserver is doing or waiting for
 * [today](https://github.com/microsoft/TypeScript/issues/62960#issuecomment-3740668755) **RyanCavanaugh** noted that there is no way to inspect what tsserver is doing or waiting for without attaching a debugger
 * **RyanCavanaugh** added label `Needs More Info`

### [Issue microsoft/TypeScript#62962](https://github.com/microsoft/TypeScript/issues/62962) (Closed, `Duplicate`)

**Monorepo support**

*Allow TypeScript compiler to recognize monorepo package boundaries and skip type checking of node_modules during noEmit builds*

 * (3 days ago) **RyanCavanaugh** added label `Duplicate`, and removed label `Needs Proposal`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3732365532) **valler** acknowledged the similarity to an existing issue, thanked the pointer, and explained that they already knew about tsc -b behavior and suggested an enum for composite might suffice for some setups
 * [today](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3741374150) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#62969](https://github.com/microsoft/TypeScript/pull/62969) (Closed, `For Uncommitted Bug`)

**Remove unnecessary type assertions**

*Remove unnecessary type assertions found during testing of the @typescript-eslint/no-unnecessary-type-assertion lint rule without affecting runtime or TS errors.*

 * (3 days ago) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62969#issuecomment-3736259974) **jakebailey** expressed doubt that the changes would be merged because the TypeScript codebase is due to be overwritten soon
 * [today](https://github.com/microsoft/TypeScript/pull/62969#issuecomment-3740735228) **ulrichstark** thanked for feedback and offered to close the PR, noting it was a proof of concept for lint changes

### [PR microsoft/TypeScript#62973](https://github.com/microsoft/TypeScript/pull/62973) (Open, `For Uncommitted Bug`)

**Add explicit type variance specifiers to Promise, Map, Set**

*Add explicit type variance specifiers to Promise, Map, and Set to potentially improve type checking performance.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3733279171) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #62954. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3733280151) **akaltar** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3740703134) **jakebailey** expressed doubt about feasibility and asked the typescript-bot to run tests
 * [today](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3740703575) **typescript-bot** posted automated build status update for CI jobs
 * [today](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3740747918) **ritschwumm** explained that mutable collections cannot define covariant value types and illustrated the variance conflict using Map’s get and set methods
 * [today](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3740789609) **typescript-bot** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3740810752) **typescript-bot** reported user test results comparing main and merge, noted infrastructure failures and new type errors, and asked to have a look
 * [today](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3740901124) **typescript-bot** posted the performance run results comparing baseline to PR for tsc
 * [today](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3740953606) **typescript-bot** reported comparative build results for the top 400 repos between main and the PR, noted a build error in microsoft/playwright, and requested a review

### [Issue microsoft/TypeScript#62974](https://github.com/microsoft/TypeScript/issues/62974) (Open, `Bug`, `Help Wanted`, `Domain: Crashes`)

**Crash: TypeError: Cannot read properties of undefined \(reading 'flags'\) in isFreshLiteralType during recursive tuple expansion with unresolved identifiers**

*TypeScript compiler crashes with a TypeError reading 'flags' in isFreshLiteralType during recursive tuple expansion with unresolved identifiers*

 * created by **na7ure-a**
 * [today](https://github.com/microsoft/TypeScript/issues/62974#issuecomment-3738033715) **Andarist** reproduced the issue with a TypeScript variadic tuple code example
 * **RyanCavanaugh** added label `Bug`
 * [today](https://github.com/microsoft/TypeScript/issues/62974#issuecomment-3740665614) **RyanCavanaugh** said "Repros in TS7 as well"
 * (today) **RyanCavanaugh** added label `Help Wanted`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#62975](https://github.com/microsoft/TypeScript/issues/62975) (Closed, `Working as Intended`)

**SkipLibCheck isn't working on erasableSyntaxCheck**

*SkipLibCheck fails to suppress errors in external index.d.ts files defining enums and namespaces under erasableSyntaxCheck*

 * created by **wparad**
 * [today](https://github.com/microsoft/TypeScript/issues/62975#issuecomment-3740275212) **RyanCavanaugh** said "https://github.com/Microsoft/TypeScript/wiki/FAQ#the-lib-in-skiplibcheck-refers-to-dts-files"
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/62975#issuecomment-3740288675) **RyanCavanaugh** noted that the errors originated from `.ts` files
 * [today](https://github.com/microsoft/TypeScript/issues/62975#issuecomment-3740308284) **wparad** said "Correct, but those files are only referenced by index.d.ts, which means we are back to the same issue."
 * [today](https://github.com/microsoft/TypeScript/issues/62975#issuecomment-3740368499) **RyanCavanaugh** said "Lib-ness is not transitive; the check is based only on filename. This package is misconfigured."
 * [today](https://github.com/microsoft/TypeScript/issues/62975#issuecomment-3740376562) **wparad** said "Can you point us to some reference docs that explain what the configuration is supposed to be?"
 * [today](https://github.com/microsoft/TypeScript/issues/62975#issuecomment-3741298292) **RyanCavanaugh** noted that PR #67 contains the correct fix and referenced documentation on publishing declaration files to npm

### [Issue microsoft/TypeScript#62977](https://github.com/microsoft/TypeScript/issues/62977) (Closed, `Suggestion`, `Out of Scope`)

**\`disallowClassExpressions\`**

*Add a TypeScript compiler option to disallow class expressions for stricter type checking and error prevention.*

 * [today](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3739224279) **valler** argued that the rule belonged in tsc rather than a linter to avoid duplication and because compiler options align with compiler issues
 * [today](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3739277604) **MartinJohns** explained that the options existed in tsc due to legacy reasons before linter support was adequate
 * [today](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3739287291) **valler** clarified that the discussion pertained to language types rather than style and distinguished between a class and a class expression
 * [today](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3739328334) **MartinJohns** disagreed that TypeScript limitations justify syntax restrictions and pointed to ESLint's no-restricted-syntax rule
 * [today](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3739357538) **valler** argued that linters and compilers inherently provide type safety features, stated type-safe JS without TS syntax would differ greatly, and noted recommended patterns often reflect feasibility rather than JS structural ideals
 * [today](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3739365015) **valler** argued that TypeScript is a language guided by JavaScript rather than a compiler, that tsc remains the baseline despite tooling, and that classes in closures should be disallowed similarly to indexing static interfaces
 * [today](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3740270237) **RyanCavanaugh** criticized that the compiler option would not improve the situation
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Out of Scope`
 * [today](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3740274634) **valler** thanked the reviewer and noted that although the compiler option won’t solve all issues, the language still improved user experience and may help avoid design limitations
 * [today](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3740450411) **valler** observed that the option, being scoped to expressions, wouldn't affect declarations in closures and thus was less useful than initially expected

### [PR microsoft/TypeScript#62978](https://github.com/microsoft/TypeScript/pull/62978) (Open, `For Backlog Bug`)

**Fix \#25083: Allow bracket notation for enum keys in computed properties**

*Enable bracket notation for enum keys in computed properties by modifying AST checks to accept ElementAccessExpression on enum names.*

 * created by **RodrigoSanchezDev**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62978#issuecomment-3740277239) **microsoft-github-policy-service[bot]** asked the contributor to agree to the CLA by replying with the agree command and optionally specifying a company

### [PR microsoft/TypeScript#62979](https://github.com/microsoft/TypeScript/pull/62979) (Open, `For Backlog Bug`)

**Fix duplicate JSDoc @typedef and @callback comments in declaration emit**

*Declaration emit now skips raw JSDoc @typedef and @callback comments to prevent duplicate type declarations.*

 * created by **heathdutton**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62979#issuecomment-3745118718) **heathdutton** said "Both suggestions would deviate from existing codebase conventions, but happy to make a change if a human replies."

### [Issue microsoft/TypeScript#62980](https://github.com/microsoft/TypeScript/issues/62980) (Closed, `Bug`, `Breaking Change`, `Fix Available`)

**Deprecate, remove \`\-\-outFile\`**

*Deprecate and prepare removal of the `--outFile` compiler option in TypeScript 6.0 ahead of version 7.0.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Bug`, `Breaking Change`, and set milestone to `TypeScript 6.0.0`
 * **typescript-bot** added label `Fix Available`
 * **DanielRosenwasser** removed label `Fix Available`
 * **typescript-bot** added label `Fix Available`

### [PR microsoft/TypeScript#62981](https://github.com/microsoft/TypeScript/pull/62981) (Closed, `Author: Team`, `For Milestone Bug`, **RyanCavanaugh**)

**Deprecate \`\-\-outFile\`**

*Deprecate the --outFile compiler option as part of the fix for issue #62980.*

 * created by **RyanCavanaugh**
 * (today) **typescript-bot** added labels `Author: Team`, `For Milestone Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/62981#issuecomment-3741283804) **jakebailey** requested the typescript-bot to run tests
 * [today](https://github.com/microsoft/TypeScript/pull/62981#issuecomment-3741283947) **typescript-bot** reported build start and completion statuses for the 'user test this' and 'test top800' commands
 * [today](https://github.com/microsoft/TypeScript/pull/62981#issuecomment-3741343885) **typescript-bot** reported user test comparisons between main and the merge pull request, noted infrastructure failures, and affirmed everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/62981#issuecomment-3741688191) **typescript-bot** reported that running tsc on the top 800 repos comparing main and the PR merge produced no issues

### [PR microsoft/TypeScript#62982](https://github.com/microsoft/TypeScript/pull/62982) (Open, `For Uncommitted Bug`)

**fix\(lib\): allow 'default' in Intl\.CollatorOptions\.collation**

*Add 'default' as a valid collation option in Intl.CollatorOptions to match runtime behavior.*

 * created by **adityavyas01**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62982#issuecomment-3743884854) **adityavyas01** agreed with microsoft-github-policy-service

