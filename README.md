# taxviz

Taxonomy visualizer, intended to allow quick cross-sample and cross-location
comparisons.

Hosted at https://data.securebio.org/taxviz/

You can upload a TSV file with the following columns:

    1. taxid: the NCBI taxid for the clade
    2. parent_taxid: the NCBI taxid for the clade's parent clade
    3. name: the name of the clade
    4+. <sample>: YYYY-MM-DD-Location.  For example, 2023-12-03-HTP

You can see an exaple at https://data.securebio.org/taxviz/datasets/uci/counts.tsv

You can set a default dataset by putting it in the same directory with the name
`counts.tsv` and it will automatically load on startup.

To deploy with multiple datasets, put each one in `datasets/<dataset>/counts.tsv`
and then `ln -s index.html datasets/<dataset>/index.html`.  This is how
https://data.securebio.org/taxviz/datasets/uci/ is implemented.

