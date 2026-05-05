
A limitation of this approach is that neither of the references used for `SingleR` or `CellAssign` considered tumor cells.
However, providing consensus labels saves users time and effort and allows them to focus on cell types that are likely to be poorly assigned [@doi:10.1038/s41588-024-01993-3] using our approach, such as tumor cells.

To address the limitations of consensus cell type assignment, we provide CNV estimates from `InferCNV` for approximately half of the libraries in the Portal.
Joint information from consensus cell type annotations and CNV estimates may support researchers to identify and interrogate tumor cells, in particular for diagnoses where copy number alterations are common such as neuroblastoma (Figure {@fig:fig5}B-D) or osteosarcoma.



Beyond the automated and consensus cell type annotations, two projects (`SCPCP000004` comprised of neuroblastoma samples, and `SCPCP000015` comprised of Ewing sarcoma samples) include an additional set of cell type annotations from the ongoing OpenScPCA project [@url:https://openscpca.readthedocs.io].
Unlike annotations made within the `scpca-nf` pipeline, these labels include formal identification of normal vs. tumor cells.
All of the annotation methods used in OpenScPCA are all fully open-source, enabling transparency, reproducibility, and reuse by the research community.
Moving forward, we will continue to expand the set of projects on the Portal with cell type annotations from the OpenScPCA project, further enriching the Portal with high-quality, well-documented annotations that support scientific discovery.


Also no integration but actually this is a good thing.

we also don't have every modality but out Nextflow modular workflow will allow us to add some. 