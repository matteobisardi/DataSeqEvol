# DataSeqEvol
Data repository for the paper "*Modelling sequence-space exploration and emergence of epistatic signals in experimental protein evolution*".

This repo is companion of the [Julia](http://julialang.org) package [SeqEvol](https://github.com/matteobisardi/SeqEvol), that allows to simulate experimental evolution via Gibbs Markov Chain Monte Carlo sampling in sequence landcapes inferred via [DCA](https://en.wikipedia.org/wiki/Direct_coupling_analysis).

Data
----
Except for parameters, the data is just reformatted, cleaned and [PFAM](https://pfam.xfam.org)-aligned sequences coming from the following two papers:
[Protein Structural Information and Evolutionary Landscape by In Vitro Evolution](https://academic.oup.com/mbe/article/37/4/1179/5610534?login=true) and [Protein Structure from Experimental Evolution](https://www.sciencedirect.com/science/article/pii/S2405471219304284).

Here is a brief description of the data contained in the repo folders:
* `wt`: amino acid and nucleotide sequences of three wildtype sequences, PSE-1, TEM-1 ([PF13354](https://pfam.xfam.org/family/Beta-lactamase2)) and AAC6 ([PF00583](http://pfam.xfam.org/family/pf00583))

* `alignments/natural`: MSAs of homologous sequences from two protein families: PF13354 and PF00583 

* `alignments/experimental`: MSAs of evolved sequences from the final rounds of evolution of the three experiments 
 
* `alignments/silico`: *in silico* generated MSAs (via the SeqEvol package) to copycat the experimental alignments

* `BM_parameters`: [bmDCA](https://arxiv.org/abs/2109.04105) parameters to build the sequence landscapes and simulate evolution

Format
-----
All alignments are in `fasta.gz` (fasta and gzipped) format except for wt sequences. Once unzipped the AAC6 alignements exceed 100 Mb. Parameters are also in `.gz` format for compression.  
