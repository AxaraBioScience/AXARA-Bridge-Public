# AXARA Bridge: Automated SDA Peptide Hit Mapping for Photo-Affinity Labelling Experiments

**Version 1.0 | AXARA BioScience | 2025**

---

## Abstract

Photo-affinity labelling with SDA (succinimidyl 4,4'-azipentanoate) 
is one of the most powerful techniques in covalent drug discovery. 
It provides direct, residue-level evidence of target engagement — 
the data package required for IND-enabling studies and patent 
filing. The bottleneck is not the experiment. It is what comes 
after: the manual, time-consuming search for SDA-modified peptides 
in raw LC-MS data.

AXARA Bridge automates that search. It accepts a raw .mzML file 
from any LC-MS instrument and returns a complete, confidence-ranked 
peptide hit map with FDR control in minutes. No manual searching. 
No spreadsheets. No missed hits.

---

## 1. The Problem

A photo-affinity labelling experiment produces a raw LC-MS file 
containing tens of thousands of MS2 spectra. Somewhere in that 
file are the peptides that carried the SDA crosslink — the ones 
that tell you which proteins and residues your probe labelled.

Finding them manually means:

- Running a database search with the correct SDA modification mass
- Filtering for the modification on the right residues
- Applying FDR control to separate real hits from noise
- Rolling up peptide-level hits to protein-level conclusions
- Interpreting which hits are meaningful

For a proteomics specialist this takes hours. For a medicinal 
chemist without proteomics training it can take days — or it 
doesn't happen at all, and the structural information locked 
inside the LC-MS file is never extracted.

This is the gap AXARA Bridge was built to close.

---

## 2. The Chemistry — Two Mass Shifts, One Experiment

A common source of confusion in SDA photo-affinity labelling is 
the relationship between two distinct mass shifts that appear in 
the LC-MS data. Understanding both is essential for correct 
interpretation.

**The probe peptide adduct: +196.07 Da**

When the NHS-ester end of the SDA linker reacts with a lysine 
residue on the probe molecule, the NHS leaving group departs and 
a stable amide bond forms. The mass adduct remaining on the probe 
peptide is +196.0706 Da (monoisotopic). This is the modification 
you search for in database searching to identify which peptides 
carried the SDA probe.

**The target peptide adduct: +82.04 Da**

When UV irradiation at 365nm activates the diazirine group, a 
reactive carbene intermediate forms and inserts into a C-H or N-H 
bond on the target protein. The mass adduct on the target peptide 
is +82.0419 Da. This modification identifies which residue on the 
target protein was crosslinked.

Both modifications are real and both are scientifically meaningful. 
They represent the two ends of the same SDA linker — the probe 
attachment end and the target crosslinking end respectively. AXARA 
Bridge searches for both in a single analysis run.

---

## 3. The AXARA Bridge Pipeline

AXARA Bridge accepts a centroided .mzML file and returns a complete 
peptide hit mapping report. The pipeline is built on a validated 
proteomics search engine with a proprietary search configuration 
optimised specifically for SDA photo-affinity labelling experiments.

The pipeline is not a generic proteomics search. It is configured 
and validated specifically for:

- SDA NHS-ester adducts on lysine residues and protein N-termini
- The human proteome as the reference database
- Tryptic digestion with up to two missed cleavages
- Co-occurring modifications including methionine oxidation and 
  cysteine carbamidomethylation
- FDR control by target-decoy competition

The specific search parameters, modification masses, tolerance 
windows, and scoring thresholds are proprietary to AXARA BioScience 
and are validated against experimental SDA datasets.

---

## 4. Validation

The AXARA Bridge pipeline was validated on real LC-MS data 
from photo-affinity labelling experiments. Validation confirmed:

- Correct detection of SDA adducts at +196.0706 Da on lysine 
  residues and protein N-termini
- Co-modification detection — SDA adduct combined with 
  methionine oxidation on the same peptide
- Consistent precursor mass accuracy within instrument 
  specification
- FDR-controlled results distinguishing signal from noise
- Reproducible identification across replicate injections

The pipeline identified thousands of SDA-modified peptide 
spectrum matches in experimental data, including peptides 
carrying multiple simultaneous modifications — the hallmark 
of a genuine SDA photo-affinity labelling experiment.

The pipeline accepts centroided .mzML files from all major 
LC-MS instrument platforms. Conversion of vendor-format raw 
files to centroided .mzML using ProteoWizard msconvert is 
recommended prior to upload.

---

## 5. Output — The Peptide Hit Mapping Report

Every submission to AXARA Bridge returns three deliverables:

**Confidence-ranked hit list**
All SDA-modified peptides ranked by statistical confidence. 
Results are reported at three tiers:

- High confidence (FDR < 1%) — recommended for downstream 
  structural validation and patent filing
- Medium confidence (FDR 1-5%) — candidates for experimental 
  follow-up
- Exploratory (FDR 5-10%) — hypothesis-generating, requires 
  validation

**Downloadable report (.txt)**
Complete hit mapping report including all identified peptides, 
protein assignments, FDR values, search scores, scan numbers, 
and search parameter documentation. Ready to include in 
laboratory notebooks and patent applications.

**Downloadable hit table (.tsv)**
Machine-readable table of all SDA hits for integration into 
existing data analysis workflows.

---

## 6. The Service Tiers

AXARA Bridge is offered as a tiered analytical service matched 
to the depth of interpretation required.

**Tier 1 — Peptide Hit Mapping Report ($1,995)**
Automated identification of all SDA-modified peptides from raw 
.mzML input. Confidence-ranked results with FDR control. The 
foundation of every downstream analysis.

**Tier 2 — Full Analytical Report ($3,995)**
Everything in Tier 1 plus a clean professional PDF with 
peptide-level results, spectra highlights, biological 
interpretation, and specific next-step recommendations. 
The deliverable for teams that need a polished report for 
internal review or partner presentations.

**Tier 3 — Structural Validation Report ($6,995)**
Everything in Tier 2 plus residue-level crosslink mapping, 
AlphaFold3 3D binding pocket visualisation, annotated PDB 
file, and a 4-5 page professional report with regulatory and 
patent-ready language. The IND-enabling deliverable.

---

## 7. The AXARA Ecosystem

AXARA Bridge is the analytical backbone of the AXARA 
photo-affinity labelling ecosystem. It is designed to work 
seamlessly with the AXARA PhotoAffinity Labelling Kit — which 
provides high-purity SDA reagents, validated buffers, Suprasil 
quartz vials, and a batch Digital Twin QR code — and the AXARA 
Rule of 25 Engine, which scores lead compounds computationally 
before any wet-lab commitment.

The complete AXARA workflow:

1. Rule of 25 Engine — score your lead and identify optimal 
   SDA attachment points before synthesis
2. AXARA PAL Kit — run the photo-affinity labelling experiment 
   with validated reagents
3. AXARA Bridge — map the SDA hits from your LC-MS data in 
   minutes

From computational lead scoring to experimental structural 
validation in a single integrated platform.

---

## 8. Conclusion

The bottleneck in photo-affinity labelling is not the chemistry. 
It is the data analysis. AXARA Bridge removes that bottleneck — 
returning confidence-ranked SDA peptide hits from raw LC-MS data 
in minutes rather than days, with the statistical rigour required 
for downstream structural validation and patent filing.

Beta access is free at bridge.axara.bio

---

*© 2025 AXARA BioScience. All rights reserved.*
*The AXARA Bridge pipeline, search configuration, and analytical*
*methodology are proprietary to AXARA BioScience.*
*For research use only.*
