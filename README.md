<h1> <a href="https://mydennislab.github.io/2025-CHM13v2-SDs/" target="_blank" style="display:inline-block; padding: 14px 28px; background: linear-gradient(135deg, #4f46e5, #3b82f6); color: #fff; font-size: 16px; font-weight: 600; text-decoration: none; border-radius: 12px; box-shadow: 0 4px 14px rgba(0,0,0,0.2); transition: transform 0.2s ease-in-out; cursor: pointer;">
  🚀 Launch the Interactive Dashboard
</a> </h1>


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
