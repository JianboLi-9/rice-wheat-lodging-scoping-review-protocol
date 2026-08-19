# Protocol Amendment v2.2 — Bibliometric Methods Specification

**Amendment ID:** AMEND-2.2-BIBLIOMETRIC-METHODS  
**Amendment type:** PROSPECTIVE ANALYTIC-METHOD SPECIFICATION / PUBLIC VERSIONING TIMING DEVIATION  
**Actual amendment creation time:** 2026-08-20 04:36:38 Asia/Shanghai  
**First formal WoS query time:** 2026-08-20 03:34:42 Asia/Shanghai  
**First formal WoS result-page count:** 217  
**Authorization source:** Current Reviewer instruction in the current existing ChatGPT Reviewer conversation and current user directive  
**Analytic decisions made before first formal search:** YES — internally frozen during the immediately preceding pre-search round  
**Public amendment published before first formal search:** NO  
**Public versioning delay:** WORKFLOW SEQUENCING DEVIATION  
**Result-driven method selection:** NO  
**Eligibility impact:** NONE  
**Search-strategy impact:** NONE  
**Database-set impact:** NONE  
**Screening impact:** NONE  
**User identity/signature:** Not supplied; none is invented

## Purpose

This amendment publicly versions the bibliometric analytic rules that were frozen internally before the first successful formal database search. It does not change Eligibility, WOS-A-001, the database set, screening, extraction, robustness mapping, Study Family rules or any Stage 2 decision.

## Truthful chronology

1. During the immediately preceding pre-search round, bibliometric Sections 21–33 were frozen internally as FROZEN PRE-CONDUCT.
2. At that internal freeze, no successful formal WoS or CNKI query, formal IEEE query, formal result count or real included corpus existed.
3. The first formal WoS query was subsequently submitted at 2026-08-20 03:34:42 Asia/Shanghai, producing a valid result-page observation of 217 records.
4. Public incorporation of the already-frozen analytic rules into Protocol v2.2 occurred afterward because of workflow sequencing.
5. No bibliometric rule was selected, tuned or altered in response to the observed WoS result count of 217. The 217 result-page observation remains valid and is not invalidated by this versioning sequence.

## Frozen analytic rules

They govern a later bibliometric analysis only after formal identification, screening, extraction boundaries and corpus provenance are complete. They do not authorize formal searching, screening, extraction, Biblioshiny or VOSviewer.

## BIB-01–BIB-03 — corpus and metadata

1. **Primary bibliometric unit:** publication level. The primary network corpus does not collapse publications to Study Families. Study Family IDs remain mandatory for structured technical synthesis and sensitivity/context reporting.
2. **Primary corpus source:** all eligible included primary-study publications identified through the frozen multi-source review process (WoS, IEEE, CNKI and approved supplementary routes as actually handled). A WoS-only subset is allowed only when a field is inherently WoS-specific and must be labelled as such.
3. **Canonical metadata:** a harmonized multi-database master record with field-level provenance. Raw source exports remain unchanged; merge metadata only after a duplicate relationship is established.

## BIB-04–BIB-06 — fields and record provenance

4. **Field harmonization:** retain raw values and create a canonical mapping with SourceDatabase, OriginalRecordID, RawFilename and FormalSearchRunID. Conflicts are not silently overwritten.
5. **Citation counts:** do not pool counts from different databases as equivalent. Any citation count is contextual descriptive metadata with source and retrieval date; it is not a quality or performance measure.
6. **Citation-discovered records:** preserve as a separately labelled provenance layer. They enter the primary bibliometric corpus only when they satisfy the frozen eligibility/provenance rules; otherwise report them separately. No silent corpus expansion is permitted.

## BIB-07–BIB-08 — units and networks

7. **Study Family versus publication:** publication-level primary bibliometric networks; Study Family sensitivity/context output is optional and separate.
8. **Citation/co-citation unit:** publication/document level where a source-specific network is justified. If cited-reference data are not consistently available across the multi-database corpus, do not fabricate a full-corpus network; use a clearly labelled source-specific subset with denominator, selection rule and limitations.

## BIB-09–BIB-10 — normalization and counting

9. **Author/institution normalization:** deterministic normalization, ORCID only where actually available, verified institutional metadata and manual thesaurus review. Fuzzy merges remain candidates until manually verified.
10. **Counting and normalization:** full counting for publication/productivity and primary keyword co-occurrence; fractional counting for primary co-authorship where supported; VOSviewer association-strength normalization where applicable. Numeric network thresholds are data-dependent and must be recorded after corpus freeze; they must not be tuned to manufacture clusters.

## Keyword and language rule

The primary thematic/keyword network uses author-supplied keywords. Keywords Plus is not silently combined with the primary multi-database network; a WoS Keywords Plus subset may be reported only as a labelled supplementary analysis. Preserve OriginalKeyword, OriginalLanguage, NormalizedConcept and NormalizedEnglishConcept; ambiguous translations require manual review.

## Software roles and reporting

- **bibliometrix/Biblioshiny:** descriptive bibliometric analysis, thematic structures and data inspection where appropriate.
- **VOSviewer:** network visualization/mapping.

Record exact software versions, parameters, corpus denominator, unit of analysis, source fields, counting method and threshold values at execution time. Software defaults must not redefine eligibility. No formal bibliometric analysis has been run in this pre-conduct state.



## Reporting boundary

No formal bibliometric corpus is frozen and no Biblioshiny/VOSviewer/bibliometrix analysis has been run. These rules become operational only after formal identification, screening, extraction boundaries and corpus provenance are complete. Software defaults may not redefine eligibility.



