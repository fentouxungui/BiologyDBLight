
<!-- README.md is generated from README.Rmd. Please edit that file -->

# BiologyDBLight

<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
<!-- badges: end -->

此R包源自于`fentouxungui/BiologyDB`包，删除了数据库的整理过程，仅整理好的数据，如需查看或修改数据，建议安装`fentouxungui/BiologyDB`包。

> 为什么做这件事？
> 初衷是用于做基因的注释，后来发现有些数据库多多少少有些问题，比如基因名错了、基因ID过时了等等，为了方便重复使用数据库，所以将常用的数据库整理好了，方便重复调用。数据库预处理的原则是简单又灵活。

软件功能： **基因水平的注释**。

## 安装

``` r
library(devtools)
install_github("fentouxungui/BiologyDBLight")
```

## 数据

``` r
library(BiologyDB)
d <- data(package = "BiologyDB")
d$results[,"Item"]
#>  [1] "AnimalTFDB_Fly_TF"                                                
#>  [2] "AnimalTFDB_Fly_TFCofactors"                                       
#>  [3] "AnimalTFDB_Human_TF"                                              
#>  [4] "AnimalTFDB_Human_TFCofactors"                                     
#>  [5] "AnimalTFDB_Mouse_TF"                                              
#>  [6] "AnimalTFDB_Mouse_TFCofactors"                                     
#>  [7] "CellChat_Human_LigandReceptorsInteractions"                       
#>  [8] "CellChat_Human_Ligands"                                           
#>  [9] "CellChat_Human_Receptors"                                         
#> [10] "CellChat_Mouse_LigandReceptorsInteractions"                       
#> [11] "CellChat_Mouse_Ligands"                                           
#> [12] "CellChat_Mouse_Receptors"                                         
#> [13] "CellPhoneDB_Human_Interactions"                                   
#> [14] "CellPhoneDB_Human_Ligands"                                        
#> [15] "CellPhoneDB_Human_Receptors"                                      
#> [16] "CellTalkDB_Human_Interactions"                                    
#> [17] "CellTalkDB_Mouse_Interactions"                                    
#> [18] "Flybase_Fly_AutomatedGeneSummary"                                 
#> [19] "Flybase_Fly_BestGeneSummary"                                      
#> [20] "Flybase_Fly_GeneSnapshots"                                        
#> [21] "Flybase_Fly_Genes"                                                
#> [22] "GENCODE_Human_Genes"                                              
#> [23] "GENCODE_Mouse_Genes"                                              
#> [24] "GENEONTOLOGY_Fly"                                                 
#> [25] "GENEONTOLOGY_Human"                                               
#> [26] "GENEONTOLOGY_Mouse"                                               
#> [27] "HPA_Human_102Genes_SecretedAndFDAApprovedDrugTargets"             
#> [28] "HPA_Human_12631Genes_NotSecretedOrMembraneBound"                  
#> [29] "HPA_Human_1708Genes_BothSecretedAndMembraneBound"                 
#> [30] "HPA_Human_1708Genes_Secreted"                                     
#> [31] "HPA_Human_19670Genes_GODiseaseDistributionLocation"               
#> [32] "HPA_Human_429Genes_MembraneBoundAndHasFDAApprovedDrugTargets"     
#> [33] "HPA_Human_5520Genes_MembraneBound"                                
#> [34] "HPA_Human_754Genes_FDAApprovedDrugTargets"                        
#> [35] "HPA_Human_ProteinClass_CD"                                        
#> [36] "HPA_Human_ProteinClass_GPCR"                                      
#> [37] "HPA_Human_ProteinClass_Plasma"                                    
#> [38] "HPA_Human_ProteinClass_Transporters"                              
#> [39] "HPA_Human_ProteinClass_VoltageGatedIonChannels"                   
#> [40] "Human_GuideToPHARMACOLOGY_Interactions_LigandTargetsFull"         
#> [41] "Human_GuideToPHARMACOLOGY_Interactions_LigandTargetsFull_Expanded"
#> [42] "Human_GuideToPHARMACOLOGY_Interactions_OnlyTargetsFull_Expanded"  
#> [43] "Human_GuideToPHARMACOLOGY_LigandsPeptides"                        
#> [44] "Human_GuideToPHARMACOLOGY_Targets"                                
#> [45] "Mouse_GuideToPHARMACOLOGY_Interactions_LigandTargetsFull"         
#> [46] "Mouse_GuideToPHARMACOLOGY_Interactions_LigandTargetsFull_Expanded"
#> [47] "Mouse_GuideToPHARMACOLOGY_Interactions_OnlyTargetsFull_Expanded"  
#> [48] "Mouse_GuideToPHARMACOLOGY_LigandsPeptides"                        
#> [49] "Mouse_GuideToPHARMACOLOGY_Targets"                                
#> [50] "NCBI_Human_GeneSummary"                                           
#> [51] "NCBI_Mouse_GeneSummary"                                           
#> [52] "TheHumanTranscriptionFactors"                                     
#> [53] "UniProt_Human_GeneFunction"                                       
#> [54] "UniProt_Mouse_GeneFunction"                                       
#> [55] "UniProt_ProteinFamily_AllSpecies"                                 
#> [56] "UniProt_ProteinFamily_Human"                                      
#> [57] "UniProt_ProteinFamily_Mouse"                                      
#> [58] "VerSeDa_Mouse_SecretomePrediction"
```

## R sessions

``` r
sessionInfo()
#> R version 4.4.1 (2024-06-14 ucrt)
#> Platform: x86_64-w64-mingw32/x64
#> Running under: Windows 11 x64 (build 22631)
#> 
#> Matrix products: default
#> 
#> 
#> locale:
#> [1] LC_COLLATE=Chinese (Simplified)_China.utf8 
#> [2] LC_CTYPE=Chinese (Simplified)_China.utf8   
#> [3] LC_MONETARY=Chinese (Simplified)_China.utf8
#> [4] LC_NUMERIC=C                               
#> [5] LC_TIME=Chinese (Simplified)_China.utf8    
#> 
#> time zone: Asia/Shanghai
#> tzcode source: internal
#> 
#> attached base packages:
#> [1] stats     graphics  grDevices utils     datasets  methods   base     
#> 
#> other attached packages:
#> [1] BiologyDB_0.0.0.9000
#> 
#> loaded via a namespace (and not attached):
#>  [1] compiler_4.4.1    fastmap_1.2.0     cli_3.6.3         tools_4.4.1      
#>  [5] htmltools_0.5.8.1 rstudioapi_0.16.0 yaml_2.3.8        rmarkdown_2.27   
#>  [9] knitr_1.47        xfun_0.45         digest_0.6.36     rlang_1.1.4      
#> [13] evaluate_0.24.0
```
