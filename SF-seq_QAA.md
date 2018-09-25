# Bi 624 (Fall 2018) – Problem Set 1
## SF-Seq Quality Assessment Assignment

The objectives of this assignment are to use existing tools for quality assessment and adaptor trimming, compare the quality assessments to those from your own software, and demonstrate your ability to summarize other important information about this RNA-Seq data set.

### Data: 
Each of you will be working with 2 of the demultiplexed file pairs. For all steps below, process the two libraries separately. Library assignments are here: ```/projects/bgmp/Bi624/PS1_file_assignments.tsv```

The demultiplexed .fastq files are here: ```/projects/bgmp/2017_sequencing/demultiplexed/```

### Part 1 – SF-Seq read quality score distributions

1. Using ```FastQC``` on Talapas, produce plots of quality score distributions for forward and reverse reads. Also, produce plots of the per-base N content, and comment on whether or not they are consistent with the quality score plots.

2. Run your quality score plotting script from the index hopping assignment. Describe how the ```FastQC``` quality score distribution plots compare to your own. If different, propose an explanation. Also, does the runtime differ? If so, why?

### Part 2 – Adaptor trimming comparison

3. Look into the adaptor trimming options for ```cutadapt```, ```process_shortreads```, and ```Trimmomatic``` (all on Talapas), and briefly describe the differences. Pick one of these to properly trim adapter sequences. Use default settings. What proportion of reads (both forward and reverse) was trimmed? 
    - *Sanity check*: Use your Unix skills to search for the adapter sequences in your datasets and confirm the expected sequence orientations.
  
4. Plot the trimmed read length distributions for both forward and reverse reads (on the same plot). If necessary, consult Assignment 5 (Block 1) from Bi 623 to refresh your memory.

5. Briefly describe whether the adaptor trimming results are consistent with the insert size distributions for your libraries. The size distribution information is in the Fragment Analyzer trace file on Github.
  
### Part 3 – rRNA reads and strand-specificity
6. Find publicly available mouse rRNA sequences and generate a gsnap database from them. Align the SF-Seq reads to your mouse rRNA database and report the proportion of reads that likely came from rRNAs.

7. Demonstrate convincingly that the SF-Seq data are from “strand-specific” RNA-Seq libraries. There are a number of possible strategies to address this problem, but you need only implement one. Report your evidence in numeric and graphical (e.g. a plot) forms.

**To turn in your work for this assignment**:
Please upload your Talapas batch script/code, FastQC plots, answers to questions, and any additional plots/code to github. You should create a final, single file for submission (pdf, R markdown, or similar) containing all these elements. The three parts of the assignment should be clearly labeled
