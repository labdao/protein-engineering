# fastCAR 🏎️ 
Let's build open source tools to generate CAR constructs.

## Problem
Therapeutic antibodies, ADCs, BITEs, DARPINs, and CAR-based therapeutics are promising platform technologies to remove antigen expressing cells within a multicellular organism. They are all united in their reliance on sufficient on-target protein-protein interactions. Applications for these therapeutics can range from oncology to chronic diseases (senolytics). 

## Solution
Develop a toolset of open-source computational tools and data that can be used to generate candidate constructs, such as CAR plasmids for in-vitro testing. These tools will be hosted as executable APIs using the openlab protocol.
We will start by developing a set of [senolytic CAR-T](https://www.nature.com/articles/s41586-020-2403-9) constructs. 

## Technology
The tools we plan to develop cover a series of steps: 

1. identify target cell state from multiple public sources
    1. senescence: decide criteria (upregulated in specific senescent settings or more universal?)
        1. Compile available datasets of different triggers of senescence  → a list of PMID - Corina
            1. papers
            2. tabula muris senis - actually not that great
        2. [refine.bio](http://refine.bio) → a table with n PMID rows x k genes - Niklas
            1. input: paper reference
            2. output: RNA-Seq count
        3. Filter out potential toxic candidates: human protein atlas and human proteome map
            1. [refine.bio](http://refine.bio) - compare expression of genes from paper with healthy human tissue
        4. test: 
            1. uPAR
            2. SAbGAL
            3. CDNK2A
            4. 
            - [[A2M]] macroglobulin goes up
            - [[CDKN1A]] up
            - [[CCND2]] up
            - [[LCAT]] up
            - [[MMP3]] up
2. identify expressed surface antigens in target cell state.
    1. uPAR
        1. surfaceome filter - job#1
            1. genecards: criterium > 5
            
            ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4469558f-b9a3-4b08-80c5-b4f939f2f004/Untitled.png)
            
            1. other tools? 
        2. expression intensity
            1. fold change relative to all transcripts in refine.bio
        3. expression robustness
            1. moderated t-test DGE vs. background expression cohort
3. identify binders for antigens based on existing data → CDR1, CDR2, CD3 sequence
    1. patents - job#2
        1. ABCD ExPasy - [https://academic.oup.com/nar/article/48/D1/D261/5549708](https://academic.oup.com/nar/article/48/D1/D261/5549708)
            1. 
        2. NLP for patent search - gene name & amino acid sequence
        3. [https://www.lens.org/](https://www.lens.org/)
            1. search for sequence of target protein
                1. [https://about.lens.org/patseq-bulk-download-tou/](https://about.lens.org/patseq-bulk-download-tou/)
                2. [https://www.lens.org/lens/bio/patseqfinder](https://www.lens.org/lens/bio/patseqfinder)
            2. search for gene name
    2. commercial vendors
        1. abgene
4. avoid patent coverage (important)
    1. alphafold based estimation of 3D conformation - naturalantibodies.com
5. induce variation into the binders (nice to have)
    1. stability & multimerization
    2. titrate binding affinity
        1. titrate binding affinity with alphafold + KDdock
6. clone constructs → CAR construct lentivirus? retrovirus?
    1. scFv - binder
        1. heavy chain CDR1, CDR2, CDR3
        2. Glycin- linker length
            1. length
        3. light chain CDR1, CDR2, CDR3
    2. activation domain
        1. 41BB 
        
7. cloning - hand off to wet-lab (London Biofoundry - golden gate as a service?)
    1. order gBLOCK from IDT 
    2. golden gate assembly with primers/short gBLOCKS?
8. fastCAR pooled testing - real project on its own - method in Amor lab? 

transfect with

- check CAR backbone with MIT or openMTA license? - Corina
    - addgene
    

## pooled → potentially also in array format with multiple T-cells and cell lines

Kole Roybal? 

multiplex sort incl CD69

target cells 

no target cells

MAGEKVISPR - differential abundance of CAR constructs

next steps 

- validation in-vitro
- validation in-vivo
    - persistence

1. test binder affinity
2. generate constructs for production: creation of basic “universal” CAR constructs.
3. produce high titer virus for T-cell transduction:
    1. measure cytokine expression
    2. measure in vitro cytotoxicity

CAR Pools - UCSF

FACS sorting of activity markers and then amplicon sequncing

permute antibody sequences

generate antibody from scratch

## Team (alphabetical)
* [Corina Amor Vegas](https://twitter.com/corina_amor_MD)
* [Leo Chicaybam](https://twitter.com/leochicaybam)
* [Niklas Rindtorff](https://twitter.com/Niklas_TR)

### support needed
* structural biologist
* scientific software engineer
* computational biologist

## Financials - raising open-source funding on gitcoin
* stipends for full-time supporters are planned
* fractional ownership of resulting IP-NFT

## Reading
* [notion](https://www.notion.so/67a570bc9a97434f8126d06522709f9d) 
* [DARPIN based cell therapy](https://pubmed.ncbi.nlm.nih.gov/31548346/)
