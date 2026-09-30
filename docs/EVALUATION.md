# Evaluation methodology and limits

## Fixed comparison

The reported comparison uses the same 70-case evaluation contract across seven workflow types,
with ten cases per workflow. Both runs completed all 70 cases. The public JSON contains only
aggregate values; raw legal questions, answers, reviewer outputs, and corpus excerpts are private.

The provisional pass criterion combined structured-output requirements, required evidence and
citation behavior, forbidden-hallucination checks, and an internal rubric threshold. Critical
errors were tracked separately so that a higher aggregate score could not hide severe failures.

## Result

- provisional pass rate: `20/70 (0.2857)` to `43/70 (0.6143)`;
- critical errors: `39` to `12`;
- forbidden-hallucination flags: `6` to `3`;
- mean rubric score: `5.400` to `7.429`.

The result supports a bounded claim: failure-driven changes improved this fixed internal rubric.
It does not establish general legal correctness, production readiness, or superiority to another
system.

## Limitations

- `legal_accuracy_certified` was false for both runs.
- The evaluation corpus was restricted to noncommercial research/evaluation use.
- The system did not have a complete, continuously current, commercially approved legal corpus.
- Aggregate values do not replace review by qualified legal professionals.
- Public evidence omits raw content to respect licensing, privacy, and product-IP boundaries.
