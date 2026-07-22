# Report for 2026-07-21 (Tuesday, July 21st, 2026)

6 different users commented on 9 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#63657](https://github.com/microsoft/TypeScript/issues/63657) (Closed, `Duplicate`)

**Proposal: Add \\\`enum const\\\` modifier to auto\-generate union types for constant objects**

*Add a fully erasable `enum const` modifier in TypeScript to auto-generate union types for constant objects without runtime overhead.*

 * **RyanCavanaugh** added label `Duplicate`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63657#issuecomment-5025733622) **RyanCavanaugh** pointed out that the issue was a duplicate of #60790 and critiqued the asker's understanding
 * (yesterday) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63657#issuecomment-5040032735) **yxdtg** acknowledged the oversight and apologized

### [Issue microsoft/TypeScript#63663](https://github.com/microsoft/TypeScript/issues/63663) (Closed)

**Missing "used before declaration" error, with uninitialized variable reference inside callback**

*TypeScript does not report a "used before declaration" error when an uninitialized variable is referenced inside an async callback.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript/issues/63663#issuecomment-5033863241) **guillaumebrunerie** described that TypeScript cannot infer that a callback is invoked before a function returns and illustrated this with a setInterval example
 * [today](https://github.com/microsoft/TypeScript/issues/63663#issuecomment-5036091358) **MartinJohns** said "Duplicate of #46136, which falls under #9998 / #11498."
 * (today) **hkleungai** closed the issue

### [Issue microsoft/TypeScript#63664](https://github.com/microsoft/TypeScript/issues/63664) (Open)

**Incremental builder re\-emits entire transitive import closure on a whitespace\-only edit \(regression in 5\.5: exportedModulesMap removal \+ text version hashes stored as shape signatures\)**

*TypeScript 5.5’s incremental builder re-emits all transitive imports on whitespace-only edits due to exportedModulesMap removal and text-version shape hashes*

 * created by **kaiguogit**

### [PR microsoft/TypeScript#63665](https://github.com/microsoft/TypeScript/pull/63665) (Open, `For Uncommitted Bug`)

**Do not overwrite computed \.d\.ts signatures with file versions; add disableUseFileVersionAsSignature to BuilderProgramHost**

*Retain computed .d.ts signatures instead of file-version hashes to avoid false rebuilds and add disableUseFileVersionAsSignature.*

 * created by **kaiguogit**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63665#issuecomment-5039679411) **kaiguogit** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63665#issuecomment-5042719813) **MartinJohns** said "This looks like AI. Besides that, you made the changes in the wrong repository."

### [Issue microsoft/TypeScript#63666](https://github.com/microsoft/TypeScript/issues/63666) (Open)

**\[5\.9 regression\] as const readonly tuple inferred as mutable through a nested generic call under a conditional\-type circular constraint**

*TypeScript 5.9 regression infers readonly 'as const' tuples as mutable in nested generic circular conditional types.*

 * created by **xkatianx**

### [Issue microsoft/TypeScript#63667](https://github.com/microsoft/TypeScript/issues/63667) (Open)

**Ambient redeclaration of a global type alias no longer overrides the built\-in lib declaration in TypeScript 7\.0 \(regression from 6\.0\)**

*Ambient redeclaration of a global type alias no longer overrides built-in library declarations in TypeScript 7.0.*

 * created by **chrisvltn**

### [Issue microsoft/TypeScript#63668](https://github.com/microsoft/TypeScript/issues/63668) (Open)

**Package missing error from Typescript 7 via npm**

*Running TypeScript 7.0.2 offline via npm causes tsc to throw an 'Unable to resolve @typescript/typescript-linux-x64' error.*

 * created by **mind-bending-forks**

