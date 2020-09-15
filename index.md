Sequencing the SARS-CoV-2 virus
===

# Introduction

TODO

## Resources

CanCOGen: https://github.com/jaleezyy/covid-19-signal
Read cleaning for Nanopore: https://github.com/nodrogluap/nanostripper
Discussion of human read removal: https://github.com/jaleezyy/covid-19-signal/issues/21
Jared Simpson ncov-tools: https://github.com/jts/ncov-tools
COG: https://github.com/connor-lab/ncov2019-artic-nf
viralrecon: https://nf-co.re/viralrecon
viral-ngs: https://github.com/broadinstitute/viral-ngs

1. SARS-CoV-2 sequencing technologies
    1. The Challenge of viral sequencing: Host removal, RNA preservation, RNA diversity
    2. Metagenomic, Bead capture and amplicon sequencing
    3. Illumina and Nanopore sequencing
2. Primal Scheme and the ARTIC amplicon protocol

3. Bioinformatics Software installation
    1. Conda
    2. Docker
    3. Singularity

4. Scientific workflows
    1. Snakemake (covid-19-signal)
    2. Nextflow (ncov2019-artic-nf / viralrecon)
    3. Galaxy (https://usegalaxy.eu/u/wolfgang-maier/w/covid19-variation-analysis-on-artic-pe-data)

5. Steps in typical analysis
    1. Sequencing QC:
        1. FastQC
        2. ?? Nanopore QC?
    2. Human host removal
        1. Competitive Mapping
        2. ?? Other approaches (consult viral
    3. Adapter & Quality trimming (Trimmomatic, trim-galore, fastp)
    4. Map reads (bwa or minimap2)
        1. BamQC
        2. Depth of coverage
    5. Remove amplicon primers (ivar trim)
    6. Call variants
        2. ivar var
        3. lofreq
        4. ???
    7. Filter variants: allele frequency & minimum coverage, indels
        1. can be done by ivar var
        2. lofreq filter
        3. ??? SnpSift
    8. Consensus genome: % coverage and amplicon dropouts, %Ns, % ambiguous base 
        1. ivar consensus
        2. bcftools consensus
    9. Taxonomic QC: % of SARS-CoV-2 reads
        1. Kraken
        2. ?? Others
    10.  After the genome
        1. Metadata format
        2. Clade calling: pangolin and nextclade
        3. Phylogeny / ncov-tools

