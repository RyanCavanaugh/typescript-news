# Report for 2025-12-13 (Saturday, December 13th, 2025)

10 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @Benjamin-Dobell reported that PR #2361 did not fix the issue and provided error output in [microsoft/TypeScript-go#1080](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3650241893)
    * @jordan-cutler asked if the issue was solely with ts-go and not the original TypeScript repo in [microsoft/TypeScript-go#2233](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3649895000)
    * @fooooooooooooooo provided repro steps and environment details in [microsoft/TypeScript-go#2375](https://github.com/microsoft/TypeScript-go/issues/2375#issuecomment-3649823930)
    * @xxxxue provided requested system information and resolution steps in [microsoft/TypeScript-go#2375](https://github.com/microsoft/TypeScript-go/issues/2375#issuecomment-3650321936)
    * @ChangeHow provided log output for the bundler mode bug in [microsoft/TypeScript-go#2379](https://github.com/microsoft/TypeScript-go/issues/2379#issuecomment-3651559068)

## Activity Summary

### [Issue microsoft/TypeScript-go#1080](https://github.com/microsoft/TypeScript-go/issues/1080) (Open, `Domain: Program`)

**Deduplicate doubly\-installed packages**

*Duplicated installations of the same npm package across workspaces lead to instances TypeScript tolerates but break Go type compatibility.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3457417471) **chriskrycho** added a real-world example showing that disabling deduplication prevents runtime errors due to unique symbols across dependencies and suggested maintaining the behavior with an opt-in migration flag
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3458576531) **jakebailey** referred to PR 62684 showing minimal breakage, described a potential implementation of a load plus dedupe pass, and expressed preference not to reintroduce the idea
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3644998431) **jakebailey** asked users to try building PR #2361 from source to see if it fixed their issues
 * [today](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3650241893) **Benjamin-Dobell** reported that building PR #2361 did not fix the reproduction and provided the error output

### [PR microsoft/TypeScript-go#1808](https://github.com/microsoft/TypeScript-go/pull/1808) (Closed)

**Add option for overriding \`GOMEMLIMIT\`**

*Provide a configuration option to override the GOMEMLIMIT environment variable.*

 * created by **maschwenk**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/1808#issuecomment-3648125290) **jakebailey** expressed desire to merge the changes to enable testing and noted that a merge from main was required
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/1808#issuecomment-3648129981) **maschwenk** said "@jakebailey on it!"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2162](https://github.com/microsoft/TypeScript-go/issues/2162) (Closed, `Domain: Type Checking`, **ahejlsberg**)

**Type inference lost for callback parameter**

*Using ts-go configuration causes TypeScript to lose type inference for the organization plugin's sendInvitationEmail callback parameter.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3633194332) **Azzerty23** said "I understand better, thank you for the detailed explanation!"
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3633253412) **ahejlsberg** explained that TypeScript uses parameter and return type inferences before applying constraints, described why the example infers Record<string, any> instead of OrganizationOptions, and suggested using a NoInfer marker in the return type of organization as a fix
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3633624829) **Azzerty23** thanked maintainers for the clear breakdown and said they would open a PR for Better Auth and let the team close the issue
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2233](https://github.com/microsoft/TypeScript-go/issues/2233) (Open, `Domain: Declaration Emit`, **weswigham**)

**Project references indirect dependencies: Error 2742 Inferred type of xxx \.\.\.**

*tsgo reports a TS2742 error when a package infers a type from an indirect project reference without directly referencing the originating package*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3633964119) **safareli** said "have same issue with pnpm"
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3633988288) **dimitraz** said "Likewise"
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3634836621) **sanny-io** said "@dimitraz @samdcoding please use the thumbs up instead. It is more considerate of subscribers watching issues."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3649895000) **jordan-cutler** disabled project references by setting composite to false, shared related research links, and asked if the issue was specific to ts-go

### [Issue microsoft/TypeScript-go#2245](https://github.com/microsoft/TypeScript-go/issues/2245) (Closed, `Domain: JS`, `Crash`, **ahejlsberg**)

**Folding range crash in JS file for \`exports\.property = CallExpression\(ObjectLiteral\)\`**

*The TypeScript Go LSP panics computing folding ranges for an export assignment call expression with an object literal.*

 * **DanielRosenwasser** added label `Domain: JS`
 * (yesterday) **ahejlsberg** assigned to **ahejlsberg**, and unassigned **navya9singh**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2284](https://github.com/microsoft/TypeScript-go/issues/2284) (Closed, `Crash`, **ahejlsberg**)

**Crash in \`getBaseTypes\`**

*The TypeScript Go internal checker panics with a nil pointer dereference in getBaseTypes during type checking.*

 * created by **DorianListens**
 * **DorianListens** added label `Crash`
 * **ahejlsberg** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2284#issuecomment-3649899671) **ahejlsberg** provided a short reproduction demonstrating the crash and announced plans to submit a PR to fix it
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2289](https://github.com/microsoft/TypeScript-go/issues/2289) (Closed, `Domain: JS`, `Crash`, **ahejlsberg**)

**Completions crash in JSDoc object type literal**

*Requesting completions inside a JSDoc object type literal crashes the TypeScript server due to a token cache mismatch.*

 * **DanielRosenwasser** added label `Domain: JS`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2289#issuecomment-3643508281) **DanielRosenwasser** reported a crash outside the object in a typedef and included a code snippet and panic stack trace
 * **DanielRosenwasser** assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2346](https://github.com/microsoft/TypeScript-go/issues/2346) (Closed, `Crash`, **ahejlsberg**)

**Crash for completion for property in JSDoc \`/\*\* @type \*/\` tag**

*TypeScript-Go language server crashes with a nil pointer panic when requesting completions inside a JSDoc @type property tag.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * **ahejlsberg** assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2371](https://github.com/microsoft/TypeScript-go/pull/2371) (Open)

**Fix getTokenAtPos in JSDoc trivia position**

*getTokenAtPosition incorrectly scans JSDoc trivia gaps, causing AST position mismatches, so we now track the next node to constrain scanning.*

 * created by **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2371#issuecomment-3649659571) **ahejlsberg** said "@gabritto See my comment here."

### [PR microsoft/TypeScript-go#2372](https://github.com/microsoft/TypeScript-go/pull/2372) (Closed)

**Reparse fixes**

*Revise AST reparsing for @type and @satisfies to retain original expressions and only flag cloned type nodes.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2372#issuecomment-3649566615) **ahejlsberg** explained that PR 2371 became simpler because tracking of special reparsed nodes was no longer needed and shouldVisitNode just checks that a node isn't reparsed
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2374](https://github.com/microsoft/TypeScript-go/pull/2374) (Closed)

**Support \`\<caption\>\</caption\>\` in JSDoc \`@example\` tags**

*Enable support for <caption> tags inside JSDoc @example blocks.*

 * created by **ahejlsberg**

### [Issue microsoft/TypeScript-go#2375](https://github.com/microsoft/TypeScript-go/issues/2375) (Open, `Domain: Editor`)

**panic: bundled: failed to evaluate symlinks: The system cannot find the path specified\. \[recovered, repanicked\]**

*Setting typescript.experimental.useTsgo in VS Code on Windows causes a panic in the TypeScript-Go bundle due to failed symlink resolution.*

 * created by **xxxxue**
 * **xxxxue** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2375#issuecomment-3649778536) **jakebailey** said "Can you provide more info about your system? Are all of your files living within a symlink somehow?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2375#issuecomment-3649823930) **fooooooooooooooo** reported the same error when evaluating symlinks on a scoop-installed VS Code data directory and included Go code and panic output
 * [today](https://github.com/microsoft/TypeScript-go/issues/2375#issuecomment-3650321936) **xxxxue** described linking D:\UserDir\admin to C:\Users\admin via a directory symlink and noted that moving main.exe out of the symlinked directory allowed the code to run successfully

### [PR microsoft/TypeScript-go#2376](https://github.com/microsoft/TypeScript-go/pull/2376) (Closed)

**Fix \`isPropertyDeclaredInAncestorClass\` function**

*Revise the isPropertyDeclaredInAncestorClass function to accurately identify properties inherited from ancestor classes.*

 * created by **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2376#issuecomment-3650972594) **camc314** said "nice, thank you 🙏 "
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2377](https://github.com/microsoft/TypeScript-go/issues/2377) (Open, `Crash`, **Copilot**)

**Crashes in decorators transform compiling VS Code**

*Compiling VS Code with tsgo crashes in the decorators transform, triggering a nil pointer panic during the emit pipeline.*

 * created by **DanielRosenwasser**
 * (later) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**

### [PR microsoft/TypeScript-go#2378](https://github.com/microsoft/TypeScript-go/pull/2378) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix crashes in decorators transform compiling VS Code**

*Fixes two crashes in decorators transform caused by missing nil checks and incorrect modifier indexing, adds tests and updates baselines.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2379](https://github.com/microsoft/TypeScript-go/issues/2379) (Open)

**TS2307 can't resolve type that import from pkg/dist directly**

*TypeScript fails to resolve types imported from a package’s dist folder, triggering TS2307 errors and any type fallbacks*

 * created by **ChangeHow**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2379#issuecomment-3651551480) **DanielRosenwasser** explained that the issue was caused by removal of support for --moduleResolution node10 and asked if the same issues occurred with nodenext or bundler
 * [later](https://github.com/microsoft/TypeScript-go/issues/2379#issuecomment-3651559068) **ChangeHow** confirmed the same bundler mode bug and provided log output

