# DE NOVO GENOME ASSEMBLY USING LONG READS
&nbsp;

## Basecalling
Base calling is the process of translating the electronic raw signal (fast5 format) of the sequencer into bases (fastq format).
- **environment**: the i-Trop computing cluster.
- **software**: guppy
- **input data**:
- **[link to the tutorial](https://timkahlke.github.io/LongRead_tutorials/BS_G.html)**
&nbsp;

## Quality assessment
Verify the quality of reads within nanopore fastq files.
- **environment**: the i-Trop computing cluster.
- **software**: fastqc
- **input data**: output of Basecalling (previous step)
- **[link to the tutorial](https://timkahlke.github.io/LongRead_tutorials/QC_F.html)**
&nbsp;

## Read filtering, trimming and adapter removal
Verify the quality of reads within nanopore fastq files.
- **environment**: the i-Trop computing cluster.
- **software**: porechop; nanofilt
- **input data**: output of Basecalling passing quality control
- **[link to the tutorial](https://timkahlke.github.io/LongRead_tutorials/FTR.html)**
&nbsp;

## Genome assembly
"De novo" assembly of long reads
- **environment**: the i-Trop computing cluster.
- **software**: flye
- **input data**: Klebsiella pneumoniae nanopore sequences [link to input files](https://www.ebi.ac.uk/ena/browser/view/PRJEB45084)
- **[link to the tutorial](https://timkahlke.github.io/LongRead_tutorials/ASS_F.html)**
&nbsp;

