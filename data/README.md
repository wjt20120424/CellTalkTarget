__`evbiog.rda` is a data.frame of the system data containing extracellular vesicle biogenesis genes__

```
> load("evbiog.rda")
> str(evbiog)
'data.frame':	75 obs. of  2 variables:
 $ species: chr  "Human" "Human" "Human" "Human" ...
 $ gene   : chr  "ARRDC1" "ARRDC4" "ATP13A2" "ATP9A" ...

# including "Human", "Mouse", "Rat"
> evbiog[evbiog$species == "Human",]$gene
 [1] "ARRDC1"  "ARRDC4"  "ATP13A2" "ATP9A"   "CD34"    "CHMP2A"  "CHMP3"   "CHMP6"   "COPS5"   "HGS"    
[11] "IFNG"    "PDCD6IP" "PRKN"    "RAB11A"  "RAB27A"  "RAB7A"   "SDC1"    "SDC4"    "SDCBP"   "SMPD3"  
[21] "SNF8"    "STAM"    "TSG101"  "VPS4A"   "VPS4B"
```

__`risc.rda` is a data.frame of the system data containing RNA-induced silencing complex (RISC) related genesfor the inference of MiTIs with negative regulation__

```
> load("risc.rda")
> str(risc)
'data.frame':	36 obs. of  2 variables:
 $ species: chr  "Human" "Human" "Human" "Human" ...
 $ gene   : chr  "AGO1" "AGO2" "AGO3" "AGO4" ...

# including "Human", "Mouse", "Rat"
> risc[risc$species == "Human",]$gene
 [1] "AGO1"     "AGO2"     "AGO3"     "AGO4"     "DICER1"   "HSPA4"    "HSP90AA1" "HSP90AB1" "HSPA8"   
[10] "HOPX"     "DNAJA2"   "PTGES3"
```

__`ritac.rda` is a data.frame of the system data containing RNA-induced transcriptional activation complex (RITAC) related genes for the inference of MiTIs with positive regulation__

```
> load("ritac.rda")
> str(ritac)
'data.frame':	45 obs. of  2 variables:
 $ species: chr  "Human" "Human" "Human" "Human" ...
 $ gene   : chr  "AGO2" "DHX9" "PAF1" "LEO1" ...

# including "Human", "Mouse", "Rat"
> ritac[ritac$species == "Human",]$gene
 [1] "AGO2"    "DHX9"    "PAF1"    "LEO1"    "CTR9"    "CDC73"   "RTF1"    "SKIC8"  
 [9] "SUPT4H1" "SUPT5H"  "SUPT16H" "SSRP1"   "TCEA1"   "TCEA2"   "TCEA3" 
```

__`mir2tar.rda` include two data.frame of the system data containing containing information of EV-derived miRNA and miRNA-target interactions(MiTIs)__

```
> load("mir2tar.rda")
> str(mir_info)
'data.frame':	3934 obs. of  10 variables:
 $ miRNA            : chr  "hsa-let-7a" "hsa-let-7a" "hsa-let-7a-2" "hsa-let-7b" ...
 $ miRNA_mature     : chr  "hsa-let-7a-3p" "hsa-let-7a-5p" "hsa-let-7a-2-3p" "hsa-let-7b-3p" ...
 $ gene             : chr  "MIRLET7A1" "MIRLET7A1" "MIRLET7A2" "MIRLET7B" ...
 $ species          : chr  "Human" "Human" "Human" "Human" ...
 $ EV_evidence      : chr  "ExoCarta; Vesiclepedia; EVmiRNA" "ExoCarta; Vesiclepedia; EVmiRNA" "Vesiclepedia; ExoCarta" "ExoCarta; Vesiclepedia; EVmiRNA" ...
 $ tissue_TarBase   : chr  "Lymphatic tissue; Kidney; Cervix; Fetal kidney; Bone marrow; Umbilical vein; Pancreas; Brain - Cingulate gyrus;"| __truncated__ "Kidney; Embryo; Pleura; Lymphatic tissue; Cervix; Bone marrow; Fetal kidney; Umbilical vein; Pancreas; Brain - "| __truncated__ "Breast; Brain" "Cervix; Bone marrow; Umbilical vein; Pancreas; Brain - Motor cortex; Brain - Cingulate gyrus; Breast; Blood; Lu"| __truncated__ ...
 $ celltype_TarBase : chr  "B lymphocytes; Epithelial cells; CD4+ T cells; Mesenchymal stem cells; Fibroblasts; Endothelial cells; Pancreat"| __truncated__ "Epithelial cells; Stem cells; B lymphocytes; CD4+ T cells; Mesenchymal stem cells; Fibroblasts; Endothelial cel"| __truncated__ "Epithelial cells" "Epithelial cells; CD4+ T cells; Mesenchymal stem cells; Fibroblasts; Endothelial cells; Pancreatic Islets; Mono"| __truncated__ ...
 $ seq              : chr  "CUAUACAAUCUACUGUCUUUC" "UGAGGUAGUAGGUUGUAUAGUU" "CUGUACAGCCUCCUAGCUUUCC" "CUAUACAACCUACUGCCUUCCC" ...
 $ circulating_miRNA: chr  "ASRA" "ASRA" "NA" "ASRA" ...
 $ avg_rpm          : num  1.247 5719.045 0 0.026 7393.804 ...

> str(mir2tar)
'data.frame':	6212276 obs. of  9 variables:
 $ miRNA       : chr  "hsa-miR-1" "hsa-miR-200a" "hsa-miR-9" "hsa-miR-4701" ...
 $ source      : chr  "miRTarBase: MIRT002769" "miRTarBase: MIRT732658" "miRTarBase: MIRT732659" "miRTarBase: MIRT683071" ...
 $ miRNA_mature: chr  "hsa-miR-1-3p" "hsa-miR-200a-3p" "hsa-miR-9-5p" "hsa-miR-4701-3p" ...
 $ target_gene : chr  "RBM28" "FOXG1" "FOXG1" "A1BG" ...
 $ species     : chr  "Human" "Human" "Human" "Human" ...
 $ experiments : chr  "Microarray" "Western blot" "Western blot" "HITS-CLIP" ...
 $ support     : chr  "Functional MTI (Weak)" "Functional MTI" "Functional MTI" "Functional MTI (Weak)" ...
 $ pmid        : num  15685193 25937343 25937343 23706177 23706177 ...
 $ regulation  : chr  "Negative" "Negative" "Negative" "Negative" ...
```

|__Species__|__Number of EV-derived miRNAs__|__Number of EV-derived MiTIs__|
|:---:    |:---:   |:---:  |
|Human| 2,567  |1,595,450|
|Mouse| 935    |484,123  |
|Rat  | 179    |1,626    |


__`mir2path.rda` is a data.frame of the system data containing miRNA-related pathways from KEGG, Reactome, GO_BP, Wikipathways__

```
> load("mir2path.rda")
> str(mir2path)
'data.frame':	130339 obs. of  4 variables:
 $ term  : chr  "2-OXOCARBOXYLIC ACID METABOLISM" "ABC TRANSPORTERS" "ABC TRANSPORTERS" "ABC TRANSPORTERS" ...
 $ mir   : chr  "hsa-miR-4323" "hsa-miR-223-3p" "hsa-miR-548q" "hsa-miR-5571-3p" ...
 $ type  : chr  "KEGG" "KEGG" "KEGG" "KEGG" ...
 $ source: chr  "miRPathDB2" "miRPathDB2" "miRPathDB2" "miRPathDB2" ...
```

|__Functional annotation type__|__Total number__|__Unique number__|
|:---:    |:---:   |:---:  |
|GO BP        | 77,897    |6,040|
|KEGG         | 8,416     |261  |
|Reactome     | 26,530    |1,592|
|Wikipathways | 17,496    |458  |


__`geneinfo.rda` is a data.frame of the system data containing gene symbols__

```
> load("geneinfo.rda")
> str(geneinfo)
'data.frame':	288559 obs. of  3 variables:
 $ symbol  : chr  "A1BG" "A1BG" "A1BG" "A1BG" ...
 $ synonyms: chr  "A1B" "ABG" "GAB" "HYST2477" ...
 $ species : chr  "Human" "Human" "Human" "Human" ...
```

__`gene2gene.rda` is a data.frame of the system data containing the gene orthologs among human, mouse, and rat__

```
> load("gene2gene.rda")
> str(gene2gene)
'data.frame':	33071 obs. of  3 variables:
 $ gene      : chr  "ZGLP1" "LDLRAP1" "MDN1" "PRR35" ...
 $ gene_other: chr  "Zglp1" "Ldlrap1" "Mdn1" "A930017K11Rik" ...
 $ species   : chr  "Mouse" "Mouse" "Mouse" "Mouse" ...
```

__`gene2path.rda` is a data.frame of the system data containing gene-related pathways from KEGG, Reactome, GO_BP, Wikipathways__

```
> load("gene2path.rda")
> str(gene2path)
'data.frame':	2817311 obs. of  5 variables:
 $ term   : chr  "ABC TRANSPORTERS" "ABC TRANSPORTERS" "ABC TRANSPORTERS" "ABC TRANSPORTERS" ...
 $ gene   : chr  "ABCA1" "ABCA10" "ABCA12" "ABCA13" ...
 $ type   : chr  "KEGG" "KEGG" "KEGG" "KEGG" ...
 $ species: chr  "Human" "Human" "Human" "Human" ...
 $ source : chr  "msigdbr" "msigdbr" "msigdbr" "msigdbr" ...
```

