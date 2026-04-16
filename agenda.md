# Metagenomics Workshop

## Purpose of the workshop

The primary aim of this workshop is to familiarise the group with current and emerging metagenomic pipelines and analytical approaches, and how these are applied to real datasets across projects.

The focus is on:
- understanding where the data comes from
- how it is processed
- how outputs are translated into biological conclusions

---

# Day 1 — Data generation, pipelines, and outputs

## 10:00–10:20 | Opening: Why this workshop?
**Lead:** Ben

- Overview of datasets and projects (GETCampy, Peru, wildlife)
- Key challenges:
  - heterogeneous datasets
  - inconsistent processing
  - interpretation difficulty
- Goals:
  - shared understanding
  - standardisation
  - practical capability

---

## 10:20–11:20 | Where does the data come from?

- **Manik:** Human clinical sampling challenges
- **Narhulan:** Environmental / wild bird datasets
- **Fran:** DNA extraction challenges (chicken & wild birds)

---

## 11:20–11:35 | Coffee break

---

## 11:35–12:20 | Sample QC and preprocessing
**Lead:** Madison

- Read QC (FastQC, MultiQC)
- Trimming and filtering
- Host removal
- Contamination

**Key concept:** garbage in, garbage out

---

## 12:20–13:00 | Current pipelines
**Leads:** Matt / Alex

- nf-core `taxprofiler` and `mag`
- Workflow structure
- Outputs:
  - taxonomic profiles
  - MAGs
  - QC reports

---

## 13:00–14:00 | Lunch

---

## 14:00–15:30 | Post-processing and biological interpretation (hands-on)
**Leads:** Ben and Matt (with Alex and Madison) 

### Objective
Move from pipeline outputs to interpretable biological results using real datasets.

---

### Part 1 — Preparing analysis-ready data

- Load abundance tables (Bracken output)
- Merge with metadata
- Filter low-abundance taxa (<0.01%)
- Normalise data

```r
abundance_rel <- abundance / rowSums(abundance)
```

---

### Part 2 — Read-based analyses

- Extract species-specific reads (e.g. Campylobacter)
- Calculate relative abundance
- Generate:
  - barplots
  - boxplots
  - presence/absence summaries

---

### Part 3 — Diversity analysis

- Alpha diversity (e.g. Shannon)
- Beta diversity (e.g. Bray–Curtis)

---

### Part 4 — Assembly-based comparison

- MAG-based workflows
- Requirements and limitations
- Comparison with read-based approaches

---

### Core message

Read-based approaches detect presence.  
Assembly-based approaches explain biology.

---

### Outputs

- Cleaned abundance table
- Diversity metrics
- Species-specific plots
- Case vs control comparisons

---

## 15:30–15:45 | Break

---

## 15:45–16:45 | Discussion and integration

- Standardisation of pipelines
- QC thresholds
- Detection thresholds
- When to use MAGs

---

## 16:45–17:00 | Wrap-up

---

# Day 2 — Advanced post-processing hackathon

## Overview

Hands-on hackathon using real datasets to:
- process outputs
- integrate metadata
- identify biological signals
- generate interpretable results

---

## 10:00–10:20 | Introduction and setup

- Recap Day 1
- Assign datasets
- Define tasks

---

## 10:20–11:45 | Data preparation

- Extract abundance tables
- Merge metadata
- Filter low-abundance taxa
- Normalise data

```r
abundance_rel <- abundance / rowSums(abundance)
```

---

## 11:45–12:00 | Coffee break

---

## 12:00–13:00 | Identifying biological signal

- Detect key taxa
- Compare across groups
- Generate plots

---

## 13:00–14:00 | Lunch

---

## 14:00–15:00 | Detection limits

```r
plot(read_depth, campy_abundance)
```

- detection thresholds
- sequencing depth
- false negatives

---

## 15:00–15:15 | Break

---

## 15:15–16:15 | Advanced analyses

Options:
- MAG analysis
- AMR detection
- Visualisation

---

## 16:15–16:45 | Group presentations

- dataset
- approach
- findings
- limitations

---

## 16:45–17:00 | Wrap-up

---

# Core principles

- Interpretation > execution
- Filtering > plotting
- Biological question > pipeline choice
- Data quality determines conclusions
