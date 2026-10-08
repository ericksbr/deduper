# Grouper

Grouper groups similar public comments based on **word overlap** (not topic). It finds comments with shared wording, even if they're not identical. Upload a CSV, Excel, or Parquet file, run the notebook in Google Colab, and download your file with each comment labeled by grouping status and similarity level.

## Labels
- **Ungrouped**: no other comment is similar enough
- **Grouped - Identical**: exactly matches another comment after normalization
- **Grouped - Highly similar**: best match in group has Jaccard ≥ 0.90
- **Grouped - Moderately similar**: best match in group has Jaccard in (0.50, 0.90)

## Note
Similarity is based on *word-level 5-gram shingles* (word overlap), not semantic topic similarity. Two comments discussing the same topic in different words may not group together.
