# Report for 2025-12-12 (Friday, December 12th, 2025)

10 different users commented on 19 different issues.

## Recommended Actions

 * Moderation
    * @a-non-a-mouse posted rude content in [microsoft/TypeScript#62849](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3647355034)
 * Response Recommended
    * @AryanBagade reported that they submitted a fix for the issue in [microsoft/TypeScript#62870](https://github.com/microsoft/TypeScript/issues/62870#issuecomment-3649152851)
    * @valler asked why TS Server ignores 'files', 'include', and 'types' settings when picking up configurations in [microsoft/TypeScript#62886](https://github.com/microsoft/TypeScript/issues/62886#issuecomment-3648941857)
    * @code-forge-temple reported the bug origin and requested reviewing the mid-May 2025 changes in [microsoft/TypeScript#62887](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3649495289)
    * @ghosuser706 asked where to propose changes to the TypeScript design goals in [microsoft/TypeScript#62893](https://github.com/microsoft/TypeScript/issues/62893#issuecomment-3648705526)

## Activity Summary

### [PR microsoft/TypeScript#54935](https://github.com/microsoft/TypeScript/pull/54935) (Open, `For Milestone Bug`, **weswigham**)

**Extend \`addPropertyToElementList\` to differentiate get/set accessors from properties**

*Enable addPropertyToElementList to distinguish and emit get/set accessors rather than regular properties.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/pull/54935#issuecomment-1659678381) **kring** said "@sandersn just a bump on this because it's in the "Waiting on Author" state, but I don't think it's actually waiting on anything from me anymore. Sorry for the noise if I just need to be more patient!"
 * [2.3 years ago](https://github.com/microsoft/TypeScript/pull/54935#issuecomment-1663109722) **sandersn** said "Woops, I misread the comment history. I moved it back to Waiting on Reviewers."
 * [1.8 years ago](https://github.com/microsoft/TypeScript/pull/54935#issuecomment-1902582699) **athewsey** said "@sandersn / @weswigham any update on this? Seems like it's been waiting for review for a while and I just ran in to the same issue it's trying to solve. Thanks for your help!"
 * [today](https://github.com/microsoft/TypeScript/pull/54935#issuecomment-3648320931) **RyanCavanaugh** criticized modifying all object type emit instead of targeting class types and warned that replacing readonly with getters could confuse users and break duplicate property equivalence logic

### [Issue microsoft/TypeScript#55091](https://github.com/microsoft/TypeScript/issues/55091) (Open, `Bug`, `Help Wanted`, `Fix Available`, `Domain: enum`)

**Enum value \`1 / 0\` incorrectly transformed if there is \`Infinity\` declared in scope**

*A local Infinity variable shadows the global Infinity constant, so enum member initialized with 1/0 incorrectly uses the local value.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/55091#issuecomment-2399926341) **ravin00** explained that redefining the global Infinity as 3 caused unexpected behavior and advised removing that redefinition to restore the expected Infinity in enum
 * **RyanCavanaugh** added label `Domain: enum`
 * (today) **RyanCavanaugh** set milestone to `Dormant`, and removed from milestone `Backlog`
 * **typescript-bot** added label `Fix Available`

### [PR microsoft/TypeScript#55107](https://github.com/microsoft/TypeScript/pull/55107) (Open, `For Milestone Bug`, **rbuckton**)

**Don't emit enum members as evaluated \`Infinity\`/\`NaN\` when their symbols are shadowed**

*Prevent enum members from being emitted as Infinity or NaN when their symbols are shadowed.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/pull/55107#issuecomment-1646657354) **fatcerberus** said "Just for completeness’ sake, how does this interact with const enum?"
 * [2.3 years ago](https://github.com/microsoft/TypeScript/pull/55107#issuecomment-1646680080) **Andarist** asked how this interacted with const enum and noted that TS still inlines Infinity and NaN despite errors, concluding it’s acceptable to ignore the bug for invalid input emits
 * **sandersn** assigned to **rbuckton**
 * (today) **typescript-bot** added label `For Milestone Bug`, and removed label `For Backlog Bug`

### [PR microsoft/TypeScript#62730](https://github.com/microsoft/TypeScript/pull/62730) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**DOM update 2025\-12\-10**

*Update the DOM to include the latest changes made on December 10, 2025.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3639719897) **typescript-bot** posted the requested perf run results for tsc with detailed comparison metrics
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3639794378) **typescript-bot** reported build results for top 400 repos and highlighted new TS2345 errors in microsoft/vscode comparing main and the pull request
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3643825924) **jakebailey** said "Hm, I guess the generated Navigator is missing a few things"
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3648441269) **Renegade334** identified that the @types/dom-navigation package clashed with the new Navigation API

### [Issue microsoft/TypeScript#62809](https://github.com/microsoft/TypeScript/issues/62809) (Closed, `Help Wanted`)

**Typo in CopyrightNotice\.txt**

*CopyrightNotice.txt contains a typo with “MERCHANTABLITY” misspelled.*

 * created by **justanotheranonymoususer**
 * (1 week ago) **RyanCavanaugh** added label `Help Wanted`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/62809#issuecomment-3647379635) **RyanCavanaugh** said "Fixed in #62891"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62849](https://github.com/microsoft/TypeScript/issues/62849) (Closed, `Not a Defect`)

**The existence of /// reference directives in dependencies breaks explicit typeRoots ordering**

*Dependencies using triple-slash reference directives load their type definitions before custom typeRoots, ignoring explicit typeRoots ordering.*

 * (2 days ago) **RyanCavanaugh** added label `Not a Defect`, and removed label `Needs More Info`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3638906355) **a-non-a-mouse** argued that it was the same issue and advocated resolving typeRoots first to eliminate hard conflicts between globals while preserving mergeable definitions, noting that external globals should be constrained at package boundaries
 * [today](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3647355034) **a-non-a-mouse** said "MS engineers, again, too stupid to recognize an obvious bug  🤷‍♂️"
 * (today) **a-non-a-mouse** closed the issue

### [Issue microsoft/TypeScript#62870](https://github.com/microsoft/TypeScript/issues/62870) (Open, `Bug`, `Help Wanted`, `Domain: Decorators`)

**ES  \`ClassDecoratorContext\.name\` has incorrect value with static \`name\`**

*ClassDecoratorContext.name returns the static name property's value instead of the actual class name literal.*

 * (3 days ago) **RyanCavanaugh** added label `Domain: Decorators`, and set milestone to `Backlog`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62870#issuecomment-3641999947) **sAchin-680** asked to be assigned, offered to open a PR, and identified that the issue came from using renamedClassThis.name invoking the user-defined getter instead of the literal class name
 * [later](https://github.com/microsoft/TypeScript/issues/62870#issuecomment-3649152851) **AryanBagade** submitted a fix using the literal class name instead of accessing _classThis.name and added test cases covering static name getter, static name property, and normal class scenarios

### [Issue microsoft/TypeScript#62880](https://github.com/microsoft/TypeScript/issues/62880) (Open, `Needs Investigation`, **andrewbranch**)

**subpath imports should play well with project references**

*TypeScript project references misinterpret Node.js subpath imports like '#bob/module' as internal files, causing TS6307 build errors.*

 * created by **valler**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62880#issuecomment-3643147213) **valler** noted that removing `composite` in tsconfig.other.json removed the error but was unsure about build implications given docs recommendation
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#62882](https://github.com/microsoft/TypeScript/issues/62882) (Open, `Suggestion`, `Experience Enhancement`)

**Autocompletion does NOT remove \`type\` from \`import type\` when needed**

*VS Code autocompletion no longer removes the type keyword from import type statements when switching to value imports.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/62882#issuecomment-3642787238) **vs-code-engineering[bot]** thanked the user for creating the issue and suggested upgrading to the latest VS Code version to see if the issue persists
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/62882#issuecomment-3647569898) **RyanCavanaugh** said "I don't think this is a regression; AFAIK we've never had the feature to promote type-only import to value import on completion. But it'd be a nice change to do."
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Experience Enhancement`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#62883](https://github.com/microsoft/TypeScript/issues/62883) (Closed, `Duplicate`)

**Redesign \`\(const\) enum\` and \`namespace\` emit for better treeshaking**

*Propose redesigning TypeScript's enum and namespace code generation using pure IIFEs like esbuild for improved treeshaking.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/62883#issuecomment-3644205817) **MartinJohns** said "Duplicate of #27604."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62883#issuecomment-3644308777) **Septh** expressed surprise and thanked the finder, hoping to bring the seven-year-old duplicate issue back to maintainers' attention
 * [today](https://github.com/microsoft/TypeScript/issues/62883#issuecomment-3646947172) **MartinJohns** said "Related: https://github.com/microsoft/typescript/wiki/faq#time-marches-on"
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#62884](https://github.com/microsoft/TypeScript/issues/62884) (Closed, `Question`)

**ts\.parseJsonConfigFileContent double\-adds relative path, resulting in broken "include" pattern\.**

*ts.parseJsonConfigFileContent incorrectly prefixes include paths with the base directory twice, causing no files to be matched.*

 * created by **maxpatiiuk**
 * [today](https://github.com/microsoft/TypeScript/issues/62884#issuecomment-3647339115) **RyanCavanaugh** explained that `directoryPath` must be an absolute path for ts.parseJsonConfigFileContent, suggested using `path.resolve(directoryPath)` to fix the issue, and showed the expected output
 * **RyanCavanaugh** added label `Question`
 * [today](https://github.com/microsoft/TypeScript/issues/62884#issuecomment-3647399536) **maxpatiiuk** acknowledged the explanation and mentioned confusion about inconsistent relative paths in the TypeScript API
 * (today) **maxpatiiuk** closed the issue

### [Issue microsoft/TypeScript#62886](https://github.com/microsoft/TypeScript/issues/62886) (Closed, `Duplicate`)

**composite typescript project types should not leak into excluded files**

*Composite TypeScript projects' types settings in referenced tsconfigs are leaking into excluded files.*

 * created by **valler**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/62886#issuecomment-3647591319) **RyanCavanaugh** noted that the issue duplicated #33094 and suggested a way to specify alternative tsconfig files while ignoring tsconfig.json
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/62886#issuecomment-3648941857) **valler** explained that TS Server was leaking types across referenced projects due to tsconfig.json and package.json combination and noted that include/files/types settings seemed to be ignored

### [Issue microsoft/TypeScript#62887](https://github.com/microsoft/TypeScript/issues/62887) (Open, `Needs Investigation`, **sheetalkamat**)

**TS Server Crash Loop: Copilot Chat virtual files \('vscode\-chat\-code\-block'\) trigger infinite Directory Watcher recursion on InferredProject**

*Copilot Chat’s virtual “vscode-chat-code-block” files cause the TypeScript server to enter infinite directory watcher recursion, spike CPU, and crash repeatedly.*

 * (yesterday) **mjbvz** removed label `Bug`, and unassigned **justschen**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3644229903) **mjbvz** said "@sheetalkamat Can you please take a look at the virtual file watching to make sure it's handling the chat code block documents correctly "
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **sheetalkamat**
 * [later](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3649495289) **code-forge-temple** identified the bug's introduction around mid-May 2025 and recommended reviewing changes from that period; criticized Microsoft for ignoring critical bugs and expressed intent to cancel Copilot subscription due to corporate priorities

### [PR microsoft/TypeScript#62890](https://github.com/microsoft/TypeScript/pull/62890) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix accidental module replacements in tests**

*Remove unintended redundant module replacements in tests introduced during cherry-picking to the tsgo-port branch.*

 * (yesterday) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62891](https://github.com/microsoft/TypeScript/pull/62891) (Closed, `For Backlog Bug`)

**Fix typo: MERCHANTABLITY → MERCHANTABILITY**

*Corrects the typo 'MERCHANTABLITY' to 'MERCHANTABILITY' in copyright notices and related test files.*

 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62891#issuecomment-3645848623) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/62891#issuecomment-3645918958) **tt-a1i** said "@microsoft-github-policy-service agree"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62893](https://github.com/microsoft/TypeScript/issues/62893) (Closed, `Duplicate`)

**Support proper function overloading**

*Add clearer function overloading syntax to TypeScript to reduce boilerplate and improve readability.*

 * created by **ghosuser706**
 * [today](https://github.com/microsoft/TypeScript/issues/62893#issuecomment-3647418536) **RyanCavanaugh** said "Duplicate #3442"
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/62893#issuecomment-3648705526) **ghosuser706** noted they missed the earlier issue because they only searched open issues, highlighted arguments for supporting clean syntax, and asked where to propose changes to TypeScript design goals
 * [today](https://github.com/microsoft/TypeScript/issues/62893#issuecomment-3648715871) **MartinJohns** clarified that TypeScript still requires writing JavaScript with added type information
 * [today](https://github.com/microsoft/TypeScript/issues/62893#issuecomment-3649028100) **RyanCavanaugh** rejected a proposal to change the project's design goals and recommended using a different project for unmet requirements
 * [today](https://github.com/microsoft/TypeScript/issues/62893#issuecomment-3649089699) **ghosuser706** clarified that TypeScript syntax is based on JavaScript but can be used without JavaScript knowledge, argued that TypeScript is a superior version that could be supported directly by runtimes, and noted that conventional function overloading is feasible as shown by GWT

### [PR microsoft/TypeScript#62894](https://github.com/microsoft/TypeScript/pull/62894) (Open, `Author: Team`, `For Uncommitted Bug`, **sheetalkamat**)

**Handle resolution watching when its dynamic scriptInfo**

*Stop watching failed lookup paths, inferred typeRoots, and typing installer locations for dynamic scripts using unwatchable or default directories.*

 * created by **sheetalkamat**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **sheetalkamat**

### [PR microsoft/TypeScript#62895](https://github.com/microsoft/TypeScript/pull/62895) (Open, `For Backlog Bug`)

**Fix ClassDecoratorContext\.name to use literal class name \(\#62870\)**

*Emit the literal class name for decorator context name rather than accessing the static name property*

 * created by **AryanBagade**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62895#issuecomment-3649150576) **AryanBagade** said "@microsoft-github-policy-service agree"

