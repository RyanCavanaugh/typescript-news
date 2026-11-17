# Report for 2026-11-10 (Tuesday, November 10th, 2026)

18 different users commented on 844 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#10077](https://github.com/microsoft/TypeScript/issues/10077) (Open, `Suggestion`, `Effort: Difficult`)

**Suggestion: output fewer errors for incorrectly implemented interface**

*Reduce redundant property-missing errors when a class incorrectly implements an interface and the missing member is subsequently accessed.*

 * [10.2 years ago](https://github.com/microsoft/TypeScript/issues/10077#issuecomment-241579997) **RyanCavanaugh** stated that PRs would be accepted only if the change could be implemented very simply or cheaply
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#10126](https://github.com/microsoft/TypeScript/issues/10126) (Open, `Suggestion`, `Domain: Formatter`, `VS Code Tracked`)

**Formatter fails to format uglified files**

*VS Code’s formatter only adds spacing and fails to properly format JavaScript files minified by UglifyJS.*

 * [9.6 years ago](https://github.com/microsoft/TypeScript/issues/10126#issuecomment-291354163) **sdwarwick** asked whether the issue matched #23829 and whether code highlighting or equivalent command-line functionality was planned or available
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#10203](https://github.com/microsoft/TypeScript/issues/10203) (Open, `Suggestion`, `Effort: Moderate`, `Domain: Error Messages`, `Experience Enhancement`)

**Error message for invalid string literal type could be improved**

*Improve invalid string literal argument errors to report all accepted overload values instead of only the last overload’s type.*

 * (7.6 years ago) **RyanCavanaugh** added label `Experience Enhancement`, removed label `Needs Proposal`, and set milestone to `Backlog`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#10285](https://github.com/microsoft/TypeScript/issues/10285) (Open, `Suggestion`, `Domain: lib.d.ts`)

**Scope of this is lost when passing a member function to setInterval**

*Passing a class method directly to setInterval loses its this context, causing member access to be undefined instead of referencing the instance.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/10285#issuecomment-5492446141) **LeonxLJX** said "I'd like to take this one (Scope of this is lost when passing a member function to setI). I'll look into the root cause and follow up with a PR. (claiming via @LeonxLJX)"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/10285#issuecomment-5492965062) **LeonxLJX** said "I'd like to take this one (Scope of this is lost when passing a member function to setI). I'll dig into the root cause and follow up with a PR shortly. (claiming via @LeonxLJX)"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/10285#issuecomment-5492966388) **LeonxLJX** said "I'd like to take this one (Scope of this is lost when passing a member function to setI). I'll look into the root cause and follow up with a PR. (claiming via @LeonxLJX)"
 * (today) **RyanCavanaugh** removed labels `Help Wanted`, `Good First Issue`

### [Issue microsoft/TypeScript#10383](https://github.com/microsoft/TypeScript/issues/10383) (Open, `Suggestion`)

**Comments on inner properties are stripped**

*Comments on nested object properties are omitted from generated declaration files, with a request for separate comment-removal controls for declarations and JavaScript.*

 * [10.2 years ago](https://github.com/microsoft/TypeScript/issues/10383#issuecomment-240496725) **mhegazy** welcomed PRs and indicated that the change belonged in the typewriter responsible for serializing types
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#10498](https://github.com/microsoft/TypeScript/issues/10498) (Open, `Suggestion`, `Experience Enhancement`)

**Template string downlevel to ES5 escapes more Unicode characters than necessary**

*TypeScript 1.8.10 unnecessarily Unicode-escapes non-ASCII characters when downleveling template strings to ES5.*

 * (4.9 years ago) **RyanCavanaugh** added labels `Experience Enhancement`, `Suggestion`, and removed label `Bug`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#1057](https://github.com/microsoft/TypeScript/issues/1057) (Open, `Effort: Moderate`, `Domain: Error Messages`, `Experience Enhancement`)

**Gracefully handle template literal properties in the parser**

*Improve parser error recovery for template literal properties in object literals, reporting the actual missing separator or syntax error.*

 * (6.7 years ago) **DanielRosenwasser** added labels `Effort: Moderate`, `Experience Enhancement`, and removed label `Suggestion`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#10886](https://github.com/microsoft/TypeScript/issues/10886) (Open, `Suggestion`, `Domain: lib.d.ts`)

**Array inheritance in ES6 declaration file \(lib\.es6\.d\.ts\)**

*Update lib.es6.d.ts to accurately type Array subclassing, including inherited method returns, generic map results, static constructors, and Symbol.species.*

 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/10886#issuecomment-3949053605) **Bertie690** asked whether the feature was still desired and whether they could submit a PR implementing the standard Array methods
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#11167](https://github.com/microsoft/TypeScript/issues/11167) (Open, `Bug`, `Domain: Parser`)

**Line break in module declaration causes compile time error**

*A line break between `declare module` and the module name causes a compile-time error, contrary to expected syntax behavior.*

 * (7.6 years ago) **RyanCavanaugh** added label `Domain: Parser`, set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#11434](https://github.com/microsoft/TypeScript/issues/11434) (Open, `Suggestion`, `Committed`, `Effort: Moderate`)

**Move away from Classic module resolution as default for all module kinds**

*Consider replacing Classic module resolution with Node resolution by default for non-CommonJS targets after assessing compatibility, impact, and breakage.*

 * **DanielRosenwasser** added label `help wanted`
 * [6.3 years ago](https://github.com/microsoft/TypeScript/issues/11434#issuecomment-656869557) **DanielRosenwasser** said "If someone wants to send a PR, I think that the hardest part would be updating the tests."
 * [4.4 years ago](https://github.com/microsoft/TypeScript/issues/11434#issuecomment-1135043736) **DanielRosenwasser** said "This is probably no longer the solution we would want give the fact that there are 2 new module modes for ESM in Node.js, and Deno has its own rules."
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#11500](https://github.com/microsoft/TypeScript/issues/11500) (Open, `Suggestion`, `VS Code Tracked`, `Domain: JSDoc`)

**Support formatting JSDoc comments**

*Add support for formatting JSDoc comments by normalizing indentation, spacing, and parameter annotations.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/11500#issuecomment-1742856285) **negativems** said "Is there any VSCode extension for this while we continue waiting for it to be implemented?"
 * [3 years ago](https://github.com/microsoft/TypeScript/issues/11500#issuecomment-1748282102) **HolgerJeromin** said "You could try prettier and/or eslint jsdoc plugin."
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#11504](https://github.com/microsoft/TypeScript/issues/11504) (Open, `Suggestion`, `Domain: API`)

**Go\-to\-Implementation & class names**

*Request to include implementing class names in tsserver’s implementation results to improve Eclipse’s Go-to-Implementation feature.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#11648](https://github.com/microsoft/TypeScript/issues/11648) (Open, `Suggestion`, `Effort: Moderate`, `Domain: Error Messages`)

**Give better error messages when reserved names are used for binding identifiers**

*Improve error messages when reserved names are used as binding identifiers in destructuring declarations.*

 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [6.2 years ago](https://github.com/microsoft/TypeScript/issues/11648#issuecomment-672161227) **Dean-NC** shared an image without additional context
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#11779](https://github.com/microsoft/TypeScript/issues/11779) (Open, `Suggestion`)

**Unoptimized destructuring compilation**

*TypeScript 2.0 generates an unnecessary temporary array when compiling array destructuring inside loops, reducing runtime efficiency.*

 * [10 years ago](https://github.com/microsoft/TypeScript/issues/11779#issuecomment-260504271) **RyanCavanaugh** welcomed pull requests to emit optimized code when the initializer was a sufficiently long array literal
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#11781](https://github.com/microsoft/TypeScript/issues/11781) (Open, `Suggestion`, `Domain: lib.d.ts`)

**Service Worker typings**

*Request to include built-in TypeScript definitions for Service Worker APIs.*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/11781#issuecomment-3377075608) **FusillyCode** explained that the referenced solutions broke Firefox compatibility for ServiceWorker scripts using imports or exports, and provided TypeScript configuration and code workarounds
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/11781#issuecomment-4199635479) **vadimmos** said "Is there any progress on this issue? Are developers still doomed to write ServiceWorker code with one eye on the documentation, without the ability to rely on autocompletion and type checking tools?"
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/11781#issuecomment-4454858857) **supernovus** asked whether TypeScript would accept and merge a separate Service Worker library definition, criticizing the longstanding lack of proper support and resulting workarounds
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#11859](https://github.com/microsoft/TypeScript/issues/11859) (Open, `Suggestion`, `In Discussion`, `VS Code Tracked`, `Domain: JSDoc`)

**JSDoc support for destructured parameters**

*Add JSDoc support for documenting individual properties of destructured function parameters and providing IntelliSense descriptions.*

 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/11859#issuecomment-886904818) **MarcosAtApprentice** said "This seems related to this weird issue I'm having with type inference on object destructuring. Posted about it here: https://github.com/microsoft/TypeScript/pull/44730#issuecomment-886865460"
 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/11859#issuecomment-1208601482) **PoulBak** said "Is JSDoc dead? This has not been fixed in almost 6 years."
 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/11859#issuecomment-1829536217) **steida** noted that JSDoc should not document TypeScript code, while Markdown and @link remain usable but @param and @example do not
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#1213](https://github.com/microsoft/TypeScript/issues/1213) (Open, `Suggestion`)

**Allow classes to be parametric in other parametric classes**

*Proposes higher-kinded type parameters so interfaces and typedefs can abstract over generic types and compose parametric types.*

 * [33 weeks ago](https://github.com/microsoft/TypeScript/issues/1213#issuecomment-4109921837) **laverdet** said "I don't think it is a software problem. It's a problem of research and consensus."
 * [33 weeks ago](https://github.com/microsoft/TypeScript/issues/1213#issuecomment-4110201752) **gund** mocked the idea of delegating research, consensus, and software design decisions entirely to AI
 * [33 weeks ago](https://github.com/microsoft/TypeScript/issues/1213#issuecomment-4111405670) **exoRift** said "At that point, we don't need this feature because AI can just cast as any and we should trust it to be right because AI should be making the decisions for us :D"
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#12400](https://github.com/microsoft/TypeScript/issues/12400) (Open, `Suggestion`, `Committed`)

**Treating \`undefined\` parameters as optional**

*Request guidance on treating `undefined` generic parameters as optional while preserving type-guard narrowing for required properties.*

 * **RyanCavanaugh** added label `Help Wanted`
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/12400#issuecomment-3279411135) **phaux** provided a TypeScript workaround for making a tuple element optional when its type is nullable
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/12400#issuecomment-3366422369) **zeorin** adapted the approach to support an arbitrary number of optional arguments and provided TypeScript examples with a Playground link
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#12405](https://github.com/microsoft/TypeScript/issues/12405) (Open, `Suggestion`)

**error TS5053: Option 'declarationDir' cannot be specified with option 'outFile'\.**

*Request to allow declarationDir with outFile so generated declaration files can be emitted separately without maintaining duplicate TypeScript configurations.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#12539](https://github.com/microsoft/TypeScript/issues/12539) (Open, `Suggestion`, `Domain: Formatter`, `VS Code Tracked`)

**Provide Format Options for JSX/TSX End of Tag Placement**

*Add formatting options to control JSX/TSX closing angle-bracket placement, including consolidating brackets with tags when appropriate.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#12681](https://github.com/microsoft/TypeScript/issues/12681) (Open, `Suggestion`, `VS Code Tracked`, `Domain: JSDoc`, `Domain: JavaScript`, `Has Repro`)

**Support @class in JSDoc**

*Support recognizing JSDoc’s @class annotation so constructor functions provide correct inferred types instead of any.*

 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/12681#issuecomment-1987278955) **rubiesonthesky** reported that the issue remained reproducible in the playground despite VS Code displaying the correct type, and provided a TypeScript repro with a Workbench link
 * **typescript-bot** added label `Has Repro`
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/12681#issuecomment-1987829896) **typescript-bot** reported that the nightly TypeScript repro failed because the deprecated `moduleResolution=node10` option triggered TS5107
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#12824](https://github.com/microsoft/TypeScript/issues/12824) (Open, `Suggestion`)

**How tsconfig exclude pattern should actually work**

*Clarify and correct TypeScript tsconfig exclude glob behavior, especially recursive node_modules patterns and default exclusions.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#12944](https://github.com/microsoft/TypeScript/issues/12944) (Open, `Suggestion`)

**Type Inference in for\.\.\. in combined with typeof**

*TypeScript 2.1 incorrectly rejects narrowing indexed properties with typeof inside for...in loops, breaking method binding code that worked in 2.0.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#13627](https://github.com/microsoft/TypeScript/issues/13627) (Open, `Docs`)

**\[BUG\] Docs say es6 modules can't export class objects, but that's not true\.**

*Documentation incorrectly claims ES6 modules cannot export classes, despite valid default class exports being supported.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#13793](https://github.com/microsoft/TypeScript/issues/13793) (Open, `Suggestion`, `Domain: API`, `Experience Enhancement`)

**Expose ts\.matchFiles as public API to make implementing readDirectory easier\.**

*Expose TypeScript’s `matchFiles` helper or provide filesystem-entry support so custom virtualized hosts can implement `readDirectory` consistently with `tsc`.*

 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [6.3 years ago](https://github.com/microsoft/TypeScript/issues/13793#issuecomment-648673409) **usergenic** said "I'm currently having to implement a readDirectory etc and I was really hoping this had been addressed 3 years ago when brought up."
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#13855](https://github.com/microsoft/TypeScript/issues/13855) (Open, `Bug`, `Domain: JSDoc`)

**Doc comment applied to all components of dotted namespace declaration**

*Doc comments on dotted namespace declarations incorrectly appear in quick info and completion for both outer and innermost namespaces.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/13855#issuecomment-1984835537) **RyanCavanaugh** provided a passing fourslash testcase that exposed an incorrect quick-info result for dotted namespace declarations and explained that binder desugaring obscured the declaration’s full name, complicating disambiguation
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#14211](https://github.com/microsoft/TypeScript/issues/14211) (Open, `Suggestion`)

**Suggestion: tsc should display a one line summary**

*Suggests that tsc display a concise one-line compilation summary, including error count and potentially compilation time.*

 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [6.4 years ago](https://github.com/microsoft/TypeScript/issues/14211#issuecomment-637099598) **kumar303** requested an option to show an error summary without enabling color formatting, so output could be piped to a log file
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#14802](https://github.com/microsoft/TypeScript/issues/14802) (Open, `Suggestion`, `Effort: Moderate`, `Experience Enhancement`)

**Improve feedback for abstract class instantiation error messages**

*Improve abstract class instantiation errors by identifying whether the class is declared abstract or which abstract methods remain unimplemented.*

 * (7.6 years ago) **RyanCavanaugh** added label `Experience Enhancement`, set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#14877](https://github.com/microsoft/TypeScript/issues/14877) (Open, `Bug`, `Domain: lib.d.ts`)

**Unable to access ServiceWorkerGlobalScope via \`self\.\`**

*`lib.webworker.d.ts` types `self` as `WorkerGlobalScope`, preventing access to ServiceWorkerGlobalScope properties such as `clients`.*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/14877#issuecomment-2953809333) **saschanaz** clarified that the core issue was using `lib=serviceworker` instead of `webworker`, noted that issue #1498 would not fix it, and suggested closing this issue
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/14877#issuecomment-3221359143) **SirzBenjie** questioned why `lib=serviceworker` was unsupported and what distinction existed between `webworker` and service workers
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/14877#issuecomment-3297063234) **falco467** explained that service workers are a type of web worker but use a distinct global scope and therefore require separate types for their APIs
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#14994](https://github.com/microsoft/TypeScript/issues/14994) (Open, `Suggestion`, `Domain: Formatter`, `VS Code Tracked`)

**Control application of insertSpaceAfterOpeningAndBeforeClosingNonemptyBrackets for Array Literal vs Array Access Expression**

*Request separate formatting controls for spaces inside array literals versus array access expressions.*

 * [9 years ago](https://github.com/microsoft/TypeScript/issues/14994#issuecomment-339904757) **atian25** said "any plan on this? @mjbvz "
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#15402](https://github.com/microsoft/TypeScript/issues/15402) (Open, `Suggestion`, `Domain: lib.d.ts`)

**Suggestion: a built\-in TypedArray interface**

*Add a built-in TypedArray interface as a common base for typed array types and enable simpler type-safe declarations.*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/15402#issuecomment-2596173471) **kyr0** reported that published TypedArray constructor types omitted the optional byte-length argument and provided a custom constructor type workaround
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/15402#issuecomment-3148287607) **BlackAsLight** said "After finding myself needing this type today, I discover others have been wanting it for 8 years. "
 * **jakebailey** removed label `Fix Available`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#15506](https://github.com/microsoft/TypeScript/issues/15506) (Open, `Suggestion`)

**Flag boolean in comparison operator operands as errors**

*Report boolean operands used with comparison operators, such as `x > y`, as errors because the expression is likely suspicious.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/15506#issuecomment-5492445474) **LeonxLJX** said "I'd like to take this one (Flag boolean in comparison operator operands as errors). I'll look into the root cause and follow up with a PR. (claiming via @LeonxLJX)"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/15506#issuecomment-5492964278) **LeonxLJX** said "I'd like to take this one (Flag boolean in comparison operator operands as errors). I'll dig into the root cause and follow up with a PR shortly. (claiming via @LeonxLJX)"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/15506#issuecomment-5492965723) **LeonxLJX** said "I'd like to take this one (Flag boolean in comparison operator operands as errors). I'll look into the root cause and follow up with a PR. (claiming via @LeonxLJX)"
 * (today) **RyanCavanaugh** removed labels `Help Wanted`, `Good First Issue`

### [Issue microsoft/TypeScript#15655](https://github.com/microsoft/TypeScript/issues/15655) (Open, `Bug`, `Domain: check: Control Flow`)

**Noncrashing property access through non\-null assertion operator should narrow that property to NonNullable**

*Non-null assertions on nested optional properties do not narrow the asserted property or its parent object to non-nullable types.*

 * (5.3 years ago) **RyanCavanaugh** added labels `help wanted`, `Domain: Control Flow`, and set milestone to `Backlog`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#1631](https://github.com/microsoft/TypeScript/issues/1631) (Open, `Suggestion`, `Domain: API`)

**QuickInfo shows icon and name of item type**

*Remove redundant item type names from QuickInfo when the corresponding type icons already identify them.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#17088](https://github.com/microsoft/TypeScript/issues/17088) (Open, `Suggestion`, `Effort: Moderate`, `Awaiting More Feedback`)

**Mixed es5/es2015 code with mixin classes causes runtime errors**

*Mixing ES5-targeted mixin classes with ES2015+ classes causes runtime errors when the generated subclass invokes the native class without `new`.*

 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/17088#issuecomment-1371965851) **kungfooman** reported being unable to reproduce the error and shared a TypeScript Playground link
 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/17088#issuecomment-1372597900) **rbuckton** noted that the issue still existed, outlined the required helper and tslib changes for a fix, and asked whether to close it, implement the fix, or gate it behind a flag
 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/17088#issuecomment-1518985631) **satanTime** provided reproduction examples and requested a flag
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#17630](https://github.com/microsoft/TypeScript/issues/17630) (Open, `Suggestion`, `Domain: API`, `VS Code Tracked`)

**Feedback to improve compileOnSave with tsserver\.**

*Improve tsserver compile-on-save commands by reporting excluded files, ignoring declaration files, and returning diagnostics and emitted file paths.*

 * **mhegazy** added label `Suggestion`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#18013](https://github.com/microsoft/TypeScript/issues/18013) (Open, `Suggestion`, `Domain: API`)

**Suggestion: Change \`Diagnostic\.file\` to be \`SourceFileLike\` instead of \`SourceFile\`\.**

*Change `Diagnostic.file` from `SourceFile` to a narrower interface describing only the requirements plugins need to report diagnostics.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#18283](https://github.com/microsoft/TypeScript/issues/18283) (Open, `Suggestion`, `Committed`)

**Allow class inheritance in ambient contexts, even with a base private constructor**

*Allow classes in ambient declarations to extend classes with private constructors while preserving non-constructibility and nominal typing.*

 * [9 years ago](https://github.com/microsoft/TypeScript/issues/18283#issuecomment-336946910) **RyanCavanaugh** said "@zspitz https://github.com/Microsoft/TypeScript/wiki/FAQ#what-do-the-labels-on-these-issues-mean"
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#18319](https://github.com/microsoft/TypeScript/issues/18319) (Open, `Suggestion`)

**Surprising \`Not all code paths return a value\`**

*TypeScript incorrectly reports missing returns for async functions contextually typed as promises of a union including void.*

 * [6.2 years ago](https://github.com/microsoft/TypeScript/issues/18319#issuecomment-675691415) **wycats** said "@mhegazy since some time has gone by: is this still "PRs welcome"?"
 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/18319#issuecomment-803209050) **rohitkhurmi095** suggested setting `noImplicitReturns` to `false` in `compilerOptions`
 * [4.5 years ago](https://github.com/microsoft/TypeScript/issues/18319#issuecomment-1092548771) **Mahi** questioned why a `void` function without an explicit return triggered the implicit-return warning and reported that the behavior appeared buggy when an optional `void` return type was used
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#18433](https://github.com/microsoft/TypeScript/issues/18433) (Open, `Domain: lib.d.ts`, `Cursed?`, `Possible Improvement`)

**Dangerous "name" \(and potentially others\) global **

*Global DOM properties such as `name` mask undeclared local variables, prompting removal or opt-in inclusion of these globals in TypeScript.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/18433#issuecomment-5492444910) **LeonxLJX** said "I'd like to take this one (Dangerous "name" (and potentially others) global). I'll look into the root cause and follow up with a PR. (claiming via @LeonxLJX)"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/18433#issuecomment-5492963547) **LeonxLJX** said "I'd like to take this one (Dangerous "name" (and potentially others) global). I'll dig into the root cause and follow up with a PR shortly. (claiming via @LeonxLJX)"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/18433#issuecomment-5492964958) **LeonxLJX** said "I'd like to take this one (Dangerous "name" (and potentially others) global). I'll look into the root cause and follow up with a PR. (claiming via @LeonxLJX)"
 * (today) **RyanCavanaugh** added labels `Cursed?`, `Possible Improvement`, and removed labels `Suggestion`, `Help Wanted`, `Committed`, `Good First Issue`

### [Issue microsoft/TypeScript#18482](https://github.com/microsoft/TypeScript/issues/18482) (Open, `Suggestion`, `Revisit`, `Domain: lib.d.ts`)

**Add WebVR API to lib\.d\.ts**

*Add WebVR API type definitions to lib.d.ts based on the documented browser interfaces.*

 * [9.1 years ago](https://github.com/microsoft/TypeScript/issues/18482#issuecomment-330701662) **mhegazy** said "Thanks for the note. we should not include it in the default lib untill it makes WD stage."
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#1920](https://github.com/microsoft/TypeScript/issues/1920) (Open, `Bug`, `Domain: Something Else`)

**Report error if code precedes /// reference**

*Report an error and clarify the specification when code precedes a triple-slash reference, preventing referenced declarations from resolving.*

 * (7.6 years ago) **RyanCavanaugh** added label `Domain: Something Else`, set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#19299](https://github.com/microsoft/TypeScript/issues/19299) (Open, `Suggestion`, `Committed`, `Effort: Moderate`)

**Create Annex B lib target**

*Add a separate Annex B library target to isolate nonstandard browser declarations while allowing users to opt in when needed.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#19635](https://github.com/microsoft/TypeScript/issues/19635) (Open, `Bug`, `Domain: lib.d.ts`)

**Fix setTimeout/setInterval/setImmediate functions**

*Tighten TypeScript typings for setTimeout, setInterval, and setImmediate to correctly support optional timeouts and additional arguments.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [5.1 years ago](https://github.com/microsoft/TypeScript/issues/19635#issuecomment-910257767) **xaviergxf** said "Hi, no news about this?"
 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/19635#issuecomment-1459852189) **Jack-Works** reported that TypeScript failed to flag passing a callback with an incompatible signature to setTimeout, and provided a reproduction
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#19707](https://github.com/microsoft/TypeScript/issues/19707) (Open, `Suggestion`, `Revisit`, `Effort: Moderate`, `Experimentation Needed`)

**typeof Foo\['bar'\] has strange precedence**

*Clarify whether the surprising parsing of `typeof Foo['bar']` as `(typeof Foo)['bar']` is intentional.*

 * (5.3 years ago) **DanielRosenwasser** added label `help wanted`, and set milestone to `Backlog`
 * [4.8 years ago](https://github.com/microsoft/TypeScript/issues/19707#issuecomment-1018257496) **a-tarasyuk** explained that TypeQuery currently accepts only identifiers and qualified names because it is parsed as EntityName, and asked whether it should instead be parsed as an expression
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#19806](https://github.com/microsoft/TypeScript/issues/19806) (Open, `Suggestion`, `Domain: lib.d.ts`, `Experience Enhancement`)

**URLSearchParams/Headers constructor also receives iterables including Map**

*TypeScript incorrectly rejects iterable inputs, including Map instances, for URLSearchParams and Headers constructors.*

 * (7.6 years ago) **RyanCavanaugh** added label `Experience Enhancement`, removed label `In Discussion`, and set milestone to `Backlog`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#1988](https://github.com/microsoft/TypeScript/issues/1988) (Open, `Suggestion`)

**Support column limit in formatter**

*Add formatter configuration for maximum line width and insert breaks in overly wide, complex statements.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#1991](https://github.com/microsoft/TypeScript/issues/1991) (Open, `Suggestion`)

**Formatter: allow continuation indent different from nested indent**

*Allow the formatter to configure continuation indentation separately from nested code indentation to support Google’s JavaScript style guide.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#20183](https://github.com/microsoft/TypeScript/issues/20183) (Open, `Suggestion`, `Domain: LS: Completion Lists`, `VS Code Tracked`)

**Sort jsdoc parameter suggestions by argument position **

*Sort JSDoc @param completion suggestions by their corresponding function argument position rather than alphabetically.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/20183#issuecomment-5492444357) **LeonxLJX** said "I'd like to take this one (Sort jsdoc parameter suggestions by argument position). I'll look into the root cause and follow up with a PR. (claiming via @LeonxLJX)"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/20183#issuecomment-5492962744) **LeonxLJX** said "I'd like to take this one (Sort jsdoc parameter suggestions by argument position). I'll dig into the root cause and follow up with a PR shortly. (claiming via @LeonxLJX)"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/20183#issuecomment-5492964199) **LeonxLJX** said "I'd like to take this one (Sort jsdoc parameter suggestions by argument position). I'll look into the root cause and follow up with a PR. (claiming via @LeonxLJX)"
 * (today) **RyanCavanaugh** removed labels `Help Wanted`, `Good First Issue`

### [Issue microsoft/TypeScript#20846](https://github.com/microsoft/TypeScript/issues/20846) (Open, `Bug`, `Domain: lib.d.ts`)

**Typescript can't infer types when using Proxy**

*TypeScript fails to infer Proxy trap return types, providing incorrect IntelliSense and callable typings for proxied properties.*

 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/20846#issuecomment-1529904372) **AleksandrHovhannisyan** explained that the `set` trap loses the relationship between key and value types, causing type errors and allowing invalid key-value combinations that violate the `Data` constraints
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/20846#issuecomment-2832510545) **xanatos** said "Was this issue ever solved? I'm writing a proxy-to-array, and I'm having this problem :-)"
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/20846#issuecomment-3263248779) **pkit** criticized Microsoft for calling TypeScript a JavaScript superset while allegedly lacking Proxy support
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#21050](https://github.com/microsoft/TypeScript/issues/21050) (Open, `Suggestion`, `Domain: Error Messages`)

**Better error for semicolon after decorator**

*Improve the TypeScript error message for semicolons placed after decorators.*

 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [5.7 years ago](https://github.com/microsoft/TypeScript/issues/21050#issuecomment-784930447) **JoshuaKGoldberg** asked whether the issue was still considered help wanted and offered to resolve merge conflicts and update the abandoned pull request
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#21124](https://github.com/microsoft/TypeScript/issues/21124) (Open, `Suggestion`, `Domain: Formatter`)

**Formatter: Place JSX closing tag on new line**

*Formatter should move JSX closing tags onto a new line when the opening tag and content span multiple lines.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#21150](https://github.com/microsoft/TypeScript/issues/21150) (Open, `Suggestion`, `Domain: lib.d.ts`, `Experience Enhancement`)

**Provide lib for modern DOM**

*Add a TypeScript library option for modern or living-standard DOM APIs, including newer methods like `append`, `prepend`, and `replaceWith`.*

 * [8 years ago](https://github.com/microsoft/TypeScript/issues/21150#issuecomment-435426740) **chharvey** mentioned that TypeScript 3.1 added substantial DOM functionality, including new ChildNode and ParentNode methods, through programmatically generated definitions from the WHATWG DOM specification
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#21656](https://github.com/microsoft/TypeScript/issues/21656) (Open, `Suggestion`, `Domain: Error Messages`)

**esmoduleinterop: Improve error message when calling static method on class**

*Improve the error message for namespace-style imports that incorrectly call static methods on exported classes.*

 * [8.7 years ago](https://github.com/microsoft/TypeScript/issues/21656#issuecomment-363510843) **ghost** said "Similar for use in instanceof."
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#21736](https://github.com/microsoft/TypeScript/issues/21736) (Open, `Suggestion`, `Effort: Moderate`)

**Suggestion: case\-sensitive imports**

*Request for TypeScript to detect case-mismatched imports on case-insensitive systems to prevent runtime failures on case-sensitive servers.*

 * [5.4 years ago](https://github.com/microsoft/TypeScript/issues/21736#issuecomment-859193037) **vprasanth** mentioned that a low-priority PR had passed locally on macOS but failed in the container due to kebab-case issues, delaying resolution for over two months
 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/21736#issuecomment-1055417598) **MarekZhang** reported that `forceConsistentCasingInFileNames` failed to catch an incorrectly cased import from an external library, which worked on macOS but failed in Linux CI/CD
 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/21736#issuecomment-1381308027) **Inviz** asked why macOS path casing differed for the username directory and triggered the forceConsistentCasingInFileNames error
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#22203](https://github.com/microsoft/TypeScript/issues/22203) (Open, `Suggestion`, `Domain: Error Messages`)

**Improve error when parameter is missing a name**

*Improve the compiler error for optional properties in destructuring parameters to clearly identify the invalid `?` syntax.*

 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [4.8 years ago](https://github.com/microsoft/TypeScript/issues/22203#issuecomment-1001795170) **JoshuaKGoldberg** reported that the error differed for a constructor and provided a TypeScript playground link, code sample, and resulting diagnostics
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#22208](https://github.com/microsoft/TypeScript/issues/22208) (Open, `Suggestion`, `Committed`)

**foo\.ts is resolved before foo\.d\.ts even if the latter is in files\[\]**

*TypeScript resolves existing source files before explicitly included declaration files, causing separate compilation with rootDirs to fail or ignore --noResolve.*

 * **RyanCavanaugh** added to milestone `Future`
 * [6.6 years ago](https://github.com/microsoft/TypeScript/issues/22208#issuecomment-605370981) **rkirov** said "@RyanCavanaugh just to confirm on the "help wanted" and "committed" tags that is fixing it the way https://github.com/microsoft/TypeScript/issues/22208#issuecomment-376879283 is proposing?"
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/22208#issuecomment-611166967) **manughub** said "Here's a reproduction of the issue."
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#22378](https://github.com/microsoft/TypeScript/issues/22378) (Open, `Bug`, `Domain: lib.d.ts`)

**String\.replace does not accept string \| \(string, \.\.\.any\[\]\) =\> string replacer**

*TypeScript rejects a union of string and function replacers when passed to String.replace, despite both being valid overload arguments.*

 * [7.4 years ago](https://github.com/microsoft/TypeScript/issues/22378#issuecomment-496791381) **bluelovers** reported that TypeScript rejected a union of string and callback arguments for `String.replace`, despite accepting explicit casts and a custom overload using the same union, and suggested that the standard library needed a true union overload
 * [5.4 years ago](https://github.com/microsoft/TypeScript/issues/22378#issuecomment-847423358) **santi020k** suggested solving the problem with `toString()` and shared a Next.js router workaround
 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/22378#issuecomment-1191899737) **ghost** suggested replacing matches using `str.replace` with a regular expression and the replacer’s string representation
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#22446](https://github.com/microsoft/TypeScript/issues/22446) (Open, `Bug`, `Effort: Moderate`, `Domain: JavaScript`, `Experience Enhancement`, `Rescheduled`)

**Assignments to global objects in Javascript should be global declarations**

*JavaScript assignments to global, window, and this properties should create globally visible declarations without errors.*

 * (2.7 years ago) **RyanCavanaugh** added label `Domain: JavaScript`, set milestone to `Backlog`, and removed from milestone `TypeScript 5.1.0`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#2306](https://github.com/microsoft/TypeScript/issues/2306) (Open, `Suggestion`, `Domain: API`)

**Support for tabs in language service formatter\.**

*Request support for configuring the language service formatter to indent generated code with tabs instead of spaces.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#23185](https://github.com/microsoft/TypeScript/issues/23185) (Open, `Suggestion`, `Domain: Error Messages`)

**Cannot Load Custom Definition File in Repository**

*TypeScript 2.8.1 fails to discover a repository-local custom declaration file for an untyped JavaScript module.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/23185#issuecomment-5490016410) **LeonxLJX** said "I'd like to take this one — I'll follow up with a PR. (claiming via @LeonxLJX)"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/23185#issuecomment-5492444388) **LeonxLJX** said "Hi! I'd like to fix custom definition file loading. Plan: reproduce, fix the resolution, add a test. May I be assigned?"
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/23185#issuecomment-6098045419) **mahesh-desu** expressed intent to work on the issue by adding targeted diagnostics for unresolved non-relative modules with matching global declarations, plus compiler tests and baselines
 * (today) **RyanCavanaugh** removed labels `Help Wanted`, `Good First Issue`

### [Issue microsoft/TypeScript#23719](https://github.com/microsoft/TypeScript/issues/23719) (Open, `Suggestion`, `Domain: API`)

**Compiler API: Expose More from typescript\.d\.ts**

*Request to expose useful internal TypeScript compiler API properties and functions, including node locals, symbol parents, containing functions, and assignment targets.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [7 years ago](https://github.com/microsoft/TypeScript/issues/23719#issuecomment-541257068) **jirutka** said "@granmoe, take a look at TypeChecker#getSymbolsInScope (you can get its instance from the program)."
 * [6.7 years ago](https://github.com/microsoft/TypeScript/issues/23719#issuecomment-583775443) **Zemnmez** said "I second symbol.parent! It's very hard to operate on symbol trees without it."
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#23759](https://github.com/microsoft/TypeScript/issues/23759) (Open, `Suggestion`, `Domain: API: Transforms`)

**Verbose computed property transpilation**

*Computed property transpilation unnecessarily introduces a temporary variable and rewrites unrelated method names.*

 * [6.6 years ago](https://github.com/microsoft/TypeScript/issues/23759#issuecomment-606553494) **weswigham** said "? How so? Afaik there aren't computed private names?"
 * [6.6 years ago](https://github.com/microsoft/TypeScript/issues/23759#issuecomment-606559194) **falsandtru** reported that compiling a class with a private field and a static Symbol.species method generated problematic WeakMap initialization inside the computed property expression
 * [6.6 years ago](https://github.com/microsoft/TypeScript/issues/23759#issuecomment-606563048) **falsandtru** said "Looks like no workaround with ES private fields."
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#24063](https://github.com/microsoft/TypeScript/issues/24063) (Open, `Suggestion`)

**Typescript does not recognize function Boolean\(\) as a check for undefined**

*TypeScript fails to narrow potentially undefined values when checked with Boolean(value), unlike the equivalent !!value condition.*

 * **mhegazy** added label `help wanted`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#243](https://github.com/microsoft/TypeScript/issues/243) (Open, `Suggestion`, `Domain: API`)

**External interfaces included in IDE symbol space**

*TypeScript declarations in referenced or excluded `.d.ts` files appear in Visual Studio’s Navigate To results, polluting the IDE symbol space.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#24706](https://github.com/microsoft/TypeScript/issues/24706) (Open, `Breaking Change`, `Infrastructure`)

**API: incorrect declarations in types\.ts**

*Incorrectly non-nullable TypeScript API declarations in types.ts should be restored or corrected to reflect values that can be undefined.*

 * (6.7 years ago) **RyanCavanaugh** added label `help wanted`, and set milestone to `Backlog`
 * **DanielRosenwasser** added label `Breaking Change`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#24746](https://github.com/microsoft/TypeScript/issues/24746) (Open, `Bug`, `Domain: JSDoc`)

**JSDoc comment for destructuring param: description text not displayed**

*JSDoc descriptions for properties of destructured parameters are omitted from VSCode IntelliSense when the parent parameter has an Object type.*

 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/24746#issuecomment-1603287606) **dmrickey** reported that tooltips still failed for destructured parameters despite using the official JSDoc example and linked the relevant documentation
 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/24746#issuecomment-1735694624) **jpc-ae** reported that semicolons appeared instead of commas in object parameters in JSDoc tooltips, regardless of the syntax used, and requested a fix
 * [3 years ago](https://github.com/microsoft/TypeScript/issues/24746#issuecomment-1762016879) **Genroa** highlighted that destructured parameter support in VSCode's JSDoc tooltips remained a major issue despite ES6 usage and official documentation, and questioned why it was not properly supported
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#25033](https://github.com/microsoft/TypeScript/issues/25033) (Open, `Suggestion`, `Domain: Related Error Spans`, `Experience Enhancement`)

**Related error spans for derived members in interfaces/classes**

*Improve incompatible derived-member errors by adding related spans pointing to the corresponding base type member.*

 * (8 years ago) **RyanCavanaugh** added label `help wanted`, set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#25083](https://github.com/microsoft/TypeScript/issues/25083) (Open, `Bug`, `Domain: enum`)

**Enum keys not accepted as computed properties if their name is not a valid identifier**

*TypeScript rejects enum members accessed with bracket notation as computed property keys in type literals, especially for non-identifier names.*

 * [28 weeks ago](https://github.com/microsoft/TypeScript/issues/25083#issuecomment-4328482421) **RyanCavanaugh** warned AI coding agents and humans that the issue did not meet the 6.0 patch bar, discouraged submitting a PR, and advised reading AGENTS.md before proceeding
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/25083#issuecomment-5490015763) **LeonxLJX** said "I'd like to take this one — I'll follow up with a PR. (claiming via @LeonxLJX)"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/25083#issuecomment-5492443973) **LeonxLJX** said "Hi! I'd like to fix enum keys not accepted as computed properties. Plan: reproduce, adjust the checker, add a test. May I be assigned?"
 * **RyanCavanaugh** removed label `Good First Issue`

### [Issue microsoft/TypeScript#25175](https://github.com/microsoft/TypeScript/issues/25175) (Open, `Suggestion`, `Domain: LS: Refactorings`)

**simply logic predicate code fix or suggestion**

*Suggests adding a code fix or refactoring tool to simplify complex logical predicates using equivalent expressions.*

 * [8.3 years ago](https://github.com/microsoft/TypeScript/issues/25175#issuecomment-401199870) **mhegazy** noted that using Karnaugh maps would be difficult and emphasized the challenge of achieving constant memory and time
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#25607](https://github.com/microsoft/TypeScript/issues/25607) (Open, `Suggestion`, `Domain: Mapped Types`, `Experience Enhancement`, `Domain: LS: Symbol Navigation`)

**Services for non\-homomorphic mapped type**

*Go-to-definition and related services fail for properties in non-homomorphic mapped types because their symbols lack references to the source properties.*

 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **DanielRosenwasser** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#25771](https://github.com/microsoft/TypeScript/issues/25771) (Open, `Suggestion`, `Domain: Formatter`)

**Formatter should convert object literal to multiple lines / one line**

*Add a formatter refactor to toggle object literals between single-line and multi-line layouts.*

 * [8.3 years ago](https://github.com/microsoft/TypeScript/issues/25771#issuecomment-406325694) **ajafff** said "import and export specifiers "
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#25894](https://github.com/microsoft/TypeScript/issues/25894) (Open, `Suggestion`, `Domain: LS: Quick Info`, `Experience Enhancement`)

**Enums and interfaces do not have definitions in quick info/tooltips**

*Request hover tooltips to display complete enum and interface definitions, including their members, across local and imported usage.*

 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/25894#issuecomment-615000397) **ro-savage** asked where the codebase created the Type and Interface definitions so the community could help address the issue
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/25894#issuecomment-615275589) **orta** described using TSServer logging to trace requests and identified `SymbolDisplay.getSymbolDisplayPartsDocumentationAndSymbolKind` as the likely relevant code
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/25894#issuecomment-2529595842) **ugoi** said "Any updates on this?"
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#25898](https://github.com/microsoft/TypeScript/issues/25898) (Open, `Bug`, `Effort: Moderate`, `Domain: Error Messages`)

**Improve errors for potential arrow functions**

*Improve parser error messages for contexts where arrow functions are invalid, while preserving existing parsing behavior and limiting implementation scope.*

 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [6.2 years ago](https://github.com/microsoft/TypeScript/issues/25898#issuecomment-682969419) **DanielRosenwasser** said "https://github.com/microsoft/TypeScript/issues/39548 is sorta related to this because it's about parsing arrow function types in union types."
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#26413](https://github.com/microsoft/TypeScript/issues/26413) (Open, `Suggestion`, `Effort: Moderate`, `Domain: Error Messages`)

**Improve diagnostic when string from property is not assignable to string literal\.**

*Improve diagnostics and offer a codefix recommending type annotations when object-literal property values widen to incompatible string types.*

 * [8.2 years ago](https://github.com/microsoft/TypeScript/issues/26413#issuecomment-416678483) **RyanCavanaugh** said "@Kingwl discussion at #10195"
 * [7.6 years ago](https://github.com/microsoft/TypeScript/issues/26413#issuecomment-475708700) **Kingwl** explained that diagnostic types lacked position information, proposed replacing the diagnostic message chain with related information for `isRelatedTo`, and asked whether anything was missing
 * **RyanCavanaugh** added to milestone `Backlog`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#26617](https://github.com/microsoft/TypeScript/issues/26617) (Open, `Bug`, `Domain: Intersection`)

**Intersection type of abstract classes does not throw error if same member exists in multiple abstract classes**

*TypeScript fails to report an unimplemented member when identical abstract properties appear in multiple intersected classes.*

 * (7.6 years ago) **RyanCavanaugh** added label `Domain: Intersection`, set milestone to `Backlog`, and removed from milestone `TypeScript 3.4.0`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#26631](https://github.com/microsoft/TypeScript/issues/26631) (Open, `Bug`, `Domain: check: Variance Relationships`)

**Overriding generic method inconsistently errors**

*TypeScript inconsistently reports generic method override incompatibility, with a duplicate partial interface declaration unexpectedly suppressing the error.*

 * (8.2 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Variance Relationships`, and set milestone to `Future`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#26892](https://github.com/microsoft/TypeScript/issues/26892) (Open, `Suggestion`, `Experience Enhancement`)

**Typescript Autocompletion Not Working For Function Overloads**

*TypeScript autocompletion suggests literals from all function overloads instead of narrowing suggestions to the matched overload.*

 * [4 years ago](https://github.com/microsoft/TypeScript/issues/26892#issuecomment-1269451430) **dani-ras** asked for an update and reported that autocomplete failed to narrow after providing a partial argument to an overloaded function
 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/26892#issuecomment-1553785914) **ethanresnick** asked about the difficulty of fixing the language server issue and requested guidance on how to get started contributing
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/26892#issuecomment-2401089179) **dwjohnston** provided another example demonstrating missing autocomplete with function overloads and showed a generic-based workaround
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#26981](https://github.com/microsoft/TypeScript/issues/26981) (Open, `Suggestion`, `Committed`)

**Covariant assignability of type guard functions is unsound**

*TypeScript unsoundly allows assigning a narrower type guard to a broader one, causing incorrect narrowing and potential runtime errors.*

 * (7.6 years ago) **RyanCavanaugh** removed label `In Discussion`, set milestone to `Backlog`, and removed from milestone `TypeScript 3.4.0`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#27173](https://github.com/microsoft/TypeScript/issues/27173) (Open, `Docs`)

**NodeList is no more compatible with Array\<Node\>\. Breaking change in 3\.0 **

*TypeScript 3.0 introduced an undocumented incompatibility between NodeList and Array<Node> through conflicting forEach signatures.*

 * (8.1 years ago) **RyanCavanaugh** set milestones to `Community`, `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#27311](https://github.com/microsoft/TypeScript/issues/27311) (Open, `Bug`, `Domain: Error Messages`)

**Strange "Cannot use namespace 'Foo' as a type" error with dummy \`declare module "foo";\` declaration**

*A dummy ambient module declaration causes imported values to trigger a confusing “Cannot use namespace as a type” error.*

 * [5.1 years ago](https://github.com/microsoft/TypeScript/issues/27311#issuecomment-919132183) **bombillazo** confirmed that prefixing the namespace usage with `typeof` resolved the error while retaining the module declaration
 * [4.5 years ago](https://github.com/microsoft/TypeScript/issues/27311#issuecomment-1106340773) **denkhis** confirmed that removing the `.ts` extension from the import fixed the error and thanked the commenter
 * **RyanCavanaugh** added label `Domain: Error Messages`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#27545](https://github.com/microsoft/TypeScript/issues/27545) (Open, `Suggestion`, `Domain: lib.d.ts`)

**Typescript ESType definition improvements**

*Proposes improving TypeScript ESType definitions for object omission, assignment, array concatenation, and filtering undefined values.*

 * [7.8 years ago](https://github.com/microsoft/TypeScript/issues/27545#issuecomment-458394185) **saschanaz** questioned whether ES types were covered by the referenced repository
 * [7.8 years ago](https://github.com/microsoft/TypeScript/issues/27545#issuecomment-458395109) **weswigham** said "Ahhhh, you would be correct. I suppose here, then."
 * **RyanCavanaugh** added to milestone `Backlog`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#27910](https://github.com/microsoft/TypeScript/issues/27910) (Open, `Suggestion`, `Domain: Error Messages`, `Experience Enhancement`)

**TS2367: This condition will always return 'false' since the types 'Constructor\<T\>' and 'typeof Child' have no overlap\.**

*TypeScript incorrectly reports TS2367 when comparing a generic constructor parameter with the concrete Child class constructor.*

 * **RyanCavanaugh** removed label `PursuitFellowship`
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-5490015144) **LeonxLJX** said "I'd like to take this one — I'll follow up with a PR. (claiming via @LeonxLJX)"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-5492443531) **LeonxLJX** said "Hi! I'd like to fix TS2367 false positive for 'Con...' types. Plan: reproduce, adjust the comparison logic, add a test. May I be assigned?"
 * (today) **RyanCavanaugh** removed labels `Help Wanted`, `Good First Issue`

### [Issue microsoft/TypeScript#28003](https://github.com/microsoft/TypeScript/issues/28003) (Open, `Docs`)

**Wiki page 'Using the Language Service API' does not describe how to use the Language Service API**

*The wiki page lacks practical guidance on using the TypeScript Language Service API and needs more complete documentation.*

 * [6.7 years ago](https://github.com/microsoft/TypeScript/issues/28003#issuecomment-582998894) **ahnpnl** said "I hope the wiki can be updated soon"
 * (2.6 years ago) **RyanCavanaugh** added label `Help Wanted`, and set milestone to `Backlog`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#28097](https://github.com/microsoft/TypeScript/issues/28097) (Open, `Bug`, `Domain: Related Error Spans`)

**Imports in \.d\.ts files break wildcard modules declarations**

*An import in a declaration file prevents wildcard module declarations from resolving imported HTML files.*

 * [5.4 years ago](https://github.com/microsoft/TypeScript/issues/28097#issuecomment-863568596) **tsugabloom** described a module augmentation pitfall where self-referential imports resolve to `any`, causing the original type to be lost, and noted inconsistent behavior based on import placement
 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/28097#issuecomment-890553820) **djfm** said "Holy cow that's true, I had been trying to debug why my .d.ts file wasn't picked up for over an hour, thanks :)"
 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/28097#issuecomment-1409157390) **XieJiSS** said "Gently pinging - is there any plan to fix this in typescript 5.0? Thanks!"
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#283](https://github.com/microsoft/TypeScript/issues/283) (Open, `Bug`, `Domain: lib.d.ts`)

**cloneNode should return sub type, not Node**

*Update cloneNode typing so it returns the specific subtype of the element being cloned rather than the generic Node type.*

 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/283#issuecomment-2026808489) **callionica** requested that maintainers reassess the ongoing cloneNode typing issue and consider adding Element and HTMLElement-specific overloads
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/283#issuecomment-2802350962) **miss-programgamer** suggested introducing a generalized `typeof class` type to represent the current class or its subtypes in TypeScript, with examples involving cloning and constructor parameters
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/283#issuecomment-4169322887) **denis-migdal** suggested redefining `cloneNode` for `DocumentFragment`, `Element`/`HTMLElement`, or generically on `Node` to improve TypeScript typing without modifying every subclass
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#28308](https://github.com/microsoft/TypeScript/issues/28308) (Open, `Bug`, `Domain: lib.d.ts`)

**AudioWorkletProcessor type definition is missing**

*TypeScript’s Web Audio API definitions are missing the AudioWorkletProcessor interface and constructor declaration.*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/28308#issuecomment-1879719320) **NuclearPhoenixx** noted that `@types/audioworklet` caused definition conflicts when used alongside the `DOM` library
 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/28308#issuecomment-1921865859) **majaha** proposed updated AudioWorklet type definitions and highlighted TypeScript limitations with modeling multiple global scopes
 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/28308#issuecomment-1935417258) **UrielCh** reported that the TypeScript declarations worked only partially, leaving process parameter types as `any`, and noted issues using the `@types/audioworklet` reference with the VS Code Deno plugin
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#2850](https://github.com/microsoft/TypeScript/issues/2850) (Open, `Suggestion`, `Effort: Moderate`, `VS Code Tracked`)

**TSServer: 'quickInfo' request should return symbol display parts as completion does**

*Update TSServer’s quickInfo response to include symbol display parts, matching completion responses for consistent UI formatting.*

 * **mhegazy** unassigned **zhengbli**
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#2858](https://github.com/microsoft/TypeScript/issues/2858) (Open, `Suggestion`)

**Port from old compiler code to emit compilation flags into the source map**

*Port the old compiler’s behavior of embedding compilation flags in source maps to support potential live-edit recompilation tooling.*

 * **mhegazy** added to milestone `Community`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#29531](https://github.com/microsoft/TypeScript/issues/29531) (Open, `Suggestion`, `Domain: lib.d.ts`, `Experience Enhancement`)

**type predicate\-ness lost when using Function\.prototype\.bind**

*Function.prototype.bind loses type predicate information, preventing bound predicate functions like Array.isArray from matching their original type.*

 * (7.8 years ago) **RyanCavanaugh** set milestones to `Community`, `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#29548](https://github.com/microsoft/TypeScript/issues/29548) (Open, `Suggestion`, `In Discussion`, `Domain: lib.d.ts`)

**Add type definitions for Files And Directories API**

*Add TypeScript definitions for the Files and Directories API interfaces supporting drag-and-drop handling of files and folders.*

 * [5.7 years ago](https://github.com/microsoft/TypeScript/issues/29548#issuecomment-777294757) **youk** said "https://github.com/DefinitelyTyped/DefinitelyTyped/tree/master/types/wicg-file-system-access"
 * [5.5 years ago](https://github.com/microsoft/TypeScript/issues/29548#issuecomment-827600564) **HenningCash** clarified the distinction between the Entries API and File System Access API, compared browser support, and noted that DefinitelyTyped now provides Entries API types
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/29548#issuecomment-2474083588) **jonkoops** said "I think this issue can be closed, this is now part of the DOM types so should be fully supported."
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#29707](https://github.com/microsoft/TypeScript/issues/29707) (Open, `Bug`, `Domain: classes`)

**TS is overly picky when declaring a class constructor type**

*TypeScript rejects extending a generic constructor constrained with signatures other than `...args: any[]`, such as `unknown[]`.*

 * [29 weeks ago](https://github.com/microsoft/TypeScript/issues/29707#issuecomment-4253541609) **RyanCavanaugh** said "@snarbles2 I'm tempted to set up a script to auto-ban anyone who gets a 🚀 reaction from you 😅"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/29707#issuecomment-5490014523) **LeonxLJX** said "I'd like to take this one — I'll follow up with a PR. (claiming via @LeonxLJX)"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/29707#issuecomment-5492443090) **LeonxLJX** said "Hi! I'd like to fix the overly-picky constructor type check. Plan: reproduce, adjust the check, add a test. May I be assigned?"
 * (today) **RyanCavanaugh** removed labels `Help Wanted`, `Good First Issue`

### [Issue microsoft/TypeScript#29789](https://github.com/microsoft/TypeScript/issues/29789) (Open, `Bug`, `Domain: lib.d.ts`)

**\`\.call\` selects the wrong overload for \`String\.prototype\.replace\`**

*TypeScript incorrectly selects the callback overload for String.prototype.replace.call, rejecting valid string replacement arguments in checked JavaScript.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [7.5 years ago](https://github.com/microsoft/TypeScript/issues/29789#issuecomment-494001748) **jaredh159** reported encountering the same issue without using `.call`, provided a TypeScript example showing that `String.replace` rejects a `string | ReplacerFn` union, and included a Playground link
 * [6.9 years ago](https://github.com/microsoft/TypeScript/issues/29789#issuecomment-558970471) **marcin-serwin** said "Hi, Could I get any feedback on #34941?"
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#299](https://github.com/microsoft/TypeScript/issues/299) (Open, `Suggestion`, `Domain: lib.d.ts`)

**Request to change currentTarget in Event interface for lib\.d\.ts**

*Request to change Event.currentTarget in lib.d.ts from EventTarget to Element or HTMLElement for event listener callbacks.*

 * [4.4 years ago](https://github.com/microsoft/TypeScript/issues/299#issuecomment-1161327360) **DaSchTour** said "The PRs are there, but blocked by performance issues. I would not expect this issue to be solved any time soon. I guess everybody got used to this problem."
 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/299#issuecomment-1452219277) **minecrawler** noted that an earlier PR addressing the issue was closed due to poor generic-related performance and inactivity, and asked whether someone familiar with tsc could implement the requested feature
 * [3 years ago](https://github.com/microsoft/TypeScript/issues/299#issuecomment-1759573514) **nscarcella** said "For anyone still interested in this feature, I created a PR here and could use some feedback regarding the performance."
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#30130](https://github.com/microsoft/TypeScript/issues/30130) (Open, `Suggestion`, `Experience Enhancement`)

**Nested classes are not collapsible/expandable in Visual Studio**

*Visual Studio does not support collapsing or expanding code inside nested class expressions.*

 * (7.7 years ago) **RyanCavanaugh** set milestones to `Community`, `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#30162](https://github.com/microsoft/TypeScript/issues/30162) (Open, `Suggestion`, `Experience Enhancement`)

**is not under 'rootDir' 'src/'\. even with exclude**

*TypeScript reports TS6059 for files in an excluded `gen` directory because they fall outside the configured `src/` rootDir.*

 * (7.7 years ago) **RyanCavanaugh** set milestones to `Community`, `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#30223](https://github.com/microsoft/TypeScript/issues/30223) (Open, `Bug`, `Domain: Error Messages`)

**Inconsistent behavior of "export as" symbols\.**

*TypeScript inconsistently displays aliased export names, showing the original class name in error messages but the public alias in valid code hints.*

 * [7.6 years ago](https://github.com/microsoft/TypeScript/issues/30223#issuecomment-471700180) **Fabianopb** said "Bingo! That shows the behavior as you described! I'd be interested in working on this issue, is that fine @RyanCavanaugh and @KostyaTretyak ?"
 * [7.6 years ago](https://github.com/microsoft/TypeScript/issues/30223#issuecomment-480205243) **Fabianopb** asked for guidance on addressing the reported error by displaying an export alias instead of the original type name, and proposed two implementation approaches
 * **RyanCavanaugh** added label `Domain: Error Messages`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#3025](https://github.com/microsoft/TypeScript/issues/3025) (Open, `Suggestion`, `Domain: API`, `Domain: LS: Quick Info`)

**Rationalize our presentation and handling of merged/alias symbols in the IDE\.**

*Improve IDE presentation and navigation for alias, union, and merged symbols by exposing their targets and constituent declarations.*

 * **DanielRosenwasser** added label `Domain: Quick Info`
 * (7.6 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** removed label `Help Wanted`

### [Issue microsoft/TypeScript#30408](https://github.com/microsoft/TypeScript/issues/30408) (Open, `Suggestion`, `Effort: Moderate`, `Domain: Error Messages`, `Experience Enhancement`)

**Confusing error message for labels used before definition**

*TypeScript reports a confusing cross-function-boundary error when a loop continues to a label defined later in the function.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/30408#issuecomment-5661952649) **anbv29** said "Hey, i would like to work on this. Can i be assigned this issue?"
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/30408#issuecomment-5873737878) **RyanCavanaugh** warned that opening another PR without acknowledging the issue and explaining what would differ from the previous seven would be treated as automated behavior and lead to an immediate ban
 * (today) **RyanCavanaugh** removed labels `Help Wanted`, `Good First Issue`

### [Issue microsoft/TypeScript#31104](https://github.com/microsoft/TypeScript/issues/31104) (Open, `Suggestion`, `Effort: Moderate`, `Experience Enhancement`, **DanielRosenwasser**)

**'Omit' should alias a distinct mapped type \(for display purposes\)**

*Define `Omit` as a distinct mapped type so quick info and error messages display it directly instead of expanding it to `Pick<Exclude<...>, ...>`.*

 * [6.1 years ago](https://github.com/microsoft/TypeScript/issues/31104#issuecomment-696515204) **ExE-Boss** said "For TS 4.0 and older, you can use @Jack-Works’s ."
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`
 * (today) **RyanCavanaugh** removed label `Help Wanted`, and set milestone to `Backlog`

