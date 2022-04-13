# Protein Binder Engineering
Let's build open tools to generate protein binders at scale.

## Problem
Therapeutic [antibodies](https://en.wikipedia.org/wiki/Monoclonal_antibody), [ADCs](https://www.nature.com/articles/s41571-021-00470-8), [BITEs](https://en.wikipedia.org/wiki/Bi-specific_T-cell_engager), [DARPins](https://en.wikipedia.org/wiki/DARPin), and [CAR](https://en.wikipedia.org/wiki/Chimeric_antigen_receptor_T_cell)-based therapeutics are platform technologies that are giving rise to an increasing number of modern (and very expensive) medicines. These platforms are all united by the fact that an engineered protein needs to bind tightly to a target protein associated with a disease. This type of protein engineering is a minimization task: The input is the 3D structure (a .pdb file) of a target protein and the goal is to find the sequence of amino acids that code for a protein, referred to as a binder, that binds tightly to the target.

Despite the great overall potential of protein binders, the tools used to design these therapeutics are expensive and inaccessible. For example, most [display](https://en.wikipedia.org/wiki/Yeast_display#:~:text=Yeast%20display%20(or%20yeast%20surface,for%20isolating%20and%20engineering%20antibodies.) methods take multiple weeks to generate promising antibody candidates and tools for computational protein design are pubblished by academic scientists without a further incentive to make the tool run at production-grade scale. 

A particularly interesting use-case for protein binders as therapeutics against aging related diseases, is the clearance of senescent cells from the human body by senolytic cell therapies. Previous work by [Amor et al.](https://www.nature.com/articles/s41586-020-2403-9), demonstrated that senescent cells can be effectively cleared from the body using CAR-T cells targeting the surface protein encoded by the [PLAUR](https://www.genecards.org/cgi-bin/carddisp.pl?gene=PLAUR) gene. While most CAR-T cells are based on scFv binders, prior studies have demonstrated that computationally more tractable [DARPin](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4678647) binders can also be used for cell therapies.

## Solution
We aim to develop a series of computational tools enabling the easy generation of candidate protein binders, ready for in-vitro affinity testing and refinement. These tools will be hosted as executable APIs ontop the openlab exchange.

In detail, the tools we will develop comprise a 

Generation of proposed constructs 
Planning of construct generation 
target binding affinity estimation

## Application 
removing senescent cells from human tissue. A target robustly expressed on the cell surface of 


## Protein Representation learning infrastructure 


Huggingface API
FastAPI / https://cceyda.github.io/blog/huggingface/torchserve/streamlit/ner/2020/10/09/huggingface_streamlit_serve.html

## Technology
protein representation learning 
* ESM-1B
* Prot-Trans
* Rostlab
    * https://huggingface.co/Rostlab/prot_t5_xl_bfd

https://huggingface.co/models?other=protein%20language%20model

## folding into desired shapes
graph neural networks
https://www.sciencedirect.com/science/article/pii/S2405471220303276
https://gitlab.com/ostrokach/proteinsolver

[DLAB](https://github.com/oxpig/dlab-public)
[DMSopt](https://github.com/dahjan/DMS_opt)

### Target identification and candidate generation workflow

## Team (alphabetical)
* [Corina Amor Vegas](https://twitter.com/corina_amor_MD)
* [Finsam Samson](https://twitter.com/FinsamSamson)
* [Leo Chicaybam](https://twitter.com/leochicaybam)
* [Mahdi Chaker](https://twitter.com/MahdiMC)
* [Niklas Rindtorff](https://twitter.com/Niklas_TR)
* [Stanley Bishop](https://twitter.com/ScienceStanley)

### support needed
* structural biologist
* scientific software engineer
* computational biologist

## Financials
100k USDC from VitaDAO 
* stipends for full-time supporters are planned
* fractional ownership of resulting IP-NFT

## Literature
### Protein binder design
* [Design of protein binding proteins from target structure alone (Mar 2022)](https://doi.org/10.1038/s41586-022-04654-9)
* [De novo design of picomolar SARS-CoV-2 miniprotein inhibitors (Oct 2020)](https://doi.org/10.1126/science.abd9909)
* 

### Binder refinement
### unsorted Reading
* [notion](https://www.notion.so/67a570bc9a97434f8126d06522709f9d) 
* [DARPIN based cell therapy](https://pubmed.ncbi.nlm.nih.gov/31548346/)


Literature: Protein Binders



### Additional protein design 
* [A defined structural unit enables de novo design of small-molecule–binding proteins (Sep 2020)](https://doi.org/10.1126/science.abb8330)
* [De novo design of potent and selective mimics of IL-2 and IL-15 (Jan 2019)](https://doi.org/10.1038/s41586-018-0830-7)
* [De novo design of a fluorescence-activating β-barrel (Sep 2018)](https://doi.org/10.1038/s41586-018-0509-0)

Computational design of ligand-binding proteins with high affinity and selectivity (Sep 2013)
https://doi.org/10.1038/nature12443


Literature: Non-binder ML/Design of Proteins
Protein sequence design with a learned potential (Feb 2022)
https://doi.org/10.1038/s41467-022-28313-9

Efficient evolution of human antibodies from general protein language models and
sequence information alone (Apr 2022) (doi doesnt work)
https://www.biorxiv.org/content/10.1101/2022.04.10.487811v122.04.10.487811-1

Software
RosettaDock 4.0 Protocol
https://r2.graylab.jhu.edu/apps/submit/docking-4
https://doi.org/10.1016/j.bpj.2017.11.1919

RIFdock
https://github.com/rifdock/rifdock
https://doi.org/10.1038/s41586-018-0509-0




https://twitter.com/Romeritos/status/1512007307655266312
