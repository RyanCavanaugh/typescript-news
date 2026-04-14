# Report for 2026-04-09 (Thursday, April 9th, 2026)

11 different users commented on 15 different issues.

## Recommended Actions

 * Response Recommended
    * @krutoo asked if it's possible to describe types for modules imported with attributes in [microsoft/TypeScript#55994](https://github.com/microsoft/TypeScript/issues/55994#issuecomment-4217062536)
    * @Jasper-Nelligan asked if anyone else was facing this issue in [microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4220113144)
    * @denis-migdal asked whether using const T would force the more precise inference in [microsoft/TypeScript#63377](https://github.com/microsoft/TypeScript/issues/63377#issuecomment-4221303828)
    * @denis-migdal provided detailed inference example and clarification in [microsoft/TypeScript#63378](https://github.com/microsoft/TypeScript/issues/63378#issuecomment-4216001335)
    * @kidCaulfield provided reproduction steps and test results in [microsoft/TypeScript#63382](https://github.com/microsoft/TypeScript/issues/63382#issuecomment-4218277267)

## Activity Summary

### [Issue microsoft/TypeScript#10011](https://github.com/microsoft/TypeScript/issues/10011) (Closed, `By Design`, `Suggestion`, `Needs Proposal`, `Help Wanted`, `Committed`, `Canonical`, `Effort: Difficult`, `Working as Intended`, `Awaiting More Feedback`)

**Love for TypeScript**

*The author expresses gratitude for Anders Hejlsberg’s contributions to TypeScript and VS Code and suggests adding a LOVE tag on GitHub.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/10011#issuecomment-4194592524) **RyanCavanaugh** said "Bad bots, what are we doing here"
 * (3 days ago) **RyanCavanaugh** reopened the issue
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/10011#issuecomment-4195652127) **FagnerMartinsBrack** said "@RyanCavanaugh BOTs can't love, so they don't see a reason for one's existence =("
 * [today](https://github.com/microsoft/TypeScript/issues/10011#issuecomment-4219296769) **typescript-bot** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/10011#issuecomment-4222334679) **johnnyreilly** said "Nooooooooo"

### [Issue microsoft/TypeScript#55994](https://github.com/microsoft/TypeScript/issues/55994) (Closed, `Suggestion`, `Help Wanted`, `Committed`)

**Type\-check Import Attributes in static imports**

*Support type-checking and auto-completion of static ES module import attributes using the global ImportAttributes interface.*

 * (2.2 years ago) **andrewbranch** closed the issue
 * (2.1 years ago) **DanielRosenwasser** set milestone to `TypeScript 5.4.0`, and removed from milestone `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/55994#issuecomment-4217062536) **krutoo** asked if it was possible to describe types for modules imported with attributes and shared a non-working example
 * [today](https://github.com/microsoft/TypeScript/issues/55994#issuecomment-4217083245) **jakebailey** said "That is #46135, I searched for "module attribute" and it was the first result."

### [Issue microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **andrewbranch**, **Copilot**)

**Deprecate, remove support for \`baseUrl\`**

*TypeScript 6.0 will deprecate baseUrl support and require explicit prefixes in paths mappings.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4187271405) **jakebailey** said "There's no problem. This is very intentional. Remove that option."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4197912770) **SOMONSOUM** suggested removing the baseUrl setting and adding a paths configuration
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4205504780) **ArfanFahad** removed baseUrl and confirmed it worked after adding paths
 * [today](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4220113144) **Jasper-Nelligan** reported that adding a catch-all paths entry caused VSCode to auto-suggest imports from node_modules and asked if anyone else was facing the issue

### [Issue microsoft/TypeScript#63346](https://github.com/microsoft/TypeScript/issues/63346) (Closed, `Question`)

**Experimental \(deprecated\) decorators are included by default**

*The ESNext library includes legacy experimental decorator types by default, causing conflicts with new decorator definitions.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4193336835) **RyanCavanaugh** thanked the user and provided a list of similar issues
 * **RyanCavanaugh** added label `Question`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4200850258) **RyanCavanaugh** said "The error message means what it says; you are missing the export modifier on your type alias"
 * [today](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4219297379) **typescript-bot** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63373](https://github.com/microsoft/TypeScript/issues/63373) (Open)

**tsserver hangs in Yarn PnP projects — incorrect directory watcher due to unchecked indexOf returning \-1**

*tsserver in Yarn PnP projects hangs because unchecked indexOf on non-node_modules paths produces incorrect directory watcher paths.*

 * created by **sebaspf**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63373#issuecomment-4208290436) **RyanCavanaugh** provided an auto-generated analysis listing similar issues to help get started
 * [today](https://github.com/microsoft/TypeScript/issues/63373#issuecomment-4217077271) **jakebailey** said "This is out of our control; this is a patch and we do not maintain it."

### [Issue microsoft/TypeScript#63376](https://github.com/microsoft/TypeScript/issues/63376) (Open, `Fixed`)

**TS2589 regression in 6\.0: implements without type parameters causes excessive type instantiation when property uses concrete generic type**

*TypeScript 6.0 regression triggers TS2589 excessive type instantiation when implementing a generic interface without type parameters for concrete-generic properties.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63376#issuecomment-4210461429) **RyanCavanaugh** explained that adding variance annotations prevented the problem, noted it didn't repro in TS 7, and asserted it wouldn't meet the 6.0 patch bar
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63376#issuecomment-4210463969) **RyanCavanaugh** provided a smaller reproduction snippet demonstrating the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63376#issuecomment-4212933992) **julienw** thanked the reviewer and mentioned that Claude had helped compare type instantiations with and without explicitly specifying the generic parameter
 * **RyanCavanaugh** added label `Fixed`

### [Issue microsoft/TypeScript#63377](https://github.com/microsoft/TypeScript/issues/63377) (Open, `Question`)

**TS doesn't properly infer generic callback \`\<T\>\(x: X\<T\>\) =\> T\` when providing \`\(x\) =\> new T\(\)\` \(parameter defined without type\)**

*TypeScript does not infer a generic callback’s type when its parameter is untyped, resulting in any instead.*

 * created by **denis-migdal**
 * [today](https://github.com/microsoft/TypeScript/issues/63377#issuecomment-4212713074) **denis-migdal** suggested assuming the callback had a ControllerProvider shape and using single or two-pass type inference guided by error feedback
 * **RyanCavanaugh** added label `Unactionable`
 * [today](https://github.com/microsoft/TypeScript/issues/63377#issuecomment-4217684561) **RyanCavanaugh** explained that this behavior is by design due to how TypeScript's inference algorithm handles contextual typing of callback parameters and generic type parameter inference
 * (today) **RyanCavanaugh** added label `Question`, and removed label `Unactionable`
 * [today](https://github.com/microsoft/TypeScript/issues/63377#issuecomment-4221303828) **denis-migdal** thanked for the answer, described two possible inference results for createViewClass2, and asked if using a const generic parameter would select the more precise inference

### [Issue microsoft/TypeScript#63378](https://github.com/microsoft/TypeScript/issues/63378) (Open, `Domain: check: Type Inference`, `Possible Improvement`)

**Object properties are inferred in the wrong order: should infer properties with \`NoInfer\<T\>\` AFTER properties with \`T\`**

*TypeScript infers object properties with NoInfer<T> before plain generics rather than after, causing inconsistent inference order.*

 * created by **denis-migdal**
 * [today](https://github.com/microsoft/TypeScript/issues/63378#issuecomment-4215837275) **RyanCavanaugh** asked if this was the same as issue #47599 and expressed confusion about inferring something before or after
 * [today](https://github.com/microsoft/TypeScript/issues/63378#issuecomment-4216001335) **denis-migdal** clarified their issue is a specific subcase of #47599 and described the observed inference behavior with and without attachController
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63379](https://github.com/microsoft/TypeScript/issues/63379) (Open, `Docs`)

**\`es2025\` is not a valid enum option for \`jsconfig\.json\`'s \`compilerOptions\.target\` enum**

*The JSON schema for jsconfig.json/tsconfig.json compilerOptions.target enum doesn’t include 'es2025' as a valid option.*

 * created by **Abrifq**
 * [today](https://github.com/microsoft/TypeScript/issues/63379#issuecomment-4215183885) **MartinJohns** noted the option was missing in jsconfig
 * **RyanCavanaugh** added label `Docs`

### [Issue microsoft/TypeScript#63380](https://github.com/microsoft/TypeScript/issues/63380) (Open, `Bug`, `Domain: check: Type Inference`)

**Wrong inference for defaulted generic in nested call**

*TypeScript fails to infer the correct return type for nested calls to a generic function with a default type parameter.*

 * created by **TurtIeSocks**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63381](https://github.com/microsoft/TypeScript/issues/63381) (Open, `Needs More Info`)

**ESM strict imports mode option to moduleResolution bundler**

*Add a tsconfig option to enforce including file extensions on ESM imports when using bundler moduleResolution*

 * created by **paztis**

### [Issue microsoft/TypeScript#63382](https://github.com/microsoft/TypeScript/issues/63382) (Open, **mjbvz**)

**Typescript Server syntax highlighting bug: introduced by recent update**

*The latest VS Code update causes the TypeScript server to ignore custom global types, resulting in red syntax errors.*

 * created by **kidCaulfield**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63382#issuecomment-4218277248) **RedCMD** said "typeRoots or types?"
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/63382#issuecomment-4218277267) **kidCaulfield** clarified that typeRoots includes the global types folder, explained the docs distinction with types, and reported that switching to types reintroduced the VS Code syntax highlighting issue after restarting the TS server

### [Issue microsoft/TypeScript#63384](https://github.com/microsoft/TypeScript/issues/63384) (Closed, `Won't Fix`, `7.0 LS Migration`)

**JS and TS Tasking long time to start which make the save of tsx files slower\.**

*Delays in the JavaScript and TypeScript formatter startup are slowing or blocking TSX file saves.*

 * created by **flexdevguy**
 * **vs-code-engineering[bot]** assigned to **mjbvz**

