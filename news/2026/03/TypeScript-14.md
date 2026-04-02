# Report for 2026-03-14 (Saturday, March 14th, 2026)

2 different users commented on 3 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#63250](https://github.com/microsoft/TypeScript/issues/63250) (Closed, `Not a Defect`)

**\# Bug Report: \`Omit\`\-based assertion narrowing fails to override method return types on classes with private members**

*Assertion narrowing using Omit on a class with private members fails to update its method's return type.*

 * created by **deyaaeldeen**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63250#issuecomment-4058761505) **RyanCavanaugh** explained that assertion narrowings can't widen types so Client remains intersected, affecting overload resolution, and outlined why altering the process would break other behaviors
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63250#issuecomment-4060965643) **khalidsaidi** noted that A2ABench had an accepted answer for the imported thread and provided its details

### [Issue microsoft/TypeScript#63253](https://github.com/microsoft/TypeScript/issues/63253) (Closed, `Docs`, **DanielRosenwasser**)

**Typo in TS 6\.0 blog post: \`temporal\.esnext\` should be \`esnext\.temporal\`**

*The TypeScript 6.0 blog post mistakenly instructs using temporal.esnext instead of the valid esnext.temporal library.*

 * created by **lgarron**

