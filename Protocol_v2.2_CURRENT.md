# Protocol v2.2 CURRENT — Full Protocol plus prospective Amendments v2.1, v2.1a and v2.2

> **CURRENT OPERATIVE VIEW**  
> **v2.0 substantive content remains FINAL / FROZEN**  
> **AMEND-2.1-REG-TIMING + AMEND-2.1A-PUBLIC-AVAILABILITY: prospective administrative amendments**  
> **AMEND-2.2-BIBLIOMETRIC-METHODS: prospective analytic-method specification, publicly versioned after the first formal WoS identification run because of workflow sequencing**  
> **Formal WoS WOS-A-001 query/count executed 2026-08-20 03:34:42 / result page count 217; RAW export pending; no screening or extraction**

## Amendment control

This file carries forward the complete substantive content of `Protocol_v2.0_FINAL.md` and applies `Protocol_Amendment_v2.1_Registration_Timing_20260819.md`, `Protocol_Amendment_v2.1a_Public_Availability_20260820.md` and `Protocol_Amendment_v2.2_Bibliometric_Methods_20260820.md`. v2.1 and v2.1a change only administrative registration/public-availability timing. v2.2 publicly versions analytic rules that were frozen internally during the immediately preceding pre-search round, before the first successful formal WoS query, but the public incorporation occurred afterward because of workflow sequencing. v2.2 changes no review design, research questions, Population, Concept, Context, Eligibility, language/year/publication-type rules, database set, WOS-A-001, Stage 2, screening, extraction, robustness or Study Family rules, and no analytic rule was selected or altered in response to the WoS result count of 217. v2.0 and v2.1a remain preserved as historical protocol states.

# Protocol v2.0 substantive content carried forward

**Project:** 水稻小麦倒伏综述_正式版_2026  
**Working title:** *Remote Sensing and Intelligent Sensing of Rice and Wheat Lodging: A Scoping Review and Bibliometric Analysis of Technological Evolution, Quantitative Assessment, and Research Gaps*  
**Title status:** Working title — subject to refinement  
**Version:** v2.2 CURRENT (v2.0 substantive content frozen; v2.2 analytic-method specification publicly versioned)  
**Revision date:** 2026-08-20  
**Stage:** Stage 3 formal identification underway; prospective amendments recorded  
**Status:** CURRENT CONTENT FROZEN; PUBLIC v2.2 AVAILABLE; FORMAL WOS QUERY/COUNT EXECUTED; RAW EXPORT PENDING; CNKI SECURITY CHALLENGE; IEEE PENDING

## 1. Review design

本项目采用：

> **A scoping review with embedded bibliometric analysis and structured descriptive technical mapping.**

中文表述为：**以范围综述为主体，嵌入文献计量分析，并开展结构化描述性技术映射。**

- **Scoping Review** 是总体证据综合框架，用于依据PCC映射证据范围、概念、平台、传感器、任务、算法、验证设计与研究空白。
- **Embedded bibliometric analysis** 是嵌入式宏观科学计量分析，用于描述最终核心原始研究语料库的产出、来源、合作和知识/主题网络。
- **Structured descriptive technical mapping** 基于数据提取矩阵进行情境化的技术比较，不是meta-analysis、quantitative evidence synthesis或effect-size comparison。

由于研究在平台、传感器、标签单位、任务、数据集和验证设计方面高度异质，本协议不预设效应量合并。不同研究的Accuracy、F1、IoU等结果只有在任务、作物、数据集、标签定义、训练/测试划分和验证情境可比时才能并列描述；不得仅凭95%高于90%就断言一种方法优于另一种方法。正式综合采用**context-aware descriptive comparison**。

## 2. Introduction

Lodging is the displacement or collapse of crop stems and/or the failure of the root–soil anchorage system. In rice and wheat, lodging can reduce light interception, disrupt canopy structure, increase disease and moisture problems, impede harvest, and reduce grain yield and quality. The timing, extent and geometry of lodging matter: an early event may alter subsequent growth, whereas lodging near grain filling can produce substantial yield and harvest losses. Lodging is therefore simultaneously an agronomic outcome, a structural phenotype, a management risk and a spatially explicit event. A protocol for evidence mapping must accommodate all of these meanings without treating them as interchangeable outcomes.

Historically, lodging has been assessed by field walks, visual scores, angle measurements, quadrat estimates and post-event agronomic observations. These approaches remain important because they provide reference labels and contextual information, but they are labour intensive, observer dependent and difficult to repeat over large areas or across rapidly changing weather conditions. They also capture different units: a plot-level score, a lodged-area fraction, a plant or stem angle, a binary lodged/non-lodged label, a susceptibility class or a seasonal risk estimate are not the same construct. A central methodological problem is therefore not simply whether a sensor detects lodging, but what is observed, at which spatial and temporal unit, against which reference, and for which decision.

Remote sensing and imaging have expanded the observation space from ground measurements to vehicle- and harvester-mounted cameras, unmanned aerial vehicles (UAV/UAS), airborne systems and satellite platforms. Ground and proximal measurements can provide detailed spectral, radiometric or structural information under controlled conditions. Vehicle and harvester systems can capture observations close to operational decisions. UAV imagery can deliver high spatial resolution, repeatable plot coverage and RGB, multispectral, thermal or three-dimensional products. Airborne and satellite systems provide broader spatial coverage and multi-temporal observations, although cloud, revisit time, spatial resolution and mixed pixels may constrain interpretation. The 2019 review by Chauhan and colleagues groups crop-lodging remote-sensing work into ground-based, airborne and spaceborne platforms and identifies the continuing gap between experimental demonstrations and operational large-area deployment ([Chauhan et al., 2019](https://doi.org/10.1016/j.isprsjprs.2019.03.005)).

The sensor repertoire has also diversified. Passive spectral observations include visible, red-edge, near-infrared and hyperspectral reflectance; thermal observations can indicate canopy temperature differences; active sensors include radar and polarimetric SAR; structural observations include LiDAR, depth, point clouds, binocular reconstruction, photogrammetry and surface models. Lodging may change canopy orientation, shadowing, exposed soil, backscatter, height distribution, texture and reflectance. A method can therefore be sensitive to a lodging-related signal without directly measuring the underlying mechanical cause. This distinction is important when comparing a spectral index, a polarimetric feature, a segmentation mask, a point-cloud descriptor and a risk model. They may answer related but non-identical questions.

Analytical approaches have evolved from visual interpretation, spectral ratios, vegetation indices, texture measures, thresholds and object-based image analysis to statistical learning, random forests, support-vector machines, convolutional neural networks, semantic segmentation, temporal models and multimodal fusion. For example, rice UAV studies have combined visible imagery, vegetation indices and deep-learning segmentation ([Yang et al., 2020](https://doi.org/10.3390/rs12040633)), while wheat studies have used multi-temporal Sentinel-1/Sentinel-2 observations and SAR-based angle or susceptibility modelling ([Chauhan et al., 2020a](https://doi.org/10.1016/j.rse.2020.111804); [Chauhan et al., 2020b](https://doi.org/10.1016/j.rse.2019.111488)). These examples illustrate technological evolution, but they do not make performance numbers directly comparable.

Direct ranking of Accuracy, F1, IoU, correlation or error is inappropriate across heterogeneous studies. Metrics depend on task definition, class balance, label quality, spatial support, training/test partition, image resolution, cultivar, growth stage, weather and whether observations from the same field or year occur in both training and test sets. Random splits can be optimistic when neighbouring plots or dates share information; spatial, temporal, cross-year, cross-site and external validation answer different generalisation questions. Ground truth may be a visual score, field survey, destructive measurement, expert annotation, yield consequence or a derived map. A high score on a narrow and potentially leaky split does not establish superiority over a lower score obtained under a genuinely independent external test. The protocol therefore uses context-aware descriptive comparison rather than unconditional performance ranking.

Both rice and wheat are included because they are major agricultural cereals with distinct canopy architectures, management systems, phenology and lodging expressions, while sharing a need for scalable monitoring. Rice/paddy/Oryza studies may involve flooded fields, dense canopies and different viewing geometries; wheat studies may involve winter, spring, bread/common, durum or other clearly agricultural subtypes. Excluding a study solely because it uses a specific subtype would create an avoidable coverage bias. Mixed-crop studies will be included only when rice- or wheat-specific evidence can be separated. No initial publication-year cutoff is used because early spectral, Landsat and SAR routes are part of the technological history; the formal search will run across each selected database's available coverage up to an actual, recorded final search date.

A scoping review is appropriate because the evidence is conceptually broad and methodologically heterogeneous. The objective is to map platforms, sensors, modalities, tasks, labels, algorithms, validation designs, robustness signals and research gaps rather than to pool a common effect size. Embedded bibliometric analysis will describe production, sources, collaboration and themes only after the included primary-study corpus and the later bibliometric corpus are frozen. Structured descriptive technical mapping will connect technology choices to observation requirements, ground truth and validation context. This hierarchy follows the logic of a scoping review while preventing bibliometric or visual-mapping outputs from silently redefining eligibility.

The preliminary review-of-reviews check identified Chauhan et al. (2019) as the principal anchor/navigation review. It provides broad historical and technological context, but the present protocol differs by focusing explicitly on agricultural rice and wheat lodging, including Chinese-language eligibility and CNKI as an approved evidence-identification source, retaining conference papers when sufficient primary methodology and results are present, excluding standalone preprints from the Core Evidence Corpus, and charting label units, leakage risks, cross-year/site/cultivar validation, external validation and reproducibility. The current project therefore adds an auditable evidence-identification strategy, a separate bibliometric-corpus gate and a structured technical map designed to preserve methodological context rather than flatten it into a single ranking. The search terms, platforms, date, limitations and identified-review roles are archived in `00_Protocol\\Review_Preliminary_Search\\Existing_Review_Preliminary_Search_Log.md`.

The overarching objective is to map how sensor-derived spectral, radiometric, spatial, structural and image observations are used to monitor, detect, classify, segment, quantify or assess agricultural rice and wheat lodging; to describe technological evolution from conventional sensing and analysis to machine learning, deep learning and multimodal systems; to characterise ground truth, validation and robustness; and to identify evidence, methodological and operational gaps. This objective is aligned with the PCC framework and with the protocol's planned JBI-concordant source-selection process.

## 3. Review objectives

1. 描述最终核心原始研究语料库在年份、期刊、作者、机构、国家/地区和合作网络方面的演变。
2. 总结水稻和小麦倒伏研究使用的观测平台。
3. 总结传感器类型、数据形态和空间/时间/光谱分辨率。
4. 总结倒伏检测、分类、分割、映射和量化任务。
5. 梳理从传统光谱、纹理和图像处理到机器学习、深度学习和多模态方法的算法路线。
6. 分析ground truth获取方式、标签单位和样本规模。
7. 分析训练、验证、测试和性能指标设计。
8. 分析cross-year、cross-site、cross-cultivar和external validation的实施情况。
9. 分析数据集、代码、模型和实验设置的开放情况。
10. 识别技术与方法学局限。
11. 提出未来研究方向和可验证的研究议程。

## 4. Research questions

- **RQ1**：最终纳入的核心原始研究语料库在发表年份、来源期刊、作者、机构、国家/地区及合作网络方面呈现怎样的发展特征？所有performance和合作描述均限定为**the included primary-study corpus**，不声称代表所有crop-lodging publications。
- **RQ2**：纳入的水稻和小麦倒伏研究使用了哪些观测平台和传感器？
- **RQ3**：在满足观测数据要求的前提下，从传统光谱、纹理和图像处理，到机器学习、深度学习和多模态方法，算法路线如何演化？
- **RQ4**：纳入研究量化了哪些倒伏指标（lodged/non-lodged、area、rate、degree、severity、angle、direction、susceptibility、risk）？
- **RQ5**：不同研究如何获取ground truth？
- **RQ6**：模型如何训练、验证和测试？
- **RQ7**：是否进行了cross-year、cross-location、cross-cultivar或external validation？
- **RQ8**：当前核心原始研究存在哪些主要技术和方法学局限？
- **RQ9**：未来最值得发展的方向是什么？

## 5. PCC framework

### Population

Include agricultural rice and wheat lodging studies. Wheat includes winter wheat, spring wheat, bread/common wheat, durum wheat and other clearly agricultural wheat subtypes if encountered. Rice includes cultivated rice studies identified as rice, paddy or Oryza in an agricultural lodging context. A study is not excluded solely because it uses a specific subtype. Mixed-crop studies are included only when rice/wheat-specific evidence can be separately identified.

### Concept

核心概念为**以遥感、成像、机器视觉或 sensor-derived spectral, radiometric, spatial, structural, or image observations 为主要输入的作物倒伏监测及定量评价**。允许的分析包括传统图像/光谱分析、图像处理、机器学习、深度学习、计算机视觉和数据融合，但分析算法不能代替观测数据要求。

### Context

场景包括农业田间、实验小区、表型环境和收获环境；平台包括ground-based、vehicle-mounted、harvester-mounted、UAV/UAS、airborne和satellite。

## 6. Core evidence corpus vs contextual literature

### Core Evidence Corpus

仅由最终Eligibility Criteria筛选通过的研究组成，用于范围综述主体、结构化技术映射，并在语料库冻结后进行嵌入式Bibliometric Analysis。核心计量描述只代表**included primary-study corpus**。Reviews、背景文章和仅用于citation chasing的来源不得偷偷混入核心网络。

### Contextual / Background Literature

用于倒伏机理、茎秆力学、育种、农艺、已有综述、方法背景、术语收割和citation searching导航。若不满足Core Eligibility，不进入核心计量语料库；其角色和引用用途单独记录。

## 7. Eligibility Criteria v2.0 FINAL CANDIDATE (v1.2 preserved as historical)

字段化候选版本见 `00_Protocol\Eligibility_Criteria_v2.0_FINAL_CANDIDATE.xlsx`；`Eligibility_Criteria_v1.2.xlsx`保持不变，作为历史版本保留。

### 7.1 Population and lodging relevance

- 研究对象为rice或wheat；混合作物只有在能单独提取rice/wheat结果时才考虑纳入。
- Lodging必须是主要研究目标、结果、监测任务或定量评价目标；仅在Introduction、Keywords Plus、背景或Discussion偶然出现的研究排除。

### 7.2 Technology eligibility — two conditions

#### Observation requirement

研究必须使用remote sensing、imaging、machine vision，或sensor-derived spectral、radiometric、spatial、structural或image observations作为主要观测输入之一。允许示例包括satellite/airborne/UAV/UAS sensing、RGB、多光谱、高光谱、热红外、radar/SAR/PolSAR、LiDAR、laser scanning、point cloud、depth camera、binocular camera、3D sensing、field spectroradiometer、canopy spectral reflectance、non-imaging spectral measurement和radiometric sensing；这些观测必须用于rice/wheat lodging的monitoring、detection、identification、mapping、assessment、quantification或phenotyping等核心任务。

#### Analysis requirement

研究可以使用传统图像/光谱分析、image processing、machine learning、deep learning、computer vision或multimodal/data fusion进行分析。

**机器学习或深度学习本身不能单独满足Technology Eligibility。** 纯农艺测量、茎秆力学性状、施肥数据、基因型性状或表格型育种数据，即使使用Random Forest、SVM、XGBoost或Neural Network，如果没有遥感、图像、机器视觉或传感器观测作为核心输入，不得进入Core Evidence Corpus。

### 7.3 Study type, language and year

- Primary research enters the core candidate set. Full conference papers/proceedings papers are eligible when they contain sufficient primary-study methodology and results and otherwise meet PCC/Eligibility. Conference abstracts, poster abstracts, extended abstracts without sufficient methods/results and presentation-only records are excluded. Study Family ID links conference and journal versions; multiple reports of the same underlying study are not double-counted in structured technical synthesis.
- Standalone preprints do not enter the Core Evidence Corpus. They may be retained in a contextual/supplementary tracking file; when a peer-reviewed final publication exists, the final publication is linked through Study Family ID.
- **Final language eligibility: English + Chinese.** No WoS language filter will be applied during formal searching unless required by database mechanics; language eligibility is normally applied during screening. CNKI searching will use the approved Chinese terminology and the Chinese implementation record.
- **Publication year：No lower publication-year restriction will be applied. Each database will be searched across its available coverage up to the date of its actual formal execution. The final search date for the formal search cycle will be the actual date on which the last prespecified database is searched. Formal database searches should be executed within the narrowest feasible time window, target <=48 hours, and every database-specific execution date/time will be recorded in Asia/Shanghai timezone.** 中文为：正式检索不设置出版年份下限；每个数据库检索至其实际正式执行日期的可用覆盖范围。正式检索周期的final search date是最后一个预设数据库实际执行检索的日期。正式数据库检索应在可行的最窄时间窗内完成，目标不超过48小时，并记录每个数据库的Asia/Shanghai执行日期和时间。不得预先虚构未来正式检索日期。

## 8. Information sources and database roles

The prespecified formal evidence-identification sources are **Web of Science Core Collection, IEEE Xplore and CNKI**. Scopus was considered and a translation draft was developed, but it is **not included in the prespecified formal database set at protocol freeze because authenticated institutional document-search access could not be secured**. If Scopus becomes available during the formal review, adding it requires a documented protocol amendment. Backward and forward citation searching are approved supplementary methods under Step 3. Google Scholar and Crossref are supplementary discovery/verification sources only, not primary formal bibliographic databases. Bibliometric corpus source/field integration follows the frozen AMEND-2.2 rules and is not automatically identical to the evidence-identification sources. The historical decision table remains archived in `00_Protocol\Information_Sources_Decision_Table.xlsx`. 区分：

1. **Evidence Identification Sources**：尽可能全面识别证据。
2. **Bibliometric Corpus Source**：提供字段一致、可重复的计量语料库。

Main bibliometric corpus尚未最终冻结；publication-level unit, source/field provenance, canonical mapping, citation handling, author-keyword primary network and counting/normalization rules are frozen by AMEND-2.2. Corpus membership and source-specific field availability will be recorded after formal identification and screening; no rule is silently changed.

## Protocol dissemination / public availability

JBI要求在开展范围综述前先制定a priori protocol；JBI当前章节说明范围综述协议可以通过Open Science Framework（OSF）、Figshare或发表协议的期刊公开获得。PRISMA-ScR也要求报告协议是否存在及其访问地址。

因此，本项目在 v2.1/v2.1a 前瞻性行政修订下确定：**OSF registration metadata/identifier and the irreversible public action may occur later, but a legitimate public version of Protocol v2.1a CURRENT must be available before formal Stage 3 evidence identification under strict JBI reporting.** Approved repository remains **Open Science Framework (OSF)**, with preferred registration type **Generalized Systematic Review registration**; another legitimate public protocol route may be used only when authorized and recorded. No OSF submission is made by this amendment. The human OSF Register/Submit/Make Public action remains required later, and its actual date, URL, registration identifier and DOI (if any) must be recorded. The D-drive copy remains a local audit/working copy and cannot substitute for public availability.

## 9. Search development

### Step 1 — Initial / exploratory search and seed identification (completed protocol-development work)

JBI Step 1 second-database developmental search was executed using two appropriate online databases, but the final abstract/index-term evidence gate remains open:

1. **Web of Science Core Collection** — official Shandong University of Science and Technology WebVPN/CAS route, 2026-08-18; purpose: seed identification, seed verification, term harvesting and strategy development.
2. **IEEE Xplore Digital Library** — official IEEE Xplore Basic Search, 2026-08-19 01:50:53 Asia/Shanghai; purpose: limited engineering/sensing terminology validation against a second topic-relevant bibliographic database.

Both were protocol-development searches only. They were not formal review searches, were not entered into PRISMA, and their counts are not formal identification counts. The IEEE result set contained 22 records and the title/result-metadata terminology check found no new major crop, lodging, observation/sensing, sensor or platform concept requiring amendment of WOS-A-001. **JBI Step 1 final status: second-database search executed; title/result-metadata terminology check completed; abstract/index-term human verification completed from human-supplied evidence on 2026-08-19; no new major concept identified; WOS-A-001 remains frozen.** CNKI remains an approved formal Chinese-language evidence-identification source, but no formal CNKI search was performed; the current browser TLS/script issue is not a methodological exclusion of CNKI.

### Step 2 — Full search strategy development and translation (completed protocol-development work)

Using Step 1 terms, the project completed concept-block development, WOS-A-001/WOS-B-001/WOS-C-001 candidate construction, Boolean/field/proximity testing, full local development exports, fixed-seed retrieval validation, supplementary challenge-route checks, developmental Noise QA, an internal PRESS pre-check, and IEEE Xplore/CNKI translation drafts. A Scopus translation draft is retained as an archive/development record but Scopus is not in the prespecified formal database set at protocol freeze. These activities were developmental only. **Seed retrieval validation belongs to Step 2.**

### Step 3 — Supplementary searching

在正式数据库检索和主要筛选流程完成相应阶段后，Step 3正式实施对预先定义关键来源的backward citation searching与forward citation searching。具体seed reference选择、实施顺序、每轮迭代和停止规则在正式citation-search protocol中定义。reference list checking作为backward方法的操作形式记录；relevant grey literature searching、co-cited searching、co-citing searching和iterative citation searching的深度仍需确认。不得把Step 3与主检索式开发混为一谈。

## 10. Citation searching and TARCiS audit

Backward和forward citation searching现在是本项目正式Step 3 supplementary searching的计划组成，并使用TARCiS术语。每次补充检索记录Seed reference、Search method、Backward/forward、Source/platform、Search date、Number retrieved、Number screened、Number eligible、Number finally included、Deduplication、Eligibility decision和Notes。co-cited、co-citing、iterative citation searching深度，以及citation-searching发现的新文献是否进入Main bibliometric corpus仍需用户确认；本阶段不执行citation searching。

## 11. Search validation, PRESS and WoS

候选策略必须评估seed retrieval performance、sensitivity-oriented search development、noise/false-positive burden、logical correctness和reproducibility。项目当前只计算Seed Retrieval Rate，不把它表述为全领域覆盖率估计。PRESS检查研究问题转换、Boolean/proximity、subject headings、text words、拼写、语法、truncation、wildcards、limits、filters、日期、语言和字段标签。

Clarivate当前官方字段定义用于解释TS/Topic、TI/Title、AB/Abstract和AK/Author Keywords。TS包含Title、Abstract、Author Keywords和Keywords Plus；TS不得写成Author Keywords。Search History、完整查询、数据库/平台、日期、限制条件和导出字段必须在正式阶段记录。


## 11.1 Stage 2 final consolidation — development record

This subsection records the completed offline Stage 2 development work. It is not a formal database search record, does not create PRISMA counts and does not override the frozen AMEND-2.2 analytic rules or the later corpus gate.

**Key development database:** Web of Science Core Collection, executed through the official Shandong University of Science and Technology WebVPN/CAS authenticated development session.

**Preferred Development Strategy:** WOS-A-001 (frozen). WOS-C-001 is retained as a precision-oriented diagnostic alternative; WOS-B-001 is retained as a proximity diagnostic alternative. No A-002, B-002 or C-002 was created.

### WOS-A-001 exact development query

```text
TS=((rice OR paddy OR "Oryza sativa" OR wheat OR "Triticum aestivum") AND (lodg* OR "crop lodging" OR "plant lodging" OR "lodging severity" OR "lodging angle" OR "lodging susceptibility" OR "lodging risk") AND ("remote sensing" OR satellite* OR airborne OR UAV OR UAS OR drone* OR RPAS OR "unmanned aerial vehicle*" OR imaging OR imagery OR "machine vision" OR spectr* OR reflectance OR spectroradiometer* OR multispectral OR hyperspectral OR thermal OR radar OR SAR OR PolSAR OR microwave OR LiDAR OR "laser scanning" OR "point cloud*" OR photogrammetry OR camera* OR "3D sensing"))
```

Development count: **217** (earlier same-query development count: 216). The count is retained as a development workload observation and is not a PRISMA count.

- Primary Seeds: **11/11** retrieved; fixed denominator S-A01–S-A11.
- Challenge Seeds: **2/2** retrieved; S-A12 and S-A13 remain supplementary challenge seeds outside the denominator.
- No primary seed miss was identified.

### Historical challenge closure

Historical Challenge Seeds were checked offline against the complete WOS-A-001 export to test early sensing-route coverage without changing the primary denominator. H-C01 (`The Canopy Spectral Features and Remote Sensing of Wheat Lodging`, 2005, DOI `10.11834/jrs.20050347`) and H-C03 (`Discrimination of lodged rice based on visible/near infrared (VIS/NIR) spectroscopy`, 2009, DOI `10.3724/SP.J.1010.2009.00342`) have verified DOI/title metadata but were not present in the current A export; their WoS indexing status was not independently confirmed. H-C02 (`Wheat lodging monitoring using polarimetric index from RADARSAT-2 data`, 2015, DOI `10.1016/j.jag.2014.08.010`) was present by exact DOI/title match with UT `WOS:000343357500016` and was retrieved by A.

These are **HISTORICAL CHALLENGE SEEDS**, not Primary Development Seeds. H-C01 and H-C03 are retained as historical terminology/coverage references relevant to the future CNKI/language decision if they are not WoS-indexed; their absence from the A export is not a strategy failure without confirmed WoS indexing. No historical coverage failure was identified, no A query amendment was made, and no A-002 was created. The complete check is archived in `01_Seed_Papers\Coverage\Historical_Challenge_Seed_Check.md`.
- Full harvested sensing-term coverage is retained through TS coverage of Title, Abstract, Author Keywords and Keywords Plus. Keywords Plus is reported separately from Author Keywords and is not a controlled vocabulary.
- Development workload is manageable; the additional records relative to WOS-C-001 are not used as an argument that “more is better.” A is preferred for comprehensiveness and sensitivity protection, consistent with the scoping-review objective and JBI-oriented search development.

### Alternative strategy roles

- **WOS-C-001:** precision-oriented diagnostic alternative; current development count 135; Primary Seed Retrieval 11/11; Challenge Retrieval 2/2; no primary miss.
- **WOS-B-001:** proximity diagnostic alternative; current development count 167; Primary Seed Retrieval 11/11; Challenge Retrieval 2/2; no primary miss.

### Developmental Noise QA limitation

The fixed sample was retained without re-sampling (random seed `20260818`, n=50 per candidate). Noise QA is a **supplementary developmental diagnostic only**, not a formal screening or precision estimate. The metadata heuristic produced the following separate proportions:

| Candidate | Clearly relevant | Potentially relevant / uncertain | Clearly irrelevant | Non-clearly-irrelevant proportion |
|---|---:|---:|---:|---:|
| WOS-A-001 | 16/50 | 19/50 | 15/50 | 35/50 = 70.0% |
| WOS-B-001 | 18/50 | 7/50 | 25/50 | 25/50 = 50.0% |
| WOS-C-001 | 17/50 | 23/50 | 10/50 | 40/50 = 80.0% |

The denominator is not a formal relevance label. For example, 40/50 in C means that 40 records were **not automatically classified as clearly irrelevant under the developmental rubric**; it does not mean that 80% of records are formally relevant. Noise classification status is `DEVELOPMENTAL METADATA QA / NOT FORMAL SCREENING / NOT HUMAN-VALIDATED ELIGIBILITY`.

During the targeted human methodological audit, `ESTIMATING SAFETY FACTOR AGAINST ROOT LODGING USING SENTINEL-1 DATA` was corrected to **Clearly relevant for developmental topical relevance** because it concerns wheat lodging susceptibility estimation using Sentinel-1. Final evidence eligibility remains subject to formal screening and publication-type rules; the remaining 149 records were not automatically reclassified as formal eligibility outcomes.

### PRESS and database-role boundary

PRESS-based internal self-audit is `COMPLETED` for the approved protocol candidate: controlled-vocabulary searching is N/A for WoS, Keywords Plus is not controlled vocabulary or Author Keywords, and final year/language/document-type rules are explicitly resolved. Independent PRESS review is `NOT YET COMPLETED`; it is strongly recommended before the formal search where feasible, but is not treated as a mandatory JBI requirement. If not undertaken, that fact will be transparently documented. The prespecified formal database set is WoS Core Collection, IEEE Xplore and CNKI; Scopus is archived as a translation draft but excluded at protocol freeze for access/resource reasons.

## 12. Source selection and Pilot Screening placement

Management/screening software: **Rayyan**, with Blind Mode planned for independent screening. Local audit exports and backups will remain under `D:\水稻小麦倒伏综述_正式版_2026\04_Deduplication_and_Screening`. No Rayyan review was created and no formal records were uploaded in this task.

Stage 2 — Protocol Search Strategy Development included: seed reference identification, search-term harvesting, concept-block development, candidate search-strategy development, seed retrieval validation, developmental noise QA, PRESS-based internal pre-check, database translation drafts, and preparation of the search appendix. **Pilot Screening仍不属于Stage 2。**

The planned source-selection workflow is: **formal database exports → merge records → documented deduplication → upload/import the deduplicated screening set into Rayyan → pilot calibration → independent title/abstract screening → conflict resolution → full-text retrieval → independent full-text screening → conflict resolution → record exclusion reasons → final included corpus**.

For a JBI-concordant scoping-review source-selection process, title/abstract screening and full-text screening are planned to be conducted independently by two or more reviewers, with disagreements resolved by consensus or a third reviewer. Pilot calibration will use 25 randomly selected titles/abstracts: the team independently screens, discrepancies are discussed, eligibility guidance is refined, and at least 75% agreement is required before formal screening. If project resources cannot support two independent reviewers, the protocol must record **POTENTIAL DEVIATION FROM JBI SOURCE-SELECTION METHOD — REQUIRES HUMAN DECISION AND TRANSPARENT REPORTING**; it must not be silently changed to single-reviewer screening.

## 13. Data charting and extraction

`06_Data_Extraction\Data_Extraction_Codebook.xlsx` is the draft charting instrument. It separates Observation from Analysis; Observation source/eligibility fields record whether the sensing requirement is met, while ML/DL, model names and training strategies remain Analysis fields and cannot substitute for observation data.

Before full extraction, the form will be piloted on **2–3 eligible sources**, with at least two team members participating in the pilot charting. After calibration, one reviewer may perform primary extraction with a second human reviewer verifying key fields, unless the team elects duplicate independent extraction. Codex/AI is not a verifying human reviewer. New fields identified during iterative charting will be added through a versioned codebook change, with the date, rationale, affected records and backward-compatibility note recorded in the audit log.

At minimum the chart retains fields aligned with the research questions: bibliographic metadata; crop/subtype; study context; platform; sensor; data modality; spatial/temporal/spectral resolution; lodging target/task; ground truth; label unit; sample size; analysis/algorithm; training design; validation design; metrics; cross-year/site/cultivar validation; external validation; dataset/code/model availability where relevant; limitations; and methodological-robustness variables.

## 14. Critical appraisal / methodological robustness

JBI明确指出范围综述的critical appraisal不是强制要求；本项目批准实施：**Non-exclusionary methodological robustness mapping = YES**。不使用医学式分数机械淘汰研究，而是结构化记录ground-truth method/quality、sample size、label unit、train/test independence、spatial leakage risk、temporal leakage risk、random versus spatial/temporal split、cross-year validation、cross-site/location validation、cross-cultivar validation、external validation、dataset availability、code availability、model availability where relevant和reproducibility information。研究不得仅因robustness mapping结果较弱而被排除。

## 15. Bibliometric analysis

### AMEND-2.2-BIBLIOMETRIC-METHODS — truthful chronology

The bibliometric analytic decisions below were frozen internally during the immediately preceding pre-search round, before the first successful formal WoS query. At the time of that internal freeze, no successful formal WoS or CNKI query, formal IEEE query, formal result count or real included corpus existed. The first formal WoS query was subsequently submitted at 2026-08-20 03:34:42 Asia/Shanghai and produced a valid result-page observation of 217 records. Public incorporation of these already-frozen decisions into Protocol v2.2 occurred afterward because of workflow sequencing. This is a public-versioning timing deviation, not result-driven method selection. Eligibility, WOS-A-001, the database set and screening rules were unaffected.

The operative pre-conduct rules are carried forward exactly from the internal Bibliometric Method Decisions FINAL PRE-CONDUCT record:

1. The primary bibliometric unit is the publication level. Study Family IDs remain mandatory for structured technical synthesis and optional sensitivity/context reporting; primary networks do not collapse publications to Study Families.
2. The primary corpus is the eligible included primary-study publication corpus from the frozen multi-source review process. WoS-only subsets are labelled as source-specific where a field is inherently WoS-specific.
3. Raw source exports remain immutable. Canonical metadata is a harmonized multi-database master with field-level provenance; conflicts are not silently overwritten.
4. Every canonical field retains SourceDatabase, OriginalRecordID, RawFilename and FormalSearchRunID where applicable. Citation counts remain source-specific contextual metadata with retrieval date; counts from different databases are not pooled as equivalent.
5. Citation-discovered records remain a separate provenance layer and enter the primary bibliometric corpus only when they satisfy the frozen eligibility/provenance rules.
6. Publication-level networks are primary. Citation/co-citation networks are document-level and source-specific when justified; no full-corpus network is fabricated when cited-reference fields are inconsistent.
7. Author/institution normalization uses deterministic rules, verified metadata, ORCID only when actually available and manual thesaurus review; fuzzy merges remain candidates until verified.
8. Full counting is used for productivity and primary keyword co-occurrence; fractional counting is used for primary co-authorship where supported; VOSviewer association-strength normalization is used where applicable. Numeric thresholds are data-dependent and recorded after corpus freeze, not tuned to manufacture clusters.
9. The primary thematic network uses author-supplied keywords. Keywords Plus is not silently combined; any WoS Keywords Plus subset is supplementary and labelled. Original and normalized language/concept fields are preserved, with ambiguous translations manually reviewed.
10. bibliometrix/Biblioshiny is used for descriptive analysis/data inspection where appropriate; VOSviewer is used for network mapping. Software versions, parameters, denominator, unit, fields, counting method and thresholds are recorded at execution time. No formal bibliometric analysis has yet been run.

The bibliometric corpus is not yet frozen. These rules do not authorize screening, extraction, Biblioshiny or VOSviewer before their prerequisites are satisfied.
## 16. Structured descriptive technical mapping

技术比较使用Data Extraction Codebook，以context-aware descriptive comparison呈现平台、传感器、观测数据、倒伏任务、ground truth、算法、训练/验证设计、指标、跨年份/地点/品种泛化、开放数据/代码和局限。不同研究的性能数字不做无条件排名，不把异质数据集上的Accuracy差异解释为普遍优劣。

## 17. Results presentation plan

The protocol-stage presentation plan includes:

- a PRISMA-ScR flow diagram;
- a characteristics table for included primary studies;
- a Crop × Platform × Sensor distribution table;
- a lodging task/outcome taxonomy table;
- a ground-truth and label-design characteristics table;
- a training/testing/validation design table;
- a methodological robustness and reproducibility mapping table;
- a technology-evolution timeline figure or table;
- a Platform–Sensor–Task structured map figure or table.

After the final evidence and bibliometric corpora are frozen, bibliometric outputs may include annual production, sources, authors, institutions, countries, collaboration networks, keyword/theme mapping and other pre-specified science-mapping outputs. All performance results will be presented as context-aware descriptive comparisons; no unconditional Accuracy/F1/IoU ranking will be made across heterogeneous datasets.

## 18. Audit, version control, and Stage 2 final gate

- v1.0的Markdown和DOCX已复制到`00_Protocol\Versions`，作为历史版本保留。
- 本次修改逐项写入`10_Audit_Log\Protocol_Change_Log.xlsx`，Approved by统一为Pending user review。
- User-approved decisions in the 2026-08-18 finalization command are recorded in `10_Audit_Log\Decision_Log.xlsx`; corpus membership remains pending, while the v2.2 field-integration rules are frozen and are not silently altered.
- 旧80/220/209/201/85等探索性数字不进入新PRISMA；VOSviewer阈值不预设。

**Stage 2 search-strategy development complete. v2.0 substantive Protocol content FINAL FROZEN; v2.1 and v2.1a prospective administrative amendments were recorded before formal search; AMEND-2.2-BIBLIOMETRIC-METHODS publicly versions analytic rules that were frozen internally before the first formal WoS query but published afterward because of workflow sequencing. Formal WoS WOS-A-001 query/count executed 2026-08-20 03:34:42 with 217 result-page records; RAW export remains pending. No screening, extraction, PRISMA finalization, Biblioshiny or VOSviewer has been performed.** Scopus remains excluded from the prespecified formal set for access/resource reasons; CNKI remains an approved formal source but currently has a security-challenge blocker. HG-01 IEEE terminology verification is closed; HG-02/HG-03 remain open administrative actions.

Protocol v2.2 CURRENT is the operative view. Under AMEND-2.1-REG-TIMING, AMEND-2.1A-PUBLIC-AVAILABILITY and AMEND-2.2-BIBLIOMETRIC-METHODS, the public protocol version and analytic-method chronology must be reported transparently; the first formal WoS result-page observation of 217 is valid, while the RAW export, CNKI and IEEE branches remain pending. Development searches are not formal review searches and are not PRISMA identification counts.

本v2.2完整协议文件为当前操作版本。不得因v2.2公开时序偏差而回溯或作废已观察的217条WoS结果页；不得重新改写WOS-A-001。可继续执行官方WoS RAW导出恢复和其他已授权数据库识别，但在RAW校验、正式筛选与语料库冻结前不得执行筛选、Pilot Screening、最终PRISMA、Biblioshiny或VOSviewer。




