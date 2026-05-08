# Report for 2026-05-04 (Monday, May 4th, 2026)

12 different users commented on 28 different issues.

## Recommended Actions

 * Response Recommended
    * @dhoulb requested that missing imports be added automatically on save in [microsoft/TypeScript-go#3318](https://github.com/microsoft/TypeScript-go/issues/3318#issuecomment-4373817264)
    * @hkleungai requested better documentation of expected differences in [microsoft/TypeScript-go#3694](https://github.com/microsoft/TypeScript-go/issues/3694#issuecomment-4377297602)

## Activity Summary

### [PR microsoft/TypeScript-go#2478](https://github.com/microsoft/TypeScript-go/pull/2478) (Closed)

**Exit LSP process if parent process stops existing**

*Implement periodic parent process ID checks in the LSP server to terminate the server when the parent process exits.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4270307434) **andrewbranch** said "I'm not against this if we think we still need it, but it feels like a bug (like #2499 was) if we can't exit just by reading from a STDIN that's no longer connected to anything"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4270354928) **jakebailey** explained that a client could set up a FIFO as the file descriptor for a child process which might never close
 * [today](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4372407010) **andrewbranch** said "I ended last week with 7 orphaned tsgo processes, so I guess we do still need this."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4372807985) **DanielRosenwasser** noted that the behavior seemed like a bug, observed it didn’t occur with Strada or the VS Code built-in, suggested investigating the latest language client, and proposed that sending events to a closed file descriptor could crash the process
 * [today](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4373756615) **jakebailey** questioned the concern, stating that if the client died without closing the child it wasn’t their bug and if the client is still alive accumulating tsgo processes it’s a client bug unaffected by the PR

### [Issue microsoft/TypeScript-go#3318](https://github.com/microsoft/TypeScript-go/issues/3318) (Open, `Domain: Editor`, **iisaduan**)

**Missing \`addMissingImports\` code action/code fix**

*VSCode’s editor.codeActionOnSave lacks implementation of TypeScript’s addMissingImports code action and code fix.*

 * (2 weeks ago) **RyanCavanaugh** added label `Domain: Editor`, and set milestone to `Post-7.0`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3318#issuecomment-4364081565) **dhoulb** said "Have become so reliant on this it might force me back to the non-experimental extension for now."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3318#issuecomment-4373717770) **iisaduan** described the addition of the 'fix all autoimports' functionality via PR 3382 and asked which trigger methods were relied on
 * [today](https://github.com/microsoft/TypeScript-go/issues/3318#issuecomment-4373817264) **dhoulb** described that code actions on save no longer automatically add missing imports, causing red squiggles and manual steps and lamented the loss of the previous smooth workflow
 * [today](https://github.com/microsoft/TypeScript-go/issues/3318#issuecomment-4374763168) **iisaduan** noted that the behavior would resume with the old configuration after naming fixes and suggested adding editor.codeActionsOnSave.source.fixAll set to always or explicit to replicate it now

### [Issue microsoft/TypeScript-go#3319](https://github.com/microsoft/TypeScript-go/issues/3319) (Open, **iisaduan**)

**Missing \`fixAll\` code action/code fix**

*VSCode’s TypeScript Go extension does not support the source.fixAll.ts code action or corresponding individual codefixes for editor.codeActionOnSave.*

 * **iisaduan** assigned to **iisaduan**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3319#issuecomment-4257481981) **jakebailey** said "Is this done with #3382? "
 * [today](https://github.com/microsoft/TypeScript-go/issues/3319#issuecomment-4373669906) **iisaduan** clarified that fixAll only applies a subset of codefixes, distinguished issues #3382 and #3318, and stated they would update naming and noted that issue #3305 is needed to reveal missing codeactions

### [Issue microsoft/TypeScript-go#3490](https://github.com/microsoft/TypeScript-go/issues/3490) (Closed, `wontfix`)

**TS2411 reported on properties declared in \`node\_modules\` \`\.d\.ts\` files \(e\.g\. @types/jsdom DOMWindow\), where tsc 6\.0 silently allows them**

*TypeScript native-preview 7.0 reports TS2411 conflicts for @types/jsdom DOMWindow properties in node_modules that tsc 6.0 silently allows.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3490#issuecomment-4298063413) **jakebailey** explained that the behavior was intentional to enable concurrent compilation since error details might vary with checking order
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3490#issuecomment-4305256978) **ahejlsberg** described a bug in Strada where index signature compatibility checks ran only on the first declaration encountered, causing missed diagnostics depending on file order, and noted that it was fixed in Corsa
 * **ahejlsberg** added label `wontfix`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3550](https://github.com/microsoft/TypeScript-go/issues/3550) (Closed, `wontfix`, `Domain: Declaration Emit`)

**Baselines: Optional property types in JS declarations drop \| undefined**

*Optional property types in JS declarations are incorrectly simplified by removing | undefined from the type signature.*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3550#issuecomment-4316567837) **RyanCavanaugh** said "Yeah, this is the right behavior under EOPT=false since it's local to the function"
 * **RyanCavanaugh** added label `wontfix`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3561](https://github.com/microsoft/TypeScript-go/issues/3561) (Closed, `wontfix`, `Domain: Declaration Emit`)

**Baselines: noImplicitThis functions returning this now fully expand the object type**

*Functions returning this under noImplicitThis now emit fully expanded object types instead of any, changing type contracts.*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3561#issuecomment-4316537499) **RyanCavanaugh** demonstrated Strada bailing at one level and Corsa at two, and showed the resulting type declaration diff
 * **RyanCavanaugh** added label `wontfix`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3621](https://github.com/microsoft/TypeScript-go/issues/3621) (Open, `Crash`, `Needs More Info`)

**Panic Alert Notification when Cursor edits some file and opening that file causes panic\.**

*Opening or editing a file causes a panic in the semanticTokens request because a token improperly spans multiple lines.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4342371254) **Swiftwork** said "Observing same issue for the last 1-2 weeks"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4361443953) **Raynos** said "Observing same issue in cursor too."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4369143872) **CarlosZiegler** said "Observing same issue in cursor too. "
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4373908974) **RyanCavanaugh** suggested opening in VS Code with the TypeScript Native Preview to verify whether the issue persisted and asked for a minimal LSP trace to reproduce the crash

### [Issue microsoft/TypeScript-go#3682](https://github.com/microsoft/TypeScript-go/issues/3682) (Closed, `wontfix`)

**Behavior difference: Assigning static field outside class definition gives TS7005 in tsc but gives TS7008 in tsgo**

*Assigning a static field outside a class triggers TS7005 in tsc but TS7008 in tsgo.*

 * created by **hkleungai**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3682#issuecomment-4364020807) **ahejlsberg** stated that Strada incorrectly tagged expando properties as variables and that the Corsa terminology was more correct, so no fix was needed
 * **ahejlsberg** added label `wontfix`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3683](https://github.com/microsoft/TypeScript-go/issues/3683) (Closed, `wontfix`)

**Behavior difference: jsdoc \`@readonly\` placed on class getter gives error on tsgo but not in tsc**

*Applying jsdoc @readonly to a class getter produces no error with tsc but triggers a TS1024 error in tsgo.*

 * created by **hkleungai**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3683#issuecomment-4364015917) **ahejlsberg** said "This definitely seems like a reasonable diagnostic. I don't think we want to change anything here."
 * **ahejlsberg** added label `wontfix`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3687](https://github.com/microsoft/TypeScript-go/issues/3687) (Open, `possible improvement`)

**No compiled packages for netbsd**

*No compiled @typescript/native-preview package is available for NetBSD x64, causing an error.*

 * created by **mudcovered**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3687#issuecomment-4375095282) **jakebailey** explained that builds currently match VS Code and that supporting additional platforms will be considered but nightly builds for all platforms are unlikely at this time

### [Issue microsoft/TypeScript-go#3691](https://github.com/microsoft/TypeScript-go/issues/3691) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behavior difference: Assigning \`Object\.values\(obj\)\` to \`obj\[field\]\` gives error on tsgo but not on tsc**

*Assigning Object.values(obj) to a property triggers a self-referential initialization type error in tsgo but not in tsc*

 * (today) **ahejlsberg** added label `Domain: Type Checking`, and set milestone to `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3691#issuecomment-4372295101) **ahejlsberg** explained that failing to recognize an expando object literal had led to inferring an index type and causing circularity
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3692](https://github.com/microsoft/TypeScript-go/issues/3692) (Open, `Needs More Info`)

**Excessive CPU usage**

*WebStorm’s ts-go server often consumes 80-100% CPU when adding new imports in a monorepo frontend until restarted.*

 * created by **Jelcoo**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4365884783) **Jelcoo** shared WebStorm TypeScript server settings screenshot
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4365889287) **Jelcoo** said "While writing this issue I was working on https://github.com/calagopus/panel/commit/2db0200f2c03ab2174db6f012363fe0a49a7c967, but it has been happening with all sorts of other changes."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4374556539) **jakebailey** said "I have no idea how WebStorm works, but in VS Code, we have a command that can take a profile and you could upload that."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4374635334) **andrewbranch** explained that briefly spiking to 80–100% CPU usage when adding imports was not unusual, and that only sustained high usage would be abnormal

### [Issue microsoft/TypeScript-go#3693](https://github.com/microsoft/TypeScript-go/issues/3693) (Closed, `wontfix`)

**Behavior difference: Exporting object literal from js file emits object literal type in tsgo, as opposed to \`namespace\` in tsc\.**

*tsgo exports JavaScript object literals as literal types instead of namespaces like tsc, and this behavior difference (along with optional omission of @satisfies JSDoc comments) should be documented in CHANGES.md.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3693#issuecomment-4372517238) **ahejlsberg** explained that the new declaration file emitter differs from Strada and stays closer to the original code and pointed to the CHANGES.md section
 * **ahejlsberg** added label `wontfix`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3694](https://github.com/microsoft/TypeScript-go/issues/3694) (Closed, `wontfix`, **DanielRosenwasser**, **iisaduan**, **Copilot**)

**Behavior difference: jsdoc \`@param\` referencing object attribute value throws TS2749 in tsc but throws TS2503 in tsgo**

*When using jsdoc @param to reference an object property, tsgo throws TS2503 instead of TS2749 like tsc*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3694#issuecomment-4372991421) **DanielRosenwasser** said "This is sort of expected and documented - you now need to write typeof map.foo."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3694#issuecomment-4373421301) **hkleungai** agreed that the documented behavior was expected but noted that the namespace error was no better than the typeof error in the jsdoc @param context
 * [today](https://github.com/microsoft/TypeScript-go/issues/3694#issuecomment-4374659308) **jakebailey** said "@hkleungai General question: how are you finding these? Do you have a project that we could have in our extended test suite going forward? Is this at some company?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3694#issuecomment-4374776508) **DanielRosenwasser** said "Sorry, I misread the issue."
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3694#issuecomment-4377297602) **hkleungai** described how they found issues by diffing tsc and tsgo outputs, noted the productivity of the manual process, and requested better documentation of expected differences

### [PR microsoft/TypeScript-go#3698](https://github.com/microsoft/TypeScript-go/pull/3698) (Open)

**Add minimal tsc output format**

*Implement a new --outputFormat minimal option in tsgo to emit compact, one-line diagnostics for easier parsing and reduced token usage.*

 * created by **JoviDeCroock**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3698#issuecomment-4373045201) **JoviDeCroock** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#3699](https://github.com/microsoft/TypeScript-go/pull/3699) (Closed)

**Fix circularity in expando object property assignment**

*Break the circular reference causing infinite recursion during expando object property assignments.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3700](https://github.com/microsoft/TypeScript-go/issues/3700) (Closed, `Domain: Editor`, `Crash`, **jakebailey**)

**isolatedDeclarations code action crash for whitespace\-only JSX text nodes**

*IsolatedDeclarations code action panics on whitespace-only JSX text nodes with an index out of range error.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Domain: Editor`, `Crash`, and assigned to **jakebailey**
 * (later) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3701](https://github.com/microsoft/TypeScript-go/issues/3701) (Open, **jakebailey**, **Copilot**)

**When using \`module=commonjs\`, Array destructuring is transpiled with wrong \(non\-iterator\) behavior**

*Compiling with module=commonjs wrongly transpiles exported array destructuring into fixed index access instead of iterator logic.*

 * created by **blickly**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3702](https://github.com/microsoft/TypeScript-go/pull/3702) (Open)

**Update dependencies**

*Update npm, Go, golangci-lint, jsonv2, and dprint plugin dependencies (including gofumpt).*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3703](https://github.com/microsoft/TypeScript-go/pull/3703) (Open, **jakebailey**)

**Fixes to \-\-generateTrace to make analyze\-trace work**

*Fix the --generateTrace option to ensure analyze-trace functions correctly.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3704](https://github.com/microsoft/TypeScript-go/issues/3704) (Closed, `wontfix`)

**Behavior difference: Plain js class field with initial value \`null\` is \`null\` type in tsgo, but used to be \`any\` type in tsc**

*tsgo infers a plain JS class field initialized to null as null rather than any, causing clearInterval type errors.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3704#issuecomment-4374459625) **ahejlsberg** explained that Corsa infers this.timeout as number|null and ignores self-references in nested functions while Strada infers any for such self-references
 * **ahejlsberg** added label `wontfix`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3705](https://github.com/microsoft/TypeScript-go/pull/3705) (Open, **jakebailey**, **Copilot**)

**Preserve native destructuring for CommonJS exports to keep iterator semantics**

*Emit native destructuring for CommonJS exports and generate separate export assignments per identifier to preserve iterator semantics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4374885896) **jakebailey** noted uncertainty about its impact on cjs-module-lexer scanning and asked if it was the intended change

### [PR microsoft/TypeScript-go#3706](https://github.com/microsoft/TypeScript-go/pull/3706) (Open, **DanielRosenwasser**, **Copilot**)

**Fix JSDoc @param qualified name error: produce TS2749 instead of TS2503**

*Implement two-step JSDoc qualified name resolution in JS files to produce TS2749 instead of TS2503 errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3706#issuecomment-4375172726) **Copilot** clarified that the PR only changed the error message from TS2503 to TS2749 and did not resolve obj.foo as typeof obj.foo in type position

### [PR microsoft/TypeScript-go#3707](https://github.com/microsoft/TypeScript-go/pull/3707) (Closed)

**fix\(3700\): fix index out of range panic when emitting whitespace\-only jsx text**

*Fix index out-of-range panic during JSX emission when text nodes contain only whitespace.*

 * created by **a-tarasyuk**
 * (later) **gabritto** closed the issue

