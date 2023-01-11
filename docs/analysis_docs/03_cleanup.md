# 03 - Cleanup

Created: 2023/01/12 10:55:21
Last modified: 2023/01/12 11:02:14

- **Aim:** This document outlines how to back up the analyses on the dedicated space on production and cleanup
- **Prerequisite software:** [rsync](https://rsync.samba.org/)
- **OS:**

## Table of contents

- [03 - Cleanup](#03---cleanup)
  - [Table of contents](#table-of-contents)
  - [Backup analyses and cleanup](#backup-analyses-and-cleanup)
  - [Output files](#output-files)

## Backup analyses and cleanup

Minimal analyses have already been backed up at `/NGS/clinicalgenomics/archive/2022/results/adipose_ont_methylation/`

Also backup the README before cleaning up

```bash
rsync -av /NGS/humangenomics/active/2022/run/adipose_ont_methylation/README.md /NGS/clinicalgenomics/archive/2022/results/adipose_ont_methylation/
```

Cleanup analyses

```bash
rm -rf /NGS/humangenomics/active/2022/run/adipose_ont_methylation/
```

## Output files

Have a look at the final output files

```bash
tree -hv /NGS/clinicalgenomics/archive/2022/results/adipose_ont_methylation/
```

<details><summary markdown="span">My output (click to expand)</summary>

```bash

```

</details>
<br/>

Check it's size

```bash
du -sh /NGS/clinicalgenomics/archive/2022/results/adipose_ont_methylation/
```

<details><summary markdown="span">My output (click to expand)</summary>

```bash

```

</details>
<br/>
