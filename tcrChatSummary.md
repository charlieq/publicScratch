# TCR Database Design & User Interface
## A Comprehensive Conversation on Immunology, Bioinformatics, and Research Data Management

**Date:** January 14, 2026  
**Participants:** Computer Scientist (User) & AI Assistant  
**Topic:** Designing a MongoDB-based TCR (T Cell Receptor) database for clinical research

---

## Table of Contents

1. [Introduction: T Cell Receptors](#introduction-t-cell-receptors)
2. [Public vs. Private Chains](#public-vs-private-chains)
3. [TCR Analysis & Disease Progression](#tcr-analysis--disease-progression)
4. [TCR-Based Biomarkers & Drug Development](#tcr-based-biomarkers--drug-development)
5. [Teplizumab: Current Clinical Reality](#teplizumab-current-clinical-reality)
6. [Database Structure Design](#database-structure-design)
7. [Data Deduplication Pipeline](#data-deduplication-pipeline)
8. [User Interface & Query Patterns](#user-interface--query-patterns)
9. [Implementation Roadmap](#implementation-roadmap)

---

## Introduction: T Cell Receptors

### Why T Cell Receptors Matter

T cells function as your immune system's specialist security team. Each T cell has a unique **T cell receptor (TCR)** on its surface—essentially a molecular "lock" that recognizes specific "keys" (antigens, or foreign proteins). When a TCR finds its matching antigen, it triggers the T cell to multiply and attack the threat.

This specific recognition is what gives you **adaptive immunity**—your immune system can "remember" and respond faster to pathogens you've encountered before.

Without TCR diversity, your immune system couldn't recognize the endless variety of pathogens out there. TCRs are critical for:
- Fighting infections
- Clearing cancer cells
- Responding to vaccines

---

## Public vs. Private Chains

### Private Clonotypes

**Private chains** (or "private clonotypes") are TCR sequences unique to an individual. When you get infected with a virus, your immune system generates millions of different T cell clones, each with slightly different TCRs. A specific TCR sequence in your body is almost certainly not present in anyone else's—it's your private invention, suited to your particular infection and genetic background.

### Public Clonotypes

**Public chains** (or "public clonotypes") are TCR sequences that appear across multiple unrelated people. This happens when different people's immune systems independently converge on the same or very similar TCR sequence in response to the same antigen. It suggests that particular TCR is especially "good" at recognizing that target—like how multiple engineers might independently arrive at the same efficient solution to a design problem.

### The Computer Science Analogy

If you think of TCRs as evolved solutions to a recognition problem:
- **Private ones** are highly customized implementations unique to each person
- **Public ones** are the "obvious" or "optimal" solutions that people independently rediscover

---

## TCR Analysis & Disease Progression

### The Core Insight

In **Type 1 Diabetes (T1D)**, the immune system mistakenly attacks insulin-producing beta cells in the pancreas. By sequencing TCRs from a patient's blood or tissue, you're essentially asking: **"Which T cells are actively fighting the body's own cells, and how much are they expanding?"**

### Tracking Disease Progression

#### Private TCRs Tell Individual Story

If you see new, expanding clones of T cells targeting beta cell antigens (like insulin or GAD), that signals disease is progressing in **that person**. You're watching their immune system ramp up the attack. Conversely, if autoreactive clones are shrinking, treatment might be working.

#### Public TCRs Reveal Shared Mechanisms

Many T1D patients independently develop the same TCR sequences targeting the same beta cell proteins. These public clonotypes are like "weak points" in beta cells—TCRs that are particularly good at recognizing them. Finding public TCRs across patients tells you which immune attacks are most universal and dangerous, which could guide vaccine or treatment development.

### Practical Questions TCR Analysis Answers

- **Disease stage:** Are autoreactive T cells expanding (active disease) or stable (established disease)?
- **Prognosis:** Do patients with certain TCR profiles progress faster toward needing insulin?
- **Treatment response:** Are immunotherapies actually shrinking the autoreactive clones?
- **Heterogeneity:** Why do some patients progress slowly while others are aggressive? Different TCR repertoires could explain different disease courses in "the same disease."

In your work with clinical research participants, **TCR sequencing lets you map individual immune states over time**—essentially reading out which biological "war" is happening inside each person.

---

## TCR-Based Biomarkers & Drug Development

### Predictive Potential

Yes, research suggests certain TCRs—especially public ones—could predict rapid progression to insulin-dependence. If you identify that a newly diagnosed patient carries specific high-risk clonotypes, you'd know they're on a fast trajectory toward complete beta cell loss.

This is far more granular than current diagnostics, which mostly just check "do you have antibodies against beta cells?" (yes/no), without predicting **how fast** you'll progress.

### How This Transforms Drug Development

#### Patient Stratification

Instead of enrolling "all Type 1 Diabetes patients" in a trial, you'd stratify by TCR profile. A drug that works brilliantly for patients with public clonotype X might be wasted on patients with private clonotypes. This dramatically improves trial signal-to-noise and approval chances.

#### Preventive Intervention (The Game-Changer)

Currently, by the time someone is diagnosed with T1D, they've already lost 80-90% of their beta cells. But if you could identify someone at genetic/immune risk **before diagnosis** (say, a sibling of a T1D patient with dangerous TCRs), you could treat them prophylactically.

Instead of managing established disease, you **prevent it**.

#### Rational Drug Targets

Once you know which public TCRs are driving disease, you can design drugs specifically to kill those T cells or block those particular receptors. Rather than broad immunosuppression (which causes infections), you'd do **"sniper" immunotherapy**—targeted elimination of the problematic cells.

#### Responder Prediction

Before giving someone an expensive biologic, you could test whether their TCR profile suggests they'll respond. Saves money and lets patients avoid useless treatments.

### Real-World Impact

Imagine: a teenager tests positive for beta cell antibodies. TCR sequencing shows they carry three of the most aggressive public clonotypes associated with rapid progression. Instead of waiting for symptoms, you offer them a monoclonal antibody therapy targeting those exact TCRs. Their beta cell destruction slows or stops, and they avoid diabetes entirely—or delay it decades. Their sibling doesn't carry those TCRs, so no treatment needed.

This is fundamentally different from current medicine, which is mostly reactive.

---

## Teplizumab: Current Clinical Reality

### What Teplizumab Does

Teplizumab is an **anti-CD3 monoclonal antibody**. Instead of targeting *specific* TCRs, it targets CD3—a protein that's on the surface of *all* T cells. When you inject teplizumab, it essentially depletes or inactivates a broad swath of T cells, including (hopefully) the autoreactive ones attacking beta cells.

**It's NOT TCR-specific**—it's more of a "broad-spectrum reduction of T cell numbers" approach rather than the sniper approach described above.

### Why It Works (and Why It's Limited)

It works because reducing total T cell burden reduces autoimmune attack, even without targeting specific cells. The FDA approved it in 2023 based on the **DELAY trial**, which showed it delayed T1D onset in at-risk people (those with beta cell autoimmunity but not yet diabetic).

This is genuinely the **preventive approach**—intervening before diagnosis.

But it has downsides: you're suppressing your entire T cell population, which increases infection risk and other immune complications. **It's immunosuppression with a sledgehammer.**

### The Future Direction

What researchers are working toward—and where TCR analysis becomes critical—is exactly what you asked: drugs targeting **specific autoreactive TCRs or clonotypes**. Teplizumab is the current clinical option, but it's a stepping stone. 

TCR sequencing in patients would identify which of them carry the worst clonotypes, potentially predicting who benefits most from teplizumab (or who needs something more targeted).

So teplizumab is **proof the preventive concept works**, but TCR-profiling would make future therapies far more precise.

---

## Database Structure Design

### Core Motivation

If you build a MongoDB database that can load TCR from multiple libraries (samples) for a range of disease types, you need a structure that supports:

1. **Tracking disease trajectory over time** (temporal dimension is critical)
2. **Identifying which clonotypes drive disease** (frequency and expansion patterns)
3. **Comparing public vs. private repertoires** across cohorts
4. **Correlating TCR patterns with clinical outcomes** (is this clonotype associated with rapid progression?)

### Core Collections

#### Patients

Top-level entity containing:
- `patient_id`, `disease_diagnosis` (Type 1 Diabetes, healthy control, etc.)
- `disease_stage`, `genetic_markers` (relevant to autoimmunity)
- `treatment_history`, key outcomes (`insulin_dependent: yes/no`, `progression_rate`)

**Key insight:** You're tracking disease trajectory, so you need temporal metadata built in.

#### Samples

Each document represents a single biological sample:
- Links to `patient_id`
- `sample_type` (blood draw, tissue biopsy)
- `timepoint` (day 0, month 3, month 12 after diagnosis)
- `processing_info`, `sequencing_depth`

**This temporal dimension is critical for tracking clonal expansion over time.**

#### TCR Clonotypes

Each clonotype is defined by its **CDR3 sequence** (the variable part that actually binds antigen) plus V-gene and J-gene segments:
- `clonotype_id` (hash or canonical ID)
- Full nucleotide and amino acid sequences
- `is_public`, and if public, reference to canonical public version
- `associated_antigens` (insulin, GAD, etc. for T1D)
- Pulled from literature or databases like IEDB

#### Clonal Abundance

The link between clonotypes and samples:
- `clonotype_id`, `sample_id`
- `count` (raw number of reads), `frequency` (percentage of all T cells)

**This is what lets you track clonal expansion.** Query: "Show me this clonotype's frequency across all timepoints for patient X" and see if it's growing (bad) or shrinking (treatment working).

#### Public TCR Registry (Optional but Useful)

Deduplicated collection of known public clonotypes:
- `public_clonotype_id`, `canonical_cdr3`
- `associated_antigens`, `diseases`, `patients_carrying` (array)
- `literature_refs`

Instead of replicating the same public clonotype data across many clonotype documents, you'd have a canonical entry. Then clonotypes reference it.

### Key Design Decisions

#### Denormalization for Speed

In MongoDB, you'd probably denormalize more than in SQL. For example, in each Clonal Abundance document, you might embed the disease status from the patient ("T1D progressor", "T1D stable") so you can query "give me all clonotypes expanding in progressors" without joining across collections.

#### Indexing Strategy

You'd want indexes on:
- `patient_id` (to pull all samples/clonotypes for one person)
- `sample_id`
- `clonotype_id`
- Compound index on `(clonotype_id, sample_id, timepoint)` to efficiently track individual clonotypes over time

#### Array Fields for Disease Associations

Public clonotypes would have an array of associated diseases and target antigens, so you can quickly ask "which clonotypes target insulin?" or "how many patients carry the DELAY trial-associated public clonotypes?"

### Query Patterns to Support

The database structure should make these queries fast:

- "For all T1D progressors, what are the most expanded clonotypes in the first 6 months?" (helps identify high-risk markers)
- "Show me public clonotypes that appear in >5% of patients with disease X" (identifies universal weak points)
- "Track patient X's clonotypes from diagnosis to month 12—which ones expanded, which contracted?" (treatment response)

### Approximate MongoDB Schema

```javascript
db.patients: {
  patient_id,
  disease_type,
  disease_status,
  genetic_markers,
  treatment_history,
  outcomes
}

db.samples: {
  sample_id,
  patient_id,
  timepoint,
  sample_type,
  sequencing_depth
}

db.tcr_clonotypes: {
  clonotype_id,
  cdr3_aa,
  cdr3_nt,
  v_gene,
  j_gene,
  is_public,
  public_clonotype_id_ref,
  target_antigen,
  disease_associations
}

db.clonal_abundance: {
  clonotype_id,
  sample_id,
  count,
  frequency,
  patient_disease_status  // denormalized for queries
}

db.public_tcr_registry: {
  public_clonotype_id,
  canonical_cdr3,
  target_antigen,
  diseases,
  patients_carrying,  // array
  literature_refs
}
```

---

## Data Deduplication Pipeline

### Why Duplicates Exist

TCR sequencing reads the CDR3 region repeatedly across millions of cells. But sequencing has an error rate (~0.1-1% per base depending on sequencer and chemistry). So the "true" clonotype `GGGAAATTT` might also appear as `GGGAAATCT` (one-base error), and these look like two different clonotypes even though they're the same.

When you're trying to identify rare clones and track frequencies, a single clonotype scattered across 5 slightly-different sequences **destroys your signal**.

### Where It Fits in the Pipeline

```
Raw FASTQ files
    ↓
Trim adapters, filter low-quality reads (cutadapt, fastp)
    ↓
Align to reference TCR genes (IMGT, BLAST)
    ↓
Extract CDR3 sequences
    ↓
**DEDUPLICATION/CLUSTERING** ← This is the step
    ↓
Count clonotype frequencies
    ↓
Assign clonotype IDs
    ↓
Database insertion
```

### How It's Actually Done

#### Clustering by Sequence Similarity

Most approaches cluster CDR3 sequences (both nucleotide and amino acid versions) where sequences within a certain Hamming distance or edit distance are grouped together. The typical threshold is **1-2 mismatches for nucleotide sequences**.

#### Python Approach (Increasingly Common)

Use libraries like:
- `scikit-learn` for sequence clustering
- `parasail` for fast pairwise alignment

Pipeline:
1. Read extracted CDR3 sequences
2. Perform pairwise comparisons with edit distance/Hamming distance
3. Cluster sequences within your threshold (usually 1 mismatch)
4. Pick representative sequence (usually most abundant or longest) as canonical clonotype
5. Map all reads back to their canonical clonotype

#### R Approach

R packages like `stringdist` and `cluster` can do this, but R is typically slower for large-scale sequence comparisons. Some labs do use R if more comfortable with it.

#### Specialized Tools

Several dedicated TCR analysis tools handle this:
- **immcantation** (R/Python framework) — very comprehensive
- **MixCR** (Java-based, industry standard) — handles whole pipeline including deduplication
- **TRUST4** — specifically for TCR assembly and deduplication
- **VDJtools** (Java) — post-processing of TCR data

### Practical Implementation Decision at Benaroya

**Option 1 (Recommended):** Use MixCR or immcantation as your upstream processing tool. They handle quality filtering, TCR assignment, *and* deduplication automatically. Output a cleaned abundance matrix or clonotype table ready for database insertion.

**Option 2:** Write a Python pipeline using `parasail` or `biopython` for alignment, then use `scipy.cluster` for clustering. More flexible but requires careful validation.

**Option 3:** Use existing R package if your team is heavily R-oriented, but acknowledge you might hit performance issues at scale.

### MixCR vs. TRUST4: When to Revisit

Currently at Benaroya you use **MixCR**, but periodic validation is important:

#### Red Flags to Run TRUST4

1. **Unexpectedly low clonotype recovery** — If top 10 clonotypes only explain 40% of sample when you expected 70%+
2. **Validation mismatches** — If qPCR or known clonotypes don't match MixCR calls
3. **Weird diversity metrics** — Anomalously flat or constrained diversity
4. **Samples with unusual quality** — Low input material, contamination, non-standard chemistry

#### When TRUST4 is Genuinely Better

- **Novel TCRs or non-reference sequences** (tumor TILs, heavily mutated clones)
- **Non-human organisms** (if studying mice, primates)
- **Protocol changes** (switching 10X chemistry versions)

#### Recommended Periodic Audit

Every 6-12 months:
- Pick 3-5 diverse samples (progressor, stable, control)
- Run both MixCR and TRUST4
- Compare: total clonotype count, top 20 clonotypes, frequencies, overall recovery
- If they agree on major clonotypes, you're good. If they diverge, investigate further.

### Database Implication

Once deduplicated, clonotypes going into database are "canonical" representations. Store metadata about this:
- `canonical_cdr3`
- Notes: `"clustered from 23 raw sequences, error threshold 1bp"`

This lets you track data quality and reproduce results later.

**Key insight:** Deduplication happens **before the database, not within it.** Your database stores clean, deduplicated clonotypes.

---

## User Interface & Query Patterns

### Core Query Patterns Researchers Need

1. **Cohort exploration:** "Show me all T1D progressors diagnosed in 2023, filter by clonotype diversity"
2. **Clonotype hunting:** "Find all patients carrying this public clonotype" or "Show me the top expanding clonotypes in the first 6 months post-diagnosis"
3. **Temporal tracking:** "Plot this patient's clonotype frequencies from diagnosis to month 12"
4. **Comparative analysis:** "Compare the public clonotype repertoire of progressors vs. stable patients"
5. **Export for downstream:** "Give me a CSV of all clonotypes from cohort X for pathway analysis"

### Interface Architecture

Three main views:

#### 1. Search Hub
Find patients/samples/clonotypes with:
- **Clonotype lookup:** "Find all patients with this TCR"
- **Patient lookup:** "Show me this patient's clonal evolution"
- **Cohort analysis:** "Compare public TCRs across disease progressors vs. stable patients"

Features:
- Quick stats cards showing database scope (2.4K public TCRs, 847 patients, 3.2K samples)
- Flexible search type selector (clonotype/patient/cohort)
- Intelligent filters (only public, insulin-targeting, etc.)

#### 2. Results Explorer
Sortable, filterable table of findings:
- **Frequency column** — Which clonotypes dominate
- **Patient count** — "Is this public or rare?"
- **Type badge** — Public (red) vs. Private (gray)
- **Export button** — Pull data for downstream analysis in R, Python, Seurat
- **Cohort comparison chart** — Visual summary of how public vs. private TCRs differ across disease groups

#### 3. Patient Detail View
Zoom into one patient's trajectory:
- **Time-series plot** — Clonal expansion from diagnosis → month 12 (identifies rapid progressors)
- **Expanding clonotypes table** — Which TCRs drive disease (public vs. private matters)
- **Risk indicators** — "This patient carries 3 high-risk public clonotypes"

### Real Queries This Enables

**"Which TCRs predict rapid progression?"**
→ Filter cohort view for "Progressors" only, identify top expanding public clonotypes, export for machine learning

**"Find all patients with insulin-targeting TCRs"**
→ Search by antigen filter, get all 47 patients carrying CASSGYSNQPQHF, download their metadata for follow-up studies

**"Does MixCR vs. TRUST4 change clonotype calls?"**
→ Run both pipelines, query same patient in UI with both assembly methods, compare top clonotypes

**"Which patients are outliers in their cohort?"**
→ Look at clonal diversity metrics in cohort comparison, identify patient X with unusually flat repertoire

### Technical Architecture

```
Frontend (React UI)
    ↓
API Layer (Node.js Express / GraphQL)
    ↓
MongoDB Queries
  - db.clonal_abundance.aggregate() for time-series data
  - db.tcr_clonotypes.find() for clonotype metadata
  - db.patients.aggregate() for cohort statistics
```

You could also expose a **MongoDB query interface for power users** (researchers who want raw aggregation queries), but the UI handles 80% of use cases without needing to write pipelines.

### Additional Considerations

#### Export Formats
CSV (Excel), JSON (downstream bioinformatics), TSV (R)

#### Sharing & Reproducibility
Each search result gets a shareable URL: `/tcr-explorer?cohort=T1D-progressors&filters=public-insulin-targeting`

Makes collaboration and publication reproducible.

#### Performance at Scale
With 3K+ samples, you need:
- Indexes on `(patient_id, disease_status, timepoint)` for fast patient lookups
- Materialized views for cohort statistics (precompute rather than aggregate on every query)
- Frontend pagination for large result sets

---

## Implementation Roadmap

### Phase 1: Database Foundation
- [ ] Design MongoDB schema (patients, samples, clonotypes, clonal_abundance)
- [ ] Set up indexes for common queries
- [ ] Create ETL pipeline from MixCR output → MongoDB
- [ ] Write basic CRUD operations and aggregation functions

### Phase 2: Backend API
- [ ] Build REST API (or GraphQL) for core query patterns
- [ ] Implement authentication/authorization (who can access what)
- [ ] Add caching layer for cohort statistics
- [ ] Create export endpoints (CSV, JSON, TSV)

### Phase 3: Frontend UI
- [ ] Build Search Hub with flexible query builder
- [ ] Implement Results Explorer with sorting/filtering
- [ ] Create Patient Detail view with time-series visualization
- [ ] Add cohort comparison charts

### Phase 4: Validation & Optimization
- [ ] Run periodic validation (MixCR vs. TRUST4 on pilot samples)
- [ ] Performance testing at scale (3K+ samples)
- [ ] User feedback from immunology team
- [ ] Refinement based on real-world usage patterns

### Phase 5: Advanced Features
- [ ] TCR-based biomarker prediction models
- [ ] Integration with clinical outcomes (who progressed, who stayed stable)
- [ ] Automated alerts ("New high-risk clonotype detected in cohort")
- [ ] Collaboration features (shared workspaces, annotations)

---

## Conclusion

Building a TCR database is fundamentally about making it **easy for researchers to ask biological questions** and get answers quickly. The design should:

1. **Lower barriers to exploration** — Search hub should be intuitive for non-bioinformaticians
2. **Visualize temporal patterns** — Disease progression is a story over time
3. **Support statistical comparison** — Public vs. private, progressors vs. stable
4. **Enable reproducibility** — Shareable URLs, documented query history
5. **Export for downstream analysis** — Don't lock researchers into your UI

The success of this database will ultimately be measured by how many research hypotheses it enables and how much time it saves your team from manual data wrangling.

---

**Document Generated:** January 14, 2026  
**Scope:** TCR database design, bioinformatics pipeline, UI/UX architecture  
**Use Case:** Type 1 Diabetes research at Benaroya Research Institute