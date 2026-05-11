# Report for 2026-05-07 (Thursday, May 7th, 2026)

5 different users commented on 5 different issues.

## Recommended Actions

 * Response Recommended
    * @spaceemotion asked where to place NoInfer and if behavior differs between TS versions in [microsoft/TypeScript#63461](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4406385564)

## Activity Summary

### [Issue microsoft/TypeScript#63231](https://github.com/microsoft/TypeScript/issues/63231) (Open, `Needs More Info`)

**exports subpath with array types is not autocompleting**

*VS Code’s JavaScript/TypeScript language server does not autocomplete import paths for subpaths when exports.types is defined as an array*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63231#issuecomment-4041227902) **unional** said "Hi @RyanCavanaugh, sure will give that a try when I get a chance to. "
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63231#issuecomment-4204245115) **unional** confirmed the issue also existed in tsgo
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63231#issuecomment-4204282083) **unional** provided examples of wildcard exports not being autocompleted and described import map bloat mitigation using explicit file extensions
 * [today](https://github.com/microsoft/TypeScript/issues/63231#issuecomment-4403745996) **unional** clarified that while './*' works, './*.js' does not and noted that per HTML spec wildcard without extension is valid so this issue can be ignored

### [Issue microsoft/TypeScript#63457](https://github.com/microsoft/TypeScript/issues/63457) (Closed, `Duplicate`)

**\`Equals\<T, U\>\` used inside of generic type gets simplified to \`false\` immediately if only \`T\` or only \`U\` depends on a type variable**

*Equals<T, U> inside a generic type prematurely resolves to false when only one type parameter varies, even if types match.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4373016442) **carljohnsonnewhampshire-hue** thanked the maintainer for the FAQ link, suggested adding a TOC for the long page, acknowledged the documented implementation detail, and asked if the conditional type falls under Hyrum's Law and is valid to rely on
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4374434222) **mkantor** asked what the use case for the type was and suggested that mutual assignability might be the intended concept instead of type equality
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4378267616) **carljohnsonnewhampshire-hue** explained that he wanted strong type assertions in unit tests to ensure types are identical without unsoundness and decided to stick to the augmented Equals definition
 * [today](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4402575271) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63461](https://github.com/microsoft/TypeScript/issues/63461) (Closed, `Design Limitation`)

**\[6\.x\] Getting'unassingable to type' when returning value from method that needs to infer generic from parameters**

*TypeScript 6.x fails to infer the generic type for mapTo, marking the 'label' literal as unassignable.*

 * created by **spaceemotion**
 * [later](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4406369813) **mkantor** explained that inference from the return type was relevant and noted that string is assignable to Record<PropertyKey, unknown>, provided a link showing that changing RuntimePrimitive to string | Label resolves the issue, and suggested using NoInfer to disable return type inference
 * [later](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4406385564) **spaceemotion** questioned where to apply NoInfer after noting that return type precedence and assignment to a temporary variable eliminate the error, and checked the tsgo playground where the error appears in output but is not highlighted, wondering if the behavior differs between TS versions
 * [later](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4406402893) **mkantor** provided a playground link demonstrating where to place the `NoInfer` suggestion so that the return type of `mapTo` becomes `RuntimeList<NoInfer<TTo>>`
 * [later](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4407822649) **RyanCavanaugh** provided automated analysis on TS 6.0 inference change affecting mapTo and suggested using explicit type arguments or contextual typing to restore inference

