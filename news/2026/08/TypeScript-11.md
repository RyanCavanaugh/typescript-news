# Report for 2026-08-11 (Tuesday, August 11th, 2026)

4 different users commented on 9 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#59574](https://github.com/microsoft/TypeScript/issues/59574) (Open, `Suggestion`, `Awaiting More Feedback`)

**Symbol = LiveSymbol \| DeadSymbol**

*Distinguish live and dead symbols in TypeScript’s type system to catch invalid WeakMap key usage.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/59574#issuecomment-2278244386) **RyanCavanaugh** said "Useful information would be how someone might accidently make this kind of error (apart from the very first time, which would statically fail)"
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/59574#issuecomment-2278598871) **Josh-Cena** reminded that Symbol.iterator was eligible as WeakMap keys and explained that 'non-registered symbol' denotes symbols that can be weakly held
 * [today](https://github.com/microsoft/TypeScript/issues/59574#issuecomment-5259296478) **Daniel15** agreed with the proposal, suggested renaming the types to RegisteredSymbol and NonRegisteredSymbol as subtypes of symbol, and noted that symbols currently cannot be used as WeakMap keys and should be fixed

### [Issue microsoft/TypeScript#63726](https://github.com/microsoft/TypeScript/issues/63726) (Closed, `Bug`, `Domain: JSDoc`, `Fix Available`, **sandersn**)

**Poorly formed output with JSDoc typedef**

*JSDoc typedef produces malformed TypeScript definitions embedding stray asterisks in the union type.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`
 * **RyanCavanaugh** assigned to **sandersn**
 * **RyanCavanaugh** added label `Domain: JSDoc`

### [Issue microsoft/TypeScript#63728](https://github.com/microsoft/TypeScript/issues/63728) (Open, `Bug`, `Help Wanted`, `Domain: tslib and Helper Functions`)

**\`importHelpers\` incorrectly requires \`tslib\` for native \`\#private\` class members at every dated \`target\` \(ES2022–ES2025\), even though no helper is ever emitted**

*TypeScript’s importHelpers option wrongly requires tslib for native private class fields when targeting ES2022–ES2025 despite no helper emission*

 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: tslib and Helper Functions`

### [Issue microsoft/TypeScript#63737](https://github.com/microsoft/TypeScript/issues/63737) (Closed, `Not a Defect`)

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

