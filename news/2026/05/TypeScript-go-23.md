# Report for 2026-05-23 (Saturday, May 23rd, 2026)

6 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @kuishou68 asked for another review in [microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4527804370)

## Activity Summary

### [PR microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618) (Open)

**fix: prevent wildcard pattern from overriding exact match in FindBestPatternMatch**

*Assign math.MaxInt for exact matches in FindBestPatternMatch to ensure wildcard patterns cannot override exact matches.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4331007584) **DanielRosenwasser** said "As far as I remember, this code path isn't supposed to be hit for an exact match. Did you actually run into a problem with a specific project?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4411656223) **kuishou68** identified that the Go port compared StarIndex instead of prefixLength, causing wildcard matches to overwrite exact matches, and offered to add a side-by-side test to verify the fix
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4492416380) **DanielRosenwasser** asked why the user was tracing tsconfig.json resolution for paths and reiterated that the pattern list wasn't supposed to be passed
 * [today](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4527660962) **kuishou68** added a new test file internal/core/pattern_test.go covering exact versus wildcard orderings, longer versus shorter prefix wildcard precedence, no-match behavior, and single/multiple wildcard match scenarios with self-documenting assertions
 * [later](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4527804370) **kuishou68** said "I have added the test cases as requested. Could you please take another look?"

### [Issue microsoft/TypeScript-go#4037](https://github.com/microsoft/TypeScript-go/issues/4037) (Open, `bug`, **ahejlsberg**)

**TS2304 when a generic \(@template\) function JSDoc contains @overload**

*Generic functions documented with @template and @overload produce 'Cannot find name T' TS2304 errors in tsgo.*

 * created by **antichris**

### [Issue microsoft/TypeScript-go#4038](https://github.com/microsoft/TypeScript-go/issues/4038) (Open, `bug`, **ahejlsberg**)

**TS2315 when using \`@template\` more than once in a file**

*tsgo misreports TS2315 'export=' is not generic when a file contains more than one JSDoc @template declaration.*

 * created by **avivkeller**

### [Issue microsoft/TypeScript-go#4039](https://github.com/microsoft/TypeScript-go/issues/4039) (Open)

**Behavior difference: Inline comment on arrow function parameters is emitted on tsc but not on tsgo**

*tsgo removes inline comments on arrow function parameters that tsc retains, resulting in lost parameter comments*

 * created by **hkleungai**

### [Issue microsoft/TypeScript-go#4040](https://github.com/microsoft/TypeScript-go/issues/4040) (Open)

**Behavior difference: Implicitly declared class member appear after constructor in tsc emit, but show up before constructor in tsgo**

*Implicitly declared class members appear before the constructor in tsgo output but after it in tsc output.*

 * created by **hkleungai**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4040#issuecomment-4527951322) **jakebailey** said "This is entirely benign and a side effect of https://github.com/microsoft/typescript-go/pull/3541 (see comments there)"

### [Issue microsoft/TypeScript-go#4041](https://github.com/microsoft/TypeScript-go/issues/4041) (Open)

**Behavior difference: getTypeAtLocation returns method type for private method call**

*tsgo’s getTypeAtLocation incorrectly returns the private method’s function type instead of the call expression’s return type.*

 * created by **lucasavila00**

