# callpeaks
Bash script to call peaks from MACS2 peak caller

```
---------------------------------------------------------------------------------------------------------------------------------------------------
usage: callpeaks [options] <chip.bam>

callpeaks - wrapper around macs2 callpeak. Also generates bigWigs from bedGraphs by subtracting input signal.

positional arguments:
  <chip.bam>   ChIP bam file. Required.

optional arguments:
  -d           Output directory to store results. Optional. Default ./macs_op
  -o           Basename for output file. Usually sample name. Default parses from <chip.bam>
  -f           Format of Input file, AUTO, BED or ELAND or ELANDMULTI or ELANDEXPORT or SAM or BAM or BOWTIE or BAMPE or BEDPE
  -g           Effective genome size. Default hs. (can be mm, ce, dm)
  -q           Minimum FDR (q-value) cutoff for peak detection. Deafult 0.05
  -i           Input bam file. e.g, IgG or whole cell extract
  -b           Call broad peaks. Default false
               Broad histone marks:  H3F3A H3K27me3 H3K4me1 H3K79me2 H3K79me3 H3K9me1 H3K9me2 H4K20me1
               Narrow histone marks: H2AFZ H3ac H3K27ac H3K4me2 H3K4me3 H3K9ac
               See here: https://www.encodeproject.org/chip-seq/histone/

Example: callpeaks -i HeLa_IgG.bam HeLa_H3K27Ac.bam
---------------------------------------------------------------------------------------------------------------------------------------------------
```
