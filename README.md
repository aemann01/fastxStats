# fastxStats
Collection of simple scripts for generating summary statistics from fastq and fasta files.

seq_len_hist_trim.py:
Generates summary statistics from either a fastq or fasta file and generates length histogram. Optional: trim fastq or fasta file based on median size.

Useage: python seq_len_hist_trim.py input.fastx 

length_hist_with_insert_size.py:
Generates fragment length histogram from assembled fastq file (eg PEAR merged reads) and a two column, tab separated frequency table where the first column is a list sequence sizes and the second is a list of counts per size (eg insert size metrics output from picard tools). Useful if you want to calculate true distribution of paired fragment lengths and have sequences that are too long/short to assemble with PEAR or some other read merging software.

Useage: python length_hist_with_insert_size.py in.fastq freq_table.txt

outlier_stats.py:
Pulls sequences in a fasta file shorter than specified limit (example, shorter than 10 nt).

Useage: python outlier_stats.py in.fasta 10

fasta_trim_length.py & fastq_trim_length.py:
Stand alone functions for reading in fastx file, generating summary statistics, sequence length histogram, option to trim based on median size.

Useage: python fastx_trim_length.py input.fasta

