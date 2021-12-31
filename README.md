### A Parallel Version of metaSearch function
---
#### 1./ How to parallelize metaSearch function in Maude:

- Generate states up to a depth, with state dupcation checked as well as state checking

- For each state at the depth, we conduct a search independently

#### 2./ How to use:

```
red in PARALLEL-META-SEARCH : p-metaSearch(<module>, <initState>, <goalState>, <condition>, <type>, <depth>, <#workers>)
```
`<module>`, `<initState>`, `<goalState>`, `<condition>`, `<type>` are the same arguments in `metaSearch` function

`<depth>` is the depth described above

`<#workers>` is the number of workers used

`Note that:` to make the best use of parallelization, the specification should avoid long lasso loops.
