# Report for 2026-03-21 (Saturday, March 21st, 2026)

9 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @hkleungai provided repro steps and error output in [microsoft/TypeScript-go#2911](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-4105364769)
    * @hkleungai offered to open a new issue in the TypeScript repository in [microsoft/TypeScript-go#2911](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-4105800838)
    * @hkleungai reported a possible unintentional breaking change in TS 7.0.0-dev regarding readonly array emission in [microsoft/TypeScript-go#3192](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4105762522)
    * @hkleungai provided additional details on inconsistent type emit in [microsoft/TypeScript-go#3192](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4106320452)

## Activity Summary

### [Issue microsoft/TypeScript-go#2911](https://github.com/microsoft/TypeScript-go/issues/2911) (Open, **jakebailey**, **Copilot**)

**TS4053 happens when public class method adopts imported type from library**

*Public methods in an exported class using an imported library type cause TS4053 errors with tsgo.*

 * **jakebailey** assigned to **jakebailey**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-3971719843) **hkleungai** edited the issue description with test results for various subcases and asked if they should open a new issue on the ts6 repo
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-3974546052) **hkleungai** mentioned that a similar issue had been reported for an exported variable with a different error code, and noted that TypeScript 6 still mishandles some cases
 * [today](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-4105364769) **hkleungai** thanked the team for PR 2459 and noted unresolved subcases in issue 2911 on TS6 and TS7, provided reproduction code and error outputs, and pinged @jakebailey
 * [today](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-4105529495) **jakebailey** said "I'm only assigned because I assigned copilot to it, which didn't really work."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-4105652784) **jakebailey** asked if the issue wasn't a regression because it persisted in both ts6 and ts7
 * [later](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-4105800838) **hkleungai** stated that the bug may be new or a rediscovery in TypeScript and offered to open an issue in the TypeScript repo if needed

### [PR microsoft/TypeScript-go#3167](https://github.com/microsoft/TypeScript-go/pull/3167) (Open)

**Fix: skip CommonJS export binding when module or exports is a local variable**

*Skips binding CommonJS exports when module or exports is locally defined to avoid shadowing ESM exports and spurious diagnostics.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3167#issuecomment-4093018437) **Muhammad-Bin-Ali** said "@microsoft-github-policy-service agree"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3167#issuecomment-4099806795) **jakebailey** questioned clearing the CJS indicator mid walk and suggested guarding the initial assignment instead
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3167#issuecomment-4100028136) **Muhammad-Bin-Ali** agreed with the suggestion to guard the assignment and said they would implement it
 * [today](https://github.com/microsoft/TypeScript-go/pull/3167#issuecomment-4105043960) **Muhammad-Bin-Ali** explained that there was no clean way to solve the problem earlier in the walk and modified the approach and added tests to address the issue

### [PR microsoft/TypeScript-go#3188](https://github.com/microsoft/TypeScript-go/pull/3188) (Closed)

**Fix identifier unicode escaping for parameter props**

*Properly parent cloned identifier nodes for parameter properties to fix unicode escaping*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3189](https://github.com/microsoft/TypeScript-go/pull/3189) (Closed)

**Remove \`AssignmentDeclarationMembers\` and \`GlobalExports\` from \`Symbol\`**

*Remove rarely used AssignmentDeclarationMembers and GlobalExports fields from Symbol to reduce memory footprint by relocating their tracking.*

 * created by **ahejlsberg**

### [PR microsoft/TypeScript-go#3190](https://github.com/microsoft/TypeScript-go/pull/3190) (Closed)

**Use iter\.Seq for GetSpellingSuggestion**

*Optimize GetSpellingSuggestion by using iterator-based sequence traversal to avoid sorting large symbol tables and improve performance.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3191](https://github.com/microsoft/TypeScript-go/pull/3191) (Closed)

**Reuse fileloader task data when atomic store fails**

*Reuse file loader task data via a global pool after atomic store failures to reduce memory allocations by about 80%.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3192](https://github.com/microsoft/TypeScript-go/issues/3192) (Closed, **weswigham**, **jakebailey**, **Copilot**)

**0320 vs 0321**

*The workglow build fails when using tsgo 7.0.0-dev.20260321.1 but succeeds with the previous day's 20260320.1 version.*

 * created by **sroussey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4104385157) **jakebailey** said "A CI log isn't a repro; can you give us something we can test in isolation without a big repo? Or bisect it?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4105762522) **hkleungai** noted that between 7.0.0-dev.20260320.1 and 7.0.0-dev.20260321.1 readonly arrays were processed differently leading to an extra readonly in the emitted types and asked if it was an unintentional breaking change
 * [later](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4106219802) **jakebailey** said "Yes, if it differs from TS6, it should be reported; I am assuming a regression from #2459 "
 * [later](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4106320452) **hkleungai** clarified that the issue should count as a report and noted inconsistent type emit
 * [later](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4106400401) **Andarist** said "Correct behavior related to https://github.com/microsoft/TypeScript/pull/55229 + https://github.com/microsoft/TypeScript/pull/55522"
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3193](https://github.com/microsoft/TypeScript-go/issues/3193) (Closed)

**isolatedDeclarations does not flag potential type predicate funcs**

*Functions resembling type predicates, such as isString returning boolean, are not flagged as errors when isolatedDeclarations and declaration are enabled.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3194](https://github.com/microsoft/TypeScript-go/pull/3194) (Closed)

**Report inferred type predicate inference fallback**

*Enable error reporting for inferred type predicates while reusing AST nodes from explicitly annotated predicates*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3195](https://github.com/microsoft/TypeScript-go/pull/3195) (Open)

**API encode/decode fixes**

*Fixed API encoder/decoder by adding missing node properties, assigning a HeritageClause token type, and extending isTypeNode to recognize type keywords.*

 * created by **virtulis**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4104786681) **virtulis** agreed with microsoft-github-policy-service

### [PR microsoft/TypeScript-go#3196](https://github.com/microsoft/TypeScript-go/pull/3196) (Open, **gabritto**)

**Fixes a crash when renaming import path of a JSON file**

*Renaming a JSON file’s import path causes the compiler to crash in TypeScript-Go and Strada.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3197](https://github.com/microsoft/TypeScript-go/pull/3197) (Closed)

**Fixed a go\-to\-implementations crash related to reexported type\-only namespace**

*Fixes go-to-implementations crash when navigating reexported type-only namespaces.*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#3198](https://github.com/microsoft/TypeScript-go/issues/3198) (Closed)

**ts 2322**

*Mocking window.open to return null triggers a 'null not assignable to ArrayBuffer' error in TypeScript 5.9.3 but not in tsgo.*

 * created by **yzhe554**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3198#issuecomment-4106310819) **jakebailey** requested testing with v6.0 instead of 5.9 and asked if strictNullChecks was enabled

### [PR microsoft/TypeScript-go#3199](https://github.com/microsoft/TypeScript-go/pull/3199) (Open, **jakebailey**, **Copilot**)

**Fix declaration emit readonly tuple regression from \`as const satisfies\`**

*Fix regression that wrongly adds readonly to tuple declarations when using as const satisfies by updating pseudotype builder logic.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

