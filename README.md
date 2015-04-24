# targeted_TAP
Using make file for targeted_TAP
#Readme file
# April 23, 2015 Yi-Ming Sun
# sample usage. Note
source /projects/btl/ymingsun/multibf_tTAP/centos5/tap_profile.sh; \
time /projects/btl/ymingsun/multibf_tTAP/centos5/targeted_tap k='32 52 72' \
readlen=74 \
reads1=/projects/btl/ymingsun/test_library/A10000_1.fq.gz \ reads2=/projects/btl/ymingsun/test_library/A10000_2.fq.gz \
outdir=./multi_bf_tTap \
sample=A10000 \
filter_list=/home/ymingsun/work/seqExtract/multibf/trans_geno/jan30/bf_files/listfiter.txt
Targeted tap pipeline
Written in GNU Makefile
Command options:
k - kmer size for Transabyss-assembly , can be a list. eg. k='32 52 72'
readlen - cut off length of Transabyss-merge
sample - string indicate library names, use as output suffix
outdir - output directory
reads1 - single .fastq, .gz, .bz2, .bam [sorted by read name] file
reads2 - single .fastq, .gz, .bz2 file. If use bam file, specify 'reads1' will run successfully. Do not need to specify 'reads2'
reads1_list - .txt file contains absolute path of reads1 files
reads2_list - .txt file contains absolute path of reads2 files
ss - specify strand specific libraries
filter - sinlgle bloom filter
filter_list - .txt file contains absolute path of all filters
System configuration:
Source tap_profile
