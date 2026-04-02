# Report for 2025-11-29 (Saturday, November 29th, 2025)

3 different users commented on 4 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#1616](https://github.com/microsoft/TypeScript-go/issues/1616) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**The last overload gave the following error\. Type 'unknown' is not assignable to type 'Foo'**

*After updating the TypeScript native-preview extension, DialogConfig calls fail with unknown not assignable to the expected modal confirmation generic type.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3573412591) **urielzen** reported that the issue persisted in version 0.20251124.1 despite merging #1603
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3584828612) **urielzen** said "I think this could be closed now! I just updated to version 0.20251127.1 and the error is no longer there. Thank u"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3585660594) **jakebailey** said "Do you know what version between those fixed it? Not sure we changed something on this front"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3592010666) **urielzen** acknowledged that they updated the extensions but didn't realize it was disabled and apologized for the confusion
 * [today](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3592032586) **jakebailey** said "So, it's fixed? 😄"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3592034829) **urielzen** said "not yet, sorry"

### [PR microsoft/TypeScript-go#2168](https://github.com/microsoft/TypeScript-go/pull/2168) (Closed)

**Revise type\-only alias logic to not depend on full type checks**

*Revise type-only import/export alias checking so files can be type-checked independently without full program checks.*

 * created by **ahejlsberg**

