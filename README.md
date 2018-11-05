# Personalized-Medicine-Redefining-Cancer-Treatment
**Personalized-Medicine-Redefining-Cancer-Treatment** is a problem of classifying the given genetic mutations based on the literature available in the medical domain into one of the given 9 classes. 
In reality, The molecular pathologist searches for evidence in the medical literature that is relevant to the given genetic variations. 
Finally, this molecular pathologist spends a huge amount of time analyzing the evidence related to each of the variations to classify them. 
The goal of this case study is to replace the last step with a machine learning model.


# Dataset 

Dataset consists of two files namely **[training_variants,training_text]**


###### training_variants: 
 comma separated file containing the description of the genetic mutations used for training. Fields are ID (the id of the row used to link the mutation to the clinical evidence), Gene (the gene where this genetic mutation is located), Variation (the aminoacid change for this mutations), Class (1-9 the class this genetic mutation has been classified on)
training_text (ID, Text)

**Ex:**

ID,Gene,Variation,Class

0,FAM58A,Truncating Mutations,1

1,CBL,W802*,2

2,CBL,Q249E,2

###### training_text: 
a double pipe (||) delimited file that contains the clinical evidence (text) used to classify genetic mutations. Fields are ID (the id of the row used to link the clinical evidence to the genetic mutation), Text (the clinical evidence used to classify the genetic mutation)

**Ex:**

ID,Text

0||Cyclin-dependent kinases (CDKs) regulate a variety of fundamental cellular processes. CDK10 stands out as one of the last
orphan CDKs for which no activating cyclin has been identified and no kinase activity revealed. Previous work has shown that CDK10
silencing increases ETS2 (v-ets erythroblastosis virus E26 oncogene homolog 2)-driven activation of the MAPK pathway, which
confers tamoxifen resistance to breast cancer cells. The precise mechanisms by which CDK10 modulates ETS2 activity, and more
generally the functions of CDK10, remain elusive. Here we demonstrate that CDK10 is a cyclin-dependent kinase by identifying cyclin
M as an activating cyclin. Cyclin M, an orphan cyclin, is the product of FAM58A, whose mutations cause STAR syndrome, a human
developmental anomaly whose features include toe syndactyly, telecanthus, and anogenital and renal malformations. We show that
STAR syndrome-associated cyclin M mutants are unable to interact with CDK10. Cyclin M silencing phenocopies CDK10 silencing in
increasing c-Raf and in conferring tamoxifen resistance to breast cancer cells. CDK10/cyclin M phosphorylates ETS2 in vitro, and in
cells it positively controls ETS2 degradation by the proteasome. ETS2 protein levels are increased in cells derived from a STAR
patient, and this increase is attributable to decreased cyclin M levels. Altogether, our results reveal an additional regulatory
mechanism for ETS2, which plays key roles in cancer and development. They also shed light on the molecular mechanisms
underlying STAR syndrome.Cyclin-dependent kinases (CDKs) play a pivotal role in the control of a number of fundamental cellular
processes (1). The human genome contains 21 genes encoding proteins that can be considered as members of the CDK family
owing to their sequence similarity with bona fide CDKs, those known to be activated by cyclins (2). Although discovered almost 20 y
ago (3, 4), CDK10 remains one of the two CDKs without an identified cyclin partner. This knowledge gap has largely impeded the
exploration of its biological functions. CDK10 can act as a positive cell cycle regulator in some cells (5, 6) or as a tumor suppressor in
others (7, 8). CDK10 interacts with the ETS2 (v-ets erythroblastosis virus E26 oncogene homolog 2) transcription factor and inhibits
its transcriptional activity through an unknown mechanism (9). CDK10 knockdown derepresses ETS2, which increases the..


# Machine Learing Objectives and Constraints
1. Interpretability is very important because it provides reason why we are assigning a particular class.
2. Instead of giving Classes we need Class probabilities because probability provides confidence in our reslut.
3. Metric is Log-loss because it rewards correct prediciton and penalizes the in-correct prediciton.
4. No Latency constraints.
