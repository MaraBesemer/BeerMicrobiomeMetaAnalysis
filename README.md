# BeerMicrobiomeMetaAnalysis
Meta-Analysis and Visualization of Beer Microbiome Data

- Dataset (Beer): https://docs.google.com/spreadsheets/d/1RblHxOcXIFd2tg4P7cHtZNuElin5ifOHt_0KawkYU7A/edit?gid=0#gid=0 

Steps:
1.  MGnify workflow complete: https://usegalaxy.eu/u/marabesemer/w/mgnifys-amplicon-pipeline-complete
  
   Inputs:
  SRA accession list: txt file where accession ids are listet below each other (in my case the accession from the dataset (Beer))  
  Clan information file: robi.claninfo file (https://github.com/MaraBesemer/BeerMicrobiomeMetaAnalysis/blob/main/ribo.claninfo.txt)  
  Covariance models: ribo.cm file (https://github.com/MaraBesemer/BeerMicrobiomeMetaAnalysis/blob/main/ribo.cm)
  
  History of MGnify workflow complete with beer dataset: https://usegalaxy.eu/u/marabesemer/h/mgnify-complete-dataset-1  


2. MGnify workflow after quality control (if complete workflow failed, to not run the coplete workflow again I only ran the after quality workflow with the merged results): https://usegalaxy.eu/u/marabesemer/w/mgnifys-amplicon-pipeline---after-quality-control
     
   Inputs:
   Processed sequences:  
   Clan information file: robi.claninfo file   
   Covariance models: ribo.cm file
   
   History with beer dataset: https://usegalaxy.eu/u/marabesemer/h/after-quality-control-complete-dataset
  

3. mapseqToAmpviz and AmpvizLoad worfklow: https://usegalaxy.eu/u/marabesemer/w/copy-of-mapseqtoampvis-and-appvisload-1
     
   Inputs:
   mapseq outputs: each output (otu_SSU_SILVA, OTU_LSU_SILVA...) from the MGnify workflow
   Metadata: corresponding metadata to the dataset which is used (link)
     
  History with OTU_SSU_SILVA input: https://usegalaxy.eu/u/marabesemer/h/mapseqtoampviz-and-ampvizload-v2  
  History with OTU_LSU_SILVA input: https://usegalaxy.eu/u/marabesemer/h/mapseqtoampviz-and-ampvizload-lsu  
  History with OTU_ITS_UNITE input: https://usegalaxy.eu/u/marabesemer/h/mapseq-to-ampvis-its-unite     
  History with OTU_ITSoneDB input: https://usegalaxy.eu/u/marabesemer/h/mapseq-to-ampvis-itsonedb   
  
