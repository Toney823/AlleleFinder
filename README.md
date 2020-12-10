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
AlleleFinder [-h] -r REF -d REF_CDS -f REF_GFF3 -c CDS -g GFF3 -n NUM_ALLELE [-b BLAST_COUNT] [-i BLAST_IDENTITY] [-e TE] [-j TE_OVERLAP] [-w WORKDIR] [-t THREADS] [-m|--is_mono]
```

**Notice** there must no '-' in gene id

**-r, --ref** fasta file of ref genome

**-d, --ref_cds** cds file of ref genome

**-f, --ref_gff3** gff3 file of ref genome

**-c, --cds** cds file of polyploid genome

**-g, --gff3** gff3 file of polyploid  genome

**-n, --num_allele** number of allele

**-m, --is_mono** if ref genome is mono assembly of polyploid genome, add this parameter

**-b, --blast_count** iteration count for running blast, default: 2

**-i, --blast_identity** threshold of blast identity, default: 80

**-e, --TE** TE file for filtering, default: NULL

**-j, --TE_overlap** threshold of TE overlap, default: 0.3, only effect when TE is not NULL

**-w, --workdir** work directory, default: wrkdir

**-t, --threads** threads, default: 12



## Results

1. **Without TE filter**

**allele.adjusted.txt** is the file contain all allele genes

**allele.adjusted.*.stat** are the statistics information of allele

2. **With TE filter**

**allele.adjusted.nonTEs.txt** is the file contain all allele genes

**allele.adjusted.nonTEs.*.stat** are the statistics information of allele
