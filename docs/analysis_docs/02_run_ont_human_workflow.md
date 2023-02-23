# 02 - Run ont_human_workflow

Created: 2022/12/22 13:55:37
Last modified: 2023/02/22 14:11:16

- **Aim:** This document documents/describes running [ont_human_workflow](https://github.com/leahkemp/ont_human_workflow)
- **Prerequisite software:** See software dependecies outlined in [ont_human_workflow](https://github.com/leahkemp/ont_human_workflow)
- **OS:** ORAC (CentOS Linux) (ESR production network)

## Table of contents

- [02 - Run ont\_human\_workflow](#02---run-ont_human_workflow)
  - [Table of contents](#table-of-contents)
  - [Run ont\_human\_workflow](#run-ont_human_workflow)

## Run ont_human_workflow

Run through the [analysis documentation for ont_human_workflow](https://github.com/leahkemp/ont_human_workflow/tree/f57cc4830b39289eafdb2f472f3ae441e351c0bc/docs/analysis_docs) as of commit [f57cc4830b39289eafdb2f472f3ae441e351c0bc](https://github.com/leahkemp/ont_human_workflow/tree/f57cc4830b39289eafdb2f472f3ae441e351c0bc)

---

Note. I was getting an error on the [./scripts/module_scripts/02-ont-bam-merge.sh](./scripts/module_scripts/02-ont-bam-merge.sh) when analysing the AB1052B sample (Adipose_AS_ours_new_extraction) despite trying to re-basecall. I'd get the following error:

```bash
bamtools merge ERROR: could not open input BAM file list... Aborting.
```

To resolve the issue, I found the bam that was causing the error and removed it before re-running the bam merge step and continuing on with the analysis of this sample. The files I removed:

- ./results/01-ont-guppy-gpu/AB1052B/pass/bam_runid_6bbfb8fcec255bf70d4cff5b7f2140925fe57412_263_0.bam
- ./results/01-ont-guppy-gpu/AB1052B/pass/bam_runid_6bbfb8fcec255bf70d4cff5b7f2140925fe57412_263_0.bam.bai
- ./results/01-ont-guppy-gpu/AB1052B/pass/bam_runid_6bbfb8fcec255bf70d4cff5b7f2140925fe57412_2631_0.bam
- ./results/01-ont-guppy-gpu/AB1052B/pass/bam_runid_6bbfb8fcec255bf70d4cff5b7f2140925fe57412_2631_0.bam.bai

---
