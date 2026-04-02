# Report for 2026-02-27 (Friday, February 27th, 2026)

15 different users commented on 18 different issues.

## Recommended Actions

 * Response Recommended
    * @JoostK provided repro steps, heap profile, and asked about potential extension interactions in [microsoft/TypeScript-go#2910](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3975829460)
    * @sgjm provided repro steps showing comment formatting differences in [microsoft/TypeScript-go#2927](https://github.com/microsoft/TypeScript-go/issues/2927#issuecomment-3974111276)

## Activity Summary

### [Issue microsoft/TypeScript-go#2457](https://github.com/microsoft/TypeScript-go/issues/2457) (Open)

**Proposal: Prettified type display in hover output**

*Add optional settings to display prettified, expanded types in hover output for better readability.*

 * created by **sQVe**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2457#issuecomment-3974008251) **EvgenyOrekhov** stated that VS Code now supports this natively and showed how to increase hover verbosity by clicking '+'

### [Issue microsoft/TypeScript-go#2910](https://github.com/microsoft/TypeScript-go/issues/2910) (Closed, `Domain: Editor`)

**Abnormal RAM/swap and CPU usage**

*Enabling the experimental tsgo TypeScript server in VSCode consumes excessive CPU and RAM/swap, making macOS sluggish.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3972092239) **obedparla** reported that migrating to TSGO succeeded in 7.0.0-dev.20260130.1 but failed in 0.20260226.1, suggesting a regression
 * [today](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3972146716) **andzdroid** reported issue persisted across versions when running tsgo --watch idle after initial build
 * [today](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3973086152) **GGomez99** reproduced excessive memory and CPU usage in the TypeScript-Go LSP, provided reproduction steps, attempted fixes, and a heap profile, and asked if cached data/config might be triggering the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3975829460) **JoostK** reported high memory and CPU usage by the TypeScript LSP with repro steps, heap profile, and attempted fixes, and asked if cached data or another extension could be causing the issue

### [Issue microsoft/TypeScript-go#2911](https://github.com/microsoft/TypeScript-go/issues/2911) (Open, **jakebailey**, **Copilot**)

**TS4053 happens when public class method adopts imported type from library**

*Public methods in an exported class using an imported library type cause TS4053 errors with tsgo.*

 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-3971719843) **hkleungai** edited the issue description with test results for various subcases and asked if they should open a new issue on the ts6 repo
 * [today](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-3974546052) **hkleungai** mentioned that a similar issue had been reported for an exported variable with a different error code, and noted that TypeScript 6 still mishandles some cases

### [PR microsoft/TypeScript-go#2923](https://github.com/microsoft/TypeScript-go/pull/2923) (Closed)

**created agent from minimization prompt**

*Custom replay-minimizer agent uses a multi-step prompt to reduce replay JSON files to minimal reproductions.*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#2926](https://github.com/microsoft/TypeScript-go/pull/2926) (Open)

**Implement ES decorator transform \(ESNext \-\> ES2022\)**

*Add ESNext-to-ES2022 decorator transform support in tsgo to unblock its adoption.*

 * created by **AlCalzone**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-3975214922) **AlCalzone** said "Thanks for the thorough review - I'll see what I can do about it."

### [Issue microsoft/TypeScript-go#2927](https://github.com/microsoft/TypeScript-go/issues/2927) (Closed)

**"removeComments" may not work correctly in an if block\.**

*tsgo fails to remove comments inside if statements when removeComments is enabled, unlike the TypeScript compiler.*

 * created by **sgjm**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2927#issuecomment-3974111276) **sgjm** provided another case comparing tsc and tsgo outputs to illustrate comment handling differences
 * [today](https://github.com/microsoft/TypeScript-go/issues/2927#issuecomment-3974118999) **jakebailey** said "Yeah, i'm pretty sure this is just a simple emit bug where we are not checking removeComments; I fixed this in a branch but could send it early."

### [PR microsoft/TypeScript-go#2928](https://github.com/microsoft/TypeScript-go/pull/2928) (Open, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix crash during compilation of SubTup type**

*Added nil guards and tests to fix a nil pointer dereference crash during SubTup type compilation*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#2929](https://github.com/microsoft/TypeScript-go/pull/2929) (Open, **RyanCavanaugh**, **Copilot**)

**Add high\-quality SKILL for compiler and fourslash tests**

*Create a comprehensive SKILL.md guide documenting compiler and fourslash test workflows with proper formatting and integrated review feedback.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2929#issuecomment-3974292707) **Copilot** notified that the skill lacked the proper header and moved it to .github/skills/compiler-and-fourslash-tests/SKILL.md with YAML frontmatter
 * [today](https://github.com/microsoft/TypeScript-go/pull/2929#issuecomment-3974740167) **RyanCavanaugh** said "@copilot+claude-opus-4.6 integrate everyone's feedback and push a new commit"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2929#issuecomment-3974776460) **Copilot** integrated feedback and pushed commit 45bec897, removing unnecessary sections, updating syntax, and adjusting commands

### [PR microsoft/TypeScript-go#2930](https://github.com/microsoft/TypeScript-go/pull/2930) (Closed, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Port changes from TypeScript pull request 63200**

*Port TypeScript PR 63200 by adding symbol name to unsafe import error messages and introducing a new TS2883 diagnostic.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#2931](https://github.com/microsoft/TypeScript-go/pull/2931) (Closed, **gabritto**, **Copilot**)

**Port PR \#63200: Add symbol name to unsafe import error \(TS2883\)**

*Ports symbol name support in unsafe import error (TS2883) by updating SymbolTracker interface, implementations, and call sites.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **gabritto**

### [Issue microsoft/TypeScript-go#2932](https://github.com/microsoft/TypeScript-go/issues/2932) (Closed, `Crash`, **DanielRosenwasser**)

**Panic on find\-all\-refs when a parameter property is preceded by a non\-property member\.**

*Invoking find-all-references on a constructor parameter property after a non-property class member causes a panic.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2933](https://github.com/microsoft/TypeScript-go/pull/2933) (Closed)

**Fix deadlock in LSPClient**

*Formatting tests for LSPClient are hanging indefinitely because NewLSPClient’s goroutines deadlock on a WaitGroup.*

 * created by **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2933#issuecomment-3975090670) **jakebailey** asked why cancellation was not exiting the writeLoop select loop

### [PR microsoft/TypeScript-go#2934](https://github.com/microsoft/TypeScript-go/pull/2934) (Closed)

**fix\(2932\): handle parameter\-property ref to method with same name**

*Ensure parameter-property references to methods with the same name are resolved correctly.*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#2935](https://github.com/microsoft/TypeScript-go/issues/2935) (Closed, `Crash`, **ahejlsberg**, **jakebailey**, **Copilot**)

**Stack overflow in type instantiation with recursive function and generic type params**

*A recursive generic camelCase transformation using type-fest triggers a tsgo stack overflow from v4.38.0 onward, while tsc compiles it.*

 * created by **wadjoh**
 * **wadjoh** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2935#issuecomment-3976721921) **apendua** said "A fun fact, this crash does not seem to occur with the latest version of type-fest (i.e. ^5.0.0), but I was able to confirm that it breaks for ^4.0.0."

### [Issue microsoft/TypeScript-go#2936](https://github.com/microsoft/TypeScript-go/issues/2936) (Open, **jakebailey**, **Copilot**)

**\[bug\] JSX parsing fails with spurious syntax errors in ternary expression with nested JSX and multi\-property object literals**

*tsgo 7.0.0-dev misparses nested JSX inside a ternary with object literal props, producing spurious syntax errors.*

 * created by **hou-pu**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2937](https://github.com/microsoft/TypeScript-go/pull/2937) (Open, **jakebailey**, **Copilot**)

**Fix JSX parsing failures in ternary expressions with nested JSX attributes**

*The Go port of the TypeScript parser fails to handle nested JSX in ternary expressions due to missing parameter-list checks.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2938](https://github.com/microsoft/TypeScript-go/pull/2938) (Closed, `dependencies`, `javascript`)

**Bump minimatch from 10\.2\.1 to 10\.2\.4**

*Update minimatch dependency from version 10.2.1 to 10.2.4 to apply performance optimizations, bug fixes, and a ReDoS warning.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

### [PR microsoft/TypeScript-go#2939](https://github.com/microsoft/TypeScript-go/pull/2939) (Closed)

**fix\(2927\): add missing commentsDisabled checks to prevent emitting comments**

*Add missing commentsDisabled checks to prevent comments from being emitted when disabled.*

 * created by **a-tarasyuk**

