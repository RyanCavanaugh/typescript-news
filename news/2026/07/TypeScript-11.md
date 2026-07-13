# Report for 2026-07-11 (Saturday, July 11th, 2026)

3 different users commented on 5 different issues.

## Recommended Actions

 * Response Recommended
    * @Mahnoor-Zaffar requested assignment to the issue in [microsoft/TypeScript#63616](https://github.com/microsoft/TypeScript/issues/63616#issuecomment-4951667613)
    * @Mahnoor-Zaffar asked to assign the issue to them in [microsoft/TypeScript#63628](https://github.com/microsoft/TypeScript/issues/63628#issuecomment-4951665353)

## Activity Summary

### [Issue microsoft/TypeScript#63616](https://github.com/microsoft/TypeScript/issues/63616) (Open, `Bug`, `Domain: This-Typing`)

**Inconsistent \`typeof this\` when the \`this\` parameter declared in the signature of a function parameter**

*Declaring a this parameter for callback functions leads to inconsistent inferred types for typeof this depending on whether this is used in the function body.*

 * (5 days ago) **RyanCavanaugh** added labels `Bug`, `Domain: This-Typing`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/63616#issuecomment-4951667613) **Mahnoor-Zaffar** noted the inconsistency with `typeof this` in function signatures and requested to be assigned to the issue

### [Issue microsoft/TypeScript#63628](https://github.com/microsoft/TypeScript/issues/63628) (Open, `Bug`, `Domain: Error Messages`)

**Incorrect diagnostic message in TS2814**

*TS2814’s misleading error “Function with bodies can only merge with ambient classes” is shown when merging a body-less function declaration with a class.*

 * (4 days ago) **RyanCavanaugh** added labels `Bug`, `Domain: Error Messages`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/63628#issuecomment-4951665353) **Mahnoor-Zaffar** noticed that the diagnostic message for function declarations was misleading when there was no body, planned to update checker.ts and diagnosticMessages.json accordingly, and asked to have the issue assigned to them

### [Issue microsoft/TypeScript#63632](https://github.com/microsoft/TypeScript/issues/63632) (Open, `Suggestion`, `Awaiting More Feedback`)

**Feature request: machine\-readable \(JSONL\) diagnostics output**

*Add a JSONL output flag to the TypeScript compiler to provide machine-readable diagnostics in watch and noEmit modes.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63632#issuecomment-4906907350) **Alex-Bond** agreed to target the change for version 7.1 to avoid additional cleanup, acknowledged overengineering by considering SARIF, JSONL, and template outputs, and explained the adapter motivation
 * (4 days ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63632#issuecomment-4948211325) **MartinJohns** said "Related: #31566"

### [Issue microsoft/TypeScript#63637](https://github.com/microsoft/TypeScript/issues/63637) (Closed, `Question`)

**v7 missing GitHub releases**

*TypeScript v7.0.2 is missing from the main repository's GitHub releases page and appears only under typescript-go.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63637#issuecomment-4923638845) **jakebailey** said "Bugs are fine to file here and that's the main place the project lives; is this causing a problem for you in some way?"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63637#issuecomment-4923690763) **hyunbinseo** mentioned confusion about how to follow up with the v7 release and updated the issue body with a tl;dr section
 * **RyanCavanaugh** added label `Question`
 * [today](https://github.com/microsoft/TypeScript/issues/63637#issuecomment-4949496717) **typescript-automation[bot]** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#63639](https://github.com/microsoft/TypeScript/issues/63639) (Closed, `Duplicate`)

**Consistent Typechecking Mode**

*Add a TypeScript compiler option enabling consistent typechecking by treating missing object keys as never or unknown.*

 * created by **p-98**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63639#issuecomment-4925849782) **MartinJohns** said "Essentially you want #12936."
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63639#issuecomment-4949496635) **typescript-automation[bot]** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

