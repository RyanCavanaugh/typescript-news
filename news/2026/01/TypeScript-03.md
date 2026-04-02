# Report for 2026-01-03 (Saturday, January 3rd, 2026)

9 different users commented on 10 different issues.

## Recommended Actions

 * Response Recommended
    * @oppong07 asked if maintainers prefer submission to microsoft/typescript-go instead in [microsoft/TypeScript#37782](https://github.com/microsoft/TypeScript/issues/37782#issuecomment-3707833723)
    * @marqdouj suggested mentioning the workaround in the TypeScript documentation in [microsoft/TypeScript#62948](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3707923154)

## Activity Summary

### [Issue microsoft/TypeScript#37782](https://github.com/microsoft/TypeScript/issues/37782) (Open, `Suggestion`, `Help Wanted`, `Good First Issue`)

**'declare method' quick fix for adding a private method**

*Request a quick fix feature to declare missing private methods in classes, similar to the existing private property quick fix.*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/37782#issuecomment-2244876785) **NsdHSO** said "@DanielRosenwasser is it still open?"
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/37782#issuecomment-3233122916) **kamolovd** said "This is my first investment in outsourcing, can I start with this? @mjbvz "
 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/37782#issuecomment-3375208607) **tysoncung** suggested checking the error logs and asked for environment details to help investigate the issue
 * [today](https://github.com/microsoft/TypeScript/issues/37782#issuecomment-3707833723) **oppong07** announced plans to implement the "declare method" quick fix, add tests, open a PR, and asked whether maintainers prefer submission to microsoft/typescript-go

### [Issue microsoft/TypeScript#60954](https://github.com/microsoft/TypeScript/issues/60954) (Open, `Suggestion`, `Awaiting More Feedback`)

**Getting a setter\-only property is typed as the setter's parameter's type instead of undefined**

*TypeScript infers the type of accessing a setter-only property as the setter’s parameter type instead of undefined*

 * [50 weeks ago](https://github.com/microsoft/TypeScript/issues/60954#issuecomment-2588044972) **jcalz** linked to the TypeScript FAQ about the ECMAScript spec being descriptive rather than normative
 * [50 weeks ago](https://github.com/microsoft/TypeScript/issues/60954#issuecomment-2588088975) **Gouvernathor** said "Ok, fair point. But as per the examples above, I still think it's a useful feature."
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/60954#issuecomment-3358505626) **jogibear9988** described encountering an error in their codebase caused by a setter-only property recursively referencing itself
 * [today](https://github.com/microsoft/TypeScript/issues/60954#issuecomment-3707179711) **waelbettayeb** noted that implicitly making a get/set that isn't reflexive could be breaky and would require stronger motivation, and suggested that issue #62943 may provide stronger motivation
 * [later](https://github.com/microsoft/TypeScript/issues/60954#issuecomment-3708092004) **Gouvernathor** questioned how the rationale supported keeping setter-only properties implicit and suggested they should be explicit rather than typed as two-way properties

### [Issue microsoft/TypeScript#62933](https://github.com/microsoft/TypeScript/issues/62933) (Open, `Bug`, `Domain: check: Type Circularity`)

**Maximum call stack size exceeded in isTypeAssignableTo when using recursive template literal types in a generic context**

*Using recursive template literal types inside a generic context causes checker.isTypeAssignableTo to exceed the maximum call stack size.*

 * created by **mdm317**
 * [later](https://github.com/microsoft/TypeScript/issues/62933#issuecomment-3708138963) **Andarist** demonstrated that the same issue could be triggered when typechecking a recursive string literal type example

### [Issue microsoft/TypeScript#62937](https://github.com/microsoft/TypeScript/issues/62937) (Closed, `Not a Defect`)

**Crash: RangeError: Invalid string length in addSpans when evaluating deeply recursive Template Literal Types with \-\-strict enabled**

*TypeScript compiler crashes with a RangeError on deeply recursive template literal type evaluation when strict mode is enabled*

 * created by **na7ure-a**
 * [today](https://github.com/microsoft/TypeScript/issues/62937#issuecomment-3707209815) **Andarist** explained that it ended up creating a humongous string equivalent to 'k'.repeat(536000000) + 'k'.repeat(1000000)

### [PR microsoft/TypeScript#62947](https://github.com/microsoft/TypeScript/pull/62947) (Closed, `For Uncommitted Bug`)

**Update Apache License to version 2\.0, January 2026**

*Change the license header date of Apache License 2.0 from January 2004 to January 2026.*

 * created by **AkiUse306**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62947#issuecomment-3707443353) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/62947#issuecomment-3707498359) **jakebailey** said "Oh, you just changed it to the current month. No, that's not right"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62948](https://github.com/microsoft/TypeScript/issues/62948) (Open, `Needs Investigation`, **joj**)

**TypeScript MSBuild Target named GetTypeScriptOutputForPublishing should not include the removed Content files**

*The GetTypeScriptOutputForPublishing MSBuild target ignores Content Remove directives and re-includes generated .js and .d.ts files in the package.*

 * created by **marqdouj**
 * [later](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3707876032) **MartinJohns** advised using fewer search terms and stated the behavior worked correctly with a viable workaround
 * [later](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3707923154) **marqdouj** reported that after months of troubleshooting a Microsoft engineer helped and planned to submit a ticket to the TypeScript team, and suggested mentioning the solution in the TypeScript documentation

### [PR microsoft/TypeScript#62949](https://github.com/microsoft/TypeScript/pull/62949) (Open, `For Uncommitted Bug`)

** add fourslash test for declare missing method quickfix \(\#37782\)**

*Add a fourslash test to verify the quick fix that declares a missing private method in a class.*

 * created by **oppong07**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62949#issuecomment-3707875038) **oppong07** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#62950](https://github.com/microsoft/TypeScript/pull/62950) (Open, `For Backlog Bug`)

**Ignore computed name parents when looking up containing functions**

*Update lookup to skip computed name parent nodes when identifying a node’s containing function.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`

