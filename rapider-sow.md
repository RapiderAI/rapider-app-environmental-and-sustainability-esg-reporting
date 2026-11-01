<!-- Rapider Official App SOW & Specification | App #193: Environmental & Sustainability / ESG Reporting (environmental-and-sustainability-esg-reporting) | Domain: IND -->

# #193 Environmental & Sustainability / ESG Reporting (`environmental-and-sustainability-esg-reporting`) — Scope of Work (SOW)

- **App Number & Name:** `#193` — Environmental & Sustainability / ESG Reporting
- **Proposed App Key:** `environmental-and-sustainability-esg-reporting`
- **Suite / Domain Key & Model Prefix:** `IND` (`Ind*`)
- **Category:** `20. Specialized Business & Industry SaaS`
- **Representative Product (`P1`):** Watershed
- **Combined Feature Catalog:** [../combined-features/193-environmental-and-sustainability-esg-reporting-features.md](../combined-features/193-environmental-and-sustainability-esg-reporting-features.md)
- **Target Release Posture:** Audit-Grade GHG Protocol (Scopes 1, 2 & 15 Scope 3 Categories), Multi-Framework Regulatory ESG Disclosure (CSRD/ISSB/CDP/SB 253) & SBTi Decarbonization Microapplication

---

## 1. Executive Outcome & Target Audience

### 1.1 Business Problem Solved
Organizations face binding climate and sustainability mandates—EU CSRD/ESRS, ISSB (IFRS S1 & S2), California SB 253/261, and enterprise customer Scope 3 supply-chain questionnaires—while still relying on error-prone spreadsheets that lack emission-factor provenance, duplicate ERP spend exports, and fail third-party limited/reasonable assurance audits. **Rapider Environmental & Sustainability / ESG Reporting (`environmental-and-sustainability-esg-reporting`)** delivers an audit-grade corporate carbon subledger and multi-framework ESG disclosure engine natively connected to `#194 Energy Consumption & Utility Management`, `accpayable` (`FinSupplierBill`), `expenses` (`ExpExpense`), `assets` (`OpsOperationsAsset`), `vendors` (`OpsSupplierProfile`), and `hrs` (`HrLocation`).

### 1.2 Target Personas & Progressive Disclosure
- **SME Fast-Path Defaults (Operations Managers, Finance Controllers, B2B Suppliers):** Launch an annual carbon footprint in under 15 minutes using Operational Control defaults, pre-loaded EPA/DEFRA/IEA/CEDA emission factors, automatic Scope 1/2 pull from `#194` utility meters, automatic Scope 3 spend mapping from `FinSupplierBill` and `ExpExpense`, and a one-click customer/CDP climate scorecard export.
- **Enterprise Progressive Disclosure (Chief Sustainability Officers, ESG Controllers, Internal Audit, External Assurance Verifiers):** Unlock Equity-Share consolidation across multi-country `FinLegalEntity` trees, Double Materiality Assessments (DMA), market-based Energy Attribute Certificate (EAC/REC/GO/PPA) retirement allocation, hybrid primary-supplier PCF waterfalls across all 15 Scope 3 categories, SBTi Marginal Abatement Cost Curve (`\$/tCO2e`) modeling, and read-only external verifier assurance rooms.

### 1.3 Measurable Business Outcomes
- **100% Calculation Lineage:** Every reported metric ton of $\text{CO}_2\text{e}$ drills down deterministically to a source invoice, meter reading, or survey response plus the exact version-pinned `IndEmissionFactor` and IPCC AR5/AR6 GWP set.
- **>= 70% Reduction in Reporting Prep Time:** Automated Scope 1/2 feeds from `#194` and Scope 3 spend/travel connectors from `accpayable`/`expenses` eliminate manual CSV extracts.
- **Zero Gross/Net Greenwashing Defects:** Enforces GHG Protocol Dual Scope 2 reporting and strict separation of gross emissions from retired voluntary carbon offsets.

### 1.4 Benchmark Summary (`P1`–`P6`)
Synthesizes the *Measure-Report-Act* GHG Protocol rigor, 500k+ CEDA/primary factor waterfalls, and SBTi planning of **`P1` Watershed**, general-ledger-grade carbon accounting and AI spend classification of **`P2` Persefoni**, Double Materiality and ESRS/ISSB multi-framework assurance workflows of **`P3` Workiva ESG**, ERP-native legal-entity Green Ledger integration of **`P4` SAP Sustainability Control Tower**, supplier PCF engagement and EAC allocation of **`P5` Salesforce Net Zero Cloud**, and unified carbon/water/waste ingestion of **`P6` Microsoft Sustainability Manager**.

---

## 2. In-Scope, Out-of-Scope & Suite Ownership Boundaries

### 2.1 In-Scope Capabilities
1. Organizational boundary setup (`OPERATIONAL_CONTROL`, `FINANCIAL_CONTROL`, `EQUITY_SHARE`) and reporting period governance (`IndEsgReportingPeriod`) with base-year restatement controls.
2. Version-pinned emission factor & GWP reference catalog (`IndEmissionFactor`) covering physical activity, grid location/residual-mix, primary supplier PCFs, and inflation-adjusted EEIO spend factors (`kgCO2e / \$1.00`).
3. Automated activity capture (`IndActivityRecord`) and immutable GHG calculation ledger (`IndGhgCalculationEntry`) across Scope 1, dual Scope 2, and all 15 Scope 3 categories.
4. Contractual renewable Energy Attribute Certificate (`IndEnergyAttributeCertificate`) and voluntary removal registry tracking without netting against gross footprints.
5. Quantitative & qualitative non-carbon E, S, and G metric collection (`IndEsgMetricDatapoint`), Double Materiality Assessment (`IndMaterialityTopic`), and multi-framework disclosure mapping (`IndDisclosureRequirement` for CSRD/ESRS, ISSB, GRI, CDP, CA SB 253).
6. Net-zero target tracking and Marginal Abatement Cost Curve (`IndAbatementInitiative`) scenario modeling.

### 2.2 Out-of-Scope Capabilities (Delegated to Adjacent Rapider Apps)
- **Raw utility invoice OCR/auditing, tariff anomaly checks, 15-minute interval smart meters, and ENERGY STAR building benchmarking:** Owned by `#194 Energy Consumption & Utility Management` (`energy-consumption-and-utility-management`), which feeds validated kWh/therms/water consumption into `#193`.
- **Accounts Payable ledger, supplier invoices, and employee travel expense reimbursements:** Owned by `accpayable` (`FinSupplierBill`) and `expenses` (`ExpExpense`).
- **Core HR employee PII, payroll records, and individual safety incident cases:** Owned by `employees`, `payroll`, and `hrs` (`#193` ingests only anonymized/aggregated KPIs).
- **Standalone custom approval inbox:** Strictly prohibited; all controller reviews, gap-estimate approvals, and factor overrides route via Rapider Home `WorkItem`s.

### 2.3 Cross-Suite Ownership & Integration Contract

| Domain / App | Owns (Canonical Models) | Integration Contract with `environmental-and-sustainability-esg-reporting` |
| :--- | :--- | :--- |
| **`#193` (This App — `IND` Suite)** | `IndEsgReportingPeriod`, `IndEmissionFactor`, `IndActivityRecord`, `IndGhgCalculationEntry`, `IndEnergyAttributeCertificate`, `IndEsgMetricDatapoint`, `IndMaterialityTopic`, `IndDisclosureRequirement`, `IndAbatementInitiative` | Owns corporate GHG subledger, emission factors, DMA materiality, ESRS/ISSB disclosures, EAC allocations, and SBTi abatement models. |
| **`#194` Utility Management (`IND`)** | `IndUtilityAccount`, `IndUtilityMeter`, `IndMeterReading`, `IndUtilityBill` | Publishes `ind.utility.period_validated` and `ind.meter.monthly_aggregated`; `#193` consumes electricity, gas, steam, and water totals for Scope 1, Scope 2, and ESRS E3 water metrics. |
| **`acc` & `accpayable` (`FIN` Suite)** | `FinLegalEntity`, `FinSupplierBill`, `FinAccount` | `#193` references `FinLegalEntity.id` for consolidation boundaries and reads posted `FinSupplierBill` lines for Scope 3 Cat 1/2/4 spend-based & hybrid calculations. |
| **`expenses` & `hrs` (`HR` Suite)** | `ExpExpense`, `HrLocation`, `HrEmployee`, `HrCase` | `#193` references `HrLocation.id` for facility attribution, ingests approved `ExpExpense` air/rail/hotel/mileage lines for Scope 3 Cat 6, and reads aggregated workforce ratios for ESRS S1. |
| **`assets`, `maintenance` & `vendors` (`OPS`/`MFG`)** | `OpsOperationsAsset`, `MfgMaintenanceWorkOrder`, `OpsSupplierProfile` | Tracks fleet/equipment fuel & refrigerant top-ups from `OpsOperationsAsset`/`MfgMaintenanceWorkOrder`; links Scope 3 primary PCFs to `OpsSupplierProfile.id`. |
| **`apm` & `surveys` (`APM` / `MKT`)** | `ApmProject`, `MktSurvey` | Links approved `IndAbatementInitiative` execution to `ApmProject.id`; dispatches supplier climate questionnaires via `MktSurvey`. |
| **Rapider Platform Services** | Identity/RBAC, Drive/Files, Home `WorkItem`, `projectChannelMessage` | Stores assurance evidence in Drive, routes sign-offs via `WorkItem`, and hosts grounded ESG AI threads on `projectChannelMessage`. |

---

## 3. Primary Web Pages & Sidebar Navigation Architecture

Every visible sidebar section strictly enforces the **Minimum 3 Items Rule (`>= 3` items per section)**; create/edit drawers and drill-down detail views set `displayOnMenu: false`.

| # | Route | Page Title | Sidebar Section | Menu Visible | Key Components & UX Standards |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | `esg-dashboard` | Climate & ESG Command | `Overview` | `true` (Order 1) | Executive KPI cards (Gross Scope 1, Location/Market Scope 2, Scope 3, Carbon Intensity), SBTi trajectory chart, framework readiness gauges via `findSWR`/`countSWR`. |
| 2 | `ghg-ledger` | GHG Emissions Ledger | `Overview` | `true` (Order 2) | Filterable Scope 1/2/3 ledger (`IndGhgCalculationEntry`) with `#activeFilterTagsBar` + `Clear all`, clickable entry ref to lineage view, icon+text Edit (drafts), icon-only Delete. |
| 3 | `activity-ingestion` | Activity & Spend Feeds | `Overview` | `true` (Order 3) | Sync status & staging queue (`IndActivityRecord`) from `#194` utilities, `FinSupplierBill`, `ExpExpense`, and CSV uploads; outlier badges & unmapped spend filter pills. |
| 4 | `esg-metrics` | E, S & G Metric Hub | `Disclosures & Targets` | `true` (Order 4) | Quantitative/qualitative datapoints (`IndEsgMetricDatapoint`) for Water, Waste, Workforce & Governance with `<rapider-kanban>` status board (`OPEN` -> `SUBMITTED` -> `VERIFIED`). |
| 5 | `disclosure-hub` | CSRD / ISSB Disclosures | `Disclosures & Targets` | `true` (Order 5) | Multi-framework schedule workspace (`IndDisclosureRequirement`) for ESRS, IFRS S1/S2, CDP & SB 253 with Double Materiality filter, evidence counter, and assurance status. |
| 6 | `decarbonization-plan` | Net-Zero & Abatement | `Disclosures & Targets` | `true` (Order 6) | SBTi target burndown, Marginal Abatement Cost Curve (`\$/tCO2e`), and `IndAbatementInitiative` table linked to `ApmProject` execution milestones. |
| 7 | `emission-factors` | Emission Factor Library | `Governance` | `true` (Order 7) | Searchable catalog (`IndEmissionFactor`) across EPA, DEFRA, IEA, CEDA, and approved supplier PCFs with version pinning and GWP (`AR5`/`AR6`) selector. |
| 8 | `eac-certificates` | Renewable EACs & Offsets | `Governance` | `true` (Order 8) | Registry of RECs, Guarantees of Origin, PPAs, and carbon removals (`IndEnergyAttributeCertificate`) with facility allocation meter matching and retirement proof. |
| 9 | `reporting-periods` | Boundaries & Assurance | `Governance` | `true` (Order 9) | `IndEsgReportingPeriod` configuration, `FinLegalEntity` consolidation weights, Double Materiality matrix (`IndMaterialityTopic`), and read-only Auditor Assurance Room toggle. |
| 10 | `ghg-entry-detail` | Calculation Lineage Detail | *(Hidden)* | `false` | Full formula breakdown, input activity unit conversion, pinned `IndEmissionFactor` citation, source invoice/meter link, SHA-256 audit hash, and `#btnGoBack` state restoration. |
| 11 | `disclosure-detail` | Disclosure Requirement View | *(Hidden)* | `false` | ESRS/ISSB requirement text, bound quantitative metrics, citation-grounded AI narrative editor (`projectChannelMessage`), evidence attachments, and `WorkItem` sign-off trigger. |
| 12 | `activity-record-drawer` | Log / Map Activity Drawer | *(Hidden)* | `false` | Sliding drawer to log manual facility activity or map uncategorized `FinSupplierBill` spend lines; auto-closes via `closePageDrawer()`, resets button in `finally`, broadcasts refresh. |

**UI Compliance Mandates:** All primary/danger buttons enforce `!text-white text-white` and `style="color: #ffffff !important;"`; zero native `window.alert`/`confirm`/`prompt` dialogs; no standalone `View` button in table `Actions` columns; supplier/verifier contact phone inputs use `<rapider-phone-input>`.

---

## 4. Canonical Data Models (`Ind*`)

All models omit `projectId`/`tenantId` (multi-tenant isolation is handled by `project-data-manager`), use platform UUIDs (`00000000-xxxx-xxxx-xxxx-xxxxxxxxxxxx` in seed fixtures), and store exact quantities/rates/amounts in `Decimal128`.

| Model Name | Key Fields & Types | Relationships & External Refs | Invariants & Lifecycle |
| :--- | :--- | :--- | :--- |
| **`IndEsgReportingPeriod`** | `code` (`String`), `name` (`String`), `startDate` (`Date`), `endDate` (`Date`), `consolidationApproach` (`Enum`: `OPERATIONAL_CONTROL`, `FINANCIAL_CONTROL`, `EQUITY_SHARE`), `gwpStandard` (`Enum`: `IPCC_AR5`, `IPCC_AR6`), `baseYearPeriodId` (`UUID?`), `revenueDenominatorUsd` (`Decimal128`), `fteDenominator` (`Decimal128`), `status` (`Enum`: `DRAFT`, `DATA_COLLECTION`, `INTERNAL_REVIEW`, `EXTERNAL_ASSURANCE`, `LOCKED_PUBLISHED`), `version` (`Int`) | Scopes `FinLegalEntity[]` with `ownershipPct` (`Decimal128`) and `HrLocation[]`. | Only authorized ESG Admin can transition `EXTERNAL_ASSURANCE` -> `LOCKED_PUBLISHED`; locking freezes all child `IndGhgCalculationEntry` rows. |
| **`IndEmissionFactor`** | `factorCode` (`String`), `sourceAuthority` (`Enum`: `EPA`, `DEFRA`, `IEA`, `EGRID`, `CEDA_EEIO`, `SUPPLIER_PCF`, `CUSTOM`), `releaseYear` (`Int`), `scope` (`Enum`: `SCOPE_1`, `SCOPE_2_LOCATION`, `SCOPE_2_RESIDUAL`, `SCOPE_3`), `scope3Category` (`Int?` `1..15`), `activityUnit` (`String`), `co2Factor` (`Decimal128`), `ch4Factor` (`Decimal128`), `n2oFactor` (`Decimal128`), `totalKgCo2ePerUnit` (`Decimal128`), `regionCode` (`String`), `status` (`Enum`: `DRAFT`, `ACTIVE`, `SUPERSEDED`), `version` (`Int`) | Optional `supplierProfileId` -> `OpsSupplierProfile.id`; Drive `certificateFileId`. | Once referenced by a posted `IndGhgCalculationEntry`, factor rate fields are immutable; updates create a new `version` / `SUPERSEDED` chain. |
| **`IndActivityRecord`** | `referenceNo` (`String`), `reportingPeriodId` (`UUID`), `sourceType` (`Enum`: `UTILITY_APP_194`, `AP_BILL`, `EXPENSE_CLAIM`, `ASSET_FUEL_LOG`, `SUPPLIER_PRIMARY`, `MANUAL_ESTIMATE`), `scope` (`Enum`: `SCOPE_1`, `SCOPE_2`, `SCOPE_3`), `scope3Category` (`Int?`), `activityDate` (`Date`), `rawQuantity` (`Decimal128`), `rawUnit` (`String`), `spendAmountUsd` (`Decimal128?`), `dataQualityScore` (`Decimal128` `1.0..5.0`), `mappingStatus` (`Enum`: `UNMAPPED`, `MAPPED`, `ANOMALY_HOLD`, `CALCULATED`), `version` (`Int`) | `legalEntityId` -> `FinLegalEntity.id`, `locationId` -> `HrLocation.id?`, `externalSourceId` (`IndUtilityBill.id` / `FinSupplierBill.id` / `ExpExpense.id` / `OpsOperationsAsset.id`). | Deduplicated on `(reportingPeriodId, sourceType, externalSourceId)` so re-syncing AP bills or `#194` meters never double-counts activity. |
| **`IndGhgCalculationEntry`** | `entryNumber` (`String`), `reportingPeriodId` (`UUID`), `activityRecordId` (`UUID`), `emissionFactorId` (`UUID`), `calculationMethod` (`Enum`: `SUPPLIER_SPECIFIC`, `PHYSICAL_ACTIVITY`, `HYBRID`, `SPEND_EEIO`), `accountingBasis` (`Enum`: `STANDARD`, `LOCATION_BASED`, `MARKET_BASED`), `normalizedQuantity` (`Decimal128`), `ownershipWeightPct` (`Decimal128`), `grossTonnesCo2e` (`Decimal128`), `formulaTraceJson` (`Object`), `ledgerState` (`Enum`: `PROVISIONAL`, `POSTED`, `REVERSED_BY_RESTATEMENT`), `sha256LineageHash` (`String`), `version` (`Int`) | Links `IndActivityRecord.id`, `IndEmissionFactor.id`, optional `eacAllocationId` -> `IndEnergyAttributeCertificate.id`. | Append-only once `POSTED` or period locked; corrections post a reversing entry + restatement entry preserving full audit trail. |
| **`IndEnergyAttributeCertificate`** | `certificateSerial` (`String`), `instrumentType` (`Enum`: `REC`, `GUARANTEE_OF_ORIGIN`, `I_REC`, `VPPA`, `CARBON_REMOVAL_OFFSET`), `generationTech` (`Enum`: `SOLAR`, `WIND`, `HYDRO`, `GEOTHERMAL`, `BIOCHAR`, `DAC`), `vintageYear` (`Int`), `totalMwhOrTonnes` (`Decimal128`), `allocatedQuantity` (`Decimal128`), `retirementStatus` (`Enum`: `AVAILABLE`, `ALLOCATED`, `RETIRED`), `retirementRegistryUrl` (`String`), `version` (`Int`) | `locationId` -> `HrLocation.id?`, `reportingPeriodId` -> `IndEsgReportingPeriod.id`. | `allocatedQuantity <= totalMwhOrTonnes`; `CARBON_REMOVAL_OFFSET` instruments are strictly blocked from reducing `grossTonnesCo2e` in Scope 1/2/3 totals. |
| **`IndEsgMetricDatapoint`** | `metricCode` (`String`, e.g., `ESRS-E3-WATER-WITHDRAWAL`, `ESRS-S1-TURNOVER`), `pillar` (`Enum`: `ENVIRONMENTAL`, `SOCIAL`, `GOVERNANCE`), `reportingPeriodId` (`UUID`), `numericValue` (`Decimal128?`), `unit` (`String?`), `narrativeValue` (`String?`), `status` (`Enum`: `OPEN`, `SUBMITTED`, `VERIFIED`, `LOCKED`), `version` (`Int`) | `ownerUserId` -> Platform User, `locationId` -> `HrLocation.id?`, Drive `evidenceFileIds[]`. | Transition to `VERIFIED` requires at least one source connector trace or attached evidence document. |
| **`IndMaterialityTopic`** | `topicCode` (`String`), `esrsStandard` (`String`, e.g., `E1`, `E2`, `S1`, `G1`), `topicTitle` (`String`), `impactMaterialityScore` (`Decimal128` `0..5`), `financialMaterialityScore` (`Decimal128` `0..5`), `isMaterial` (`Boolean`), `rationale` (`String`), `stakeholderSummary` (`String`), `version` (`Int`) | `reportingPeriodId` -> `IndEsgReportingPeriod.id`. | Topics exceeding configured materiality threshold (`>= 3.0` on either axis) automatically mark linked `IndDisclosureRequirement` records as `MANDATORY`. |
| **`IndDisclosureRequirement`** | `framework` (`Enum`: `CSRD_ESRS`, `ISSB_IFRS_S1_S2`, `GRI`, `CDP`, `CA_SB253`), `disclosureCode` (`String`, e.g., `ESRS E1-6`, `IFRS S2.29`), `title` (`String`), `reportingPeriodId` (`UUID`), `applicability` (`Enum`: `MANDATORY`, `VOLUNTARY`, `NOT_MATERIAL`), `draftNarrativeMd` (`String`), `xbrlTaxonomyTag` (`String`), `assuranceStatus` (`Enum`: `IN_PROGRESS`, `CONTROLLER_REVIEW`, `ASSURANCE_READY`, `ASSURED`), `version` (`Int`) | Binds `metricDatapointIds[]` and Scope totals from `IndGhgCalculationEntry`; `reviewerWorkItemId` -> Home `WorkItem`. | Cannot reach `ASSURANCE_READY` while any bound `IndEsgMetricDatapoint` or GHG scope calculation remains `UNMAPPED` or `ANOMALY_HOLD`. |
| **`IndAbatementInitiative`** | `code` (`String`), `title` (`String`), `targetScope` (`Enum`: `SCOPE_1`, `SCOPE_2`, `SCOPE_3`), `leverCategory` (`Enum`: `RENEWABLE_PPA`, `FLEET_EV`, `HVAC_ELECTRIFICATION`, `SUPPLIER_ENGAGEMENT`, `PROCESS_EFFICIENCY`), `estimatedAnnualAbatementTonnes` (`Decimal128`), `capexUsd` (`Decimal128`), `annualOpexDeltaUsd` (`Decimal128`), `marginalAbatementCostPerTonne` (`Decimal128`), `status` (`Enum`: `IDEATION`, `APPROVED`, `IN_EXECUTION`, `REALIZED`), `version` (`Int`) | `locationId` -> `HrLocation.id?`, `apmProjectId` -> `ApmProject.id?`, `supplierProfileId` -> `OpsSupplierProfile.id?`. | Deterministically computes `marginalAbatementCostPerTonne` (`\$/tCO2e`) using `Decimal128` net lifetime cost divided by lifetime abated tonnes. |

---

## 5. Core End-to-End User Journeys

### Journey 1: SME Fast-Path Annual Carbon Footprint (Under 15 Minutes)
1. Sustainability Coordinator opens `reporting-periods`, creates `FY2026` with default `OPERATIONAL_CONTROL` and `IPCC_AR6`, and selects active `FinLegalEntity` and `HrLocation` records.
2. Navigates to `activity-ingestion` and clicks **Sync Rapider Sources**: `#193` ingests validated electricity/gas bills from `#194`, `FinSupplierBill` spend lines from `accpayable`, and `ExpExpense` flight/hotel records from `expenses`.
3. Engine auto-matches regional EPA/IEA grid factors and CEDA EEIO spend factors (`kgCO2e / \$1.00`), generating `IndGhgCalculationEntry` rows for Scope 1, dual Scope 2, and Scope 3.
4. Coordinator opens `esg-dashboard` to review gross footprints and exports a customer-ready CDP/SME Carbon Scorecard PDF.

### Journey 2: Market-Based Scope 2 REC Allocation & Dual Reporting
1. Energy & ESG Manager navigates to `eac-certificates` and registers a `2,500 MWh` Wind REC bundle (`IndEnergyAttributeCertificate`) with registry serial numbers for the Austin plant (`HrLocation`).
2. Allocates the REC bundle against Austin's `FY2026` electricity `IndActivityRecord` rows imported from `#194`.
3. Engine recalculates dual Scope 2 entries in `ghg-ledger`: `LOCATION_BASED` continues using eGRID ERCOT average factor, while `MARKET_BASED` applies `0.000 tCO2e/MWh` to covered load and ERCOT residual-mix factor to uncovered MWh.

### Journey 3: Outlier Hold & Scope 3 Primary Supplier PCF Upgrade via Home `WorkItem`
1. During monthly `FinSupplierBill` sync, a `\$480,000` steel procurement invoice triggers an `ANOMALY_HOLD` because the vendor (`OpsSupplierProfile`) belongs to a high-emission pareto tier with an unverified primary PCF submission.
2. `#193` creates a Rapider Home `WorkItem` assigned to the Sustainable Procurement Lead linking directly to the supplier's attached ISO 14067 PCF certificate.
3. Lead reviews the certificate, approves the `SUPPLIER_PCF` `IndEmissionFactor`, and resolves the `WorkItem`; `#193` upgrades the `IndGhgCalculationEntry` from `SPEND_EEIO` (`DQI 4.0`) to `SUPPLIER_SPECIFIC` (`DQI 1.5`) with full audit trail.

### Journey 4: CSRD / ISSB Multi-Framework Disclosure & External Assurance Verification
1. ESG Controller runs Double Materiality scoring in `reporting-periods` (`IndMaterialityTopic`), marking `ESRS E1 Climate Change` and `ESRS E3 Water` as `MANDATORY`.
2. In `disclosure-hub`, Controller clicks into `ESRS E1-6 Gross Scopes 1, 2, 3` (`disclosure-detail`), uses grounded AI in `projectChannelMessage` to draft methodology notes citing locked `IndGhgCalculationEntry` totals, and triggers Controller Sign-Off (`WorkItem`).
3. External Assurance Verifier logs in with `EsgExternalAuditor` read-only access, filters `ghg-ledger` via `#activeFilterTagsBar`, clicks an entry identifier to `ghg-entry-detail`, inspects the SHA-256 lineage hash and source `#194` utility bill PDF, and clicks `#btnGoBack`—returning to `ghg-ledger` with active Scope/Location filter tags intact.

### Journey 5: SBTi Target Modeling & Abatement Handoff to `APM`
1. CSO opens `decarbonization-plan`, sets a `-42%` near-term Scope 1+2 SBTi target against the base year, and creates three `IndAbatementInitiative` proposals (Rooftop Solar PPA, Chiller Electrification, Top-20 Supplier Engagement).
2. Reviews the MACC chart (`\$/tCO2e`), approves Rooftop Solar PPA (`-\$18.50/tCO2e` net savings), and clicks **Launch Execution Project**, creating a linked `ApmProject` in `apm` via guarded cross-app command.

---

## 6. Consolidated Feature Priorities & Work Packages

### 6.1 `P0` Foundation Work Packages (Must-Ship Core)
- **WP-P0-1 (Boundaries & Factor Engine — `ESG-001`, `ESG-002`, `ESG-003`):** `IndEsgReportingPeriod` lifecycle, `FinLegalEntity`/`HrLocation` boundary mapping, and versioned `IndEmissionFactor` library (`Decimal128`).
- **WP-P0-2 (Automated Ingestion & GHG Subledger — `ESG-005`, `ESG-006`, `ESG-007`, `ESG-008`, `ESG-009`):** Deduplicated connectors to `#194` utility bills/meters, `FinSupplierBill`, `ExpExpense`, and `OpsOperationsAsset` fuel/refrigerants; Scope 1, dual Scope 2, and 15-category Scope 3 calculation engine with immutable lineage hashes.
- **WP-P0-3 (Core E/S/G Metrics, Multi-Framework Hub & Command Dashboard — `ESG-012`, `ESG-013`, `ESG-016`, `ESG-017`, `ESG-021`, `ESG-025`):** Water/waste metric capture, CSRD/ISSB/GRI/CDP/SB 253 requirement mapping, `WorkItem` sign-off gates, SBTi baseline tracking, and SWR executive dashboard.

### 6.2 `P1` Scale & Enterprise Governance Work Packages
- **WP-P1-1 (Market Instruments, Custom PCFs & Anomaly Triage — `ESG-004`, `ESG-010`, `ESG-011`):** Supplier PCF factor approval workflow, EAC/REC/GO allocation & retirement tracking, and statistical gap/outlier `WorkItem` routing.
- **WP-P1-2 (HR/Governance Aggregations, Double Materiality & Auditor Portal — `ESG-014`, `ESG-015`, `ESG-018`, `ESG-019`):** Privacy-safe `HR` KPI rollups, ESRS Double Materiality matrix, and scoped read-only `EsgExternalAuditor` assurance workspace.
- **WP-P1-3 (MACC Scenarios & Supplier Campaigns — `ESG-022`, `ESG-023`):** Marginal Abatement Cost Curve calculator linked to `ApmProject` and pareto Scope 3 supplier survey dispatch via `MktSurvey`.

### 6.3 `P2` Adjacent & Grounded AI Work Packages
- **WP-P2-1 (Taxonomy Export & Removal Registry — `ESG-020`, `ESG-024`):** ESRS iXBRL/JSON assurance binder export and non-netted voluntary carbon removal registry.
- **WP-P2-2 (Grounded Sustainability Co-Pilot — `ESG-026`, `ESG-027`, `ESG-028`):** `projectChannelMessage` AI spend-to-factor recommender, YoY structural/operational variance decomposition, and citation-backed ESRS/ISSB narrative drafter.

---

## 7. Roles, Permissions & Field-Level Governance

| Role | Permitted Actions | Restricted / Field-Level Boundaries |
| :--- | :--- | :--- |
| **`EsgAdmin` (CSO / ESG Controller)** | Configure `IndEsgReportingPeriod` boundaries, approve custom `IndEmissionFactor`s, retire `IndEnergyAttributeCertificate`s, approve `WorkItem` sign-offs, lock/publish periods, restate base years. | Cannot directly mutate `POSTED` `IndGhgCalculationEntry` rows without generating a formal restatement reversal pair; cannot view individual `HR` salaries. |
| **`SustainabilityAnalyst`** | Sync connectors, map `IndActivityRecord` rows, run provisional GHG calculations, manage `IndAbatementInitiative` models, draft `IndDisclosureRequirement` narratives. | Cannot transition period to `LOCKED_PUBLISHED` or self-approve custom emission factors they authored (segregation of duties). |
| **`FacilityContributor`** | Submit facility activity/water/waste `IndActivityRecord` and `IndEsgMetricDatapoint` records and upload supporting evidence for assigned `HrLocation`s. | Scoped strictly to assigned `HrLocation`s; cannot view global AP supplier spend or enterprise-wide financial denominators. |
| **`EsgExternalAuditor` (Assurance Verifier)** | Read-only inspection of `EXTERNAL_ASSURANCE` / `LOCKED_PUBLISHED` periods, full calculation lineage (`ghg-entry-detail`), factor versions, and evidence files; post verification status notes. | Strictly zero write/edit/delete permissions on activity, factors, metrics, or ERP source ledgers. |

---

## 8. Technical APIs, Guarded Commands, Events & `requiredWorkflows`

### 8.1 Guarded Domain Commands
All state-mutating commands require `idempotencyKey`, `correlationId`, and optimistic `expectedVersion`:
- `ind.esg.syncSourceActivities` — Pulls incremental records from `#194`, `FinSupplierBill`, `ExpExpense`, and `OpsOperationsAsset` idempotently.
- `ind.esg.calculatePeriodFootprint` — Evaluates mapped `IndActivityRecord` rows against pinned `IndEmissionFactor` versions and writes `IndGhgCalculationEntry` rows with SHA-256 lineage hashes.
- `ind.esg.allocateEnergyCertificate` — Binds `IndEnergyAttributeCertificate` MWh to facility electricity records and recomputes Market-Based Scope 2.
- `ind.esg.submitDisclosureForReview` — Validates zero unmapped/anomaly blockers and opens a Rapider Home `WorkItem` for controller sign-off.
- `ind.esg.lockReportingPeriod` — Freezes period calculations, snapshots XBRL/assurance hash, and blocks further provisional edits.

### 8.2 Domain Events Published & Consumed (Kafka)
- **Published:** `ind.esg.period_locked`, `ind.esg.footprint_calculated`, `ind.esg.anomaly_detected`, `ind.esg.disclosure_assured`, `ind.esg.abatement_approved`.
- **Consumed:** `ind.utility.bill_approved` & `ind.meter.monthly_closed` (from `#194`), `fin.supplier_bill.posted` (from `accpayable`), `hr.expense.approved` (from `expenses`), `mfg.work_order.completed` (refrigerant logs from `maintenance`).

### 8.3 `requiredWorkflows` (`app.manifest.json`)
- `esgSourceIngestionAndDedupeWorkflow`: Scheduled/event-driven OpenWhisk pipeline ingesting `#194`, `FIN`, and `HR` feeds with currency normalization and anomaly detection.
- `esgAssuranceSignOffWorkflow`: Orchestrates multi-stage metric owner -> ESG controller sign-off via Rapider Home `WorkItem`s.
- `esgSupplierPcfCampaignWorkflow`: Dispatches Scope 3 data collection surveys via `MktSurvey` and routes returned PCF certificates for analyst verification.

### 8.4 Grounded Rapider AI Rules
AI assistants operating in `projectChannelMessage` threads **MUST** cite exact `IndGhgCalculationEntry.id`, `IndEmissionFactor.factorCode`, and `IndEsgMetricDatapoint.metricCode` records, enforce caller RBAC (`FacilityContributor` location scoping), **NEVER** invent emission factors or hallucinate quantitative disclosures, and require explicit human click-confirmation before applying spend-to-factor mappings or saving disclosure text.

---

## 9. Security, Privacy, Compliance & Non-Functional Requirements

- **Regulatory & Assurance Rigor (CSRD / ISSB / ISAE 3000 & 3410):** Full SHA-256 lineage hashing, segregation of duties between preparer and approver, immutable factor versioning, and 10-year audit retention for SEC/EU CSRD statutory lookbacks.
- **GDPR & Workforce Privacy Isolation:** Social metrics (`ESRS S1` pay equity, turnover, diversity) ingest only pre-aggregated statistical ratios (`count >= 5` anonymity threshold) from `HR`—never storing individual employee compensation, health, or demographic PII inside `Ind*` tables.
- **Precision & Currency Integrity:** All $\text{CO}_2\text{e}$ calculations, GWP multipliers, ownership percentages, and `\$` financial intensities use `Decimal128` with deterministic rounding only at final presentation layer.
- **Accessibility & Responsive UX:** WCAG 2.2 AA contrast (including `#ffffff !important` text on primary/danger buttons), full keyboard navigation across tables/drawers/kanban, and responsive layouts verified at `390px`, `768px`, and `1440px`.

---

## 10. Deterministic Acceptance Criteria

1. **Zero Duplicate Activity Ingestion:** Re-running `ind.esg.syncSourceActivities` for the same reporting period and `FinSupplierBill` / `#194` `IndUtilityBill` batch produces zero duplicate `IndActivityRecord` rows.
2. **Dual Scope 2 Mandatory Output:** Every electricity `IndActivityRecord` produces both a `LOCATION_BASED` and a `MARKET_BASED` `IndGhgCalculationEntry`, and allocating an `IndEnergyAttributeCertificate` updates `MARKET_BASED` $\text{tCO}_2\text{e}$ while leaving `LOCATION_BASED` unchanged.
3. **Non-Netting Carbon Offset Invariant:** Retiring a `CARBON_REMOVAL_OFFSET` instrument records neutralization volume separately and never subtracts from gross Scope 1, Scope 2, or Scope 3 `grossTonnesCo2e` totals.
4. **Equity-Share Consolidation Precision:** Setting a `FinLegalEntity` to `49.50%` ownership under `EQUITY_SHARE` multiplies facility gross emissions by `0.4950` using `Decimal128` without floating-point rounding drift.
5. **Immutable Locked Period & Factors:** Attempting to edit an `IndEmissionFactor` rate or `IndGhgCalculationEntry` inside a `LOCKED_PUBLISHED` period is rejected unless executed via a formal restatement command that preserves the original row.
6. **Double Materiality Auto-Scoping:** Saving an `IndMaterialityTopic` with `impactMaterialityScore >= 3.0` automatically switches linked ESRS `IndDisclosureRequirement` rows to `MANDATORY`.
7. **Home `WorkItem` Governance Gate:** Submitting a disclosure for controller approval creates a canonical Rapider Home `WorkItem` and blocks transition to `ASSURANCE_READY` if any underlying activity is `UNMAPPED` or `ANOMALY_HOLD`.
8. **External Auditor Read-Only Enforcement:** A user with `EsgExternalAuditor` role can inspect `ghg-entry-detail` lineage and source bills but receives `403 Forbidden` on every create, update, or delete endpoint and sees zero mutation buttons in the UI.
9. **Sidebar Minimum-3-Items Compliance:** `app.manifest.json` renders exactly three visible sidebar sections (`Overview`, `Disclosures & Targets`, `Governance`), each containing `>= 3` visible items, while detail and drawer routes set `displayOnMenu: false`.
10. **SWR Clean Query & Optimistic UI Compliance:** All initial page loads use `findSWR`/`countSWR` with zero `isDeleted` `where` filters; editing or deleting a draft `IndActivityRecord` updates the table optimistically, clears `swr_*` cache keys, and rolls back on simulated error.
11. **Active Filter Tags & Clear All:** Typing a search query or selecting a Scope/Status pill on `ghg-ledger` renders `#activeFilterTagsBar` with HTML-escaped dismissible chips and `[Clear all]`, synchronously filtering the dataset and restoring full data upon clearing.
12. **Drawer Auto-Close & `finally` Button Reset:** Submitting or cancelling `activity-record-drawer` invokes `closePageDrawer()`, resets the Save button inside a `finally` block, and broadcasts `RECORD_CREATED`/`RECORD_UPDATED` to refresh `activity-ingestion`.
13. **Real Click-Through Navigation & State Restoration:** Physically clicking an entry identifier in `ghg-ledger` navigates to `#/ghg-entry-detail?id=...` without `<base href>` 404 diversion, renders calculation lineage, and clicking `#btnGoBack` restores `ghg-ledger` with prior filters preserved.
