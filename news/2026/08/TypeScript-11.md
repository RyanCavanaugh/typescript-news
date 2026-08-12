# Report for 2026-08-11 (Tuesday, August 11th, 2026)

5 different users commented on 6 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#202](https://github.com/microsoft/TypeScript/issues/202) (Open, `Suggestion`, `In Discussion`)

**Support some non\-structural \(nominal\) type matching**

*Introduce nominal typing in TypeScript to distinguish structurally identical types and prevent unintended type mixing.*

 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/202#issuecomment-2868870489) **emilioplatzer** shared a workaround with example repository and Playground link and explained a typing-by-example approach using string literal types
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/202#issuecomment-4549960682) **bluepnume** described how they currently simulate opaque types with intersection types and custom tooling, illustrated how native opaque types and operator overloading would improve their workflow, linked to issue #42218, and expressed strong support
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/202#issuecomment-4549960682) **bluepnume** described how they currently simulate opaque types with intersection types and custom tooling, illustrated how native opaque types and operator overloading would improve their workflow, linked to issue #42218, and expressed strong support
 * [later](https://github.com/microsoft/TypeScript/issues/202#issuecomment-5264716824) **yun520-1** argued that nominal typing should not be added to TS core and that branded types with tooling improvements address nominal use cases without compromising structural typing
 * [later](https://github.com/microsoft/TypeScript/issues/202#issuecomment-5264716824) **yun520-1** argued that nominal typing should not be added to TS core and that branded types with tooling improvements address nominal use cases without compromising structural typing

### [Issue microsoft/TypeScript#59574](https://github.com/microsoft/TypeScript/issues/59574) (Open, `Suggestion`, `Awaiting More Feedback`)

**Symbol = LiveSymbol \| DeadSymbol**

*Distinguish live and dead symbols in TypeScript’s type system to catch invalid WeakMap key usage.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/59574#issuecomment-2278244386) **RyanCavanaugh** said "Useful information would be how someone might accidently make this kind of error (apart from the very first time, which would statically fail)"
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/59574#issuecomment-2278598871) **Josh-Cena** reminded that Symbol.iterator was eligible as WeakMap keys and explained that 'non-registered symbol' denotes symbols that can be weakly held
 * [today](https://github.com/microsoft/TypeScript/issues/59574#issuecomment-5259296478) **Daniel15** agreed with the proposal, suggested renaming the types to RegisteredSymbol and NonRegisteredSymbol as subtypes of symbol, and noted that symbols currently cannot be used as WeakMap keys and should be fixed

### [Issue microsoft/TypeScript#63737](https://github.com/microsoft/TypeScript/issues/63737) (Open, `Not a Defect`)

**Superclass type argument inferred as unknown when it's only used as a method parameter type constraint**

*TypeScript infers unknown when extracting a superclass’s generic type used only in a method parameter constraint instead of the expected type.*

 * created by **aweebit**
 * [today](https://github.com/microsoft/TypeScript/issues/63737#issuecomment-5254915607) **RyanCavanaugh** said "Constraints aren't inference sites; trying to do this caused way more problems than it solved. There's an issue on this somewhere but I can't find it at the moment."
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63737#issuecomment-5257232755) **jcalz** suggested issue #7234 and explained that B<boolean> extends B<infer T> works because TypeScript uses instantiation-based inference without a structural check

### [Issue microsoft/TypeScript#63747](https://github.com/microsoft/TypeScript/issues/63747) (Open, `Docs`, `Fix Available`)

**Update wiki "Using the Compiler API" for TypeScript v7**

*Update the Using the Compiler API wiki documentation to cover new types and patterns in TypeScript v7.*

 * (today) **RyanCavanaugh** added label `Docs`, and set milestone to `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/63747#issuecomment-5259820023) **RyanCavanaugh** said "I don't see how it's possible for someone external to have the necessary context on this. The API isn't even ready to be documented."

### [Issue microsoft/TypeScript#63748](https://github.com/microsoft/TypeScript/issues/63748) (Closed)

**wtf**

*The user expresses surprise that the project’s code is written in TypeScript itself.*

 * created by **asanaliopensource**
 * [later](https://github.com/microsoft/TypeScript/issues/63748#issuecomment-5268744988) **RyanCavanaugh** said "Well, not anymore 😛"
 * (later) **RyanCavanaugh** closed the issue

