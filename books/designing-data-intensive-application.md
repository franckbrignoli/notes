# Designing Data-Intensive Application

### Storage and Retrieval

* Hash Indexes
  * In memory index pointing to a file offset
  * Data file segment compacted \(merged\)
* SSTables and LSM-Trees
  * \(Sorted String Tables\)
  * Keys are sorted in the segments
  * Allowing to use a merge sort algorithmn
* B-Tree index

