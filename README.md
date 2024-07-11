# BeerMicrobiomeMetaAnalysis

## Meta-Analysis and Visualization of Beer Microbiome Data

### Dataset

- **Beer Microbiome Data**: [Google Sheets Dataset](https://docs.google.com/spreadsheets/d/1RblHxOcXIFd2tg4P7cHtZNuElin5ifOHt_0KawkYU7A/edit?gid=0#gid=0)

### Steps

#### 1. MGnify Workflow Complete

- **Workflow Link**: [MGnify's Amplicon Pipeline Complete](https://usegalaxy.eu/u/marabesemer/w/mgnifys-amplicon-pipeline-complete)
- **Inputs**:
  - **SRA Accession List**: [listing accession IDs](https://github.com/MaraBesemer/BeerMicrobiomeMetaAnalysis/blob/main/input_tabular.txt)
  - **Clan Information File**: [ribo.claninfo file](https://github.com/MaraBesemer/BeerMicrobiomeMetaAnalysis/blob/main/ribo.claninfo.txt)
  - **Covariance Models**: [ribo.cm file](https://github.com/MaraBesemer/BeerMicrobiomeMetaAnalysis/blob/main/ribo.cm)
- **Workflow History**: [History with Beer Dataset](https://usegalaxy.eu/u/marabesemer/h/mgnify-complete-dataset-1)

#### 2. MGnify Workflow After Quality Control
*(This workflow is not necessary and was only used because the complete workflow failed at the end. I didn't want to run the whole workflow again.)*

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
  - **Metadata**: [Metadata Beer](https://github.com/MaraBesemer/BeerMicrobiomeMetaAnalysis/blob/main/Metadata-formatted.txt)
- **Workflow Histories**:
  - [OTU_SSU_SILVA Input](https://usegalaxy.eu/u/marabesemer/h/mapseqtoampviz-and-ampvizload-v2)
  - [OTU_LSU_SILVA Input](https://usegalaxy.eu/u/marabesemer/h/mapseqtoampviz-and-ampvizload-lsu)
  - [OTU_ITS_UNITE Input](https://usegalaxy.eu/u/marabesemer/h/mapseq-to-ampvis-its-unite)
  - [OTU_ITSoneDB Input](https://usegalaxy.eu/u/marabesemer/h/mapseq-to-ampvis-itsonedb)

After the data preperation, the ampviz2 ready data can be processed with ampviz2 tools. I used the [apviz2 heatmap tool](https://usegalaxy.eu/?tool_id=toolshed.g2.bx.psu.edu%2Frepos%2Fiuc%2Fampvis2_heatmap%2Fampvis2_heatmap%2F2.8.6%2Bgalaxy1&version=latest) to create heatmaps to show the data more clearly.

### Data Visualization with Ampvis2

#### Preparing the Ampvis2 Ready Data

After completing the data preparation workflows, the processed data can be visualized using Ampvis2 tools. Here's how to proceed:

#### Generating Heatmaps with Ampvis2

1. **Input Data**:
   - **Ampvis2 RDS Dataset**: This is the output from the mapseqToAmpviz and AmpvizLoad workflow.
   - **Metadata List (Optional)**: The metadata list output from the mapseqToAmpviz and AmpvizLoad workflow.

2. **Creating a Heatmap**:
   - **Tool**: [Ampvis2 Heatmap Tool](https://usegalaxy.eu/?tool_id=toolshed.g2.bx.psu.edu%2Frepos%2Fiuc%2Fampvis2_heatmap%2Fampvis2_heatmap%2F2.8.6%2Bgalaxy1&version=latest)
   - **Inputs**:
     - **Ampvis2 RDS Dataset**: Select the Ampvis2 RDS dataset output.
     - **Metadata List (Optional)**: Input the metadata list if available.
     - **Taxonomic Level**: Choose the desired taxonomic level to aggregate the OTUs.
     - **Grouping and Faceting**: You can group and facet the samples based on values from the metadata list (if provided).

#### Example Output

For example, using the OTU_ITS_UNITE input aggregated at the species level and grouped by beer type, the resulting heatmap provides a clear visualization of the data. 

Sample output can be seen here:
[Galaxy1742-[ampvis2_heatmap_on_data_1394_and_data_1393].pdf](https://github.com/user-attachments/files/16174758/Galaxy1742-.ampvis2_heatmap_on_data_1394_and_data_1393.pdf)

By following these steps, you can generate informative heatmaps to visualize the microbiome data from beer samples effectively.


