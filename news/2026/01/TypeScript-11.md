# Report for 2026-01-11 (Sunday, January 11th, 2026)

10 different users commented on 11 different issues.

## Recommended Actions

 * Response Recommended
    * @WorldMaker asked for help typing the context object and JSX factory function to preserve JSX ambient types when destructuring in [microsoft/TypeScript#45741](https://github.com/microsoft/TypeScript/issues/45741#issuecomment-3736618290)
    * @mizdra asked whether the behavior should be considered intended specification rather than a bug in [microsoft/TypeScript#62972](https://github.com/microsoft/TypeScript/issues/62972#issuecomment-3737245693)
    * @krryan asked why the rule was added to the compiler rather than as a linting check in [microsoft/TypeScript#62977](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3739186063)

## Activity Summary

### [Issue microsoft/TypeScript#17293](https://github.com/microsoft/TypeScript/issues/17293) (Open, `Bug`, `Domain: Declaration Emit`)

**Unexpected TS4094 with the build parameter \`declaration: true\`**

*TypeScript 2.4.1 incorrectly reports TS4094 on private properties of exported class expressions when declaration files are generated.*

 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/17293#issuecomment-1434089997) **sukima** asked what was wrong with a subclass extending a class with private properties
 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/17293#issuecomment-1439340789) **Marckon** stated that exporting the base class eliminated the error
 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/17293#issuecomment-1440593463) **rjamesnw** asked for a simple explanation of why subclassing a class with private members is problematic in TypeScript and provided a code example
 * [today](https://github.com/microsoft/TypeScript/issues/17293#issuecomment-3735663811) **valler** explained that extending a class with private properties is valid, demonstrated how the given factory pattern breaks instanceof, challenged the relevance of the linked issue, and proposed a constructor-based alternative

### [Issue microsoft/TypeScript#45741](https://github.com/microsoft/TypeScript/issues/45741) (Open, `Suggestion`, `In Discussion`, `Domain: JSX/TSX`)

**TS7026 when using JSX factory from a variable rather than import**

*TypeScript does not detect a JSX factory obtained via variable, causing TS7026 errors for missing IntrinsicElements.*

 * (4.3 years ago) **andrewbranch** added labels `Domain: JSX/TSX`, `In Discussion`, `Suggestion`
 * [today](https://github.com/microsoft/TypeScript/issues/45741#issuecomment-3736618290) **WorldMaker** described difficulty typing the context object and JSX factory function to preserve the JSX ambient type namespace when destructuring and referenced issue #14729 as a potential solution

### [Issue microsoft/TypeScript#52023](https://github.com/microsoft/TypeScript/issues/52023) (Open, `Suggestion`, `Awaiting More Feedback`)

**It is proposed to add support for multiple jsx factory functions\.**

*Add support for configuring multiple JSX factory functions in tsconfig.json by mapping file extensions to import sources.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/52023#issuecomment-1721152328) **Enteleform** said "+1 for this.  It would greatly improve the DX in multi-framework environments like Astro."
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/52023#issuecomment-2294946247) **Christoph-Koschel** said "Are there any updates to this feature?"
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/52023#issuecomment-2417546669) **TenviLi** said "Are there any updates to this feature?"
 * [today](https://github.com/microsoft/TypeScript/issues/52023#issuecomment-3736593639) **WorldMaker** suggested using the scoped JSX import form and proposed a tagged JSX syntax to mix frameworks in a single document

### [PR microsoft/TypeScript#62969](https://github.com/microsoft/TypeScript/pull/62969) (Closed, `For Uncommitted Bug`)

**Remove unnecessary type assertions**

*Remove unnecessary type assertions found during testing of the @typescript-eslint/no-unnecessary-type-assertion lint rule without affecting runtime or TS errors.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62969#issuecomment-3730722397) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (2 days ago) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62969#issuecomment-3736259974) **jakebailey** expressed doubt that the changes would be merged because the TypeScript codebase is due to be overwritten soon

### [Issue microsoft/TypeScript#62972](https://github.com/microsoft/TypeScript/issues/62972) (Closed, `Not a Defect`)

**\`errorType\` does not propagate with non\-distributive conditional types**

*Non-distributive conditional types in TypeScript fail to propagate errorType, unlike distributive conditional types.*

 * created by **mizdra**
 * [today](https://github.com/microsoft/TypeScript/issues/62972#issuecomment-3737245693) **mizdra** questioned whether the behavior should be considered intended specification rather than a bug, reasoning that [ErrorType] extends [unknown] evaluates to true because arrays are of type Array
 * [later](https://github.com/microsoft/TypeScript/issues/62972#issuecomment-3737630505) **Andarist** clarified that eagerly reducing those constructs would degrade the in-IDE experience and compared { prop: ErrorType } to ErrorType

### [Issue microsoft/TypeScript#62974](https://github.com/microsoft/TypeScript/issues/62974) (Open, `Bug`, `Help Wanted`, `Domain: Crashes`)

**Crash: TypeError: Cannot read properties of undefined \(reading 'flags'\) in isFreshLiteralType during recursive tuple expansion with unresolved identifiers**

*TypeScript compiler crashes with a TypeError reading 'flags' in isFreshLiteralType during recursive tuple expansion with unresolved identifiers*

 * created by **na7ure-a**
 * [later](https://github.com/microsoft/TypeScript/issues/62974#issuecomment-3738033715) **Andarist** reproduced the issue with a TypeScript variadic tuple code example

### [Issue microsoft/TypeScript#62975](https://github.com/microsoft/TypeScript/issues/62975) (Closed, `Working as Intended`)

**SkipLibCheck isn't working on erasableSyntaxCheck**

*SkipLibCheck fails to suppress errors in external index.d.ts files defining enums and namespaces under erasableSyntaxCheck*

 * created by **wparad**

### [Issue microsoft/TypeScript#62976](https://github.com/microsoft/TypeScript/issues/62976) (Closed, `Duplicate`)

**Nested Branded type does not error**

*TypeScript fails to enforce branded type distinctions in nested Records, allowing incompatible nested branded types to be assigned without error.*

 * created by **nitzcard**
 * [later](https://github.com/microsoft/TypeScript/issues/62976#issuecomment-3739117679) **jcalz** said "Duplicate of or related to #43852 "

### [Issue microsoft/TypeScript#62977](https://github.com/microsoft/TypeScript/issues/62977) (Closed, `Suggestion`, `Out of Scope`)

**\`disallowClassExpressions\`**

*Add a TypeScript compiler option to disallow class expressions for stricter type checking and error prevention.*

 * created by **valler**
 * [later](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3739186063) **krryan** said "This feels like a linting thing, not a compiler thing. What’s the rationale for putting it in the compiler?"
 * [later](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3739224279) **valler** argued that the rule belonged in tsc rather than a linter to avoid duplication and because compiler options align with compiler issues
 * [later](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3739277604) **MartinJohns** explained that the options existed in tsc due to legacy reasons before linter support was adequate
 * [later](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3739287291) **valler** clarified that the discussion pertained to language types rather than style and distinguished between a class and a class expression

