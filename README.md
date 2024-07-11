# BeerMicrobiomeMetaAnalysis

## Meta-Analysis and Visualization of Beer Microbiome Data

### Dataset

- **Beer Microbiome Data**: [Google Sheets Dataset](https://docs.google.com/spreadsheets/d/1RblHxOcXIFd2tg4P7cHtZNuElin5ifOHt_0KawkYU7A/edit?gid=0#gid=0)

### Steps

#### 1. MGnify Workflow Complete

- **Workflow Link**: [MGnify's Amplicon Pipeline Complete](https://usegalaxy.eu/u/marabesemer/w/mgnifys-amplicon-pipeline-complete)
- **Inputs**:
  - **SRA Accession List**: Text file listing accession IDs (from the Beer dataset).
  - **Clan Information File**: [ribo.claninfo file](https://github.com/MaraBesemer/BeerMicrobiomeMetaAnalysis/blob/main/ribo.claninfo.txt)
  - **Covariance Models**: [ribo.cm file](https://github.com/MaraBesemer/BeerMicrobiomeMetaAnalysis/blob/main/ribo.cm)
- **Workflow History**: [History with Beer Dataset](https://usegalaxy.eu/u/marabesemer/h/mgnify-complete-dataset-1)

#### 2. MGnify Workflow After Quality Control

- **Workflow Link**: [MGnify's Amplicon Pipeline - After Quality Control](https://usegalaxy.eu/u/marabesemer/w/mgnifys-amplicon-pipeline---after-quality-control)
- **Inputs**:
  - **Processed Sequences**
  - **Clan Information File**: [ribo.claninfo file](https://github.com/MaraBesemer/BeerMicrobiomeMetaAnalysis/blob/main/ribo.claninfo.txt)
  - **Covariance Models**: [ribo.cm file](https://github.com/MaraBesemer/BeerMicrobiomeMetaAnalysis/blob/main/ribo.cm)
- **Workflow History**: [History with Beer Dataset](https://usegalaxy.eu/u/marabesemer/h/after-quality-control-complete-dataset)

#### 3. mapseqToAmpviz and AmpvizLoad Workflow

- **Workflow Link**: [mapseqToAmpviz and AmpvizLoad Workflow](https://usegalaxy.eu/u/marabesemer/w/copy-of-mapseqtoampvis-and-appvisload-1)
- **Inputs**:
  - **mapseq Outputs**: Each output (OTU_SSU_SILVA, OTU_LSU_SILVA, etc.) from the MGnify workflow
  - **Metadata**: Corresponding metadata for the dataset used
- **Workflow Histories**:
  - [OTU_SSU_SILVA Input](https://usegalaxy.eu/u/marabesemer/h/mapseqtoampviz-and-ampvizload-v2)
  - [OTU_LSU_SILVA Input](https://usegalaxy.eu/u/marabesemer/h/mapseqtoampviz-and-ampvizload-lsu)
  - [OTU_ITS_UNITE Input](https://usegalaxy.eu/u/marabesemer/h/mapseq-to-ampvis-its-unite)
  - [OTU_ITSoneDB Input](https://usegalaxy.eu/u/marabesemer/h/mapseq-to-ampvis-itsonedb)
