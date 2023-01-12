# 03 - Cleanup

Created: 2023/01/12 10:55:21
Last modified: 2023/01/13 12:43:06

- **Aim:** This document outlines how to back up the analyses on the dedicated space on production and cleanup
- **Prerequisite software:** [rsync](https://rsync.samba.org/)
- **OS:** ORAC (CentOS Linux) (ESR production network)

## Table of contents

- [03 - Cleanup](#03---cleanup)
  - [Table of contents](#table-of-contents)
  - [Backup analyses and cleanup](#backup-analyses-and-cleanup)
  - [Output files](#output-files)

## Backup analyses and cleanup

Minimal analyses have already been backed up at `/NGS/clinicalgenomics/archive/2022/results/adipose_ont_methylation/`

Backup the README before cleaning up

```bash
rsync -av /NGS/humangenomics/active/2022/run/adipose_ont_methylation/README.md /NGS/clinicalgenomics/archive/2022/results/adipose_ont_methylation/
```

Cleanup analyses

```bash
rm -rf /NGS/humangenomics/active/2022/run/ont_human_workflow/
```

## Output files

Have a look at the final output files

```bash
tree -hv /NGS/clinicalgenomics/archive/2022/results/adipose_ont_methylation/
```

<details><summary markdown="span">My output (click to expand)</summary>

```bash
/NGS/clinicalgenomics/archive/2022/results/adipose_ont_methylation/
├── [ 127]  Adipose_AS_RRMS
│   ├── [1.9K]  CNV
│   │   ├── [244K]  AB740B_fastq_bins.bed
│   │   ├── [223K]  AB740B_fastq_calls.bed
│   │   ├── [ 791]  AB740B_fastq_calls.vcf
│   │   ├── [254K]  AB740B_fastq_combined.bed
│   │   ├── [ 31K]  AB740B_fastq_cov.png
│   │   ├── [ 22K]  AB740B_fastq_isobar_plot.png
│   │   ├── [7.2K]  AB740B_fastq_noise_plot.png
│   │   ├── [1.1M]  AB740B_fastq_plots.pdf
│   │   ├── [274K]  AB740B_fastq_raw_bins.bed
│   │   ├── [243K]  AB740B_fastq_segs.bed
│   │   ├── [  46]  AB740B_fastq_segs.seg
│   │   ├── [ 791]  AB740B_fastq_segs.vcf
│   │   ├── [244K]  AB755B_fastq_bins.bed
│   │   ├── [223K]  AB755B_fastq_calls.bed
│   │   ├── [ 791]  AB755B_fastq_calls.vcf
│   │   ├── [254K]  AB755B_fastq_combined.bed
│   │   ├── [ 31K]  AB755B_fastq_cov.png
│   │   ├── [ 21K]  AB755B_fastq_isobar_plot.png
│   │   ├── [6.6K]  AB755B_fastq_noise_plot.png
│   │   ├── [1.1M]  AB755B_fastq_plots.pdf
│   │   ├── [269K]  AB755B_fastq_raw_bins.bed
│   │   ├── [241K]  AB755B_fastq_segs.bed
│   │   ├── [  46]  AB755B_fastq_segs.seg
│   │   ├── [ 791]  AB755B_fastq_segs.vcf
│   │   ├── [244K]  OM1052A_fastq_bins.bed
│   │   ├── [223K]  OM1052A_fastq_calls.bed
│   │   ├── [ 791]  OM1052A_fastq_calls.vcf
│   │   ├── [254K]  OM1052A_fastq_combined.bed
│   │   ├── [ 30K]  OM1052A_fastq_cov.png
│   │   ├── [ 23K]  OM1052A_fastq_isobar_plot.png
│   │   ├── [6.8K]  OM1052A_fastq_noise_plot.png
│   │   ├── [987K]  OM1052A_fastq_plots.pdf
│   │   ├── [274K]  OM1052A_fastq_raw_bins.bed
│   │   ├── [242K]  OM1052A_fastq_segs.bed
│   │   ├── [  46]  OM1052A_fastq_segs.seg
│   │   ├── [ 791]  OM1052A_fastq_segs.vcf
│   │   ├── [244K]  OM1052B_fastq_bins.bed
│   │   ├── [223K]  OM1052B_fastq_calls.bed
│   │   ├── [ 791]  OM1052B_fastq_calls.vcf
│   │   ├── [254K]  OM1052B_fastq_combined.bed
│   │   ├── [ 33K]  OM1052B_fastq_cov.png
│   │   ├── [ 34K]  OM1052B_fastq_isobar_plot.png
│   │   ├── [5.8K]  OM1052B_fastq_noise_plot.png
│   │   ├── [1.1M]  OM1052B_fastq_plots.pdf
│   │   ├── [269K]  OM1052B_fastq_raw_bins.bed
│   │   ├── [245K]  OM1052B_fastq_segs.bed
│   │   ├── [  46]  OM1052B_fastq_segs.seg
│   │   └── [ 791]  OM1052B_fastq_segs.vcf
│   ├── [ 590]  QC
│   │   ├── [3.4M]  AB740B.wf-human-snp-report.html
│   │   ├── [3.7M]  AB740B.wf-human-sv-report.html
│   │   ├── [1.7M]  AB740B_fastq_wf-cnv-report.html
│   │   ├── [3.4M]  AB755B.wf-human-snp-report.html
│   │   ├── [3.7M]  AB755B.wf-human-sv-report.html
│   │   ├── [1.7M]  AB755B_fastq_wf-cnv-report.html
│   │   ├── [3.4M]  OM1052A.wf-human-snp-report.html
│   │   ├── [3.7M]  OM1052A.wf-human-sv-report.html
│   │   ├── [1.7M]  OM1052A_fastq_wf-cnv-report.html
│   │   ├── [3.4M]  OM1052B.wf-human-snp-report.html
│   │   ├── [3.6M]  OM1052B.wf-human-sv-report.html
│   │   └── [1.7M]  OM1052B_fastq_wf-cnv-report.html
│   ├── [ 324]  SNP
│   │   ├── [ 31M]  AB740B.wf_snp.vcf.gz
│   │   ├── [1.5M]  AB740B.wf_snp.vcf.gz.tbi
│   │   ├── [ 23M]  AB755B.wf_snp.vcf.gz
│   │   ├── [1.4M]  AB755B.wf_snp.vcf.gz.tbi
│   │   ├── [ 32M]  OM1052A.wf_snp.vcf.gz
│   │   ├── [1.5M]  OM1052A.wf_snp.vcf.gz.tbi
│   │   ├── [ 17M]  OM1052B.wf_snp.vcf.gz
│   │   └── [1.3M]  OM1052B.wf_snp.vcf.gz.tbi
│   ├── [  68]  SV
│   │   ├── [ 166]  cutesv
│   │   │   ├── [146K]  AB740B_sv_cutesv.vcf.gz
│   │   │   ├── [143K]  AB755B_sv_cutesv.vcf.gz
│   │   │   ├── [103K]  OM1052A_sv_cutesv.vcf.gz
│   │   │   └── [ 59K]  OM1052B_sv_cutesv.vcf.gz
│   │   └── [ 316]  wf-human-variation-calling
│   │       ├── [1.4M]  AB740B.wf_sv.vcf.gz
│   │       ├── [ 68K]  AB740B.wf_sv.vcf.gz.tbi
│   │       ├── [1.4M]  AB755B.wf_sv.vcf.gz
│   │       ├── [ 68K]  AB755B.wf_sv.vcf.gz.tbi
│   │       ├── [1.2M]  OM1052A.wf_sv.vcf.gz
│   │       ├── [ 61K]  OM1052A.wf_sv.vcf.gz.tbi
│   │       ├── [999K]  OM1052B.wf_sv.vcf.gz
│   │       └── [ 55K]  OM1052B.wf_sv.vcf.gz.tbi
│   ├── [ 380]  bam
│   │   ├── [ 12G]  AB740B_sorted_merged.hp.bam
│   │   ├── [5.7M]  AB740B_sorted_merged.hp.bam.bai
│   │   ├── [8.6G]  AB755B_sorted_merged.hp.bam
│   │   ├── [4.8M]  AB755B_sorted_merged.hp.bam.bai
│   │   ├── [ 11G]  OM1052A_sorted_merged.hp.bam
│   │   ├── [5.5M]  OM1052A_sorted_merged.hp.bam.bai
│   │   ├── [6.1G]  OM1052B_sorted_merged.hp.bam
│   │   └── [3.7M]  OM1052B_sorted_merged.hp.bam.bai
│   └── [ 836]  methyl
│       ├── [440M]  AB740B_methylation.aggregated.cpg.bed.gz
│       ├── [190M]  AB740B_methylation.hp1.cpg.bed.gz
│       ├── [191M]  AB740B_methylation.hp2.cpg.bed.gz
│       ├── [1.7G]  AB740B_mod-counts.cpg.acc.bed
│       ├── [390M]  AB755B_methylation.aggregated.cpg.bed.gz
│       ├── [180M]  AB755B_methylation.hp1.cpg.bed.gz
│       ├── [182M]  AB755B_methylation.hp2.cpg.bed.gz
│       ├── [1.5G]  AB755B_mod-counts.cpg.acc.bed
│       ├── [442M]  OM1052A_methylation.aggregated.cpg.bed.gz
│       ├── [175M]  OM1052A_methylation.hp1.cpg.bed.gz
│       ├── [175M]  OM1052A_methylation.hp2.cpg.bed.gz
│       ├── [1.7G]  OM1052A_mod-counts.cpg.acc.bed
│       ├── [347M]  OM1052B_methylation.aggregated.cpg.bed.gz
│       ├── [146M]  OM1052B_methylation.hp1.cpg.bed.gz
│       ├── [148M]  OM1052B_methylation.hp2.cpg.bed.gz
│       └── [1.4G]  OM1052B_mod-counts.cpg.acc.bed
└── [ 127]  Adipose_AS_ours
    ├── [5.3K]  CNV
    │   ├── [244K]  AB526A_fastq_bins.bed
    │   ├── [223K]  AB526A_fastq_calls.bed
    │   ├── [ 791]  AB526A_fastq_calls.vcf
    │   ├── [254K]  AB526A_fastq_combined.bed
    │   ├── [ 30K]  AB526A_fastq_cov.png
    │   ├── [ 26K]  AB526A_fastq_isobar_plot.png
    │   ├── [6.6K]  AB526A_fastq_noise_plot.png
    │   ├── [800K]  AB526A_fastq_plots.pdf
    │   ├── [274K]  AB526A_fastq_raw_bins.bed
    │   ├── [244K]  AB526A_fastq_segs.bed
    │   ├── [  46]  AB526A_fastq_segs.seg
    │   ├── [ 791]  AB526A_fastq_segs.vcf
    │   ├── [244K]  AB526B_fastq_bins.bed
    │   ├── [223K]  AB526B_fastq_calls.bed
    │   ├── [ 791]  AB526B_fastq_calls.vcf
    │   ├── [254K]  AB526B_fastq_combined.bed
    │   ├── [ 30K]  AB526B_fastq_cov.png
    │   ├── [ 24K]  AB526B_fastq_isobar_plot.png
    │   ├── [6.3K]  AB526B_fastq_noise_plot.png
    │   ├── [795K]  AB526B_fastq_plots.pdf
    │   ├── [274K]  AB526B_fastq_raw_bins.bed
    │   ├── [241K]  AB526B_fastq_segs.bed
    │   ├── [  46]  AB526B_fastq_segs.seg
    │   ├── [ 791]  AB526B_fastq_segs.vcf
    │   ├── [244K]  AB740B_fastq_bins.bed
    │   ├── [223K]  AB740B_fastq_calls.bed
    │   ├── [ 791]  AB740B_fastq_calls.vcf
    │   ├── [254K]  AB740B_fastq_combined.bed
    │   ├── [ 30K]  AB740B_fastq_cov.png
    │   ├── [ 36K]  AB740B_fastq_isobar_plot.png
    │   ├── [6.7K]  AB740B_fastq_noise_plot.png
    │   ├── [800K]  AB740B_fastq_plots.pdf
    │   ├── [275K]  AB740B_fastq_raw_bins.bed
    │   ├── [239K]  AB740B_fastq_segs.bed
    │   ├── [  46]  AB740B_fastq_segs.seg
    │   ├── [ 791]  AB740B_fastq_segs.vcf
    │   ├── [244K]  AB755A_fastq_bins.bed
    │   ├── [223K]  AB755A_fastq_calls.bed
    │   ├── [ 791]  AB755A_fastq_calls.vcf
    │   ├── [254K]  AB755A_fastq_combined.bed
    │   ├── [ 30K]  AB755A_fastq_cov.png
    │   ├── [ 30K]  AB755A_fastq_isobar_plot.png
    │   ├── [6.2K]  AB755A_fastq_noise_plot.png
    │   ├── [796K]  AB755A_fastq_plots.pdf
    │   ├── [274K]  AB755A_fastq_raw_bins.bed
    │   ├── [245K]  AB755A_fastq_segs.bed
    │   ├── [  46]  AB755A_fastq_segs.seg
    │   ├── [ 791]  AB755A_fastq_segs.vcf
    │   ├── [244K]  AB755B_fastq_bins.bed
    │   ├── [223K]  AB755B_fastq_calls.bed
    │   ├── [ 791]  AB755B_fastq_calls.vcf
    │   ├── [254K]  AB755B_fastq_combined.bed
    │   ├── [ 30K]  AB755B_fastq_cov.png
    │   ├── [ 33K]  AB755B_fastq_isobar_plot.png
    │   ├── [6.7K]  AB755B_fastq_noise_plot.png
    │   ├── [802K]  AB755B_fastq_plots.pdf
    │   ├── [275K]  AB755B_fastq_raw_bins.bed
    │   ├── [245K]  AB755B_fastq_segs.bed
    │   ├── [  46]  AB755B_fastq_segs.seg
    │   ├── [ 791]  AB755B_fastq_segs.vcf
    │   ├── [244K]  AB792A_fastq_bins.bed
    │   ├── [223K]  AB792A_fastq_calls.bed
    │   ├── [ 791]  AB792A_fastq_calls.vcf
    │   ├── [254K]  AB792A_fastq_combined.bed
    │   ├── [ 30K]  AB792A_fastq_cov.png
    │   ├── [ 31K]  AB792A_fastq_isobar_plot.png
    │   ├── [6.6K]  AB792A_fastq_noise_plot.png
    │   ├── [799K]  AB792A_fastq_plots.pdf
    │   ├── [275K]  AB792A_fastq_raw_bins.bed
    │   ├── [244K]  AB792A_fastq_segs.bed
    │   ├── [  46]  AB792A_fastq_segs.seg
    │   ├── [ 791]  AB792A_fastq_segs.vcf
    │   ├── [244K]  AB792B_fastq_bins.bed
    │   ├── [223K]  AB792B_fastq_calls.bed
    │   ├── [ 791]  AB792B_fastq_calls.vcf
    │   ├── [254K]  AB792B_fastq_combined.bed
    │   ├── [ 30K]  AB792B_fastq_cov.png
    │   ├── [ 22K]  AB792B_fastq_isobar_plot.png
    │   ├── [6.3K]  AB792B_fastq_noise_plot.png
    │   ├── [792K]  AB792B_fastq_plots.pdf
    │   ├── [275K]  AB792B_fastq_raw_bins.bed
    │   ├── [244K]  AB792B_fastq_segs.bed
    │   ├── [  46]  AB792B_fastq_segs.seg
    │   ├── [ 791]  AB792B_fastq_segs.vcf
    │   ├── [244K]  AB1052A_fastq_bins.bed
    │   ├── [223K]  AB1052A_fastq_calls.bed
    │   ├── [ 791]  AB1052A_fastq_calls.vcf
    │   ├── [254K]  AB1052A_fastq_combined.bed
    │   ├── [ 32K]  AB1052A_fastq_cov.png
    │   ├── [ 22K]  AB1052A_fastq_isobar_plot.png
    │   ├── [6.1K]  AB1052A_fastq_noise_plot.png
    │   ├── [1.1M]  AB1052A_fastq_plots.pdf
    │   ├── [274K]  AB1052A_fastq_raw_bins.bed
    │   ├── [245K]  AB1052A_fastq_segs.bed
    │   ├── [  46]  AB1052A_fastq_segs.seg
    │   ├── [ 791]  AB1052A_fastq_segs.vcf
    │   ├── [244K]  AB1052B_fastq_bins.bed
    │   ├── [223K]  AB1052B_fastq_calls.bed
    │   ├── [ 791]  AB1052B_fastq_calls.vcf
    │   ├── [254K]  AB1052B_fastq_combined.bed
    │   ├── [ 31K]  AB1052B_fastq_cov.png
    │   ├── [ 18K]  AB1052B_fastq_isobar_plot.png
    │   ├── [6.2K]  AB1052B_fastq_noise_plot.png
    │   ├── [1.1M]  AB1052B_fastq_plots.pdf
    │   ├── [274K]  AB1052B_fastq_raw_bins.bed
    │   ├── [244K]  AB1052B_fastq_segs.bed
    │   ├── [  46]  AB1052B_fastq_segs.seg
    │   ├── [ 791]  AB1052B_fastq_segs.vcf
    │   ├── [244K]  OM1052A_fastq_bins.bed
    │   ├── [223K]  OM1052A_fastq_calls.bed
    │   ├── [ 791]  OM1052A_fastq_calls.vcf
    │   ├── [254K]  OM1052A_fastq_combined.bed
    │   ├── [ 30K]  OM1052A_fastq_cov.png
    │   ├── [ 25K]  OM1052A_fastq_isobar_plot.png
    │   ├── [6.7K]  OM1052A_fastq_noise_plot.png
    │   ├── [798K]  OM1052A_fastq_plots.pdf
    │   ├── [275K]  OM1052A_fastq_raw_bins.bed
    │   ├── [245K]  OM1052A_fastq_segs.bed
    │   ├── [  46]  OM1052A_fastq_segs.seg
    │   ├── [ 791]  OM1052A_fastq_segs.vcf
    │   ├── [244K]  OM1052B_fastq_bins.bed
    │   ├── [223K]  OM1052B_fastq_calls.bed
    │   ├── [ 791]  OM1052B_fastq_calls.vcf
    │   ├── [254K]  OM1052B_fastq_combined.bed
    │   ├── [ 29K]  OM1052B_fastq_cov.png
    │   ├── [ 24K]  OM1052B_fastq_isobar_plot.png
    │   ├── [6.5K]  OM1052B_fastq_noise_plot.png
    │   ├── [792K]  OM1052B_fastq_plots.pdf
    │   ├── [274K]  OM1052B_fastq_raw_bins.bed
    │   ├── [243K]  OM1052B_fastq_segs.bed
    │   ├── [  46]  OM1052B_fastq_segs.seg
    │   └── [ 791]  OM1052B_fastq_segs.vcf
    ├── [1.7K]  QC
    │   ├── [3.4M]  AB526A.wf-human-snp-report.html
    │   ├── [3.7M]  AB526A.wf-human-sv-report.html
    │   ├── [1.7M]  AB526A_fastq_wf-cnv-report.html
    │   ├── [3.4M]  AB526B.wf-human-snp-report.html
    │   ├── [3.8M]  AB526B.wf-human-sv-report.html
    │   ├── [1.7M]  AB526B_fastq_wf-cnv-report.html
    │   ├── [3.4M]  AB740A.wf-human-snp-report.html
    │   ├── [3.7M]  AB740A.wf-human-sv-report.html
    │   ├── [1.7M]  AB740A_fastq_wf-cnv-report.html
    │   ├── [3.4M]  AB740B.wf-human-snp-report.html
    │   ├── [3.8M]  AB740B.wf-human-sv-report.html
    │   ├── [1.7M]  AB740B_fastq_wf-cnv-report.html
    │   ├── [3.4M]  AB755A.wf-human-snp-report.html
    │   ├── [3.7M]  AB755A.wf-human-sv-report.html
    │   ├── [1.7M]  AB755A_fastq_wf-cnv-report.html
    │   ├── [3.4M]  AB755B.wf-human-snp-report.html
    │   ├── [3.8M]  AB755B.wf-human-sv-report.html
    │   ├── [1.7M]  AB755B_fastq_wf-cnv-report.html
    │   ├── [3.4M]  AB792A.wf-human-snp-report.html
    │   ├── [3.7M]  AB792A.wf-human-sv-report.html
    │   ├── [1.7M]  AB792A_fastq_wf-cnv-report.html
    │   ├── [3.4M]  AB792B.wf-human-snp-report.html
    │   ├── [3.8M]  AB792B.wf-human-sv-report.html
    │   ├── [1.7M]  AB792B_fastq_wf-cnv-report.html
    │   ├── [3.4M]  AB1052A.wf-human-snp-report.html
    │   ├── [3.8M]  AB1052A.wf-human-sv-report.html
    │   ├── [1.7M]  AB1052A_fastq_wf-cnv-report.html
    │   ├── [3.4M]  AB1052B.wf-human-snp-report.html
    │   ├── [3.8M]  AB1052B.wf-human-sv-report.html
    │   ├── [1.7M]  AB1052B_fastq_wf-cnv-report.html
    │   ├── [3.4M]  OM1052A.wf-human-snp-report.html
    │   ├── [3.8M]  OM1052A.wf-human-sv-report.html
    │   ├── [1.7M]  OM1052A_fastq_wf-cnv-report.html
    │   ├── [3.4M]  OM1052B.wf-human-snp-report.html
    │   ├── [3.8M]  OM1052B.wf-human-sv-report.html
    │   └── [1.7M]  OM1052B_fastq_wf-cnv-report.html
    ├── [ 968]  SNP
    │   ├── [ 46M]  AB526A.wf_snp.vcf.gz
    │   ├── [1.5M]  AB526A.wf_snp.vcf.gz.tbi
    │   ├── [ 51M]  AB526B.wf_snp.vcf.gz
    │   ├── [1.5M]  AB526B.wf_snp.vcf.gz.tbi
    │   ├── [ 45M]  AB740A.wf_snp.vcf.gz
    │   ├── [1.5M]  AB740A.wf_snp.vcf.gz.tbi
    │   ├── [ 44M]  AB740B.wf_snp.vcf.gz
    │   ├── [1.5M]  AB740B.wf_snp.vcf.gz.tbi
    │   ├── [ 44M]  AB755A.wf_snp.vcf.gz
    │   ├── [1.5M]  AB755A.wf_snp.vcf.gz.tbi
    │   ├── [ 43M]  AB755B.wf_snp.vcf.gz
    │   ├── [1.5M]  AB755B.wf_snp.vcf.gz.tbi
    │   ├── [ 42M]  AB792A.wf_snp.vcf.gz
    │   ├── [1.5M]  AB792A.wf_snp.vcf.gz.tbi
    │   ├── [ 47M]  AB792B.wf_snp.vcf.gz
    │   ├── [1.5M]  AB792B.wf_snp.vcf.gz.tbi
    │   ├── [ 34M]  AB1052A.wf_snp.vcf.gz
    │   ├── [1.5M]  AB1052A.wf_snp.vcf.gz.tbi
    │   ├── [ 37M]  AB1052B.wf_snp.vcf.gz
    │   ├── [1.5M]  AB1052B.wf_snp.vcf.gz.tbi
    │   ├── [ 42M]  OM1052A.wf_snp.vcf.gz
    │   ├── [1.5M]  OM1052A.wf_snp.vcf.gz.tbi
    │   ├── [ 49M]  OM1052B.wf_snp.vcf.gz
    │   └── [1.5M]  OM1052B.wf_snp.vcf.gz.tbi
    ├── [  68]  SV
    │   ├── [ 496]  cutesv
    │   │   ├── [221K]  AB526A_sv_cutesv.vcf.gz
    │   │   ├── [507K]  AB526B_sv_cutesv.vcf.gz
    │   │   ├── [104K]  AB740A_sv_cutesv.vcf.gz
    │   │   ├── [410K]  AB740B_sv_cutesv.vcf.gz
    │   │   ├── [164K]  AB755A_sv_cutesv.vcf.gz
    │   │   ├── [362K]  AB755B_sv_cutesv.vcf.gz
    │   │   ├── [ 83K]  AB792A_sv_cutesv.vcf.gz
    │   │   ├── [341K]  AB792B_sv_cutesv.vcf.gz
    │   │   ├── [308K]  AB1052A_sv_cutesv.vcf.gz
    │   │   ├── [343K]  AB1052B_sv_cutesv.vcf.gz
    │   │   ├── [198K]  OM1052A_sv_cutesv.vcf.gz
    │   │   └── [427K]  OM1052B_sv_cutesv.vcf.gz
    │   └── [ 944]  wf-human-variation-calling
    │       ├── [1.7M]  AB526A.wf_sv.vcf.gz
    │       ├── [ 85K]  AB526A.wf_sv.vcf.gz.tbi
    │       ├── [2.4M]  AB526B.wf_sv.vcf.gz
    │       ├── [102K]  AB526B.wf_sv.vcf.gz.tbi
    │       ├── [1.2M]  AB740A.wf_sv.vcf.gz
    │       ├── [ 69K]  AB740A.wf_sv.vcf.gz.tbi
    │       ├── [2.3M]  AB740B.wf_sv.vcf.gz
    │       ├── [102K]  AB740B.wf_sv.vcf.gz.tbi
    │       ├── [1.6M]  AB755A.wf_sv.vcf.gz
    │       ├── [ 84K]  AB755A.wf_sv.vcf.gz.tbi
    │       ├── [2.2M]  AB755B.wf_sv.vcf.gz
    │       ├── [100K]  AB755B.wf_sv.vcf.gz.tbi
    │       ├── [1.1M]  AB792A.wf_sv.vcf.gz
    │       ├── [ 65K]  AB792A.wf_sv.vcf.gz.tbi
    │       ├── [1.9M]  AB792B.wf_sv.vcf.gz
    │       ├── [ 89K]  AB792B.wf_sv.vcf.gz.tbi
    │       ├── [2.0M]  AB1052A.wf_sv.vcf.gz
    │       ├── [ 90K]  AB1052A.wf_sv.vcf.gz.tbi
    │       ├── [2.2M]  AB1052B.wf_sv.vcf.gz
    │       ├── [101K]  AB1052B.wf_sv.vcf.gz.tbi
    │       ├── [1.7M]  OM1052A.wf_sv.vcf.gz
    │       ├── [ 86K]  OM1052A.wf_sv.vcf.gz.tbi
    │       ├── [2.3M]  OM1052B.wf_sv.vcf.gz
    │       └── [ 99K]  OM1052B.wf_sv.vcf.gz.tbi
    ├── [1.1K]  bam
    │   ├── [ 18G]  AB526A_sorted_merged.hp.bam
    │   ├── [9.6M]  AB526A_sorted_merged.hp.bam.bai
    │   ├── [ 23G]  AB526B_sorted_merged.hp.bam
    │   ├── [ 12M]  AB526B_sorted_merged.hp.bam.bai
    │   ├── [ 18G]  AB740A_sorted_merged.hp.bam
    │   ├── [9.5M]  AB740A_sorted_merged.hp.bam.bai
    │   ├── [ 20G]  AB740B_sorted_merged.hp.bam
    │   ├── [ 11M]  AB740B_sorted_merged.hp.bam.bai
    │   ├── [ 18G]  AB755A_sorted_merged.hp.bam
    │   ├── [9.8M]  AB755A_sorted_merged.hp.bam.bai
    │   ├── [ 19G]  AB755B_sorted_merged.hp.bam
    │   ├── [ 10M]  AB755B_sorted_merged.hp.bam.bai
    │   ├── [ 16G]  AB792A_sorted_merged.hp.bam
    │   ├── [8.4M]  AB792A_sorted_merged.hp.bam.bai
    │   ├── [ 21G]  AB792B_sorted_merged.hp.bam
    │   ├── [ 11M]  AB792B_sorted_merged.hp.bam.bai
    │   ├── [ 15G]  AB1052A_sorted_merged.hp.bam
    │   ├── [8.1M]  AB1052A_sorted_merged.hp.bam.bai
    │   ├── [ 15G]  AB1052B_sorted_merged.hp.bam
    │   ├── [8.6M]  AB1052B_sorted_merged.hp.bam.bai
    │   ├── [ 17G]  OM1052A_sorted_merged.hp.bam
    │   ├── [9.3M]  OM1052A_sorted_merged.hp.bam.bai
    │   ├── [ 23G]  OM1052B_sorted_merged.hp.bam
    │   └── [ 12M]  OM1052B_sorted_merged.hp.bam.bai
    └── [2.4K]  methyl
        ├── [488M]  AB526A_methylation.aggregated.cpg.bed.gz
        ├── [255M]  AB526A_methylation.hp1.cpg.bed.gz
        ├── [257M]  AB526A_methylation.hp2.cpg.bed.gz
        ├── [1.9G]  AB526A_mod-counts.cpg.acc.bed
        ├── [503M]  AB526B_methylation.aggregated.cpg.bed.gz
        ├── [297M]  AB526B_methylation.hp1.cpg.bed.gz
        ├── [298M]  AB526B_methylation.hp2.cpg.bed.gz
        ├── [1.9G]  AB526B_mod-counts.cpg.acc.bed
        ├── [488M]  AB740A_methylation.aggregated.cpg.bed.gz
        ├── [221M]  AB740A_methylation.hp1.cpg.bed.gz
        ├── [219M]  AB740A_methylation.hp2.cpg.bed.gz
        ├── [1.9G]  AB740A_mod-counts.cpg.acc.bed
        ├── [490M]  AB740B_methylation.aggregated.cpg.bed.gz
        ├── [284M]  AB740B_methylation.hp1.cpg.bed.gz
        ├── [286M]  AB740B_methylation.hp2.cpg.bed.gz
        ├── [1.9G]  AB740B_mod-counts.cpg.acc.bed
        ├── [488M]  AB755A_methylation.aggregated.cpg.bed.gz
        ├── [253M]  AB755A_methylation.hp1.cpg.bed.gz
        ├── [253M]  AB755A_methylation.hp2.cpg.bed.gz
        ├── [1.9G]  AB755A_mod-counts.cpg.acc.bed
        ├── [488M]  AB755B_methylation.aggregated.cpg.bed.gz
        ├── [285M]  AB755B_methylation.hp1.cpg.bed.gz
        ├── [287M]  AB755B_methylation.hp2.cpg.bed.gz
        ├── [1.9G]  AB755B_mod-counts.cpg.acc.bed
        ├── [479M]  AB792A_methylation.aggregated.cpg.bed.gz
        ├── [213M]  AB792A_methylation.hp1.cpg.bed.gz
        ├── [212M]  AB792A_methylation.hp2.cpg.bed.gz
        ├── [1.8G]  AB792A_mod-counts.cpg.acc.bed
        ├── [498M]  AB792B_methylation.aggregated.cpg.bed.gz
        ├── [265M]  AB792B_methylation.hp1.cpg.bed.gz
        ├── [264M]  AB792B_methylation.hp2.cpg.bed.gz
        ├── [1.9G]  AB792B_mod-counts.cpg.acc.bed
        ├── [449M]  AB1052A_methylation.aggregated.cpg.bed.gz
        ├── [243M]  AB1052A_methylation.hp1.cpg.bed.gz
        ├── [246M]  AB1052A_methylation.hp2.cpg.bed.gz
        ├── [1.7G]  AB1052A_mod-counts.cpg.acc.bed
        ├── [458M]  AB1052B_methylation.aggregated.cpg.bed.gz
        ├── [275M]  AB1052B_methylation.hp1.cpg.bed.gz
        ├── [278M]  AB1052B_methylation.hp2.cpg.bed.gz
        ├── [1.8G]  AB1052B_mod-counts.cpg.acc.bed
        ├── [484M]  OM1052A_methylation.aggregated.cpg.bed.gz
        ├── [255M]  OM1052A_methylation.hp1.cpg.bed.gz
        ├── [255M]  OM1052A_methylation.hp2.cpg.bed.gz
        ├── [1.8G]  OM1052A_mod-counts.cpg.acc.bed
        ├── [504M]  OM1052B_methylation.aggregated.cpg.bed.gz
        ├── [291M]  OM1052B_methylation.hp1.cpg.bed.gz
        ├── [291M]  OM1052B_methylation.hp2.cpg.bed.gz
        └── [1.9G]  OM1052B_mod-counts.cpg.acc.bed

18 directories, 404 files
```

</details>
<br/>

Check it's size

```bash
du -sh /NGS/clinicalgenomics/archive/2022/results/adipose_ont_methylation/
```

<details><summary markdown="span">My output (click to expand)</summary>

```bash
411G    /NGS/clinicalgenomics/archive/2022/results/adipose_ont_methylation/
```

</details>
<br/>
