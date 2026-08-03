# Report for 2026-08-01 (Saturday, August 1st, 2026)

6 different users commented on 9 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#55733](https://github.com/microsoft/TypeScript/issues/55733) (Open, `Bug`, `Help Wanted`, `Domain: Conditional Types`, `Cursed?`)

**Certain conditional types allow unsound assignments**

*Unbox<T> conditional types allow arbitrary assignments to a variable, causing unsound typing in generic contexts.*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/55733#issuecomment-1722311889) **GheorgheP** asked about how the any type is described and how it differed from unknown, and whether unknown should be treated as a bottom type
 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/55733#issuecomment-1723350794) **fatcerberus** explained that `any` disables typechecking whereas `unknown` represents any possible value without disabling typechecking and clarified that the bottom type is `never`.
 * **RyanCavanaugh** added label `Domain: Conditional Types`
 * [today](https://github.com/microsoft/TypeScript/issues/55733#issuecomment-5154221977) **aweebit** noted that the issue matched issue #62665 and suggested using type inference in Unbox's definition

### [Issue microsoft/TypeScript#63677](https://github.com/microsoft/TypeScript/issues/63677) (Open, `Bug`)

**type parameter variance in generic call signature is incorrectly bivariant**

*TypeScript incorrectly allows bivariant assignments for invariant generic call signatures, resulting in unsound type checking.*

 * (5 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63677#issuecomment-5133861386) **ayishaatwork** offered to work on the issue, reproduce the behavior, trace the compiler's assignability handling for generic function signatures, identify the unsound variance check, and share findings before opening a PR
 * [today](https://github.com/microsoft/TypeScript/issues/63677#issuecomment-5152761234) **ahmedajiz629** noted that intersecting a generic type T with D is equivalent to using a constraint <T extends D> and suggested D be contravariant

### [Issue microsoft/TypeScript#63697](https://github.com/microsoft/TypeScript/issues/63697) (Closed, `Design Limitation`)

**Return type inference limitation**

*TypeScript fails to infer the context property b in a generic callback passed to route.*

 * created by **aquapi**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63697#issuecomment-5135643442) **RyanCavanaugh** explained that inference couldn't alternate between an outer call's contextual type and an inner call's context-sensitive expression, since resolving both would require a unification-based algorithm that is unlikely for performance and practical reasons
 * **RyanCavanaugh** added label `Design Limitation`
 * [today](https://github.com/microsoft/TypeScript/issues/63697#issuecomment-5154464359) **typescript-automation[bot]** said "This issue has been marked as "Design Limitation" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#63705](https://github.com/microsoft/TypeScript/issues/63705) (Open, `Needs Investigation`, **weswigham**)

**TypeScript 7 declaration emit reuses an unrelated JSDoc import and generates an invalid type reference**

*TypeScript 7's declaration emit incorrectly reuses a private JSDoc import alias, producing invalid type references in declarations.*

 * created by **platypii**
 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/issues/63705#issuecomment-5153126629) **platypii** provided context as maintainer of hyparquet and hyparquet-writer and described a type error that surfaced after regenerating types with TypeScript 7 due to a dependency on SchemaElement

### [Issue microsoft/TypeScript#63708](https://github.com/microsoft/TypeScript/issues/63708) (Open)

**It is possible to violate generic constraints when distributing union types**

*Distributive union types in TypeScript can bypass generic constraints, allowing invalid B extends A combinations without error.*

 * created by **aweebit**

### [Issue microsoft/TypeScript#63709](https://github.com/microsoft/TypeScript/issues/63709) (Open)

**Property lookups on arguments to type parameters constrained by string index signatures can violate other constraints because undefined is included for optional properties**

*Property lookups on generics constrained by string index signatures include undefined for optional properties, allowing type constraint violations to go undetected.*

 * created by **aweebit**

### [Issue microsoft/TypeScript#63710](https://github.com/microsoft/TypeScript/issues/63710) (Open)

**\`ReadonlyMap\` lacks documentation for \`forEach\`, \`get\`, \`has\` and \`size\`**

*Document ReadonlyMap’s forEach, get, has, and size members in lib.es2015.collection.d.ts to match Map<K,V>.*

 * created by **KimMaru10**

### [PR microsoft/TypeScript#63711](https://github.com/microsoft/TypeScript/pull/63711) (Open, `For Uncommitted Bug`)

**docs: add JSDoc comments to ReadonlyMap interface**

*Add JSDoc comments for ReadonlyMap methods forEach, get, has, and size in lib.es2015.collection.d.ts for consistency with Map*

 * created by **KimMaru10**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63712](https://github.com/microsoft/TypeScript/issues/63712) (Open)

**Exported namespace class suppresses TS1308 for await in computed member names**

*Exporting a namespace class incorrectly disables the TS1308 error for await in computed member names.*

 * created by **mohsen1**

