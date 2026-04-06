# Report for 2026-04-01 (Wednesday, April 1st, 2026)

9 different users commented on 12 different issues.

## Recommended Actions

 * Response Recommended
    * @nmain asked what type the argument to JSON.stringify would have in [microsoft/TypeScript#63333](https://github.com/microsoft/TypeScript/issues/63333#issuecomment-4176413347)
    * @GuichiZhao provided root cause analysis and a suggested fix in [microsoft/TypeScript#63339](https://github.com/microsoft/TypeScript/issues/63339#issuecomment-4176716230)

## Activity Summary

### [Issue microsoft/TypeScript#42219](https://github.com/microsoft/TypeScript/issues/42219) (Open, `Suggestion`, `Awaiting More Feedback`)

**\[Feature\] Import non\-js content as const string**

*Enable importing non-JS file content as const string with compile-time TypeScript types via import.meta.content.*

 * [4.8 years ago](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-849032239) **mariusGundersen** said "I think with #42539 and the support for go-to-definition for text files then this feature would be a nice next step. "
 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-1400486580) **nsaunders** supported the idea and described a CSS workaround using a `*.css.ts` module with build tool extraction, syntax highlighting and Prettier limitations, and linked a demo project
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-3732822567) **valler** said "This should be compatible with type stripping, so it should be a JS feature really. The request is not so much about typing, but to reduce the need for custom loaders and/or intermediary build steps."
 * [later](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-4177548196) **linusg** mentioned that importing modules as plain text was being standardized in TC39 via import attributes and linked to the stage 3 proposal

### [Issue microsoft/TypeScript#63313](https://github.com/microsoft/TypeScript/issues/63313) (Closed, `Not a Defect`)

**Type of return value of \`yield\` cannot be inferred from explicitly declared \`TNext\`**

*Generator yield return type isn't inferred from the declared TNext, causing 'i' to be any instead of number.*

 * created by **zimtsui**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63313#issuecomment-4154411899) **RyanCavanaugh** explained that the situation was a true circularity and not a bug
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63313#issuecomment-4174058227) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63315](https://github.com/microsoft/TypeScript/issues/63315) (Closed, `Duplicate`)

**Error type constructor**

*Provide a type error constructor in TypeScript to allow explicit type-level errors instead of fallback to never.*

 * created by **masaeedu**
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63315#issuecomment-4148730562) **MartinJohns** said "Duplicate of #23689."
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63315#issuecomment-4174058109) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63330](https://github.com/microsoft/TypeScript/issues/63330) (Open, `Docs`, **DanielRosenwasser**)

**\[V6\] \`module\` defaults is not \`esnext\`**

*TypeScript 6.0 incorrectly defaults the module option to ES2015 instead of ESNext, causing import attributes errors.*

 * [today](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4169933585) **mkantor** explained that module defaulted to es2022 due to ScriptTarget.LatestStandard being es2025 and confirmed the same error with --module es2022
 * [today](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4169953503) **mkantor** noticed that the documentation for the default value of `target` was incorrect and that `ES3` was still mentioned as allowed though no longer supported
 * [today](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4169983541) **mkantor** questioned the repeated phrasing in the announcement post and asked if it was a typo
 * (today) **RyanCavanaugh** added label `Docs`, and assigned to **DanielRosenwasser**

### [Issue microsoft/TypeScript#63331](https://github.com/microsoft/TypeScript/issues/63331) (Closed)

**Admin Dashboard Implementation Progress Update**

*The admin dashboard tRPC backend is now 75% complete with all procedures implemented and ready for frontend integration.*

 * created by **rrader26**
 * [today](https://github.com/microsoft/TypeScript/issues/63331#issuecomment-4168993162) **MartinJohns** said "You seem to be lost. Which repository were you looking for?"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63332](https://github.com/microsoft/TypeScript/issues/63332) (Closed, `Duplicate`)

**instanceof narrowing should respect type parameter bounds for covariant types**

*TypeScript’s instanceof narrowing of generic covariant classes defaults type parameters to any instead of their bounded unions*

 * created by **ethanresnick**

### [Issue microsoft/TypeScript#63333](https://github.com/microsoft/TypeScript/issues/63333) (Closed, `Duplicate`)

**JSON\.stringify should disallow BigInt value**

*Restrict JSON.stringify’s parameter type to disallow BigInt values and prevent runtime errors.*

 * created by **wyattscarpenter**
 * [later](https://github.com/microsoft/TypeScript/issues/63333#issuecomment-4176413347) **nmain** inquired what type the argument to JSON.stringify would have and referenced issues #1897 and #4196

### [Issue microsoft/TypeScript#63334](https://github.com/microsoft/TypeScript/issues/63334) (Open)

**Playground typing issue**

*Importing from @octokit/core/types in the TypeScript Playground results in any types and stale diagnostic errors.*

 * created by **BrandonStudio**

### [PR microsoft/TypeScript#63335](https://github.com/microsoft/TypeScript/pull/63335) (Closed)

**Restore README\.md content**

*Add back previously removed content to README.md to fully restore project documentation*

 * created by **saiganesh47**
 * (today) **saiganesh47** closed the issue
 * (today) **saiganesh47** reopened the issue
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63339](https://github.com/microsoft/TypeScript/issues/63339) (Closed)

**"Find All References" does not show all sources when the same property is contributed by multiple \`declare module\` augmentations**

*Find All References only lists the first declare module augmentation for a merged interface property, omitting additional declarations.*

 * created by **GuichiZhao**
 * [later](https://github.com/microsoft/TypeScript/issues/63339#issuecomment-4176716230) **GuichiZhao** traced through the TypeScript source, identified that definitionToReferencedSymbolDefinitionInfo used firstOrUndefined to drop merged declarations, and suggested iterating over symbol.declarations to include all declaration sites

### [Issue microsoft/TypeScript#63340](https://github.com/microsoft/TypeScript/issues/63340) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Redundant leading apostrophe in the ts1344 diagnostic**

*TypeScript diagnostic ts1344 incorrectly includes a redundant leading apostrophe in its error message.*

 * created by **JLHwung**

