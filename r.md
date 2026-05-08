cat > r.md << 'EOF'
# R Commands I Use

cd /e/bioinformatics-cheatsheet
cat > r.md << 'EOF'
# R Commands I Use

## Tidyverse — Chapter 1: Data wrangling

- `filter(df, column > value)` — keep only rows that match a condition
- `select(df, col1, col2)` — keep only specific columns
- `mutate(df, new_col = old_col * 2)` — create or transform a column
- `arrange(desc(column))` — sort rows by a column, biggest first

## Tidyverse — Chapter 2: Data visualization with ggplot2

- `ggplot(df, aes(x = col1, y = col2)) + geom_point()` — scatter plot
- `aes(color = column)` — color points by a categorical variable
- `+ scale_x_log10()` — change x-axis to log scale
- `+ facet_wrap(~ column)` — split plot into panels by a variable

## Tidyverse — Chapter 3: Group and summarize

- `group_by(column)` — split a dataframe into groups based on a column value
- `summarize(mean_x = mean(x))` — compute a single summary value per group
- `count(column)` — quick frequency count
- `top_n(5, column)` — pick the top 5 rows by a column value

## Tidyverse — Chapter 4: Types of visualizations

- `geom_line()` — line plot, good for trends over time
- `geom_col()` — bar chart from pre-summarized values
- `geom_histogram(binwidth = 5)` — distribution of a single variable
- `geom_boxplot()` — distribution per group, shows median plus outliers
- `theme_bw()` — clean black-and-white theme for publication

## Bioconductor — Chapter 1

- `BiocManager::install("package")` — install a Bioconductor package
- `Biostrings::readDNAStringSet("file.fasta")` — read DNA sequences
- `GRanges()` — store genomic intervals (chromosome, start, end, strand)
- `width(seq)` — length of each sequence in a Biostrings object

## Bioconductor — Chapter 2: Biostrings (Zika virus)

- `readDNAStringSet("file.fasta")` — read DNA sequences from a FASTA file
- `length(seq)` — number of sequences in the set
- `width(seq)` — length of each sequence (number of bases)
- `alphabetFrequency(seq, baseOnly = TRUE)` — count A, C, G, T frequencies
- `letterFrequency(seq, "GC")` — count specific letters (e.g., GC content)
- `reverseComplement(seq)` — get the reverse complement strand
- `subseq(seq, start = 1, end = 100)` — extract a sub-sequence by position
- `translate(seq)` — translate a DNA sequence to amino acids

## My gotchas

- Forgot: pipe operator is `%>%` (or `|>` in R 4.1+)
- Forgot: tidyverse needs `library(tidyverse)` at the top of each script
- Forgot: `summarize` and `summarise` are both valid (US/UK spelling)
EOF