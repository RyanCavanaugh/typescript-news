# Report for 2026-01-11 (Sunday, January 11th, 2026)

17 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @mustafa519 asked why the errors occur and provided a stack trace in [microsoft/TypeScript-go#1673](https://github.com/microsoft/TypeScript-go/issues/1673#issuecomment-3738641522)
    * @rektide asked about decorator transform implementation and granularity options in [microsoft/TypeScript-go#2354](https://github.com/microsoft/TypeScript-go/issues/2354#issuecomment-3736508508)
    * @jansedlon asked about not seeing a difference in autoimport speed after the release in [microsoft/TypeScript-go#2390](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3735316463)
    * @rubnogueira asked if the initial completion delay was expected behavior in [microsoft/TypeScript-go#2390](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3737965364)
    * @jansedlon reported encountering issue #2467 after updating to version 0.20260112 in [microsoft/TypeScript-go#2390](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3738018268)
    * @Titozzz asked whether to create a new issue for incremental caching behavior in [microsoft/TypeScript-go#2455](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3738468999)
    * @christophe-g asked if the issue was related to a pnpm compatibility comment in [microsoft/TypeScript-go#2467](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3735094359)
    * @Bill-Owen provided information about using pnpm as environment detail in [microsoft/TypeScript-go#2467](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3736673419)
    * @jansedlon provided environment details (pnpm + monorepo) in [microsoft/TypeScript-go#2467](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3738021094)
    * @lukpsaxo reported errors on every file after upgrading and indicated the extension is unusable in [microsoft/TypeScript-go#2467](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3738443438)
    * @gggdomi reported that tsgo 0.20260112.1 crashed on launch using yarn and VSCode's typescriptteam.native-preview in [microsoft/TypeScript-go#2467](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3738502725)
    * @WonderPanda reported that downgrading to version 0.20260109.1 resolved the issue in [microsoft/TypeScript-go#2467](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3739018524)

## Activity Summary

### [Issue microsoft/TypeScript-go#1673](https://github.com/microsoft/TypeScript-go/issues/1673) (Open, `Crash`, **Copilot**)

**Panic on textDocument/definition**

*A panic occurs during textDocument/definition handling when the requested line number exceeds the document’s line map.*

 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1673#issuecomment-3433177361) **jakebailey** said "@richburdon That's #1867. I don't think this should be too hard to fix quick."
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1673#issuecomment-3447744485) **jakebailey** reported a panic in the definition handler due to a bad line number
 * **jakebailey** assigned to **Copilot**
 * [later](https://github.com/microsoft/TypeScript-go/issues/1673#issuecomment-3738641522) **mustafa519** mentioned also getting similar errors and provided a stack trace

### [Issue microsoft/TypeScript-go#2233](https://github.com/microsoft/TypeScript-go/issues/2233) (Closed, `Domain: Declaration Emit`, **weswigham**)

**Project references indirect dependencies: Error 2742 Inferred type of xxx \.\.\.**

*tsgo reports a TS2742 error when a package infers a type from an indirect project reference without directly referencing the originating package*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3634836621) **sanny-io** said "@dimitraz @samdcoding please use the thumbs up instead. It is more considerate of subscribers watching issues."
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3649895000) **jordan-cutler** disabled project references by setting composite to false, shared related research links, and asked if the issue was specific to ts-go
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3725740998) **marvinroger** clarified that the errors occur with npm as well as pnpm, Yarn, and Bun and noted that the issue persists in version 7.0.0-dev.20260108.1
 * [later](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3738637535) **fubhy** reported encountering the same issue with the new Effect codebase and traced it to a small fix in the typescript-go repository

### [Issue microsoft/TypeScript-go#2354](https://github.com/microsoft/TypeScript-go/issues/2354) (Open, `Domain: Emit`)

**Implement esnext\-\>es2022 transformer \(ES decorators, \`using\` declarations\)**

*Implement ES decorator transformations to enable --target es2022 support in the esnext->es2022 transformer.*

 * created by **DanielRosenwasser**
 * **jakebailey** added label `Domain: Emit`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2354#issuecomment-3736508508) **rektide** requested implementation of the decorator transform in tsgo, loosening of decorator type‐signature restrictions, and more granular control such as enabling decorators with newer ES targets

### [PR microsoft/TypeScript-go#2390](https://github.com/microsoft/TypeScript-go/pull/2390) (Closed)

**New auto\-import infrastructure**

*Redesigns TypeScript's auto-import collection infrastructure to support snapshot-based LSP, parallelized data collection, and improved caching.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3686389797) **rubnogueira** reported that upgrading to the latest master broke auto-imports and related features in their pnpm mono/polyrepo, requiring a revert, and said they looked forward to testing the fixes when time permitted
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3705657539) **andrewbranch** expressed uncertainty about why the performance difference was small, noted how fast TS-based completions were, mentioned opportunities to optimize Go completions, and removed all profile hot spots for the auto-import path
 * (2 days ago) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3735316463) **jansedlon** reported not seeing a difference in autoimport speed after updating to the released version and shared logs from the Go version
 * [later](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3737965364) **rubnogueira** described resolving auto-import issues, noted a 3–4 second initial completion delay, and asked if it was expected behavior
 * [later](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3738018268) **jansedlon** mentioned restarting VSCode and updating from 0.20260111.1 to 0.20260112, then encountering issue #2467 and promised to report when it’s resolved

### [Issue microsoft/TypeScript-go#2455](https://github.com/microsoft/TypeScript-go/issues/2455) (Open, `Needs More Info`)

**TSGO not reporting TS2548**

*TSGO reports TS6133 but omits the TS2548 error when spreading a value typed as unknown[]|null.*

 * **ahejlsberg** added label `Needs More Info`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3725009336) **ahejlsberg** showed error output from tsgo and tsc with noUnusedLocals enabled, reporting errors TS6133 and TS2488 for spreading a null value
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3729341477) **Titozzz** said "I'll try to either narrow it down to a small reproduction, or, find what causes my issue and will be back to you. "
 * [later](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3738468999) **Titozzz** noted that omitting or setting a deprecated ‘target’ to “es5” reproduced the issue and asked about an incremental caching annoyance and whether to open a new issue

### [Issue microsoft/TypeScript-go#2467](https://github.com/microsoft/TypeScript-go/issues/2467) (Closed, `Crash`, **andrewbranch**)

**\[Panic Report\] : panic: module symbol has no non\-augmentation declaration**

*Panic occurs in TypeScript-Go autoimport when a module symbol lacks a non-augmentation declaration*

 * created by **christophe-g**
 * **christophe-g** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3735094359) **christophe-g** said "There was a comment about #2390 not working with pnpm  - might be related https://github.com/microsoft/typescript-go/pull/2390#issuecomment-3686389797  ?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3735153843) **jakebailey** said "I don't think they implied a crash; a repro would be most helpful here."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3736673419) **Bill-Owen** said "Getting this too. We are using pnpm if that's relevant"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3738021094) **jansedlon** said "Same, pnpm + monorepo"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3738443438) **lukpsaxo** said "I use yarn with a traditional copy files into node_modules and after upgrading I get this error on seemingly every file - so the extension appears to have become unusable for me."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3738489291) **rvion** said "same; can't use tsgo at all on my project"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3738502725) **gggdomi** said "Same issue here, using yarn. tsgo 0.20260112.1 via VSCode's typescriptteam.native-preview just crashes on launch."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3739018524) **WonderPanda** reported experiencing the issue with tsgo in an NX monorepo using pnpm and noted that downgrading to version 0.20260109.1 resolved the problem

### [PR microsoft/TypeScript-go#2469](https://github.com/microsoft/TypeScript-go/pull/2469) (Open)

**Update JsxOpeningElement type**

*Correct the JsxOpeningElement type to reflect that it can only appear as a child of a JsxElement rather than as an Expression.*

 * created by **ArnaudBarre**

### [Issue microsoft/TypeScript-go#2470](https://github.com/microsoft/TypeScript-go/issues/2470) (Closed, `Domain: Editor`)

**Rename symbol \(textDocument/rename\) fails for Class Private Elements \(\#\-prefixed fields, methods, etc\)**

*VS Code’s rename command fails to rename TypeScript class private fields, methods, and accessors prefixed with #.*

 * created by **ThinaticSystem**
 * **ThinaticSystem** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#2471](https://github.com/microsoft/TypeScript-go/pull/2471) (Closed)

**Fix module specifiers to use source file for project reference outputs**

*Use original source filenames instead of compiled outputs when generating module specifiers for project references to avoid TS2742 errors.*

 * created by **fubhy**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2471#issuecomment-3738628457) **fubhy** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#2472](https://github.com/microsoft/TypeScript-go/pull/2472) (Closed)

**fix\(2470\): extend rename eligibility for additional node kinds**

*Extend rename feature to include class private elements by adding support for private identifier nodes.*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#2473](https://github.com/microsoft/TypeScript-go/issues/2473) (Closed, `Crash`, **andrewbranch**)

**Autocompletion panics**

*Autocompletion and autoimport suggestions trigger a panic due to an unexpected internal symbol name in export.*

 * created by **pedro757**
 * **pedro757** added label `Crash`

