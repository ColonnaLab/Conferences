#Prioritization of causative genomic variants in miscarried embryos from idiopathic pregnancy losses 

S Buonaiuto1+ I Di Biase2+ V Aleotti3 A De Marino4  G Damaggio1 M Chierici5 M Pulijala6 P D’Ambrosio2, G Esposito2, Q Ayub6, C Furlanello5, N Soranzo7, M Rubini3, A Capalbo4, S Di Biase2  V Colonna1 

1IGB-CNR, Napoli, Italy - 2MeriGen Research s.r.l., Naples, Italy - 3University of Ferrara, Ferrara, Italy - 4Igenomix Italy, Marostica, Italy - 5 Fondazione Bruno Kessler, Povo, Italy - 6 Monash University,  Bandar Sunway, Malaysia - 7 Wellcome Sanger Institute, Hinxton, UK - +equal contribution

##Background. 
Miscarriage, the spontaneous termination of a pregnancy before 24 weeks of gestation, occurs in 10-15% of all pregnancies and has both environmental and genetic causes. Miscarriages are often caused by chromosomal aneuploidies of the gametes but they can also have non random genetic causes like small-size mutations both de-novo or inherited. Miscarriages are mostly studied using parental genetic information1 which might be ineffective as only half of the inheritance in the embryo is revealed and de-novo mutations are missed. Extending therefore the analysis to fetal genomes is the necessary next step. 
DNA sequence of miscarried fetuses has already been used to study genetic components of miscarriages both as candidate gene or exomes analysis.2 Most studies have small sample sizes (tens) and adopt a family-based approach often with focus on a reduced range of fetal phenotypes. Two studies adopt istead a cohort-based approach to evaluate the diagnostic potential of sequencing3 and identify genes essential for the embryonic development.4 All studies perform sequencing followed by variant annotation and prioritization, investigating rare variation in euploid embryos. Nevertheless always different criteria areused to select the variants, and in any case the code to fully reproduce the variant prioritization is available, making it difficult to replicate results and perform comparisons.
##Results. 
To understand genetic susceptibility to miscarriage we studied the genome of 46 miscarried embryos from mothers in the range of healthy adult individuals. After screening for chromosomal aneuploidies, 32.6% of samples were euploid and could be sequenced at high coverage to discover 11M single-nucleotide polymorphisms and 2M small insertions or deletions.
We developed GP5 a pipeline to prioritize putatively causative variants in coding regions. GP performs filtering of high-quality genomic variants based on functional predictions.   After that, GP filters for technical artifacts and for random selection of genes in a control cohort through resampling. GP could also use knowledge of genes involved in the trait under study. 
We applied the GP pipeline to data from the high-coverage whole-genome sequences of the embryos using as control 100 resampling of 10 individuals from 929 individuals of the Human Genome Diversity Project. GP prioritized 439 unique variants in 399 genes in the embryonic sequences. 4.1% of the prioritized variants classify as having high impact on the gene products, while missense mutations prevail among the variant with moderate effect. 18.8% of the prioritized genes are not in the lists of candidate genes used by GP as input during the prioritization, demonstrating that GP is robust to detection of novel genes.
We identified genetic variants in genes involved in embryonic development. Among them one extremely rare high-impact alteration of a splice site in STAG2 on the X chromosome, coding for the cohesin complex subunit, for which inactivation in mouse is lethal and only mildly-deleterious mutations are seen in living human males. We also found an heterozygous missense mutation in the TLE4 gene, a trascriptional repressor of embryonic stem cells naive pluripotency as target of Notch, also expressed in the extravillous trophoblasts as part of the Wnt pathway, physically interacting with a region on chromosome 9 associated to miscarriages.6
##Future perspectives. 
We are interested in understanding genetic causes of miscarriages in a larger cohort of embryo samples under collection. In this pilot we developed a robust approach to investigate coding regions. The next logical extension will be to non-coding genomic regions, as well as to a more comprehensive set of variation, including copy number and structural variants.

##References
1. Pereza, N., Ostoji ́c, S., Kapovi ́c, M. & Peterlin, B.  Systematic review and meta-analysis of geneticassociation studies in idiopathic recurrent spontaneous abortion.Fertility sterility107, 150–159 (2017).
2. Rajcan-Separovic, E. Next generation sequencing in recurrent pregnancy loss-approaches and outcomes.Eur. J. Med. Genet.63, 103644 (2020).
3. Zhao, C.et al.Exome sequencing analysis on products of conception:  a cohort study to evaluateclinical utility and genetic etiology for pregnancy loss.Genet. Medicine1–8 (2020).
4. Chen, Y.et al.Characterization of chromosomal abnormalities in pregnancy losses reveals criticalgenes and loci for human early development.Hum. Mutation38, 669–677 (2017).
5. Buonaiuto S, C. V.  gp:  a pipeline for genomic prioritization.  https://github.com/ezcn/grep (2020).[Online; accessed 11-November-2020].
6. Laisk, T.et al.The genetic architecture of sporadic and recurrent miscarriage.bioRxiv575167 (2019).

Keywords: miscarriages, variant prioritization, whole-genome DNA sequence

Contacts: vincenza.colonna@igb.cnr.it, silvia.buonaiuto@igb.cnr.it

Website(s): https://colonnalab.github.io/laboratory_WebPage/, https://github.com/ezcn/grep
