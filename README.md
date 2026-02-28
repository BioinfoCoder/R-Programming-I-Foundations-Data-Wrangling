# R Programming I – Foundations & Data Wrangling

**Lecture:** `R_Programming_I_Foundations_Data_Wrangling.Rmd`
**Purpose:** Beginner-friendly guide to R Markdown, data wrangling, and bioinformatics-ready data structures.

---

## Conceptual Mind Map

```
R Programming I
│
├── 1) Foundations
│   ├── What is R?
│   ├── R vs RStudio
│   ├── Script vs Console
│   ├── Basic Syntax
│   │   ├── Comments (#)
│   │   ├── Arithmetic (+ - * / ^)
│   │   └── Assignment (<-)
│   ├── Data Types
│   │   ├── Numeric
│   │   ├── Character
│   │   └── Logical
│   └── Functions
│       └── function_name(arguments)
│
├── 2) Core Data Structures
│   ├── Vector (c())
│   │   ├── Single data type only
│   │   └── Indexing starts at 1
│   ├── Matrix (matrix())
│   │   ├── 2D structure
│   │   ├── Single data type only
│   │   ├── Rows = Genes
│   │   └── Columns = Samples
│   └── Data Frame (data.frame())
│       ├── Tabular structure
│       ├── Multiple data types allowed
│       ├── Access columns with $
│       └── Most used in bioinformatics
│
├── 3) Biological Data Logic
│   ├── RNA-seq Count Matrix
│   │   ├── Rows = Genes
│   │   ├── Columns = Samples
│   │   └── Values = Read counts
│   └── Structured data enables analysis
│
├── 4) tidyverse Philosophy
│   ├── Install once → install.packages("tidyverse")
│   ├── Load each session → library(tidyverse)
│   └── Pipe Operator (%>%) → "Then do this"
│
├── 5) dplyr – Data Wrangling
│   ├── select()    → choose columns
│   ├── filter()    → choose rows
│   ├── mutate()    → create new column
│   ├── arrange()   → sort rows
│   ├── summarise() → aggregate values
│   └── group_by()  → analyze by category
│
└── 6) tidyr – Data Reshaping
    ├── Wide Format → One column per sample
    ├── Long Format → One measurement per row
    ├── pivot_longer() → Wide → Long
    └── pivot_wider()  → Long → Wide
```

---

## Core Concepts to Understand

1. **Everything in R is an object** – Any data can be stored and analyzed.
2. **Data structure determines analysis** – Proper structure = accurate and feasible analysis.
3. **Vectors are the foundation** – Matrices and data frames are built from vectors.
4. **Data frames are central in bioinformatics** – RNA-seq, metadata, and clinical data usually use data frames.
5. **tidyverse promotes readable workflows** – Pipelines simplify analysis instead of nested code:

```r
data %>%
  filter(...) %>%
  group_by(...) %>%
  summarise(...)
```

6. **Long format is essential** – Most visualizations (ggplot2) and statistical models require tidy (long) data.

---

## Quick Command Reference

### Create Objects & Data

```r
x <- 10                        # Assign a value
c(1, 2, 3)                     # Vector
matrix(c(1,2,3,4), nrow=2)     # Matrix
data.frame(col1=c(1,2,3), col2=c("A","B","C")) # Data frame
```

### Load tidyverse

```r
library(tidyverse)
```

### dplyr Core Verbs

```r
select()     # Choose columns
filter()     # Choose rows
mutate()     # Create new column
arrange()    # Sort rows
group_by()   # Analyze by category
summarise()  # Aggregate values
```

### Reshaping Data

```r
pivot_longer() # Wide → Long
pivot_wider()  # Long → Wide
```

---

## Learning Flow

1. Understand **syntax** and **comments**.
2. Understand **objects** and **data types**.
3. Build **biological tables** (vectors → matrices → data frames).
4. Manipulate data using **dplyr**.
5. Reshape data with **tidyr**.
6. Interpret results biologically.

---

## After This Module, You Are Ready For

* Differential expression analysis
* Data visualization (**ggplot2**)
* Statistical modeling
* Advanced bioinformatics workflows

---

## Recommendation

Keep this READM
