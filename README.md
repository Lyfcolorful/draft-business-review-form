# Draft a Business Review Form

A reusable agent skill for turning business plans, process documents, spreadsheets, and historical inputs into prefilled working methods that nontechnical business owners can review.

The agent does the source reading and prefilling. The reviewer checks the actual way of working, amends differences, and resolves genuine open decisions.

## What it produces

Each review row connects a concrete situation, a proposed method, a specific business decision, the information needed to assess it, and an example change request. The reviewer's actual comment field stays blank.

The skill preserves adopted rules, distinguishes suggestions and unresolved points, and avoids asking the reviewer to repeat information already available in the sources.

## Package contents

```text
draft-business-review-form/
|-- SKILL.md
|-- README.md
`-- references/
    `-- review-row-example.md
```

`SKILL.md` is the skill entry point. The reference contains one generic example; it does not prescribe a universal customer-support workflow.

## Use

Make the complete folder available to a skill-capable agent using that environment's supported skill-loading mechanism. Keep the reference file beside the entry point at the relative path shown above. In an environment without skill loading, provide `SKILL.md` and its reference as task instructions.

Example request:

> Use draft-business-review-form to turn the attached process plan and historical notes into a prefilled review workbook for a nontechnical operations manager. Preserve the original files, distinguish existing rules from suggestions and unresolved points, and leave actual reviewer comments blank.

Supply the relevant source materials, intended reviewer, desired format, and output destination. The skill does not include a spreadsheet generator or external service connector; the agent uses the artifact tools available in its environment.

## Scope

This is a business-method review workflow. It does not replace an implementation-readiness questionnaire, expand formatting-only requests, or authorize publishing, sending messages, or changing external systems.

The example is generic. This distribution contains no source customer records, original business documents, conversation logs, local validation logs, account identifiers, or machine-specific paths. No runtime dependencies or credentials are bundled.
