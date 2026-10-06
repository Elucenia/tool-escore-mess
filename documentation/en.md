<!-- ELUCENIA technical documentation · escore-mess · en · no clinical/professional/rights approval -->

# MESS (Mangled Extremity Severity Score)

[conditions, sources and permissions](https://elucenia.org/en/tools/escore-mess)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Skeletal and soft-tissue injury

`energia`

- `1` — Low energy (stab wound, simple fracture, handgun projectile)
- `2` — Medium energy (open or multiple fracture, dislocation)
- `3` — High energy (high-speed accident, rifle projectile)
- `4` — Very high energy (the above + gross contamination)

### Limb ischemia

`isquemia`

- `0` — No ischemia
- `1` — Reduced or absent pulse, normal perfusion
- `2` — Absent pulse, paresthesia, slow capillary refill
- `3` — Cold, paralyzed, insensate limb

### Ischemia for more than 6 hours?

`tempo`

- `0` — No
- `1` — Yes

### Shock

`choque`

- `0` — Systolic blood pressure always \> 90 mmHg
- `1` — Transient hypotension
- `2` — Persistent hypotension

### Age

`idade`

- `0` — \< 30 years
- `1` — 30 to 50 years
- `2` — \> 50 years

## Method edition

MESS/Johansen 1990: 4 domains, ischemia doubled \>6 h; no automatic amputation order

## Documented formula

MESS = skeletal/soft tissue injury (1 to 4) + ischemia (0 to 3, doubled if lasting more than 6 h) + shock (0 to 2) + age (0 to 2).

## Limits and population

The original MESS was derived in small groups with severe lower-limb trauma. The association of the ≥7 cutoff with amputation in those groups does not establish a universal rule or automatic indication. Limb salvage depends on multidisciplinary assessment and clinical conditions not summarized by the score.

## References

- [Johansen K et al. Objective criteria accurately predict amputation following lower extremity trauma. J Trauma, 1990.](https://doi.org/10.1097/00005373-199005000-00007)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Documented results

The information below preserves the method outputs for synthetic examples. It does not constitute independent clinical validation.

### 1

MESS < 7: limb salvage range in the original series

| Result details | |
| --- | --- |
| Ischemia points | 1 |

MESS does not decide on its own: the indication for primary amputation is made by the team (orthopedics, vascular surgery, and plastic surgery), with the patient stabilized.


### 2

MESS ≥ 7: in the original series, all limbs with this score were amputated

| Result details | |
| --- | --- |
| Ischemia points | 4 (doubled: ischemia > 6 h) |

MESS does not decide on its own: the indication for primary amputation is made by the team (orthopedics, vascular surgery, and plastic surgery), with the patient stabilized.


### 3

MESS ≥ 7: in the original series, all limbs with this score were amputated

| Result details | |
| --- | --- |
| Ischemia points | 2 |

MESS does not decide on its own: the indication for primary amputation is made by the team (orthopedics, vascular surgery, and plastic surgery), with the patient stabilized.

