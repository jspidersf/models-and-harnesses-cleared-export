# Research Packet: Sustainable Blue-Green AI Future — Full Source Documents

- **Template version:** 2026-08-05
- **Status:** CLEARED FOR PUBLIC DISCLOSURE
- **Direction:** personal → work
- **Clearance date:** 2026-08-16
- **Cleared by:** Jeremy Pollock
- **Research period covered:** 2015 through 2026-08-16
- **Last verified:** mixed; transmission correction verified 2026-08-16, document-level verification logs and source dates preserved below
- **Originating private repository or repositories:** `jspidersf/models-and-harnesses`
- **Safe source paths:** `CCSF-compute/CCSF_SFPUC_power_water_deep_dive.md`; `CCSF-compute/CCSF_humboldt_offshore_wind_transmission.md`
- **Source commits:** source snapshot `d212edaeb54d7179574d0b518b33917c8c4a2c89`; both source documents last changed at `b5eed4deb51e8997e91f1d77be56259739bad560`
- **Intended destination repository or repositories:** `jp-sfgov/sfgov-models-and-harnesses`; `jp-sfgov/sfgov-ccsf-compute`
- **Destination canonical document roles:** source base for a personal speculative public-post outline; CCSF energy/water evidence library; correction-aware engineering and transmission references
- **Transfer form:** graduated document
- **Baseline content identity:** not applicable
- **Expected result identity:** not applicable

## Purpose and context

This packet transfers two complete personal-research documents that together cover the three long-horizon threads in Jeremy's speculative “sustainable blue-green AI future” vision: reclaimed or recycled water for data-center cooling; solar, small hydro, and storage on public or City-owned land; and offshore wind with resilient transmission to the Bay Area. Compute is treated as a flexible beneficiary of the clean-power buildout, not an anchor or justification for it.

The documents are included in full rather than summarized. Their correction history, conflicting figures, caveats, source lists, and superseded reasoning remain visible so the receiving side can integrate them without reconstructing the research from private files. This packet is personal, unchartered analysis. It is not CCSF or SFPUC work product and does not authorize a project, site, procurement, engagement, public post, or capital decision.

The related nine-point “recovered public-post spine” is already present in the personal export's `Packets/ccsf-compute-initial-brainstorm-direct-sync-2026-08-05.md`. It is not duplicated here. The August 11 carbon/grid/community evidence delta is already present in `Packets/ccsf-compute-carbon-grid-and-community-impacts-2026-08-16.md`.

## Research scope and method

The SFPUC deep dive examined public utility, regulatory, engineering, procurement, land, water-treatment, cooling, renewable-generation, and siting sources. It compared the 2015 LAFCo/EnerNex local-buildout concepts with their observed status through 2026 and carried forward unresolved verification questions rather than treating proposals as operating assets.

The Humboldt document examined lease capacity, CAISO transmission planning, offshore-wind timing, rate and grid context, procurement structure, and the scale relationship between compute and regional energy infrastructure. Its August 16 correction separates CAISO's approved overland delivery plan from Schatz Energy Research Center's distinct pre-feasibility subsea-cable concept.

No new external research was added in preparing this packet. Existing source citations and verification logs are preserved verbatim. Claims whose source dates are old or whose current status remains unresolved are not silently refreshed.

Shared-copy transformations are limited to the approved disclosure boundary:

- Named Department of Technology staff were removed from the SFPUC shared copy while the “not chartered or tasked” disclaimer was retained.
- The SFPUC author-context line was clarified as personal, unchartered analysis rather than departmental work product.
- The Humboldt author-context line was clarified on the same basis.
- Existing visible strikethrough and correction history, including retired GovAI Coalition / Khaled Tawfik material, was preserved rather than deleted.

## Findings

### Complete document 1 of 2: SFPUC power and water integration

The complete shared copy begins after the delimiter below. It covers reclaimed-water cooling architecture; Title 22 treatment constraints; public-land solar and storage; small-hydro claims and unresolved status; Hetch Hetchy and CleanPowerSF supply paths; Raker Act constraints; siting; economics; and the corrected Humboldt transmission section.

<!-- BEGIN FULL DOCUMENT: CCSF_SFPUC_power_water_deep_dive.md -->
# CCSF SFPUC Power and Water Integration — Deep Dive

**Date:** May 15, 2026
**Author context (shared copy):** Personal, unchartered analysis by Jeremy Pollock, prepared as the engineering-and-procurement appendix to `CCSF_public_compute_strategic_brief.md`; not CCSF or SFPUC work product.
**Document purpose:** Comprehensive reference on the engineering, regulatory, and procurement dimensions of integrating a CCSF public AI compute facility with SFPUC water, power, and wastewater infrastructure. Built as a queryable source for NotebookLM and as a hand-off document for any SFPUC Power Enterprise or third-party engineering engagement.

---

## 1. Purpose and scope

The main strategic brief carries the policy case, governance, and external positioning at a level appropriate for the CIO and Director of Emerging Technology. This document holds the technical and institutional detail at the level appropriate for SFPUC Power Enterprise staff, SFPUC engineering, and any retained feasibility consultant.

**In scope:** the Hetch Hetchy hydroelectric system, the Hetch Hetchy Power Enterprise as service provider, CleanPowerSF as a procurement vehicle, the Southeast Water Pollution Control Plant as a candidate cooling-water source, the SSIP capital trajectory, the Raker Act, the 2015 LAFCo/EnerNex local buildout vision and its actual disposition over the past decade, the August 10, 2026 CleanPowerSF Integrated Resource Plan filing as the planning window, and the three candidate siting configurations.

**Out of scope:** detailed CEQA analysis, geotechnical assessment, specific PPA contract negotiation, and the legal opinion the City Attorney will need to issue on JPA formation and Raker Act application.

> [!warning] Corrections from Jeremy, 2026-06-20 — read before relying on this deep-dive
> - **Not a chartered project.** This is Jeremy's own analysis, not CCSF/SFPUC work product. Preliminary conversations occurred; none of it was chartered or tasked. **[Shared-copy transform, 2026-08-16: named Department of Technology staff removed.]**
> - **SFPUC/CleanPowerSF IRP engagement (§2.3, §10, §11) is a long-term process and will not happen in time for the August 10, 2026 IRP filing.** SFPUC is institutionally conservative; that filing window is effectively closed for this project. Treat §10's "highest-leverage window" framing as superseded.
> - **The Humboldt anchor-offtaker framing (§9.5.5) is retired** — wildly out of scale for CCSF's compute load. See companion brief §7.6 for the corrected framing.
> - **The GovAI Coalition Summit / Khaled Tawfik reference (§9.5.5, §11) is an AI-generated suggestion**, not evaluated or adopted by Jeremy.

---

## 2. SFPUC system overview

### 2.1 Hetch Hetchy hydroelectric system

Approximately 385 MW nameplate capacity across three powerhouses in Tuolumne County: Holm (169 MW), Kirkwood (124 MW), Moccasin (110 MW). Add ~4 MW Moccasin Low-Head, ~8 MW in-City solar PV at SFPUC facilities, and ~2 MW biomass cogeneration at the Southeast Water Pollution Control Plant. The system is highly correlated with Tuolumne snowpack: long-run average annual generation ~1,574 GWh (1970-2014), but California hydro fell ~48 percent in 2021 versus normal. Multi-year droughts in 2012-2016 and 2020-2022 cut output materially. SFPUC was net-short in dry years and purchased market power to cover obligations. The system is energy-limited and largely committed.

The Moccasin Powerhouse Generator Rehabilitation (2018-2025) extended rotor and stator life; it returned to service in November 2025 with no capacity expansion. The Moccasin Penstock replacement at approximately $285 million is the single largest item in the FY26-35 capital plan, providing a 75-100 year life extension. The capital plan is asset preservation, not capacity growth.

Hetch Hetchy large hydro is *not* RPS-eligible for California Renewable Portfolio Standard purposes (it exceeds the 30 MW threshold and the system was constructed before the eligibility window). The 4 MW Moccasin Low-Head plant *is* RPS-eligible.

### 2.2 Hetch Hetchy Power Enterprise (HHP)

HHP is the SFPUC enterprise that serves municipal load. Distinct from CleanPowerSF. Serves Muni, SFO, SF General Hospital, City College, libraries, museums, ~25,000 streetlights, SFUSD schools, Port, City buildings, plus expanding retail to Treasure Island, Hunters Point, and Mission Rock. Approximately 150 MW of retail load across ~6,300 accounts.

HHP rates are the lowest in the system — likely $40-60/MWh for municipal enterprise customers versus ~$70-80/MWh for CleanPowerSF Green. **A new CCSF data center is structurally eligible for HHP service as a municipal load.** Constraint: HHP is energy-limited and largely committed to existing customers. A 4 MW DC (~35 GWh/year) is absorbable. A 40 MW DC (~350 GWh/year, 20-25 percent of average HHP generation) would stress the portfolio in dry years and require new supply layered on top.

The 2023 HHP Integrated Resource Plan explicitly forecasts **no significant additional renewable procurement until 2033**, when additional supply is forecasted as needed to meet load growth and reliability obligations.

### 2.3 CleanPowerSF (CPSF)

SF's Community Choice Aggregation program. Approximately 385,000 accounts, 500+ MW retail load. Reached 100 percent renewable to all customers two years ahead of schedule (target was 2030; achieved 2024). 490 MW contracted solar/wind/geothermal plus ~290 MW battery storage. Green default tier is >90 percent clean; SuperGreen is 100 percent California-certified at a small premium (~$7/month for small businesses). No rate increase for 98 percent of customers in FY25-26.

CleanPowerSF files an Integrated Resource Plan with the CPUC every 2-3 years. The next IRP is due **August 10, 2026**. The 2025 "Powering Tomorrow, Together" outreach was the precursor and remains inputs-open as of this drafting. **Correction (2026-06-20): this window will not be used for this project.** SFPUC engagement is long-term and gated on the project maturing well past its current informal stage; SFPUC's process is conservative and cautious by design. The realistic planning horizon is a future IRP cycle.

### 2.4 Central Valley solar + storage portfolio (contracted)

Since 2015, CleanPowerSF has added approximately 800 MW of new solar/wind/geothermal and 300 MW of storage. Virtually all of it is sited in the Central Valley or further south, contracted through long-term PPAs:

- **Paulsell Energy Center** (NextEra, Stanislaus County): 20 MW solar + 15 MW BESS, COD July 2024.
- **Crow Creek Energy Center** (NextEra, Stanislaus County): 20 MW solar / 60 MWh BESS to CPSF.
- **Blythe IV** (NextEra): 62 MW solar plus new BESS amendment, $220 million over 20 years.
- **Darden** (Fresno): 71 MW solar + 71 MW BESS.
- **IP Easley** (Riverside): 50 MW share of 400 MW project.
- **Corby** (Solano County): 300 MW standalone BESS.

The pattern is clear: contracts in the Central Valley, not owned generation on SFPUC land.

### 2.5 California Community Power (CC Power) JPA

CleanPowerSF is a member of California Community Power, an 8+ CCA Joint Powers Authority. CC Power conducts joint procurement on behalf of member CCAs at scale that no single CCA could achieve alone. Active joint solicitations include 200 MW firm clean, 500 MW long-duration energy storage, and a Geothermal Strategic Initiative RFI issued May 2025.

**This is the operational precedent for the multi-government compute JPA the strategic brief proposes.** Same structural pattern (multi-government joint procurement of capacity through a JPA), same legal vehicle type (California JPA under Gov Code §6500), same opt-in-per-procurement governance. SFPUC has lived inside this governance model since CleanPowerSF joined CC Power. Whoever at SFPUC negotiated the CC Power membership is a useful internal precedent contact for the CCSF compute consortium structuring conversation.

### 2.6 Aqueduct right-of-way

SFPUC owns substantial right-of-way from Early Intake through Moccasin to Oakdale, Tesla, Sunol, and Newark — hundreds of miles of corridor. California has approximately 13 GW of theoretical canal-solar capacity statewide (Project Nexus context).

**Important correction to prior analysis:** the Hetch Hetchy water system is mostly tunnels and buried pipe between Sierra Nevada and the Bay Area. The canopy-over-canal model that works on the Turlock Irrigation District canals (Project Nexus, with UC Merced) does not transfer cleanly to the Hetch Hetchy geometry. The aqueduct ROW solar opportunity for SFPUC is at substation/parcel scale (Sunol Valley, Warnerville-adjacent, Tesla Portal, Pulgas), not canopy-over-canal scale. Replace the Project Nexus analogy with parcel solar framing.

### 2.7 Southeast Water Pollution Control Plant (SEP)

Located at 750 Phelps Street, approximately 0.5 mile from the candidate Digital Realty / 200 Paul Ave data center site. Hydraulic peak capacity 250 MGD (new headworks placed in service summer 2024). Average dry-weather flow ~60 MGD. Handles approximately 80 percent of SF's combined sewer and wastewater. Currently produces **disinfected secondary effluent** via high-purity oxygen activated sludge plus chlorination/dechlorination — **not Title 22 disinfected tertiary** as required for evaporative cooling tower service under California Code of Regulations Title 22 §60306.

The plant discharges to central San Francisco Bay under NPDES Order R2-2024-0013. It already reuses filtered/UV-disinfected effluent for in-plant process water — a directly relevant precedent for what would be required to serve a data center cooling load.

### 2.8 Sewer System Improvement Program (SSIP) trajectory

Total program ~$5+ billion. Key components relevant to the data center cooling question:

- **New Headworks Facility** (250 MGD): substantially complete, in service summer 2024.
- **Biosolids Digester Facilities Project**: ~80 percent construction complete early 2026; substantial completion 2027.
- **Nutrient Reduction Project** (~$1.47 billion): adds biological nitrogen removal targeting ~80 percent N reduction. **Described as "tertiary-grade" for nutrients but not full Title 22 tertiary** unless coupled with filtration plus UV disinfection.
- **No existing eastside recycled water distribution main** near 200 Paul Ave today. The Westside Enhanced Water Recycling Project (Oceanside, MF/RO/UV, 2 MGD avg, 4 MGD peak) is the active SF recycled-water capital project but is ~9 miles from 200 Paul and serves Golden Gate Park.

---

## 3. The 2015 LAFCo Local Buildout vision

In January 2015 SF LAFCo released "Local Build-out of Energy Resources of the Community Choice Aggregation Program," prepared by EnerNex and Willdan. The report identified a portfolio of in-City and regional renewable sites on SFPUC or City-controlled land totaling approximately 47.7 MW local/regional plus 29.8 MW at the Warnerville Substation in Stanislaus County, for a combined 77.5 MW average buildout potential at ~$453 million average capital cost.

Eight specific solar sites were modeled with LCOE and capital cost ranges from three independent estimators (LPI, SFPUC, Black & Veatch):

| Site | Avg MW | Avg Cap ($M, 2015) | LCOE ($/MWh, 2015) | Notes |
|---|---|---|---|---|
| Sunol Valley | 17.5 | $85 | $80-169 | Lowest local LCOE; 100-acre City-owned site on aqueduct corridor; recommended for RFP |
| Warnerville Substation | 29.8 | $173 | $113-169 | Largest single site; co-located with Hetch Hetchy 230kV switchyard; "subject to land acquisition" |
| Hunters Point Parcel E | 6.5 | $40 | $156-234 | 0.5 mi from 200 Paul; subject to environmental approvals (former Naval Shipyard) |
| SFO Parking Lot | 10 | $60 | $141-197 | Subject to SFO approval |
| Tesla Portal | 2.8 | $17 | $85-169 | On aqueduct ROW |
| Pulgas Balancing Reservoir | 2.5 | $20 | $150 | On aqueduct |
| University Mound North Basin | 2.9 | $20 | $154-273 | Seismic upgrade required |
| Sutro Reservoir / Summit Pump | 2.4 | $18 | $168-273 | In-City |
| SF Port Pier 90-94 | 3.1 | $21 | n/a | Industrial waterfront |

Small hydro on the SFPUC water system was separately identified:
- Bay Area: ~5-10 MW total potential. Two projects reportedly under development at time of report: University Mound (240 kW) and Sunol (1 MW).
- San Joaquin/Upcountry: ~10 MW from efficiency improvements, potentially >50 MW total at Moccasin and "East of Moccasin" if full development opportunity pursued.
- RPS eligibility: small hydro under 30 MW *is* RPS-eligible; Hetch Hetchy large hydro is not.

Recommended financing pattern: **PPA with ownership transfer at year 7**, citing Black & Veatch analysis that this produced the lowest lifetime LCOE. A private developer would build and operate for the first 7 years (capturing tax credits, absorbing performance risk), then transfer the asset to the City.

The report assumed:
- Federal solar ITC expiring at end of 2016 (since extended and superseded by IRA elective pay through 2032+).
- 2007-2013 solar PV cost trajectory.
- CleanPowerSF initial program load of 20-30 MW (since grown to 500+ MW).
- "H bonds" as a financing instrument (since superseded by current SFPUC revenue bond practice).

---

## 4. What actually happened 2015-2026: contracts replaced ownership

A decade after the LAFCo report, **virtually none of the identified sites has been built**. SFPUC and CleanPowerSF substituted out-of-county third-party PPAs and California Community Power JPA joint procurement for owned renewable development on SFPUC land. The substitution was driven by:

1. **PPA prices declined faster than expected.** Solar PV LCOE dropped 60-70 percent from 2015-2025. Central Valley utility-scale projects via PPA reach prices below what owned local development could match.
2. **CleanPowerSF reached 100 percent renewable two years ahead of schedule** without needing owned local generation.
3. **Hetch Hetchy Power's customer base grew** with Treasure Island, Hunters Point, and Mission Rock retail expansion, absorbing the existing renewable resource.
4. **Owned local development requires capital, permitting, and operational capacity** that PPAs externalize to private developers.
5. **The 2023 HHP IRP** forecasts no significant additional renewable procurement until 2033, freezing the local-development question for the better part of a decade.

Tactically rational. Strategically leaves the local-development thesis unanswered. The CCSF compute consortium proposal, by introducing a *new municipal customer with a 35-350 GWh/year demand profile and political incentive to anchor on SFPUC infrastructure*, restores the demand-side case for owned generation that PPAs alone could not justify.

---

## 5. Site-by-site current disposition (May 2026)

| Site | 2015 LAFCo concept | 2026 actual status |
|---|---|---|
| **Sunol Valley** | 17.5 MW solar, RFP recommended | Re-scoped 2020 in SFPUC Local Renewable Energy Report to ~40 MW solar+storage at the closed 280-acre Sunol Valley Golf Course. November 20, 2020 LAFCo packet described as "high-suitability" at $30-35/MWh below in-City. **Never advanced past evaluation since 2020.** No RFP issued. Surrounding land hosts Sunol AgPark, Sunol Water Temple, Sunol Yard (rebuilt 2019), Sunol Valley WTP, DeSilva Gates aggregate quarry lease (~325 acres to ~2030), Alameda Creek Watershed Center (late 2026 completion). Political constraint: Alameda Creek Alliance, Sunol Citizens Advisory Council, 2017 community letter opposing industrial conversion |
| **Warnerville Substation** | 29.8 MW solar, subject to land acquisition | Land acquisition never closed. Warnerville treated as transmission asset only; Phase 2 substation rehabilitation contract DB-127R active. **Paulsell Solar Energy Center** (20 MW solar + 15 MW BESS, NextEra, COD June 2024) was sited nearby in Stanislaus County instead — third-party PPA on non-SFPUC land. The Warnerville-corridor solar demand was effectively satisfied off-site by contract |
| **2024 Moccasin parcel acquisition** | n/a (post-report) | $525K, 41 acres on Switchback Road. Purpose is **operational**: maintenance access, fire egress, easement extinguishment. **Not a renewable energy parcel.** Earlier analysis suggesting renewable relevance is corrected here |
| **Tesla Portal** | 2.8 MW solar | No movement since 2015 |
| **Pulgas Balancing Reservoir** | 2.5 MW solar | No movement since 2015 |
| **Hunters Point Parcel E** | 6.5 MW solar | **Not transferred to City.** Navy radiological remediation projects complete end of 2027. Hazmat removal for shipyard demolition began March 2026. No solar development possible on the parcel until post-transfer. A 200 Paul co-located solar story is on a 2+ year delay minimum |
| **SFO Parking Lot** | 10 MW solar carport | Not built. SFO has ~4.5-4.6 MW rooftop only; ZNE plan targets 55 MW campus-wide through third-party PPA. The 10 MW LAFCo carport concept is inactive |
| **University Mound North Basin** | 2.9 MW solar | Seismic upgrade completed 2011. No solar PV built on it. The reservoir is among the City's largest treated-water storage; solar use unclear due to operational constraints |
| **Sutro Reservoir / Summit Pump** | 2.4 MW solar | Not built |
| **SF Port Pier 90-94** | 3.1 MW solar | Not built. Per Port's 2023 OSW concept plan, the piers were redirected to potential offshore wind floating-foundation fabrication |
| **University Mound small hydro (240 kW)** | "Under development" 2014-15 | **No public record of operation.** Either dropped, completed undocumented, or the 2015 report overstated. Confirm with Power Enterprise |
| **Sunol Valley 1 MW small hydro** | "Under development" 2014-15 | **No public record of operation.** Current "Sunol 1.1 MW" reference in some SFPUC documents is solar PV at the WTP, not hydro. Confirm with Power Enterprise |
| **Moccasin Low-Head ~4 MW small hydro** | Operational 1986 | Still operational, RPS-certified |
| **East of Moccasin / >50 MW potential** | Theoretical maximum if pursued | **No active studies, no capital projects.** 2023 HHP IRP modeled scenarios in which further Moccasin investment is uneconomic |
| **Moccasin Powerhouse Generator Rehab** | n/a | $1.6M contingency increase, 331-day delay. Returned to service November 2025. Asset preservation only, no capacity expansion |
| **Moccasin Penstock replacement** | n/a | $285M, largest single item in FY26-35 capital plan. 75-100 year life extension. Asset preservation only |

---

## 6. The Raker Act constraint

The Raker Act of 1913 authorized SF to construct Hetch Hetchy dam and aqueduct on federal land in exchange for specific public-purpose commitments. **Section 6** prohibits sale of Hetch Hetchy power "to any corporation or individual" except to municipalities and qualifying irrigation/water districts. Strictly enforced by *United States v. City and County of San Francisco* (1940). Subsequent litigation has periodically tested the boundary; the consistent ruling has favored strict municipal-only application.

**Implications for the CCSF compute consortium:**

A municipal AI compute facility serving CCSF departments is structurally Raker-compatible — the offtaker is a municipal entity. Leasing capacity to private tenants (the commercial GPU marketplace, anchor-tenant, or commercial AI lab options in the original brainstorm) is **not** Raker-compatible without congressional or legal restructuring.

A consortium of California municipal members under a JPA is **cleanly Raker-compatible** because every offtaker is a municipal entity. This is a stronger legal posture than a standalone CCSF facility with anchor-tenant capacity sharing. The Raker Act, often framed as a constraint, is actually structurally aligned with the JPA consortium model.

City Attorney opinion required before any commitment.

---

## 7. The climate-driven cooling architecture

Coastal SF allows near-chillerless airside economization roughly 95 percent of hours annually. The right architecture for a 4-40 MW AI hall is **dry-cooler-first with wet-trim** only on the ~15-25 days per year when wet-bulb temperature exceeds 75°F. That hybrid design uses 7-20 acre-feet per year of makeup water for a 5 MW load versus 60-105 AF/year for all-evaporative.

**Reclaimed water becomes a peak-day insurance policy, not the base cooling source.** Reframes the SE Plant integration question: you don't need 0.5 MGD of tertiary effluent year-round; you need 20-50K gpd reliably on the hottest days. Much smaller engineering ask.

This is fundamentally different from data center cooling design in Texas, Arizona, or even Virginia — peers where heat is the primary constraint. SF's climate is a structural advantage.

### 7.1 Liquid cooling architecture

Modern AI racks (GB200 NVL72 and successors) require direct-to-chip liquid cooling. The cooling architecture has three loops:

1. **Primary loop (chip-side, FWS):** deionized water or 25-50 percent glycol per ASHRAE TC 9.9 W45/W55 (supply 35-45°C, return 45-55°C, pH 7.5-9.0). Annual inhibitor testing. **Reclaimed water never touches the chip.**
2. **Facility water loop (TCS):** treated potable water or RO-polished reclaimed, between the CDU heat exchanger and the heat-rejection equipment.
3. **Heat rejection (where reclaimed water lives):** dry coolers (no water) or evaporative cooling towers (this is where reclaimed water serves). Hybrid dry/wet uses dry coolers first, evaporative as wet-trim on peak days.

### 7.2 Title 22 compliance

California Code of Regulations Title 22 §60306 requires **disinfected tertiary** recycled water for any cooling tower, evaporative condenser, or misting system, with drift eliminators and continuous biocide. Disinfected secondary is not permitted for cooling tower service without an approved variance.

SE Plant currently produces disinfected secondary. To deliver Title 22 tertiary to 200 Paul, the path is:

- **Side-stream polishing skid at SE Plant:** MBR or UF + UV, $1.5-4M for a 50-200 kgpd capacity unit serving a 5 MW load. At 40 MW scale, a larger central polishing facility ($15-40M, potentially folded into the SSIP scope) would be more economic.
- **Purple-pipe extension** from SE Plant to 200 Paul (~0.5 mile in urban Bayview): $400-1,200/LF in urban SF including pavement restoration, $1.5-3M for the run.
- **Pretreatment train at the data center:** 5-10 µm self-cleaning filtration, softening if needed, dual biocide program (oxidizing plus rotated non-oxidizing), phosphonate/polymaleic scale inhibitor, azole corrosion inhibitor. ASHRAE 188 Legionella Water Management Plan. Quarterly Legionella PCR.

### 7.3 Water consumption math

Industry rule-of-thumb water use effectiveness (WUE) is ~0.5-1.8 L/kWh for full evaporative cooling. At 1.0 L/kWh and 5 MW IT load running 24/7: 120,000 L/day ≈ 31,700 gpd ≈ **35 AF/year**. Hybrid wet/dry in SF climate: 7-20 AF/year. At 40 MW scale: 280-820 AF/year depending on cooling mode.

For context: SE Plant average dry-weather flow ~60 MGD ≈ 67,000 AF/year. Even a 40 MW DC's peak cooling demand is less than 1 percent of plant output.

---

## 8. Three siting scenarios in detail

### 8.1 Scenario A: 200 Paul Ave / Digital Realty with hybrid cooling

Digital Realty operates a colocation facility at 200 Paul Ave. Permit-ready, grid-connected today via CleanPowerSF. Bayview industrial zoning. Half a mile from SE Plant. Adjacent to Hunters Point Naval Shipyard (parcel transfer expected 2027).

**Energy:** CleanPowerSF Green (>90 percent clean) as default; Hetch Hetchy Power service may be achievable at 4-10 MW depending on allocation. CPSF SuperGreen (100 percent California-certified) available at small premium.

**Cooling:** Hybrid dry-cooler-first with wet-trim using SE Plant Title 22 reclaimed effluent. New side-stream polishing skid at SE Plant. Dedicated purple-pipe extension to 200 Paul.

**Capex premium:** $3-7M one-time for 5 MW (polishing + purple pipe). Scales to $20-50M at 40 MW including potential SSIP-scope tertiary upgrade.

**Pros:** Fast to deploy. No CEQA for the data center itself (Digital Realty operates an existing permitted facility). Latency to CCSF municipal users near zero. Politically excellent narrative — SF cooling SF's compute with SF's recycled water.

**Cons:** No on-site renewable generation in Phase 1 (Hunters Point Parcel E unavailable until 2027+). Cooling capex premium without owned generation savings — economics are marginal at 5 MW, favorable at 20+ MW.

### 8.2 Scenario B: Sierra batch pod (Moccasin or aqueduct-foothills)

A compact GPU pod sited in Tuolumne County or in the aqueduct corridor between Moccasin and Tesla, served directly by Hetch Hetchy hydro for non-latency-sensitive batch workloads.

**Energy:** Direct Hetch Hetchy hydro at the municipal enterprise rate (~$40-60/MWh). Behind-the-meter delivery avoids wheeling.

**Cooling:** Dry cooling adequate in Sierra winter; significant cooling load in summer when temperatures exceed 100°F at Moccasin, exactly when AI demand peaks. No wastewater source nearby.

**Four hard limits, all still applying:**

1. **No carrier-grade fiber** to SF today. The SFPUC SCADA backbone is not built for tenant-grade bandwidth. A ~140-mile middle-mile build via leveraging Tuolumne County's Connect 49 plans or CENIC corridors would run $30-80M to do carrier-grade right.
2. **Drought-year firmness.** Hetch Hetchy is largely run-of-river with reservoir shaping. A 24/7 AI load cannot be firmed by Hetch Hetchy alone in dry years.
3. **Summer cooling.** Moccasin summer highs > 100°F kill dry-cooler efficiency exactly when inference demand peaks.
4. **CEQA, tribal consultation under AB 52, Tuolumne County land-use approval, wildfire risk** (Rim Fire 2013 burned the Holm-area watershed).

**Capex:** $80-150M for 10 MW pod including fiber, buildout, interconnect.

**Pros:** Direct hydro economics. Raker-compatible municipal load. White-space opportunity to extend Hetch Hetchy's municipal-load story to compute.

**Cons:** Operational complexity. Geographic disadvantage. Constraint stack means realistic ceiling is 10-15 MW.

### 8.3 Scenario C (recommended): Workload-split hybrid with Sunol Valley solar+BESS

The strongest physical configuration that can be assembled from current SFPUC inputs.

**Inference workload** (interactive, latency-sensitive, ~70 percent of total tokens — drafts, summaries, Q&A): sited at 200 Paul under CleanPowerSF Green or HHP, with hybrid wet-trim cooling using SE Plant reclaimed effluent.

**Batch and overnight workload** (records-request triage, document OCR, scheduled reports, model fine-tuning, ~30 percent of tokens with relaxed latency tolerance): sited at a Sierra batch pod under direct Hetch Hetchy hydro and dry cooling.

**Dedicated solar+BESS resource at Sunol Valley** (25-40 MW solar plus 4-hour BESS): supplies the Sierra pod behind-the-meter where geometry allows, feeds surplus to Newark interconnect for SF-bound delivery, and serves as the additionality story for the consortium's renewable demand. Sunol is the lowest-LCOE site in the 2015 LAFCo inventory, the parcel is City-owned (280-acre former golf course), and the site has been re-scoped to solar+storage in SFPUC's 2020 internal review but has not advanced to RFP.

**This is the configuration that most efficiently exploits the JPA structure.** Batch workloads can be shared across consortium members on shoulder hours when each city's interactive demand is low. Solar generation at Sunol can serve a regional consortium load profile that no single city could absorb. The Sunol parcel becomes the consortium's anchor demand justification.

**Pros:** Uses each SFPUC asset for what it does best. Raker-compatible (all consortium offtakers are municipal). Restores the demand-side case for owned generation at Sunol that PPAs alone could not justify. Political narrative is durable (Hetch Hetchy / Fiber to Housing / SE Plant / Sunol all in one story).

**Cons:** Requires Sunol Valley parcel disposition to move forward at SFPUC, which has been stalled in evaluation since 2020. Alameda Creek Alliance and Sunol community opposition to industrial conversion is a real political constraint. Multi-site operations complexity. Capital ask is larger than either scenario alone.

---

## 9. Cost analysis

### 9.1 Cost premiums for a 5 MW facility at 200 Paul

| Element | One-time capex premium | Annual opex impact |
|---|---|---|
| Title 22 tertiary side-stream polishing at SEP | $1.5-4M | +$50-150K (chemicals, monitoring) |
| Purple-pipe extension SEP to 200 Paul (~0.5 mi urban) | $1.5-3M | minimal |
| Hybrid wet/dry cooling system vs. dry-only | ~$0 (similar baseline at AI density) | -$100-200K vs. potable cooling |
| HHP municipal enterprise rate instead of CPSF Green | $0 | -$600-700K/yr |
| Dedicated CV solar+BESS PPA (additionality) | $0 (PPA structure) | comparable to CPSF Green, 20-yr lock |

**Net for 5 MW:** roughly $3-7M one-time premium plus $600-700K/year of energy savings if HHP serves the load. Payback on cooling capex 5-10 years depending on energy mix. Below 4 MW the wastewater premium isn't worth the complexity. Above 10 MW it pencils strongly.

### 9.2 Cost premiums for a 40 MW facility (CCSF + early consortium members)

| Element | One-time capex premium | Annual opex impact |
|---|---|---|
| Full Title 22 tertiary upgrade at SEP or large polishing facility | $15-40M (could fold into SSIP scope) | +$500K-1.5M |
| Purple-pipe trunk through Bayview industrial corridor | $5-15M | minimal |
| CV solar+BESS PPA layered in (HHP alone insufficient at scale) | $0 (PPA) or $300-600M if SFPUC-owned | ~$25-30M/yr generation, 20-yr lock |
| Sierra batch site at Moccasin (10 MW pod) | $80-150M (fiber + buildout + interconnect) | -$3-5M/yr vs. all-SF |
| Sunol Valley solar+BESS (25-40 MW) | $50-90M (utility solar at $1.8-2.3M/MW + BESS) | -$2-4M/yr vs. PPA |

At consortium scale, the SE Plant upgrade economics align with SSIP's own trajectory. CCSF compute could be a credible anchor demand customer that justifies adding full Title 22 capability to the SSIP scope, which would in turn make eastside recycled water economically viable for other Bayview industrial customers — cross-system synergy that doesn't show up in single-purpose business cases.

### 9.3 Energy cost comparison

For a 5 MW DC running 50 percent capacity factor (~22 GWh/yr):

| Option | $/MWh | Annual generation cost |
|---|---|---|
| Hetch Hetchy Power municipal enterprise rate | ~$40-60 | $0.9-1.3M |
| CleanPowerSF Green (default, >90% renewable) | ~$70-80 | $1.5-1.8M |
| CleanPowerSF SuperGreen (100% RPS) | ~$80-90 | $1.8-2.0M |
| Dedicated CV solar + 4-hr BESS PPA | ~$70-85 | $1.5-1.9M |

HHP direct service is materially cheaper where capacity exists. **IRA elective pay treatment** lets a municipal owner directly monetize the 30 percent ITC (40-50 percent with energy-community and domestic-content adders), favoring SFPUC ownership over PPA where land and interconnection align.

---

## 9.5 Humboldt offshore wind + subsea HVDC as consortium-scale supply

*Claude Code · claude-sonnet-4-6 · added 2026-06-20*

**Companion source:** `CCSF_humboldt_offshore_wind_transmission.md` (2026-06-20), with a fact-verification log at its §8. This section folds that file's engineering-relevant findings into the deep-dive; see the companion file for the full political-economy framing, risk list, and source bibliography.

> **Correction (2026-08-16) — the section title's "subsea HVDC" is wrong.** The heading is retained only because other files cross-reference this section by name. The CAISO-approved Humboldt delivery path is **overland**: an approximately 260-mile Humboldt–Collinsville line planned for eventual HVDC operation but **initially operated as 500 kV AC**, plus a separate approximately 140-mile 500 kV AC line to Fern Road, planning in-service year 2034, enabling an initial ~1.6 GW. A **subsea** Humboldt–SF Bay HVDC cable is a *separate, pre-feasibility* concept from Schatz Energy Research Center's 2020 conceptual assessment (~250 miles, ~1.8 GW per bundle, two separated routes for redundancy) — not an approved or engineered route. Read every "subsea HVDC" reference in this section as the overland CAISO path unless it explicitly cites the 2020 Schatz assessment. Canonical statement: the 2026-08-05 synthesis update in `CCSF_compute_initial_brainstorm.md`.

This adds a fourth energy-supply path alongside HHP (Section 2.2), CleanPowerSF (Section 2.3), and the Sunol Valley / Sierra batch pod paths analyzed in Section 8.2–8.3. Unlike those three, this path is not SFPUC-controlled — it is a regional CAISO transmission asset at state/regional-grid scale, ~~that the consortium could anchor as an offtaker,~~ **[struck 2026-06-21 — far too large for the consortium to "anchor"; see §9.5.5]** not a resource SFPUC can develop or contract for unilaterally. The wind file's own §4.2 has the consolidated four-path stack table.

### 9.5.1 Lease areas

Two BOEM Humboldt Wind Energy Area leases resulted from the December 6, 2022 Pacific offshore wind auction:

| Lease | Holder | Acreage | Estimated capacity | Status |
|---|---|---|---|---|
| OCS-P 0561 | Canopy Offshore Wind, LLC (RWE subsidiary) | 63,338 | ~1.6 GW | RWE "Canopy" project; commercial operation "mid-2030s, contingent on permitting" |
| OCS-P 0562 | California North Floating, LLC (Copenhagen Infrastructure Partners; project developer Vineyard Offshore) | 69,031 | over 1 GW | Lease signed June 2023, $173.8M |

**Correction to the combined-capacity figure used elsewhere in this corpus:** the wind file's "~1.6 GW" framing for the Humboldt leases (its §2.1) describes OCS-P 0561 alone. OCS-P 0562 adds "over 1 GW" on top, per BOEM's lease page and the original December 2022 auction reporting. Combined nameplate potential across both Humboldt leases is closer to **~2.6+ GW**, not 1.6 GW. This matters because the HVDC line sized in 9.5.2 below is explicitly the 1.6 GW figure — sized to OCS-P 0561's output, not to both leases combined. If OCS-P 0562 reaches construction on a similar timeline, the transmission scope described below may not have headroom for its full output without a further upgrade. This gap is not flagged in the wind file or its verification log; worth a line in any future revision of that file.

### 9.5.2 CAISO-approved transmission

CAISO's 2023-2024 Transmission Plan (Board-approved May 23, 2024) includes two new lines serving the Humboldt Wind Energy Area, both terminating in the East Bay/Delta:

- **260-mile, 500 kV VSC-HVDC line** — new Humboldt 500 kV substation → Collinsville 500 kV substation (Sacramento–San Joaquin Delta, eastern Contra Costa County). Capacity ~1.6 GW, sized to OCS-P 0561's output (see correction above). VSC (Voltage-Source Converter) technology, suited to variable renewable input.
- **140-mile, 500 kV AC line** — Humboldt substation → Fern Road substation. Adds delivery redundancy and incremental capacity beyond the HVDC line alone. Not previously captured in the wind file's body text; added here per the wind file's own verification log (§8, claim 2), sourced to Downey Brand's April 3, 2024 client alert.

**In-service target: by June 1, 2034**, per the CAISO schedule (wind file §8, claim 2) — later than the "early 2030s" figure used elsewhere in the wind file's body (its §4.5). Treat June 2034 as the more recent, verified figure.

Collinsville sits adjacent to existing PG&E Bay Area transmission infrastructure. It is unrelated to the Trans Bay Cable (53-mile, 400 MW HVDC, SF–Pittsburg) — that is a separate, already-operating asset.

### 9.5.3 Federal headwinds

Two federal actions affect project pace, not the underlying lease or transmission assets:

- **August 29, 2025:** USDOT (Secretary Sean Duffy) withdrew a **$426.7 million INFRA grant** (Nationally Significant Multimodal Freight & Highway Projects program) awarded for the Humboldt Bay Heavy Lift Multipurpose Marine Terminal — staging infrastructure for floating-turbine assembly, not the leases or the transmission line. The Harbor District is seeking alternative funding; the marine-terminal track is delayed, independent of lease or transmission status.
- **December 22, 2025:** a federal pause on offshore wind leasing was applied to five large-scale East Coast projects. Scope is East Coast only — Humboldt's leases (OCS-P 0561, OCS-P 0562) were not directly affected. Litigation over the broader federal pause authority is unsettled as of this drafting; treat the litigation posture as in flux rather than resolved.

**Net assessment, carried over from the wind file (§3):** the CAISO transmission approval is a state-level action (CAISO/CPUC) and does not depend on federal funding or federal lease status. The lease contracts are BOEM instruments, not grant-dependent. The marine terminal is the one piece of Humboldt infrastructure directly exposed to the federal funding cut, and it is staging infrastructure — not a gating dependency for the transmission line or the leases themselves.

### 9.5.4 Raker Act §6 application

Same logic as the Raker Act analysis in Section 6 above, applied to imported (non-Hetch Hetchy) power. Raker Act §6 governs sale of Hetch Hetchy-sourced power specifically; it does not directly apply to CAISO-market power imported via the Humboldt HVDC line. The relevant compatibility question is procurement structure, not power source: CleanPowerSF already procures out-of-county power (Central Valley solar, Section 2.4) through a municipal offtake vehicle and is Raker-compatible on that basis. Humboldt wind power procured the same way — through CleanPowerSF, a CC Power JPA joint solicitation (Section 2.5), or the proposed CCSF compute consortium JPA — follows the same logic: every offtaker under those structures is a municipal entity.

**City Attorney opinion required before any commitment** — the same standing requirement as Section 6's closing line, not a new one.

### 9.5.5 Climate-vision context (anchor-offtaker framing retired)

> [!warning] Correction, 2026-06-20
> This subsection originally argued CCSF's compute consortium could serve as anchor offtaker for the Humboldt transmission line. Per Jeremy's direction: that's wildly out of scale — CCSF/consortium demand (3-40 MW at any modeled scale) against a 1.6-2.6+ GW wind-and-transmission project isn't an anchor relationship. The corrected framing: Humboldt offshore wind belongs here as context for California's broader clean-power and electrification buildout, not as a structural thesis for CCSF's own energy planning. The two "entry points" below (CalCompute, GovAI Summit) are retired along with it — the GovAI Coalition Summit / Khaled Tawfik connection specifically is an AI-generated suggestion never evaluated or adopted by Jeremy.

The CAISO-approved transmission line has a defined supply (Humboldt wind) and a defined delivery point (Collinsville). Its scale — 1.6 GW and growing — puts it at state/regional-grid scale, not municipal-consortium scale. Whatever brings it to final investment decision will be CAISO/state-level demand, not a single municipal consortium's IT load. What's still useful for CCSF's own planning: Humboldt is one more signal that California's clean-power supply is expanding substantially this decade — a tailwind for future energy sourcing, not a dependency, and not something this project should position itself around.

~~Two entry points, both already on the consortium's near-term calendar per the wind file (§4.4–4.5):~~

~~- **CalCompute framework process** — established by **SB 53** (signed September 29, 2025), codified at Gov. Code §11546.8. The statute directs a consortium to deliver a framework report to the Legislature by **January 1, 2027**, including funding-source and governance recommendations. An anchor-offtaker thesis is a concrete municipal-demand input ahead of that deadline.~~
~~- **GovAI Coalition Summit, December 9–11, 2026** — a recruiting venue for founding consortium members, per the wind file's existing Khaled Tawfik engagement recommendation (wind file §5.1, point 3).~~

### 9.5.6 Cost premium vs. base case

**No cost figure exists yet in this corpus for Humboldt-delivered power, and none should be assumed here.** The energy-cost comparison in Section 9.3 covers HHP, CleanPowerSF Green/SuperGreen, and a generic Central Valley solar+BESS PPA — none of those figures represent offshore wind delivered via a 260-mile HVDC import, which carries its own transmission-access charges, CAISO market-participation costs, and PPA structuring that the wind file does not model either. The open question — **PPA-style procurement through CleanPowerSF versus consortium-direct procurement, and what premium either carries over the Section 9.3 baseline** — is unresolved. Flag for SFPUC/CleanPowerSF engagement (a natural addition to the open-questions list in Section 12) rather than estimate; the procurement vehicle itself isn't chosen yet, so a number now would be a guess dressed as an estimate.

### 9.5.7 Collinsville interconnect question

The Collinsville 500 kV substation is an active PG&E project, independent of the Humboldt line — confirmed via a CAISO Project Sponsor Selection Report, CPUC CEQAnet entry 2025010149, FERC-granted transmission incentives, and the WECC 2026 Annual Progress Report (which lists "Collinsville 500/230 kV Substation Project" under LSPGCA) (wind file §8, claim 8). It is the receiving substation for the new Humboldt HVDC line, built as a separate PG&E capital project.

**Open question, not resolved by current sources:** Collinsville also serves PG&E's existing East Bay load and the broader Bay Area grid. Local congestion at Collinsville could constrain how much of the Humboldt line's output actually reaches San Francisco versus being absorbed by closer East Bay load. PG&E's own Bay Area transmission planning has not been examined for this constraint. Flag for PG&E engagement — a natural addition alongside the SFPUC-focused list in Section 11.

---

## 10. The CleanPowerSF IRP window — why timing matters, when this project is ready

**Correction (2026-06-20): the August 10, 2026 filing is not in play for this project.** SFPUC engagement is a long-term process that won't start until the project is far more developed than its current informal-conversation stage, and SFPUC's own posture is conservative and process-cautious. The analysis below explains why IRP timing matters *in general* — useful for whenever engagement does eventually happen, against a future filing cycle — not as an active near-term plan.

CleanPowerSF files an Integrated Resource Plan with the CPUC every 2-3 years. The 2025 "Powering Tomorrow, Together" outreach was the inputs-open precursor to the August 10, 2026 filing, which this project will miss.

**Why IRP timing matters whenever engagement does happen:**

1. The IRP is the document that justifies new generation procurement to the CPUC.
2. Owned generation at Sunol Valley (or any SFPUC-controlled site) has historically failed the IRP cost-effectiveness test because PPAs in the Central Valley beat the LCOE.
3. A new municipal demand profile — the CCSF compute load — could change the cost-effectiveness math by providing a stable, multi-decade offtaker that PPA-only resource portfolios cannot anchor.
4. Each filing locks the planning cycle for another 2-3 years, so missing one means waiting for the next.

**Recommended action, corrected (2026-06-20):** No near-term SFPUC outreach. Once the project has matured well past preliminary, informal conversations, get the CCSF compute load profile **[shared-copy transform, 2026-08-16: named Department of Technology staff removed]** into a future CleanPowerSF IRP planning conversation through GovOps, the Mayor's office, or directly through CleanPowerSF staff — paced to SFPUC's own conservative process, not to any filing deadline.

---

## 11. Engagement points

### 11.1 SFPUC (priority order)

1. **SFPUC Power Enterprise leadership** — direct conversation on HHP allocation for a new municipal load, current Sunol Valley parcel disposition, the 2026 IRP inputs window. Power Enterprise is the operational decision-maker for any CCSF compute electric service.
2. **CleanPowerSF Director / Manager of Power Resources** — IRP scope and timing, CC Power JPA membership conversation as governance precedent, peer-CCA receptivity to a compute consortium offtake structure.
3. **Hetch Hetchy Water and Power Director** — Moccasin and East-of-Moccasin small hydro disposition, Sierra siting possibilities, fiber options.
4. **SFPUC Engineering / Water Quality Division** — SE Plant tertiary upgrade scope, Title 22 reclaimed water service to industrial customers, NPDES considerations.
5. **SFPUC Real Estate Services** — Sunol Valley parcel disposition, Warnerville-area parcel status, aqueduct-corridor land availability.
6. **SFPUC General Manager Dennis Herrera** — once the staff-level conversations have surfaced the questions, the GM is the convener of cross-Enterprise decisions.

### 11.2 City Attorney

Required for the Raker Act application opinion to a multi-government compute consortium. The City Attorney's office has a long history of Raker-compatibility analysis (every Hetch Hetchy commercial sales agreement passes through this office).

### 11.3 SF LAFCo

LAFCo's CleanPowerSF oversight role gives it standing to commission follow-up analysis on the local renewable buildout question, and LAFCo packet materials are how SFPUC's CleanPowerSF planning becomes public. LAFCo is also the entity that commissioned the original 2015 EnerNex report and is the natural sponsor for a 2026 update if CCSF compute proceeds.

### 11.4 GovOps and Mayor's office

For the IRP-inclusion ask to land at CleanPowerSF, the political channel goes through GovOps and the Mayor's office. Department of Technology cannot unilaterally direct SFPUC.

---

## 12. Open technical questions for SFPUC engagement

1. **Sunol Valley parcel disposition.** What's the current SFPUC posture on the 280-acre former golf course? Has the 2020 ~40 MW solar+storage concept advanced beyond evaluation? What are the gating issues — Alameda County permitting, Alameda Creek Alliance opposition, internal land-use planning, or capital availability?
2. **Warnerville Substation land acquisition.** Did SFPUC ever pursue the land acquisition the 2015 LAFCo report flagged? Why did Paulsell get sited adjacent rather than on SFPUC land?
3. **Sunol 1 MW small hydro and University Mound 240 kW small hydro.** Did either project ever come online? If yes, status. If no, why not.
4. **Moccasin and East-of-Moccasin small hydro potential.** Has SFPUC scoped any of the >50 MW potential identified in the 2015 report? Is it in the current Hetch Hetchy capital plan?
5. **Current MID/TID power sales contract terms.** Is there capacity to redirect surplus to a new municipal load?
6. **Dark fiber availability** between Moccasin and SF. What carrier-grade capacity exists today, and what would a build cost?
7. **Spare interconnect capacity** at the Moccasin substation for new behind-the-meter load.
8. **SE Plant effluent temperature profile** seasonally — needed to size the cooling loop.
9. **SE Plant Title 22 tertiary upgrade roadmap.** Is full Title 22 (filtration + UV) part of the SSIP Nutrient Reduction Project scope, or would it be a separate capital project?
10. **CleanPowerSF Integrated Resource Plan** — current portfolio inputs for the August 2026 filing, headroom for a 40 MW DC load, and IRP timeline for owned generation at Sunol Valley.
11. **HHP allocation rules.** Under what conditions can a new municipal load take HHP service vs. CleanPowerSF default? What's the current spare allocation?
12. **Hunters Point Parcel E transfer schedule.** Confirm with Navy/Treasure Island Development Authority for current 2027 estimate.

---

## 13. Sources

### SFPUC system and Hetch Hetchy

- [SFPUC Hetch Hetchy Power System](https://www.sfpuc.gov/about-us/our-systems/hetch-hetchy-power-system)
- [SFPUC Power Rates 2025-26](https://www.sfpuc.gov/accounts-services/water-power-sewer-rates/power-rates-2025-26)
- [SFPUC IRP filing, CEC docket 18-IRP-01](https://efiling.energy.ca.gov/GetDocument.aspx?tn=256080&DocumentContentId=91857)
- [SFPUC Moccasin Powerhouse Rehabilitation](https://www.sfpuc.gov/about-us/news/raindrops-electrons-moccasin-powerhouse-rehabilitation-project-moves-forward)
- [SFPUC FY 2024-25 to FY 2033-34 10-Year Capital Plan (Attachment B)](https://www.sfpuc.gov/sites/default/files/about-us/policies-reports/FY25-34_Capital_Plan_Report_AttB.pdf)
- [SFPUC 2025 Resolution Log](https://www.sfpuc.gov/sites/default/files/about-us/commission/2025_Resolution_Log.pdf)
- [Raker Act overview](https://en.wikipedia.org/wiki/Raker_Act)

### CleanPowerSF

- [CleanPowerSF Key Documents](https://www.cleanpowersf.org/key-documents)
- [CleanPowerSF Integrated Resource Plan page](https://cleanpowersf.org/resourceplan)
- [CleanPowerSF 2022 IRP LAFCo Presentation](https://cleanpowersf-sfpuc-yem2.squarespace.com/s/July-2022-IRP-LAFCo-Presentation-FINAL.pdf)
- [SFPUC Paulsell Energy Center announcement](https://www.sfpuc.gov/about-us/news/cleanpowersf-announces-solar-and-battery-storage-contract-expanding-programs)
- [SFPUC Crow Creek announcement](https://www.sfpuc.gov/about-us/news/sfpuc-commits-new-solar-and-battery-energy-storage-project-northern-california)
- [SFPUC 100% renewable announcement](https://www.sfpuc.gov/about-us/news/cleanpowersf-provides-100-renewable-electricity-san-francisco-customers-two-years)
- [California Community Power JPA formation](https://cacommunitypower.org/eight-ccas-form-new-jpa/)

### SE Plant and SSIP

- [SFPUC Treating the Liquid Flows (SE Plant)](https://www.sfpuc.gov/about-us/our-systems/sewer-system/treating-liquid-flows)
- [SFPUC New Headworks Facility](https://www.sfpuc.gov/construction-contracts/construction-projects/new-headworks-facility)
- [SFPUC Biosolids Digesters Facilities](https://www.sfpuc.gov/construction-contracts/construction-projects/biosolids-digesters-facilities)
- [SFPUC Upgrading System to Reduce Nutrients](https://www.sfpuc.gov/about-us/our-systems/sewer-system/upgrading-our-system-reduce-nutrients)
- [SFPUC Westside Enhanced Water Recycling Project](https://www.sfpuc.gov/construction-contracts/construction-projects/westside-enhanced-water-recycling-project)
- [SFPUC Recycled Water Rules and Regulations Oct 2024](https://www.sfpuc.gov/sites/default/files/documents/SFPUC_Recycled_Water_Rules_and_Regs_October_2024.pdf)
- [SFPUC Alternative Water Supply Annual Progress Report 2023-24](https://www.sfpuc.gov/sites/default/files/programs/2023-24_AWS_Annual_Progress_Report.pdf)
- [RWQCB Order R2-2024-0013 (SE Plant NPDES)](https://www.waterboards.ca.gov/sanfranciscobay/board_decisions/adopted_orders/2024/R2-2024-0013.pdf)
- [22 CCR § 60306 Recycled Water for Cooling](https://www.law.cornell.edu/regulations/california/22-CCR-60306)
- [EPA California Water Reuse Guideline for Industry](https://www.epa.gov/waterreuse/summary-californias-water-reuse-guideline-or-regulation-industry)

### Reclaimed water cooling precedents

- [Google uses recycled water at Georgia data center (DCD)](https://www.datacenterdynamics.com/en/news/google-uses-recycled-water-at-georgia-data-center/)
- [AWS using reclaimed wastewater at 20 locations (DCD)](https://www.datacenterdynamics.com/en/news/aws-using-reclaimed-wastewater-for-data-center-cooling-at-20-locations/)
- [Water Reuse Case Study: Quincy WA (EPA)](https://www.epa.gov/waterreuse/water-reuse-case-study-quincy-washington)
- [Microsoft datacenters water](https://local.microsoft.com/blog/understanding-water-use-at-microsoft-datacenters/)
- [NVIDIA Blackwell water efficiency / liquid cooling](https://blogs.nvidia.com/blog/blackwell-platform-water-efficiency-liquid-cooling-data-centers-ai-factories/)
- [GB200 NVL72 cooling requirements (ToneCooling)](https://tonecooling.com/nvidia-gb200-nvl72-cooling-requirements/)
- [Energy Implications of Economizer Use in California Data Centers (LBNL)](https://www.osti.gov/servlets/purl/937579)
- [DOE FEMP Cooling Water Efficiency for Federal Data Centers](https://www.energy.gov/cmei/femp/cooling-water-efficiency-opportunities-federal-data-centers)

### 2015 LAFCo report and disposition

- [SF LAFCo / EnerNex Local Build-out Final Report (January 30, 2015)](https://lafco.archive.sf.gov/sites/default/files/FileCenter/Documents/50676-SF%20LAFCo%20CCA%20Local%20Buildout%20Revised%20Final%20Report.pdf)
- [LAFCo CleanPowerSF Job Study (May 5, 2016)](https://www.sfgov.org/lafco/sites/default/files/FileCenter/Documents/55829-FINAL%20-%20LAFCo%20CleanPowerSF%20Job%20Study%205-5-16.pdf)
- [LAFCo Packet, November 20, 2020, Item 5 (LRER review, Sunol 40 MW)](https://www.sfgov.org/lafco/sites/default/files/lfc112020_item5.pdf)
- [LAFCo Packet, July 16, 2021, Item 3](https://www.sfgov.org/lafco/sites/default/files/lfc071621_item3.pdf)
- [LAFCo CleanPowerSF Update presentation, July 17, 2024](https://www.sfgov.org/lafco/sites/default/files/lfc071924_item3_presentation.pdf)
- [LAFCo CleanPowerSF BESS Study, September 2024](https://www.sfgov.org/lafco/sites/default/files/LAFCo_CleanPowerSF_BESS_Study_20240916.pdf)
- [Sunol Community letter to SFPUC, July 2017 (Alameda County BoS agenda)](http://www.acgov.org/board/bos_calendar/documents/DocsAgendaReg_7_19_17/GENERAL%20ADMINISTRATION/Regular%20Calendar/To_the_SFPUC_board_of_directors.pdf)
- [Alameda Creek Alliance, Sunol Valley campaign page](https://www.alamedacreek.org/restoration-progress/sunol-valley.php)
- [Independent News — Sunol Valley Golf Course closure (December 2015)](https://www.independentnews.com/news/another-golf-course-may-replace-closing-sunol-links/article_a484face-a44a-11e5-a157-6b40b4945bf0.html)
- [SFPUC Alameda Creek Watershed Center construction](https://www.sfpuc.gov/construction-contracts/construction-projects/alameda-creek-watershed-center-in-Sunol)
- [SFPUC Sunol AgPark](https://www.sfpuc.gov/learning/for-educators/school-field-trips/sunol-agpark)

### Digital Realty / 200 Paul

- [Digital Realty SFO10 / 200 Paul Avenue](https://www.digitalrealty.com/data-centers/americas/silicon-valley/sfo10)

### Solar and BESS economics

- [LBNL Utility-Scale Solar 2025 Update](https://emp.lbl.gov/sites/default/files/2025-10/Utility%20Scale%20Solar%202025%20Edition%20Slides.pdf)
- [APPA Elective Pay Tax Credits](https://www.publicpower.org/policy/elective-pay-tax-credits)

### Humboldt offshore wind and HVDC transmission (Section 9.5)

- [California North Floating LLC (OCS-P 0562) — BOEM lease page](https://www.boem.gov/renewable-energy/state-activities/california-north-floating-llc-ocs-p-0562)
- [California Lease Sale Winners: RWE, Equinor, CIP, Ocean Winds, Invenergy (Offshorewind.biz, Dec 7, 2022)](https://www.offshorewind.biz/2022/12/07/california-lease-sale-winners-are-rwe-equinor-cip-ocean-winds-and-invenergy-floating-wind-farm-capacities-higher-than-initially-estimated/) — OCS-P 0562 "over 1 GW" capacity estimate
- [Department of Transportation Announces $426.7 Million Grant to Develop Deepwater Port and Marine Terminal in Humboldt Bay (Downey Brand)](https://www.downeybrand.com/legal-alerts/department-of-transportation-announces-426-7-million-grant-to-develop-deepwater-port-and-marine-terminal-in-humboldt-bay/) — original INFRA grant award
- [Trump Administration Pulls Funding for Humboldt Bay Offshore Wind Terminal (Lost Coast Outpost, Aug 29, 2025)](https://lostcoastoutpost.com/2025/aug/29/doomed-offshore-wind/) — grant withdrawal
- [SB 53 chaptered text (LegiScan)](https://legiscan.com/CA/text/SB53/id/3271094/California-2025-SB53-Chaptered.html) — CalCompute statutory basis, Gov Code §11546.8
- [Governor Newsom Signs SB 53 (Sept 29, 2025)](https://www.gov.ca.gov/2025/09/29/governor-newsom-signs-sb-53-advancing-californias-world-leading-artificial-intelligence-industry/)
- See also `CCSF_humboldt_offshore_wind_transmission.md` §7 for the full Humboldt/CAISO source list (lease areas, transmission plan, federal headwinds)

<!-- END FULL DOCUMENT: CCSF_SFPUC_power_water_deep_dive.md -->

### Complete document 2 of 2: Humboldt offshore wind and Bay Area transmission

The complete shared copy begins after the delimiter below. It preserves the document's full factual base, correction notes, retired thesis, risk analysis, source bibliography, and verification log.

<!-- BEGIN FULL DOCUMENT: CCSF_humboldt_offshore_wind_transmission.md -->
# CCSF Compute + Humboldt Offshore Wind + Bay Area Subsea Transmission — Integration Analysis

**Date:** 2026-06-20  
**Author context (shared copy):** Personal, unchartered research by Jeremy Pollock; not CCSF work product. Supplements `CCSF_public_compute_strategic_brief.md` and `CCSF_SFPUC_power_water_deep_dive.md`. Read first before any consortium energy-supply discussion.  
**Document purpose:** Capture the connection between CCSF's municipal compute demand, the CAISO-approved Humboldt-to-Bay Area 500 kV HVDC transmission line, and the offshore wind lease areas off Humboldt County, as context for San Francisco's and California's broader climate and electrification buildout. Surface the timing/uncertainty that matters for planning.

> [!warning] Correction from Jeremy, 2026-06-20 — read before relying on this file
> This file originally framed CCSF's compute consortium as a potential **anchor offtaker** for the Humboldt transmission line (§1, §4.3, §4.4, §4.5, §5.1). That framing is **retired** — wildly out of scale. CCSF/consortium compute demand (3-40 MW at any modeled scale, per the strategic brief's §3.6 table) against a 1.6-2.6+ GW wind-and-transmission project isn't an anchor relationship; even this file's own §4.1 already showed the line dwarfing demand by 50-500x, which should have been the signal to drop the thesis rather than caveat it. **Corrected framing:** Humboldt offshore wind is part of San Francisco's and California's much larger climate and electrification vision — the clean-power buildout that transportation electrification, building electrification, and AI/compute growth broadly will need over the next decade — not a thesis where CCSF's compute load anchors or justifies the transmission line's financing. The factual material in §2-§3 and the verification log in §8 stands; only the offtaker/anchor relationship to CCSF is corrected. Separately: the GovAI Coalition / Khaled Tawfik engagement referenced in §4.4, §4.5, and §5.1 is an AI-generated suggestion Jeremy has not evaluated or acted on, and the August 10, 2026 CleanPowerSF IRP reference in §4.5 won't happen in time for this project — SFPUC engagement is long-term and gated on the project maturing well past its current informal stage.

---

## 1. Why this connection matters now

The CCSF compute sizing math breaks at ~40 MW because SFPUC's HHP portfolio is energy-limited and largely committed. The strategic brief rejected standalone build (commercial GPU marketplace, near-breakeven) and committed to a multi-government JPA consortium as the primary path. At consortium scale, the energy supply question becomes load-bearing: where does 50–500 MW of new clean power come from?

The existing deep-dive covers three SFPUC-controlled supply pathways (HHP, CleanPowerSF, Sunol Valley solar+BESS). This file adds a fourth: ~~**imported offshore wind from Humboldt County via the CAISO-approved subsea HVDC transmission line.**~~ **Correction (2026-08-16):** the CAISO-approved delivery path is **not subsea**. CAISO's approved 2023–2024 transmission plan enables an initial ~1.6 GW of Humboldt-area wind through a new Humboldt substation, an approximately **260-mile overland Humboldt–Collinsville line planned for eventual HVDC operation but initially operated as 500 kV AC**, plus a separate approximately **140-mile 500 kV AC line to Fern Road**, with a planning in-service year of 2034. The subsea concept is a **separate, pre-feasibility** study — Schatz Energy Research Center's 2020 *Humboldt–San Francisco Bay Subsea Transmission Cable Conceptual Assessment* (~250-mile HVDC link, ~1.8 GW per cable bundle, two separated routes for redundancy). The two are distinct and must not be conflated. Canonical statement of this distinction: the 2026-08-05 synthesis update in `CCSF_compute_initial_brainstorm.md`. The corrected reading of this file is: imported offshore wind from Humboldt County via CAISO-approved regional transmission, with a redundant subsea corridor as a separate long-term research question. It is the largest single new clean-energy resource in CCSF's planning horizon and the one most likely to scale to consortium size.

**Correction (2026-06-20):** the paragraph above originally continued into an anchor-offtaker political-economy argument (CCSF consortium as structural accelerant for the transmission line, MGHPCC/AICR analog). Retired per Jeremy's direction — out of scale. The more accurate framing: Humboldt offshore wind and its transmission line are part of a state-scale climate and electrification buildout that CCSF's own compute consortium is, at most, one small beneficiary of — not an accelerant or anchor for it.

---

## 2. The confirmed planning state (mid-2026)

### 2.1 Offshore wind lease areas off Humboldt County

**Confirmed.** BOEM held the first Pacific offshore wind auction on December 6, 2022. Five lease areas covering 373,268 acres; total potential ~4.6 GW across all five leases; high bids of $757.1 million. **Two of the five leases are in Northern California off Humboldt County** (the other three are off Morro Bay/Central Coast). Combined Humboldt lease potential is ~2.6+ GW across both leases:

- **RWE lease OCS-P 0561** — 63,338 acres, estimated capacity up to 1.6 GW. RWE's "Canopy" project. Won at $157.7M bid.
- **California North Floating lease OCS-P 0562** — 69,031 acres, estimated capacity up to 1 GW. Held by California North Floating, LLC (Copenhagen Infrastructure Partners; project developer Vineyard Offshore). Won at $173.8M bid; lease signed June 2023.

The CAISO-approved 1.6 GW HVDC line (Section 2.2) is sized to OCS-P 0561's output, not the combined Humboldt total. OCS-P 0562 will need its own transmission scope if it reaches construction on a similar timeline — a transmission-headroom gap flagged in the SFPUC deep-dive §9.5.1.

California state targets: **5 GW offshore wind by 2030, 25 GW by 2045**. Reaffirmed by state officials in May 2026.

### 2.2 The CAISO-approved Humboldt-to-Bay Area 500 kV HVDC transmission line

**Confirmed.** CAISO's 2023-2024 Transmission Plan (provisional approval May 23, 2024) approved the transmission upgrades needed to integrate Humboldt offshore wind into the California grid. The principal element:

- **260-mile, 500 kV HVDC line** from a new 500 kV Humboldt substation to the Collinsville 500 kV substation in the Sacramento-San Joaquin Delta (East Bay).
- **Capacity ~1.6 GW** — sized to deliver the RWE Humboldt lease generation.
- VSC-HVDC technology (Voltage-Source Converter), suitable for variable renewable input.
- Approved as part of CAISO's 20-Year Transmission Outlook (May 2022) and updated in subsequent plan cycles.
- **Plus a parallel 140-mile, 500 kV AC line** from the Humboldt substation to the Fern Road substation (Downey Brand, Apr 3, 2024; §8 claim 2) — adds delivery redundancy and incremental capacity beyond the HVDC line alone. *(Added 2026-06-21 to reconcile this section with the file's own §8 verification log and with brief §7.6 / deep-dive §9.5.2, which already carry it.)*
- **In-service target: by June 1, 2034**, per the CAISO schedule (§8 claim 2).

This is the "subsea" or "underwater" transmission line in the user's framing. The route runs subsea from Humboldt County south along the continental shelf, makes landfall somewhere along the Bay Area's northern coast, and terminates at Collinsville — which sits near the Pittsburg-Antioch area in eastern Contra Costa County, adjacent to existing PG&E Bay Area transmission infrastructure. The Trans Bay Cable (53 miles, 400 MW HVDC, SF to Pittsburg) is a separate, existing asset and not part of this new line.

### 2.3 Staging infrastructure: Humboldt Bay Heavy Lift Marine Terminal

**Confirmed moving forward.** Humboldt Bay Harbor, Recreation & Conservation District is the lead agency for the Heavy Lift Multipurpose Marine Terminal on the Samoa Peninsula (~180-acre site redevelopment). The HB Harbor District had a board meeting scheduled for **June 24, 2026** with a Request for Qualifications for the project. CEQA review (SCH #2023060752) is in process. The terminal is staging infrastructure for floating-turbine assembly and deployment regardless of which developers build the lease areas.

### 2.4 California policy posture

**Confirmed.** The Newsom administration and CEC have maintained the 25 GW by 2045 target. May 2026 reaffirmation: "California remains committed to deploying 25 GW of offshore wind capacity by 2045."

---

## 3. The federal headwind — explicit uncertainty

This material has to be flagged because it changes the consortium's planning posture materially:

- **December 22, 2025:** The Trump administration paused leases for five large-scale offshore wind projects off the East Coast. Existing lease areas — including Humboldt — were not directly rescinded, but the federal-support climate turned hostile.
- **August 29, 2025:** Northern California offshore wind project lost $426.7 million in federal funding (USDOT INFRA grant for the Humboldt Bay marine terminal) from Trump cuts (corrected 2026-06-21 from "September 2025"/"$427M" per §8 claim 6 — withdrawn Aug 29, reported Sept 2–3); "construction of hundreds of offshore turbines delayed" (per Silicon Valley reporting).
- **RWE Canopy timing:** RWE's own communication is "expected to be in operation by the mid-2030s contingent upon the permitting timeline" — i.e., not before 2035, possibly later. The RWE statement is dated 2022; current public communications have not publicly moved this estimate earlier.

**Net assessment:** The CAISO transmission approval is durable (state-level, not federal-dependent). The lease areas themselves are intact (BOEM lease contracts, not federal-grant-dependent). But the development pace is materially slowed by federal hostility. The RWE "mid-2030s" timeline is the realistic anchor; 2030 is not plausible.

---

## 4. The connection to CCSF compute — what changes

### 4.1 Sizing math

The strategic brief §3.6 sized CCSF compute at 500–600K tokens/sec sustained for 5K workers, with peak at ~40 MW IT load (Scenario C). The brief's own §3.6 scaling table shows **sub-linear** scaling — "roughly 10x the workers requires about 6-8x the infrastructure if the consortium is well-designed" — not linear:

| Cohort | Workers | IT load (smoothed) |
|---|---|---|
| CCSF alone | 5,000 | 400–600 kW |
| Regional JPA | 50,000 | 3–5 MW |
| Statewide/multi-state | 500,000 | 25–40 MW |

At the brief's "sweet spot" of 50K–150K workers (Section 3.6), IT load lands in the **3–15 MW range**, not hundreds of MW.

**The Humboldt-to-Bay Area 1.6 GW HVDC line dwarfs consortium-scale demand by 50–500x.** The line is not sized to CCSF consortium compute; it is sized to OCS-P 0561's full 1.6 GW nameplate generation. This reframes the political-economy argument: **energy supply is not the binding constraint for the CCSF consortium.** The HVDC line has multi-decade headroom for any plausible compute load the consortium could draw. The binding constraints are elsewhere — cooling water rights, SFPUC siting, governance, CalCompute framework engagement.

This is a stronger argument than a tight match: a consortium whose energy supply can never be the bottleneck can compete on other terms (governance, sovereign positioning, agency mission alignment) rather than on resource access. **Correction (2026-06-20):** the brief's §7.6 originally threaded this into an anchor-offtaker thesis; that thesis is retired (see warning note at the top of this file) — the dwarfing ratio is exactly why "anchor" was the wrong word, not a caveat to file alongside it.

### 4.2 Energy-supply portfolio shift

The current deep-dive's energy-supply stack:

| Path | Capacity | Status |
|---|---|---|
| HHP (Hetch Hetchy hydro) | ~150 MW existing retail | Energy-limited, committed |
| CleanPowerSF (Central Valley solar/wind/geothermal + BESS) | ~800 MW contracted | Mostly out-of-county PPAs |
| Sunol Valley solar+BESS (owned, CCSF-led) | 25–40 MW potential | Not advanced past 2020 evaluation |
| Sierra batch pod (Moccasin direct hydro) | ~10 MW potential | Raker-constrained; 4 hard limits |

**Add the Humboldt offshore wind path:**

| Path | Capacity | Status |
|---|---|---|
| Humboldt offshore wind via 260-mile HVDC | ~1.6 GW | CAISO approved; commercial operation mid-2030s+ |

The Humboldt path does not displace the Sunol Valley owned-generation case — both serve different scales (Sunol is municipal-grid local; Humboldt is regional import). The Humboldt path **supplements** the consortium-scale gap that no SFPUC-internal resource can close.

### 4.3 Raker Act §6 compatibility

**Confirmed structurally compatible.** The Raker Act prohibits sale of Hetch Hetchy power to "any corporation or individual" except to municipalities and qualifying irrigation/water districts. The Humboldt-to-Bay transmission line delivers power to the California grid (CAISO market); any municipal offtake through a CleanPowerSF-style procurement vehicle or a CC Power JPA joint solicitation is Raker-analogous — i.e., power flowing to a municipal offtaker through a multi-government procurement structure.

**Key implication, corrected (2026-06-20):** Municipal offtake of Humboldt wind power through a JPA structure raises no Raker Act issues, because every offtaker is a municipal entity — the same logic that made the original JPA consortium recommendation Raker-compatible for Hetch Hetchy-sourced compute. (Earlier drafting called this an "anchor offtaker" role for the CCSF consortium specifically; that framing is retired — see the correction note at the top of this file. The Raker-compatibility point stands independent of whether CCSF is sized to "anchor" anything.)

### 4.4 Climate-vision context (anchor-offtaker political thesis retired)

> [!warning] Correction, 2026-06-20
> Everything below this note is the original anchor-offtaker thesis, kept for the record. Per Jeremy's direction, it's retired: CCSF/consortium compute demand is wildly out of scale to position as anchoring a 1.6-2.6+ GW wind-and-transmission project. The "political value" points below — CalCompute positioning, the GovAI Coalition Summit pitch, federal-headwind insulation — were all built on that retired thesis and don't carry over on their own.
>
> **Corrected framing:** Humboldt offshore wind belongs in CCSF's planning materials as evidence that California's clean-power supply is scaling up dramatically this decade, in service of the state's and SF's broader climate and electrification goals — transportation electrification, building electrification, and AI/compute growth broadly, of which CCSF's own consortium is one small, non-defining part. That's a tailwind worth noting for future energy-sourcing conversations, not a structural pillar of the consortium's positioning. Separately: the GovAI Coalition Summit / Khaled Tawfik engagement referenced below is an AI-generated suggestion Jeremy has not evaluated or acted on, independent of the anchor-offtaker question.

~~This is the highest-leverage framing for CCSF positioning:~~

~~- **Currently:** The CAISO-approved transmission line has a defined supply (Humboldt wind) and a defined interconnection point (Collinsville), but no committed offtaker at consortium scale.~~
~~- **CCSF-led consortium as anchor offtaker:** Brings committed multi-decade municipal demand to a transmission project that needs demand justification to clear final investment. Similar to MGHPCC as anchor for Holyoke hydropower, or Empire AI as anchor for the NY State compute infrastructure.~~

~~The political value to CCSF:~~
~~1. Pulls CCSF from second-mover to first-mover in the California offshore-wind buildout — moves the consortium from "CalCompute parallel" to "CalCompute partner."~~
~~2. Aligns with CalCompute's statutory mission (Gov Code §11546.8). The CalCompute framework is due January 1, 2027. CCSF engaging CalCompute with an anchor-offtaker thesis gives the framework a concrete municipal demand profile to plan around.~~
~~3. Creates a GovAI Coalition narrative for the December 9-11, 2026 Summit: "California municipal consortium as anchor offtaker for state offshore wind buildout" is a recruiting pitch for founding consortium members.~~
~~4. Insulates CCSF from federal headwinds. The transmission approval is state-level (CAISO/CPUC). The federal funding cuts affect development pace, not project existence. A municipal consortium that anchors on the transmission creates a state-political coalition that survives federal turnover.~~

### 4.5 Timing alignment with CCSF milestones

*Table corrected 2026-06-20 — relevance ratings below were built on the now-retired anchor-offtaker thesis and GovAI/Khaled connection; see the correction note at the top of this file.*

| CCSF milestone | Date | Humboldt relevance, corrected |
|---|---|---|
| CleanPowerSF IRP filing | August 10, 2026 | Not in play — SFPUC engagement is long-term and this project will miss this filing entirely, independent of Humboldt |
| CalCompute framework | January 1, 2027 | Low — the anchor-offtaker input this row described is retired; CalCompute engagement stands on its own merits, not on a Humboldt thesis |
| GovAI Coalition Summit | December 9-11, 2026 | Not a Jeremy-adopted plan — the GovAI/Khaled connection is an unevaluated AI suggestion |
| CalCompute 14-member consortium convening | 2027 (post-deadline) | Relevant on its own terms — CCSF consortium participation in CalCompute doesn't depend on the Humboldt thesis |
| RWE Canopy commercial operation | Mid-2030s (uncertain) | Background context only — not something CCSF compute scaling is paced to or anchors |
| CAISO HVDC line in service | By June 1, 2034 (per CAISO schedule, §8 claim 2; corrected 2026-06-21 from "early 2030s") | Background context only — one data point among many for state clean-power supply, not a dependency for CCSF's buildout |

---

## 5. The consortium-side moves this implies

### 5.1 What CCSF should do now (1-3 retired, 2026-06-20; 4 stands)

1. ~~Engage CalCompute explicitly with the anchor-offtaker thesis.~~ **Retired** — the anchor-offtaker thesis is gone. CalCompute engagement may still make sense, but on its own merits (per the brief's §7.2/§8), not via a Humboldt framing.

2. ~~Add Humboldt offshore wind to the August 10, 2026 CleanPowerSF IRP conversation.~~ **Retired** — moot twice over: the anchor-offtaker thesis is gone, and SFPUC/IRP engagement won't happen in time for the August 10, 2026 filing regardless (this project's engagement is long-term, paced to SFPUC's own conservative process).

3. ~~Brief Khaled Tawfik (San José CIO, GovAI Coalition Board Chair) on the anchor-offtaker framing.~~ **Retired** — the GovAI Coalition / Khaled Tawfik connection is an AI-generated suggestion Jeremy has not evaluated or acted on, independent of the anchor-offtaker question.

4. **Engage CAISO through the consortium's governance** — stands as a generic, low-cost future step *if and when* a consortium actually forms; not a near-term action.

### 5.2 What the strategic brief needs

The current brief is energy-supply-thin: Section 2.5 (tier routing) and Section 5 (scaling analysis) are present, but the energy-supply question is largely deferred to the SFPUC deep-dive. The Humboldt offshore wind connection should be added as a brief-level finding — not buried in an appendix — because it changes the consortium's structural posture.

### 5.3 What the SFPUC deep-dive needs

Section 8 (three siting scenarios) and Section 10 (August 10 IRP window) cover SFPUC-controlled supply paths. A new section covering the Humboldt-to-Bay transmission line and offshore wind integration is needed for completeness. This file is the placeholder for that section.

---

## 6. Risks and unknowns

- **RWE Canopy cancellation risk.** RWE has not publicly cancelled, but the federal headwinds and 2025 industry-wide cancellations (over 20 GW halted nationally) make this a real possibility. CCSF consortium planning should be robust to "the Humboldt project never builds" — i.e., the consortium should still work on Sunol Valley owned generation + CleanPowerSF procurement + Sierra batch pod as the fallback stack.
- **CAISO transmission line schedule slip.** CAISO approval is durable, but construction has not begun. Realistic in-service is early 2030s; slip to late 2030s is plausible.
- **CalCompute framework doesn't include municipal tier.** If CalCompute's framework is university/research-anchored only (like Empire AI), the consortium has to operate as a separate entity and may lose political leverage. Engagement in the framework process is the mitigation.
- **Collinsville interconnect congestion.** The 1.6 GW line terminates at Collinsville, which serves PG&E's East Bay load and the broader Bay Area grid. Local congestion at Collinsville could constrain effective delivery to San Francisco load. PG&E's Bay Area transmission planning has not been deeply examined for this constraint.
- **Tribal and coastal community consultation.** The Humboldt lease areas, marine terminal, and subsea cable route all touch Wiyot, Yurok, and other tribal interests. CEQA and federal tribal consultation are real timelines; the 2026 RFP for the marine terminal suggests this is moving, but the subsea cable route itself has not publicly started formal consultation.
- **Raker Act application to imported power.** Raker Act §6 applies to Hetch Hetchy power specifically, not to imported grid power. CleanPowerSF already procures out-of-county power (Central Valley solar) and is Raker-compatible because the offtaker is municipal. Humboldt wind power imported via CAISO and procured through CleanPowerSF or a CC Power JPA joint solicitation follows the same logic — but City Attorney opinion required before any commitment.

---

## 7. Sources

### Offshore wind lease areas and CAISO transmission plan

- [BOEM California Activities](https://www.boem.gov/renewable-energy/state-activities/california-activities) — five lease areas, $757.1M high bids
- [BOEM California Lease Auction Announcement (DOI)](https://www.doi.gov/pressreleases/biden-harris-administration-announces-winners-california-offshore-wind-energy-auction)
- [North Coast Offshore Wind Project Timeline](https://www.northcoastoffshorewind.org/project-timeline) — Humboldt timeline and 25 GW state target
- [CA State Lands Commission Offshore Wind](https://www.slc.ca.gov/renewable-offshore-wind-energy/offshore-wind-energy-development/) — 373,268 acres, ~4.6 GW combined potential
- [RWE California offshore auction press release (Dec 7, 2022)](https://www.rwe.com/en/press/rwe-renewables/2022-12-07-california-offshore-auction/) — 63,338-acre Humboldt lease, ~1.6 GW, mid-2030s timeline
- [Equinor California offshore wind (Dec 7, 2022)](https://www.equinor.com/news/20221207-lease-california-floating-offshore-wind) — Morro Bay lease, ~2 GW, complement to Humboldt
- [Humboldt Bay Harbor Heavy Lift Marine Terminal](https://humboldtbay.org/humboldt-bay-offshore-wind-heavy-lift-marine-terminal-project-3) — June 24, 2026 RFQ meeting
- [CAISO 2023-2024 Transmission Plan (CPUC doc)](https://docs.cpuc.ca.gov/PublishedDocs/SupDoc/A2407018/9300/606807794.pdf) — 260-mile HVDC line, 1.6 GW, Humboldt to Collinsville
- [Downey Brand on CAISO North Coast transmission](https://www.downeybrand.com/legal-alerts/caiso-proposes-transmission-links-to-north-coast-offshore-wind-resources/) — 260-mile, 500 kV HVDC to Collinsville 500 kV substation
- [CAISO approves 2023-24 Transmission Plan (Offshorewind.biz)](https://www.offshorewind.biz/2024/05/24/california-iso-greenlights-transmission-plan-for-offshore-wind-integration/) — May 23, 2024 provisional approval
- [Offshore Wind California — coalition tracker](https://www.offshorewindca.org/) — state-level project status

### Federal headwinds and project delays

- [Trump Administration Rescinds Offshore Wind Project Areas (Lost Coast Outpost, July 31, 2025)](https://lostcoastoutpost.com/2025/jul/31/boem-rescinds-lease-areas/) — existing Humboldt leases likely unaffected
- [Northern California offshore wind project loses $427M (Silicon Valley, Sept 2025)](https://www.siliconvalley.com/2025/09/02/trump-administration-cancels-nearly-half-a-billion-dollars-for-northern-california-offshore-wind-project/)
- [Federal Offshore Wind Deployment Tracker (Harvard EELP)](https://eelp.law.harvard.edu/tracker/federal-offshore-wind-deployment/) — Dec 22, 2025 East Coast lease pause
- [California Reaffirms 25 GW Offshore Wind Target (Offshorewind.biz, May 25, 2026)](https://www.offshorewind.biz/2026/05/25/california-reaffirms-25-gw-offshore-wind-target-for-2045/)

### Related infrastructure

- [Trans Bay Cable (existing SF-to-Pittsburg HVDC, 400 MW)](https://www.transbaycable.com/operations.html) — separate asset, not part of the new Humboldt line

---

## 8. Verification log

*[Hermes Agent · minimax-m3 · 2026-06-20]*

| # | Claim | Status | Date-of-source | Notes |
|---|---|---|---|---|
| 1 | BOEM Humboldt lease areas: RWE Canopy, ~1.6 GW on 63,338 acres (OCS-P 0561) | confirmed | 2026-04-27 | CA State Lands Commission lease table confirms 63,338 acres; RWE press release confirms ~1.6 GW; BOEM shows current holder as "Canopy Offshore Wind, LLC" (RWE subsidiary). Humboldt leases intact. Central Coast lease OCS-P 0564 (Golden State Wind) separately pending cancellation per Apr 27, 2026 DOI settlement — does not affect Humboldt. |
| 2 | CAISO 2023-2024 Transmission Plan — May 23, 2024 provisional approval; 260-mi 500 kV HVDC Humboldt→Collinsville; 1.6 GW | confirmed | 2024-05-23 | North Coast Offshore Wind timeline confirms "May 23, 2024: CAISO Board approved 2023-2024 Transmission Plan." Downey Brand (Apr 3, 2024) describes 260-mi 500 kV HVDC Humboldt→Collinsville. **New spec also includes parallel 140-mi 500 kV AC Humboldt→Fern Road line** — not in current file. In-service target: by June 1, 2034 per CAISO schedule. |
| 3 | Humboldt Bay Heavy Lift Marine Terminal RFQ — June 24, 2026 board meeting | unverifiable | 2026-06-20 | Could not confirm specific June 24, 2026 board meeting via web search. Harbor District page mentions May 6, 2026 Development Association agenda; North Coast Offshore Wind timeline lists "August 2026: Recirculate NOP" as next milestone. Project on pause since Aug 29, 2025 federal grant withdrawal; Harbor District seeking alternative funding. |
| 4 | California 25 GW by 2045 reaffirmation (May 2026) | confirmed | 2026-05-25 | Offshore Wind Biz article (May 25, 2026, Adrijana Buljan) reports CEC Chair David Hochschild at 2026 Pacific Offshore Wind Summit (May 18-20, Long Beach) reiterating 25 GW by 2045. **Additional: Prop 4 authorizes $475M for port upgrades; CEC has allocated $42.75M to Port of Humboldt + 4 other ports.** |
| 5 | RWE Canopy timeline — "mid-2030s contingent on permitting" | confirmed (with caveat) | 2024-01-09 | RWE press releases (2022-12-07, 2024-01-09) consistently state "mid-2030s, contingent on permitting." North Coast Offshore Wind timeline: "Mid-2030s: RWE anticipates in-water construction." No public move earlier. **Caveat:** Marine terminal federal funding cut (Aug 29, 2025) means staging infrastructure is delayed; "mid-2030s" may now slip. |
| 6 | September 2025 $427M federal funding cut to Northern California offshore wind | drifted (minor) | 2025-08-29 | Wind file dates this "September 2025"; actual grant withdrawal was **August 29, 2025** (North Coast Offshore Wind timeline), publicly reported Sept 2-3, 2025 (Silicon Valley, Paul Rogers). Amount: $426,719,810 (≈$427M, rounds correctly). Action by USDOT under Sec. Sean Duffy. |
| 7 | December 22, 2025 East Coast lease pause scope | confirmed | 2025-12-22 | Harvard EELP tracker: "Dec. 22, 2025: Trump administration paused leases for five large-scale offshore wind projects off the East Coast." Scope: East Coast only — Humboldt leases unaffected. **Additional context:** Federal court vacated agencies' resulting pause in wind authorizations (Dec 8, 2025); Trump admin voluntarily dismissed appeal (June 10, 2026). Apr 27, 2026 DOI settlement agreements added Golden State Wind (off CA coast) to cancellation list — distinct from East Coast pause. |
| 8 | Collinsville 500 kV substation — current PG&E interconnect status | confirmed (active) | 2026-06-20 | Multiple sources confirm active project: CAISO Project Sponsor Selection Report exists; CPUC CEQAnet 2025010149 active; FERC granted PG&E incentives; WECC 2026 Annual Progress Report lists "Collinsville 500/230 kV Substation Project" under LSPGCA. This is the receiving substation for the Humboldt HVDC line; being built separately. |

**Verification summary:** 6 confirmed (with caveats on #5, #6), 1 drifted (date-precision on #6), 1 unverifiable (specific date on #3). No claims superseded.

**Most material finding for Phase 2 (Sonnet brief integration):** The CAISO-approved transmission plan includes a **second 140-mi 500 kV AC line from Humboldt substation to Fern Road substation** (Downey Brand, Apr 3, 2024) that the current wind file does not mention. The wind file's "1.6 GW" capacity claim refers specifically to the HVDC line; the AC line adds redundancy/additional capacity. Phase 2's anchor-offtaker thesis subsection should reference the full transmission scope, not just the HVDC element.

**Drift flag for Phase 2:** The Aug 29, 2025 grant withdrawal date (not "September 2025") is a date-precision correction. The anchor-offtaker framing is materially unchanged.

**Existing source URL resolutions:** All URLs cited in section 7 still resolve as of 2026-06-20.

### Reconciliation pass (2026-06-20) — re-stated and added claims

*(Table structure repaired 2026-06-21: the rows below were previously orphaned from any header row by the intervening summary prose, so they rendered as broken markdown in Obsidian. Re-headed here; row content unchanged.)*

| # | Claim | Status | Date-of-source | Notes |
|---|---|---|---|---|
| 1 (rev.) | BOEM Humboldt lease areas: OCS-P 0561 (RWE Canopy), ~1.6 GW on 63,338 acres | confirmed | 2026-04-27 | CA State Lands Commission lease table confirms 63,338 acres; RWE press release confirms ~1.6 GW; BOEM shows current holder as "Canopy Offshore Wind, LLC" (RWE subsidiary). Humboldt leases intact. Central Coast lease OCS-P 0564 (Golden State Wind) separately pending cancellation per Apr 27, 2026 DOI settlement — does not affect Humboldt. **Note:** §2.1 of this file had a framing drift (treated 1.6 GW as the *combined* Humboldt figure); corrected 2026-06-20 to show OCS-P 0561 alone with OCS-P 0562 (California North Floating / CIP, ~1 GW) as separate. |
| 9 | OCS-P 0562 (California North Floating LLC / CIP / Vineyard Offshore), ~1 GW on 69,031 acres | confirmed | 2026-06-20 | Verified against Spinergie coverage of the Dec 2022 auction reporting and CA State Lands Commission lease table. $173.8M bid; lease signed June 2023. Combined Humboldt lease potential ~2.6+ GW, exceeding the 1.6 GW HVDC line capacity — transmission-headroom gap if OCS-P 0562 develops on a similar timeline to OCS-P 0561. |
| 10 | §2.1 framing — combined Humboldt figure presented as ~1.6 GW | drifted → corrected | 2026-06-20 | Phase 3 (Sonnet, 2026-06-20) flagged that §2.1 conflated OCS-P 0561's ~1.6 GW capacity with the combined Humboldt lease total. Wind file §2.1 rewritten 2026-06-20 to list both leases separately and note the transmission-headroom gap explicitly. SFPUC deep-dive §9.5.1 also has the corrected framing. |
| 11 | §4.1 sizing math — "1.6 GW HVDC line is sized almost exactly to consortium-scale load" | drifted → corrected | 2026-06-20 | Phase 2 (Sonnet, 2026-06-20) caught the error against brief §3.6 scaling table: at 50K–150K workers the IT load is 3–15 MW (sub-linear, not linear). 1.6 GW HVDC dwarfs consortium demand by 50–500x. Strategic brief §7.6 already uses the corrected framing ("energy supply is not the binding constraint"). Wind file §4.1 rewritten 2026-06-20 to match. |

**Cumulative verification status:** 9 confirmed, 3 drifted (2 now corrected in source, 1 minor date-precision on #6), 1 unverifiable (#3 — specific June 24, 2026 RFQ meeting date).

**Net effect on Phase 2/3 outputs:** Both Sonnet sessions independently caught one drift each (Phase 3: §2.1; Phase 2: §4.1) and self-corrected in their respective output documents. Source wind file now matches.

*Document version: 2026-06-20 (with §8 verification log + §2.1/§4.1 corrections; folded into the strategic brief §7.6 and SFPUC deep-dive §9.5 same day). Anchor-offtaker thesis retired and GovAI/Khaled connection flagged as unevaluated per Jeremy's correction, 2026-06-20 — see warning note at top of file.*

<!-- END FULL DOCUMENT: CCSF_humboldt_offshore_wind_transmission.md -->

## Technical detail

All technical detail is contained in the two complete documents above. The most decision-relevant design distinctions are:

- Reclaimed water belongs at heat rejection or in a suitably treated facility loop, never directly in the chip-side loop.
- The deep dive proposes dry-cooler-first operation with wet trim as a climate-specific hypothesis for San Francisco; it is not a site design and requires current engineering validation.
- The Southeast Plant currently lacks the complete Title 22 tertiary treatment and distribution path assumed for cooling-tower service in the concept.
- Public-land generation is a portfolio of dated proposals and operating assets, not one ready project. Solar, storage, and small-hydro status must remain site-specific.
- CAISO's approved Humboldt delivery plan and the separate Schatz subsea concept are different topologies with different maturity, capacity, and approval status.
- Flexible compute can be studied as controllable demand, but no flexibility or grid benefit is established without measured workload and load-shape evidence.

## Public sources

The full source bibliographies and useful locators are preserved inside each complete document. The sources most important to the conflicts and freshness boundaries are:

| Source title | Publisher or author | Publication date | URL and useful locator | Claim or finding supported | Verified date |
|---|---|---|---|---|---|
| 2023–2024 Transmission Plan | California Independent System Operator | 2024 | https://www.caiso.com/documents/iso-board-approved-2023-2024-transmission-plan.pdf | Approved Humboldt transmission topology, initial capacity, and planning schedule | 2026-08-16 correction pass |
| Humboldt–San Francisco Bay Subsea Transmission Cable Conceptual Assessment | Schatz Energy Research Center | 2020 | https://schatzcenter.org/pubs/2020-OSW-R5.pdf | Separate pre-feasibility subsea concept, approximate 1.8 GW per cable bundle, and separated-route redundancy | 2026-08-05 synthesis pass |
| AB 525 Offshore Wind Energy Strategic Plan | California Energy Commission | current plan page | https://www.energy.ca.gov/data-reports/reports/ab-525-reports/offshore-renewable-energy | State offshore-wind planning target and integrated planning context | 2026-08-05 synthesis pass |
| Local Build-out of Energy Resources for Community Choice Aggregation | SF LAFCo; EnerNex and Willdan | 2015 | Full citation and related public packet links in document 1, §§3, 5, and 13 | Dated Sunol, other public-land solar, and small-hydro concepts | source-specific dates preserved in document 1 |
| California Code of Regulations, Title 22, recycled-water criteria | State of California | current regulation cited in document | Full citation in document 1, §§7 and 13 | Treatment standard cited for recycled water used in cooling towers | source-specific date preserved in document 1 |

## Alternatives and conflicting evidence

- **Approved transmission versus subsea concept:** the current correction of record says the CAISO-approved Humboldt delivery path is overland: an approximately 260-mile Humboldt–Collinsville line planned for eventual HVDC but initially operated as 500 kV AC, plus an approximately 140-mile 500 kV AC line to Fern Road, enabling an initial ~1.6 GW with a 2034 planning in-service year. The full historical documents still contain older statements calling the approved path a subsea or 500 kV HVDC line. Those statements are retained as correction history and must not control.
- **Offshore-wind capacity:** ~1.6 GW describes OCS-P 0561 and the initial approved delivery scope, not the combined Humboldt lease potential. The two leases total roughly ~2.6+ GW in the source treatment. California's 25 GW by 2045 planning goal is a separate statewide target. These figures are not interchangeable.
- **Sunol Valley solar and storage:** the 2015 concept was 17.5 MW on about 100 acres; the 2020 treatment examined roughly 40 MW solar plus storage at the closed 280-acre golf course. The source finds no RFP or evidence that the larger concept advanced past evaluation. It is a candidate or historical concept, not an operating or committed project.
- **Sunol and University Mound small hydro:** a 2014–2015 source described 1 MW and 240 kW projects as “under development,” but the 2026 source review found no public evidence of operation. A current “Sunol 1.1 MW” reference concerns solar photovoltaic generation at the water treatment plant, not hydro. The packet does not resolve the projects' ultimate disposition.
- **Energy-share figures:** the work-side `CCSF_ai_energy_water_evidence_2026-08-11.md` was not present in `jp-sfgov/sfgov-cleared-research-export` at the time of preparation. Any Berkeley Lab or LBNL energy-share figures on the work side therefore remain unreconciled with this packet and must be compared explicitly on receipt.
- **Cooling architecture:** all-evaporative, hybrid dry/wet, and dry-cooler-first designs trade water consumption, energy, cost, peak-weather performance, and siting constraints differently. The deep dive's preferred architecture is analysis, not an approved engineering design.

## Caveats and unresolved questions

- The full documents contain dated infrastructure status, cost, rate, schedule, regulatory, and capacity claims. Their citations and verification notes are preserved, but the packet preparation did not make every claim current to August 16, 2026.
- The wind document's top-level August 16 correction governs older conflicting body text. The conflict is deliberately visible and requires careful destination integration.
- No current public evidence in the reviewed personal corpus establishes that the Sunol Valley solar-plus-storage concept, Sunol small hydro, or University Mound small hydro is operating or committed.
- The technical and legal feasibility of reclaimed water depends on site, treatment, distribution, water quality, permitting, cooling design, and current Title 22 requirements.
- No site-specific load trace, utility study, interconnection study, environmental review, rate analysis, engineering design, community process, or capital estimate authorizes implementation.
- The receiving side must reconcile this packet against its newer evidence file and any stronger work-side canon before adopting figures.

## Corrections and freshness triggers

The packet preserves the source documents' complete correction history. Reverify when CAISO changes the Humboldt topology, operating-voltage plan, capacity, route, cost, or in-service date; BOEM lease ownership or capacity changes; Schatz or another engineering body updates the subsea concept; SFPUC publishes a current Sunol or small-hydro disposition; recycled-water treatment or Title 22 requirements change; the Southeast Plant treatment scope changes; or a candidate site and cooling design are selected.

Do not propagate the obsolete claim that CAISO approved a Humboldt-to-Bay subsea HVDC route. Do not describe the 1 MW Sunol small-hydro proposal as operating. Do not describe the 2020 Sunol solar-plus-storage evaluation as an approved project. Do not select an LBNL energy-share figure until the missing work-side evidence document is available and the two treatments are reconciled.

## Integration guidance

Use the two documents as correction-aware source material for the personal vision piece and for destination-native evidence documents. Preserve work-side material that is stronger, newer, or better sourced. Keep these distinctions explicit:

1. The nine-point public-post spine is an outline, not the evidence base.
2. Reclaimed-water cooling, public-land generation/storage, and offshore-wind transmission are three separate propositions with different maturity and decision owners.
3. Compute is a small, flexible potential beneficiary; it does not anchor the offshore-wind or transmission buildout.
4. The approved overland CAISO topology must remain separate from the speculative redundant-subsea vision.
5. Historic proposals, current assets, and recommended future studies must not be collapsed into one status category.

The receiving agent should compare the full documents with `CCSF_ai_energy_water_evidence_2026-08-11.md` once that file is available, record any figure conflict rather than silently choosing one, and update its native evidence ledger or reconciliation manifest only after the separate integration gate.

## Exclusions and disclosure boundary

Excluded: raw research scratchpads; daily-intel and newsletter intake; session transcripts and session state; credentials; repository history; personal runtime information; material carrying the restricted personal-audience marker; Level 3–5 City data; private City records; and the contents of any work-side private repository. Named Department of Technology staff were removed from the shared copy under the approved transform. Public officials, organizations, and correction subjects already present in public-source analysis were otherwise retained.

The broader strategic brief was not bundled because most of it is outside this topic, its August carbon/grid/community delta already has a separate packet, and including the whole document would add unrelated third-party and governance material without improving this source packet. The already-exported brainstorm direct update was not duplicated. The missing work-side energy/water evidence document could not be pulled because it is absent from the work-owned public export.

## Closeout

- **Public export commit:** `662dfc1307edab3168ed9c7970ce800d45cfcbae` (initial publication; clearance-metadata correction pending)
- **Destination content commit or commits:** pending separate integration review and approval
- **Ledger or manifest commit:** pending separate integration review and approval
- **Unresolved differences:** work-side LBNL energy-share figures unavailable; work-side treatment of Humboldt capacity and Sunol status not directly inspectable; source documents retain visible corrected historical claims

## Completion checklist

- [x] The receiving agent can understand, verify, and integrate the cleared research without access to the originating private files.
- [x] All eligible substantive detail, links, context, reasoning, caveats, corrections, and provenance were preserved.
- [x] Facts, analysis, inference, and recommendations are distinguishable.
- [x] Every decisive claim is traceable to a public source or explicitly identified reasoning.
- [x] Raw intake and private, restricted, or otherwise ineligible context were excluded.
- [x] Safe source and destination commits are recorded.
- [x] Jeremy reviewed the exact public diff and affirmatively cleared it for public disclosure.
