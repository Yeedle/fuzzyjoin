# fuzzyjoin 0.1.2.9000

* Added `interval_join`, which joins tables on cases where (start, end) intervals overlap between the two columns. This adds IRanges from Bioconductor to SUGGESTS.
* Added `genome_join`, which is a more specific case of `interval_join` that joins tables on based on (chromosome, start, end), where the chromosome must agree and (start, end) must overlap.
* Added `index_match_fun` argument to `fuzzy_join`, which handles functions (such as `interval_join` and `genome_join`) that operate on the original columns rather than all pairs of columns.

# fuzzyjoin 0.1.2

* Fixed bug that failed when single column data frames (not tbl_dfs) were given (#13)
* Updated README for newest versions of dplyr and janeaustenr

# fuzzyjoin 0.1.1

## Features

* Added option not only to join based on a maximum distance but also to append a distance column, using the `distance_col` argument. This is available in `difference_join`, `distance_join`, `stringdist_join`, and `geo_join` (#10)

## Bug fixes

* Fixed to ignore groups while preserving the groups of x in the output (#11)
* Fixed to append `.x` and `.y` to all common columns, not just those in `by` (#12)

## Package management

* Added codecov to measure test coverage
* Added AppVeyor continuous integration
* Added Code of Conduct

# fuzzyjoin 0.1

* Initial draft of package for CRAN
