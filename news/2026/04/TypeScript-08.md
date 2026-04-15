# Report for 2026-04-08 (Wednesday, April 8th, 2026)

11 different users commented on 23 different issues.

## Recommended Actions

 * Response Recommended
    * @juhort asked @RyanCavanaugh for an example where doCall and overload would differ in [microsoft/TypeScript#32164](https://github.com/microsoft/TypeScript/issues/32164#issuecomment-4213346370)
    * @posva provided an example of oxc output as demonstration in [microsoft/TypeScript#58944](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-4213203205)
    * @marqdouj asked someone to pass on feedback to the Azure Maps SDK team in [microsoft/TypeScript#63375](https://github.com/microsoft/TypeScript/issues/63375#issuecomment-4209974913)
    * @RedCMD asked whether to use typeRoots or types in [microsoft/TypeScript#63382](https://github.com/microsoft/TypeScript/issues/63382#issuecomment-4218277248)

## Activity Summary

### [Issue microsoft/TypeScript#32164](https://github.com/microsoft/TypeScript/issues/32164) (Closed, `Design Limitation`)

**Parameter type interface for overloaded functions as union type**

*Propose that Parameters<T> return a union of all parameter types from overloaded function signatures, not just the last.*

 * [40 weeks ago](https://github.com/microsoft/TypeScript/issues/32164#issuecomment-3014943371) **jcalz** said "Sure, but isn't it really supposed to be (func: T, ...args: ParametersX) instead?"
 * [40 weeks ago](https://github.com/microsoft/TypeScript/issues/32164#issuecomment-3014944366) **RyanCavanaugh** said "That won't have the same semantics as overloads anyway, since overloads have ordering behavior but tuples don't"
 * [40 weeks ago](https://github.com/microsoft/TypeScript/issues/32164#issuecomment-3021549638) **Tyler-Murphy** thanked RyanCavanaugh and asked about potential dangers of the proposed overload implementation and if the restriction aims to prevent misuse of doCall with bad types
 * [later](https://github.com/microsoft/TypeScript/issues/32164#issuecomment-4213346370) **juhort** demonstrated a tuple-based overload invocation example showing contextual typing issues and asked @RyanCavanaugh for an example where doCall and overload would differ

### [Issue microsoft/TypeScript#58944](https://github.com/microsoft/TypeScript/issues/58944) (Open, `Discussion`)

**Isolated Declarations in TS 5\.5: State of the feature**

*A status update on TypeScript 5.5’s experimental --isolatedDeclarations flag, outlining its current stability, effects, and usage guidance.*

 * [33 weeks ago](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-3197456987) **dynst** suggested adding documentation for the feature and noted issues with number and RegExp literal type inference
 * [17 weeks ago](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-3622389790) **XantreDev** asked what constituted the simple case for isolatedDeclarations and why RegExp literals were excluded from AST-level inference
 * [17 weeks ago](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-3628489902) **RyanCavanaugh** explained that the type name RegExp could be locally shadowed and that always emitting globalThis.RegExp would be correct but ugly
 * [later](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-4213203205) **posva** seconded enforcing isolatedDeclarations only for package-level exported bindings, explained that TS type inference is important for public library APIs, and noted that oxc can output these types with a playground link

### [Issue microsoft/TypeScript#63342](https://github.com/microsoft/TypeScript/issues/63342) (Open, `Experimentation Needed`, `Domain: check: Big Unions`, `Possible Improvement`)

**type checking complexity with multiple template literals in unions**

*TypeScript’s type checking time scales exponentially with unions of template literal types in dynamic route definitions.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63342#issuecomment-4197960180) **eps1lon** said "There's a Go port: https://github.com/microsoft/typescript-go/pull/3331"
 * (yesterday) **RyanCavanaugh** added labels `Experimentation Needed`, `Possible Improvement`
 * **RyanCavanaugh** added label `Domain: check: Big Unions`

### [Issue microsoft/TypeScript#63373](https://github.com/microsoft/TypeScript/issues/63373) (Open, `External`)

**tsserver hangs in Yarn PnP projects — incorrect directory watcher due to unchecked indexOf returning \-1**

*tsserver in Yarn PnP projects hangs because unchecked indexOf on non-node_modules paths produces incorrect directory watcher paths.*

 * created by **sebaspf**
 * [today](https://github.com/microsoft/TypeScript/issues/63373#issuecomment-4208290436) **RyanCavanaugh** provided an auto-generated analysis listing similar issues to help get started

### [Issue microsoft/TypeScript#63375](https://github.com/microsoft/TypeScript/issues/63375) (Closed, `Working as Intended`)

**Version 6\.0\.3 Breaks Azure Maps SDK 3\.7\.2**

*TypeScript 6.0.3 rejects Azure Maps SDK 3.7.2’s module-based namespace declaration with an error instead of a warning.*

 * created by **marqdouj**
 * [today](https://github.com/microsoft/TypeScript/issues/63375#issuecomment-4208981761) **MartinJohns** clarified that the deprecation is intentional and that TypeScript does not have warnings
 * **RyanCavanaugh** added label `Working as Intended`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63375#issuecomment-4209974913) **marqdouj** thanked the team and asked to forward feedback to the Azure Maps SDK team

### [Issue microsoft/TypeScript#63376](https://github.com/microsoft/TypeScript/issues/63376) (Open, `Fixed`)

**TS2589 regression in 6\.0: implements without type parameters causes excessive type instantiation when property uses concrete generic type**

*TypeScript 6.0 regression triggers TS2589 excessive type instantiation when implementing a generic interface without type parameters for concrete-generic properties.*

 * created by **julienw**
 * [today](https://github.com/microsoft/TypeScript/issues/63376#issuecomment-4210350123) **RyanCavanaugh** provided a minimal reproduction snippet with key ingredients to trigger the instantiation bug
 * [today](https://github.com/microsoft/TypeScript/issues/63376#issuecomment-4210398776) **RyanCavanaugh** said "Bisects to #62604"
 * [today](https://github.com/microsoft/TypeScript/issues/63376#issuecomment-4210461429) **RyanCavanaugh** explained that adding variance annotations prevented the problem, noted it didn't repro in TS 7, and asserted it wouldn't meet the 6.0 patch bar
 * [today](https://github.com/microsoft/TypeScript/issues/63376#issuecomment-4210463969) **RyanCavanaugh** provided a smaller reproduction snippet demonstrating the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63376#issuecomment-4212933992) **julienw** thanked the reviewer and mentioned that Claude had helped compare type instantiations with and without explicitly specifying the generic parameter

### [Issue microsoft/TypeScript#63377](https://github.com/microsoft/TypeScript/issues/63377) (Closed, `Question`)

**TS doesn't properly infer generic callback \`\<T\>\(x: X\<T\>\) =\> T\` when providing \`\(x\) =\> new T\(\)\` \(parameter defined without type\)**

*TypeScript does not infer a generic callback’s type when its parameter is untyped, resulting in any instead.*

 * created by **denis-migdal**
 * [later](https://github.com/microsoft/TypeScript/issues/63377#issuecomment-4212713074) **denis-migdal** suggested assuming the callback had a ControllerProvider shape and using single or two-pass type inference guided by error feedback

### [Issue microsoft/TypeScript#63378](https://github.com/microsoft/TypeScript/issues/63378) (Open, `Domain: check: Type Inference`, `Possible Improvement`)

**Object properties are inferred in the wrong order: should infer properties with \`NoInfer\<T\>\` AFTER properties with \`T\`**

*TypeScript infers object properties with NoInfer<T> before plain generics rather than after, causing inconsistent inference order.*

 * created by **denis-migdal**

### [Issue microsoft/TypeScript#63379](https://github.com/microsoft/TypeScript/issues/63379) (Open, `Docs`)

**\`es2025\` is not a valid enum option for \`jsconfig\.json\`'s \`compilerOptions\.target\` enum**

*The JSON schema for jsconfig.json/tsconfig.json compilerOptions.target enum doesn’t include 'es2025' as a valid option.*

 * created by **Abrifq**
 * [later](https://github.com/microsoft/TypeScript/issues/63379#issuecomment-4215183885) **MartinJohns** noted the option was missing in jsconfig

### [Issue microsoft/TypeScript#63382](https://github.com/microsoft/TypeScript/issues/63382) (Open, **mjbvz**)

**Typescript Server syntax highlighting bug: introduced by recent update**

*The latest VS Code update causes the TypeScript server to ignore custom global types, resulting in red syntax errors.*

 * created by **kidCaulfield**
 * [today](https://github.com/microsoft/TypeScript/issues/63382#issuecomment-4218277248) **RedCMD** said "typeRoots or types?"
 * **vs-code-engineering[bot]** assigned to **mjbvz**

### [Issue microsoft/TypeScript#63383](https://github.com/microsoft/TypeScript/issues/63383) (Closed, `Working as Intended`, **mjbvz**)

**Typescript 'rootDir' error**

*VSCode 1.114+ incorrectly reports TypeScript rootDir errors in a multi-package monorepo configuration despite successful CLI compilation*

 * created by **m-hall**
 * **vs-code-engineering[bot]** assigned to **mjbvz**

