# FOUNDIN-PD Aim 1C: Multi-omic Sequencing of CRISPR-Edited iPSC-derived Dopaminergic Neuron Cell Lines 
## Sample Overview
21 samples from 10 PPMI participants of IPSC-derived dopaminergic neuron cell lines were sequenced with 10X Genomics Multiome Single-Cell ATAC + Gene Expression assay across two batches.

Three samples (Sample_3, Sample_8, and Sample_21) are replicates of PPMI3966 Clone 107, a control participant with no known PD mutation (i.e. SNCA, GBA, and LRRK2). The other 18 samples are obtained from nine unique participants with a known PD mutation, where one sample is sequenced as is and the other is CRISPR-edited to revert the PD mutation to wildtype (i.e. isoSNCA, isoGBA, and isoLRRK2). A sample metadata file has been uploaded to the GitHub.

## Data Overview
RNA+ATAC sequencing data were analyzed using Cell Ranger ARC v2.0.2. 

## File Structure
```bash
FOUNDIN_Suppl
├── processed
│   ├── analysis
│   │   └── PPMI*
│   │       ├── feature_linkage
│   │       │   ├── feature_linkage.bedpe
│   │       │   └── feature_linkage_matrix.h5
│   │       └── tf_analysis
│   │           ├── filtered_tf_bc_matrix
│   │           │   ├── barcodes.tsv.gz
│   │           │   ├── matrix.mtx.gz
│   │           │   └── motifs.tsv
│   │           ├── filtered_tf_bc_matrix.h5
│   │           └── peak_motif_mapping.bed
│   ├── SCAT
│   │   ├── ATAC_aim1c.rds
│   │   └── PPMI*
│   │       └── cellranger_outs
│   │           ├── analysis
│   │           │   ├── clustering
│   │           │   │   ├── graphclust
│   │           │   │   │   ├── clusters.csv
│   │           │   │   │   ├── differential_accessibility.csv
│   │           │   │   │   └── differential_expression.csv
│   │           │   │   ├── kmeans_2_clusters
│   │           │   │   │   ├── clusters.csv
│   │           │   │   │   ├── differential_accessibility.csv
│   │           │   │   │   └── differential_expression.csv
│   │           │   │   ├── kmeans_3_clusters
│   │           │   │   │   ├── clusters.csv
│   │           │   │   │   ├── differential_accessibility.csv
│   │           │   │   │   └── differential_expression.csv
│   │           │   │   ├── kmeans_4_clusters
│   │           │   │   │   ├── clusters.csv
│   │           │   │   │   ├── differential_accessibility.csv
│   │           │   │   │   └── differential_expression.csv
│   │           │   │   └── kmeans_5_clusters
│   │           │   │       ├── clusters.csv
│   │           │   │       ├── differential_accessibility.csv
│   │           │   │       └── differential_expression.csv
│   │           │   └── dimensionality_reduction
│   │           │       ├── lsa
│   │           │       │   ├── lsa_components.csv
│   │           │       │   ├── lsa_dispersion.csv
│   │           │       │   ├── lsa_features_selected.csv
│   │           │       │   ├── lsa_projection.csv
│   │           │       │   └── lsa_variance.csv
│   │           │       ├── tsne
│   │           │       │   └── tsne_projection.csv
│   │           │       └── umap
│   │           │           └── umap_projection.csv
│   │           ├── atac_cut_sites.bigwig
│   │           ├── atac_fragments.tsv.gz
│   │           ├── atac_fragments.tsv.gz.tbi
│   │           ├── atac_peak_annotation.tsv
│   │           ├── atac_peaks.bed
│   │           ├── atac_possorted_bam.bam
│   │           ├── atac_possorted_bam.bam.bai
│   │           ├── per_barcode_metrics.csv
│   │           ├── cloupe.cloupe
│   │           ├── summary.csv
│   │           └── web_summary.html
│   └── SCRN
│       ├── GEX_aim1c.rds
│       └── PPMI*
│           └── cellranger_outs
│               ├── analysis
│               │   ├── clustering
│               │   │   ├── graphclust
│               │   │   │   ├── clusters.csv
│               │   │   │   ├── differential_accessibility.csv
│               │   │   │   └── differential_expression.csv
│               │   │   ├── kmeans_2_clusters
│               │   │   │   ├── clusters.csv
│               │   │   │   ├── differential_accessibility.csv
│               │   │   │   └── differential_expression.csv
│               │   │   ├── kmeans_3_clusters
│               │   │   │   ├── clusters.csv
│               │   │   │   ├── differential_accessibility.csv
│               │   │   │   └── differential_expression.csv
│               │   │   ├── kmeans_4_clusters
│               │   │   │   ├── clusters.csv
│               │   │   │   ├── differential_accessibility.csv
│               │   │   │   └── differential_expression.csv
│               │   │   └── kmeans_5_clusters
│               │   │       ├── clusters.csv
│               │   │       ├── differential_accessibility.csv
│               │   │       └── differential_expression.csv
│               │   └── dimensionality_reduction
│               │       ├── pca
│               │       │   ├── pca_components.csv
│               │       │   ├── pca_dispersion.csv
│               │       │   ├── pca_features_selected.csv
│               │       │   ├── pca_projection.csv
│               │       │   └── pca_variance.csv
│               │       ├── tsne
│               │       │   └── tsne_projection.csv
│               │       └── umap
│               ├── filtered_feature_bc_matrix
│               │   ├── barcodes.tsv.gz
│               │   ├── features.tsv.gz
│               │   └── matrix.mtx.gz
│               ├── filtered_feature_bc_matrix.h5
│               ├── gex_molecule_info.h5
│               ├── gex_possorted_bam.bam
│               ├── gex_possorted_bam.bam.bai
│               ├── per_barcode_metrics.csv
│               ├── raw_feature_bc_matrix
│               │   ├── barcodes.tsv.gz
│               │   ├── features.tsv.gz
│               │   └── matrix.mtx.gz
│               ├── raw_feature_bc_matrix.h5
│               ├── cloupe.cloupe
│               ├── summary.csv
│               └── web_summary.html
└── raw
    └── ASSAYS
        ├── SCAT
        │   ├── *_I1_001.fastq.gz
        │   ├── *_R1_001.fastq.gz
        │   ├── *_R2_001.fastq.gz
        │   ├── *_R3_001.fastq.gz
        └── SCRN
            ├── *_I1_001.fastq.gz
            ├── *_I2_001.fastq.gz
            ├── *_R1_001.fastq.gz
            └── *_R2_001.fastq.gz
 ```

