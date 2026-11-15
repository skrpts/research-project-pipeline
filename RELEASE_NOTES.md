# Release Notes

## v1.1.33
GH#1214 — the bibliography stage v1.1.32 added did not actually run. It does now.

v1.1.32 declared the stage with `id: "citation-format-templates"`, pointing at a citation-format
template. A template is an asset, and only a skill or a prompt can back an executable step — so the
entry matched no planner branch and was dropped silently, with no error and no warning. The stage
was present in the catalogue, listed in the pipeline, and produced nothing.

It is now backed by a new **Bibliography Building** skill, which is what the stage actually does.
The citation-format templates remain declared as reference material, which is their correct role.

Skills 2 → 3, total 8 → 9.

## v1.1.32
GH#1189 — the bibliography stage now runs. It was documented from the start and never wired.

Stage 4 of this pipeline has always promised to "format all cited sources into the required citation style", and an annotated bibliography has always been listed among the outputs — but no execution entry invoked the `bibliography-builder` prompt, so the stage never ran and the bibliography was never produced. The prompt and the prose were added in the same original commit; nothing was ever removed. This was a stage that was never built, not one that was retired.

It now runs after note-taking, which is where its own input comes from (`{{steps.Note-Taking.output}}`) and where the documentation places it. It produces a new `bibliography` output.

Also in this version:
  `language-polish` now declares `bindings: source` ← `Citation Extraction` instead of resolving that slot by position. The value is unchanged — position already resolved to Citation Extraction, and it still does — but the dependency is now stated, so a future reorder cannot silently feed the polish step a different artefact.
  Dependency pin `polish-language` 1.0.1 → 1.0.7, the published version that declares the `source` slot the binding targets. Checksum resolved against live Hub rather than transcribed.

This version also repairs the catalogue record. The row describing this package had not been rewritten since v1.1.30 and still described that version's workflow, because v1.1.31's catalogue write did not land (GH#1113, fixed three days after that publish). Publishing this version rewrites it.

## v1.1.31
GH#1044 — document the inputs this workflow's prompts REQUIRE but its Inputs table never listed. A user supplying exactly what the table asked for was running with required parameters unsatisfied — a silent wrong run, not a documentation nicety. documented 3 input(s): module_name, study_material, topic. Every row is generated from the requiring prompt's own declared description, example and required flag — none invented. No behaviour change; documentation only.

## v1.1.30
GH#845 — republish with American English (en-US) content, completing the source-only GH#805 flip that never reached the Hub. Copy only — no functional or behaviour change.

## v1.1.29
GH#745 — declare per-step `output: {name, type}` on every execution step (source_evaluation/text, reading_analysis/text, notes/text, interpretation/text, citations/list, polished_output/text). Lights up the #744 rich flow-map with named, typed outputs. Content-only; no bindings or logic changes.

## v1.1.28
GH#645 Row 3b — migrate to K-037 dep-referenced schema. Strip 14 inline shared-content files and declare 14 hub-shared deps (UUID id + slug name + version + checksum from `gen-dep-checksums.mjs`). Closes pre-Step-3 inline-vendoring for this bundle.

## v1.1.27
Wave 2: re-signed with canonical engine signing pipeline.

## v1.1.26
Tags migrated inline into manifest (GH#586). tags.yaml retired.

## v1.1.25
Bundle re-signed with canonical engine signing pipeline (Wave 2 migration).

## v1.1.24
Signature fix — RELEASE_NOTES.md now included in integrity checksum.

## v1.1.23
Initial catalog release with full structural and content-quality validation. All scanner checks pass.
