# GWAS Study: Analysis of Lymphoblastoid Cell Lines (LCL) mRNA Levels

## Introduction

Lymphoblastoid cell lines (LCLs) are established through the transformation of peripheral B lymphocytes by the Epstein-Barr virus (EBV) (Sie et al., 2009). LCLs are often used as surrogates for peripheral blood lymphocytes (Osorio et al., 2019) by researchers.

In this project, I performed GWAS analysis on the lymphoblastoid cell lines (LCL) mRNA levels quantified through RNA sequencing from 4 European populations. With gender and population as two covariates, I also analyzed genotype and phenotype data by employing two different strategies: excluding both covariates and including both covariates with 50,000 of the SNP genotypes for 344 samples from the CEU (Utah residents with European ancestry), FIN (Finns), GBR (British) and, TSI (Toscani) population.

**Here is the link to the data source: Genetic European Variation in Health and Disease (gEUVADIS) (http://www.internationalgenome.org/data-portal/data-collection/geuvadis/)**

I was interested in studying if **population and gender** could cause the expression of lymphoblastoid cell lines (LCL) mRNA levels to differ. Hereby, I raised my research question: Would population and gender as covariates influence the GWAS analysis result?

## Methods

1. No covariates

I built a linear model with genotype data as the independent variable and phenotype data as the dependent variable with no covariates. Then, I made manhattan plots and QQ plots and observed that 3 out of 5 phenotypes indicate potential causal polymorphism sites. Their QQ plots are ideal- most of the p-values observed follow a uniform distribution (i.e., they are not in linkage disequilibrium with a causal polymorphism, so the null hypothesis is correct!), but the few that were in linkage disequilibrium with a causal polymorphism produce significant p-values (extremely low = extremely high -log(p-values)) in the tail. However, the remaining two phenotypes do not have ideal manhattan plots and QQ plots. So I created linear models with two covariates **Population and Gender** included.

2. With covariates

After including **Population and Gender** as covariates, I discovered no significant change to the linear model without covariates. The identical three phenotypes mentioned above still indicate causal polymorphisms.

## Discussion

There is some possible further research that we can carry out in the future. For example, we can refer to the UCSC genome browser for nucleotide/codon letters and then hypothesize the mRNA levels. This will require a lot of biochemistry background.

## Conclusion

I found no significant change before or after including covariates. In my data analysis, **Population and Gender** as covariates do not seem to significantly impact the GWAS analysis result.

## References

Sie, L., Loong, S., & Tan, E. K. (2009). Utility of lymphoblastoid cell lines. *Journal of neuroscience research*, *87*(9), 1953-1959.

Osorio, D., Yu, X., Yu, P., Serpedin, E., & Cai, J. J. (2019). Single-cell RNA sequencing of a European and an African lymphoblastoid cell line. *Scientific data*, *6*(1), 1-8.
