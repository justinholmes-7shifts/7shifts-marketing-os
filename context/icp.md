# Ideal Customer Profile

> Who we sell to, and how hard we lean in by segment. Pull this into any task that touches targeting, segmentation, campaign planning, or research. When the ICP shifts, this is the one file to change. Personas mapped in [`personas.md`](personas.md).

## The canonical ICP (from the messaging guide)

North American QSR, FSR, and franchised restaurants with **16-75 employees per location, up to 20 locations**, on a **cloud-supported POS**, looking to consolidate workforce/labor management into one app.

The sharpest version: an operator running **2-5 full-service locations with 30+ employees per unit**, replacing manual systems (Excel, whiteboards, pen and paper) with a purpose-built platform for scheduling, payroll, and labor management.

## Segmentation (Best → Not a fit)

| Segment | Definition | 7shifts customers | Market size | Penetration | GTM motion |
|---|---|---|---|---|---|
| **1. FSR Scale** ⭐ Best Fit | 2-5 locations, full-service, 30+ employees/loc | 6.8K locs | ~50K locs | 13% | **Prioritize** across marketing, sales, and product. Drive volume and conversion. |
| **2. Multi-Loc** — Strong Fit | 2-5 locations, any service type, 15+ employees/loc (excl. 30+ FSR) | 4.8K locs | ~60K locs | 8% | Nurture via targeted digital + content. Position as the next logical step up from simpler tools. |
| **3. Single Loc** — Emerging Fit | Single location, any service type, 15+ employees/loc | 21.1K locs | ~245K locs | 8% | Low-friction self-serve PLG to fuel adoption and future multi-location expansion + referrals. |
| **4. Franchise Multi-Loc** — Selective Fit | 6-15 locations, QSR franchise groups, or low-customization groups | 2.6K locs | ~20K locs | 13% | Selective outbound with QSR-workflow playbooks. |
| **Neutral / Not a fit** | Single loc with ≤14 employees · non-restaurants · multi-loc/enterprise needing high customization · groups with 16+ corporate stores | — | — | — | — |

**Read the penetration numbers:** FSR Scale and Franchise are already at 13% (proven, defend and grow). Multi-Loc and Single Loc sit at 8% with the largest headroom (Single Loc alone is a ~245K-location market). Single Loc is where PLG volume lives; FSR Scale is where the highest-value, best-fit revenue lives.

## Market sizing (DataLane, May 2026)

A more current and analytical cut than the segment table above. Source: DataLane pull 2026-05-20, scoped to 1-100 location groups (franchise / 100+ excluded). The segment table is the strategic view (fit tiers + GTM motion); this is the raw TAM/SAM by group size. Note they use different cuts: the segment table keys on service type and employees/location, these bands key on group size only.

**The answer first:** we've barely scratched the SMB market. Penetration climbs steeply with group size, so we're far better at winning multi-location groups than single independents. But even where group penetration is high, we win only a fraction of each group's locations.

- **1-100 location SAM: ~793K groups / ~945K locations.** Matched to ~2.3% of groups and 2.8% of locations.
- **The structural insight:** in the 51-100 band we're in **36% of groups but only 5.7% of their locations.** When we win a group, we win a slice of it. That within-group whitespace is the single biggest expansion opportunity.

| Band | Groups | Locations | Group pen. | Loc pen. |
|---|---:|---:|---:|---:|
| 1 (single) | 743,422 | 743,422 | 1.9% | 1.9% |
| 2-5 | 43,598 | 107,254 | 7.8% | 5.6% |
| 6-10 | 3,372 | 24,903 | 16.8% | 9.0% |
| 11-25 | 1,612 | 25,210 | 20.9% | 8.2% |
| 26-50 | 570 | 20,246 | 29.8% | 7.0% |
| 51-100 | 336 | 24,011 | 36.0% | 5.7% |

**Caveats, read before quoting:**
1. ~40% of customers don't map to DataLane, so every penetration figure is understated. True penetration is likely ~1.5x these numbers.
2. ~42% of file rows have a blank location count and were excluded, so single-location TAM is understated (real number is larger than 743K).
3. DataLane counts whole-system locations for big brands (Jimmy John's = 2,794, etc.), which land in the out-of-scope 100+ bands.
4. Mid-Market and franchise TAM are separate pulls, not in this data.

## Who cares a lot

North American SMB restaurants, 16-75 employees/location, up to 20 locations:
- **Type:** FSR + QSR (full-service is where scheduling complexity, labor cost, and compliance risk peak, so the pull is strongest)
- **POS:** cloud-supported
- **Payroll:** on a supported integration, or looking to switch
- **Structure:** independently owned, corporate, or franchise groups

## Buying roles

- **Economic buyer — Owner/Operator:** profitability, labor cost, turnover, compliance.
- **Primary user / champion — General Manager:** scheduling, swaps, labor budgets, team comms.
- **End user — hourly employee:** mobile app for schedules, availability, swaps, clock-in/out.

A deal needs the buyer (ROI) and the user (daily ease) both. See the persona-to-segment map in [`personas.md`](personas.md).

## Core pain points (what they came to solve)

- Spending too much time managing schedules, payroll, and tips across different systems
- Expensive, disconnected tech stack
- Rising labor, food, and operating costs
- Finding and retaining employees
- Too much manual work, not enough automation
- Hard to forecast sales and labor to make informed decisions
- Overwhelming time-off and availability requests, and the schedule changes they trigger
- Without POS + payroll integration, no data for payroll, so manual entry eats ~45 min a pay run
- Tedious, error-prone tip calculation and distribution
