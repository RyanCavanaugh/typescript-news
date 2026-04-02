# Report for 2026-03-14 (Saturday, March 14th, 2026)

2 different users commented on 4 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#3081](https://github.com/microsoft/TypeScript-go/issues/3081) (Open)

**Stack overflow in multi\-threaded mode during type instantiation**

*tsgo 7.0.0-dev encounters a goroutine stack overflow in multi-threaded type instantiation on a large React/TypeScript codebase, while single-threaded mode works.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4057291353) **ahejlsberg** explained that concurrent checking can cause differences and asked for a repro
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4059658320) **shahmir-oscilar** found that the error was due to an older react-hook-form version, recommended upgrading to the latest version, and suggested the issue could be closed
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4059818295) **jakebailey** suggested running TypeScript 6.0 with --stableTypeOrdering to reveal the circular error
 * [today](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4061756525) **shahmir-oscilar** tried running TS 6.0 with --stableTypeOrdering and found no errors

### [Issue microsoft/TypeScript-go#3098](https://github.com/microsoft/TypeScript-go/issues/3098) (Open, `Domain: Editor`)

**"Peek References" does not show matches in other files**

*Enabling typescript.experimental.useTsgo in Cursor prevents Peek References from showing cross-file TypeScript references.*

 * created by **timephy**
 * **timephy** added label `Domain: Editor`

