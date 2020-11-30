## Introduction

This software is used for identifying allele genes from polyploid genome.



## Dependencies

Software:

&ensp;&ensp;&ensp;&ensp;MCScanX  
&ensp;&ensp;&ensp;&ensp;GMAP  
&ensp;&ensp;&ensp;&ensp;NCBI BLAST+  



## Installation

```bash
cd /path/to/install
git clone https://github.com/sc-zhang/AlleleFinder.git
chmod +x AlleleFinder/bin/AlleleFinder
# Optional
echo 'export PATH=/path/to/install/AlleleFinder/bin:$PATH' >> ~/.bash_profile
source ~/.bash_profile
```



## Usage

```bash
AlleleFinder -m MONO -d MONO_CDS -f MONO_GFF3 -c CDS -n NUM_ALLELE -g GFF3 [-b BLAST_COUNT] [-i BLAST_IDENTITY] [-w WORKDIR] [-t THREADS]
```

**-m, --mono** fasta file of mono genome

**-d, --mono_cds** cds file of mono genome

**-f, --mono_gff3** gff3 file of mono genome

**-c, --cds** cds file of polyploid genome

**-g, --gff3** gff3 file of polyploid  genome

**-n, --num_allele** number of allele

**-b, --blast_count** iteration count for running blast, default: 2

**-i, --blast_identity** threshold of blast identity, default: 80

**-w, --workdir** work directory, default: wrkdir

**-t, --threads** threads, default: 12



## Results

**allele.formated.txt** is the file contain all allele genes

**allele.formated.stat** is the statistics information of allele
