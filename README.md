# [CLICK HERE TO VISUALIZE](https://cosmograph.app/run/?data=https://gist.githubusercontent.com/mr-eyes/4adf803fdc1200c99580a5c23b6fba3c/raw/1d81a2f0d012c2f2ed516fd18dcb4382dc242eaa/edges_no_extra.tsv&source=source&target=target&gravity=0.46&repulsion=0.55&repulsionTheta=0.53&linkSpring=1.46&linkDistance=8&friction=0.97&renderLabels=true&renderHoveredLabel=true&renderLinks=true&curvedLinks=true&nodeSizeScale=0.8&linkWidthScale=2&linkArrowsSizeScale=1&nodeSize=size-total%20links&nodeColor=color-total%20links&linkWidth=width-default&linkColor=color-default&meta=https://gist.githubusercontent.com/mr-eyes/4adf803fdc1200c99580a5c23b6fba3c/raw/1d81a2f0d012c2f2ed516fd18dcb4382dc242eaa/nodes_metadata.tsv)


## `nodes_metadata.tsv`

| Column | Description |
|--------|-------------|
| `id` | Unique node ID in the format `chr:start-end` |
| `gene_name` | Annotated gene name (or `unknown`) |
| `gene_biotype` | Biotype from GFF3 (e.g., `protein_coding`, `lncRNA`) |
| `Name` | Liftoff Name attribute (alternative name) |
| `source_gene_common_name` | Liftoff common name of the source gene |
| `source_length` | Length of the segment |
| `telomeric` | Whether node overlaps telomeric region (`True`/`False`) |
| `pericentromeric` | Whether node overlaps pericentromeric region |
| `acrocentric` | Whether node overlaps acrocentric region |
| `feature_start`, `feature_end` | Coordinates of overlapping Liftoff feature |
| `num_edges` | Number of edges (connections) this node has |
| `cc_size` | Size of the connected component the node belongs to |
| `component_id` | Unique ID of the connected component |
| `genes_in_cc` | All unique gene names in this component (semicolon-separated) |
| `num_genes` | Count of unique genes in component |
| `telomeric_frac_in_cc` | Fraction of nodes in the component that are telomeric |
| `pericentromeric_frac_in_cc` | Fraction of nodes in the component that are pericentromeric |
| `acrocentric_frac_in_cc` | Fraction of nodes in the component that are acrocentric |
| `overlap_frac` | Fractional overlap between node region and gene feature |

---

## `edges.tsv`

| Column | Description |
|--------|-------------|
| `source` | Source node ID |
| `target` | Target node ID |
| `abs_length_diff` | Absolute difference in length between source and target |
| `src_component_id` | Component ID from source node |

---

### `connected_components_summary.tsv`

| Column | Description |
|--------|-------------|
| `component_id` | Unique serial ID of connected component |
| `num_nodes` | Number of nodes in the component |
| `num_edges` | Number of internal edges (connections) |
| `unique_genes` | Unique gene names within the component (semicolon-separated) |
| `node_ids` | Node IDs in this component (semicolon-separated) |
| `frac_telomeric` | Fraction of nodes marked telomeric |
| `frac_pericentromeric` | Fraction of nodes marked pericentromeric |
| `frac_acrocentric` | Fraction of nodes marked acrocentric |
| `frac_any_category` | Fraction of nodes in any region category (telo/peri/acro) |
| `avg_num_edges` | Average number of connections per node |
| `max_num_edges` | Max connections any node has in this component |
| `density` | Graph density (how tightly connected the component is) |
| `avg_clustering` | Average clustering coefficient |
| `diameter` | Longest shortest path between any two nodes |
| `radius` | Minimum eccentricity among nodes |
| `is_tree` | Whether the component forms a tree (acyclic) |
| `is_bipartite` | Whether the component can be 2-colored (no odd cycles) |