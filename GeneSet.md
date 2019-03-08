# `Kevin's gene set`




### From GO:1904749 (http://amigo.geneontology.org/amigo/term/GO:1904749) (Regulation of protein localization to nucleus). As 2019-02-18. seven human proteins are annotated to this term. (http://amigo.geneontology.org/amigo/term/GO:1904749)


```R pu
# Fetch gene symbols for GO:1904749 yields 6 unique human proteins
#  (http://amigo.geneontology.org/amigo/term/GO:1904749)

GO_1904749set <- c("PINX1", "MCRS1", "NMD3", "POLR1A",
                   "TERT", "NVL")

# validate: all symbols in HGNC dataset; load the HGNC.RData

load("~/Desktop/Bioinformatics/BCB420/BCB420-2019-resources-master/HGNC.RData")

HGNC[GO_1904749set, c("sym", "name")]  # yes, no NA's seen

```

#from KEGG pathway hsa05412 which is nuclear localization of plakoglobin, gene symbols are listed on the map 


                      
KEGGset_hsa05412<- c("CTNNB1","LEF1","JUP","DSP","EMD","LMNA"
,"DES")
                      
##Are all these symbols in the HGNC set???

HGNC[KEGGset_hsa05412, c("sym", "name")]  # yes since there is no n/a


## Expert reveiw's gene set of paper "Protein Localization to the nucleous: a search for targeting domains in nucleolin"
  
             
##paper "Localization of the AP-3 adaptor complex defines a novel
##endosomal exit site for lysosomal membrane proteins"

Adaptor_Proteins_set <- c("AP1M2","AP2M1","AP3S1","AP4S1","LAMP1","LAMP2",
                         "SCARB2","CD63","CD1A")
HGNC[Adaptor_Proteins_set, c("sym", "name")]                         

#From artile "The molecular architecture of the nuclear pore complex"
#Below is Nuclear Pore Complex(NPC) set of genes; There are many proteins in nuclear
#pore complex but only a few involved in transportation of protein

NPC_set <- c("NUP133","NUP120","Nup85","Nup170","Nup188","Nic96","Nup82","Tpr","")

HGNC[NPC_set, c("sym", "name")]                         

##From paper "Nuclear Localization and Regulation of erk- and rsk-Encoded Protein Kinases" 

Regulation_erk <-c("MAP2","NR4A1","RSK","FER","SRF","MAPK1")

HGNC[Regulation_erk, c("sym", "name")]                         



