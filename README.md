# RootNet Research Series: v5.8.0 to v6.7

**Status date:** 2026-08-21  
**Latest packaged assay:** v6.7 causal-separation development assay  
**Latest completed confirmatory evaluation:** v6.6 r2 rotation-equivalence audit  
**Frozen ecological baseline:** v5.8.0

## Read This First

RootNet is now a **series of related but distinct artificial-ecosystem models**. A higher version number does not always mean that the earlier model has simply been replaced.

There are two research lines:

```text
v5.8.0  frozen ecological transport baseline

v6.0  evolutionary kernel
  └─▶ v6.1  persistent spatial mycelium
        └─▶ v6.2  local module metabolism and partial necrosis
              └─▶ v6.2.1  calibrated patch and observer pacing
                    └─▶ v6.3  preregistered transport comparison
                          └─▶ v6.4  fixed versus adaptive conductance
                                └─▶ v6.5  dynamic-environment comparison
                                      └─▶ v6.6  continuous coordinates and rotation audit
                                            └─▶ v6.7  water-field/necrosis cause separation
```

- **v5.8.0 remains the reference for the original carbon/water/nitrogen transport ON/OFF and drought results.**
- **v6.0 starts a separate model line** from a common ancestral population. It is not an in-place upgrade of v5.8.0.
- **v6.1 through v6.2.1 progressively add a persistent spatial body, local metabolism, partial necrosis, and fragment identity.** Their fixed-seed runs are mechanism validations, not replicated biological findings.
- **v6.3 is the completed transport-presence experiment**, derived from v6.2.1. It tests three resource-translocation rules.
- **v6.4 and v6.5 test whether history-dependent adaptive conductance adds a detectable benefit over fixed conductance.** v6.4 found no clear difference in the normal artificial environment. v6.5 also found no clear difference across its dynamic environments, but its formal status is `COMPLETED_WITH_PROTOCOL_DEVIATION` because 13 early-extinction runs were not padded with zeros through tick 360 in one endpoint calculation.
- **v6.6 is a continuous-coordinate engineering audit.** Its three primary geometric endpoints passed all 24 preregistered rotation-equivalence comparisons, but 274/300 runs became extinct before tick 360 and active-patch uptake occurred in only 10/300 runs. Rotation equivalence is not evidence of ecological health.
- **v6.7 is a completed 160-run development assay, not a confirmatory evaluation.** It classified the v6.6 water field as the dominant tested cause of the observed collapse. Its sealed result is retained as a reference-runtime result; cross-platform portability of its byte-exact dynamic-state digest remains unresolved.

All versions are artificial systems. None is calibrated to predict a real fungal species, forest, mycorrhizal network, or evolutionary history.

---

## Version Map

| Version | Role | Main biological unit | Resource representation | Evidence status |
|---|---|---|---|---|
| **v5.8.0** | Frozen ecological transport baseline | Predefined `fungus`, `alga`, and `symbiotic` individuals | Individual carbon, water, and nitrogen pools; conservative transfer between connected individuals | Replicated ON/OFF and drought experiments completed |
| **v6.0** | Minimal evolutionary kernel | Organisms in non-overlapping generations | Inherited traits, energy acquisition, costs, sharing, mutation, and dispersal | Apparatus mechanically validated; no sealed replicated diversification result |
| **v6.1** | Persistent spatial mycelium | Colony made of cells, tips, and edges | Uptake is spatial, but energy and water are pooled at colony level | Deterministic mechanism validation only |
| **v6.2** | Local module metabolism | Module, ramet, genet, and lineage | Local energy, water, vitality, starvation, fixed-conductance transfer, necrosis, and detritus | Deterministic mechanism validation only |
| **v6.2.1** | Patch to v6.2 | Same as v6.2 | Same transport/death framework, with reduced post-extension water reserve and event-paced display | Calibration and observer-usability validation; seed 620 is not an evaluation seed |
| **v6.3** | Paired transport experiment | Same as v6.2.1 | `none`, `equalize`, and tip-oriented `demand` transport | Preregistered 30-seed paired evaluation completed; both transport conditions classified `SUPPORTED` against `none` |
| **v6.4 r2** | Adaptive-conductance comparison | Same module/ramet/genet system as v6.3 | Fixed equalization versus history-dependent edge-conductance allocation | Preregistered 30-seed, 90-run evaluation completed; both primary comparisons were `NO_CLEAR_DIFFERENCE` |
| **v6.5 r2** | Dynamic-environment stress test | Same core body and transport network as v6.4 | Fixed versus adaptive conductance under four environmental schedules | 240-run evaluation completed with a protocol deviation; all eight primary comparisons remained `NO_CLEAR_DIFFERENCE` in the prespecified analysis and zero-padded sensitivity analysis |
| **v6.6 r2** | Continuous-coordinate rotation audit | Modules and edges in continuous 2-D coordinates | Euclidean geometry, bilinear field coupling, and fixed/adaptive transport | 300-run confirmatory engineering audit completed; 24/24 primary rotation comparisons were equivalent within ±5%, but the assay showed severe ecological collapse |
| **v6.7** | Causal-separation development assay | Same continuous-coordinate system as v6.6 | Two water fields crossed with immediate versus 5-tick-delayed necrosis response | 160 development runs completed; `WATER_FIELD_DOMINANT` in the sealed reference runtime; no v6.7 confirmatory evaluation was designed or run |

### Which version should I use?

- Use **v5.8.0** to reproduce the original ecological transport and drought study.
- Use **v6.0** to inspect the deliberately minimal evolutionary kernel.
- Use **v6.1** to observe persistent colonies with overlapping parent and offspring lifetimes.
- Use **v6.2.1** rather than v6.2 for the patched local-metabolism demonstration.
- Use **v6.3** to reproduce or inspect the completed network-translocation comparison.
- Use **v6.4 r2** to inspect the normal-environment fixed-versus-adaptive conductance comparison.
- Use **v6.5 r2** to inspect the dynamic-environment comparison, while retaining its protocol-deviation label.
- Use **v6.6 r2** to audit continuous-coordinate rotation equivalence, not as evidence that the ecological balance or nutrient-patch assay is healthy.
- Use **v6.7** to inspect the completed water-field/necrosis development diagnosis. Do not treat its diagnostic water field as a final model choice or its development seeds as confirmatory evidence.

Results and counts should not be compared across versions as though only one parameter changed. The models change their life cycle, biological unit, resource accounting, death definitions, and research question.

### Numerical portability and operating-system differences

RootNet uses floating-point geometry and math-library operations. From v6.4 onward, audits showed that a full raw simulation-state JSON can produce a different byte-level SHA-256 digest on another operating system or Python build even when the package files themselves are unchanged. In the v6.7 audit, Windows 11 runs with CPython 3.13.5 and 3.14.5 reproduced the sealed digest, while another Python 3.13.5 platform produced a different digest. The Python version number alone therefore does not define an equivalent numerical runtime; the OS, Python build, and underlying math library can matter.

Interpret verification outputs separately:

- **Artifact integrity:** ZIP, manifest, source, protocol, seed-list, and result-file hashes must match exactly on every OS. A mismatch here can indicate a changed or damaged artifact.
- **Mechanical and numerical validation:** unit tests, conservation laws, event/accounting checks, and float comparisons should use their stated tolerances.
- **Reference-runtime replay:** an exact full-state digest is guaranteed only for the declared reference runtime. A different digest elsewhere is a portability warning, not by itself proof of package corruption or scientific falsification.

A portability warning is not automatically harmless either. If the claim depends on cross-platform replay, compare discrete IDs, events, counts, and topology exactly; compare continuous values with prespecified tolerances; and classify any discrete trajectory divergence separately from harmless last-bit numerical drift.

For exact sealed replay, use the runtime declared by the package. The reference policy prepared for the next package is **Windows 11 x86-64 with CPython 3.14.5**. Other platforms may run the model, but byte-exact dynamic-state reproduction is not promised. v6.7 should currently be reported as:

> `WATER_FIELD_DOMINANT — sealed reference-runtime result; cross-platform portability audit pending`

This qualification does not erase the sealed Windows result. It limits the claim about cross-platform replay until the full assay is independently rerun or compared semantically on another platform.

---

## What v6.3 Established

v6.3 asked a narrow question:

> In the tested artificial environment, does mass-conserving resource translocation over the existing hyphal graph contribute to persistent growth and spatial exploration?

Thirty previously unobserved deterministic seeds were paired across three conditions for 360 ticks each. Seed 620, which had already been used during development, was excluded.

| Endpoint, median across runs | No transport | Equalization transport | Demand transport |
|---|---:|---:|---:|
| Living-module tick average | 7.50 | 22.50 | 23.01 |
| Distinct cells ever occupied | 12.0 | 38.5 | 54.5 |
| Ticks with extension | 2.22% | 7.22% | 11.94% |
| Longest extension-free interval | 128.0 | 60.0 | 77.5 |
| Total extensions | 10.5 | 34.5 | 50.5 |
| Necrosis per 100 extensions | 40.00 | 25.95 | 20.59 |
| Final living modules | 9.0 | 30.0 | 45.0 |

The preregistered rule classified both `equalize` and `demand` as **`SUPPORTED` relative to `none`**.

- `equalize` improved mean living modules and explored cells in 30/30 paired runs. Growth-tick fraction was favorable in 28/29 non-tied pairs. Its longest-gap result did not remain significant after correction.
- `demand` improved mean living modules in 30/30 pairs, explored cells in 28/28 non-tied pairs, growth-tick fraction in 28/30 pairs, and longest growth gap in 27/30 pairs.
- Whole-ecosystem extinction was 0/30 in every condition.
- Maximum observed absolute balance error was `3.55e-15` for energy and `4.44e-16` for water.

The supported interpretation is:

> In this RootNet environment, conservative resource translocation over the hyphal network strongly supports sustained growth and spatial exploration.

The result does **not** show that transport is necessary for survival. The no-transport condition retained the graph itself, and all no-transport ecosystems survived. It also does not establish `demand` as universally superior to `equalize`; their direct comparison was secondary, post hoc, and mixed by endpoint.

---

## What v6.4 Established

v6.4 r2 asked whether history-dependent allocation of a fixed total edge-conductance budget improves on uniform fixed conductance in the normal artificial environment. It compared `adaptive-equalize` with `fixed-equalize`; `none` was retained only as context.

Thirty new paired evaluation seeds were run in three conditions for 360 ticks, giving 90 complete runs. The two preregistered primary comparisons were:

| Adaptive minus fixed | Median paired difference | Holm-adjusted p-value | Classification |
|---|---:|---:|---|
| Mean living modules | −0.198611111 | 0.855535552 | `NO_CLEAR_DIFFERENCE` |
| Newly occupied cells | +0.5 | 0.848712444 | `NO_CLEAR_DIFFERENCE` |

All three conditions had 0/30 ecosystem extinctions. Resource-conservation and conductance-budget errors remained within tolerance.

The bounded result is that adaptive conductance was not clearly better or worse than fixed uniform allocation under this tested normal environment. This is a valid negative result; it does not show that adaptive conductance can never matter under other environmental schedules or damage regimes.

---

## What v6.5 Established

v6.5 r2 retained the v6.4 conductance rules and compared `fixed-equalize` with `adaptive-equalize` under four schedules: a long-term fixed patch, a slowly moving patch, an abrupt relocation, and environmental edge damage. The design used 30 new paired seeds, two transport conditions, and four environments, for 240 runs and eight preregistered primary comparisons.

All eight comparisons were `NO_CLEAR_DIFFERENCE`. One unadjusted fixed-patch uptake comparison had `p = 0.0428`, but its Holm-adjusted value was `p = 0.342`, so it did not support a benefit. The maximum recorded conservation error was at most `1.42e-14`.

The formal status is **`COMPLETED_WITH_PROTOCOL_DEVIATION`**. Thirteen runs ended early in ecosystem extinction, and mean living modules after extinction were not padded with zeros through tick 360 as the protocol required. A post hoc sensitivity analysis with zero padding left all eight classifications at `NO_CLEAR_DIFFERENCE`. That supports robustness of the qualitative observation but does not erase the deviation.

The abrupt-relocation uptake endpoint was also weak: fixed had no new-patch uptake in 27/30 runs, adaptive in 25/30, and 23 pairs tied. The experiment therefore did not establish adaptive conductance as either a benefit or a protective reserve under the tested schedules. The 30 evaluation seeds are used and frozen; a corrected confirmatory test would require a new version and new seeds.

---

## What v6.6 Established and Exposed

v6.6 r2 changed the spatial representation to continuous two-dimensional coordinates while preserving the ecological rules. It added Euclidean edge lengths, continuous spatial indexing, bilinear environmental-field coupling, arbitrary-angle rotation, and a circular evaluation region within the square arena.

Thirty locked evaluation seeds were run across five angles and two transport modes, for 300/300 completed records. For the three primary endpoints—living modules, total network length, and convex-hull area—all 24 preregistered comparisons against 0° were classified `EQUIVALENT_WITHIN_5_PERCENT`. This is a successful **engineering rotation-equivalence audit**.

It is not a successful ecological-health demonstration:

- 274/300 runs, or 91.3%, became extinct before tick 360;
- active-patch substrate uptake was positive in only 10/300 runs;
- all ten positive observations came from the same evaluation seed across two transport modes and five angles;
- the active-patch endpoint was auxiliary and was not used to produce the primary rotation verdict.

Accordingly, v6.6 supports the narrow claim that the tested geometric outputs were stable under rotation. It does not support the claim that nutrient exploration, survival balance, or the overall ecology was healthy. The frozen v6.6 result should not be retroactively tuned; its collapse became the question addressed by v6.7.

---

## What v6.7 Established

v6.7 was a predeclared **development cause-separation assay**, not a confirmatory evaluation. It crossed two water-field profiles with two necrosis responses, using 20 new development seeds at 0°, both fixed and adaptive transport, for 160 runs:

| Condition | Water field | Necrosis response | Extinct by tick 360 |
|---|---|---|---:|
| A | v6.6 radial field | Immediate | 32/40 = 0.800 |
| B | v6.5-equivalent depth-stretched field | Immediate | 6/40 = 0.150 |
| C | v6.6 radial field | 5-tick grace | 31/40 = 0.775 |
| D | v6.5-equivalent depth-stretched field | 5-tick grace | 6/40 = 0.150 |

Changing only the water field reduced extinction by 26/40 runs, or 0.65. Adding only the necrosis grace reduced it by 1/40, or 0.025, and B and D did not differ. Under the preregistered rule, the sealed reference-runtime classification was **`WATER_FIELD_DOMINANT`**.

The supported interpretation is that chronic water limitation in the v6.6 water field was the dominant tested driver of the collapse, with necrosis largely following that shortage. It is not evidence that necrosis is irrelevant in general.

The v6.5-equivalent water field was a diagnostic condition, not a selected final repair. Only one founder had a positive initial water balance under that field. No v6.7 confirmatory evaluation was designed or run, and no real-organism calibration was attempted. The correct current label, including the runtime limitation described above, is:

> `WATER_FIELD_DOMINANT — sealed reference-runtime result; cross-platform portability audit pending`

---

## How the v6 Line Developed

### v6.0 — Minimal evolutionary kernel

v6.0 began a new research line without modifying v5.8.0. It removed predefined fungus, alga, symbiont, species, and ecotype states from the dynamics.

It added:

- one common-ancestor clonal initialization;
- five inherited continuous parameters;
- deterministic phenotype derivation and explicit costs;
- habitat-dependent acquisition without habitat-dependent mutation;
- conservative local resource redistribution;
- non-overlapping survival and reproduction;
- random inherited mutation and adjacent-patch dispersal;
- homogeneous and heterogeneous habitat presets;
- subject-keyed random streams;
- full ancestry and per-generation machine-readable traces.

The environment cannot directly rewrite the genome during an organism's life. Any adaptation must arise through differential survival and reproduction of inherited variants.

v6.0 provides an apparatus for a diversification experiment. A single default run is not evidence that ecological diversification occurred.

### v6.1 — Persistent spatial mycelium

v6.1 replaced whole-population generational turnover with persistent, overlapping colony lifetimes. A colony became an explicit graph of cells, tips, and edges that could grow, branch, release spores, and form contact-mediated fusion links.

Important accounting changes:

- releasing a spore does not remove the parent;
- established offspring can coexist with their parent;
- actual colony death is separated from spore establishment failure;
- failed or expired spores are not counted as dead colonies;
- the observer is read-only and cannot change the simulation.

The v6.1 environment is spatial, but absorbed resources still enter a colony-wide energy/water wallet. This limitation motivated v6.2.

The fixed seed-610, 80-tick mechanism validation observed four living colonies, 333 hyphal cells, one living parent-child pair, no actual colony deaths, two establishment failures, and three conservative fusion links. This was a deterministic validation run, not a replicated ecological result.

### v6.2 — Local metabolism and partial necrosis

v6.2 replaced the colony-wide wallet with local state on each hyphal module:

- energy;
- water;
- vitality;
- starvation duration.

It also added:

- simultaneous donor-capped, fixed-conductance transfer;
- gradual weakening and module-level necrosis;
- limited recycling, visible detritus, and delayed spatial reuse;
- explicit module, ramet, genet, and lineage identity;
- survival of disconnected fragments;
- explicit same-genet re-anastomosis;
- a separate non-self boundary for contact with another genet.

Mere adjacency no longer creates an edge automatically. Additional loops require an explicit anastomosis event.

The model records four distinct outcomes:

1. module necrosis;
2. ramet death;
3. genet extinction;
4. spore establishment failure.

These must not be combined into one generic "death" count.

The fixed seed-620, 360-tick mechanism validation observed six necrotic modules, two fragment ramets, two ramet deaths, one genet extinction, and one successful offspring establishment while the parent genet remained alive. This single run demonstrated that the mechanisms operated; it was not a general ecological or evolutionary result.

### v6.2.1 — Patched local-metabolism demonstration

v6.2.1 preserved v6.2.0 and made two bounded changes:

- it reduced an unnecessary post-extension water reserve that had produced long visual plateaus in the default demonstration;
- it made the terminal observer skip redraws when the visible state had not changed, while still simulating every tick.

`--every-tick` restores one frame per tick. The transport equation, mutation rule, death definitions, and claim boundary were not changed.

Seed 620 influenced this adjustment and is therefore a **development/calibration seed**, not independent evidence. v6.3 excludes it from the evaluation set.

### v6.3 — Separate transport comparison package

v6.3 preserved v6.2.1 and added three experimental modes:

- `none`: no energy or water moves between modules;
- `equalize`: fixed-conductance movement down local stock differences;
- `demand`: a fixed-conductance source-sink rule that reserves two ticks of maintenance and adds one extension cost for tips.

All proposed outflows are aggregated per donor, proportionally capped, and applied simultaneously. Energy and water are independently conserved. Conductance does not adapt.

The evaluation question, endpoints, seed derivation, and decision rule were fixed before the evaluation runs were inspected. The current result is described in [What v6.3 Established](#what-v63-established).

### v6.4 — Fixed versus adaptive conductance

v6.4 was deliberately reduced to one mechanism question after an earlier extended prototype proved too broad. The released simple r2 package added `adaptive-equalize`, in which edge conductances strengthen or decay from realized transport history while remaining under a fixed total budget. Its comparator, `fixed-equalize`, retained uniform conductance. A two-round flux aggregation issue was corrected before evaluation, and raw cross-platform state hashes were removed from the sealed validation in favor of semantic regression plus exact replay within the same runtime.

The 90-run evaluation found no clear adaptive benefit or harm on either primary endpoint. The result is described in [What v6.4 Established](#what-v64-established).

### v6.5 — Dynamic environment and edge damage

v6.5 froze v6.4 r2 and changed the environment rather than the adaptive rule. It introduced scheduled patch motion and explicit environmental edge damage, with environmental events separated from growth randomness. Environmental edge deletion remained distinct from module necrosis, ramet death, genet extinction, and establishment failure.

The completed evaluation found no clear fixed/adaptive difference in any of eight primary comparisons, but the early-extinction zero-padding error requires the permanent `COMPLETED_WITH_PROTOCOL_DEVIATION` label. See [What v6.5 Established](#what-v65-established).

### v6.6 — Continuous coordinates and rotation audit

v6.6 converted positions and environmental coupling from a four-neighbor lattice to continuous geometry. The purpose was to test whether coordinate-axis artifacts remained, without presenting geometric equivalence as biological validation. Zero-valued endpoints were prevented from becoming artificial log-ratio equivalence through pseudocounts; inactive patch uptake was retained only as an auxiliary diagnostic.

The primary engineering audit passed, but the ecological diagnostics revealed widespread extinction and nearly inactive patch use. See [What v6.6 Established and Exposed](#what-v66-established-and-exposed).

### v6.7 — Water-field/necrosis causal separation

v6.7 preserved the v6.6 r2 baseline and used a new seed namespace to separate water-field effects, necrosis-grace effects, and their interaction. A five-tick grace tolerates five consecutive shortfall ticks; the existing vitality-decay rule begins on the sixth, and a fully paid tick resets the counter. It does not weaken the decay coefficient. The package also added founder-level water budgets, resource-limited module-ticks, first-necrosis time, cumulative necrosis, patch-distance, and uptake diagnostics.

The development assay classified the tested water-field change as dominant. This result diagnoses v6.6 but does not select a final repaired ecology. See [What v6.7 Established](#what-v67-established).

---

# Frozen v5.8.0 Ecological Baseline

## Overview

RootNet v5.8.0 is an **artificial ecosystem inspired by fungi, algae, and symbionts**—individuals combining both functions.

It is **not a predictive model calibrated against measured data from any specific real organism**. It is not intended to estimate the population size or mortality of real forests or mycorrhizal networks. It is an experimental world for studying what kinds of resource distribution, survival, growth, reproduction, and fragmentation/reconnection arise from defined rules.

Each individual holds three internal resources: **carbon, water, and nitrogen**. RootNet—the underground network connecting individuals—transports resources between connected individuals.

Transport has the following properties:

- the exact amount subtracted from the supplier is added to the receiver;
- nothing is lost to the outside during transport;
- the total amount of each resource is conserved across the whole population during transport.

RootNet does not create resources. It redistributes resources that already exist among connected individuals.

## Biological Model

### Three functional groups

- **`fungus`**: does not photosynthesize and obtains carbon from organic substrate.
- **`alga`**: obtains carbon from light through photosynthesis.
- **`symbiotic`**: uses both photosynthesis and substrate utilization.

These predefined groups belong to v5.8.0. They were deliberately removed from the v6.0 evolutionary dynamics.

### Three resources

Each v5.8.0 individual holds three pools, each in the range 0.0–1.5:

- **carbon**: energy for maintenance and growth;
- **water**: hydration state;
- **nitrogen**: a growth requirement.

The model also records how many consecutive days each resource has been insufficient. Adequate days gradually repair the accumulated deficiency state.

### One-day sequence

Each day is computed approximately in this order:

1. resource acquisition from light, substrate, rain, storage, and soil;
2. conservative RootNet transport between connected individuals;
3. maintenance consumption;
4. deficiency and death checks;
5. growth;
6. environmental load, biosecurity, reproduction, and fragmentation/reconnection updates.

### Reproduction and inheritance

Eligible individuals produce seeds, and seeds can germinate into new individuals. Offspring inherit parental genes and physiological traits with small mutations.

Values such as `resource_sharing` are physiological parameters derived from genes and morphology, not personality labels.

For the exact variables and equations, see `BIOLOGICAL_MODEL_SPEC.md` in the v5.8.0 package.

## v5.8.0 Experiment

The study compared resource transport **ON** and **OFF** under three rainfall conditions:

1. natural rainfall;
2. a 60-day drought;
3. a 120-day drought.

The OFF condition retained connections, signaling, biosecurity, and fragmentation/reconnection. Only carbon, water, and nitrogen transport was disabled. The experiment did not dismantle the network itself.

## v5.8.0 Main Results

All results below are internal to the v5.8.0 artificial ecosystem.

### Natural rainfall

- Final survivors: ON **39.54**, OFF **49.45**
- Total deaths: ON **90**, OFF **205**
- Mean paired difference in final survivors, ON minus OFF: **−9.91**

Transport reduced deaths, but it reduced births by more, leaving a smaller final population.

### 60-day drought

- Final survivors: ON **32.01**, OFF **33.40**
- Total deaths: ON **72**, OFF **177**
- Mean paired difference in final survivors: **−1.39**

The gap narrowed relative to natural rainfall. This does not establish a tipping point; it is only an intermediate observation.

### 120-day drought

- Final survivors: ON **16.60**, OFF **14.27**
- Total deaths: ON **123**, OFF **405**
- Water-deficiency individual-days: ON **29.23**, OFF **115.01**
- Mean paired difference in final survivors: **+2.33**

Under strong drought, transport sharply reduced water deficiency and deaths, and the final survivor count was larger.

```text
[Natural rainfall]
Transport ON ─▶ deaths decrease ─▶ births decrease even more ─▶ smaller final population

[120-day drought]
Transport ON ─▶ water deficiency decreases ─▶ deaths decrease ─▶ larger final population
```

As a supplementary observation, the final number of symbionts was larger under transport ON in all three rainfall conditions. This indicates that the modeled benefit was not uniform across functional groups.

## Path of the v5.8.0 Birth Difference

Under natural rainfall, 200 paired trajectories were used to trace where the final population difference began.

| Metric | ON mean | OFF mean |
|---|---:|---:|
| New seeds | 43.00 | 69.93 |
| Germinations | 31.44 | 42.51 |
| Total growth | 2274.82 | 2992.37 |
| Reproduction-eligible individual-days | 162.97 | 259.59 |

The median first-appearance order was:

1. transport, pre-reproduction resources, and growth: **day 2**;
2. reproduction-readiness state: **day 24**;
3. new seed count: **day 52**;
4. germination and survivor count: **day 57**.

This supports the bounded interpretation that the birth difference arose before germination, through earlier growth, reproduction preparation, and seed production stages.

It does not identify resource leveling, donor cost, or population pressure as a sole direct cause. Within the ON condition, net exporters averaged 1.31 seeds and net receivers averaged 0.95 seeds. That descriptive tally does not estimate the causal effect of being an exporter or receiver.

## Relationship to Existing Theory

The broad direction overlaps with existing ecological and evolutionary theory, including stress-gradient arguments, models in which cooperation matters more under harsh conditions, models of reproductive cost and population resilience, and experiments showing water movement through mycorrhizal connections.

RootNet did not discover a new general theory of evolution. Its v5.8.0 contribution was a controlled audit inside one artificial ecosystem: conservative transfer of three resources, a reversal between natural rainfall and strong drought, and the measured path by which a birth difference appeared.

### References retained from the v5.8.0 README

- [Díaz-Sierra et al. 2024, Scientific Reports](https://doi.org/10.1038/s41598-024-52447-z)
- [Andras, Lazarus & Roberts 2007, BMC Evolutionary Biology](https://doi.org/10.1186/1471-2148-7-240)
- [Chen, Rubenstein & Shen 2022, Frontiers in Psychology](https://doi.org/10.3389/fpsyg.2022.768773)
- [Egerton-Warburton et al. 2007, Journal of Experimental Botany](https://doi.org/10.1093/jxb/erm009)
- [Kayser & Lampert 2021, Journal of Theoretical Biology](https://doi.org/10.1016/j.jtbi.2021.110603)

See `rootnet_existing_theory_audit_ja.md` in the v5.8.0 materials for the detailed point-by-point comparison.

## v5.8.0 Verification

### Resource-transport ON/OFF experiment

- seeds 0–99;
- natural rainfall, 60-day drought, and 120-day drought;
- transport ON and OFF for each condition;
- **600 trajectories** and **144,000 simulation-days**;
- transport under OFF exactly 0;
- all mass-balance errors below `1e-10`;
- overall verdict: **PASS**.

### Birth-path audit

- seeds 0–99;
- natural rainfall, paired ON and OFF;
- **200 trajectories** and **48,000 simulation-days**;
- weather and solar radiation identical within each seed pair;
- maximum absolute mass-balance error `5.684341886081e-14`;
- overall verdict: **PASS**.

### v5.8.0 file guide

- `BIOLOGICAL_MODEL_SPEC.md` — variables, formulas, and deficiency-death rules;
- `ROOTNET_TRANSPORT_ABLATION_100SEED_SUMMARY.md` — observations and differences by rainfall condition;
- `ROOTNET_TRANSPORT_ABLATION_100SEED_VERIFICATION.md` — verification record for the ON/OFF experiment;
- `BIRTH_PATH_AUDIT_PROTOCOL.md` — fixed procedure and stopping rules for the birth-path audit;
- `BIRTH_PATH_AUDIT_REPORT.md` — birth-path results;
- `BIRTH_PATH_AUDIT_VERIFICATION.md` — verification record for the birth-path audit;
- `WEATHER_PAIRING_AUDIT.md` — weather and solar-pairing audit.

Per-parent, per-day, and per-resource details are stored in the accompanying JSONL records.

---

## Evidence and Claim Boundaries Across the Series

### Supported at the stated scope

- v5.8.0 supports its transport ON/OFF findings only inside the v5.8.0 artificial ecosystem and tested conditions.
- v6.0–v6.2.1 validations support that their specified mechanisms execute reproducibly and satisfy their mechanical checks.
- v6.3 supports a benefit of conservative graph-based resource translocation for sustained growth and exploration under its tested environment.
- v6.4 records that its tested adaptive allocation did not clearly outperform or underperform fixed allocation in the normal artificial environment; this is not an equivalence claim.
- v6.5 records that no clear adaptive effect was detected under its four tested schedules, subject to the permanent protocol-deviation qualification; this is not an equivalence claim.
- v6.6 supports engineering rotation equivalence for three geometric endpoints within the preregistered ±5% bounds; it simultaneously documents an ecologically collapsed assay state.
- v6.7 supports `WATER_FIELD_DOMINANT` only as a sealed development result in the reference runtime. Cross-platform replay remains pending, and the diagnostic water field is not a final repair.

### Not established

- prediction of real organism, forest, soil, or mycorrhizal-network population sizes;
- reconstruction of real fungal evolution or real evolutionary history;
- emergence of fungi from unconstrained physics or chemistry;
- real-world optimality of the implemented transport rules;
- universal superiority of demand-based transport;
- universal benefit, harm, or uselessness of adaptive conductance;
- necessity of transport for survival;
- evolution of resource sharing because of drought;
- long-term evolutionary-fitness advantage of transport, an optimal sharing rate, or the drought frequency required for sharing to evolve;
- operational speciation, coevolving symbiotic partners, or evolution of adaptive conductance;
- ecological health inferred from rotation equivalence alone;
- cross-platform byte-identical simulation trajectories for v6.4–v6.7;
- a final corrected water field or a confirmatory v6.7 ecological result;
- calibration of any model parameter to a real fungal species.

In the later spatial v6 packages, growth locations, topology, resource histories, necrosis, fragmentation, germination, and lineage outcomes are generated from local state and keyed stochastic events. The author still supplies fungal-like primitives such as tips, edges, extension, spores, and anastomosis. The viewer remains observational and does not feed back into the dynamics.

---

## Running the Packages

Each version is a separate directory or ZIP. Open the intended version's directory before running its commands.

### v5.8.0

```powershell
python main.py --days 10 --seed 42
python -m unittest discover -v
python validate_v5_8_0.py
```

The default save target is `fusa_rootnet_v5_8_0.json`, and the lineage tree is `fusa_lineage_tree.html`.

### v6.0

```powershell
python watch.py --generations 40 --seed 600
python main.py --generations 20 --seed 600 --output smoke_output
python -m unittest discover -v
python validate_v6_0.py
python verify_package.py
```

### v6.1

```powershell
python watch.py --ticks 200 --delay 0.05
python main.py --ticks 80 --seed 610 --output run_output
python -m unittest discover -s tests -v
python validate_v6_1.py
python verify_package.py
```

### v6.2.1

```powershell
python watch.py --ticks 360 --delay 0.04
python watch.py --every-tick
python main.py --ticks 360 --seed 620 --output run_output
python -m unittest discover -s tests -v
python validate_v6_2.py
python verify_package.py
```

### v6.3

```powershell
python watch.py --transport none
python watch.py --transport equalize
python watch.py --transport demand

python main.py --transport demand --seed 620 --ticks 360 --output run_output_demand

python -m unittest discover -s tests -v
python validate_v6_3.py
python verify_package.py
```

To reproduce the sealed 30-seed evaluation:

```powershell
python experiment_v6_3.py --ticks 360 --replicates 30 --output reproduced_evaluation_v6_3.json
```

### v6.4 through v6.7

Each later package includes its own version-specific commands and sealed settings. Start with the non-mutating package checks from the extracted package directory:

```powershell
python -m unittest discover -s tests -v
python verify_package.py
```

Do not launch or alter a sealed evaluation merely to test installation. Follow the package protocol for the exact experiment command, dimensions, ticks, conditions, and locked seed list. A v6.5 replay must retain the published protocol-deviation label, and v6.7 has no confirmatory evaluation to reproduce.

Python 3.10 or newer is sufficient for v6.1–v6.3; the packages use the standard library. v6.0 recommends Python 3.11 or newer. For v6.4–v6.7, use the exact runtime declared inside the package for byte-level sealed replay and read [Numerical portability and operating-system differences](#numerical-portability-and-operating-system-differences) before interpreting a digest mismatch.

---

## Package Guide

The v6 line is distributed as separate packages:

- `rootnet_v6_0_evolutionary_kernel.zip`
- `rootnet_v6_1_spatial_mycelium.zip`
- `rootnet_v6_2_module_metabolism.zip`
- `rootnet_v6_2_1_module_metabolism.zip`
- `rootnet_v6_3_transport_experiment.zip`
- `RootNet_v6_4_simple_adaptive_conductance_r2.zip`
- `RootNet_v6_5_dynamic_environment_r2.zip`
- `RootNet_v6_6_r2_continuous_coordinates.zip`
- `RootNet_v6_7_causal_separation.zip`

Each ZIP has a companion `_SHA256.txt` file. Inside the packages:

- `README.md` gives version-specific operating instructions;
- `MODEL_SPEC.md` defines the implemented mechanics;
- `RESEARCH_BOUNDARIES.md` defines the allowed claims;
- `RELEASE_NOTES_*.md` lists changes from the preceding package;
- `validation_*.json` records deterministic mechanical validation;
- `verify_package.py` checks the package manifest and reproducibility.

The v6.3 package additionally contains:

- `V6_3_PREREGISTERED_PROTOCOL.md` — question, conditions, endpoints, seeds, and decision rule fixed before evaluation;
- `EVALUATION_REPORT_V6_3.md` — paired results and bounded interpretation;
- `evaluation_v6_3.json` — machine-readable evaluation data;
- `experiment_v6_3.py` — evaluation reproducer.

The v6.4–v6.7 distributions additionally provide version-specific preregistered protocols, locked seed lists, validation records, machine-readable evaluation or development results, and companion seal/hash records. Keep these paired with the exact package revision. In particular:

- v6.4 r2 is the evaluated simplified adaptive-conductance package; the earlier extended prototype is not the evaluation package;
- v6.5 r2 must remain labeled `COMPLETED_WITH_PROTOCOL_DEVIATION`;
- v6.6 r2 separates three primary rotation endpoints from auxiliary active-patch uptake;
- v6.7 is a causal-separation development package with 160 completed runs and zero confirmatory evaluation runs.

The packaged v6.3 ZIP SHA-256 is:

```text
3E4E0DC7B666DD4069E52D4D9AA2712419FB49021A6E97F4CC00F2667526AEE3
```

Later sealed package ZIP hashes recorded in the development logs are:

| Package | ZIP SHA-256 |
|---|---|
| v6.4 simple r2 | `E9CC0FD6A2EF3C22759FBFCC3865BA88F79920E3789DC113F2FE86296F826D6C` |
| v6.5 r2 | `7769910BD7408F393B240E074DCC7FF52785FDA5F1404D08C6D07AE3ACFD7C50` |
| v6.6 r2 | `AC6CFB094D5C14A263E1C9A39B3C946B7E6ECA61B022239C8F3AA1643DB804E2` |
| v6.7 causal-separation package | `BD21398C6F262257CB3E5B9FDEC6A84339ADADDCC974E4AD3F82861D406B5F49` |

The later outer archive `RootNet_v6_7_Causal_Separation_SEALED_2026-08-21.zip` has SHA-256 `D7FB473A68AE780FF661856644C5398006D857A190D3A727CF320EC2C7054F31`; it contains the unchanged inner v6.7 package. Package hashes establish artifact identity, not cross-platform equality of regenerated floating-point state digests.

Do not overwrite the frozen v5.8.0 baseline or an earlier v6 package when working with a later version. Extract each version into its own directory and retain its matching hash and validation records.
