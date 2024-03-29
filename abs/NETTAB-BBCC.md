# Identification of genomic variants responsible for pregnancy loss: a pilot study

Silvia Buonaiuto 1,2∗ , Imma Di Biase 3∗ , Valentina Aleotti 4∗ , Gianluca Damaggio 1,5 , Palmira D’Ambrosio 3 ,
Oriana Catapano 3 , Gabriella Esposito 3 , Marco Chierici 6 , Madhuri Pulijala 7 , Qasim Ayub 7 , Ce-
sare Furlanello 6 , Erik Garrison 8 , Nicole Soranzo 9 , Michele Rubini 4 , Sebastiano Di Biase 3 , and
Vincenza Colonna 1

∗equal contribution

1. National Research Council, Institute of Genetics and Biophysics Adriano Buzzati-Traverso, Napoli, Italy ;

2. Department of Environmental, Biological and Pharmaceutical Sciences and Technologies, University of
Campania Luigi Vanvitelli, Caserta, Italy; 

3. MeriGen Research s.r.l., Napoli, Italy; 

4. University of Ferrara,
Ferrara, Italy; 

5. Department of Biology, University of Naples Federico II, Naples, Italy; 

6. FBK - Fondazione Bruno Kessler, Povo (Trento), Italy; 

7. Monash University Malaysia Genomics Facility, School of Science,
Bandar Sunway; 

8. University of California, Santa Cruz, US; 8. Wellcome Sanger Institute, Hinxton, UK .


## Introduction
Pregnancy Loss (PL) is the spontaneous termination of pregnancy confirmed by at least two positive
human chorionic gonado-trophin (b-hCGs) in the serum or urine or by ultrasound or histology (miscar-
riage). Recurrent Pregnancy Loss (RPL) is the loss of two or more pregnancies before 24 weeks of
gestation [1]. It is estimated that pregnancy loss occurs in 10-15% of all pregnancies [2, 3, 4], while the
exact prevalence of RPL is more difficult to estimate, and current estimates are 0.8 to 3% according to
the type of pregnancy loss and the method used for the diagnosis [2].
PL has both environmental and genetic causes [2]. Sporadic PL is often the result of occasional chro-
mosomal aneuploidies of the gametes [5]. On the contrary, RPL is believed to have non-random genetic
causes and is often due to parental genetic defects [6]. The incidence of genomic abnormalities in RPL is
estimated to be around 50% [7]. Current techniques for the analysis of pregnancy or fetal tissue include
karyotyping, fluorescence in situ hybridization (FISH), or array-based comparative genomic hybridization
(array-CGH). Among these, array-CGH is the most accurate and highest resolution method [8, 9, 10].
Nevertheless, variants discovered by array-CGH are of at least several thousand base pairs, and a wide
range of smaller variants cannot be accessed by this technology. Next-generation sequencing is cur-
rently used to predict trisomies. However, sequencing is usually done at very low resolution and limited
to exomes, i.e. 2% of the genome, leaving unexplored the vast majority of the genome.
To date, PLs are studied using parental genetic information [11, 12]. Only a few studies have focused on
understanding the genetic causes of PL through the analysis of the fetal genome sequence, and these
have been limited to target regions related to specific medical conditions known to be associated with PL
[13]. Therefore, very little is known about the genetic mutations that effectively cause the death of the
embryo, and there is a need for large scale projects that systematically target small-size genetic muta-
tions to understand their relationship with PL.
We aim to identify genetic variants likely to cause PL that are not seen by current diagnostic tools either
because of their very small size or because they lie in non-coding regulatory regions of the genome that
are not routinely sequenced. To achieve this we will build a predictive model to integrate high-coverage
whole-genome sequence data with information on functional annotations and gene networks relevant to
embryonic development. Here we present the results of a pilot study in which we aim to establish pro-
cedures and protocols and estimate the needs for the realization of a larger project, such as the number
of samples required to reach robust conclusions and the computational resources that the analysis de-
mands. As preliminary results, we present the outcomes of the analysis of whole-genome sequence data
from six samples. While the full predictive model is still under development, we show that raw filtering for
deleterious variants based on simple criteria identified homozygous non-synonymous mutations shared
by three samples, showing the potential of developing the full project.

## Methods
Data and sample collection
The project relies on a collection of 194 samples of which 96 are pregnancy loss (PL) and 98 are induced
abortions. Each sample includes fetal DNA extracted from chorionic villi, maternal DNA, and the mother’s
medical records for more than 100 parameters including the most relevant PL comorbidities. Within the
PL, 70% are recurrent. The medical records of induced abortions were used to obtain reference intervals
representative of healthy mothers and used to rank the PL mothers to exclude environmental causes
and other comorbidities as causes of PL. The project has been approved by the ethical committee of the
University of Ferrara and all samples are anonymous.
Pre-sequencing screening
PL samples with no obvious evidence of environmental etiology were screened for the quality of DNA
and maternal contamination. Samples with good quality DNA were screened for aneuploidies of the
chromosomes 13,15,16,18,21,22, X, and Y using highly polymorphic tetra- and penta-nucleotide repeats
through quantitative PCR.
Array-based Comparative Genomic Hybridization (array-CGH) was carried out using 60k probes genome-
wide distributed (Agilent SurePrint G3 CGH-only). The log-ratio produced by the Agilent CytoGenomics
v3.0.4 software was segmented into regions of estimated equal copy number using both the method
implemented in the Agilent, and the Penalized least square implemented in the copynumber R package
[14] and classified as copy number of gains or losses (copy number variants, CNV) requiring at least five
probes and Z-score <0.0016 (i.e., four times the standard deviation)[15].
Whole-genome sequence analysis
30X whole-genome sequences were produced by Macrogen-europe. Sequence reads were aligned to
the reference genome using BWA-MEM. Variant calling was performed using Freebayes [16] for single
nucleotide variants and small indels and svtools[17] for structural variants. Genomic variants were anno-
tated with the prediction of their functional impact using Variant Effect Predictor [18] and ANNOVAR[19].
Filtering of variants was done using custom Python/R scripting, publicly available on the project reposi-
tory https://github.com/ezcn/grepl .

## Results
We first demonstrate that our PL data set complies with the standards of PL described in the literature
and hence can be used to investigate genetic mutations causing embryonic death. Gestational age at
pregnancy termination, calculated as the interval between the date in which the pregnancy termination
is discovered and the last menstruation date, ranges from 4 to 19.4 weeks. Because the pregnancy
termination might happen days or weeks before being discovered, we could not determine the age of the
embryo at its death since there was no information from which it could be deduced. The median age
of the mother at the event is significantly higher in recurrent PL compared to first PL (39.0 years and
28.9 years respectively, MW p-value= 2.844e-06). Menarche age has a significantly larger variance in
recurrent PL (range: 9-16 years) compared to both first PL (range: 8-17 years, F-test p-value 0.0288)
and induced abortions (range: 11-15 years, F-test p-value 0.00164). Among PL the maximum number of
full-term births prior to this event is three (range: 1-6 , mean value:1.553) while among induced abortion
is six.
We estimate that about 18% of the 96 PL samples (i.e. roughly 18 samples) have no obvious genetic
abnormalities in the range of those that is currently possible to ascertain and therefore are suitable for
the identification of novel genomic variants responsible for PL through whole-genome analysis. After ex-
cluding non-genetic comorbidities, 10% of cases is excluded for maternal contamination. A further 40%
is discarded for aneuploidies discovered either by qfPCR (30%) or array-CGH (10%). Of the remaining
cases, 18% is euploid and do not show deleterious copy-number variants after array-CGH, while 32%
remain unresolved probably due to poor quality of the DNA.
In the first six samples that have been sequenced, we find as expected 3.8M single nucleotide poly-
morphisms (3.6M median, 0.35M standard deviation), and 781k indels (746k median, 0.6k standard
deviation, when compared with the reference genome and after filtering for quality. We annotated the
variable sites with the information currently available on databases of functional consequences based on
prediction and empirical evidence. We found that on autosomes 4.3k variants are ranked as having a
high impact according to the Variant Effect Predictor scale [18], 69.1k moderate, and 111k low.
In the genome of the six sequenced PL, we find the effect allele at two loci associated with sporadic
and one with recurrent pregnancy loss [11]. These findings need to be interpreted with caution since
the allele frequencies in our sample follow those of the general European population and the size of the
sample does not allow significant conclusions. Nevertheless, it is encouraging not to find allele with no
consequences.
We are developing a model to rank variants predicted to be deleterious under a model of complex poly-
genic inheritance. The model works on a per-individual base and is made of three layers. The first is the
genetic variants described by their genotype likelihood inferred from the variant calling. The second is the
set of annotations on the functional consequences of the alleles. The third is the information on genes
related to embryonic development, early-stage developmental disorders, parental imprinting. We plan to
integrate this information to build a predictive model based on the assumption that causative mutations
act in synergy as in complex traits. We are currently building and testing the pipeline to determine its
effectiveness and the computational resources required. Meanwhile, as a proof of principle, we applied
raw filtering based on the combination of several criteria like allele frequencies in the general population
(selected to be extremely rare), homozygosity, impact of the allele with consequences. Our preliminary
results identify a number of putatively detrimental mutations. Among those, three samples carry two ho-
mozygous missense mutations in the AHNAK2 cancer-related gene, coding a cytoplasmic nucleoprotein
whose high expression is associated with negative prognosis of several cancers.

## Conclusions
We explored possibilities tested feasibility of a study for the identification of novel genomic variants caus-
ing pregnancy loss based on the integration of state of the art methodology for genomic analysis with
existing methods for genetic testing in PL.
We are confident that the inclusion/exclusion criteria used for collecting samples are adequate but we
also learned that they can be improved to reduce the number of missing information and to better define
the cases. We find that roughly 18% of the collected samples are suitable for whole-genome sequencing
after controlling for maternal contamination, DNA quality, and large chromosomal aberrations. Therefore
we estimate that collecting at least a thousand samples will allow sequencing of roughly two-hundred.
It remains to be determined which fraction of sequences if actually informative to better predict the re-
quired sample size, and this could be possible once the analysis of the first sequences produced will be
completed.
We are working on a model to rank variants according to their deleteriousness. Meanwhile, we have
evidence that some of the allele identified as potentially detrimental by our primitive filtering method, are
shared among three of the six samples, suggesting that this approach could be valid also with small
sample size.
In conclusion, the pilot study described here represents a milestone and provides essential indications
for the realization of a larger study.

## References

[1] E. G. G. on RPL, R. Bender Atik, O. B. Christiansen, J. Elson, A. M. Kolte, S. Lewis, S. Middeldorp, W. Nelen,
B. Peramo, S. Quenby, et al., “Eshre guideline: recurrent pregnancy loss,” 2018.

[2] E. C. Larsen, O. B. Christiansen, A. M. Kolte, and N. Macklon, “New insights into mechanisms behind miscar-
riage,” BMC medicine, vol. 11, no. 1, p. 154, 2013.

[3] L. Ammon Avalos, C. Galindo, and D.-K. Li, “A systematic review to calculate background miscarriage rates
using life table analysis,” Birth Defects Research Part A: Clinical and Molecular Teratology, vol. 94, no. 6,
pp. 417–423, 2012.

[4] A.-M. N. Andersen, J. Wohlfahrt, P. Christens, J. Olsen, and M. Melbye, “Maternal age and fetal loss: popula-
tion based register linkage study,” Bmj, vol. 320, no. 7251, pp. 1708–1712, 2000.

[5] R. M. Silver and D. Branch, “Sporadic and recurrent pregnancy loss,” Handbook of Clinical Obstetrics: The
Fetus & Mother, Third Edition, pp. 41–46, 2008.

[6] G.-t. G. No, “The investigation and treatment of couples with recurrent first-trimester and second-trimester
miscarriage,” April 2011, 2011.

[7] M. M. van den Berg, M. C. van Maarle, M. van Wely, and M. Goddijn, “Genetics of early miscarriage,” Biochim-
ica et Biophysica Acta (BBA)-Molecular Basis of Disease, vol. 1822, no. 12, pp. 1951–1959, 2012.

[8] C. Robberecht, V. Schuddinck, J.-P. Fryns, and J. R. Vermeesch, “Diagnosis of miscarriages by molecular
karyotyping: benefits and pitfalls,” Genetics in Medicine, vol. 11, no. 9, p. 646, 2009.

[9] R. Kudesia, M. Li, J. Smith, A. Patel, and Z. Williams, “Rescue karyotyping: a case series of array-based
comparative genomic hybridization evaluation of archival conceptual tissue,” Reproductive Biology and En-
docrinology, vol. 12, no. 1, p. 19, 2014.

[10] N. Mathur, L. Triplett, and M. D. Stephenson, “Miscarriage chromosome testing: utility of comparative genomic
hybridization with reflex microsatellite analysis in preserved miscarriage tissue,” Fertility and sterility, vol. 101,
no. 5, pp. 1349–1352, 2014.

[11] T. Laisk, A. L. G. Soares, T. Ferreira, J. N. Painter, S. Laber, J. Bacelis, C.-Y. Chen, M. Lepamets, K. Lin, S. Liu,
et al., “The genetic architecture of sporadic and recurrent miscarriage,” bioRxiv, p. 575167, 2019.

[12] N. Pereza, S. Ostojić, M. Kapović, and B. Peterlin, “Systematic review and meta-analysis of genetic association
studies in idiopathic recurrent spontaneous abortion,” Fertility and sterility, vol. 107, no. 1, pp. 150–159, 2017.

[13] I. Filges and J. M. Friedman, “Exome sequencing for gene discovery in lethal fetal disorders–harnessing the
value of extreme phenotypes,” Prenatal diagnosis, vol. 35, no. 10, pp. 1005–1009, 2015.

[14] G. Nilsen, K. Liestøl, P. Van Loo, H. K. M. Vollan, M. B. Eide, O. M. Rueda, S.-F. Chin, R. Russell, L. O.
Baumbusch, C. Caldas, et al., “Copynumber: efficient algorithms for single-and multi-track copy number seg-
mentation,” BMC genomics, vol. 13, no. 1, p. 591, 2012.

[15] J. R. Vermeesch, C. Melotte, G. Froyen, S. Van Vooren, B. Dutta, N. Maas, S. Vermeulen, B. Menten, F. Spele-
man, B. De Moor, et al., “Molecular karyotyping: array cgh quality criteria for constitutional genetic diagnosis,”
Journal of Histochemistry & Cytochemistry, vol. 53, no. 3, pp. 413–422, 2005.

[16] E. Garrison and G. Marth, “Haplotype-based variant detection from short-read sequencing,” arXiv preprint
arXiv:1207.3907, 2012.

[17] D. E. Larson, H. J. Abel, C. Chiang, A. Badve, I. Das, J. M. Eldred, R. M. Layer, and I. M. Hall, “svtools:
population-scale analysis of structural variation,” bioRxiv, p. 494203, 2018.

[18] W. McLaren, L. Gil, S. E. Hunt, H. S. Riat, G. R. Ritchie, A. Thormann, P. Flicek, and F. Cunningham, “The
ensembl variant effect predictor,” Genome biology, vol. 17, no. 1, p. 122, 2016.

[19] K. Wang, M. Li, and H. Hakonarson, “Annovar: functional annotation of genetic variants from high-throughput
sequencing data,” Nucleic acids research, vol. 38, no. 16, pp. e164–e164, 2010.
