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
- `summarize(mean_x = mean(x))` — compute a single summary value per group. Common functions inside: mean(), median(), sum(), n()
- `count(column)` — quick frequency count, equivalent to group_by + summarize(n = n())
- `top_n(5, column)` — pick the top 5 rows by a column value

## My gotchas

- Forgot: pipe operator is `%>%` (or `|>` in R 4.1+)
- Forgot: tidyverse needs `library(tidyverse)` at the top of each script
- Forgot: `summarize` and `summarise` are both valid (US/UK spelling)
EOF