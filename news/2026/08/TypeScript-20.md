# Report for 2026-08-20 (Thursday, August 20th, 2026)

30 different users commented on 213 different issues.

## Recommended Actions

 * Response Recommended
    * @aweebit requested improved excess property checking for JSX prop spreads in [microsoft/TypeScript#39998](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-5371695706)
    * @aweebit reported that conditionally added properties in JSX should trigger an error in [microsoft/TypeScript#39998](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-5371961332)

## Activity Summary

### [Issue microsoft/TypeScript#14729](https://github.com/microsoft/TypeScript/issues/14729) (Open, `Suggestion`, `In Discussion`, **weswigham**)

**Type JSX elements based on createElement function**

*Use customizable JSX.createElement overloads to infer element and prop types instead of a fixed JSX.Element type.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/14729#issuecomment-2076067603) **frzi** said "Is there still any interest or plans for this? This seems like an incredible feature that’ll make libraries utilizing JSX far more versatile. 😄"
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/14729#issuecomment-2080205977) **robbiespeed** provided TS Playground examples demonstrating recursive return type checks to enable renders types and restrict allowed JSX children
 * [45 weeks ago](https://github.com/microsoft/TypeScript/issues/14729#issuecomment-3367361306) **WorldMaker** described exploring dependency-injection of JSX functions for richer typing and asked about overcoming ambient namespace limitations to vary IntrinsicElements by context
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#15402](https://github.com/microsoft/TypeScript/issues/15402) (Open, `Suggestion`, `Help Wanted`, `Domain: lib.d.ts`)

**Suggestion: a built\-in TypedArray interface**

*Introduce a common TypedArray interface in TypeScript’s built-in declarations to consolidate typed array types and improve type-guard support.*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/15402#issuecomment-2414599484) **petamoriken** asked why TypedArray and ArrayBufferView differ between @types/node and es5.d.ts
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/15402#issuecomment-2596173471) **kyr0** described missing TypedArray constructor overloads in the published lib and proposed a comprehensive custom TypedArrayConstructor type to include the length argument
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/15402#issuecomment-3148287607) **BlackAsLight** said "After finding myself needing this type today, I discover others have been wanting it for 8 years. "
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#17002](https://github.com/microsoft/TypeScript/issues/17002) (Open, `Suggestion`, `In Discussion`, `Domain: lib.d.ts`)

**Array\.isArray type narrows to any\[\] for ReadonlyArray\<T\>**

*Array.isArray fails to correctly narrow a union including ReadonlyArray<T>, resulting in an any[] type instead of ReadonlyArray<T>.*

 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4080971605) **cahnory** described augmenting ArrayConstructor.isArray to use a readonly unknown[] type guard, compared approaches, noted a minor type-narrowing difference, and expressed a preference for a dedicated helper over standard-library augmentation
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4885934843) **daishuge** submitted a minimal fix in PR #63609 that added an overload in es5.d.ts to preserve readonly input types without affecting unknown narrowing
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4896931936) **anderson-pete** noted that the proposed fix would break a lot of existing code
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#17473](https://github.com/microsoft/TypeScript/issues/17473) (Open, `Suggestion`, `In Discussion`)

**Infer constrained generic parameters after instanceof check**

*Infer constrained generic parameter types after an instanceof check to avoid explicit casts.*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/17473#issuecomment-2551383949) **jcalz** noted that the constraint was only appropriate for covariant type parameters, that contravariant parameters should use `never`, and that otherwise `any` was probably the best due to lack of existential types
 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/17473#issuecomment-2557562508) **molisani** described current proposed fix logic for type parameter inference, including handling of contravariant, bivariant cases, fallback to unknown, and compiler option gating
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/17473#issuecomment-2646348680) **maximan3000** provided a temporary workaround involving creating a duplicated non-generic class to fix type inference in a generic class
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#21699](https://github.com/microsoft/TypeScript/issues/21699) (Open, `Suggestion`, `Breaking Change`, `Effort: Moderate`, `Domain: JSX/TSX`)

**Decouple jsx element type from jsx factory return type and sfc return type**

*Resolve JSX expression and SFC return types from factory overloads instead of relying on global JSX.Element.*

 * [2 years ago](https://github.com/microsoft/TypeScript/issues/21699#issuecomment-2304715259) **reverofevil** explained TS's context-sensitive resolution and how it led to exponential type-checking operations in nested JSX calls
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/21699#issuecomment-2304739788) **sdegutis** recommended checking out hastx as a similar HTML AST generator, noted support for typed JSX expressions, and shared anecdotes about previous JSX work and community fragmentation
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/21699#issuecomment-2304814488) **cowboyd** suggested using JSX literals to represent elements and components and asked what would be wrong with straightforward literal syntax for JavaScript values
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#23572](https://github.com/microsoft/TypeScript/issues/23572) (Open, `Bug`, `Domain: check: Control Flow`)

**Exhaustiveness checking against an enum only works when the enum has \>1 member\.**

*TypeScript's exhaustiveness checking on a discriminated union fails when the enum used for the discriminant has only one member.*

 * (35 weeks ago) **typescript-bot** added labels `Fix Available`, `Fix Available`
 * **RyanCavanaugh** unassigned **Copilot**
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#241](https://github.com/microsoft/TypeScript/issues/241) (Open, `Suggestion`, `Experimentation Needed`)

**Don't widen return types of function expressions**

*Disable return-type widening for function expressions to yield more accurate inferred types and reduce implicit anys.*

 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/241#issuecomment-2365177697) **ernestostifano** said "Having same issue as @yamcodes "
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/241#issuecomment-2395429477) **alvis** described a TypeScript discrepancy where extra properties were not reported as errors when assigning objects to variables or using object spread in return statements
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/241#issuecomment-2396897225) **snarbies** explained that extra properties are allowed in TypeScript and excess property checks only apply at the point of declaration
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#24509](https://github.com/microsoft/TypeScript/issues/24509) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add a Mutable type \(opposite of Readonly\) to lib\.d\.ts**

*Add a built-in Mutable<T> utility type to lib.d.ts to remove readonly modifiers from object types.*

 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/24509#issuecomment-1933166674) **julian-kingman-lark** described a React use-case with a class having mutable properties and requested TypeScript to error when assigning immutable values to mutable properties
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/24509#issuecomment-2104481692) **c-vetter** explained that while a `mutable` keyword would be useful, it was tangential to the issue, and provided a self-contained example illustrating how TypeScript handles mutable versus readonly types and why certain mutations won’t error
 * [45 weeks ago](https://github.com/microsoft/TypeScript/issues/24509#issuecomment-3386572799) **Eptagone** reported a type error when assigning to the read-only sessionToken property while configuring AWS credentials
 * **jakebailey** removed label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/24509#issuecomment-5366197908) **irfanstract** expressed a wish that TypeScript defaulted to immutability and referenced the tc39/proposal-composites proposal

### [Issue microsoft/TypeScript#28702](https://github.com/microsoft/TypeScript/issues/28702) (Open, `Suggestion`, `Fixed`, `Domain: JavaScript`, `Experience Enhancement`)

**In JS, don't complain about a better inferred type if there's no code action**

*When checkJS is enabled in JavaScript files, TypeScript complains about parameters lacking JSDoc without offering a fix.*

 * (7.1 years ago) **RyanCavanaugh** added label `Fix Available`, and set milestone to `Backlog`
 * [5.8 years ago](https://github.com/microsoft/TypeScript/issues/28702#issuecomment-712879076) **vjsingh** said "@AlCalzone @RyanCavanaugh Is there any way to suppress this message? Using the jsconfig.json?"
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#29841](https://github.com/microsoft/TypeScript/issues/29841) (Open, `Needs Investigation`, `Rescheduled`, **DanielRosenwasser**)

**Improve typings of Array\.map when called on tuples**

*Enhance Array.map’s TypeScript typings to return a tuple type when mapping over a tuple instead of a generic array.*

 * [47 weeks ago](https://github.com/microsoft/TypeScript/issues/29841#issuecomment-3327091081) **Anoesj** requested automatic tuple .map() typing support and suggested a tsconfig option
 * [35 weeks ago](https://github.com/microsoft/TypeScript/issues/29841#issuecomment-3642875750) **petdomaa100** reported encountering the issue frequently and suggested using a dedicated mapTuple method or utility function as a workaround
 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/29841#issuecomment-3980542123) **BarthPaleologue** said "That would be a great feature! Maybe the advent of go for TSC will help make this a reality?"
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#31104](https://github.com/microsoft/TypeScript/issues/31104) (Open, `Suggestion`, `Help Wanted`, `Effort: Moderate`, `Experience Enhancement`, **DanielRosenwasser**)

**'Omit' should alias a distinct mapped type \(for display purposes\)**

*Alias Omit to a distinct conditional mapped type to improve display by avoiding verbose Pick<Exclude> expansions.*

 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/31104#issuecomment-696439873) **DanielRosenwasser** said "Also, @weswigham may want to weigh in since he has a PR out at #37608, but I think it would be undesirable to add a 3rd type parameter just to use a default type argument."
 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/31104#issuecomment-696515204) **ExE-Boss** said "For TS 4.0 and older, you can use @Jack-Works’s ."
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#31155](https://github.com/microsoft/TypeScript/issues/31155) (Open, `Bug`, `Domain: check: Control Flow`, `Rescheduled`, **orta**)

**'instanceof' changes type outside of 'if' statement**

*An instanceof check on a variable improperly preserves the C branch in its type outside the if block, causing v.onChanges to error under strictNullChecks.*

 * (2.4 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#31426](https://github.com/microsoft/TypeScript/issues/31426) (Open, `Bug`, `Domain: classes`)

**\[3\.5\.0\-dev\.20190516\] Incorrect type error for mixin**

*Using interface-based mixin notation in TypeScript incorrectly reports type errors for property usage in mixin methods.*

 * **orta** removed from milestone `TypeScript 3.9.0`
 * (5.9 years ago) **RyanCavanaugh** added label `Domain: classes`, and set milestone to `Backlog`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#31849](https://github.com/microsoft/TypeScript/issues/31849) (Open, `Help Wanted`, `Domain: API`, `Docs`, **DanielRosenwasser**, **sheetalkamat**)

**Document \-\-incremental and composite project APIs**

*Document the TypeScript compiler’s --incremental and composite project APIs to clarify their usage.*

 * [6.4 years ago](https://github.com/microsoft/TypeScript/issues/31849#issuecomment-601780191) **hipstersmoothie** said "Here's how I ended up doing it: https://github.com/intuit/design-systems-cli/blob/master/plugins/build/src/typescript.ts#L173"
 * [6.4 years ago](https://github.com/microsoft/TypeScript/issues/31849#issuecomment-602470113) **RomainMuller** said "@hipstersmoothie that's pretty similar to what I was doing out of spite... Figured there should be a better way; but it juts looks like the necessary invalidation logic is presently burried."
 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/31849#issuecomment-754082263) **mortyccp** asked how to get the emitted files for the jest input sourcePath using solution builder
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#32529](https://github.com/microsoft/TypeScript/issues/32529) (Open, `Infrastructure`)

**Add broccoli\-typescript\-compiler to user test suite**

*Add the broccoli-typescript-compiler package from tildeio to the project's user test suite.*

 * (6.5 years ago) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 3.8.1`, and unassigned **weswigham**
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#33623](https://github.com/microsoft/TypeScript/issues/33623) (Open, `Bug`, `Domain: Module Resolution`, **weswigham**)

**Investigate altering extension priorities for wildcard loading**

*Adjust TypeScript’s wildcard file loading extension priorities to ensure declaration files have the lowest precedence*

 * (6.4 years ago) **RyanCavanaugh** added label `Domain: Module Resolution`, set milestone to `Backlog`, and removed from milestone `TypeScript 3.9.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#33700](https://github.com/microsoft/TypeScript/issues/33700) (Open, `Suggestion`, `Needs Proposal`)

**Array\.isArray refinement loses the array's type**

*TypeScript’s Array.isArray guard loses array element type information instead of refining the type correctly.*

 * [6.8 years ago](https://github.com/microsoft/TypeScript/issues/33700#issuecomment-540090753) **RyanCavanaugh** reiterated that harsh criticism and insults discouraged their efforts
 * **typescript-bot** added label `Fix Available`
 * [4.4 years ago](https://github.com/microsoft/TypeScript/issues/33700#issuecomment-1065582349) **jablko** described the similarities between two issues regarding `readonly T[]` and `Iterable<T>`, compared their type behaviors, suggested a potential generic solution and noted that `readonly T[]` is already a subtype of `Iterable<T>`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#34119](https://github.com/microsoft/TypeScript/issues/34119) (Open, `Needs Investigation`, `Domain: Performance`, `Rescheduled`, **weswigham**)

**tsc \-\-watch initial build 3x slower than tsc**

*Using ts-essentials’ DeepReadonly type on a 1000-file project causes tsc --watch initial build to be three times slower than plain tsc.*

 * (2.4 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#34933](https://github.com/microsoft/TypeScript/issues/34933) (Open, `Bug`, `Domain: check: Big Unions`, `Rescheduled`, **weswigham**)

**“Type instantiation is excessively deep and possibly infinite” but only in a large codebase**

*TypeScript 3.7+ yields an excessively deep type instantiation error for generics in a large codebase but not in the playground.*

 * **RyanCavanaugh** added to milestone `TypeScript 5.7.0`
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/34933#issuecomment-2719710058) **vipcxj** said "same issue，happened when using redux-tookit. what a horrible bug. any news?"
 * [43 weeks ago](https://github.com/microsoft/TypeScript/issues/34933#issuecomment-3418746640) **ChapelStudios** said "Still nothing? the milestone is listed as 5.7 but TS is on 5.9 now. I'm running into this on a smaller project with a lot of class inheritance and class mix-ins."
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#35824](https://github.com/microsoft/TypeScript/issues/35824) (Open, `Bug`, `Domain: check: Control Flow`, `Rescheduled`, **elibarzilay**)

**Assigning to a string fails if it was previously compared to an enum**

*TypeScript narrows a string variable to its enum type after an equality check, causing `+=` string concatenation to error.*

 * (2 years ago) **RyanCavanaugh** added label `Domain: Control Flow`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#36772](https://github.com/microsoft/TypeScript/issues/36772) (Open, `Bug`, `Domain: check: Control Flow`, `Rescheduled`)

**Type not narrowed by === when equivalent type guard works**

*TypeScript fails to narrow a generic type parameter using a direct `=== 'a'` comparison, unlike a custom type guard.*

 * (14 weeks ago) **RyanCavanaugh** set milestone to `Backlog`, and unassigned **ahejlsberg**
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#36981](https://github.com/microsoft/TypeScript/issues/36981) (Open, `Needs Investigation`, `Rescheduled`, **weswigham**)

**\`Omit\`  helper loses type information when used with extended Records\.**

*Using Omit on an interface extending Record<string, any> causes all property types, including explicitly defined ones, to be replaced with any.*

 * (2.4 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#37774](https://github.com/microsoft/TypeScript/issues/37774) (Open, `Suggestion`, `Awaiting More Feedback`)

**isolatedModules doesn't respect enabled preserveConstEnum option what the project might be build with**

*The isolatedModules flag should respect preserveConstEnums settings and allow preserved const enum imports rather than always erroring.*

 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/37774#issuecomment-2004488571) **andrewbranch** explained that module resolution in referenced .d.ts files follows the referenced project’s settings and suggested silencing the error when the ambient file’s project uses preserveConstEnums
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/37774#issuecomment-2004575433) **jakebailey** said "I wanted something like this in #51530 so that we could use const enums within TS but still refer to them by value if needed; my issue is probably a dupe of the above request."
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#39059](https://github.com/microsoft/TypeScript/issues/39059) (Open, `Bug`, `Rescheduled`, `Domain: check: Type Circularity`, **weswigham**)

**Possible regression: Maximum call stack size exceeded when migrating from 3\.7\.5 to latest version**

*Upgrading TypeScript above version 3.7.5 causes certain code to trigger a compiler stack overflow (Maximum call stack size exceeded) error.*

 * (2 years ago) **RyanCavanaugh** added label `Domain: Type Circularity`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#39693](https://github.com/microsoft/TypeScript/issues/39693) (Open, `Suggestion`, `In Discussion`)

**for\-of loop with intersection of array types produces a union of element types**

*Iterating over an intersection of array types in TypeScript yields a union of element types instead of their intersection.*

 * **typescript-bot** added label `Fix Available`
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/39693#issuecomment-1885744147) **rotu** noted that the for...of loop behavior changed between 3.9.7 and 4.0.5, now inferring elemItr as an intersection instead of a union, and provided a playground link
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/39693#issuecomment-1947769557) **craigphicks** asked where the intersection type 'Array<{ a: string }> | Array<{ b: number }>' came from and what its implementation was, questioned why it wasn’t written as 'Array<{ a: string, b: number }>', and proposed an alternative union representation with examples illustrating type narrowing
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#39749](https://github.com/microsoft/TypeScript/issues/39749) (Open, `Help Wanted`, `Effort: Moderate`, `Domain: JSX/TSX`, `Domain: Error Messages`, `Experience Enhancement`, `Rescheduled`, **weswigham**)

**Specialize JSX error messages for missing properties**

*Enhance TypeScript JSX missing property errors to specify component tags and enumerate missing attributes.*

 * (2.4 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#39998](https://github.com/microsoft/TypeScript/issues/39998) (Open, `Suggestion`, `Awaiting More Feedback`)

**Suggestion: perform excess property checks when spreading an inline object literal**

*Add excess property checks for inline object literals spread within other object literals to catch invalid properties.*

 * [51 weeks ago](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-3223170523) **dpeter99** said "I have just run into this at work, while trying to figure out whay I wasn't getting "may only specify known properties" warnings."
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-3730376223) **zacaj** critiqued the lack of validation for `satisfies` when spreads were used
 * [26 weeks ago](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-3920632797) **OliverJAsh** mentioned that with exactOptionalPropertyTypes enabled, spread must be used for optional properties and provided examples
 * [later](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-5371695706) **aweebit** described that JSX prop spreading loses excess property checking and called the ‘satisfies’ workaround clumsy
 * [later](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-5371961332) **aweebit** highlighted that conditionally added properties also affected JSX and should trigger an error

### [Issue microsoft/TypeScript#40092](https://github.com/microsoft/TypeScript/issues/40092) (Open, `Bug`, `Domain: Declaration Emit`, `Rescheduled`, **weswigham**)

**random emit declaration**

*TypeScript .d.ts emission is non-deterministic, producing random declaration files rather than stable outputs*

 * (2 years ago) **RyanCavanaugh** added label `Domain: Declaration Emit`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#40312](https://github.com/microsoft/TypeScript/issues/40312) (Open, `Bug`, `Domain: check: Variance Relationships`, **weswigham**)

**Cannot assign generic type aliases that should be equivalent\.**

*Generic type aliases in TypeScript 4.0 incorrectly disallow assigning equivalent function types under strictNullChecks compared to expanded types.*

 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/40312#issuecomment-841404787) **RyanCavanaugh** linked another repro demonstrating type assignment failure with extended interface
 * [4.5 years ago](https://github.com/microsoft/TypeScript/issues/40312#issuecomment-1046249173) **tychenjiajun** reported a similar issue and shared a TypeScript Playground link
 * **RyanCavanaugh** added label `Domain: Variance Relationships`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#41914](https://github.com/microsoft/TypeScript/issues/41914) (Open, `Needs Investigation`, `Rescheduled`, **weswigham**)

**Code invalid when \[jsx=react\-jsx\] and \[module=system\]**

*Using TypeScript’s react-jsx JSX setting with the System module target generates invalid System.register output*

 * (2.4 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#41977](https://github.com/microsoft/TypeScript/issues/41977) (Open, `Bug`, `Domain: check: Error Instability`)

**Unexpected behavior when static methods are used in an array**

*Arrays of static class methods and functions sometimes bypass type checks unless a related type alias is defined.*

 * **typescript-bot** added label `Fix Available`
 * (44 weeks ago) **RyanCavanaugh** added label `Domain: Error Instability`, and unassigned **RyanCavanaugh**
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#42079](https://github.com/microsoft/TypeScript/issues/42079) (Open, `Bug`, `Domain: Declaration Emit`, `Rescheduled`, **weswigham**)

**Syntax error in emitted declaration's generic arguments**

*Declaration emit incorrectly uses the generic type parameter T in the nested constant, causing a TS2304 error*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/42079#issuecomment-2156982951) **MichaelMitchell-at** suggested updating the milestone since the fix wouldn't make 5.5.0
 * (2.1 years ago) **weswigham** set milestone to `Backlog`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#42271](https://github.com/microsoft/TypeScript/issues/42271) (Open, `Needs Investigation`, `Rescheduled`, **rbuckton**)

**Compilation error when mixing promise and non promise types in promise\.then's onfulfilled return type**

*TypeScript reports a compilation error when a promise .then handler conditionally returns both Promise and non-Promise types.*

 * **RyanCavanaugh** added to milestone `TypeScript 5.7.0`
 * (1.8 years ago) **typescript-bot** added labels `Fix Available`, `Fix Available`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#42369](https://github.com/microsoft/TypeScript/issues/42369) (Open, `Needs Investigation`, `Rescheduled`, **weswigham**)

**Conditional type which checks nested intersect types evaluates inconsistently when outer type is also intersected and inner type intersects with any\.**

*In TypeScript, nested intersected types combined with any and an extra intersect yield inconsistent conditional type evaluations.*

 * (2.4 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#42508](https://github.com/microsoft/TypeScript/issues/42508) (Open, `Bug`, `Domain: check: Type Inference`, `Rescheduled`, **sandersn**)

**Error when spreading a union of tuples in a call**

*Spreading a union of two- and three-element tuples into Date.setHours incorrectly reports an argument count error.*

 * **RyanCavanaugh** added to milestone `TypeScript 5.7.0`
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/42508#issuecomment-2439631336) **nikelborm** suggested using a typed tuple and spread syntax for Date.prototype.setHours
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#42734](https://github.com/microsoft/TypeScript/issues/42734) (Open, `Bug`, `Rescheduled`, `Domain: classes`, **armanio123**)

**TS18030: An optional chain cannot contain private identifiers**

*TypeScript reports TS18030 when optional chaining is used to access a private class field.*

 * **RyanCavanaugh** added to milestone `TypeScript 5.7.0`
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/42734#issuecomment-2420675113) **Psychpsyo** said "I have opened a PR to fix this, it is #60263"
 * **RyanCavanaugh** added label `Domain: classes`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#43867](https://github.com/microsoft/TypeScript/issues/43867) (Open, `Bug`, `Domain: This-Typing`, `Rescheduled`, **weswigham**)

**redux\-orm broken by \#43624**

*After TypeScript PR #43624, redux-orm’s Model definitions no longer compile due to ‘this’ constraint errors, so its type definitions need updating.*

 * (2 years ago) **RyanCavanaugh** added label `Domain: This-Typing`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#44044](https://github.com/microsoft/TypeScript/issues/44044) (Open, `Domain: Performance`, `Rescheduled`, **weswigham**)

**Idea: Can declaration emit synthesize imports?**

*Allow declaration files to synthesize and reuse imports for repeatedly referenced unimported types to reduce file size.*

 * (2 years ago) **RyanCavanaugh** set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/44044#issuecomment-2334014153) **bosens-China** highlighted redundant object property generation in the TypeScript declaration resulting in duplicated structures
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#44143](https://github.com/microsoft/TypeScript/issues/44143) (Open, `Bug`, `Domain: Conditional Types`, `Rescheduled`, **weswigham**)

**KnownKeys\<T\> breaking change in 4\.3\.1\-rc**

*KnownKeys<T> type utility incorrectly fails to extract known interface keys in TypeScript 4.3.1-rc, regressing from version 4.3.0-beta.*

 * (2.4 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#44191](https://github.com/microsoft/TypeScript/issues/44191) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**Update \`TypedArray\` constructors to disallow invalid \`\(typedArray, byteOffset, byteLength\)\`**

*Correct TypeScript’s TypedArray constructor definitions to forbid specifying byteOffset and byteLength when constructing from another TypedArray.*

 * (5.2 years ago) **RyanCavanaugh** added label `help wanted`, and set milestone to `Backlog`
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#44794](https://github.com/microsoft/TypeScript/issues/44794) (Open, `Bug`, `Breaking Change`, `Domain: check: Excess Property Checking`, `Rescheduled`, **ahejlsberg**)

**Symbol properties should not be exempt from excess property checks in presence of a string index signature**

*Symbol properties bypass excess property checks when a string index signature is present but should not be exempt.*

 * (2 years ago) **RyanCavanaugh** added label `Domain: Excess Property Checking`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#44945](https://github.com/microsoft/TypeScript/issues/44945) (Open, `Bug`, `Domain: Conditional Types`, `Rescheduled`, **weswigham**)

**Conditional types behavior is different when referencing same type with different name**

*Conditional types in TypeScript behave inconsistently when the same generic type is referenced under different aliases.*

 * (2 years ago) **RyanCavanaugh** added label `Domain: Conditional Types`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#45349](https://github.com/microsoft/TypeScript/issues/45349) (Open, `Suggestion`, `Awaiting More Feedback`, `Domain: JavaScript`, `Experimentation Needed`, `Rescheduled`, **sandersn**)

**Provide Grammar Errors for JavaScript Files**

*Proposes adding grammar error reporting to JavaScript files for duplicate block-scoped variables and invalid syntax while exploring API design.*

 * (2 years ago) **RyanCavanaugh** added label `Awaiting More Feedback`, removed label `Meta-Issue`, and set milestone to `TypeScript 5.7.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#45389](https://github.com/microsoft/TypeScript/issues/45389) (Open, `Suggestion`, `Help Wanted`, `Experience Enhancement`, `Rescheduled`, `Domain: LS: Inlay Hints`)

**Inlay hints look awkward for callback parameters with a single parameter**

*Inlay hints for arrow callbacks with a lone unparenthesized parameter look awkward and lack proper formatting*

 * (2.4 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#45531](https://github.com/microsoft/TypeScript/issues/45531) (Open, `Bug`, `Domain: JS Emit`, `Rescheduled`)

**Object literal getters and setters doesn't work after spread syntax \(ES2017 and below\)**

*Getters and setters defined after an object literal spread are compiled to plain properties and thus not preserved.*

 * (44 weeks ago) **RyanCavanaugh** set milestone to `Backlog`, and unassigned **rbuckton**
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#45560](https://github.com/microsoft/TypeScript/issues/45560) (Open, `Bug`, `Domain: Mapped Types`)

**Mapped types lose type information**

*Mapped types over tuple unions lose specific element types and widen indexed access to boolean instead of true.*

 * **RyanCavanaugh** added label `Domain: Mapped Types`
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/45560#issuecomment-4676880644) **mwg-ofx** said "I wonder if such a change could be reconsidered after the Go migration is complete, given the significant speed boost it provides."
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/45560#issuecomment-4682464840) **RyanCavanaugh** said "By "unacceptable perf hits" we mean like 40%, and people are already complaining that tsgo isn't fast enough in material-ui."
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#45629](https://github.com/microsoft/TypeScript/issues/45629) (Open, `Bug`, `Domain: Index Types`)

**Only number index type is inferred from \`any\` computed property key**

*TypeScript infers only a numeric index signature for objects with any-typed computed keys, disallowing string access.*

 * **andrewbranch** added label `Fix Available`
 * [4.9 years ago](https://github.com/microsoft/TypeScript/issues/45629#issuecomment-912011451) **vepanimas** agreed that replacing a numeric indexer with a string indexer could break something, suggested adding a `{ [x: string | number | symbol]: T }` instead, and apologized for missing the comment in the PR
 * **RyanCavanaugh** added label `Domain: Index Types`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#46140](https://github.com/microsoft/TypeScript/issues/46140) (Open, `Suggestion`, `Help Wanted`, `Experience Enhancement`, **gabritto**)

**Inverted \`Promise\` should warn like it does without inverting**

*Emit a warning when negating a Promise without await, similar to non-negated Promise checks.*

 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/46140#issuecomment-2375375422) **gabritto** affirmed reasoning and suggested creating a PR with the original code to run extended tests for promises and negation
 * **typescript-bot** added label `Fix Available`
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/46140#issuecomment-2376273721) **tjenkinson** said "@gabritto sounds great opened https://github.com/microsoft/TypeScript/pull/60068 and it's back to checking everything"
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#46668](https://github.com/microsoft/TypeScript/issues/46668) (Open, `Bug`, `Rescheduled`, `Domain: classes`, **rbuckton**)

**Private field check narrows generic class too far**

*Private field checks in generic classes erroneously narrow type arguments to any instead of preserving their constraints.*

 * (2 years ago) **RyanCavanaugh** added label `Domain: classes`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#46709](https://github.com/microsoft/TypeScript/issues/46709) (Open, `Bug`, `Domain: This-Typing`, **Copilot**)

**False positive 'This condition will always return false' comparing \`this\` with an instance of a subclass**

*TypeScript incorrectly reports a “condition will always return false” error when comparing this to an instance of a subclass.*

 * (1 year ago) **typescript-bot** added labels `Fix Available`, `Fix Available`
 * **RyanCavanaugh** added label `Domain: This-Typing`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#47679](https://github.com/microsoft/TypeScript/issues/47679) (Open, `Needs Investigation`, `Rescheduled`, **sandersn**)

**TypeScript class method decorator not rendering properly in version \>= 1\.63\.2**

*VS Code version 1.63.2 and later fails to properly render TypeScript class method decorators in hover documentation.*

 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/47679#issuecomment-3495256581) **apendua** noted the key differentiator was the presence of '<<' in resolving ambiguity and preserving backwards compatibility, and mentioned that triple backticks could be used instead of EOF
 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/47679#issuecomment-3495360975) **lionel-rowe** clarified that the underlying bug was related to '@' in multiline JSDoc tags rather than backticks or '<<', and that without fixing JSDoc parsing both heredoc and code fences would be affected
 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/47679#issuecomment-3495389667) **apendua** noted that a previous attempt to implement vanilla markdown was rejected due to potential breakage of JSDoc comments with unbalanced backticks, and that lack of consensus on syntax, rather than multiline parsing, is blocking progress
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#48070](https://github.com/microsoft/TypeScript/issues/48070) (Open, `Bug`, `Domain: Conditional Types`, `Rescheduled`, **ahejlsberg**)

**Conditional type evaluation of type aliases produces different result than their equivalent substitution**

*TypeScript’s conditional type aliases produce different extends comparison results than their inline equivalents*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/48070#issuecomment-2745391757) **bergwerf** questioned why `Number_Or_Nil<T>` evaluated to `number` when `T` includes `number[]`
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/48070#issuecomment-2745394778) **jcalz** clarified that the behavior was intended due to distributive conditional types and that the generic parameter and specific type named T behave differently
 * **RyanCavanaugh** added label `Domain: Conditional Types`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#48443](https://github.com/microsoft/TypeScript/issues/48443) (Open, `Bug`, `Domain: Something Else`, **Copilot**)

**TSC \-\-showConfig throws error instead of listing configuration**

*tsc --showConfig on a tsconfig.json with only include patterns returns a TS18003 'no inputs found' error instead of showing the config.*

 * **RyanCavanaugh** assigned to **Copilot**
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: Something Else`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#48515](https://github.com/microsoft/TypeScript/issues/48515) (Open, `Bug`, `Domain: Decorators`, **rbuckton**)

**Decorators broken with private fields, generated code has syntax error**

*Applying a decorator that references a private static field causes TypeScript to emit invalid JavaScript with a syntax error.*

 * [3 years ago](https://github.com/microsoft/TypeScript/issues/48515#issuecomment-1675474247) **evanw** explained that TypeScript experimental decorators run after class initialization and lack computed property name semantics—unlike new JavaScript decorators—causing the esbuild bug
 * [3 years ago](https://github.com/microsoft/TypeScript/issues/48515#issuecomment-1675654243) **rbuckton** explained that experimental decorators run after class initialization so referencing the class name in decorators works but not in computed property names, contrasted this with Stage 3 decorators, noted issues with legacy decorator emit and static initializers, and suggested making yield/await in decorators a syntax error under `--experimentalDecorators`
 * **RyanCavanaugh** added label `Domain: Decorators`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#50603](https://github.com/microsoft/TypeScript/issues/50603) (Open, `Bug`, `Domain: check: Control Flow`, `Rescheduled`, **iisaduan**)

**No error on unconstrained type parameter in \`\>\` comparison**

*Comparing an unconstrained generic T with '>' mistakenly produces an undefined-object error in TypeScript 4.8.*

 * (2 years ago) **iisaduan** set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.6.0`
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#50635](https://github.com/microsoft/TypeScript/issues/50635) (Open, `Bug`, `Domain: check: Type Inference`, `Rescheduled`, `Has Repro`, **andrewbranch**)

**Regression in 4\.8 where string union type widens to string**

*String union types now incorrectly widen to string in TypeScript 4.8, regressing the behavior from 4.7.4.*

 * (2 years ago) **RyanCavanaugh** added label `Domain: Type Inference`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#50754](https://github.com/microsoft/TypeScript/issues/50754) (Open, `Needs Investigation`, `Rescheduled`, **weswigham**)

**Unexpected overload signature rejection since TypeScript 4\.8\.x**

*TypeScript 4.8 rejects the childByTag overload returning HTMLElementTagNameMap[Lowercase<K>] as incompatible with its implementation despite covariance.*

 * (2.4 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#50787](https://github.com/microsoft/TypeScript/issues/50787) (Open, `Needs Investigation`, **andrewbranch**)

**Literal strings with generics are inconsistant when strictNullChecks is false**

*In TypeScript 4.8.2 with strictNullChecks off, chaining two generic functions widens string literal types and misinfers the Pick<Model, 's'> result.*

 * [3.9 years ago](https://github.com/microsoft/TypeScript/issues/50787#issuecomment-1251541105) **andrewbranch** said "Adding a T extends {} constraint to transform makes it repro in --strictNullChecks too."
 * **typescript-bot** added label `Fix Available`
 * [3.9 years ago](https://github.com/microsoft/TypeScript/issues/50787#issuecomment-1251667351) **andrewbranch** said "I added a fix to #50759, which needs a review. It’s the same fix for #50635, but from one additional call site."
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#51162](https://github.com/microsoft/TypeScript/issues/51162) (Open, `Bug`, `Rescheduled`, `Domain: Crashes`, **navya9singh**)

**TS Server fatal error:  Maximum call stack size exceeded**

*VSCode’s JS/TS language service repeatedly crashes with a Maximum call stack size exceeded error when opening a JavaScript file.*

 * (2 years ago) **RyanCavanaugh** added label `Domain: Crashes`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#51525](https://github.com/microsoft/TypeScript/issues/51525) (Open, `Suggestion`, `Domain: Performance`, `Experimentation Needed`, `Rescheduled`, **weswigham**)

**Experiment with tracking which entities actually may be narrowed**

*Experiment with tracking which variables get narrowed in Pyright to avoid redundant control-flow walks at cost of memory overhead.*

 * (2 years ago) **RyanCavanaugh** added label `Rescheduled`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#52892](https://github.com/microsoft/TypeScript/issues/52892) (Open, `Needs Investigation`, `Rescheduled`, **jakebailey**)

**Instantiation expression inside nested classes produces unexpected circular reference error**

*Generic instantiation of a nested static class erroneously triggers a circular reference error in TypeScript.*

 * (2 years ago) **RyanCavanaugh** set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#53179](https://github.com/microsoft/TypeScript/issues/53179) (Open, `Needs Investigation`, `Rescheduled`, **weswigham**)

**Range Error: Maximum call stack size exceeded while compiling our code**

*Recursive conditional types mapping Mongoose schema definitions cause tsc RangeError: Maximum call stack size exceeded in TypeScript 4.6.4.*

 * (2.4 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#53343](https://github.com/microsoft/TypeScript/issues/53343) (Open, `Bug`, `Domain: check: Type Inference`, `Rescheduled`, **weswigham**)

**Record keys are inferred to be values when using \`extends string\` conditional in a generic type**

*TypeScript incorrectly infers record key names as values when a generic type conditionally extends string*

 * (2 years ago) **RyanCavanaugh** added label `Domain: Type Inference`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#53559](https://github.com/microsoft/TypeScript/issues/53559) (Open, `Bug`, `Domain: Error Messages`, `Rescheduled`, **DanielRosenwasser**)

**Error for explicit return type with no return statements is misleading**

*Compiler error erroneously disallows functions with explicit return types and no return statements despite supporting unknown annotations.*

 * (2.4 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#54500](https://github.com/microsoft/TypeScript/issues/54500) (Open, `Discussion`)

**6\.0 Deprecation List**

*Proposed deprecations of outdated TypeScript 6.0 compiler options, with full removal planned for version 7.0.*

 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3927313490) **HolgerJeromin** expressed concern about the removal of module:none in TypeScript 6.0-beta and its potential to lock projects on older versions
 * [23 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-4029987037) **n9** expressed agreement and mentioned that the amd module format with outFile is useful for enterprise systems serving as foundation for internal DSLs
 * [23 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-4039208659) **GabenGar** mocked the addition of 'enterprise' and suggested allocating budget to address tech debt
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#54805](https://github.com/microsoft/TypeScript/issues/54805) (Open, `Bug`, `Domain: check: Type Inference`, `Rescheduled`, **weswigham**)

**Version 5\.0\.4 \-\> 5\.1\.3 Regression when using generic types**

*Upgrading from TypeScript 5.0.4 to 5.1.3 causes generic LexicalCommand payload types to be inferred incorrectly.*

 * (2 years ago) **RyanCavanaugh** added label `Domain: Type Inference`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#54879](https://github.com/microsoft/TypeScript/issues/54879) (Open, `Needs Investigation`, `Rescheduled`, **weswigham**)

**A function that returns a class with a property getter is unusable via a declaration file \(TS2611\)**

*Returning a class with a property getter from a function produces unusable declaration files and TS2611 errors.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/54879#issuecomment-2153512240) **Andarist** said "Can't say how close that setup is to this issue here but the playground that you shared is sufficiently different from this issue here, I think."
 * (2 years ago) **RyanCavanaugh** set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#55091](https://github.com/microsoft/TypeScript/issues/55091) (Open, `Bug`, `Help Wanted`, `Domain: enum`)

**Enum value \`1 / 0\` incorrectly transformed if there is \`Infinity\` declared in scope**

*A local Infinity variable shadows the global Infinity constant, so enum member initialized with 1/0 incorrectly uses the local value.*

 * (35 weeks ago) **RyanCavanaugh** set milestone to `Dormant`, and removed from milestone `Backlog`
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#55217](https://github.com/microsoft/TypeScript/issues/55217) (Open, `Bug`, `Domain: Conditional Types`, `Rescheduled`, **jakebailey**)

**Conditional type triggers "No error for last overload signature" exception**

*A conditional type expression in TypeScript v5.0.4 and later triggers a 'No error for last overload signature' exception.*

 * (2 years ago) **RyanCavanaugh** added label `Domain: Conditional Types`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#55500](https://github.com/microsoft/TypeScript/issues/55500) (Open, `Bug`, `Rescheduled`, `Domain: classes`, **rbuckton**)

**Incorrect error reported when using \`class extends null\` and re\-opening interface**

*TypeScript incorrectly reports a static side extension error for classes extending null when reopened via an interface.*

 * (2 years ago) **RyanCavanaugh** added label `Domain: classes`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#55899](https://github.com/microsoft/TypeScript/issues/55899) (Open, `Bug`, `Help Wanted`, `Rescheduled`, `Effort: Casual`, `Domain: classes`, **sandersn**)

**Indexing/element access on \`super\` avoids instance property checks**

*Bracket notation super['yadda'] bypasses TypeScript's instance property checks, causing inconsistent behavior compared to dot notation.*

 * (2 years ago) **RyanCavanaugh** added label `Domain: classes`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#56081](https://github.com/microsoft/TypeScript/issues/56081) (Open, `Needs Investigation`, `Rescheduled`, **jakebailey**)

**Memory Leak / Infinite Recursion\. TS hangs, TSC never finishes, VSCode and Intellisense dies\. **

*Importing Prisma.UserCreateInput into useForm causes infinite recursion in TypeScript, making tsc and IntelliSense hang.*

 * (1.7 years ago) **PranavSenthilnathan** assigned to **jakebailey**, and unassigned **PranavSenthilnathan**
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/56081#issuecomment-2761339603) **nik-webdevelop** described that tsc hung and WebStorm intellisense got stuck due to an Icon property declared as FC<SVGProps<SVGElement>>, and noted commenting out that property resolved the issue
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#56615](https://github.com/microsoft/TypeScript/issues/56615) (Open, `Bug`, `Domain: JSDoc`, `Experience Enhancement`, **sandersn**)

**JSDocs don't support properties on functions**

*JSDoc lacks support for function properties, preventing JavaScript developers from documenting TypeScript-like function interfaces such as Redux action creators.*

 * **typescript-bot** added label `Fix Available`
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/56615#issuecomment-2831691826) **zinefer** described struggling to apply JSDOC comments to functions and shared a playground example showing unresolved types
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#57229](https://github.com/microsoft/TypeScript/issues/57229) (Open, `Bug`, `Breaking Change`, `Rescheduled`, `Domain: Node ESM`, **weswigham**)

**\.d\.json\.ts file \(allowArbitraryExtensions\) not working correctly when importing from ESM file with node16/nodenext module setting**

*allowArbitraryExtensions does not correctly support importing .d.json.ts files in Node16/Nodenext ESM modules.*

 * (2 years ago) **typescript-bot** added labels `Fix Available`, `Fix Available`
 * **RyanCavanaugh** added label `Domain: Node ESM`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#58130](https://github.com/microsoft/TypeScript/issues/58130) (Open, `Bug`, `Domain: Something Else`)

**Incorrect Chinese Translation for 'initializer' and Incorrect Use of Chinese Quotation Marks**

*Update Chinese translation of 'initializer' and replace Chinese quotes with English ones to enhance clarity*

 * **RyanCavanaugh** added to milestone `Dormant`
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: Something Else`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#58353](https://github.com/microsoft/TypeScript/issues/58353) (Open, `Needs Investigation`, **andrewbranch**)

**When relatively importing a \`\.d\.ts\` file in a declaration file, TypeScript loads a \`\.ts\` file instead**

*TypeScript incorrectly resolves relative imports of .d.ts files in declaration files by loading their .ts counterparts.*

 * **RyanCavanaugh** added to milestone `TypeScript 5.6.0`
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/58353#issuecomment-2100591969) **lucacasonato** described a workaround that emitted .js and .d.ts files into a separate directory causing import.meta.url issues, and proposed emitting only .d.ts files into a subdirectory while keeping .js files next to .ts files
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#58453](https://github.com/microsoft/TypeScript/issues/58453) (Open, `Suggestion`, `Committed`)

**Add a rule to the compiler options to disallow the \`assert\` keyword for import attributes**

*Add a new compiler option disallowAssertKeywords to prevent usage of the assert keyword in import attributes.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/58453#issuecomment-2116149939) **RyanCavanaugh** said "I'd need to understand how someone would be unintentionally writing assert in an import statement to prioritize those mitigations"
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/58453#issuecomment-2116285612) **robpalme** noted that Node LTS supports `with` while Node Latest and upcoming Chrome versions do not support `assert`, inferred that continued `assert` usage is likely unintentional, and suggested that TypeScript provide guidance toward using `with`.
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/58453#issuecomment-2257287599) **petamoriken** noted that TC39 agreed to remove `assert` from the import attributes proposal
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#58542](https://github.com/microsoft/TypeScript/issues/58542) (Open, `Bug`, `Domain: JSDoc`, **sandersn**)

**Bad error when using \`import\(\)\` type within JSDoc tag \`@implements\`**

*TypeScript reports syntax errors when using import() types directly in JSDoc @implements tags.*

 * **DanielRosenwasser** added label `Bug`
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/58542#issuecomment-2372599311) **jaydenseric** said "See also https://github.com/microsoft/TypeScript/issues/49905 ."
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#58924](https://github.com/microsoft/TypeScript/issues/58924) (Open, `Bug`, `Help Wanted`, `Domain: API: Transforms`, `Crash`, `Effort: Casual`, **rbuckton**)

**Crashes on transform and parse \(from assertion/debug failures\)**

*TypeScript crashes during transformation with Debug Failure 'Use modifierVisitor' errors in v5.3–5.4.5 and different debug failures in v4.7–5.2.*

 * (2.1 years ago) **rbuckton** closed the issue
 * (2.1 years ago) **rbuckton** reopened the issue
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/58924#issuecomment-2449585789) **codewithsupra** summarized crash details for TypeScript versions 4.7 to 5.4.5 when using `accessor` in enum, var, or function with examples
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#59346](https://github.com/microsoft/TypeScript/issues/59346) (Open, `Suggestion`, **ahejlsberg**)

**\[proposal\] Non widened string values should be valid enum values, like widened string values**

*Allow non-widened string constants as valid TypeScript enum member values, consistent with widened string support.*

 * (2 years ago) **ahejlsberg** added labels `Suggestion`, `Fix Available`, and set milestone to `TypeScript 5.7.0`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#59902](https://github.com/microsoft/TypeScript/issues/59902) (Open, `Bug`, `Domain: Mapped Types`, **ahejlsberg**)

**Removing optional modifier in homomorphic mapped types does not work in generic contexts since 5\.5\.x**

*Generic homomorphic mapped types in TypeScript 5.5 ignore the -? operator, leaving optional properties and undefined in value types.*

 * **RyanCavanaugh** added to milestone `TypeScript 5.7.0`
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: Mapped Types`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#60419](https://github.com/microsoft/TypeScript/issues/60419) (Open, `Needs Investigation`, **navya9singh**)

**Paste with imports duplicates imports for namespace imports**

*Pasting code that references an exported symbol causes a duplicate import rather than reusing existing namespace import.*

 * (44 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Backlog`
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#60598](https://github.com/microsoft/TypeScript/issues/60598) (Open, `Needs Investigation`, **andrewbranch**)

**Dynamically importing JSON should require import attribute with node16/nodenext**

*TypeScript incorrectly permits dynamic JSON imports under node16/nodenext with resolveJsonModule despite Node requiring import attributes.*

 * **RyanCavanaugh** added label `Needs Investigation`
 * **andrewbranch** added to milestone `TypeScript 5.8.0`
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#60758](https://github.com/microsoft/TypeScript/issues/60758) (Open, `Bug`, `Domain: Declaration Emit`, **weswigham**)

**instantiation expression usage leading to an invalid d\.ts file generation**

*TypeScript 5.7.2 generates an invalid d.ts for isBar by referencing an undefined generic T in its declaration.*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/60758#issuecomment-2545658108) **dragomirtitian** provided a simpler reproduction and noted inconsistent type resolution for predicate return types with playground links
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#60908](https://github.com/microsoft/TypeScript/issues/60908) (Open, `Bug`, `Help Wanted`, `Domain: JSDoc`)

**Unexpected "'Type' is declared but its value is never read\." error with jsdoc @import syntax**

*JSDoc @import type causes TS6133 'declared but its value is never read' error despite using the type in @type annotation.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/60908#issuecomment-2827525375) **regseb** provided a Bug Workbench testcase demonstrating that foo was reported as unused under nodenext settings and that the error disappeared when nodenext flags were removed or foo was referenced twice
 * (1.3 years ago) **jakebailey** reopened the issue
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#61041](https://github.com/microsoft/TypeScript/issues/61041) (Open, `Bug`, `Domain: check: Type Inference`, **weswigham**)

**Type variables in type abstractions are not properly concretized**

*TypeScript 5.0.4 no longer properly resolves type variables in nested generics, causing unknown return types and missing type errors.*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/61041#issuecomment-2613172191) **RyanCavanaugh** agreed with @jcalz on both counts, characterized the first example as overly abstract and recommended NoInfer, and noted that the second example leaked a type parameter producing an invalid declaration file
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#61216](https://github.com/microsoft/TypeScript/issues/61216) (Open, `Suggestion`, `Help Wanted`, `Committed`)

**Support source phase imports**

*Enable TC39 source phase imports in TypeScript to allow importing raw WebAssembly modules directly.*

 * (1.4 years ago) **RyanCavanaugh** added label `Help Wanted`, and set milestone to `TypeScript 5.9.0`
 * **typescript-automation[bot]** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#61426](https://github.com/microsoft/TypeScript/issues/61426) (Open, `Suggestion`, `Help Wanted`, `Experience Enhancement`, **Copilot**)

**Intellisense: deprioritise native function methods**

*Adjust TypeScript IntelliSense to prioritize custom function properties over built-in native methods in autocomplete suggestions.*

 * **typescript-bot** added label `Fix Available`
 * (1.1 years ago) **RyanCavanaugh** assigned to **Copilot**, and unassigned **Copilot**
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#61448](https://github.com/microsoft/TypeScript/issues/61448) (Open, `Help Wanted`, `Domain: lib.d.ts`, `Possible Improvement`, **rbuckton**)

**Add types for \`String\.{matchAll,replaceAll}\` with a well known symbol**

*Add TypeScript type definitions enabling String.matchAll and replaceAll to accept objects implementing Symbol.matchAll or Symbol.replace instead of only RegExp.*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/61448#issuecomment-2753163540) **segevfiner** said "Exactly. Those were simply added in later ES versions and seems to have been forgotten. I made a PR to add them. But I think I need to update some tests to complete it."
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#61524](https://github.com/microsoft/TypeScript/issues/61524) (Open, `Bug`, `Help Wanted`, `Domain: check: Variance Relationships`)

**Error: Debug Failure\. No error for last overload signature**

*TypeScript nightly v5.9.0-dev crashes with "Debug Failure. No error for last overload signature" during overload resolution in a generic function.*

 * [29 weeks ago](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-3812609059) **Andarist** requested commit information to reproduce the issue
 * [29 weeks ago](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-3814281494) **Andarist** provided a TypeScript reproduction snippet extracted from kettanaito's issue report
 * [28 weeks ago](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-3816433446) **kettanaito** provided reproduction steps for the issue, linking to a pull request and test commands
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#61714](https://github.com/microsoft/TypeScript/issues/61714) (Open, `Bug`, `Help Wanted`, `Domain: API: Transforms`, **Copilot**)

**\`using\` transform throws when a for body binding shadows the for head binding**

*TypeScript’s using-for loop transform incorrectly throws a redeclaration error when the loop variable is shadowed in the loop body.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/61714#issuecomment-3001177653) **RyanCavanaugh** suggested renaming the inner shadowing variable in ES5-transpiled loop code
 * (1.1 years ago) **RyanCavanaugh** added label `Domain: Transforms`, and assigned to **Copilot**
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#61891](https://github.com/microsoft/TypeScript/issues/61891) (Open, `Bug`, `Help Wanted`, `Domain: check: Control Flow`, **Copilot**)

**Namespaces: use before declaration is not reported**

*TypeScript does not flag use-before-declaration in nested namespaces, causing undetected runtime errors.*

 * **RyanCavanaugh** assigned to **Copilot**
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/61891#issuecomment-2997918268) **Copilot** reported an unexpected error while attempting to work on issue #61891 and provided an error identifier
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#61944](https://github.com/microsoft/TypeScript/issues/61944) (Open, `Bug`, `Help Wanted`, `Domain: Declaration Emit`, **Copilot**)

**Incorrect type declarations for a constant inside a namespace merged with an enum**

*TypeScript generates invalid declaration files for constants in a namespace merged with an enum after version 3.1.0-dev.20180907.*

 * **typescript-bot** added label `Fix Available`
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/61944#issuecomment-3034785325) **mehmadullahsheikh** requested to be assigned to the issue
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#61971](https://github.com/microsoft/TypeScript/issues/61971) (Open, `Bug`, `Help Wanted`, `Domain: Error Messages`, **Copilot**)

**Diagnostic code \`69010\` may be typo of \`6910\`?**

*TypeScript’s diagnostic code 69010 appears to be mistakenly assigned and should be 6910.*

 * (1.1 years ago) **typescript-bot** added labels `Fix Available`, `Fix Available`
 * **RyanCavanaugh** added label `Domain: Error Messages`
 * **jakebailey** removed label `Fix Available`

### [Issue microsoft/TypeScript#62027](https://github.com/microsoft/TypeScript/issues/62027) (Open, `Bug`, `Help Wanted`, `Domain: JSDoc`, **Copilot**)

**JSDoc \`@import\` causes \`getCompletionEntryDetails\` to crash**

*TypeScript 5.5's JSDoc @import in a JavaScript file causes getCompletionEntryDetails to crash when using getCompletionsAtPosition.*

 * **RyanCavanaugh** assigned to **Copilot**
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * **jakebailey** removed label `Fix Available`

