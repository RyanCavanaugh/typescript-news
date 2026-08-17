# Report for 2026-08-15 (Saturday, August 15th, 2026)

2 different users commented on 2 different issues.

## Recommended Actions

 * Moderation
    * @guillaume-mueller posted rude content in [microsoft/TypeScript#21759](https://github.com/microsoft/TypeScript/issues/21759#issuecomment-5306554910)

## Activity Summary

### [Issue microsoft/TypeScript#21759](https://github.com/microsoft/TypeScript/issues/21759) (Open, `Suggestion`, `Awaiting More Feedback`)

**SUGGESTION: add support for writeonly properties on interfaces**

*They suggest adding a writeonly keyword to TypeScript interfaces to support setter-only properties and simplify patterns like child-to-parent data publishing.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/21759#issuecomment-2080738937) **sorgloomer** noted lack of mapped type support as a shortcoming and suggested a built-in Writeonly type
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/21759#issuecomment-2234088869) **CraigMacomber** described the lack of mapped type support for getters/setters, proposed a Writeonly type workaround, and suggested marking the thread as a duplicate of issue #43826
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/21759#issuecomment-2744576801) **alexreardon** described the need for "writeonly" properties for the React ref prop, illustrated type constraint issues with code examples, and asked if the issue should be raised elsewhere
 * [later](https://github.com/microsoft/TypeScript/issues/21759#issuecomment-5306554910) **guillaume-mueller** expressed frustration and stated that accessing a setter property without error was a bug, urging simplicity and JavaScript consistency

### [Issue microsoft/TypeScript#63737](https://github.com/microsoft/TypeScript/issues/63737) (Closed, `Not a Defect`)

**Superclass type argument inferred as unknown when it's only used as a method parameter type constraint**

*TypeScript infers unknown when extracting a superclass’s generic type used only in a method parameter constraint instead of the expected type.*

 * **RyanCavanaugh** added label `Not a Defect`
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63737#issuecomment-5257232755) **jcalz** suggested issue #7234 and explained that B<boolean> extends B<infer T> works because TypeScript uses instantiation-based inference without a structural check
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63737#issuecomment-5281727576) **aweebit** demonstrated a simplified reproduction of the TypeScript inference issue in mapik when composing mappers
 * [today](https://github.com/microsoft/TypeScript/issues/63737#issuecomment-5305148839) **typescript-automation[bot]** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

