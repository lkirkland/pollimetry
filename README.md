Pollimetry: Predictive allometry for pollinating insects
==========

Tools to estimate pollinator body size as well as bee tongue length and foraging distances.

To install
==========
```
if (!requireNamespace("devtools")) {
  install.packages("devtools")
}
devtools::install_github("liamkendall/pollimetry")
library(pollimetry)
```

Estimating body size
====================

The `bodysize` function uses Bayesian generalised linear mixed models (GLMMs) to provide posterior estimates (along with S.E. and 95% confidence intervals) of pollinator body size (i.e. dry weight (mg)) using the intertegular distance (ITD), species taxonomy or phylogeny (bees only `type="phylo"`), sex and biogeography (at present only Australia, Europe, North America and South America). Estimates (and variance components) are returned as four additional columns bound to the original dataframe. These models will be periodically updated using novel data as and when it becomes available. See `bodysize` details for more information.

Pre-existing equations for Diptera, Hymenoptera and Lepidopteran taxa using body length (`lengthsize`), body length * width (`lengthwidthsize`) and head width (`headwidthsize`) are also provided.

Allometric traits
=================

Users can predict bee tongue length (`tonguelength`) from Cariveau et al. (2015) and bee foraging distances (`foragedist`) from equations described in van Nieuwstadt and Iraheta (1996) for Meliponini, Greenleaf et al. (2007) and Guedot et al. (2009) for Osmia spp.

Future traits of interest
=========================

Many other ecological traits crucial to pollination are likely to be allometric. Therefore, we hope to examine these unexplored body size - trait relationships with the aim of including new predictive models in the future. 