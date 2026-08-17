# RootNet Research Series: v5.8.0 to v6.3

**Status date:** 2026-08-18  
**Latest packaged experiment:** v6.3  
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
```

- **v5.8.0 remains the reference for the original carbon/water/nitrogen transport ON/OFF and drought results.**
- **v6.0 starts a separate model line** from a common ancestral population. It is not an in-place upgrade of v5.8.0.
- **v6.1 through v6.2.1 progressively add a persistent spatial body, local metabolism, partial necrosis, and fragment identity.** Their fixed-seed runs are mechanism validations, not replicated biological findings.
- **v6.3 is the newest completed experiment**, derived from v6.2.1. It tests three resource-translocation rules. It is a purpose-built comparison package, not a universal replacement for every earlier package.

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

### Which version should I use?

- Use **v5.8.0** to reproduce the original ecological transport and drought study.
- Use **v6.0** to inspect the deliberately minimal evolutionary kernel.
- Use **v6.1** to observe persistent colonies with overlapping parent and offspring lifetimes.
- Use **v6.2.1** rather than v6.2 for the patched local-metabolism demonstration.
- Use **v6.3** to reproduce or inspect the completed network-translocation comparison.

Results and counts should not be compared across versions as though only one parameter changed. The models change their life cycle, biological unit, resource accounting, death definitions, and research question.

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

### Not established

- prediction of real organism, forest, soil, or mycorrhizal-network population sizes;
- reconstruction of real fungal evolution or real evolutionary history;
- emergence of fungi from unconstrained physics or chemistry;
- real-world optimality of the implemented transport rules;
- universal superiority of demand-based transport;
- necessity of transport for survival;
- evolution of resource sharing because of drought;
- long-term evolutionary-fitness advantage of transport, an optimal sharing rate, or the drought frequency required for sharing to evolve;
- operational speciation, coevolving symbiotic partners, or adaptive conductance;
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

Python 3.10 or newer is sufficient for v6.1–v6.3; the packages use the standard library. v6.0 recommends Python 3.11 or newer.

---

## Package Guide

The v6 line is distributed as separate packages:

- `rootnet_v6_0_evolutionary_kernel.zip`
- `rootnet_v6_1_spatial_mycelium.zip`
- `rootnet_v6_2_module_metabolism.zip`
- `rootnet_v6_2_1_module_metabolism.zip`
- `rootnet_v6_3_transport_experiment.zip`

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

The packaged v6.3 ZIP SHA-256 is:

```text
3E4E0DC7B666DD4069E52D4D9AA2712419FB49021A6E97F4CC00F2667526AEE3
```

Do not overwrite the frozen v5.8.0 baseline or an earlier v6 package when working with a later version. Extract each version into its own directory and retain its matching hash and validation records.
