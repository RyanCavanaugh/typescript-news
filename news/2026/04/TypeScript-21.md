# Report for 2026-04-21 (Tuesday, April 21st, 2026)

6 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @li-zck asked for a workaround in [microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4293131060)

## Activity Summary

### [Issue microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **andrewbranch**, **Copilot**)

**Deprecate, remove support for \`baseUrl\`**

*TypeScript 6.0 will deprecate baseUrl support and require explicit prefixes in paths mappings.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4205504780) **ArfanFahad** removed baseUrl and confirmed it worked after adding paths
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4220113144) **Jasper-Nelligan** reported that adding a catch-all paths entry caused VSCode to auto-suggest imports from node_modules and asked if anyone else was facing the issue
 * [today](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4288080930) **ruizmarc** confirmed experiencing the same issue where autoimports start with node_modules/ instead of the library name
 * [today](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4293131060) **li-zck** affirmed encountering the issue and asked for a workaround

### [Issue microsoft/TypeScript#63416](https://github.com/microsoft/TypeScript/issues/63416) (Closed, `Duplicate`)

**JSDoc parser treats \`@foo\` inside fenced code blocks as a tag, breaking hover previews**

*JSDoc parser does not respect fenced code blocks and incorrectly treats @tags inside them as JSDoc tags, breaking hover documentation previews.*

 * created by **BojanRatkovic**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63416#issuecomment-4276891516) **MartinJohns** said "Duplicate of #58992."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63416#issuecomment-4282661729) **RyanCavanaugh** generated an automated analysis listing similar issues
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#63418](https://github.com/microsoft/TypeScript/issues/63418) (Closed, `Unactionable`)

**VS Code: support file jump for import paths with query params \(vanilla JS\)**

*Support file navigation in VS Code for vanilla JavaScript import paths that include query parameters to address browser caching*

 * created by **j787701730**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/63418#issuecomment-4290418750) **RyanCavanaugh** provided an automated list of similar issues and guidance on duplicates
 * **RyanCavanaugh** added label `Unactionable`
 * [today](https://github.com/microsoft/TypeScript/issues/63418#issuecomment-4290572603) **RyanCavanaugh** said "No repro steps or version information. Please log a new issue with enough information."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63419](https://github.com/microsoft/TypeScript/issues/63419) (Closed, `Won't Fix`)

**Transformer that updates an ambient property declaration is emitted as non\-ambient**

*TypeScript transformers updating ambient property declarations in TS 4.3 lose the ambient flag and emit the property.*

 * created by **JoostK**
 * [today](https://github.com/microsoft/TypeScript/issues/63419#issuecomment-4290418828) **RyanCavanaugh** provided an automated analysis listing similar issues and suggesting to close if duplicate
 * **RyanCavanaugh** added label `Won't Fix`
 * [today](https://github.com/microsoft/TypeScript/issues/63419#issuecomment-4290565099) **RyanCavanaugh** said "This doesn't meet the 6.0 patch bar, and 7.0+ doesn't have a corresponding implementation for this code."

### [Issue microsoft/TypeScript#63420](https://github.com/microsoft/TypeScript/issues/63420) (Open, `Bug`, `Domain: Intersection`)

**union of pattern template literals intersected with optional brand mutually assignable to one with incompatible brand**

*TypeScript incorrectly allows mutual assignment between unions of template literal types intersected with incompatible optional brand properties.*

 * created by **jcalz**
 * [today](https://github.com/microsoft/TypeScript/issues/63420#issuecomment-4290418908) **RyanCavanaugh** provided an automated analysis of why the two branded types are structurally assignable and linked relevant FAQs and issues
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63421](https://github.com/microsoft/TypeScript/issues/63421) (Closed, `Not a Defect`)

**"Using type predicates" documentation promotes lying to the type system**

*The TypeScript documentation's type predicate example encourages misuse of 'as' assertions, undermining type safety.*

 * created by **ilyash-b**
 * [today](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4293448864) **MartinJohns** explained that type assertions bypass compiler checks and require 'lying' to the compiler
 * [later](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4296729187) **jcalz** explained that using type assertions in type predicate functions can mislead the type system, illustrated pitfalls with examples of ‘lying’ predicates, proposed stricter type definitions to avoid unsoundness, and agreed that the handbook guidance is sufficient

### [Issue microsoft/TypeScript#63422](https://github.com/microsoft/TypeScript/issues/63422) (Open)

**@typescript/typescript6 does not proxy subpath imports**

*@typescript/typescript6@6.0.0 omits a subpath exports map and tsserverlibrary file, so requiring typescript/lib/tsserverlibrary fails.*

 * created by **christopher-buss**

