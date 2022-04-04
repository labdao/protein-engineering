### CAR target identification and candidate generation
1. identify datasets including gene expression information of cells in a senescent state. 
2. compile standardized RNA-Seq information from these data using open tools, e.g. [refine.bio](http://refine.bio).
3. perform differential gene expression analysis between senescent cells and the overall distribution of gene expression seen in healthy human tissue.
4. identify differentially expressed genes that are expressed on the cell surface.
5. identify binders (e.g. antibodies) for antigens based on existing data
6. introduce diversity to avoid patent infringement
7. in-silico clone CAR construct plasmids for viral delivery

### fastCAR Pooled Screening of constructs
1. clone a library of CAR constructs into an openMIT licensed backbone
2. transfect a library of CAR constructs with viral donor plasmid into HEK293T cell pool
3. collect virus and ensure titration with MOI enabling high probability of single-construct effected cells
4. infect prepared T-cells and expose to senecent cell pool and non-senecent cell pool
5. co-culture cells for t hours
6. collect T-cells from both flasks and perform FACS multiplex sorting of activity markers, incl. CD69
7. collect activated T-cells and perform amplicon sequncing of CAR construct flanking barcodes
8. use methods related to MAGEKVispr to identify CAR constructs with different abundance levels

The top hits are likely constructs that induce an activated state when T-cells are engaging with senescent cells.

### next steps post-project
- validation in-vitro
- validation in-vivo
    - persistence
- protection of generated IP and open source licensing of tools that generated the IP.
