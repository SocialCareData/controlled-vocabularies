# Controlled Vocabularies

## Status

Version 0.2 - ready for testing

Effective Date: 2025-09-11

This repository contains the controlled vocabularies, taxonomies, and categorical code lists utilized across the social care data standards. 

The Structure of `ObservationType`
The `ObservationType` schema within `vocabularies.json` is currently designed with a mixture of:
*   **Pre-coordinated Findings / Boolean Indicators:** Simple episodic states (e.g., `NEET`, `free-school-meals`, `pupil-premium`, `temp-accomodation`, `non-accidental-injury`, `asd-diagnosis`) where the existence of the observation on a start/end date implies the active truth of the state.
*   **Post-coordinated Attributes / Observable Entities:** Hierarchical question-like elements (e.g., `religion`, `EAL` (English as an Additional Language), `SEND`) that logically require a distinct code/value to form an assertion (e.g., Religion = Muslim).

Because the `Observation` object inside `serviceEpisode.json` lacks an independent `value` field, these multi-valued attributes are modeled using nested wildcard nodes (e.g., `EAL.$ISO 639-1 Code$`, `religion.$HL7 Religious Affiliation Code$`) to pack the value into the `type` string.
