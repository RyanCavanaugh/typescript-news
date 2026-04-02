# Report for 2026-02-25 (Wednesday, February 25th, 2026)

14 different users commented on 25 different issues.

## Recommended Actions

 * Response Recommended
    * @johnnycheng0210 asked for feedback on a proposed approach requiring window reloads in [microsoft/TypeScript-go#2020](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3963841180)
    * @Jack-Works reported that the issue also occurs frequently in their public repository and provided the link in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3964094295)
    * @johnsoncodehk provided a PR and requested feedback on the proposed plugin approach in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3963097012)
    * @remcohaszing asked about the exact behavior of the Next.js TypeScript plugin in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3965169605)
    * @pedro757 provided repro sandbox as requested in [microsoft/TypeScript-go#2864](https://github.com/microsoft/TypeScript-go/pull/2864#issuecomment-3967358451)

## Activity Summary

### [PR microsoft/TypeScript-go#2020](https://github.com/microsoft/TypeScript-go/pull/2020) (Open)

**Support for custom configurations**

*Enable passing custom tsconfig file names to the tsgo LSP to support solution-style repository configurations.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3924764987) **johnnycheng0210** wondered if requiring a window reload between custom config file name changes would be preferred as a simpler approach
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3928562337) **jakebailey** said "I'm definitely confused, because when I write a test for this, the test seemingly does the right thing."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3955294783) **johnnycheng0210** asked whether the issue was related to the language server state on config file refresh rather than the new config file name update
 * [today](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3961143621) **jakebailey** said "I honestly have no idea ☹️ "
 * [today](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3963841180) **johnnycheng0210** asked jakebailey for feedback on requiring a window reload between custom config file name changes to avoid edge cases
 * [today](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3963848279) **jakebailey** rejected restarting the client and asked Andrew Branch for insight
 * [today](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3963951469) **andrewbranch** said "I'm not sure off the top of my head, I'd have to debug and step through."

### [PR microsoft/TypeScript-go#2595](https://github.com/microsoft/TypeScript-go/pull/2595) (Closed, **DanielRosenwasser**, **Copilot**)

**Add regression test for inlay hints crash on reparsed nodes**

*Add regression test for inlay hints crash on reparsed nodes in JavaScript CommonJS files*

 * created by **Copilot**
 * (1 month ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2595#issuecomment-3962518036) **DanielRosenwasser** said "@copilot+claude-sonnet-4.5 merge from main, get rid of the non-test code."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2595#issuecomment-3962580285) **Copilot** merged from main and removed non-test code, keeping only test-related commits
 * [today](https://github.com/microsoft/TypeScript-go/pull/2595#issuecomment-3962836453) **jakebailey** said "Copilot massively messed up that merge."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2595#issuecomment-3962986114) **DanielRosenwasser** said "@copilot+claude-sonnet-4.5 Reset hard on origin/main, git pull, git submodule update, re-add the test, force-push."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2595#issuecomment-3963043187) **Copilot** reported being unable to force-push due to automatic rebasing and requested manual force-push or permissions
 * [today](https://github.com/microsoft/TypeScript-go/pull/2595#issuecomment-3963043450) **DanielRosenwasser** insulted the change as broken and mocked its author
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2769](https://github.com/microsoft/TypeScript-go/issues/2769) (Closed)

**reference path 不能跳转**

*Ctrl-click navigation on reference paths in .d.ts files fails to jump to the referenced file.*

 * created by **myNinety**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2769#issuecomment-3963146964) **RyanCavanaugh** said "Appears to be a misclick? Please log a new issue with more information if not. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3942722362) **shinichy** mentioned inability to share code from private repo, noted that bucket.DependencyNames was nil and len(bucket.Paths) was 0, and offered to create a public repo to reproduce the issue
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3943840500) **justinsmid** reported experiencing excessive memory usage and provided cache stats and a heap profile, noting the project was private but accessible to Jake Bailey
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3945883495) **andrewbranch** noted that the profile showed 9.5 GB of usage, explained that a nil DependencyNames bucket leads to gathering auto-imports from the entire directory, and suggested debugging computeDependenciesForNodeModulesDirectory
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3964094295) **Jack-Works** mentioned that the issue also occurred frequently in their public repository and provided the link

### [Issue microsoft/TypeScript-go#2781](https://github.com/microsoft/TypeScript-go/issues/2781) (Open)

**resolving library types with import assignment \`import = require\(\)\` fails**

*Named and default type exports from @sendgrid/mail included via import assignment work in TypeScript 6.0 but tsgo reports missing members and default-only import errors.*

 * created by **ayZagen**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-3898945713) **jakebailey** questioned the trustworthiness of the code due to ts-ignore usage and mixing export syntax
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-3899349460) **ayZagen** speculated that previous contributors left the code unchanged after it worked and expressed a desire to contribute to tsgo due to encountering a unique error
 * **RyanCavanaugh** added label `wontfix`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-3963151561) **RyanCavanaugh** said "Yeah, this isn't any sort of maintainable invariant"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3936069400) **chriskrycho** explained that projects adopt TypeScript’s module resolution semantics and likened the necessary tooling transformations to TSX/JSX syntactic shenanigans
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3936221722) **aheber** described two main actions: dynamically modifying the resolved tsconfig to register module paths and lying about non-JS files as importable modules by intercepting read/write operations; explained desire to avoid on-disk declaration files and tsconfig edits while retaining refactoring support; asked if tsgo’s architecture can support intercepting file write actions for virtual modules
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3947458101) **andrewbranch** clarified that they meant injecting types via TypeScript syntax in virtual files that don’t exist on disk, rather than inserting types directly into type resolution via a JS object API
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3963097012) **johnsoncodehk** suggested a pull-based plugin mechanism for CLI and LSP to resolve non-standard files, outlined cross-language and mapping challenges, and mentioned a concrete PR
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3965169605) **remcohaszing** suggested using JSON-RPC over IPC, avoiding stdout, and adding an initialize call for plugins to register file extensions, noting uncertainty about the Next.js TypeScript plugin’s functionality

### [PR microsoft/TypeScript-go#2853](https://github.com/microsoft/TypeScript-go/pull/2853) (Closed)

**Implement ES2017 \(async\) transforms**

*Port ES2017 async transforms with improved argument and super detection, native Promise support, and obsolete diff removal.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2861](https://github.com/microsoft/TypeScript-go/pull/2861) (Closed)

**Implement for\-await \(ES2018\) transform, fix existing ES2018 issues**

*Implements ES2018 for-await-of syntax transform and resolves existing ES2018 transform issues*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2864](https://github.com/microsoft/TypeScript-go/pull/2864) (Closed)

**Enable \`noUncheckedSideEffectImports\` by default**

*Port PR 62443 to enable the noUncheckedSideEffectImports compiler option by default.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2864#issuecomment-3942792030) **jakebailey** said "Please file an issue with a repro. That should not be the case https://devblogs.microsoft.com/typescript/announcing-typescript-5-6/#the---nouncheckedsideeffectimports-option"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2864#issuecomment-3944772586) **pedro757** said "I can confirm this breaks css imports"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2864#issuecomment-3944805108) **Andarist** said "Please open a new issue with the repro steps included. Ideally, one that would showcase the difference between typescript@next and tsgo"
 * [later](https://github.com/microsoft/TypeScript-go/pull/2864#issuecomment-3967358451) **pedro757** said "@Andarist @jakebailey I filed the issue with a repro sandbox #2912 "

### [PR microsoft/TypeScript-go#2897](https://github.com/microsoft/TypeScript-go/pull/2897) (Closed, **jakebailey**, **Copilot**)

**Respect both \`js/ts\.experimental\.useTsgo\` and \`typescript\.experimental\.useTsgo\` settings**

*Update the extension to properly detect, watch, and update both js/ts.experimental.useTsgo and typescript.experimental.useTsgo settings.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2897#issuecomment-3961038254) **jakebailey** said "Tested with insiders today, it works."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2899](https://github.com/microsoft/TypeScript-go/pull/2899) (Closed)

**Improve asynchronous transfer performance**

*Optimize asynchronous transfers to reduce JS memory usage by 10–20% with minimal throughput change.*

 * created by **liuxingbaoyu**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2899#issuecomment-3955412992) **jakebailey** said "When was this feature introduced into Node?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2899#issuecomment-3955428336) **liuxingbaoyu** said "This was added from Node.js v5, but now the tests are failing, and I'm investigating."
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2901](https://github.com/microsoft/TypeScript-go/issues/2901) (Closed)

**\`tsgo\` do not support \`exports\` perfect**

*tsgo only supports exact package export paths and fails to handle wildcard exports such as './path/*'.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2901#issuecomment-3956541329) **jakebailey** said "This isn't enough information. What module resolution mode are you using?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2901#issuecomment-3957251118) **yanyunwu** attached an image showing the module resolution mode
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2901#issuecomment-3957276562) **jakebailey** said "moduleResolution=node is deprecated. You should have gotten an error for that in 6.0 (the version goy say in your issue)."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2901#issuecomment-3963119740) **RyanCavanaugh** said "Please make a new issue with a sample repo if fixing moduleResolution doesn't address your issue. We do not transcribe screenshots."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2902](https://github.com/microsoft/TypeScript-go/issues/2902) (Closed, `duplicate`, **ahejlsberg**, **jakebailey**, **Copilot**)

**Unique symbol defined as attribute not narrowed**

*A unique symbol assigned as an object property is not properly narrowed within a union type in TypeScript 7.0.*

 * created by **jfdoming**
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **jakebailey** assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#2904](https://github.com/microsoft/TypeScript-go/pull/2904) (Closed)

**\[@typescript/api\] Port scanner and token navigation utils to API client, include JSDoc in encoded ASTs, add more SourceFile properties**

*Integrate port scanner and token navigation into the TypeScript API client with JSDoc in encoded ASTs and more SourceFile properties.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#2905](https://github.com/microsoft/TypeScript-go/pull/2905) (Open)

**Fixed a crash on completions with auto\-imports racing with \`DidClose\` notification**

*Fix completions crash from auto-import retry racing with DidClose by preserving request cache entry and using consistent snapshots.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2905#issuecomment-3962591123) **andrewbranch** described passing their branch with snapshot adoption checks to gabritto, noted its uncertain status, and suggested retaining that functionality

### [Issue microsoft/TypeScript-go#2906](https://github.com/microsoft/TypeScript-go/issues/2906) (Open, `Crash`)

**Requests failing with \` Message: no project found for URI\`**

*After reloading VS Code, textDocument/codeLens requests fail with ‘no project found for URI’ errors.*

 * created by **mjbvz**
 * **mjbvz** added label `Crash`

### [PR microsoft/TypeScript-go#2907](https://github.com/microsoft/TypeScript-go/pull/2907) (Open, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix issue 63192 in TypeScript repository**

*Add reentrancy guards in TypeScript compiler to prevent infinite recursion during destructuring loop variables with defaults.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2907#issuecomment-3963094319) **RyanCavanaugh** said "@ahejlsberg the code comments here are a bit much but does this look like a correct CFA fix?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2907#issuecomment-3963104509) **RyanCavanaugh** said "Via https://github.com/Microsoft/TypeScript/issues/63192"

### [PR microsoft/TypeScript-go#2908](https://github.com/microsoft/TypeScript-go/pull/2908) (Open, **DanielRosenwasser**, **Copilot**)

**Add regression test for inlay hints crash on reparsed nodes \(\#2460\)**

*Add a regression test to ensure computing inlay hints on reparsed AST nodes in a JS module.exports function prevents panics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2909](https://github.com/microsoft/TypeScript-go/issues/2909) (Closed)

**skipLibCheck is not working as intended on skipping modules\-as\-namespaces error**

*tsgo fails to respect skipLibCheck and incorrectly reports modules-as-namespaces type errors in gl-matrix definitions.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2909#issuecomment-3964784793) **jakebailey** said "This is intentional. https://github.com/microsoft/typescript-go/issues/2873"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2910](https://github.com/microsoft/TypeScript-go/issues/2910) (Closed, `Domain: Editor`)

**Abnormal RAM/swap and CPU usage**

*Enabling the experimental tsgo TypeScript server in VSCode consumes excessive CPU and RAM/swap, making macOS sluggish.*

 * created by **Spookywy**
 * **Spookywy** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2911](https://github.com/microsoft/TypeScript-go/issues/2911) (Open, **jakebailey**, **Copilot**)

**TS4053 happens when public class method adopts imported type from library**

*Public methods in an exported class using an imported library type cause TS4053 errors with tsgo.*

 * created by **hkleungai**

### [Issue microsoft/TypeScript-go#2912](https://github.com/microsoft/TypeScript-go/issues/2912) (Closed, `Crash`)

**Error importing css files**

*Side-effect import of 'globals.css' in Next.js layout fails type-check with TS2882 after recent commit*

 * created by **pedro757**
 * **pedro757** added label `Crash`

