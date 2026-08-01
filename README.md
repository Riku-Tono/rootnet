# RootNet v5.8.0 Biological Model

## Overview

RootNet v5.8.0 is an **artificial ecosystem inspired by fungi, algae, and symbionts** (individuals combining both functions).

An important premise: this is **not a predictive model calibrated against measured data from any specific real organism**. It is not meant to estimate the population size or mortality of real forests or mycorrhizal networks. It is an experimental world for studying "what kinds of resource distribution, survival, growth, reproduction, and fragmentation/reconnection arise from a set of defined rules."

Inside the model, each individual holds three internal resources: **carbon, water, and nitrogen**. **RootNet** — the underground network connecting individuals — transports resources between connected individuals.

Transport has the following properties:

- The exact amount subtracted from the supplier (the side with more) is added to the receiver (the side with less).
- Nothing is lost to the outside during transport.
- Therefore, transport **conserves the total amount of resources across the whole population (mass conservation)**.

In other words, RootNet is not a mechanism that *creates* new resources; it is a mechanism that *redistributes* resources that already exist among connected individuals. The purpose of the model is to observe the behavior — resource distribution, survival, growth, reproduction, fragmentation/reconnection, and so on — that emerges from these rules.

---

## Biological Model

### Three functional groups

Initial individuals are divided into three types:

- **`fungus`**: Does not photosynthesize. Obtains carbon from organic substrate (nutrient sources in the soil).
- **`alga`**: Obtains carbon from light (photosynthesis).
- **`symbiotic`**: Uses both photosynthesis and substrate utilization.

### Three resources

Each individual holds three internal pools (each in the range 0.0–1.5):

- **carbon**: Energy for the maintenance metabolism needed to stay alive, and for growth.
- **water**: The individual's hydration state.
- **nitrogen**: Required for growth.

For each resource, the model also records "how many consecutive days it has been insufficient." Days with adequate supply recover this gradually.

### One day's sequence

Each day, every individual is computed roughly in this order:

1. **Resource acquisition**: Take in resources from light, substrate, rain, water storage, and soil.
2. **RootNet resource transport**: Move resources from higher to lower among connected individuals.
3. **Maintenance metabolism**: Consume carbon, water, and nitrogen to stay alive.
4. **Deficiency and death check**: If shortages continue, tissue damage accumulates; individuals that endure long shortages and lose vitality die of deficiency.
5. **Growth**: Use the remaining resources to grow.
6. Updates to the rest (environmental load, biosecurity, reproduction, fragmentation/reconnection).

### Reproduction and inheritance

Individuals that meet the conditions produce **seeds**, and seeds eventually **germinate** into new individuals. Offspring **inherit** the parent's genes and physiological traits, with small **mutations** added.

Note that traits such as `resource_sharing` (the tendency to share resources with connections) are not "personality." They are physiological values determined by genes and morphology.

> For detailed definitions of each variable and formula, see **`BIOLOGICAL_MODEL_SPEC.md`**. Not every formula is reproduced here.

---

## Purpose of the Experiment

This study **compared a world with resource transport ON against one with it OFF**. Three things were examined:

1. In normal conditions (natural rainfall), what effect does resource transport have on survival and births?
2. During drought (60-day and 120-day), what effect does it have?
3. At which stage does the difference in the number of births begin?

The key point is that **even under the OFF condition, RootNet's connections, signaling, biosecurity, and fragmentation/reconnection are all kept in place**. Only "the transport of carbon, water, and nitrogen" was stopped. This is not an experiment that dismantled the network itself.

---

## Main Results

All of the following are **results inside the v5.8.0 artificial ecosystem**, not predictions about real ecosystems.

### Natural rainfall

- Final survivors: ON **39.54**, OFF **49.45**
- Total deaths: ON **90**, OFF **205**
- Mean paired difference in final survivors (ON−OFF): **−9.91**

Transport ON reduced deaths. However, it reduced births (new individuals) by even more, so the **final population ended up smaller instead**.

### 60-day drought

- Final survivors: ON **32.01**, OFF **33.40**
- Total deaths: ON **72**, OFF **177**
- Mean paired difference in final survivors (ON−OFF): **−1.39**

This is an **intermediate condition** in which the gap between ON and OFF narrowed compared with natural rainfall. It cannot be said here that "a tipping point in which side is favorable has been established." This is only an observation that the gap shrank.

### 120-day drought

- Final survivors: ON **16.60**, OFF **14.27**
- Total deaths: ON **123**, OFF **405**
- Water-deficiency individual-days: ON **29.23**, OFF **115.01**
- Mean paired difference in final survivors (ON−OFF): **+2.33**

Under strong drought, transport ON **greatly reduced water deficiency and deaths, and the final number of survivors was also larger**. The direction is the reverse of the natural-rainfall case.

### Flow of effects (summary figure)

Even for the same "transport ON," the direction of the final population count reversed depending on the condition.

```
[Natural rainfall]
Transport ON ─▶ deaths decrease ─▶ but births decrease even more ─▶ final population is smaller (ON−OFF = −9.91)

[120-day drought]
Transport ON ─▶ water deficiency decreases ─▶ deaths decrease ─▶ final population is larger (ON−OFF = +2.33)
```

(Supplementary observation: for symbionts, the final number of survivors was larger under ON in all conditions — natural rainfall, 60-day, and 120-day — indicating that the benefit of transport is not uniform across functional groups.)

---

## The Path by Which the Birth Difference Arises

For the natural-rainfall result "ON has fewer final individuals," we traced **at which stage that difference begins**, using paired runs with the same seed.

### Overall averages (natural rainfall, 200 trajectories)

| Metric | ON mean | OFF mean |
|---|---:|---:|
| New seeds | 43.00 | 69.93 |
| Germinations | 31.44 | 42.51 |
| Total growth | 2274.82 | 2992.37 |
| Reproduction-eligible individual-days | 162.97 | 259.59 |

### Day on which the difference first appeared (median)

The difference appeared early, in the following order:

1. Difference in resource transport, pre-reproduction resources, and growth …… **day 2**
2. Difference in reproduction-readiness state …… **day 24**
3. Difference in the number of new seeds …… **day 52**
4. Difference in germination and survivor count …… **day 57**

What this ordering allows us to say (interpretation of the experimental facts):

> The birth difference did not arise from germination alone; it arose from the earlier stages of growth, reproduction preparation, and seed production.

On the other hand, **the following are not asserted**:

- We do not claim that resource leveling alone is the cause.
- We do not claim that only the parents that gave away resources became unable to reproduce.
- We do not claim that population pressure alone is the cause.
- We do not claim that the direct cause has been fully identified.

In fact, within the ON condition, observation showed that the **average number of seeds for net-exporter individuals (those that, on balance, gave away resources) was 1.31 — actually higher than the 0.95 of net-receiver individuals**. So a simple explanation that "only the individuals that gave away resources lost out" does not fit. Note also that this is a descriptive tally within the ON condition and does not demonstrate the causal effect of an individual's role.

---

## Relationship to Existing Theory

The broad direction overlaps with existing theory in ecology and evolutionary biology. However, RootNet has not discovered a new general theory of evolution.

Stated carefully:

- The broad direction is consistent with the **"stress-gradient hypothesis"** (the harsher the environment, the more mutual help — facilitation — tends to matter over competition).
- There are existing **mathematical models** showing that the benefit of cooperation increases the harsher the environment.
- There are also **individual-based models** in which cooperation carries a reproductive cost, yet raises a population's resilience in harsh environments.
- There is **experimental research** showing that water can move between plants via mycorrhizal networks.

RootNet's distinctive contribution does not overturn these general ideas. Rather, it **audited — within a single artificial ecosystem — the conservative transport of three resources (carbon, water, nitrogen), the reversal of effect between normal conditions and strong drought, and the path by which the birth difference arises.**

### References

- Díaz-Sierra et al. 2024, *Scientific Reports* — https://doi.org/10.1038/s41598-024-52447-z
- Andras, Lazarus & Roberts 2007, *BMC Evolutionary Biology* — https://doi.org/10.1186/1471-2148-7-240
- Chen, Rubenstein & Shen 2022, *Frontiers in Psychology* — https://doi.org/10.3389/fpsyg.2022.768773
- Egerton-Warburton et al. 2007, *Journal of Experimental Botany* — https://doi.org/10.1093/jxb/erm009
- Kayser & Lampert 2021, *Journal of Theoretical Biology* — https://doi.org/10.1016/j.jtbi.2021.110603

> For the detailed point-by-point comparison of each paper with RootNet (agreements and differences), see `rootnet_existing_theory_audit_ja.md`.

---

## What Cannot Yet Be Claimed From These Results

From this experiment, the following **cannot yet be claimed** (these are future hypotheses, not proven facts):

- It cannot be claimed that the model can predict the population size of real forests or mycorrhizal networks.
- It cannot be claimed that real organisms would yield the same numbers.
- It cannot be claimed that resource sharing evolved because of drought.
- It cannot be claimed that transport ON is advantageous in long-term evolutionary fitness.
- It cannot be claimed that this is a world-first theory or a world-first model.
- It cannot be claimed that resource leveling is the sole direct cause of the decline in births.
- The optimal sharing rate is not yet known.
- How often drought must occur for sharing to evolve is not yet known.

An important distinction: this ON/OFF comparison is an experiment on **"the ecological effect of the transport function."** It is **not an evolutionary experiment** that competes different sharing strategies against one another in the same world over many generations to see which strategy survives. Therefore, "why transport might evolve" cannot be answered by this experiment alone.

---

## Verification

To preserve the reliability of the figures, the following audits were performed, all with an overall verdict of **PASS**.

### Resource transport ON/OFF experiment

- seeds 0–99
- Conditions: natural rainfall, 60-day drought, 120-day drought
- Transport ON / OFF for each condition
- Total **600 trajectories**, **144,000 simulation-days**
- Resource transport under the OFF condition is **exactly 0**
- All mass-balance errors are **below 1e-10**
- Overall verdict: **PASS**

### Birth-path audit

- seeds 0–99
- Condition: natural rainfall
- Transport ON / OFF
- Total **200 trajectories**, **48,000 simulation-days**
- Weather and solar radiation were made **exactly identical for each seed pair** (so that divergence in population structure does not contaminate weather generation)
- Maximum absolute mass-balance error: **5.684341886081e-14**
- Overall verdict: **PASS**

---

## File Guide

Further details can be found in the following files. (Because the artifacts are split across multiple folders, filenames are given without relative links.)

- `BIOLOGICAL_MODEL_SPEC.md` — Detailed specification of the biological model: variables, formulas, and deficiency death
- `ROOTNET_TRANSPORT_ABLATION_100SEED_SUMMARY.md` — Summary of the transport ON/OFF experiment (observations and differences by condition)
- `ROOTNET_TRANSPORT_ABLATION_100SEED_VERIFICATION.md` — Verification record for the above experiment
- `BIRTH_PATH_AUDIT_PROTOCOL.md` — Procedure for the birth-path audit (fixed conditions, operational boundaries, stopping rules)
- `BIRTH_PATH_AUDIT_REPORT.md` — Results report for the birth-path audit
- `BIRTH_PATH_AUDIT_VERIFICATION.md` — Verification record for the birth-path audit
- `WEATHER_PAIRING_AUDIT.md` — Audit of the weather/solar pairing consistency

(Of all records managed in this repository, the per-parent, per-day, and per-resource details are stored in the accompanying JSONL files.)

---

## Running and Inspecting

The commands below are taken from the existing technical materials (`RootNet_v5_8_Biological_Model_README.md` and `BIOLOGICAL_MODEL_SPEC.md`). Nothing has been added by guesswork.

### Run

```powershell
python main.py --days 10 --seed 42
```

The default save target is `fusa_rootnet_v5_8_0.json`, and the lineage tree is `fusa_lineage_tree.html`.

### Inspect

```powershell
python -m unittest discover -v
python validate_v5_8_0.py
```

Inspection covers functional groups, non-anthropomorphization, the difference in carbon acquisition between fungi and algae, conservative resource transport, deficiency death, the 120-day mass balance, schema v11 migration, and save/resume consistency.
