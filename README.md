# AXARA Bridge — Automated SDA Peptide Hit Mapping

**The fastest path from raw LC-MS data to a confidence-ranked 
SDA peptide hit map.**

---

## The Problem We Solve

You ran a photo-affinity labelling experiment. You have a raw 
.mzML file. Somewhere in that file are the peptides that carried 
the SDA crosslink — the ones that tell you which proteins and 
residues your probe labelled.

Finding them manually takes hours. Sometimes days. It requires 
proteomics expertise most medicinal chemistry teams do not have 
in-house. And it is the bottleneck that stops structural evidence 
from reaching the people who need it.

AXARA Bridge does it in minutes. On any instrument. Without 
a proteomics specialist.

---

## What You Upload

A centroided .mzML file from your LC-MS instrument.

AXARA Bridge accepts .mzML files from all major LC-MS platforms. 
If your instrument produces vendor-format raw files (.raw, .d, 
.wiff), convert to centroided .mzML using ProteoWizard msconvert 
before upload.

---

## What You Receive

**Confidence-ranked SDA peptide hits**
Every peptide carrying the SDA adduct (+196.07 Da on lysine), 
ranked by statistical confidence with FDR control by 
target-decoy competition against the human proteome.

**Three confidence tiers**

| Tier | FDR threshold | Recommended use |
|------|--------------|-----------------|
| High confidence | < 1% | Structural validation and patent filing |
| Medium confidence | 1-5% | Experimental follow-up |
| Exploratory | 5-10% | Hypothesis generating |

**Downloadable hit mapping report (.txt)**
Complete report including all identified peptides, protein 
assignments, FDR values, search scores, scan numbers, and 
search parameter documentation. Ready for laboratory notebooks 
and patent applications.

**Downloadable hit table (.tsv)**
Machine-readable table of all SDA hits for integration into 
existing data analysis workflows.

---

## The Two Mass Shifts

SDA photo-affinity labelling produces two distinct mass shifts 
that appear in LC-MS data. Both are real. Both are meaningful. 
They represent the two ends of the same SDA linker.

| Modification | Monoisotopic mass | Location |
|-------------|-------------------|----------|
| NHS-ester adduct on probe peptide | +196.0706 Da | Lysine (K), N-terminus |
| Carbene adduct on target peptide | +82.0419 Da | Target residue (C-H or N-H insertion) |

AXARA Bridge searches for both in a single analysis run — 
identifying which peptides carried the SDA probe and which 
residues on the target protein were crosslinked.

---

## How It Works

Upload .mzML file
↓
Automated database search against human proteome
↓
SDA modification detection at +196.07 Da and +82.04 Da
↓
FDR control by target-decoy competition
↓
Confidence-ranked peptide hit map
↓
Downloadable report — minutes not days

---

## Service Tiers

| Tier | Deliverable | Price |
|------|-------------|-------|
| Tier 1 — Peptide Hit Mapping | Confidence-ranked SDA hits, FDR table, downloadable report | $1,995 |
| Tier 2 — Full Analytical Report | Tier 1 plus professional PDF with spectra, interpretation, next steps | $3,995 |
| Tier 3 — Structural Validation | Tier 2 plus AlphaFold3 binding pocket map, annotated PDB, IND-ready report | $6,995 |

**Beta access to Tier 1 is free during the beta period.**
No credit card required.

---

## Access The Tool

### [Launch AXARA Bridge — bridge.axara.bio](https://bridge.axara.bio)

---

## The AXARA Ecosystem

AXARA Bridge is the analytical engine of the complete AXARA 
photo-affinity labelling platform. Each component is designed 
to work with the others — but each works independently too.

**Step 1 — Rule of 25 Engine**
Score your lead computationally before synthesis. Identify 
optimal SDA attachment points. Get a ranked probe design report 
in seconds from a SMILES input.
[Try the Rule of 25 Engine](https://rule-25-engine-861834762353.us-central1.run.app)

**Step 2 — AXARA PAL Kit**
Run the photo-affinity labelling experiment with validated 
reagents. High-purity SDA, validated buffers at pH 7.4 and 8.5, 
Suprasil quartz vial, and a batch Digital Twin QR code linking 
to Cary 100 purity data.

**Step 3 — AXARA Bridge**
Upload your .mzML file. Get your peptide hit map. Know which 
residues your probe labelled — in minutes.

---

## Whitepaper

Full scientific background, chemistry explanation, validation 
methodology, and service tier details:

[Read the AXARA Bridge Whitepaper](AXARA_Bridge_Whitepaper.md)

---

## Frequently Asked Questions

**What instruments does AXARA Bridge support?**
Any instrument that produces centroided .mzML files. This 
includes Thermo Orbitrap, Bruker timsTOF, Sciex TripleTOF, 
Agilent QTOF, and Waters instruments. Convert vendor raw files 
to centroided .mzML using ProteoWizard msconvert before upload.

**What proteome database is used?**
Human proteome (UniProt SwissProt). Contact us for custom 
database requests for non-human targets or proprietary sequences.

**What file size is supported?**
Recommended under 500MB for best performance during beta. 
Larger files are supported — contact us for high-volume 
processing.

**What crosslinker does this work with?**
AXARA Bridge is optimised for SDA (succinimidyl 4,4'-azipentanoate) 
photo-affinity labelling. Contact us for other diazirine 
crosslinker configurations.

**Is my data stored?**
No. All data is processed in volatile RAM. Nothing is stored 
on AXARA servers after report generation.

**What is the difference between +196.07 Da and +82.04 Da?**
+196.07 Da is the NHS-ester adduct on your probe peptide — 
this identifies which peptides carried the SDA linker. 
+82.04 Da is the carbene adduct on the target protein peptide — 
this identifies which residue was crosslinked. Both are searched 
in a single AXARA Bridge run.

---

## Policies

- [Terms of Service](terms-of-service.md)
- [Privacy Policy](privacy-policy.md)
- [Refund Policy](refund-policy.md)

---

## Contact

For Tier 2 and Tier 3 analytical reports, enterprise licensing, 
custom database requests, and the AXARA PAL Kit:

**[axara.bio](https://axara.bio)**

---

*© 2025 AXARA BioScience. All rights reserved.*
*The AXARA Bridge pipeline, search configuration, and analytical*
*methodology are proprietary to AXARA BioScience.*
*For research use only. Not for clinical decision-making*
*without experimental validation.*
