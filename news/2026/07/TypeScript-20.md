# Report for 2026-07-20 (Monday, July 20th, 2026)

5 different users commented on 8 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#43368](https://github.com/microsoft/TypeScript/issues/43368) (Open, `Suggestion`, `Awaiting More Feedback`)

**Suggestion: Allow getters to have predicate return types**

*Enable TypeScript class getters to have user-defined type predicate return types for type guards.*

 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-4046270378) **alex-at-happening** said "That would be awesome to have it in TS"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-4410653140) **owenoak** said "+1 for this"
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-4600711749) **MaestroDD0S** said "+1 "
 * [later](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-5036153917) **merlinaudio** noted that methods have different semantics than getters, expressed a strong preference for getters, and gave a +1

### [Issue microsoft/TypeScript#63599](https://github.com/microsoft/TypeScript/issues/63599) (Closed)

**Typescript api**

*Provide missing TypeScript definitions for an ES2015-targeted API library.*

 * created by **alexandercarlis2-dotcom**
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63599#issuecomment-4838708808) **alexandercarlis2-dotcom** advised to use Markdown for comment formatting
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63655](https://github.com/microsoft/TypeScript/issues/63655) (Open, `Duplicate`)

**No type mismatch for records with enum keys inside object literal with dynamic key**

*TypeScript fails to flag a type mismatch when assigning a string to a number-valued Record property via a dynamic key.*

 * created by **droooney**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63655#issuecomment-5015375931) **MartinJohns** noted that the issue was a duplicate of #38663 and clarified that 'a' | 'b' is a union type, not an enum
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#63656](https://github.com/microsoft/TypeScript/issues/63656) (Open, `Needs More Info`)

**\`\-\-build \-\-dry\` reports a noEmit project reference as perpetually out of date \(expects emitted output that noEmit never produces\)**

*tsc --build --dry incorrectly marks noEmit project references as out of date due to missing tsbuildinfo.*

 * created by **schickling-assistant**
 * [today](https://github.com/microsoft/TypeScript/issues/63656#issuecomment-5025878704) **RyanCavanaugh** said "This is a confusing premise. Why are you writing a reference to a project with noEmit on in the first place? This effectively "does nothing" as far as I'm aware."
 * **RyanCavanaugh** added label `Needs More Info`

### [Issue microsoft/TypeScript#63657](https://github.com/microsoft/TypeScript/issues/63657) (Closed, `Duplicate`)

**Proposal: Add \\\`enum const\\\` modifier to auto\-generate union types for constant objects**

*Add a fully erasable `enum const` modifier in TypeScript to auto-generate union types for constant objects without runtime overhead.*

 * created by **yxdtg**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63657#issuecomment-5016242989) **MartinJohns** said "Essentially a duplicate of #60790."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63657#issuecomment-5016282338) **yxdtg** explained that the proposal differed from #60790 by being pure syntactic sugar without new type semantics
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63657#issuecomment-5025733622) **RyanCavanaugh** pointed out that the issue was a duplicate of #60790 and critiqued the asker's understanding
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63658](https://github.com/microsoft/TypeScript/issues/63658) (Closed)

**TS Playground doesn't allow resolveJsonModule option**

*TypeScript Playground currently lacks support for the resolveJsonModule compiler option.*

 * created by **ysulyma**
 * [today](https://github.com/microsoft/TypeScript/issues/63658#issuecomment-5025706946) **RyanCavanaugh** said "Playground isn't really intended for multi-file setups"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63659](https://github.com/microsoft/TypeScript/issues/63659) (Open, `Working as Intended`)

**JSON imported with \`import type\` treated as value**

*Importing JSON with import type and resolveJsonModule incorrectly treats the import as a value, causing a type error.*

 * created by **ysulyma**
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63659#issuecomment-5025682870) **RyanCavanaugh** said "A type-only import of a value is still a value; JSON files don't export types."

### [Issue microsoft/TypeScript#63663](https://github.com/microsoft/TypeScript/issues/63663) (Closed)

**Missing "used before declaration" error, with uninitialized variable reference inside callback**

*TypeScript does not report a "used before declaration" error when an uninitialized variable is referenced inside an async callback.*

 * created by **hkleungai**
 * [later](https://github.com/microsoft/TypeScript/issues/63663#issuecomment-5033863241) **guillaumebrunerie** described that TypeScript cannot infer that a callback is invoked before a function returns and illustrated this with a setInterval example
 * [later](https://github.com/microsoft/TypeScript/issues/63663#issuecomment-5036091358) **MartinJohns** said "Duplicate of #46136, which falls under #9998 / #11498."

