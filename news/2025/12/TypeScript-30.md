# Report for 2025-12-30 (Tuesday, December 30th, 2025)

7 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @ackvf provided repro steps as requested in [microsoft/TypeScript#29732](https://github.com/microsoft/TypeScript/issues/29732#issuecomment-3702212787)

## Activity Summary

### [Issue microsoft/TypeScript#16665](https://github.com/microsoft/TypeScript/issues/16665) (Open, `Suggestion`, `Awaiting More Feedback`, `VS Code Tracked`, `Domain: LS: Signature Help`, `Domain: LS: Quick Info`)

**Include Default Parameter Values in Signature Help **

*Enhance TypeScript’s signature help to display default values for optional function parameters.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/16665#issuecomment-3313901426) **frostius** clarified that complexity arose from TypeScript and requested not to omit information in hover comments
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/16665#issuecomment-3402358452) **meduzen** showcased screenshots illustrating function definition, autocompletion, and flyout tooltips
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/16665#issuecomment-3403004341) **alystair** said "@RyanCavanaugh see updates above, hopefully this simplifies things significantly on your end."
 * [later](https://github.com/microsoft/TypeScript/issues/16665#issuecomment-3702408931) **stevenvachon** said "Flow might've been the better choice."

### [Issue microsoft/TypeScript#29732](https://github.com/microsoft/TypeScript/issues/29732) (Open, `Suggestion`, `In Discussion`)

**Overload gets lost in mapped type with conditional type**

*Conditional mapped types lose method overloads when wrapping return types in Promise, causing argument count errors.*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/29732#issuecomment-2551503319) **Khez** described failing overload resolution for string.split with a union type and provided reduced code examples
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/29732#issuecomment-2558051985) **LukeAbby** described a TypeScript type to extract function overload signatures and shared code and a playground link
 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/29732#issuecomment-3368463242) **thakyZ** provided a TypeScript utility type for extracting parameters from overloaded functions and demonstrated its use with JQuery<HTMLElement>.text
 * [later](https://github.com/microsoft/TypeScript/issues/29732#issuecomment-3702212787) **ackvf** demonstrated an issue with overloaded function parameter inference in TypeScript using a code snippet and Playground link

### [Issue microsoft/TypeScript#62933](https://github.com/microsoft/TypeScript/issues/62933) (Open, `Bug`)

**Maximum call stack size exceeded in isTypeAssignableTo when using recursive template literal types in a generic context**

*Using recursive template literal types inside a generic context causes checker.isTypeAssignableTo to exceed the maximum call stack size.*

 * created by **mdm317**

### [PR microsoft/TypeScript#62934](https://github.com/microsoft/TypeScript/pull/62934) (Open, `For Backlog Bug`)

**Add failing test for variance measurement with nested generic type aliases**

*A failing test reveals TypeScript miscomputes deeply nested generic type alias variance as independent instead of covariant, enabling unsound assignments.*

 * created by **eL1fe**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62934#issuecomment-3700408996) **eL1fe** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#62935](https://github.com/microsoft/TypeScript/pull/62935) (Open, `For Backlog Bug`)

**Fix JSDoc @type completion inside function argument**

*JSDoc @type completions for inline function parameters fail because the logic doesn't detect comments and treats tags as unattached.*

 * created by **caverac**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62935#issuecomment-3701992377) **caverac** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#62936](https://github.com/microsoft/TypeScript/issues/62936) (Closed)

**reference incorrectly resolved with var declared in catch block with same name as catch parameter**

*TypeScript incorrectly resolves and type-checks an inner var that shadows a catch parameter in the same catch block.*

 * created by **camc314**
 * [later](https://github.com/microsoft/TypeScript/issues/62936#issuecomment-3702230754) **camc314** said "Hmm I think TS is correct here, actually, ignore me 🙂 ."
 * (later) **camc314** closed the issue

### [Issue microsoft/TypeScript#62937](https://github.com/microsoft/TypeScript/issues/62937) (Closed, `Not a Defect`)

**Crash: RangeError: Invalid string length in addSpans when evaluating deeply recursive Template Literal Types with \-\-strict enabled**

*TypeScript compiler crashes with a RangeError on deeply recursive template literal type evaluation when strict mode is enabled*

 * created by **na7ure-a**

