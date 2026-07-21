# Report for 2026-07-18 (Saturday, July 18th, 2026)

6 different users commented on 6 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#12936](https://github.com/microsoft/TypeScript/issues/12936) (Open, `Suggestion`, `Awaiting More Feedback`)

**Exact Types**

*Introduce an Exact<T> type (e.g. |T|) to enforce exact object types and disallow extra properties.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5013665085) **dead-claudia** explained that requiring a runtime component would be a non-starter for the TS team and that exact types are meant for constrained use cases like socket messages and configurations rather than database objects
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5013665085) **dead-claudia** explained that requiring a runtime component would be a non-starter for the TS team and that exact types are meant for constrained use cases like socket messages and configurations rather than database objects
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5013665085) **dead-claudia** explained that requiring a runtime component would be a non-starter for the TS team and that exact types are meant for constrained use cases like socket messages and configurations rather than database objects
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5013665085) **dead-claudia** explained that requiring a runtime component would be a non-starter for the TS team and that exact types are meant for constrained use cases like socket messages and configurations rather than database objects
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5013665085) **dead-claudia** explained that requiring a runtime component would be a non-starter for the TS team and that exact types are meant for constrained use cases like socket messages and configurations rather than database objects
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5013665085) **dead-claudia** explained that requiring a runtime component would be a non-starter for the TS team and that exact types are meant for constrained use cases like socket messages and configurations rather than database objects
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5013665085) **dead-claudia** explained that requiring a runtime component would be a non-starter for the TS team and that exact types are meant for constrained use cases like socket messages and configurations rather than database objects
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5013665085) **dead-claudia** explained that requiring a runtime component would be a non-starter for the TS team and that exact types are meant for constrained use cases like socket messages and configurations rather than database objects
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5013665085) **dead-claudia** explained that requiring a runtime component would be a non-starter for the TS team and that exact types are meant for constrained use cases like socket messages and configurations rather than database objects
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5013665085) **dead-claudia** explained that requiring a runtime component would be a non-starter for the TS team and that exact types are meant for constrained use cases like socket messages and configurations rather than database objects
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5013665085) **dead-claudia** explained that requiring a runtime component would be a non-starter for the TS team and that exact types are meant for constrained use cases like socket messages and configurations rather than database objects
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-5013665085) **dead-claudia** explained that requiring a runtime component would be a non-starter for the TS team and that exact types are meant for constrained use cases like socket messages and configurations rather than database objects

### [Issue microsoft/TypeScript#63655](https://github.com/microsoft/TypeScript/issues/63655) (Open, `Duplicate`)

**No type mismatch for records with enum keys inside object literal with dynamic key**

*TypeScript fails to flag a type mismatch when assigning a string to a number-valued Record property via a dynamic key.*

 * created by **droooney**
 * [later](https://github.com/microsoft/TypeScript/issues/63655#issuecomment-5015375931) **MartinJohns** noted that the issue was a duplicate of #38663 and clarified that 'a' | 'b' is a union type, not an enum

### [Issue microsoft/TypeScript#63656](https://github.com/microsoft/TypeScript/issues/63656) (Open, `Needs More Info`)

**\`\-\-build \-\-dry\` reports a noEmit project reference as perpetually out of date \(expects emitted output that noEmit never produces\)**

*tsc --build --dry incorrectly marks noEmit project references as out of date due to missing tsbuildinfo.*

 * created by **schickling-assistant**

### [Issue microsoft/TypeScript#63657](https://github.com/microsoft/TypeScript/issues/63657) (Closed, `Duplicate`)

**Proposal: Add \\\`enum const\\\` modifier to auto\-generate union types for constant objects**

*Add a fully erasable `enum const` modifier in TypeScript to auto-generate union types for constant objects without runtime overhead.*

 * created by **yxdtg**
 * [later](https://github.com/microsoft/TypeScript/issues/63657#issuecomment-5016242989) **MartinJohns** said "Essentially a duplicate of #60790."
 * [later](https://github.com/microsoft/TypeScript/issues/63657#issuecomment-5016282338) **yxdtg** explained that the proposal differed from #60790 by being pure syntactic sugar without new type semantics

### [Issue microsoft/TypeScript#63658](https://github.com/microsoft/TypeScript/issues/63658) (Closed)

**TS Playground doesn't allow resolveJsonModule option**

*TypeScript Playground currently lacks support for the resolveJsonModule compiler option.*

 * created by **ysulyma**

### [Issue microsoft/TypeScript#63659](https://github.com/microsoft/TypeScript/issues/63659) (Open, `Working as Intended`)

**JSON imported with \`import type\` treated as value**

*Importing JSON with import type and resolveJsonModule incorrectly treats the import as a value, causing a type error.*

 * created by **ysulyma**

