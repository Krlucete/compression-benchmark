## Data Repository

All reference files should be pre-processed with `ref.py`, as explained in the [Manual](README).

### SAM Samples

| Organism | Technology | Coverage | Uncompressed<br>size | Link | Reference |
|----------|------------|----------|----------------------|------|-----------|
| *E.coli* | Illumina MiSeq | 420x | 5.2 GB | [MiSeq_Ecoli_DH10B_110721_PF](ftp://webdata:webdata@ussd-ftp.illumina.com/Data/SequencingRuns/DH10B/MiSeq_Ecoli_DH10B_110721_PF.bam)<sup> 1</sup> (1.3 GB) | [CP000948](http://www.ebi.ac.uk/ena/data/view/CP000948&display=fasta) |
| *H.sapiens* | IonTorrent | 0.6x | 5.6 GB | [sample-2-10_sorted](ftp://ftp.sra.ebi.ac.uk/vol1/ERA229/ERA229587/bam/sample-2-10_sorted.bam) (1.4 GB) | [Homo_sapiens_assembly19](http://www.broadinstitute.org/ftp/pub/seq/references/Homo_sapiens_assembly19.fasta) |
| *H.sapiens* | Illumina HiSeq | 2x | 20 GB | [9827_2#49](ftp://ftp.sra.ebi.ac.uk/vol1/ERA242/ERA242167/bam/9827_2%2349.bam) (6.1 GB) | [hs37d5](ftp://ftp.1000genomes.ebi.ac.uk/vol1/ftp/technical/reference/phase2_reference_assembly_sequence/hs37d5.fa.gz) |
| *D.melangoster* | PacBio | 75x | 29 GB | [dm3PacBio](http://bergmanlab.ls.manchester.ac.uk/data/tracks/dm3/dm3PacBio.bam) (12 GB) | [dm3](http://hgdownload.soe.ucsc.edu/goldenPath/dm3/bigZips/chromFa.tar.gz) |
| *H.sapiens* | RNASeq | 6x | 71 GB | [K562_cytosol_LID8465_TopHat_v](http://www.ebi.ac.uk/arrayexpress/files/E-MTAB-1728/K562_cytosol_LID8465_TopHat_v2.bam) (12.8 GB) | [hg19](http://hgdownload.cse.ucsc.edu/goldenpath/hg19/bigZips/chromFa.tar.gz)<sup> 2</sup> |
| *H.sapiens* | PacBio | 15x | 118 GB | [NA12878.pacbio.bwa-sw.20140202](ftp://ftp.1000genomes.ebi.ac.uk/vol1/ftp/technical/working/20131209_na12878_pacbio/si/NA12878.pacbio.bwa-sw.20140202.bam) (53.8 GB) | [hs37d5](ftp://ftp.1000genomes.ebi.ac.uk/vol1/ftp/technical/reference/phase2_reference_assembly_sequence/hs37d5.fa.gz) |
| *H.sapiens* | Illumina-like Cancer Cell | 30x | 398 GB | [HCC1954.mix1.n80t20](https://cghub.ucsc.edu/cghub/metadata/analysisAttributes?analysis_id=360b4736-6c5e-48df-af58-c1cf51609350)<sup> 3</sup> (122.5 GB) | [Homo_sapiens_assembly19](http://www.broadinstitute.org/ftp/pub/seq/references/Homo_sapiens_assembly19.fasta) |
| *H.sapiens* | Illumina HiSeq | 50x | 549 GB | [NA12878_S1](ftp://ftp.sra.ebi.ac.uk/vol1/ERA172/ERA172924/bam/NA12878_S1.bam) (113.3 GB) | [hg19](http://hgdownload.cse.ucsc.edu/goldenpath/hg19/bigZips/chromFa.tar.gz) |

1. All BAM files must be decompressed via `samtools view -h <bam> -o <sam>`.
2. You can concatenate separate chromosome files into a large FASTA file via `cat chr*.fa > hg19.fa`.
3. You need [GeneTorrent](https://cghub.ucsc.edu/software/downloads.html) to download this sample. After you obtain it, you can fetch this particular sample via `gtdownload -vv -c https://cghub.ucsc.edu/software/downloads/cghub_public.key  -d 360b4736-6c5e-48df-af58-c1cf51609350`.

### FASTQ Samples

| Organism | Technology | Paired Coverage | Uncompressed size | Link | Reference |
|-----|------|-------|-------|--------|------|
| *P.aeruginosa* | Illumina GAIIx | 50x | 1 GB | [SRR554369_1](ftp://ftp.ddbj.nig.ac.jp/ddbj_database/dra/fastq/SRA058/SRA058002/SRX181937/SRR554369_1.fastq.bz2)<sup> 1</sup> (119 MB) <br> [SRR554369_2](ftp://ftp.ddbj.nig.ac.jp/ddbj_database/dra/fastq/SRA058/SRA058002/SRX181937/SRR554369_2.fastq.bz2) (120 MB) | [NC_002516.2](http://www.ncbi.nlm.nih.gov/nuccore/110645304?report=fasta) |
| *E.coli* | PacBio | 140x | 1.3 GB | [SRR1284073](ftp://ftp.ddbj.nig.ac.jp/ddbj_database/dra/sralite/ByExp/litesra/SRX/SRX533/SRX533603)<sup> 3</sup> (2.2 GB) | [Arabidopsis](http://datasets.pacb.com.s3.amazonaws.com/2014/Arabidopsis/reads/polished_assembly.fasta) |
| *H.sapiens* gut | Illumina GAII | Unknown | 3.6 GB | [MH0001_081026_clean.1](http://public.genomics.org.cn/BGI/gutmeta/High_quality_reads/MH0001/081026/MH0001_081026_clean.1.fq.gz)<sup> 2</sup> (478 MB) <br> [MH0001_081026_clean.2](http://public.genomics.org.cn/BGI/gutmeta/High_quality_reads/MH0001/081026/MH0001_081026_clean.2.fq.gz) (550 MB) | [hg19](http://hgdownload.cse.ucsc.edu/goldenpath/hg19/bigZips/chromFa.tar.gz) |
| *S.cerevisiae* | Illumina GAII | 175x | 7.7 GB | [SRR327342_1](ftp://ftp.ddbj.nig.ac.jp/ddbj_database/dra/fastq/SRA043/SRA043851/SRX089128/SRR327342_1.fastq.bz2) (792 MB) <br> [SRR327342_2](ftp://ftp.ddbj.nig.ac.jp/ddbj_database/dra/fastq/SRA043/SRA043851/SRX089128/SRR327342_2.fastq.bz2) (947 MB) | [ACFL01000033](http://www.ebi.ac.uk/ena/data/view/ACFL01000033&display=fasta) |
| *T.cacao* | Illumina GAIIx | 35x | 39 GB | [SRR870667_1](ftp://ftp.ddbj.nig.ac.jp/ddbj_database/dra/fastq/SRA082/SRA082615/SRX288435/SRR870667_1.fastq.bz2) (5.2 GB) <br> [SRR870667_2](ftp://ftp.ddbj.nig.ac.jp/ddbj_database/dra/fastq/SRA082/SRA082615/SRX288435/SRR870667_2.fastq.bz2) (4.0 GB) | [Cacao](http://arthropods.eugenes.org/genes2/cacao/genes/genome/cacao11allasm_repmask_nomito.fa.gz) |
| *H.sapiens* | Illumina HiSeq | 13x | 102 GB | [ERR174310_1](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174310/ERR174310_1.fastq.gz) (17.3 GB) <br> [ERR174310_2](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174310/ERR174310_2.fastq.gz) (16.8) |  [hg19](http://hgdownload.cse.ucsc.edu/goldenpath/hg19/bigZips/chromFa.tar.gz) |
| *H.sapiens* | Illumina HiSeq | 120x (single-end) | 887 GB |  [ERR174324](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174324/ERR174324_1.fastq.gz) <sup>(4)</sup> (17.5 GB) <br> [ERR174325](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174325/ERR174325_1.fastq.gz)  (16.7 GB) <br> [ERR174326](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174326/ERR174326_1.fastq.gz)  (16.3 GB) <br> [ERR174327](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174327/ERR174327_1.fastq.gz)  (16.3 GB) <br> [ERR174328](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174328/ERR174328_1.fastq.gz)  (16.3 GB) <br> [ERR174329](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174329/ERR174329_1.fastq.gz)  (16.3 GB) <br> [ERR174330](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174330/ERR174330_1.fastq.gz)  (16.1 GB) <br> [ERR174331](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174331/ERR174331_1.fastq.gz)  (17.3 GB) <br> [ERR174332](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174332/ERR174332_1.fastq.gz)  (15.7 GB) <br> [ERR174333](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174333/ERR174333_1.fastq.gz)  (15.4 GB) <br> [ERR174334](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174334/ERR174334_1.fastq.gz)  (15.6 GB) <br> [ERR174335](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174335/ERR174335_1.fastq.gz)  (15.6 GB) <br> [ERR174336](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174336/ERR174336_1.fastq.gz)  (15.9 GB) <br> [ERR174337](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174337/ERR174337_1.fastq.gz)  (16.0 GB) <br>  [ERR174338](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174338/ERR174338_1.fastq.gz)  (16.0 GB) <br> [ERR174339](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174339/ERR174339_1.fastq.gz)  (15.6 GB) <br> [ERR174340](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174340/ERR174340_1.fastq.gz)  (11.2 GB) <br> [ERR174341](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR174/ERR174341/ERR174341_1.fastq.gz)  (14.8 GB) <br> Total 284.6 GB | [hg19](http://hgdownload.cse.ucsc.edu/goldenpath/hg19/bigZips/chromFa.tar.gz) |

1. All bzip2 files must be decompressed via `bzip2 -d <bz> -c > <fastq>`.
2. All Gzip files must be decompressed via `gzip -d <gz> -c > <fastq>`.
3. You need [NCBI SRA Toolkit](http://www.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?view=software) to download this sample. After you obtain it, you can fetch this particular sample via `fastq-dump SRR1284073`.
4. For this sample, only first library mate (`_1`) files are used.

### Coverage calculation

Coverage was calculated by dividing a total number of nucleotides in SAM or FASTQ file with the rounded 
reference genome size. These numbers are not intended to be exact, but more as a rough estimate of a coverage 
in the given sample.

The following reference genome sizes were used:

| Organism | Size |
|-----|------|
| H.sapiens | 3,100,000,000 |
| T.cacao |	345,000,000 |
| D.melangoster	|	168,000,000 |
| S.cerevisiae |	12,000,000 |
| P.aeruginosa | 6,300,000	|
| E.coli | 4,700,000	|
