# [CLICK HERE TO VISUALIZE](https://cosmograph.app/run/?data=https://gist.githubusercontent.com/mr-eyes/4adf803fdc1200c99580a5c23b6fba3c/raw/1d81a2f0d012c2f2ed516fd18dcb4382dc242eaa/edges_no_extra.tsv&source=source&target=target&gravity=0.46&repulsion=0.55&repulsionTheta=0.53&linkSpring=1.46&linkDistance=8&friction=0.97&renderLabels=true&renderHoveredLabel=true&renderLinks=true&curvedLinks=true&nodeSizeScale=0.8&linkWidthScale=2&linkArrowsSizeScale=1&nodeSize=size-total%20links&nodeColor=color-total%20links&linkWidth=width-default&linkColor=color-default&meta=https://gist.githubusercontent.com/mr-eyes/4adf803fdc1200c99580a5c23b6fba3c/raw/1d81a2f0d012c2f2ed516fd18dcb4382dc242eaa/nodes_metadata.tsv)

## `node_metadata.tsv`

A table with one row per **unique genomic region** (node) involved in a structural duplication.

| Column | Description |
|--------|-------------|
| `id` | Unique ID for the genomic region (`chr:start-end`) |
| `gene_name` | Ensembl or Liftoff-assigned gene name overlapping this region (if any) |
| `gene_biotype` | Gene biotype (e.g., lncRNA, protein_coding) |
| `Name` | Short name from Liftoff GFF3 `Name` attribute |
| `source_gene_common_name` | Common name for the gene |
| `source_length` | Length of the region in bp |
| `telomeric` | Boolean: Is this region telomeric? |
| `pericentromeric` | Boolean: Is this region pericentromeric? |
| `acrocentric` | Boolean: Is this region acrocentric? |
| `feature_start` | Start of overlapping gene/transcript feature |
| `feature_end` | End of overlapping gene/transcript feature |
| `num_edges` | Number of duplications (edges) this region is involved in |
| `cc_size` | Number of nodes in the connected component |
| `component_id` | Unique identifier for the connected component |
| `genes_in_cc` | Semicolon-separated list of all gene names in the component |
| `num_genes` | Count of unique genes in the component |
| `telomeric_frac_in_cc` | % of nodes in the component that are telomeric |
| `pericentromeric_frac_in_cc` | % pericentromeric |
| `acrocentric_frac_in_cc` | % acrocentric |
| `overlap_frac` | Fraction of the region that overlaps the feature from annotation (e.g. gene body) |

---

## `edges.tsv`

| Column | Description |
|--------|-------------|
| `source` | ID of the first region in the duplication pair |
| `target` | ID of the second region |
| `abs_length_diff` | Absolute difference in length between the two regions |
| `src_component_id` | Component ID assigned based on the source node |
