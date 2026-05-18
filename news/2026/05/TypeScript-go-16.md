# Report for 2026-05-16 (Saturday, May 16th, 2026)

9 different users commented on 58 different issues.

## Recommended Actions

 * Response Recommended
    * @Withered-Flower-0422 reported tsgo throws an error when awaiting an empty array in [microsoft/TypeScript-go#3936](https://github.com/microsoft/TypeScript-go/issues/3936#issuecomment-4469628013)

## Activity Summary

### [Issue microsoft/TypeScript-go#2201](https://github.com/microsoft/TypeScript-go/issues/2201) (Closed, `Domain: Editor`, **Copilot**)

**Bad formatting of multiline ternary expression**

*Formatting multiline ternary expressions with tabs results in inconsistent mixing of tabs and spaces.*

 * **DanielRosenwasser** added label `Domain: Editor`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2201#issuecomment-4445042494) **antichris** asked where the resolution is tracked and requested a link to the new issue or PR
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2201#issuecomment-4445210196) **DanielRosenwasser** assumed a formatting/printing PR introduced the change, manually validated the examples, and asked if the issue persisted
 * [today](https://github.com/microsoft/TypeScript-go/issues/2201#issuecomment-4467798308) **antichris** confirmed that formatting was correct, withdrew the ticket, and said they would fully switch to tsgo

### [PR microsoft/TypeScript-go#2928](https://github.com/microsoft/TypeScript-go/pull/2928) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix crash related to tuple rest arity**

*Prevent nil pointer dereference during variadic tuple rest type inference by adding nil guards and a new compiler test case.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/2928#issuecomment-4269802788) **RyanCavanaugh** said "Hoisting comment: This is a fix for https://github.com/microsoft/TypeScript/issues/63199"
 * (1 month ago) **RyanCavanaugh** set milestones to `TypeScript 7.0 RC`, `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/2928#issuecomment-4467971908) **jakebailey** said "Also #3917 and #3883, might need to consolidate tests and/or fixes"
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3883](https://github.com/microsoft/TypeScript-go/issues/3883) (Open, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when inferring \[\.\.\.rest, \.\.\.T\] from a tuple shorter than fixed\-arity constraint**

*tsgo panics from slice bounds error when inferring rest and generic types from too-short tuples*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3883#issuecomment-4467960569) **jakebailey** said "I think this effectively https://github.com/microsoft/typescript-go/pull/2928, https://github.com/microsoft/TypeScript/issues/63199"

### [Issue microsoft/TypeScript-go#3884](https://github.com/microsoft/TypeScript-go/issues/3884) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when a JS class has @augments or @extends JSDoc and empty extends clause**

*tsgo panics when a JS class uses @augments or @extends JSDoc with an empty extends clause*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3885](https://github.com/microsoft/TypeScript-go/issues/3885) (Closed, `Crash`)

**tsgo panics when a get/set accessor with an illegal async modifier contains for\-await\-of**

*tsgo panics when checking a get/set accessor illegally declared async containing a for-await-of loop*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3886](https://github.com/microsoft/TypeScript-go/issues/3886) (Open, `Crash`, **jakebailey**, **Copilot**)

**tsgo printer panics when emitting declarations for CommonJS files with numeric export names**

*tsgo printer panics when emitting declarations for CommonJS files with numeric export names*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3887](https://github.com/microsoft/TypeScript-go/issues/3887) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo printer panics during "JSX expressions must have one parent element" recovery**

*The tsgo printer panics during JSX recovery when encountering an unhandled binary expression in a JSX attribute.*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3888](https://github.com/microsoft/TypeScript-go/issues/3888) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics with interface conversion error when a @this appears inside of a @typedef comment**

*Parsing a JSDoc typedef comment that contains a @this tag triggers an interface conversion panic in tsgo.*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3889](https://github.com/microsoft/TypeScript-go/issues/3889) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when a @callback / @overload @param has a qualified name**

*tsgo panics with an unhandled QualifiedName case when a @callback or @overload @param uses a qualified name*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3889#issuecomment-4467242662) **jakebailey** said "How are you finding all of these? Is this some specific codebase? Are you fuzzing?"
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3890](https://github.com/microsoft/TypeScript-go/issues/3890) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when a @this JSDoc tag is combined with a literal this parameter**

*tsgo panics with an index out of range error when encountering a JSDoc @this tag alongside a literal this parameter*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3891](https://github.com/microsoft/TypeScript-go/issues/3891) (Open, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when an anonymous class declaration has a member decorator when downleveling to ES2022**

*tsgo panics with a debug assertion failure when downleveling anonymous classes with member decorators to ES2022*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3892](https://github.com/microsoft/TypeScript-go/issues/3892) (Closed, **jakebailey**, **Copilot**)

**tsgo hangs on large template literal types with combinatorial explosion**

*tsgo hangs indefinitely when compiling large combinatorial template literal types that tsc rejects as too complex.*

 * created by **mariusschulz**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3893](https://github.com/microsoft/TypeScript-go/issues/3893) (Closed)

**tsgo emits broken JS when a \.tsx file's only JSX element is self\-closing**

*When transpiling a TSX file containing only a self-closing JSX element, tsgo omits the necessary jsx import, producing invalid JavaScript.*

 * created by **mariusschulz**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3895](https://github.com/microsoft/TypeScript-go/issues/3895) (Open, **jakebailey**, **Copilot**)

**tsgo's Uppercase/Lowercase intrinsic types don't apply Unicode special case mappings**

*tsgo's Uppercase and Lowercase intrinsic types omit Unicode special case mappings, causing incorrect type errors for characters like ß.*

 * created by **mariusschulz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3895#issuecomment-4467314515) **jakebailey** said "This is effectively https://github.com/microsoft/typescript-go/issues/3489"
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3896](https://github.com/microsoft/TypeScript-go/issues/3896) (Open, **jakebailey**, **Copilot**)

**tsgo emits \-NaN for enum members with NaN value in declaration output**

*tsgo outputs -NaN instead of normalizing NaN values when emitting enum member declarations initialized with -NaN.*

 * created by **mariusschulz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3896#issuecomment-4467305977) **jakebailey** said "I'm not sure this is really a bug, but rather an improvement in node reuse"
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3898](https://github.com/microsoft/TypeScript-go/issues/3898) (Open, **jakebailey**, **Copilot**)

**tsgo creates a distinct enum literal type for each NaN\-valued enum member**

*tsgo treats NaN-valued enum members as distinct literal types, causing assignment errors between them*

 * created by **mariusschulz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3898#issuecomment-4467309242) **jakebailey** said "That or NaN is not NaN and is being keyed somewhere (Go maps hash every NaN as new items)"
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3899](https://github.com/microsoft/TypeScript-go/issues/3899) (Open, **jakebailey**, **Copilot**)

**tsgo breaks type soundness for lone\-surrogate string literals**

*tsgo improperly accepts assignments between different lone-surrogate string literals, breaking TypeScript’s type soundness.*

 * created by **mariusschulz**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3900](https://github.com/microsoft/TypeScript-go/issues/3900) (Open, `Crash`, **jakebailey**, **Copilot**)

**tsgo source\-map emit panics for an unclosed block**

*Emitting source maps in tsgo causes a slice bounds panic when encountering an unclosed code block.*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3901](https://github.com/microsoft/TypeScript-go/issues/3901) (Closed, `Crash`)

**tsgo panics when emitting a \`do\` statement with no \`while\`**

*tsgo panics with slice bounds out of range when printing a do statement missing its while clause*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3902](https://github.com/microsoft/TypeScript-go/issues/3902) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics for a contextually typed function with optional and rest params**

*tsgo panics with a makeslice: len out of range error when type-checking a function using optional and rest parameters*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3903](https://github.com/microsoft/TypeScript-go/issues/3903) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics for rest properties in catch binding when targeting ES2017**

*tsgo crashes when transforming object rest properties in catch bindings targeting ES2017 because of an AST conversion error.*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3904](https://github.com/microsoft/TypeScript-go/issues/3904) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when a type\-only export is the body of an if statement**

*tsgo crashes with a nil pointer dereference when an if statement’s body is a type-only export.*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3905](https://github.com/microsoft/TypeScript-go/issues/3905) (Closed, `Crash`)

**tsgo panics when destructuring pattern has no leaf pattern and targeting ES2017**

*tsgo panics with index-out-of-range error when destructuring pattern has no leaf on ES2017 target*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3906](https://github.com/microsoft/TypeScript-go/issues/3906) (Open, **jakebailey**, **Copilot**)

**tsgo emits incorrect string value when encountering a backslash before a non\-special character**

*tsgo emits invalid Unicode escape sequences for enum string values containing backslashes before non-special characters.*

 * created by **mariusschulz**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3907](https://github.com/microsoft/TypeScript-go/issues/3907) (Open, **jakebailey**, **Copilot**)

**tsgo declaration emit drops readonly from method shorthands and outer properties in \`as const\` object literal**

*tsgo’s declaration emitter drops readonly modifiers on methods and outer properties in as const object literals.*

 * created by **mariusschulz**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3908](https://github.com/microsoft/TypeScript-go/issues/3908) (Open, **jakebailey**, **Copilot**)

**tsgo incorrectly renames arguments destructuring property when targeting ES2015**

*When targeting ES2015, tsgo wrongly renames destructured property 'arguments' to 'arguments_1' in async functions.*

 * created by **mariusschulz**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3909](https://github.com/microsoft/TypeScript-go/issues/3909) (Closed, **jakebailey**, **Copilot**)

**tsgo loses all type narrowing in a \`switch \(typeof x\)\` when any clause is \`case ""\`**

*tsgo’s type checker loses type narrowing in a switch(typeof x) when a case uses an empty string, causing incorrect errors.*

 * created by **mariusschulz**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3910](https://github.com/microsoft/TypeScript-go/pull/3910) (Open, **jakebailey**, **Copilot**)

**Fix incorrect renaming of \`arguments\` in non\-reference positions in async downlevel**

*The async transformer for ES2015 downleveling improperly renames destructured and JSX attribute 'arguments' identifiers due to missing guard checks.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3911](https://github.com/microsoft/TypeScript-go/pull/3911) (Open, **jakebailey**, **Copilot**)

**Fix scanEscapeSequence for multi\-byte UTF\-8 characters after backslash**

*Fix scanEscapeSequence to correctly decode multi-byte UTF-8 escape sequences including U+2028/U+2029 and set containsNonASCII=true.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3912](https://github.com/microsoft/TypeScript-go/pull/3912) (Open, **jakebailey**, **Copilot**)

**Fix type soundness for lone\-surrogate string literals**

*Use CESU-8 encoding and decoding to preserve distinct lone-surrogate string literals and enforce correct type mismatches.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3913](https://github.com/microsoft/TypeScript-go/pull/3913) (Closed)

**fix\(3885\): remove extra panic for for\-await\-of inside async get/set accessor**

*Remove unnecessary panic when using for-await-of loops inside async get or set accessors*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3914](https://github.com/microsoft/TypeScript-go/pull/3914) (Closed)

**fix\(3901\): handle out\-of\-bounds pos in skip trivia**

*Ensure the skip trivia function gracefully handles positions outside the valid text range*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3915](https://github.com/microsoft/TypeScript-go/pull/3915) (Closed)

**fix\(3893\): fix missing JSX runtime import**

*Add the missing JSX runtime import to restore proper JSX functionality.*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3916](https://github.com/microsoft/TypeScript-go/pull/3916) (Closed)

**fix\(3905\): fix out\-of\-bounds access when flattening destructuring with no bindings**

*Prevent out-of-bounds error when flattening destructured assignments with no bindings.*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3917](https://github.com/microsoft/TypeScript-go/pull/3917) (Open, **jakebailey**, **Copilot**)

**Fix panic when inferring \[\.\.\.rest, \.\.\.T\] from tuple shorter than fixed\-arity constraint**

*Slice indices in [...rest, ...T] inference go negative and panic when the source tuple is shorter than the arity constraint.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3917#issuecomment-4470720336) **ahejlsberg** said "@copilot resolve the merge conflicts in this pull request"
 * [later](https://github.com/microsoft/TypeScript-go/pull/3917#issuecomment-4470768518) **Copilot** resolved the merge conflict in internal/checker/inference.go and combined the bounds check with the restType guard

### [PR microsoft/TypeScript-go#3918](https://github.com/microsoft/TypeScript-go/pull/3918) (Closed, **jakebailey**, **Copilot**)

**Fix panic when JS class has @augments/@extends JSDoc with empty extends clause**

*Guard against empty extends clauses when checking JSDoc @augments/@extends tags to prevent index-out-of-range panics and add related compiler tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3919](https://github.com/microsoft/TypeScript-go/pull/3919) (Open, **jakebailey**, **Copilot**)

**Handle numeric literal export names in declaration emit**

*Fix declaration emit to convert numeric export names to string literals, preventing printer panics and invalid syntax.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3919#issuecomment-4470587854) **ahejlsberg** said "@copilot Please make the requested changes."
 * [later](https://github.com/microsoft/TypeScript-go/pull/3919#issuecomment-4470705583) **ahejlsberg** agreed that converting numeric literals to string literals was best and contrasted with Strada's approach

### [PR microsoft/TypeScript-go#3920](https://github.com/microsoft/TypeScript-go/pull/3920) (Closed, **jakebailey**, **Copilot**)

**Fix printer panic on unexpected JSX attribute value during error recovery**

*Modify emitJsxAttributeValue to emit arbitrary expression nodes instead of panicking on malformed JSX attributes and add a reproducing test.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3921](https://github.com/microsoft/TypeScript-go/pull/3921) (Closed, **jakebailey**, **Copilot**)

**Fix panic when @this tag appears inside @typedef JSDoc comment**

*Skip non-property JSDoc tags such as @this in typedef comments to avoid parser panics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3922](https://github.com/microsoft/TypeScript-go/pull/3922) (Closed, **jakebailey**, **Copilot**)

**Fix panic when @callback/@overload @param has a qualified name**

*The reparser treated JSDoc parameters with qualified names as ParameterDeclarations in callback/overload signatures, causing a panic.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3923](https://github.com/microsoft/TypeScript-go/pull/3923) (Open, **jakebailey**, **Copilot**)

**Fix source\-map emit panic for unclosed blocks**

*Prevent panics in source-map emission by handling positions beyond EOF when processing unclosed code blocks*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3924](https://github.com/microsoft/TypeScript-go/pull/3924) (Closed, **jakebailey**, **Copilot**)

**Fix panic in getRestTypeAtPosition for contextually typed function with optional and rest params**

*getRestTypeAtPosition panics with negative slice length for contextually typed functions with optional and rest parameters.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3925](https://github.com/microsoft/TypeScript-go/pull/3925) (Closed, **jakebailey**, **Copilot**)

**Fix panic when @this JSDoc tag is combined with a literal this parameter**

*tsgo reparser panics on JSDoc @this combined with a literal this parameter because it fails to recognize the this identifier*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3926](https://github.com/microsoft/TypeScript-go/pull/3926) (Open, **jakebailey**, **Copilot**)

**Fix panic on anonymous class declaration with decorator targeting ES2022**

*Prevent panic on anonymous class decorators targeting ES2022 by naming classes, optimizing traversal, adding tests, and enabling experimental decorators.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3926#issuecomment-4468394332) **jakebailey** said "@copilot apply changes based on the comments in this thread"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3926#issuecomment-4468420316) **Copilot** applied both requested changes: short-circuited ChildIsDecorated behind name == nil and replaced hardcoded false with tx.compilerOptions.ExperimentalDecorators.IsTrue()

### [PR microsoft/TypeScript-go#3927](https://github.com/microsoft/TypeScript-go/pull/3927) (Closed, **jakebailey**, **Copilot**)

**Fix panic for rest properties in catch binding when targeting ES2017**

*Replaced bitwise check with equality for KindSyntaxList in catch clause rest properties to fix transformer panic.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3928](https://github.com/microsoft/TypeScript-go/pull/3928) (Closed, **jakebailey**, **Copilot**)

**Fix panic in printer when type\-only export is body of an if statement**

*Printer panics when a type-only export is used as an if statement body, now fixed by emitting an empty statement.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3929](https://github.com/microsoft/TypeScript-go/pull/3929) (Closed, **jakebailey**, **Copilot**)

**Fix integer overflow in getCrossProductUnionSize causing hang on large template literal types**

*Add overflow checks to getCrossProductUnionSize to avoid signed integer wraparound and hanging on large template literal unions*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3930](https://github.com/microsoft/TypeScript-go/pull/3930) (Open, **jakebailey**, **Copilot**)

**Fix Uppercase/Lowercase intrinsic types to apply Unicode special case mappings**

*Update intrinsic Uppercase/Lowercase types to use full Unicode special case mappings via golang.org/x/text to match JavaScript*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3931](https://github.com/microsoft/TypeScript-go/pull/3931) (Open, **jakebailey**, **Copilot**)

**Fix \-NaN emission for enum members in declaration output**

*Enum declaration output now includes NaN and Infinity checks to avoid emitting -NaN or invalid infinite literals.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3932](https://github.com/microsoft/TypeScript-go/pull/3932) (Open, **jakebailey**, **Copilot**)

**Fix NaN\-valued enum members creating distinct literal types**

*Add specialized handling to ensure NaN-valued enum members share the same literal type within an enum but remain distinct across different enums.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3933](https://github.com/microsoft/TypeScript-go/pull/3933) (Open, **jakebailey**, **Copilot**)

**Fix declaration emit dropping readonly from \`as const\` object literal properties**

*Declaration emit omits readonly on as const object literal methods and properties due to method-level const context detection bug*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3934](https://github.com/microsoft/TypeScript-go/pull/3934) (Closed, **jakebailey**, **Copilot**)

**Fix typeof switch narrowing broken by \`case ""\` clauses**

*Empty string case clauses in typeof switch statements are misinterpreted as non-literals, aborting type narrowing entirely.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3935](https://github.com/microsoft/TypeScript-go/pull/3935) (Open)

**Narrow keyword completions for concise arrow expression bodies**

*Port keyword completion filtering to Go so concise arrow function bodies only suggest expression keywords.*

 * created by **DhineshPonnarasan**

### [Issue microsoft/TypeScript-go#3936](https://github.com/microsoft/TypeScript-go/issues/3936) (Closed, **jakebailey**, **Copilot**)

**tsgo wrongly parses literal object after \`await\`**

*tsgo incorrectly parses object literals after await, resulting in erroneous syntax errors compared to TypeScript 6.0.*

 * created by **Withered-Flower-0422**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3936#issuecomment-4469628013) **Withered-Flower-0422** reported tsgo threw an error when awaiting an empty array that did not occur in TypeScript 6.0
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3937](https://github.com/microsoft/TypeScript-go/pull/3937) (Closed, **jakebailey**, **Copilot**)

**Fix reparseTopLevelAwait diagnostic slicing bug**

*Adjusts the diagnostic range search in reparseTopLevelAwait to prevent initial-parse errors leaking into await reparsing.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3938](https://github.com/microsoft/TypeScript-go/issues/3938) (Open)

**Result of getTypeOfLocation for \`PropertyAccessExpression\` and \`ElementAccessExpression\` may be different between 6 and 7**

*Parenthesized and nested property accesses yield incorrect object types in tsgo v7’s getTypeAtLocation compared to TypeScript 6.*

 * created by **jet2jet**

