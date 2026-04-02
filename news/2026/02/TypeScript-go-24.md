# Report for 2026-02-24 (Tuesday, February 24th, 2026)

11 different users commented on 25 different issues.

## Recommended Actions

 * Response Recommended
    * @johnnycheng0210 asked whether the issue was related to the language server state on config file refresh in [microsoft/TypeScript-go#2020](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3955294783)
    * @husayt reported that ignoreDeprecations: "6.0" didn't help and asked for a solution in [microsoft/TypeScript-go#2873](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3955967356)
    * @yanyunwu provided requested information in [microsoft/TypeScript-go#2901](https://github.com/microsoft/TypeScript-go/issues/2901#issuecomment-3957251118)

## Activity Summary

### [Issue microsoft/TypeScript-go#1578](https://github.com/microsoft/TypeScript-go/issues/1578) (Closed, `Domain: Porting Meta`)

**Fix GetLineAndCharacterOfPosition and audit all users**

*Refactor GetLineAndCharacterOfPosition and related methods to clearly differentiate rune and byte offsets and consistently handle newline variations for all callers.*

 * created by **jakebailey**
 * **jakebailey** added label `Domain: Porting Meta`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2020](https://github.com/microsoft/TypeScript-go/pull/2020) (Open)

**Support for custom configurations**

*Enable passing custom tsconfig file names to the tsgo LSP to support solution-style repository configurations.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3924761855) **johnnycheng0210** reported similar behavior with findAllReferences when switching project configurations, observed that results didn't update after reverting to single project config, and asked why the old configuration persisted
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3924764987) **johnnycheng0210** wondered if requiring a window reload between custom config file name changes would be preferred as a simpler approach
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3928562337) **jakebailey** said "I'm definitely confused, because when I write a test for this, the test seemingly does the right thing."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3955294783) **johnnycheng0210** asked whether the issue was related to the language server state on config file refresh rather than the new config file name update

### [Issue microsoft/TypeScript-go#2632](https://github.com/microsoft/TypeScript-go/issues/2632) (Open)

**\`@param\` JSDoc requires parameter names, did not in 6\.0 and prior**

*Omitting parameter names in JSDoc @param tags prevents TypeScript from reporting argument type mismatches under noImplicitAny.*

 * created by **DanielRosenwasser**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2632#issuecomment-3836132764) **a-tarasyuk** said "@DanielRosenwasser If I remember correctly, earlier versions also required a parameter name. Is this intentional, or is it a new feature to make it optional?"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2632#issuecomment-3836891087) **DanielRosenwasser** said "I probably complained to @sandersn about it then and I'll complain about it in 7.0 too. 😄"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2632#issuecomment-3959962309) **a-tarasyuk** said "@DanielRosenwasser I’ve opened a PR to address this — could you confirm whether the current behavior is intentional?"

### [PR microsoft/TypeScript-go#2717](https://github.com/microsoft/TypeScript-go/pull/2717) (Closed)

**parse formatting options in initialization, and pull \`editor\` scope during \`Configuration\` **

*Allow parsing of editor-formatting preferences from initializationOptions and configuration changes in VS/VSCode and fix indentSize handling for organize imports/formatting*

 * created by **iisaduan**
 * (today) **iisaduan** closed the issue

### [PR microsoft/TypeScript-go#2863](https://github.com/microsoft/TypeScript-go/pull/2863) (Closed, **jakebailey**, **Copilot**)

**Unskip 14 passing formatting fourslash tests**

*Re-enable 14 skipped fourslash formatting tests after fixing indentation computation, list guard, and JSDoc reparsing bugs.*

 * created by **Copilot**
 * (4 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2873](https://github.com/microsoft/TypeScript-go/issues/2873) (Closed)

**dexie validation 7\.0\.0\-dev\.20260219\.1 works, 7\.0\.0\-dev\.20260222\.1 fails**

*Updating to dexie 7.0.0-dev.20260222.1 triggers a TS1540 'namespace' declaration error in dexie.d.ts that was not present in 7.0.0-dev.20260219.1*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3942921426) **siphosenkosindhlovu** acknowledged missing the fix and thanked the contributor
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3942927604) **jakebailey** acknowledged that the readme claim about parsing/scanning matching TS 6.0 wasn't strictly true when being pedantic
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3943016313) **AntonOfTheWoods** mentioned that pedantry is typically beneficial in programming contexts
 * [today](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3955967356) **husayt** reported encountering the same issue with Dexie and noted that ignoreDeprecations: "6.0" didn't help
 * [today](https://github.com/microsoft/TypeScript-go/issues/2873#issuecomment-3956013315) **jakebailey** said "Yes, because this codebase is TS 7.0, where we've entirely removed things that were deprecated in TS 6.0."

### [PR microsoft/TypeScript-go#2879](https://github.com/microsoft/TypeScript-go/pull/2879) (Closed)

**Hopefully settle line endings / position mapping**

*Renamed various position-mapping functions, introduced a UTF16Offset type, and corrected line-ending and source-map offset calculations.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2886](https://github.com/microsoft/TypeScript-go/issues/2886) (Closed, `Domain: Editor`)

**Incorrect formatting after override modifier**

*Formatting fails to remove extra spaces following the override modifier in TypeScript class methods.*

 * created by **itrapashko**
 * **itrapashko** added label `Domain: Editor`
 * (today) **iisaduan** closed the issue

### [PR microsoft/TypeScript-go#2887](https://github.com/microsoft/TypeScript-go/pull/2887) (Closed)

**Fix formatting after override keyword**

*Adjust code formatting rules to correctly format code following the override keyword.*

 * created by **itrapashko**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2887#issuecomment-3952283432) **itrapashko** said "I'm not sure where to put the test. I ended up putting it to the internal/fourslash/tests folder."
 * (today) **iisaduan** closed the issue

### [Issue microsoft/TypeScript-go#2889](https://github.com/microsoft/TypeScript-go/issues/2889) (Closed)

**Tsgo considers wrong API usage as correct \- difference in typechecking**

*tsgo wrongly treats improper use of orderBy in attachments as valid and infers incorrect types, unlike TypeScript’s stricter checks*

 * created by **jansedlon**
 * **jakebailey** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#2890](https://github.com/microsoft/TypeScript-go/issues/2890) (Closed, `Crash`)

**panic handling request textDocument/inlayHint**

*The TypeScript-Go LSP server panics on textDocument/inlayHint requests because ComputedPropertyName AST nodes are unhandled.*

 * created by **Zzzen**
 * **Zzzen** added label `Crash`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2891](https://github.com/microsoft/TypeScript-go/pull/2891) (Closed)

**fix\(ast\): handle computed property names in Node\.Text**

*Add support for computed property names in Node.Text AST generation*

 * created by **Zzzen**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2891#issuecomment-3952520923) **ahejlsberg** clarified that Node.Text was intended only as an accessor for nodes with a text property and recommended not calling it on nodes without that property
 * [today](https://github.com/microsoft/TypeScript-go/pull/2891#issuecomment-3953137591) **jakebailey** said "Yeah, don't let the JSDoc bit fool you, that is just a performance optimization we didn't need in JS due to deferred string building meaning it was rarely read."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2891#issuecomment-3953950072) **jakebailey** said "#2892"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2892](https://github.com/microsoft/TypeScript-go/pull/2892) (Closed)

**Fixed a crash on computed property name when computing inlay hints**

*Computing inlay hints now correctly handles computed property names without crashing.*

 * created by **Andarist**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2895](https://github.com/microsoft/TypeScript-go/issues/2895) (Closed)

**\[ServerErrors\]\[TypeScript\] linux\-x64\-7\.0\.0\-dev\.20260224\.1 vs **

*The linux-x64-7.0.0-dev.20260224.1 build on Azure pipelines reported server errors in 294 of the 300 popular TypeScript GitHub repositories analyzed.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953951448) **typescript-bot** reported a panic during textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953951536) **typescript-bot** reported a panic in textDocument/formatting due to integer divide by zero
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953951626) **typescript-bot** reported a panic during textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953951687) **typescript-bot** reported panic handling request textDocument/formatting due to negative repeat count and included the stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953951759) **typescript-bot** reported a panic during textDocument/formatting caused by integer divide by zero
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953951819) **typescript-bot** reported a panic in textDocument/formatting due to negative Repeat count and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953951890) **typescript-bot** reported a panic in textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953951963) **typescript-bot** reported a panic in textDocument/formatting due to strings: negative Repeat count and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952018) **typescript-bot** reported a panic in handling textDocument/formatting due to strings: negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952086) **typescript-bot** reported a panic handling textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952161) **typescript-bot** reported a panic handling a textDocument/formatting request due to integer divide by zero
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952248) **typescript-bot** reported a runtime panic during textDocument/formatting caused by an integer divide by zero
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952317) **typescript-bot** reported a panic in textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952381) **typescript-bot** reported a panic while handling a textDocument/formatting request due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952451) **typescript-bot** reported a panic in textDocument/formatting due to strings: negative Repeat count and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952524) **typescript-bot** reported a panic during handling a textDocument/formatting request due to strings: negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952591) **typescript-bot** reported a panic due to integer divide by zero during textDocument/formatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952658) **typescript-bot** reported a panic in textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952725) **typescript-bot** reported a panic handling request textDocument/formatting due to negative repeat count with stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952783) **typescript-bot** reported a panic during textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952850) **typescript-bot** reported a panic in textDocument/formatting due to a 'strings: negative Repeat count' error
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952929) **typescript-bot** reported a panic handling request textDocument/formatting due to a negative repeat count and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953952997) **typescript-bot** reported panic during textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953056) **typescript-bot** reported a panic handling textDocument/formatting due to negative repeat count and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953107) **typescript-bot** described a panic during textDocument/formatting caused by a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953181) **typescript-bot** reported a runtime panic caused by integer divide by zero in textDocument/formatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953236) **typescript-bot** reported a panic while handling textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953294) **typescript-bot** reported a panic in textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953355) **typescript-bot** reported panic handling textDocument/formatting request due to negative string repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953419) **typescript-bot** reported a panic during textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953481) **typescript-bot** reported a panic in textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953577) **typescript-bot** reported a panic when handling a textDocument/formatting request due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953668) **typescript-bot** reported a panic in textDocument/formatting due to negative repeat count and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953732) **typescript-bot** reported a panic handling textDocument/formatting due to strings: negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953826) **typescript-bot** reported a panic handling request textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953930) **typescript-bot** reported a panic handling textDocument/formatting request due to strings: negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953953995) **typescript-bot** reported a panic during textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954087) **typescript-bot** reported panic during handling of textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954153) **typescript-bot** reported a runtime panic with integer divide by zero during textDocument/formatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954220) **typescript-bot** reported a runtime panic on textDocument/formatting due to integer divide by zero
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954291) **typescript-bot** reported panic handling formatting request due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954365) **typescript-bot** reported a panic during handling of textDocument/implementation due to an invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954444) **typescript-bot** reported a panic error during textDocument/implementation handling due to a nil pointer dereference and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954511) **typescript-bot** reported a panic in request textDocument/formatting due to strings: negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954569) **typescript-bot** reported panic in textDocument/formatting due to negative repeat count along with a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954637) **typescript-bot** reported a panic during textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954708) **typescript-bot** reported a panic handling textDocument/formatting request due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954785) **typescript-bot** reported a panic handling request for textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954848) **typescript-bot** reported panic in textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954930) **typescript-bot** reported a panic in textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953954998) **typescript-bot** reported a panic handling request textDocument/formatting due to strings: negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955063) **typescript-bot** reported a panic during textDocument/formatting caused by a negative repeat count with stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955151) **typescript-bot** reported a panic handling a textDocument/formatting request due to a negative Repeat count and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955209) **typescript-bot** reported a panic during textDocument/formatting due to a 'strings: negative Repeat count'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955277) **typescript-bot** reported panic handling textDocument/formatting request due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955331) **typescript-bot** reported a panic handling request textDocument/formatting due to negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955386) **typescript-bot** reported a panic error during textDocument/rename request handling
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955462) **typescript-bot** reported panic handling textDocument/formatting request due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955519) **typescript-bot** reported a panic in textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955583) **typescript-bot** reported a panic handling a textDocument/formatting request due to strings: negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955644) **typescript-bot** reported a panic during handling of textDocument/formatting due to strings: negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955704) **typescript-bot** reported a panic handling textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955771) **typescript-bot** reported a panic handling request textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955820) **typescript-bot** reported a panic in textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955883) **typescript-bot** reported a panic in textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953955955) **typescript-bot** reported a panic handling request textDocument/formatting due to negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956026) **typescript-bot** reported a panic handling textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956091) **typescript-bot** reported a panic in textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956153) **typescript-bot** reported a panic during textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956234) **typescript-bot** reported a panic in textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956292) **typescript-bot** reported a panic handling textDocument/formatting request due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956356) **typescript-bot** reported a panic in textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956429) **typescript-bot** reported a panic during textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956504) **typescript-bot** reported a panic while handling a textDocument/formatting request due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956570) **typescript-bot** reported a panic handling request textDocument/formatting with strings: negative Repeat count and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956622) **typescript-bot** reported a panic handling request textDocument/formatting due to strings: negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956693) **typescript-bot** reported a panic handling textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956767) **typescript-bot** reported panic handling textDocument/formatting request due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956826) **typescript-bot** reported a panic in textDocument/formatting due to a negative Repeat count and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956886) **typescript-bot** reported a panic while handling textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953956946) **typescript-bot** reported panic handling request textDocument/formatting due to negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957014) **typescript-bot** reported a panic occurring during handling of textDocument/formatting request due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957089) **typescript-bot** reported a panic handling the textDocument/formatting request due to negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957148) **typescript-bot** reported a panic handling a textDocument/formatting request due to integer divide by zero
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957211) **typescript-bot** reported a panic handling request textDocument/formatting due to negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957267) **typescript-bot** reported a panic in textDocument/formatting due to strings: negative Repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957351) **typescript-bot** reported a panic in textDocument/formatting due to a negative string repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957427) **typescript-bot** reported panic handling request textDocument/formatting due to negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957495) **typescript-bot** reported a panic handling request textDocument/formatting due to strings: negative Repeat count and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957535) **typescript-bot** reported a panic handling textDocument/formatting due to a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957599) **typescript-bot** reported a panic during textDocument/formatting caused by a negative repeat count
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957659) **typescript-bot** reported a panic due to integer divide by zero during textDocument/formatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957725) **typescript-bot** reported a panic in textDocument/rangeFormatting due to bad line number
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957793) **typescript-bot** reported a panic handling textDocument/rangeFormatting due to a bad line number
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957866) **typescript-bot** reported a panic crash during textDocument/rangeFormatting due to a bad line number
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953957939) **typescript-bot** reported a panic handling textDocument/rangeFormatting due to a bad line number
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953958029) **typescript-bot** reported a panic during textDocument/rangeFormatting due to bad line number and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953958108) **typescript-bot** reported a panic in textDocument/rangeFormatting due to bad line number and provided stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953958176) **typescript-bot** reported a panic during textDocument/rangeFormatting due to a bad line number
 * [today](https://github.com/microsoft/TypeScript-go/issues/2895#issuecomment-3953958245) **typescript-bot** reported a panic when handling textDocument/rangeFormatting due to a bad line number, including a stacktrace
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2896](https://github.com/microsoft/TypeScript-go/pull/2896) (Closed)

**Handled tabsize of zero in getIndentationString**

*TabSize zero in getIndentationString causes division by zero and infinite spaces, resulting in a 'negative Repeat count' error.*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#2897](https://github.com/microsoft/TypeScript-go/pull/2897) (Closed, **jakebailey**, **Copilot**)

**Respect both \`js/ts\.experimental\.useTsgo\` and \`typescript\.experimental\.useTsgo\` settings**

*Update the extension to properly detect, watch, and update both js/ts.experimental.useTsgo and typescript.experimental.useTsgo settings.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2898](https://github.com/microsoft/TypeScript-go/pull/2898) (Closed)

**Update Go image version in devcontainer\.json**

*Update the Go image version in devcontainer.json to use a newer release.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2899](https://github.com/microsoft/TypeScript-go/pull/2899) (Closed)

**Improve asynchronous transfer performance**

*Optimize asynchronous transfers to reduce JS memory usage by 10–20% with minimal throughput change.*

 * created by **liuxingbaoyu**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2899#issuecomment-3955412992) **jakebailey** said "When was this feature introduced into Node?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2899#issuecomment-3955428336) **liuxingbaoyu** said "This was added from Node.js v5, but now the tests are failing, and I'm investigating."

### [PR microsoft/TypeScript-go#2900](https://github.com/microsoft/TypeScript-go/pull/2900) (Closed)

**Update devcontainer image to use dev\-1\.26\-bookworm**

*Request to update the development container image to use the dev-1.26-bookworm tag.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2901](https://github.com/microsoft/TypeScript-go/issues/2901) (Closed)

**\`tsgo\` do not support \`exports\` perfect**

*tsgo only supports exact package export paths and fails to handle wildcard exports such as './path/*'.*

 * created by **yanyunwu**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2901#issuecomment-3956541329) **jakebailey** said "This isn't enough information. What module resolution mode are you using?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2901#issuecomment-3957251118) **yanyunwu** attached an image showing the module resolution mode
 * [today](https://github.com/microsoft/TypeScript-go/issues/2901#issuecomment-3957276562) **jakebailey** said "moduleResolution=node is deprecated. You should have gotten an error for that in 6.0 (the version goy say in your issue)."

### [Issue microsoft/TypeScript-go#2902](https://github.com/microsoft/TypeScript-go/issues/2902) (Closed, `duplicate`, **ahejlsberg**, **jakebailey**, **Copilot**)

**Unique symbol defined as attribute not narrowed**

*A unique symbol assigned as an object property is not properly narrowed within a union type in TypeScript 7.0.*

 * created by **jfdoming**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2903](https://github.com/microsoft/TypeScript-go/pull/2903) (Closed, **jakebailey**, **Copilot**)

**Fix unique symbol widening in expando property assignments**

*Unique symbols assigned as expando properties are incorrectly widened to symbol, breaking type narrowing via equality checks.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

