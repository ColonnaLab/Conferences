# Identification of genomic variants responsible for pregnancy loss: a pilot study 

Buonaiuto S. 1, 2 ∗ , Di Biase I. 3 ∗ , Aleotti V. 4 ∗ , Ravaei A. 4, Damaggio G. 1 , 5 , D’Ambrosio P. 3 , Catapano O. 3 , Esposito G. 3 , Chierici M. 6 , Pulijala M. 7 , Ayub Q. 7 , Furlanello C. 6 , Garrison E. 8 , Soranzo N. 9 , Capalbo A. 10 , Rubini M. 4 , Di Biase S. 3 , and Colonna V. 1
∗ equal contribution

1. National Research Council, Institute of Genetics and Biophysics Adriano Buzzati-Traverso, Napoli, Italy; 

2. Department of Environmental, Biological and Pharmaceutical Sciences and Technologies, University of Campania Luigi Vanvitelli, Caserta, Italy; 

3. MeriGen Research s.r.l., Napoli, Italy; 

4. University of Ferrara, Ferrara, Italy; 

5. Department of Biology, University of Naples Federico II, Naples, Italy; 

6. FBK-Fondazione Bruno Kessler, Povo (Trento), Italy; 

7. Monash University Malaysia Genomics Facility, School of Science, Bandar Sunway; 

8. University of California, Santa Cruz, US;

9. Wellcome Sanger Institute, Hinxton, UK;10. Igenomix Italy, Marostica, Italy



## Study question: 
Do whole-genome sequences of embryos from recurrent pregnancy loss clarify the impact of genetic variants of small-size and/or located in non-coding regulatory regions?  

## Summary answer:
Whole-genome analysis of embryonic DNA from pregnancy loss successfully identifies putatively detrimental genomic variants

## What is known already:
100 Pregnancy Loss (PL), the spontaneous demise of a pregnancy before 24 weeks of gestation, occurs in 10-15% of pregnancies. PL is often the result of chromosomal aneuploidies of the gametes but it can also have non random genetic causes like small mutations (SNPs and indels), both de-novo or inherited from parents. Comparative genomic hybridization (CGH) detects variants of several thousand base pairs while targeted resequencing resolves point mutations. Both are currently the most accurate methods for the genetic analysis of PL, but are not sensitive to small variants (CGH), or do not target those located in non-coding regulatory regions (targeted resequencing). 
Study design, size, duration: 75  Our aim is to identify small-size genetic variants likely to cause PL using a predictive model integrating whole-genome sequence data with functional annotations and gene networks relevant to embryonic development. Seventy women, mostly European (82.7%) diagnosed with first (n=39, av.age 28.9 ) or recurrent (n=31, av.age 39.0) miscarriage  were recruited by the University of Ferrara from 2017 to 2019. Ethical committee approval is from Emilia-Romagna CE/FE (#170475).

## Participants/materials, setting, methods: 
Fetal DNA extracted from chorionic villi was used to exclude samples with aneuploidies using both CGH and shallow sequencing of random genomic regions. Euploid samples were whole-genome sequenced at high-coverage. Variant calling against the reference genome GRCh38 was done using Freebayes. Variants were annotated with a custom script that integrates information from Ensembl99 with publicly available manually curated lists of genes associated with embryonic development, miscarriages, lethality, cell cycle. The code is available on gitHub (ezcn/grep) .  

## Main results and the role of chance: 
200 We understood the requirements to scale-up the project and obtained initial results from the analysis of these genomic sequences. We determined that shallow sequencing of random genomic regions is more efficient compared to CGH in detecting aneuploidies in samples with poor quality DNA. We estimated that 20% of collected samples are suitable for sequencing, the rest presenting aneuploidies or quality issues and maternal contamination. Sequenced samples have on average 4M high-quality variable sites that were annotated with information on gene content and functional consequences. In the autosomes 4.3k variants are ranked as having a high deleterious impact according to Ensembl, 69.1k moderate, and 111k low. After filtering based on the combination of several criteria, such as allele frequency in the general population, homozygosity, impact of the allele with consequences we identify a number of putatively detrimental mutations. Three samples carry two homozygous missense mutations in the same exon of the AHNAK2 cancer-related gene, which codes for a cytoplasmic nucleoprotein. Five samples share the same stop gain mutation in the RPTOR gene, a component of a signaling pathway which regulates cell growth and survival, and autophagy in response to nutrient and hormonal signals.
