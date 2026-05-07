---
title: 'The Single-cell Pediatric Cancer Atlas: Data portal and open-source tools for single-cell transcriptomics of pediatric tumors'
keywords:
- single-cell RNA-seq
- single-nuclei RNA-seq
- pediatric cancer
- resource
- Nextflow
- open science
- reproducibility
lang: en-US
date-meta: '2026-05-07'
author-meta:
- Allegra G. Hawkins
- Joshua A. Shapiro
- Stephanie J. Spielman
- David S. Mejia
- Deepashree Venkatesh Prasad
- Nozomi Ichihara
- Arkadii Yakovets
- Avrohom M. Gottlieb
- Kurt G. Wheeler
- Chante J. Bethell
- Steven M. Foltz
- Jennifer O'Malley
- Casey S. Greene
- Jaclyn N. Taroni
header-includes: |
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta property="og:type" content="article" />
  <meta name="dc.title" content="The Single-cell Pediatric Cancer Atlas: Data portal and open-source tools for single-cell transcriptomics of pediatric tumors" />
  <meta name="citation_title" content="The Single-cell Pediatric Cancer Atlas: Data portal and open-source tools for single-cell transcriptomics of pediatric tumors" />
  <meta property="og:title" content="The Single-cell Pediatric Cancer Atlas: Data portal and open-source tools for single-cell transcriptomics of pediatric tumors" />
  <meta property="twitter:title" content="The Single-cell Pediatric Cancer Atlas: Data portal and open-source tools for single-cell transcriptomics of pediatric tumors" />
  <meta name="dc.date" content="2026-05-07" />
  <meta name="citation_publication_date" content="2026-05-07" />
  <meta property="article:published_time" content="2026-05-07" />
  <meta name="dc.modified" content="2026-05-07T18:36:03+00:00" />
  <meta property="article:modified_time" content="2026-05-07T18:36:03+00:00" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Allegra G. Hawkins" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author_orcid" content="0000-0001-6026-3660" />
  <meta name="citation_author" content="Joshua A. Shapiro" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author_orcid" content="0000-0002-6224-0347" />
  <meta name="citation_author" content="Stephanie J. Spielman" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author_orcid" content="0000-0002-9090-4788" />
  <meta name="citation_author" content="David S. Mejia" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author_orcid" content="0000-0003-1679-0353" />
  <meta name="citation_author" content="Deepashree Venkatesh Prasad" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author_orcid" content="0000-0001-5756-4083" />
  <meta name="citation_author" content="Nozomi Ichihara" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author" content="Arkadii Yakovets" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author" content="Avrohom M. Gottlieb" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author" content="Kurt G. Wheeler" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author" content="Chante J. Bethell" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author_institution" content="The University of Texas MD Anderson Cancer Center, UTHealth Houston Graduate School of Biomedical Sciences, Houston, TX, 77030, USA" />
  <meta name="citation_author_orcid" content="0000-0001-9653-8128" />
  <meta name="citation_author" content="Steven M. Foltz" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author_institution" content="Translational Research, Multiple Myeloma Research Foundation, Norwalk, CT, 06851, USA" />
  <meta name="citation_author_orcid" content="0000-0002-9526-8194" />
  <meta name="citation_author" content="Jennifer O&#39;Malley" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author" content="Casey S. Greene" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author_institution" content="Center for Health AI, University of Colorado School of Medicine, Aurora, CO, 80045, USA" />
  <meta name="citation_author_institution" content="Department of Biomedical Informatics, University of Colorado School of Medicine, Aurora, CO, 80045, USA" />
  <meta name="citation_author_orcid" content="0000-0001-8713-9213" />
  <meta name="citation_author" content="Jaclyn N. Taroni" />
  <meta name="citation_author_institution" content="Childhood Cancer Data Lab, Alex&#39;s Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA" />
  <meta name="citation_author_orcid" content="0000-0003-4734-4508" />
  <link rel="canonical" href="https://AlexsLemonade.github.io/ScPCA-manuscript/" />
  <meta property="og:url" content="https://AlexsLemonade.github.io/ScPCA-manuscript/" />
  <meta property="twitter:url" content="https://AlexsLemonade.github.io/ScPCA-manuscript/" />
  <meta name="citation_fulltext_html_url" content="https://AlexsLemonade.github.io/ScPCA-manuscript/" />
  <meta name="citation_pdf_url" content="https://AlexsLemonade.github.io/ScPCA-manuscript/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://AlexsLemonade.github.io/ScPCA-manuscript/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://AlexsLemonade.github.io/ScPCA-manuscript/v/2662f4594f6a388de83ae8f04049fbf05601a279/" />
  <meta name="manubot_html_url_versioned" content="https://AlexsLemonade.github.io/ScPCA-manuscript/v/2662f4594f6a388de83ae8f04049fbf05601a279/" />
  <meta name="manubot_pdf_url_versioned" content="https://AlexsLemonade.github.io/ScPCA-manuscript/v/2662f4594f6a388de83ae8f04049fbf05601a279/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://AlexsLemonade.github.io/ScPCA-manuscript/v/2662f4594f6a388de83ae8f04049fbf05601a279/))
was automatically generated
from [AlexsLemonade/ScPCA-manuscript@2662f45](https://github.com/AlexsLemonade/ScPCA-manuscript/tree/2662f4594f6a388de83ae8f04049fbf05601a279)
on May 7, 2026.
</em></small>



## Authors



+ **Allegra G. Hawkins**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0001-6026-3660](https://orcid.org/0000-0001-6026-3660)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [allyhawkins](https://github.com/allyhawkins)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>

+ **Joshua A. Shapiro**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0002-6224-0347](https://orcid.org/0000-0002-6224-0347)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [jashapiro](https://github.com/jashapiro)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>

+ **Stephanie J. Spielman**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0002-9090-4788](https://orcid.org/0000-0002-9090-4788)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [sjspielman](https://github.com/sjspielman)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>

+ **David S. Mejia**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0003-1679-0353](https://orcid.org/0000-0003-1679-0353)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [davidsmejia](https://github.com/davidsmejia)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>

+ **Deepashree Venkatesh Prasad**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0001-5756-4083](https://orcid.org/0000-0001-5756-4083)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [dvenprasad](https://github.com/dvenprasad)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>

+ **Nozomi Ichihara**
  <br>
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [nozomione](https://github.com/nozomione)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>

+ **Arkadii Yakovets**
  <br>
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [arkid15r](https://github.com/arkid15r)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>

+ **Avrohom M. Gottlieb**
  <br>
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [avrohomgottlieb](https://github.com/avrohomgottlieb)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>

+ **Kurt G. Wheeler**
  <br>
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [kurtwheeler](https://github.com/kurtwheeler)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>

+ **Chante J. Bethell**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0001-9653-8128](https://orcid.org/0000-0001-9653-8128)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [cbethell](https://github.com/cbethell)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA; The University of Texas MD Anderson Cancer Center, UTHealth Houston Graduate School of Biomedical Sciences, Houston, TX, 77030, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>

+ **Steven M. Foltz**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0002-9526-8194](https://orcid.org/0000-0002-9526-8194)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [envest](https://github.com/envest)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA; Translational Research, Multiple Myeloma Research Foundation, Norwalk, CT, 06851, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>

+ **Jennifer O'Malley**
  <br>
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [Jen-OMalley](https://github.com/Jen-OMalley)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>

+ **Casey S. Greene**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0001-8713-9213](https://orcid.org/0000-0001-8713-9213)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [cgreene](https://github.com/cgreene)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA; Center for Health AI, University of Colorado School of Medicine, Aurora, CO, 80045, USA; Department of Biomedical Informatics, University of Colorado School of Medicine, Aurora, CO, 80045, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>

+ **Jaclyn N. Taroni**
  ^[✉](#correspondence)^<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0003-4734-4508](https://orcid.org/0000-0003-4734-4508)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [jaclyn-taroni](https://github.com/jaclyn-taroni)
    <br>
  <small>
     Childhood Cancer Data Lab, Alex's Lemonade Stand Foundation, Bala Cynwyd, PA, 19004, USA
     · Funded by Alex's Lemonade Stand Foundation Childhood Cancer Data Lab (CCDL)
  </small>


::: {#correspondence}
✉ — Correspondence possible via [GitHub Issues](https://github.com/AlexsLemonade/ScPCA-manuscript/issues)
or email to
Jaclyn N. Taroni \<jaclyn.taroni@ccdatalab.org\>.


:::


## Abstract {.page_break_before}

The Single-cell Pediatric Cancer Atlas (ScPCA) Portal (<https://scpca.alexslemonade.org/>) is a data resource for uniformly processed single-cell and single-nuclei RNA sequencing (RNA-seq) data and de-identified metadata from pediatric tumor samples.
Originally comprised of data from 10 projects funded by Alex’s Lemonade Stand Foundation (ALSF), the Portal currently contains summarized gene expression data for over 700 samples across 55 cancer types from ALSF-funded and community-contributed datasets.
Downloads include gene expression data as `SingleCellExperiment` or `AnnData` objects containing raw and normalized counts, PCA and UMAP coordinates, automated cell type annotations, and copy-number variation estimates, along with summary reports.
Some samples have additional data from bulk RNA-seq, spatial transcriptomics, and/or feature barcoding (e.g., CITE-seq and cell hashing) included in the download.
All data on the Portal were uniformly processed using `scpca-nf`, an efficient and open-source Nextflow workflow that uses `alevin-fry` to quantify gene expression.
Comprehensive documentation, including descriptions of file contents and a guide to getting started, is available at <https://scpca.readthedocs.io>.


## Introduction

The number of studies employing single-cell RNA-seq (scRNA-seq) has grown rapidly since this technology was introduced [@doi:10.1038/nprot.2017.149].
Unlike its predecessor bulk RNA-seq, which averages expression profiles of all cells within a sample, single-cell technology quantifies gene expression in individual cells.
Tumors are transcriptionally heterogeneous, highlighting the importance of using scRNA-seq in studying tumor samples [@doi:10.1101/gr.190595.115].
Researchers can use scRNA-seq data from patient tumor samples to analyze and identify individual cell populations that may influence tumor growth, resistance, and metastasis [@doi:10.1126/science.1254257], as well as how tumor cells interact with normal cells in the tumor microenvironment [@10.1038/s41588-022-01141-9].

As the number of scRNA-seq datasets expands, efforts have emerged to create centralized data resources.
For example, CELLxGENE [@doi:10.1101/2021.04.05.438318; @doi:10.1101/2023.10.30.563174] offers gene expression data from samples spanning hundreds of cell types in standardized analysis formats.
Other resources such the Human Cell Atlas (HCA) and Human Tumor Atlas Network (HTAN) offer harmonized data, enabling reliable cross-sample comparisons and discovery across diverse biological contexts and disease types.
The HCA, which provides a comprehensive map of all cell types in the human body using single-cell genomics, contains uniformly processed scRNA-seq data obtained from normal tissue with few samples derived from diseased tissue [@doi:10.7554/eLife.27041].
The HTAN also hosts a collection of genomic data from tumors across multiple cancer types, including scRNA-seq [@doi:10.1016/j.cell.2020.03.053].

Despite these resources, there have been considerably fewer efforts to harmonize and distribute data specifically from pediatric tumors.
As pediatric cancer is much less common than adult cancer, there are fewer available pediatric tumor than adult tumor samples, [@url:https://www.cancer.gov/types/childhood-cancers/child-adolescent-cancers-fact-sheet#how-do-cancers-in-adolescents-and-young-adults-differ-from-those-in-younger-children] and access to data from pediatric tumors is often limited.
Recently, Xu and colleagues highlighted lack of standardization of pediatric cancer single-cell data as a barrier to reuse in their attempt to create an atlas [@doi:10.1002/cti2.70033].
Thus, it is imperative to make harmonized data from pediatric tumors accessible to researchers [@doi:10.1186/s13040-018-0190-8].
To address this unmet need, Alex's Lemonade Stand Foundation (ALSF) and the Childhood Cancer Data Lab developed and maintain the Single-cell Pediatric Cancer Atlas (ScPCA) Portal (<https://scpca.alexslemonade.org/>), a data resource for single-cell and single-nuclei RNA-seq data of pediatric tumor samples.

The ScPCA Portal holds uniformly processed summarized gene expression from 10x Genomics droplet-based single-cell and single-nuclei RNA-seq for over 700 samples from a diverse set of 55 types of pediatric cancers.
Originally comprised of data from 10 projects funded by ALSF, the Portal has since expanded to include data contributed by pediatric cancer research community members.
The Portal additionally includes data obtained from bulk RNA-seq, spatial transcriptomics, and feature barcoding methods such as CITE-seq and cell hashing.
All data on the Portal are available in formats ready for downstream analysis with common workflow ecosystems, including `SingleCellExperiment` objects used by `R/Bioconductor`[@doi:10.1038/s41592-019-0654-x] or `AnnData` objects used by `Scanpy` and related Python modules [@doi:10.1186/s13059-017-1382-0].
Downloaded objects contain both raw and normalized gene expression counts, dimensionality reduction results, cell type annotations, and copy-number variation estimates.
As of May 2026, over 950 unique downloaders had accessed the Portal since its launch.

To ensure uniform processing of all current and future Portal data, we created `scpca-nf`, an open-source Nextflow [@doi:10.1038/nbt.3820] pipeline (<https://github.com/AlexsLemonade/scpca-nf>).
This pipeline increases transparency and facilitates analyses across multiple samples and projects without re-processing.
The `scpca-nf` workflow uses `alevin-fry` [@doi:10.1038/s41592-022-01408-3] for fast and efficient quantification of single-cell gene expression for all samples on the Portal, including scRNA-seq data and any associated CITE-seq or cell hash data.
The `scpca-nf` pipeline is also a resource, allowing researchers to process their own samples for comparison to Portal data and or for submission to the Portal.

Here, we present the Single-cell Pediatric Cancer Atlas as a freely-available resource for all pediatric cancer researchers.
The ScPCA Portal provides downloads ready for immediate use, allowing researchers to skip time-consuming data re-processing and wrangling steps.
We provide comprehensive documentation about data processing and the contents of the Portal, including a guide to getting started working with an ScPCA dataset (<https://scpca.readthedocs.io/>).
The ScPCA Portal advances pediatric cancer research by accelerating researchers' ability to answer important biological questions.


## Results

### The Single-cell Pediatric Cancer Atlas Portal

In March 2022, the Childhood Cancer Data Lab launched the Single-cell Pediatric Cancer Atlas (ScPCA) Portal to make uniformly processed, summarized single-cell and single-nuclei RNA-seq data and de-identified metadata from pediatric tumor samples openly available for download by the research community.
Data on the Portal was obtained using two different mechanisms: raw data was accepted from ALSF-funded investigators and processed using our open-source pipeline `scpca-nf`, or investigators processed their raw data using `scpca-nf` and submitted the output for inclusion on the Portal.

All samples on the Portal include a core set of metadata obtained from investigators, including age, sex, diagnosis, subdiagnosis (if applicable), tissue location, and disease stage.
The majority of projects include additional metadata, such as treatment or tumor stage, if provided.
We standardized all provided metadata to maintain consistency across projects.
Where applicable, we include ontology term identifiers in addition to human-readable values.
We use ontology term identifiers obtained from HsapDv (age) [@url:https://www.ebi.ac.uk/ols4/ontologies/hsapdv], PATO (sex) [@doi:10.1093/bib/bbx035; @url:https://www.ebi.ac.uk/ols4/ontologies/pato], NCBI taxonomy (organism) [@doi:10.1093/database/baaa062; @url:https://www.ncbi.nlm.nih.gov/taxonomy], MONDO (disease) [@doi:10.1101/2022.04.13.22273750; @url:https://www.ebi.ac.uk/ols4/ontologies/mondo], UBERON (tissue) [@doi:10.1186/2041-1480-5-21; @doi:10.1186/gb-2012-13-1-r5; @url:https://www.ebi.ac.uk/ols4/ontologies/uberon], and Hancestro (ethnicity, if applicable) [@doi:10.1186/s13059-018-1396-2; @url:https://www.ebi.ac.uk/ols4/ontologies/hancestro].
These ontology term identifiers standardize metadata terms and facilitate comparisons across Portal datasets and other research projects.

The Portal contains data from over 700 samples and 55 tumor types [@doi:10.1016/j.devcel.2022.04.003; @doi:10.21203/rs.3.rs-2517703/v1; @doi:10.21203/rs.3.rs-2517758/v1; @doi:10.1038/nature23647; @doi:10.1038/s41467-021-24781-7; @doi:10.1093/neuonc/noad207; @doi:10.1101/2023.12.26.573390].
<!-- `TODO`: Update numbers -->
Figure {@fig:fig1}A summarizes all samples from patient tumors and patient-derived xenografts currently available on the Portal.
The most common sample diagnosis on the Portal is leukemia (n = 216), followed by from sarcoma and soft tissue tumors (n = 194), brain and central nervous system tumors (n = 167), and a variety of other solid tumors (n = 115).
Most samples were collected at initial diagnosis (n = 520), with a smaller number of samples collected at recurrence (n = 129), during progressive disease (n = 12), during or after treatment (n = 11), or post-mortem (n = 5).
The Portal also contains a small number of human tumor cell line samples (n = 6) and non-cancerous samples (n = 6).

Sample data includes summarized gene expression data from either single-cell or single-nuclei RNA sequencing with the 10x Genomics droplet-based platform.
Some samples also include additional data, such as CITE-seq quantification of cell-surface protein levels with antibody-derived tags (ADTs) [@doi:10.1038/nmeth.4380], or hashtag oligonucleotide (HTO) quantification for multiplexed samples [@doi:10.1186/s13059-018-1603-1].
Raw FASTQ files are not available for download from the Portal, but we provide links to raw data sources in external repositories, such as the Database of Genotypes and Phenotypes (dbGaP) [@doi:10.1038/ng1007-1181; @doi:10.1093/nar/gkt1211], when available.
95 samples have associated CITE-seq data, and 35 samples have associated multiplexing data.
In some cases, multiple libraries from the same sample were created for additional assays, either for bulk RNA-seq (n = 182) or spatial transcriptomics (n = 41).
<!-- Note context for these values: https://github.com/AlexsLemonade/ScPCA-manuscript/issues/245 -->
Seven samples in the Portal have only bulk RNA-seq or spatial transcriptomics data.
A summary of the number of single-cell or single-nuclei samples and their associated additional modalities is shown in Figure {@fig:fig1}B, and a detailed summary of the total samples with each sequencing method broken down by project is available in Table S1.

Samples on the Portal are organized by project, where each project is a collection of similar samples from an individual lab.
Users can filter projects based on diagnosis, included modalities (e.g., CITE-seq, bulk RNA-seq), 10x Genomics kit version (e.g., 10Xv2, 10Xv3), and whether a project includes samples from patient-derived xenografts or cell lines.
The project card displays an abstract, the total number of samples, a list of all present diagnoses, and links to any external information associated with the project, including publications and links to external resources, e.g., SRA or GEO (Figure {@fig:fig1}C).
The project card also indicates the sequencing metadata such as the 10x Genomics kit version, the suspension type (cell or nucleus), if additional sequencing like bulk RNA-seq is present, or if the samples were multiplexed using cell hashing.

The Portal also provides visualization of individual samples via the UCSC Cell Browser interface [@doi:10.1093/bioinformatics/btab503] as seen in Figure {@fig:fig1}C.
Interactive UMAPs allow users to explore the cells within each sample, coloring by cell type annotations, gene expression values, or other calculated metrics.

### Uniform processing of data available on the ScPCA Portal

We developed [`scpca-nf`](https://github.com/AlexsLemonade/scpca-nf), an open-source and efficient Nextflow [@doi:10.1038/nbt.3820] workflow for quantifying single-cell and single-nuclei RNA-seq data to process data for the Portal.
Nextflow is a workflow management system that facilitates multi-step and long-running bioinformatics processes in a portable and reproducible manner across computing environments, including high-performance computing clusters and cloud-based computing [@doi:10.1186/s13059-025-03673-9].
Nextflow allows seamless dependency management, as each workflow process is run using a specified container image.
This flexibility and containerization make the workflow easily portable for general use.
Setup requires only installing Nextflow and a supported container engine, managing a configuration file for the computing environment, and organizing input files.

When building `scpca-nf`, we sought a fast and memory-efficient tool for gene expression quantification to minimize processing costs with comparable performance to the widely-used Cell Ranger platform [@doi:10.1038/ncomms14049; @url:https://www.10xgenomics.com/support/software/cell-ranger/latest].
Our comparisons between `alevin-fry` [@doi:10.1038/s41592-022-01408-3] and Cell Ranger showed that `alevin-fry` had lower run time and memory usage (Figure {@fig:figS1}A) but retained comparable mean gene expression(Figure {@fig:figS1}B), total UMIs per cell (Figure {@fig:figS1}C), and total genes detected per cell (Figure {@fig:figS1}D).
We therefore used `salmon alevin` and `alevin-fry` [@doi:10.1038/s41592-022-01408-3] in `scpca-nf` to quantify gene expression data.

Taking FASTQ files as input, `scpca-nf` aligns reads using the selective alignment option in `salmon alevin` to an index with transcripts corresponding to spliced cDNA and intronic regions, known as the `splici` index in `alevin-fry` (Figure {@fig:fig2}A).
`alevin-fry` outputs a gene-by-cell count matrix for all barcodes identified, even those that may not contain true cells.

`scpca-nf` performs filtering of empty droplets, removal of low-quality cells, normalization, dimensionality reduction, cell type annotation, and copy-number variation (CNV) inference (Figure {@fig:fig2}A).
We used the Bioconductor ecosystem [@doi:10.1186/gb-2004-5-10-r80; @doi:10.1038/nmeth.3252] for filtering, normalization, and dimensionality reduction because of its rich documentation, wide use in the community, and relatively small file sizes.
The unfiltered gene-by-cell counts matrices are filtered to remove any barcodes that are unlikely to contain cells using `DropletUtils::emptyDropsCellRanger()` [@doi:10.1186/s13059-019-1662-y].
Low-quality cells are identified and removed with `miQC` [@doi:10.1371/journal.pcbi.1009290], which jointly models the proportion of mitochondrial reads and detected genes per cell and calculates a probability that each cell is compromised.
The remaining cells' counts are normalized [@doi:10.1186/s13059-016-0947-7], and reduced-dimension representations are calculated using both principal component analysis (PCA) and uniform manifold approximation and projection (UMAP) [@arxiv:1802.03426].
Cell types are classified using three automated methods, `SingleR` [@doi:10.1038/s41590-018-0276-y], `CellAssign` [@doi:10.1038/s41592-019-0529-1], and `SCimilarity` [@doi:10.1038/s41586-024-08411-y], and a consensus cell type label is derived from these labels.
Finally, CNV is estimated for each cell using `inferCNV` [@url:https://github.com/broadinstitute/inferCNV].

To support both R and Python users, downloads are available as either `SingleCellExperiment` or `AnnData` [@doi:10.21105/joss.04371] objects.
The workflow outputs three different `SingleCellExperiment` objects to `.rds` files: a processed object containing dimension reduction results, cell type annotations, and CNV inference; an unfiltered object with no processing; and a filtered object with the empty droplet filtered gene-by-cell matrices.
`scpca-nf` also converts all `SingleCellExperiment` objects to `AnnData` objects to `.h5ad` files (Figure {@fig:fig2}A).
Downloads contain the unfiltered, filtered, and processed objects from `scpca-nf` to allow users to choose to perform their own filtering and normalization or to start their analysis from a processed object.
Providing unfiltered raw counts is consistent with the recommendations in Xu et al. [@doi:10.1002/cti2.70033] for maximizing reusability when sharing pediatric cancer single-cell data.

All downloads from the Portal include a quality control (QC) report with a summary of processing information (e.g., `alevin-fry` version), library statistics (e.g., the total number of cells), and a collection of diagnostic plots for each library (Figure {@fig:fig2}B-G).
A knee plot displaying total UMI counts for all droplets (i.e., including empty droplets) indicates the effects of the empty droplet filtering (Figure {@fig:fig2}B).
For each cell remaining after filtering, the total UMI count, genes detected, and mitochondrial fraction are calculated and summarized in a scatter plot (Figure {@fig:fig2}C).
We include plots showing the `miQC` model and the results of `miQC` filtering (Figure {@fig:fig2}D-E).
We also provide a UMAP with cells colored by the number of genes detected and a faceted UMAP plot colored by the expression of highly-variable genes (Figure {@fig:fig2}F-G).

### Processing samples with additional modalities

`scpca-nf` includes modules for processing sequencing modalities beyond single-cell or single-nuclei RNA-seq, including CITE-seq (ADT) [@doi:10.1038/nmeth.4380], multiplexed (cell hashing) [@doi:10.1186/s13059-018-1603-1], spatial transcriptomics, or bulk RNA-seq.

For CITE-seq libraries, ADT reads are quantified using `salmon alevin` and `alevin-fry` (Figure {@fig:figS2}A).
The workflow performs ADT-by-cell counts matrix normalization (see Methods for details) and calculates QC statistics that users can employ for additional filtering before downstream analysis.
For these libraries, the QC report includes additional ADT-related statistics and ADT-specific diagnostic and exploratory plots (Figure {@fig:figS2}B-D).

For multiplexed libraries, the HTO FASTQ files are quantified using `salmon alevin` and `alevin-fry` (Figure {@fig:figS2}E).
Although `scpca-nf` quantifies the HTO data and includes an HTO-by-cell counts matrix in all objects, final demultiplexing is not performed.
Instead, `scpca-nf` applies multiple demultiplexing methods, including demultiplexing with `DropletUtils::hashedDrops()` [@doi:10.18129/B9.bioc.DropletUtils], `Seurat::HTODemux()` [@doi:10.1186/s13059-018-1603-1], and genetic demultiplexing [@doi:10.1093/gigascience/giab062] if bulk RNA-seq data from constituent samples are available.
All demultiplexing results are saved in the filtered and processed `SingleCellExperiment` objects, and HTO-specific library statistics are included in the QC report.

For bulk RNA-seq data, `scpca-nf` trims reads using `fastp` [@doi:10.1093/bioinformatics/bty560], quantifies expression with `salmon` (Figure {@fig:figS3}A) [@doi:10.1038/nmeth.4197], and outputs a TSV file with the gene-by-sample counts matrix for all samples in a given ScPCA project.

Spatial transcriptomics data is processed with Space Ranger [@url:https://www.10xgenomics.com/support/software/space-ranger/latest] to quantify expression and process slide images (Figure {@fig:figS3}B).
The output includes the spot-by-gene matrix along with a summary report produced by Space Ranger.

### Merged objects

Combining data from multiple samples into a single object facilitates joint gene-level analyses, such as differential expression or gene set enrichment analyses.
Therefore, we provide a single merged object for each ScPCA project containing all raw and normalized gene expression data and metadata for all single-cell and single-nuclei RNA-seq libraries (with some exceptions as described in the Methods) produced using our `merge.nf` workflow (Figure {@fig:figS3}C).
Merged objects are not batch-corrected or integrated; users can perform their own batch correction or integration as needed to suit their experimental designs.

### Downloading projects from the ScPCA Portal

Users can download data from individual samples or all data from an ScPCA project as either `SingleCellExperiment` (`.rds`) or `AnnData` (`.h5ad`) objects.
When downloading a complete project, users can either download individual files for each sample (Figure {@fig:fig2}H) or one file containing the gene expression data and metadata for all project samples in the project as a merged object (Figure {@fig:fig2}I).
Users can also generate custom datasets by selecting specific samples across projects for a single download.
In addition to the web interface, we provide an R package, `ScPCAr`, for programmatic access to metadata and files on the Portal, available at <https://alexslemonade.github.io/ScPCAr/>.


### Annotating cell types

Assigning cell type labels to single-cell and single-nuclei RNA-seq data is an essential step in analysis.
Cell type annotation requires knowledge of expected cell types and their associated gene expression patterns, which may be available from public databases or individual publications.
Automated cell type annotation methods leveraging public databases are an excellent initial step in this process, as they can be applied consistently and transparently across samples.
As such, we include cell type annotations from three different automated methods, `SingleR` [@doi:10.1038/s41590-018-0276-y], `CellAssign` [@doi:10.1038/s41592-019-0529-1], and `SCimilarity` [@doi:10.1038/s41586-024-08411-y], in all processed `SingleCellExperiment` and `AnnData` objects (Figure {@fig:fig3}A) (see Methods for details).
An additional cell type report with information about references, comparisons among cell type annotation methods, and diagnostic plots is also provided.

Some ScPCA projects also have curated cell type annotations, including tumor cells and disease-specific cell states, provided by submitters.
These submitter-provided annotations are in all `SingleCellExperiment` and `AnnData` objects (unfiltered, filtered, and processed).
Cell type reports for these projects include a table summarizing the submitter cell type annotations, a UMAP colored by the submitter annotation, and a comparison of submitter annotations to automated cell typing results.

#### Assigning consensus cell types

`SingleR`, `CellAssign`, and `SCimilarity` use different references and computational approaches.
Additionally, most public annotated reference datasets compatible with `SingleR` and `CellAssign`, including those used for the Portal, are derived from normal tissue, making annotating tumor datasets particularly difficult.
Consistent cell type annotations across methods can indicate higher confidence, so we created a set of ontology-aware rules to assign consensus cell type labels based on the methods' agreement.

`scpca-nf` assigns consensus cell type labels when two of the three automated methods agree.
Specifically, we perform pairwise comparisons among automated cell type annotations to identify the latest common ancestor (LCA) in Cell Ontology [@doi:10.1186/s13326-016-0088-7; @doi:10.1186/1471-2105-12-6; @doi:10.1186/gb-2005-6-2-r21].
The consensus cell type is the LCA term with the fewest descendants (Figure {@fig:fig3}B).
To ensure specificity, cells are only assigned a consensus cell type if the identified LCA has fewer than 170 descendant terms (see Methods for exceptions).
This threshold excludes overly general cell ontology terms like lymphocyte, while retaining meaningful classifications like T cell and B cell.
Consensus cell type assignments are available in all processed objects on the Portal.
Figure {@fig:fig3}C shows an example heatmap comparing automated and consensus cell type labels for a glioma library on the Portal.

This ontology-based approach allowed us to account for different levels of granularity in annotation reference datasets.
For example, Figure {@fig:figS4}A displays cells that are annotated as different T cell subtypes by each automated method.
Harmonizing annotations into a consensus cell type provides a single, consistent label for each cell (Figure {@fig:figS4}B) and facilitates downstream analyses across multiple samples.

We validated consensus cell types by evaluating cell-type-specific marker gene expression across all cells (Figure {@fig:fig4}A, Figure {@fig:figS5}), observing high concordance between consensus labels and marker gene expression.
Library-specific versions of Figures {@fig:fig4}A and {@fig:fig3}C are included in the QC report, allowing users to assess the reliability of consensus annotations and compare labels across methods.


#### Consensus cell type annotations in brain and CNS samples available on the Portal

Consensus annotations are particularly useful when examining samples from multiple projects.
Figure {@fig:fig4}B, for example, displays cell types across all high-grade (HGG) and low-grade glioma (LGG) samples, which originate from six projects and four investigators and reveals similar cell types across all glioma samples.

Previous studies have characterized the glioma immune microenvironment as predominantly comprised of myeloid cells, including microglia and glioma-associated macrophages, with smaller proportions of lymphocytes such as T cells [@doi:10.1038/s41698-024-00717-4; @doi:10.1093/noajnl/vdad009].
While we observe that most immune cells in glioma samples are myeloid or T cell types, there is notable notable heterogeneity within HGG and LGG subtypes (Figure {@fig:fig4}C).
Figure {@fig:fig4}D shows the expression of cell-type specific markers for more granular immune cell types, validating the assignment of various immune cell types within the assigned consensus cell types.
A summary of all the consensus cell types observed in all other ScPCA samples can be found in Figure {@fig:figS6}.


#### Augmenting cell type annotations for malignant cell identification

Because the references used for automated methods do not consider tumor cell states, they provide limited information for distinguishing malignant from normal cells.
We therefore sought complementary avenues to help identify malignant cells.

To this end, we launched the OpenScPCA project [@url:https://openscpca.readthedocs.io], an open-science collaborative initiative to characterize and analyze Portal data, focusing first on improving cell type annotations.
Thus far, we have added cell type annotations for two projects, `SCPCP000004` (neuroblastoma) and `SCPCP000015` (Ewing sarcoma), to the Portal based on OpenScPCA analyses.
Figure {@fig:fig5}A displays a UMAP of all libraries in `SCPCP000004` highlighting this project's OpenScPCA annotations, derived using the `NBAtlas` reference dataset [@doi:10.1016/j.celrep.2024.114804].
Unlike the consensus cell type annotations, the OpenScPCA annotations distinguish between normal and malignant cells and contain far fewer uncharacterized cells.
Summary cell type reports for projects with OpenScPCA annotations also include comparisons between `scpca-nf` and OpenScPCA annotations.

In addition, `scpca-nf` applies `inferCNV` [@url:https://github.com/broadinstitute/inferCNV] to estimate copy-number alterations (Figure {@fig:fig2}A) when enough normal cells are present in a library to serve as a reference (see Methods for details).
The CNV estimates complement the consensus cell types by providing a proxy for a cell's malignant status; cells with high levels of CNV are more likely to be tumor cells.
Across libraries within `SCPCP000004`, malignant cell type annotations from OpenScPCA (which does not use CNV information) (Figure {@fig:fig5}A) and the total per-cell CNV (Figure {@fig:fig5}B) broadly correspond.
We probed this relationship further within a single neuroblastoma library, finding signatures of canonical neuroblastoma CNV events such as `1q` loss, `11q` gain, and `17p` loss [@doi:10.1038/nrdp.2016.78; @doi:10.1016/j.celrep.2024.114804; @doi:10.1158/2159-8290.CD-14-0622] within malignant cells (Figure {@fig:fig5}C).
By contrast, normal cells show very few CNV events.
Unknown cells show CNV event signatures similar to the malignant cells, suggesting many of these cells may be malignant.

Malignancy can also be assessed by interpreting consensus cell types alongside CNV inferences, which is particularly useful for projects which do not yet have OpenScPCA annotations.
Figure {@fig:fig5}D shows per-cell CNV distributions for the most common consensus cell types in a neuroblastoma library.
Unknown and neuron cells have distinctly higher values, suggesting possible malignancy.
We see similar patterns in a ganglioglioma library (Figure {@fig:figS4}B-C), where consensus immune cell types have low CNV values, while other cell types including oligodendrocyte precursor cells, neuron associated cells, and unknown cells have much higher CNV values.

### Analysis of bulk RNA-seq

Several projects in the ScPCA Portal contain bulk RNA-seq data in addition to single-cell or single-nuclei RNA-seq data.
Compared to bulk RNA-seq, single-cell and single-nuclei RNA-seq technologies may fail to capture certain cell types [@doi:10.1038/s41587-020-0465-8] due to technical aspects of library preparation.
We therefore asked whether we could identify differences in biological signal between these two modalities that may suggest distinct cell type distributions by interrogating ScPCA projects of solid tumors, considering only samples with both sequencing modalities.
We analyzed 97 samples across five projects: `SCPCP00001` (high-grade glioma), `SCPCP000002` (low-grade glioma), `SCPCP000006` (Wilms tumor), `SCPCP000009` (CNS tumors), and `SCPCP000017` (osteosarcoma).
As described in Methods, we derived pseudobulk expression matrices for each single-cell or single-nuclei library and compared the pseudobulk expression to bulk using a series of linear models (one per ScPCA project) with a random effect controlling for sample (Figure {@fig:fig6}A, Figure {@fig:figS7}A).
As expected, all projects showed a positive relationship between bulk and pseudobulk expression.

We next performed an overrepresentation analysis to probe for differences in gene expression suggestive of different cell type compositions and/or abundances between modalities.
We calculated the per-gene median of each project's model residuals and identified outliers.
"Positive outliers" are genes with higher bulk RNA-seq expression than expected from pseudobulk expression, and "negative outliers" are genes with lower bulk RNA-seq expression than expected from pseudobulk expression.
Using cell type marker gene sets from each project's respective `CellAssign` reference, we calculated the odds ratio in each direction as the odds a cell type marker gene is present in the given outlier direction compared to other genes.
Following permutation testing and P-value correction to control the FDR at 5\%, we found several cell type marker gene sets with higher, but never lower, bulk RNA-seq expression than expected (Figure {@fig:fig6}B, Figure {@fig:figS7}B).

In brain and CNS tumors, the overrepresented marker gene sets in bulk RNA-seq were primarily stromal (e.g., endothelial cells and pericytes) and neuronal cell types (e.g., astrocytes and glial cells), all of which are prevalent in glioma tumor microenvironments [@doi:10.3389/fimmu.2023.1227126; @doi:10.3389/fphar.2024.1355242] (Figure {@fig:fig6}B).
By contrast, only monocytes and neuronal cell types were overrepresented in `SCPCP000009` (brain and CNS tumors) bulk RNA-seq.
As `SCPCP000009` was sequenced at the single-nuclei level while `SCPCP000001` and `SCPCP000002` were sequenced at the single-cell level, this difference may reflect the reduced sensitivity of single-nuclei approaches to detecting immune cells [@doi:10.4132/jptm.2022.12.19].
The other single-nuclei projects similarly showed immune cell overrepresentation in bulk RNA-seq: Monocytes for `SCPCP000006` and a mix of immune and non-immune cell types for `SCPCP000017` (Figure {@fig:figS7}B), the latter possibly reflecting challenges in dissociating bone tissue [@doi:10.1186/s12885-023-10977-1].
Overall, while bulk and single-cell/nuclei expression are highly correlated, cell type composition differences between modalities may reflect cell-type-specific loss in single-cell experiments.



## STAR Methods

### RESOURCE AVAILABILITY

#### Lead contact

Requests for resources and information regarding resource sharing should be directed to the lead contact, Jaclyn N. Taroni (jaclyn.taroni@ccdatalab.org).

#### Materials availability

This study did not generate any new material resources.

#### Data and code availability

##### Data

All processed RNA-seq data and de-identified metadata described in this study are freely available through the ScPCA Portal at <scpca.alexslemonade.org>, which is designed for long-term open access of single-cell, single-nuclei, and spatial transcriptomics data; data are available as of the date of publication.
Each project, sample, and library is assigned a stable, unique accession number.
Raw data (e.g., FASTQ files) are not available for download from the Portal due to the human origins of most samples, which may be subject to controlled-access restrictions. 
When raw or processed data are also deposited to external sources such as the Database of Genotypes and Phenotypes (dbGaP) or Gene Expression Omnibus (GEO), the project accession numbers are available from the Portal.

All projects included in this publication are available from the ScPCA Portal with the following accession numbers: [SCPCP000001](https://scpca.alexslemonade.org/projects/SCPCP000001), [SCPCP000002](https://scpca.alexslemonade.org/projects/SCPCP000002), [SCPCP000003](https://scpca.alexslemonade.org/projects/SCPCP000003), [SCPCP000004](https://scpca.alexslemonade.org/projects/SCPCP000004), [SCPCP000005](https://scpca.alexslemonade.org/projects/SCPCP000005), [SCPCP000006](https://scpca.alexslemonade.org/projects/SCPCP000006), [SCPCP000007](https://scpca.alexslemonade.org/projects/SCPCP000007), [SCPCP000008](https://scpca.alexslemonade.org/projects/SCPCP000008), [SCPCP000009](https://scpca.alexslemonade.org/projects/SCPCP000009), [SCPCP000010](https://scpca.alexslemonade.org/projects/SCPCP000010), [SCPCP000011](https://scpca.alexslemonade.org/projects/SCPCP000011), [SCPCP000012](https://scpca.alexslemonade.org/projects/SCPCP000012), [SCPCP000013](https://scpca.alexslemonade.org/projects/SCPCP000013), [SCPCP000014](https://scpca.alexslemonade.org/projects/SCPCP000014), [SCPCP000015](https://scpca.alexslemonade.org/projects/SCPCP000015), [SCPCP000016](https://scpca.alexslemonade.org/projects/SCPCP000016), [SCPCP000017](https://scpca.alexslemonade.org/projects/SCPCP000017), [SCPCP000018](https://scpca.alexslemonade.org/projects/SCPCP000018), [SCPCP000020](https://scpca.alexslemonade.org/projects/SCPCP000020), [SCPCP000021](https://scpca.alexslemonade.org/projects/SCPCP000021), [SCPCP000022](https://scpca.alexslemonade.org/projects/SCPCP000022), [SCPCP000023](https://scpca.alexslemonade.org/projects/SCPCP000023), [SCPCP000024](https://scpca.alexslemonade.org/projects/SCPCP000024).

##### Code

- The Nextflow workflow used to process all samples is available on GitHub at <https://github.com/AlexsLemonade/scpca-nf> and is archived at [TODO: Zenodo DOI].
- The ScPCA Portal code can be found at <https://github.com/AlexsLemonade/scpca-portal> and is archived at 10.5281/zenodo.20058961 [@doi:10.5281/zenodo.20058961].
- The benchmarking of tools used to build `scpca-nf` are available at <https://github.com/AlexsLemonade/alsf-scpca/tree/main/analysis> and <https://github.com/AlexsLemonade/sc-data-integration/tree/main/celltype_annotation>, with all repository contents archived at 10.5281/zenodo.20044281 [@doi:10.5281/zenodo.20044281] and 10.5281/zenodo.20044314 [@doi:10.5281/zenodo.20044313], respectively.
- All code for creating reference files for consensus cell type assignment is available at <https://github.com/AlexsLemonade/OpenScPCA-analysis/tree/main/analyses/cell-type-consensus>, and all repository contents are archived at 10.5281/zenodo.18459136.
- All code to assign OpenScPCA project cell type annotations is available at <https://github.com/AlexsLemonade/OpenScPCA-nf> and is archived at 10.5281/zenodo.20056054 [@doi:10.5281/zenodo.20056054].
- All code for the `ScPCAr` package for programmatically downloading data from the Portal can be found at <https://github.com/AlexsLemonade/ScPCAr> and is archived at 10.5281/zenodo.20044462 [@doi:10.5281/zenodo.20044462].
- All code for the underlying figures and analyses is available at <https://github.com/AlexsLemonade/scpca-paper-figures> and is archived at [TODO: Zenodo DOI].
To reproduce the figures in this manuscript, see <https://github.com/AlexsLemonade/scpca-paper-figures/tree/main/reproduce-figures>.

##### Additional information

ScPCA documentation that describes the contents of downloads available from the Portal is available at <https://scpca.readthedocs.io/en/stable/>.
Any additional information required to reanalyze the data in this study is available from the lead contact upon request.

### EXPERIMENTAL MODEL AND SUBJECT DETAILS

Data on the ScPCA Portal were generated and compiled by each contributing lab and institution.
As of May 1, 2026, gene expression data from 704 samples are available.
This includes 581 human patient samples, 117 samples from patient-derived xenografts, 4 samples from immortalized human cell lines, and 2 samples from cell lines passaged from patient-derived xenografts representing 55 different pediatric cancer types.

#### Metadata

Submitters were required to submit the age, sex, organism, diagnosis, subdiagnosis (if applicable), disease timing (e.g., initial diagnosis) and tissue of origin for each sample.
The submitted metadata was standardized across projects, including converting all ages to years, removing abbreviations used in diagnosis, subdiagnosis, or tissue of origin, and using standard values across projects as much as possible for diagnosis, subdiagnosis, disease timing, and tissue of origin.
For example, all samples obtained at diagnosis were assigned the value `Initial diagnosis` for disease timing.

In an effort to ensure sample metadata for ScPCA are compatible with CZI's CELLxGENE, ontology term identifiers were assigned to metadata categories for each sample following the guidelines present in the CELLxGENE schema [@url:https://cellxgene.cziscience.com; @url:https://github.com/chanzuckerberg/single-cell-curation/blob/main/schema/3.0.0/schema.md], as shown in Table {@tbl:metadata}.
<br><br>

| Metadata field   | Ontology term description             |
| ----------- | ------------------------------------------------------------------------------ |
| Age             | Ontology term obtained from HsapDv [@url:https://www.ebi.ac.uk/ols4/ontologies/hsapdv]. For ages 0-11 months, the HsapDv for age in months was used. For ages 12 months and greater, the HsapDv for age in years was used. |
| Sex             | Ontology term obtained from PATO, either male (PATO:0000384), female (PATO:0000383), or unknown  [@doi:10.1093/bib/bbx035; @url:https://www.ebi.ac.uk/ols4/ontologies/pato].  |
| Organism   | NCBI taxonomy term for organism. All current samples available on the Portal are from Homo sapiens or NCBITaxon:9606 [@doi:10.1093/database/baaa062; @url:https://www.ncbi.nlm.nih.gov/taxonomy].|
| Diagnosis   | The most appropriate MONDO term based on the provided diagnosis [@doi:10.1093/genetics/iyaf215; @url:https://www.ebi.ac.uk/ols4/ontologies/mondo]. An exact match was identified for most samples, but in a handful of cases, the most closely related term was used.  |
| Tissue of origin | The most appropriate UBERON term based on the provided tissue of origin [@doi:10.1186/2041-1480-5-21; @doi:10.1186/gb-2012-13-1-r5; @url:https://www.ebi.ac.uk/ols4/ontologies/uberon]. An exact match was identified for most samples, but in a handful of cases, the most closely related term was used.  |
| Ethnicity (if applicable)  | If the submitter provided ethnicity, the associated Hancestro term [@doi:10.1186/s13059-018-1396-2; @url:https://www.ebi.ac.uk/ols4/ontologies/hancestro]. If ethnicity is unavailable, `unknown` is used. |

Table: Assignment of metadata fields to ontology terms. {#tbl:metadata}

The majority (87%) of projects on the Portal have additional metadata fields, such as the presence or absence of treatment, tumor grade, or whether a sample was obtained from a primary tumor or metastasis.

#### Ethics statement

For ALSF-funded datasets comprised of human subjects data, Institutional Review Boards (IRB) or research ethics boards at grantee institutions approved the research or determined it was exempt.
For community-contributed datasets containing summarized data and de-identified metadata from human subjects, submitting institutions certified that all approvals and consents were obtained or listed the IRB protocol in transfer agreements.
ALSF-funded xenograft datasets were approved by the grantee institution's Institutional Animal Care and Use Committee.


### METHOD DETAILS

#### Data generation and processing

Raw data and metadata were generated and compiled by each lab and institution contributing to the Portal.
Single-cell or single-nuclei libraries were generated using one of the commercially available kits from 10x Genomics.
For bulk RNA-seq, RNA was collected and sequenced using either paired-end or single-end sequencing.
For spatial transcriptomics, cDNA libraries were generated using the Visium kit from 10x Genomics.
All libraries were processed using our open-source pipeline, `scpca-nf`, to produce summarized gene expression data.
A detailed summary with the total number of samples and libraries collected for each sequencing method broken down by project is available in Table S1.

#### Processing single-cell and single-nuclei RNA-seq data with alevin-fry

To quantify RNA-seq gene expression for each cell or nucleus in a library, `scpca-nf` uses `salmon alevin` [@doi:10.1186/s13059-020-02151-8] and `alevin-fry` [@doi:10.1038/s41592-022-01408-3] to generate a gene-by-cell counts matrix.
Prior to mapping, we generated an index using transcripts from both spliced cDNA and unspliced cDNA sequences, denoted as the `splici` index [@doi:10.1038/s41592-022-01408-3].
The index was generated from the human genome, GRCh38, Ensembl version 104.
`salmon alevin` was run using selective alignment to the `splici` index with the `--rad` option to generate a reduced alignment data (RAD) file required for input to `alevin-fry`.

The RAD file was used as input to the recommended `alevin-fry` workflow, with the following customizations.
At the `generate-permit-list` step, we used the `--unfiltered-pl` option to provide a list of expected barcodes specific to the 10x kit used to generate each library.
The `quant` step was run using the `cr-like-em` resolution strategy for feature quantification and UMI de-duplication.

#### Post alevin-fry processing of single-cell and single-nuclei RNA-seq data

The output from running `alevin-fry` includes a gene-by-cell counts matrix, with reads from both spliced and unspliced reads for all potential cell barcodes.
The gene-by-cell counts matrix is read into R to create a `SingleCellExperiment` object using `fishpond::load_fry()`.
The resulting object contains a `counts` assay with a gene-by-cell counts matrix where all spliced and unspliced reads for a given gene are totaled together.
We also include a `spliced` assay that contains a gene-by-cell counts matrix with only spliced reads.
These matrices include all potential cells, including empty droplets, and are provided for all Portal downloads in the unfiltered objects saved as `.rds` files with the `_unfiltered.rds` suffix.

Each droplet was tested for deviation from the ambient RNA profile using `DropletUtils::emptyDropsCellRanger()` [@doi:10.1186/s13059-019-1662-y; @doi:10.1038/s41467-018-05083-x] and those with an FDR ≤ 0.01 were retained as likely cells.
If a library did not have a sufficient number of droplets and `DropletUtils::emptyDropsCellRanger()` failed, cells with fewer than 100 UMIs were removed.
Gene expression data for any cells that remain after filtering are provided in the filtered objects saved as `.rds` files with the `_filtered.rds` suffix.
These filtered objects additionally contain results from doublet detection performed with `scDblFinder::scDblFinder()` [@doi:10.12688/f1000research.73600.2], including each cell's predicted class ("singlet" or "doublet") as well as the associated doublet score.
However, predicted doublets were not filtered out; users can instead use these `scDblFinder` results to filter doublets as needed for their specific analysis needs.

Following removal of empty droplets, `scpca-nf` proceeds to remove cells that are likely to be compromised by damage or low-quality sequencing.
`miQC` was used to calculate the posterior probability that each cell is compromised [@doi:10.1371/journal.pcbi.1009290].
Any cells with a probability of being compromised greater than 0.75 and fewer than 200 genes detected were removed before further processing.
The gene expression counts from the remaining cells were log-normalized using the deconvolution method from Lun, Bach, and Marioni [@doi:10.1186/s13059-016-0947-7].
Briefly, `scran::quickCluster()` was used to derive cell clusters on which to calculate sum factors with `scran::computeSumFactors()`, which are in turn used during normalization with `scuttle::logNormCounts()`.
If this deconvolution-based approach failed for any reason, only `scuttle::logNormCounts()` was used for normalization.

Next, `scran::modelGeneVar()` was used to model gene variance from the log-normalized counts and `scran::getTopHVGs()` was used to select the top 2000 high-variance genes.
These were used as input to calculate the top 50 principal components using `scater::runPCA()`.
Finally, UMAP embeddings were calculated from the principal components with `scater::runUMAP()`.
The raw and log-normalized counts, list of 2000 high-variance genes, principal components, and UMAP embeddings are all stored in the processed objects saved as `.rds` files with the `_processed.rds` suffix.

#### Quantifying gene expression for libraries with CITE-seq or cell hashing

All libraries with antibody-derived tags (ADTs) or hashtag oligonucleotides (HTOs) were mapped to a reference index using `salmon alevin` and quantified using `alevin-fry`.
The reference indices were constructed using the `salmon index` command with the `--feature` option.
References were custom-built for each ScPCA project and constructed using the submitter-provided list of ADTs or HTOs and their barcode sequences.

The ADT-by-cell or HTO-by-cell counts matrix produced by `alevin-fry` were read into R as a `SingleCellExperiment` object and saved as an alternative experiment (`altExp`) in the same `SingleCellExperiment` object with the unfiltered gene expression counts data.
The `altExp` within the unfiltered object contains all identified ADTs or HTOs and all barcodes identified in the RNA-seq gene expression data.
Any barcodes that only appeared in either ADT or HTO data were discarded, and cell barcodes that were only found in the gene expression data (i.e., did not appear in the ADT or HTO data) were assigned zero counts for all ADTs and HTOs.
Any cells removed after filtering empty droplets were also removed from the ADT and HTO counts matrices and before creating the filtered `SingleCellExperiment` object.

#### Processing ADT expression data from CITE-seq

The ADT count matrix stored in the unfiltered object was used to calculate an ambient profile with `DropletUtils::ambientProfileEmpty()`.
The ambient profile was used to calculate quality-control statistics with `DropletUtils::cleanTagCounts()` for all cells remaining after removing empty droplets.
Any negative or isotype controls were taken into account when calculating QC statistics.
This function flags cells as low-quality if they either have very high levels of ambient contamination and/or negative/isotype controls (if present), or lack ambient expression altogether, which may indicate failed capture.
However, we did not remove any cells based on ADT quality because that would remove those cells from the `SingleCellExperiment` object, regardless of the quality of the RNA expression.
Instead, the filtered and processed objects contain the results from running `DropletUtils::cleanTagCounts()`, which users can leverage for filtering as desired.

ADT count data were then normalized using `scuttle::computeMedianFactors()`, which calculates a per-cell size factor as the median ratio of the cell's counts to the background profile previously calculated with `DropletUtils::ambientProfileEmpty()`.
We then used these factors to normalize ADT counts with `scuttle::logNormCounts()`.
If median-based normalization failed for any reason, ADT counts were log-transformed after adding a pseudocount of 1.
We only performed normalization on cells that would be retained after ADT filtering; we assigned `NA` normalized counts to any cells that would be filtered out based on `DropletUtils::cleanTagCounts()`.
The normalized ADT data are available in the `altExp` of the processed object.
Although `scpca-nf` normalizes ADT counts, the workflow does not perform any dimensionality reduction of ADT data; only the RNA counts data are used as input for dimensionality reduction.
Additionally, note that we did not perform background subtraction on the ADT counts, but we provide the ambient profile calculated with `DropletUtils::ambientProfileEmpty()`, which users can employ to perform global de-noising as needed.
During conversion to `AnnData` objects, the modalities are exported as separate RNA (`_rna.h5ad`) and ADT (`_adt.h5ad`) objects.

#### Processing HTO data from multiplexed libraries

As with ADT data, `scpca-nf` does not filter any cells based on HTO expression, and any cells removed after filtering empty droplets based on the unfiltered RNA counts matrix are also removed from the HTO counts matrix in the filtered object.
`scpca-nf` does not perform any additional filtering or processing of the HTO-by-cell counts matrix, so the same filtered matrix is included in the processed object.

To identify which cells come from which sample in a multiplexed library, we applied three different demultiplexing methods: genetic demultiplexing, HTO demultiplexing using `DropletUtils::hashedDrops()`, and HTO demultiplexing using `Seurat::HTODemux()`.
We do not provide separate `SingleCellExperiment` objects for each sample in a library.
Each multiplexed library object contains the counts data from all samples and the results from all three demultiplexing methods to allow users to select which method(s) to use.

##### Genetic demultiplexing

If all samples in a multiplexed library were also sequenced using bulk RNA-seq, we performed genetic demultiplexing using genotype data from both bulk RNA-seq and single-cell or single-nuclei RNA-seq [@doi:10.1093/gigascience/giab062].
If bulk RNA-seq was not available, no genetic demultiplexing was performed.

Bulk RNA-seq reads for each sample were mapped to a reference genome using `STAR` [@doi:10.1093/bioinformatics/bts635], and multiplexed single-cell or single-nuclei RNA-seq reads were mapped to the same reference genome using `STARsolo`[@doi:10.1101/2021.05.05.442755].
The mapped bulk reads were used to call variants and assign genotypes with `bcftools mpileup` [@doi:10.1093/gigascience/giab008].
`cellsnp-lite` was then used to genotype single-cell data at the identified sites found in the bulk RNA-seq data [@doi:10.1093/bioinformatics/btab358].
Finally, `vireo` was used to identify the sample of origin [@doi:10.1093/bioinformatics/btab358].

##### HTO demultiplexing

For all multiplexed libraries, we performed demultiplexing using `DropletUtils::hashedDrops()` and `Seurat::HTODemux()`.
For both methods, we used the default parameters and only performed demultiplexing on the filtered cells present in the filtered object.
The results from both these methods are available in the filtered and processed objects.

#### Quantification of spatial transcriptomics data

10x Genomics' Space Ranger [@url:https://www.10xgenomics.com/support/software/space-ranger/latest] was used to quantify gene expression data from spatial transcriptomics libraries.
`cellranger mkref` was used to create a reference index from the human genome, GRCh38, Ensembl version 104.
The FASTQ files, microscopic slide image, and slide serial number were provided as input to `spaceranger count`.
The raw and filtered counts matrix, slide images, and the summary report output by `spaceranger count` are included in the output from `scpca-nf`.

#### Quantification of bulk RNA-seq data

`fastp` was used to trim adapters and perform quality and length filtering on all FASTQ files from bulk RNA-seq.
We used a decoy-aware reference created from spliced cDNA sequences with the entire human genome sequence (GRCh38, Ensembl version 104) as the decoy [@doi:10.1038/nmeth.4197].
The trimmed reads were then provided as input to `salmon quant` for selective alignment.
In addition to using the default parameters for `salmon quant`, we applied the `--seqBias` and `--gcBias` flags to correct for sequence-specific biases due to random hexamer priming and fragment-level GC biases, respectively.

#### Cell type annotation

Cell type labels determined by `SingleR` [@doi:10.1038/s41590-018-0276-y], `CellAssign` [@doi:10.1038/s41592-019-0529-1], and `SCimilarity` [@doi:10.1038/s41586-024-08411-y] were added to processed `SingleCellExperiment` objects.
If cell types were obtained from the submitter of the dataset, the submitter-provided annotations were incorporated into all `SingleCellExperiment` objects (unfiltered, filtered, and processed).

To prepare the references used for assigning cell types, we developed a separate workflow, `build-celltype-index.nf`, within `scpca-nf`.
We used the `BlueprintEncodeData` reference from the `celldex` package [@doi:10.1038/s41590-018-0276-y; @doi:10.3324/haematol.2013.094243; @doi:10.1038/nature11247] to train the `SingleR` classification model with `SingleR::trainSingleR()`.
In the main `scpca-nf` workflow, this model and the processed `SingleCellExperiment` object were input to `SingleR::classifySingleR()`.
The `SingleR` output of cell type annotations and a score matrix for each cell and all possible cell types were added to the processed `SingleCellExperiment` object.

The `BlueprintEncodeData` reference was chosen because it had either a similar or higher delta median statistic compared to other references available in `celldex` when applied to samples from a variety of diagnoses.
The delta median statistic for each cell was calculated by subtracting the median cell type score from the score associated with the assigned cell type [@url:https://bioconductor.org/books/release/SingleRBook/annotation-diagnostics.html#based-on-the-deltas-across-cells] and was used to evaluate confidence in `SingleR` cell type assignments.
The cell type report shows the distribution of delta median values for each cell type.
A higher delta median statistic for a cell generally indicates higher confidence in the final cell type annotation.

For `CellAssign`, marker gene references were created using the marker gene lists available on `PanglaoDB` [@doi:10.1093/database/baz046].
Organ-specific references were built using all cell types in a specified organ listed in `PanglaoDB` to accommodate all ScPCA projects encompassing a variety of disease and tissue types.
If a set of disease types in a given project encompassed cells that may be present in multiple organ groups, multiple organs were combined.
Since many cancers may have infiltrating immune cells, all immune cells were also included in each organ-specific reference.
For example, we created a reference containing bone, connective tissue, smooth muscle, and immune cells for sarcomas that appear in bone or soft tissue.
The specific reference information and list of organs included in that reference for a given library is available in the metadata of each processed object.

Given the processed `SingleCellExperiment` object and organ-specific reference, `scvi.external.CellAssign()` was used in the main `scpca-nf` workflow to train the model and predict the assigned cell type.
For each cell, `CellAssign` calculates a probability of assignment to each cell type in the reference.
The probability matrix and a prediction based on the most probable cell type were added as cell type annotations to the processed `SingleCellExperiment` object.
We also display the distribution of all probabilities calculated by `CellAssign` in the cell type report; more confident labels are expected to have many values close to 1.

For `SCimilarity`, the foundation model described in Heimberg et al. [@doi:10.1038/s41586-024-08411-y] containing 7.3 million cells from various normal and diseased tissues was obtained from Zenodo (<https://zenodo.org/records/10685499>) and used to annotate cells in all samples.
Embeddings were first computed on the processed `AnnData` objects using `scimilarity.get_embeddings()` followed by cell type prediction using `scimilarity.get_predictions_knn()` with `weighting=True`.
The assigned cell type label and the distance of the query cell to the closest cell in the model were added to the processed `SingleCellExperiment` object.
A plot showing the distribution of the distance metric calculated by `SCimilarity` is present in the cell type report.
Distances larger than 0.05 can indicate that the model is less confident in the prediction.

##### Assigning consensus cell types

Cell type labels obtained from `SingleR`, `CellAssign`, and `SCimilarity` were then used to assign an ontology-aware consensus cell type label.
We first assigned each of the cell types present in the `PanglaoDB` [@doi:10.1093/database/baz046] reference used with `CellAssign` to an appropriate Cell Ontology term [@doi:10.1186/gb-2005-6-2-r21; @doi:10.1186/1471-2105-12-6; @doi:10.1186/s13326-016-0088-7; @doi:10.1038/s41597-026-07173-8].
For cell types available in the `BlueprintEncodeData` reference used with `SingleR` and the foundation model used with `SCimilarity`, we used the provided Cell Ontology terms.

We then created a reference table containing all possible combinations of cell types assigned using `SingleR`, `CellAssign`, and `SCimilarity`.
Consensus cell types are assigned if two of the three annotations share a latest common ancestor (LCA), identified using `ontoProc::findCommonAncestors()` [@doi:10.18129/B9.bioc.ontoProc], that meets the following criteria.
Otherwise, no consensus cell type is assigned, and the cell is labeled as "Unknown".

1. The terms share at least 1 LCA that either has fewer than 170 descendants or is one of "neuron", "epithelial cell", "columnar/cuboidal epithelial cell", or "endo-epithelial cell".

2. If more than 1 LCA is shared between two terms, then the LCA with the fewest descendants is kept and all others are discarded.

3. If the LCA has fewer than 170 descendants and is one of the following non-specific LCA terms, no consensus cell type is assigned: "bone cell", "lining cell", "blood cell", "progenitor cell", "supporting cell", "biogenic amine secreting cell", "protein secreting cell", "extracellular matrix secreting cell", "serotonin secreting cell", "peptide hormone secreting cell", "exocrine cell", "sensory receptor cell", or "interstitial cell".

If more than one LCA is identified as a possible consensus cell type, meaning there is agreement among all three methods, the LCA with the fewest descendants is used as the consensus cell type.

The consensus cell type assignments, including both the Cell Ontology term and the associated human-readable name, are available in processed object files on the Portal.

Consensus cell type assignments were evaluated by looking at marker gene expression in a set of cell-type specific marker genes.
Marker genes were obtained from the list of Human cell markers on `CellMarker 2.0` [@doi:10.1093/nar/gkac947].
We considered only those that are specific to a single cell type, with the exception of hematopoietic precursor cells, which express genes found in other, more differentiated immune cells.

##### Cell types annotated as part of the OpenScPCA Project

As part of the ongoing OpenScPCA project [@url:https://openscpca.readthedocs.io], cell types for each project are manually annotated to label disease-specific cell types or cell states.
After annotations for all samples in a given project have been validated, they are added to all `SingleCellExperiment` objects (unfiltered, filtered, and processed) for that project on the Portal.
To date, cell types have been assigned and validated for `SCPCP000004` (neuroblastoma) and `SCPCP000015` (Ewing sarcoma).
The approaches for cell type annotation were originally developed in the `OpenScPCA-analysis` GitHub repository [@url:https://github.com/AlexsLemonade/OpenScPCA-analysis] in the `cell-type-neuroblastoma-04` and `cell-type-ewings` analysis modules, respectively.
These analysis modules provide full information on the specific approaches used for annotation.
The cell type annotations included in the ScPCA Portal were subsequently generated in corresponding Nextflow modules in the `OpenScPCA-nf` GitHub repository [@url:https://github.com/AlexsLemonade/OpenScPCA-nf].

For `SCPCP000004` (neuroblastoma), shown in Figure 5, cell type annotation is performed with both `SingleR` [@do:10.1016/j.celrep.2024.114804] and `scANVI/scArches` [@doi:10.1038/s41587-021-01001-7] using the `NBAtlas` from Bonine et al. as a reference [@doi:10.1016/j.celrep.2024.114804]. 
Final annotations are derived based on agreement between these two methods and the consensus cell types. 
If `SingleR` and `scANVI/scArches` agree exactly, then that label is used. 
If `SingleR` and `scANVI/scArches` labels are in same broad family (e.g., T cell and CD4 + T cell) then the broad family label is used (e.g., T cell). 
If `SingleR` and `scANVI/scArches` disagree and at least one inference agrees with the consensus cell type label then we assign that label. 
If the consensus cell type is `Unknown` and one of the `SingleR` and/or `scANVI/scArches` labels is one of `Neuroendocrine` and the other is one of `Schwann`, `Stromal other`, or `Fibroblast`, the `Neuroendocrine` label is assigned. 

For `SCPCP000015` (Ewing sarcoma), tumor cells were first identified by running `AUCell` [@doi:10.18129/B9.bioc.AUCell] on a merged object containing all samples with `EWS::FLI1` marker gene sets obtained from `MSigDB` and published literature. 
Cells with an AUC > 0.4 for the `EWS::FLI1` marker gene set obtained from Aynaud et al. [@doi:10.1016/j.celrep.2020.01.049] and AUC > 0.1 for the `STAEGE_EWING_FAMILY_TUMOR` gene set from `MSigDB` [@doi:0.1158/0008-5472.CAN-03-4059] were classified as `tumor EWS-high`. 
Cells with an AUC > 0.1 for the `EWS::FLI1` marker gene set obtained from Wrenn et al. [@doi:10.1158/1078-0432.CCR-23-1111] and AUC > 0.05 for the `HALLMARK_EPITHELIAL_MESENCHYMAL_TRANSITION` gene set from `MSigDB` [@doi:10.1016/j.cels.2015.12.004] were classified as `tumor EWS-low`.
Cells that met the criteria for `tumor EWS-high` and had mean expression of proliferative markers (`MKI67`, `PCNA`, and `TOP2A`) > 0 were classified as `tumor EWS-high proliferative`.
For all non-tumor cells, the consensus cell type label was used. 

#### Copy-number variation inference

We used `inferCNV` [@url:https://github.com/broadinstitute/inferCNV] with the `i6` HMM to estimate copy-number variation (CNV) events for each library, for each chromosome arm.
We designated a set of normal consensus cell types to use for each library's normal reference based on the given sample's diagnosis.
The list of cell types included in the reference used for `inferCNV` can be found in the metadata of the processed object for a given library.
All libraries were processed with `inferCNV` except: i) libraries without assigned consensus cell types, ii) libraries with fewer than 100 normal reference cells, and iii) libraries from non-cancerous samples.
We calculated the total CNVs per cell using the feature output from the `i6` HMM by summing CNV calls across all chromosome arms.


#### Generating merged data

Merged objects are created with the `merge.nf` workflow within `scpca-nf`.
This workflow takes as input the processed `SingleCellExperiment` objects in a given ScPCA project output by `scpca-nf` and creates a single merged `SingleCellExperiment` object containing gene expression data and metadata from all libraries in that project.
The merged object includes both raw and normalized counts for all cells from all libraries.
Because the same reference index was used to quantify all single-cell and single-nuclei RNA-seq data, the set of genes is the same in the merged object and the individual objects.
Library-, cell- and gene-specific metadata from each of the processed `SingleCellExperiment` objects are also combined and stored in the merged object.
The `merge.nf` workflow does not perform batch correction or integration, so the counts in the merged object are not batch-corrected.

The top 2000 shared high-variance genes are identified from the merged counts matrix by modeling variance using `scran::modelGeneVar()` and specifying library IDs for the `block` argument.
These genes are used to calculate library-aware principal components with `batchelor::multiBatchPCA()` [@doi:10.1038/nbt.4091].
The top 50 principal components were selected and used to calculate UMAP embeddings for the merged object.

If any libraries included in the ScPCA project contain additional ADT data, the raw and normalized ADT data are also merged and stored in the `altExp` slot of the merged `SingleCellExperiment` object.
If the merged object contains an `altExp` with merged ADT data, two `AnnData` objects are exported to create separate RNA (`_rna.h5ad`) and ADT (`_adt.h5ad`) objects.

If any libraries in the ScPCA project are multiplexed and contain HTO data, no merged object is created due to potential ambiguity in identifying samples across multiplexed libraries.
Merged objects were not created for projects with more than 100 samples because of the computational resources required to work with them.

#### Converting SingleCellExperiment objects to AnnData objects

`zellkonverter::writeH5AD()` [@doi:10.18129/B9.bioc.zellkonverter] was used to convert `SingleCellExperiment` objects to `AnnData` format and export the objects as `.h5ad` files.
For any `SingleCellExperiment` objects containing an `altExp` (e.g., ADT data), the RNA and ADT data were exported and saved separately as RNA (`_rna.h5ad`) and ADT (`_adt.h5ad`) files.
Multiplexed libraries were not converted to `AnnData` objects, due to the potential for ambiguity in sample origin assignments.

All merged `SingleCellExperiment` objects were converted to `AnnData` objects and saved as `.h5ad` files.
If a merged `SingleCellExperiment` object contained any ADT data, the RNA and ADT data were exported and saved separately as RNA (`_rna.h5ad`) and ADT (`_adt.h5ad`) objects.
In contrast, if a merged `SingleCellExperiment` object contained HTO data due to the presence of any multiplexed libraries in the merged object, the HTO data was removed from the `SingleCellExperiment` object and not included in the exported `AnnData` object.

### QUANTIFICATION AND STATISTICAL REPORTING

Details regarding total sample and/or cell numbers and any statistical tests used can be found in the figure legends and figures. 
For Figure {@fig:fig4}, Figure {@fig:fig5}, Figure {@fig:figS4}, and Figure {@fig:figS5}, numbers in parentheses in the figure indicate total cell numbers.
For Figure {@fig:fig1}, Figure {@fig:fig6}, and Figure {@fig:figS7}, numbers in parenthesis in the figure indicate total sample numbers.

#### Benchmarking of `alevin-fry` and `cellranger count` performance 

Six libraries, three single-cell and three single-nuclei, were randomly selected and used to benchmark the performance of `alevin-fry` and `cellranger count`, results of which are shown in Figure {@fig:figS1}. 
Libraries were processed with `salmon alevin` v1.5.2 and `alevin-fry` v0.4.1 or `cellranger count` from Cell Ranger v6.1.2.
Results were generated using default parameters for single-cell libraries and use of the `--include_introns` flag to include intronic reads for single-nuclei libraries only. 
The Pearson correlation between mean gene expression across both methods is reported in Figure {@fig:figS1}B.

#### Analysis of bulk RNA-seq data

##### Data preparation

We identified solid tumor samples with both bulk and single-cell (or single-nuclei) RNA-seq data in the ScPCA Portal for analysis, with multiplexed samples excluded (N=105).
We removed low-quality samples based on visual inspection of quality control reports (N=8), leaving a total of 97 samples across five ScPCA projects for analysis.

For each project, we transformed and normalized bulk counts matrices for all samples using `DESeq2::rlog()` [@doi:10.1186/s13059-014-0550-8].
We obtained pseudobulk counts by summing raw single-cell counts for each sample, and similarly transformed each project's resulting counts matrix with `DESeq2::rlog()`.
We filtered out genes which were not observed in either the bulk or pseudobulk raw counts matrices before subsequent analysis.
For each project, we then used the `lme4` R package [@doi:10.18637/jss.v067.i01] to construct a linear model predicting bulk from pseudobulk counts considering a random effect for sample id: `bulk ~ pseudobulk + (1|sample_id)`.

##### Overrepresentation analysis

We next conducted overrepresentation analysis (ORA) to ascertain whether certain cell types might be overrepresented either modality (bulk vs. pseudobulk).
We specifically tested overrepresentation of the `PanglaoDB` cell type marker gene sets used for each project's respective `CellAssign` reference.

For input to the ORA, we summarized model residuals within each project by taking the median residual for each gene across samples and then transformed these summarized residuals into Z-scores.
We identified outlier genes as those with Z-scores greater than 2.5 (positive outliers) or less than -2.5 (negative outliers).
In this case, positive outliers represent genes with comparatively higher expression in the bulk modality, and negative outliers represent genes with comparatively higher expression in the single-cell modality.

For each set of cell type marker genes, we calculated two odds ratios representing whether genes were overrepresented in the positive outliers (enriched in bulk) or negative outliers (enriched in pseudobulk).
We calculated P-values for both the bulk and pseudobulk enrichment directions via permutation testing with 10,000 replicates.
We defined gene sets with significant overrepresentation as those with a false-discovery-rate-corrected P-value ≤ 0.05 [@doi:10.1111/j.2517-6161.1995.tb02031.x].

### ADDITIONAL RESOURCES 

Documentation for the ScPCA Portal can be found at <https://scpca.readthedocs.io>.

### KEY RESOURCES TABLE 

| **REAGENT or RESOURCE** | **SOURCE** | **IDENTIFIER** |
| ------------------- | ------ | ---------- |
| **Deposited Data** |  |  |
| Summarized gene expression data | This paper | https://scpca.alexslemonade.org |
| | |
| **Software and algorithms** |  |  |
| `scpca-nf` workflow used for processing all ScPCA Portal data | This paper | https://github.com/AlexsLemonade/scpca-nf [TODO: Link to zenodo] |
| ScPCA Portal code | This paper | https://github.com/AlexsLemonade/scpca-portal [@doi:10.5281/zenodo.20058961] |
| Benchmarking of tools used to build `scpca-nf` | This paper | https://github.com/AlexsLemonade/alsf-scpca [@doi:10.5281/zenodo.20044281] and https://github.com/AlexsLemonade/sc-data-integration [@doi:10.5281/zenodo.20044313] |
| Code for creating reference files for consensus cell type assignment | This paper | https://github.com/AlexsLemonade/OpenScPCA-analysis [@doi:10.5281/zenodo.18459136] |
| Workflow for assigning OpenScPCA project cell type annotations to ScPCA data | This paper | https://github.com/AlexsLemonade/OpenScPCA-nf [@doi:10.5281/zenodo.20056054] |
| `ScPCAr` package for programmatically downloading from the Portal | This paper | https://github.com/AlexsLemonade/ScPCAr [@doi:10.5281/zenodo.20044462]|
| Code for underlying figures and analyses | This paper | https://github.com/AlexsLemonade/scpca-paper-figures [TODO: LInk to zenodo] |
| Nextflow | Tomasso et al. [@doi:10.1038/nbt.3820] | https://github.com/nextflow-io/nextflow/tree/master | 
| `salmon` | Patro et al. [@doi:10.1038/nmeth.4197] | https://anaconda.org/channels/bioconda/packages/salmon/overview | 
| `alevin-fry` | He et al. [@doi:10.1038/s41592-022-01408-3] | https://anaconda.org/channels/bioconda/packages/alevin-fry/overview | 
| Space Ranger | 10x Genomics | https://www.10xgenomics.com/support/software/space-ranger/latest | 
| `SingleCellExperiment` | Amezquita et al. [@doi:10.1038/s41592-019-0654-x] | https://bioconductor.org/packages/release/bioc/html/SingleCellExperiment.html |
| `anndata` | Virshup et al. [@doi:10.21105/joss.04371] | https://pypi.org/project/scvi-tools/ |
| `DropletUtils` | Lun et al. [@doi:0.1186/s13059-019-1662-y.]; Griffiths et al. [@doi:10.1038/s41467-018-05083-x] | https://bioconductor.org/packages/release/bioc/html/DropletUtils.html | 
| `miQC` | Hippen et al. [@doi:10.1371/journal.pcbi.1009290] | https://bioconductor.org/packages/release/bioc/html/miQC.html | 
| `scDblFinder` | Germain et al. [@doi:10.12688/f1000research.73600.2] | https://bioconductor.org/packages/release/bioc/html/scDblFinder.html | 
| `scuttle` | McCarthy et al. [@doi:10.1093/bioinformatics/btw777] | https://bioconductor.org/packages/release/bioc/html/scuttle.html |
| `scran` | Lun et al. [@doi:10.12688/f1000research.9501.2] | https://bioconductor.org/packages/release/bioc/html/scran.html |
| `scater` | McCarthy et al. [@doi:10.1093/bioinformatics/btw777] | https://bioconductor.org/packages/release/bioc/html/scater.html | 
| `Seurat` | Hao et al. [@doi:10.1038/s41587-023-01767-y] | https://satijalab.org/seurat/ | 
| `vireo` | Huang et al. [@doi:10.1186/s13059-019-1865-2]; Weber et al. [@doi:10.1093/gigascience/giab062] | https://github.com/single-cell-genetics/vireo | 
| `batchelor` | Lun et al. [@doi:10.1038/nbt.4091] | https://bioconductor.org/packages/release/bioc/html/batchelor.html | 
| `SingleR` | Aran et al. [@doi:10.1038/s41590-018-0276-y] | https://bioconductor.org/packages/release/bioc/html/SingleR.html | 
| `celldex` | Aran et al. [@doi:10.1038/s41590-018-0276-y] | https://bioconductor.org/packages/release/data/experiment/html/celldex.html |
| `CellAssign` | Zhang et al. [@doi:10.1038/s41592-019-0529-1] | https://docs.scvi-tools.org/en/stable/installation.html | 
| `SCimilarity` | Heimberg et al. [@doi:10.1038/s41586-024-08411-y] | https://genentech.github.io/scimilarity/index.html |
| `inferCNV` | inferCNV of the Trinity CTAT Project [@url:https://github.com/broadinstitute/infercnv] | https://www.bioconductor.org/packages/release/bioc/html/infercnv.html |
| `zellkonverter` | Zappia et al. [@doi:10.18129/B9.bioc.zellkonverter] | https://bioconductor.org/packages/release/bioc/html/zellkonverter.html | 
| `DESeq2` | Love et al. [@doi:10.1186/s13059-014-0550-8] | https://bioconductor.org/packages/release/bioc/html/DESeq2.html | 
| `lme4` | Bates et al. [@doi:10.18637/jss.v067.i01] | https://cran.r-project.org/web/packages/lme4/index.html | 
| **Other** | | | 
| HsapDv | Ontology Lookup Service [@url:https://www.ebi.ac.uk/ols4/ontologies/hsapdv] | https://www.ebi.ac.uk/ols4/ontologies/hsapdv | 
| PATO | Gkoutos et al. [@doi:10.1093/bib/bbx035] |https://www.ebi.ac.uk/ols4/ontologies/pato | 
| NCBI Taxonomy | Schoch et al. [@doi:10.1093/database/baaa062] | https://www.ncbi.nlm.nih.gov/taxonomy | 
| Mondo | Vasilevsky et al. [@doi:10.1093/genetics/iyaf215] | https://www.ebi.ac.uk/ols4/ontologies/mondo |
| UBERON | Haendel et al. [@doi:10.1186/2041-1480-5-21] | https://www.ebi.ac.uk/ols4/ontologies/uberon | 
| Hancestro | Morales et al. [@doi:10.1186/s13059-018-1396-2] | https://www.ebi.ac.uk/ols4/ontologies/hancestro |
| Cell Ontology | Bard et al. [@doi:10.1186/gb-2005-6-2-r21]; Meehan et al. [@doi:10.1186/1471-2105-12-6]; Diehl et al. [@doi:10.1186/s13326-016-0088-7]; Tan et al. [@doi:10.1038/s41597-026-07173-8] | https://www.ebi.ac.uk/ols4/ontologies/cl | 
| Blueprint and ENCODE | Martens et al. [@doi:10.3324/haematol.2013.094243]; The ENCODE Consortium [@doi:10.1038/nature11247] | https://rdrr.io/github/LTLA/celldex/man/BlueprintEncodeData.html |
| PanglaoDB | [@doi:10.1093/database/baz046] | https://panglaodb.se/ | 
| CellMarker 2.0 | [@doi:10.1093/nar/gkac947] | http://117.50.127.228/CellMarker/ | 



## Discussion

The ScPCA Portal is a downloadable collection of uniformly processed, summarized single-cell and single-nuclei RNA-seq data and de-identified metadata from pediatric tumor samples.
The Portal includes over 700 samples from 55 tumor types, making this the most comprehensive collection of publicly available pediatric tumor single-cell transcriptomic datasets to our knowledge.
Users can browse and search the Portal via an intuitive web interface and explore visualizations of individual samples via a UCSC Cell Browser interface [@doi:10.1093/bioinformatics/btab503].
Summarized data are available at three different processing stages (unfiltered, filtered, or processed objects) allowing users to 
start from a processed object or perform their own processing, e.g. filtering and normalization.
Processed objects contain normalized gene expression data, reduced dimensionality results from PCA and UMAP, cell type annotations, and CNV inference results.
Standardized metadata, containing human-readable values for all fields and ontology term identifiers for a subset of fields, is also provided for all samples.
Every library includes a quality control report for assessing data quality.
These processed results and metadata allow researchers to save time by moving directly to downstream analyses, such as identifying marker genes or exploring genes of interest.

Data on the Portal is available as either `SingleCellExperiment` or `AnnData` objects for ease of use within R or Python (i.e., `Bioconductor` or `scverse`, respectively) environments.
The `AnnData` objects also allow users to integrate ScPCA data with data and tools on other platforms.
In particular, our `AnnData` objects are designed to be mostly compliant with the requirements of CZI CELLxGENE [@doi:10.1101/2021.04.05.438318; @doi:10.1101/2023.10.30.563174; @{https://cellxgene.cziscience.com/}], and these objects can also be used with Kana [@doi:10.1101/2022.03.02.482701; @{https://www.kanaverse.org/kana/}].
Data can be downloaded both via the Portal web interface and programmatically using the `ScPCAr` R package, which is a wrapper for the ScPCA Portal API (<https://api.scpca.alexslemonade.org/docs/>).


Cell type annotations are also available from three automated methods: `SingleR`, `CellAssign`, and `SCimilarity`.
The first two approaches use publicly available references, while the third uses a foundation model to label cells.
These labels are used to construct ontology-aware consensus cell type labels, which provide a harmonized labeling scheme across samples.

Many samples on the Portal have additional sequencing data which can also be downloaded, including ADT data from CITE-seq, cell hashing data, bulk RNA-seq, or spatial transcriptomics.
These modalities can facilitate expanded analyses.
For example, ADT data can help label unknown cell types and correlate RNA to protein expression [@doi:10.1038/nmeth.4380], and spatial transcriptomics data can be leveraged to gain more insights about distribution of cell types in the tissue [@doi:10.1038/s41467-023-37168-7].
Similarly, users can gain more insight from bulk RNA-seq data available on the Portal by integrating with scRNA-seq data from the same sample [@doi:10.1093/bioinformatics/bty019; @doi:10.1186/s13059-023-03016-6].
The scRNA-seq data available on the Portal can also be used to deconvolute existing bulk RNA-seq datasets.
The ScPCA Portal therefore enables multimodal comparisons that reveal biological and/or technical signals that would otherwise not be apparent from one sequencing modality alone.

We also introduced our open-source and efficient workflow for uniformly processing datasets available on the Portal, `scpca-nf`, which is available to the entire research community.
In one command, `scpca-nf` can process raw data from various sequencing types, turning FASTQ files into processed `SingleCellExperiment` or `AnnData` objects ready for downstream analyses.
Using Nextflow as the framework for `scpca-nf` with container images for each process makes the workflow modular and portable.
Processed output from running `scpca-nf` on samples from pediatric tumors, cell lines, or other model organisms is eligible for submission to the ScPCA Portal, enabling us to continue to grow the Portal, improving its utility to the research community.

Portal data can also support re-analysis of existing pediatric cancer datasets with bulk RNA-seq, such as the Pediatric Brain Tumor Atlas [@doi:10.1016/j.neo.2022.100846; @doi:10.1016/j.xgen.2023.100340], allowing researchers to glean more insight from published data without obtaining additional samples.
Ultimately, the ScPCA Portal will save researchers time and money, advancing pediatric cancer research.

### Limitations of this study

We note several limitations of the current ScPCA Portal and `scpca-nf` workflow.
First, labeling tumor cells is challenging as neither `SingleR` nor `CellAssign` references include them.
We mitigate this in several ways.
As references are biased towards normal cells, cells without a consensus cell type annotation are likely to be malignant.
We provide CNV estimates for roughly half of Portal libraries, and together with consensus cell types, these can help identify tumor cells, particularly for diagnoses with common copy number alterations such as neuroblastoma (Figure {@fig:fig5}B-D) and osteosarcoma.
We are also augmenting projects through the ongoing OpenScPCA project [@url:https://openscpca.readthedocs.io], which provides robust, fully open-source annotations that formally distinguish normal from tumor cells and will continue to expand across Portal projects.

Second, although we provide merged objects for each project, we do not provide integrated or batch-corrected objects, as the appropriate correction approach depends on the scientific question and is best left to the user.

Third, while the Portal features several modalities beyond single-cell and single-nuclei RNA-seq, not all modalities are currently represented — for example, epigenomic modalities such as scATAC-seq.
Our modular Nextflow workflow is flexibly designed to accommodate additional modalities as the Portal expands.

## Acknowledgments

We thank the data generators and submitters of the Single-cell Pediatric Cancer Atlas.
We also thank Anna Greene for her role in constructing the Single-cell Pediatric Cancer Atlas funding opportunity.

This work was funded through the Alex's Lemonade Stand Foundation Childhood Cancer Data Lab and Childhood Cancer Data Lab Postdoctoral Fellowship (SMF).

## Author Contributions

|Author|Contributions|
|---|---|
|Allegra G. Hawkins|Methodology, Software, Investigation, Validation, Formal analysis, Data curation, Writing - Original Draft, Writing - Review & Editing, Visualization|
|Joshua A. Shapiro|Methodology, Software, Investigation, Validation, Formal analysis, Resources, Data curation, Writing - Original Draft, Writing - Review & Editing, Visualization|
|Stephanie J. Spielman|Methodology, Software, Investigation, Validation, Formal analysis, Data curation, Writing - Original Draft, Writing - Review & Editing, Visualization|
|David S. Mejia|Methodology, Software, Validation, Data curation, Writing - Review & Editing, Resources|
|Deepashree Venkatesh Prasad|Methodology, Software, Validation, Visualization, Writing - Review & Editing|
|Nozomi Ichihara|Methodology, Software, Writing - Review & Editing|
|Arkadii Yakovets|Methodology, Software, Validation, Data curation, Resources, Writing - Review & Editing|
|Avrohom M. Gottlieb|Methodology, Software, Validation, Data curation, Writing - Review & Editing, Resources|
|Kurt G. Wheeler|Methodology, Software, Validation, Data curation, Resources, Writing - Review & Editing|
|Chante J. Bethell|Software, Validation, Writing - Review & Editing|
|Steven M. Foltz|Writing - Review & Editing|
|Jennifer O'Malley|Data curation, Supervision, Writing - Review & Editing|
|Casey S. Greene|Conceptualization, Project administration, Supervision, Writing - Review & Editing|
|Jaclyn N. Taroni|Conceptualization, Methodology, Investigation, Validation, Data curation, Writing - Original Draft, Writing - Review & Editing, Visualization, Supervision, Project administration|

## Declarations of Interest

AGH, JAS, SJS, DSM, DVP, NI, AY, AMG, KGW, CJB, JO, and JNT are or were employees of Alex's Lemonade Stand Foundation, a sponsor of this research.


## Figure Titles and Legends {.page_break_before}

<!-- Figure 1 -->
![**Overview of ScPCA Portal contents.**](https://raw.githubusercontent.com/AlexsLemonade/scpca-paper-figures/v0.2.2/figures/compiled_figures/pngs/figure_1.png?sanitize=true){#fig:fig1 tag="1" width="7in"}

A. Barplots showing sample counts across four main cancer groupings in the ScPCA Portal with the total number of samples per cancer type displayed.
Bars are colored by the number of samples with the indicated disease timing.

B. Barplot showing sample counts across modalities present in the ScPCA Portal.
All single-cell or single-nuclei samples in the Portal are shown under the "All Samples" heading, a subset of which also have additional modalities as shown under the "Samples with additional modalities" heading.
As indicated, sample suspensions are either single-cell or single-nuclei.
For example, 75 single-cell samples and 101 single-nuclei samples have accompanying bulk RNA-seq data.
Note that two samples were sequenced with both single-cell and single-nuclei suspensions.
Samples with only bulk RNA-seq or spatial transcriptomics modalities are not shown.

C. Example of a project card as displayed on the "Browse" page of the ScPCA Portal and a "Visualize" view for a library within that project, colored by consensus cell type annotation.
This project card and visualized sample are from project `SCPCP000004` [@doi:10.1101/2024.01.07.574538; @doi:10.1186/s13059-024-03309-4].
Project cards include information about the number of samples, technologies and modalities, additional sample metadata information, submitter-provided diagnoses, and a submitter-provided abstract.
Where available, submitter-provided citation information and other databases hosting this data are also provided.
The visualization employs the UCSC Cell Browser [@doi:10.1093/bioinformatics/btab503], enabling interactive exploration with user-selectable coloring options for cell types, gene-level expression, and other per-cell annotations created by `scpca-nf`.
<br><br><br><br><br>


<!-- Figure 2 -->
![**Overview of the `scpca-nf` workflow and download file structures.**](https://raw.githubusercontent.com/AlexsLemonade/scpca-paper-figures/v0.2.2/figures/compiled_figures/pngs/figure_2.png?sanitize=true){#fig:fig2 tag="2" width="7in"}

A. Overview of `scpca-nf`, the primary workflow for processing single-cell/nuclei RNA-seq data for the ScPCA Portal.
Mapping is first performed with `alevin-fry` to generate a gene-by-cell count matrix, which is read into `R` and converted into a `SingleCellExperiment` (`SCE`) object (`Unfiltered SCE Object`).
Next, empty droplets are filtered out (`Filtered SCE Object`).
The filtered object undergoes additional post-processing, including removing low-quality cells, normalizing counts, and performing dimension reduction with principal components analysis and UMAP.
The object undergoes cell type annotation and CNV inference (`Processed SCE Object`).
A summary QC report and a supplemental cell type report are prepared and exported.
Finally, all `SCE` files are converted to `AnnData` format and exported.

Panels B-G show abbreviated versions of figures that appear in the summary QC report, shown here for `SCPCL000001` [@doi:10.1093/neuonc/noad207], as follows:

B. The total UMI count for each cell in the `Unfiltered SCE Object`, ordered by rank.
Points are colored by the percentage of cells that pass the empty droplets filter.

C. The number of genes detected in each cell passing the empty droplets filter against the total UMI count.
Points are colored by the percentage of mitochondrial reads in the cell.

D. `miQC` model diagnostic plot showing the percent of mitochondrial reads in each cell against the number of genes detected in the `Filtered SCE Object`.
Points are colored by the probability that the cell is compromised as determined by `miQC`.

E. The percent of mitochondrial reads in each cell against the number of genes detected in each cell.
Points are colored by whether the cell was kept or removed, as determined by both `miQC` and a minimum unique gene count cutoff, prior to normalization and dimensionality reduction.

F. UMAP of log-normalized RNA expression colored by the number of genes detected.

G. UMAP of log-normalized RNA expression for the top four most variable genes, colored by the given gene's expression.
In the actual summary QC report, the top 12 most highly variable genes are shown.

H. File download structure for an ScPCA Portal project download in `SingleCellExperiment` (`SCE`) format.
The download folder is named according to the project ID, data format, and the date it was downloaded.
Download folders contain a folder for all single-cell data, `_single-cell`.
Here, each sample ID has a dedicated folder containing the three processing levels of the expression data, the summary QC report, and cell type report all named according to the ScPCA library ID.
The `single-cell_metadata.tsv` file contains sample metadata for all samples included in the download.
The `README.md` file provides information about the contents of each download file, additional contact and citation information, and terms of use for data downloaded from the ScPCA Portal.
The folder `_bulk` – only present for projects with bulk RNA-Seq data – contains a gene-by-sample matrix of counts quantified by `salmon` and associated metadata for samples with bulk RNA-Seq data.

I. File download structure for an ScPCA Portal merged project download in `SCE` format.
As in panel H, the download folder is named by project ID, format, and date.
Download folders contain a folder for all single-cell data, `_single-cell_merged`, with a single merged object containing all samples in the given project and a summary report detailing the merged object's contents.
Summary QC and cell type reports for each library are provided in the `individual_reports` folder arranged by their library ID.
As in panel (H), additional files `single-cell_metadata.tsv`, `_bulk_quant.tsv`, `_bulk_metadata.tsv`, and `README.md` are also included.
<br><br>


<!-- Figure 3 -->
![**Consensus cell type annotation in `scpca-nf`.**](https://raw.githubusercontent.com/AlexsLemonade/scpca-paper-figures/v0.2.2/figures/compiled_figures/pngs/figure_3.png?sanitize=true){#fig:fig3 tag="3" width="7in"}

A. Expanded view of cell type annotation process within `scpca-nf`, as introduced in Figure {@fig:fig2}A.
Cell type annotation is performed on the `Processed SCE Object`.
`SingleR` [@doi:10.1038/s41590-018-0276-y] annotation uses a `celldex` [@doi:10.1038/s41590-018-0276-y] reference dataset with ontology labels, `CellAssign`[@doi:10.1038/s41592-019-0529-1] annotation uses a list of marker genes compiled from `PanglaoDB` [@doi:10.1093/database/baz046], and `SCimilarity` [@doi:10.1038/s41586-024-08411-y] annotation uses the `SCimilarity` foundation model.
These cell typing results, along with consensus cell type annotations, are then added to the `Processed SCE Object`.
A cell type summary report with information about reference sources, comparisons among cell type annotation methods, and diagnostic plots is created.
Note that cell type annotations are also included in the `Processed AnnData Object` (Figure {@fig:fig2}A).

B. Diagram of ontology-aware consensus cell type annotation performed in `scpca-nf`, using T cell annotation as an example.
The numbers in parentheses indicate the number of descendants for each cell type in the Cell Ontology.
Pairwise comparisons are made among annotations, and the consensus cell type is the latest common ancestor in Cell Ontology with the fewest descendants, indicated by the black check mark.

C. Example heatmap (`SCPCL000001`) as shown in the cell type summary report comparing the consensus cell type annotations to automated annotations assigned by `SingleR`, `CellAssign`, and `SCimilarity`.
Heatmap cells are colored by the Jaccard similarity index.
A value of 1 indicates complete overlap and 0 indicates no overlap between cells annotated with each label.
This figure shows only the top seven consensus cell type annotations with at least three cells, but the heatmap in the cell type summary report shows all cell types.
<br><br>


<!-- Figure 4 -->
![**Consensus cell type annotations in brain and CNS tumors.**](https://raw.githubusercontent.com/AlexsLemonade/scpca-paper-figures/v0.2.2/figures/compiled_figures/pngs/figure_4.png?sanitize=true){#fig:fig4 tag="4" width="7in"}

A. Dot plot showing expression of cell-type-specific marker genes across all libraries from brain and central nervous system (CNS) tumors, excluding multiplexed libraries.
Expression is shown for each broad cell type annotation, each of which represents a collection of similar consensus cell type annotations.
The y-axis displays broad consensus cell types.
The x-axis displays marker genes, determined by `CellMarker 2.0` [@doi:10.1093/nar/gkac947], used to validate cell types in the top annotation bar.
Dots are colored by mean gene expression across libraries and sized proportionally to the percent of libraries they are observed in, out of all cells with the same broad cell type annotation in brain and CNS tumor libraries.
Up to 10 marker genes are shown per broad cell type.
Only broad cell type annotations present in at least 50 cells across samples in the given diagnosis group are shown.

B. Barplot showing the percentage of each broad consensus cell type annotation across brain and CNS tumors libraries, separated into high-grade (top panel) and low-grade (bottom panel) glioma diagnoses for non-multiplexed libraries from patient tissue samples.

C. Barplot showing all consensus cell types classified as immune cells across brain and CNS tumor libraries, separated into high-grade (top panel) and low-grade (bottom panel) glioma diagnoses for non-multiplexed libraries.
The percentage of immune cells classified as the indicated consensus cell type is shown.
Only libraries comprised of at least 1\% immune cells, based on consensus cell type annotations, are shown.
Specific consensus cell types for myeloid and lymphocyte immune cells are shown, with all other consensus immune cell types included in "other."
Myeloid or lymphocyte immune cell types with fewer than 1000 cells across all libraries are included in "other."

D. Dot plot as in panel A, but restricted to immune cells across all non-multiplexed libraries from brain and CNS tumors and showing consensus rather than broad cell types showing expression of cell-type-specific marker genes, considering only immune cells.
Only broad cell type annotations present in at least 50 cells across samples in the given diagnosis group are shown.
Cell types without associated marker genes in `CellMarker 2.0` are excluded, including `lymphocyte of B lineage`, `mature T cell`, `mature alpha-beta T cell`, `alpha-beta T cell`, `myeloid leukocyte`, and `tissue-resident macrophage`.
<br><br>

<!-- Figure 5 -->
![**Cell type annotation and CNV inference on neuroblastoma samples.**](https://raw.githubusercontent.com/AlexsLemonade/scpca-paper-figures/v0.2.2/figures/compiled_figures/pngs/figure_5.png?sanitize=true){#fig:fig5 tag="5" width="7in"}

A-B. UMAP of all libraries in the neuroblastoma-only ScPCA Project `SCPCP000004` (N = 42).
The UMAP was constructed from the merged `SCPCP000004` object with equal library weighting, but no batch correction was performed.
Panel A highlights cell type annotations made with the OpenScPCA Project, collapsed into broad annotation groups.
Panel B highlights total per-cell CNV events calculated as the sum of chromosome arms with a CNV event, as estimated by the `i6` HMM in `InferCNV` [@url:https://github.com/broadinstitute/inferCNV].
Gray cells in panel B represent libraries excluded from `InferCNV` inference due to insufficient normal cells for defining the `InferCNV` reference baseline.

C. Heatmap displaying per-cell CNV events across chromosomes with canonical neuroblastoma alterations [@doi:10.1038/nrdp.2016.78; @doi:10.1016/j.celrep.2024.114804; @doi:10.1158/2159-8290.CD-14-0622] for a single library, `SCPCL000130`.
Each cell in `SCPCL000130` is represented by two adjacent rows, the first indicating copy-number gain and the second indicating copy-number loss.
The heatmap is grouped by chromosome arm and OpenScPCA Project cell type annotation, where "normal" cells comprise all non-malignant cells.

D. Ridge plot from the summary QC report (`SCPCL000130`) of per-cell total CNV distributions across the top seven consensus cell type annotations.
Other consensus cell types are shown in the "all remaining cell types" category.


<!-- Figure 6 -->
![**Comparison of bulk and pseudobulk modalities.**](https://raw.githubusercontent.com/AlexsLemonade/scpca-paper-figures/v0.2.2/figures/compiled_figures/pngs/figure_6.png?sanitize=true){#fig:fig6 tag="6" width="7in"}

A. Scatter plots colored by point density of `DESeq2`-transformed and normalized bulk RNA-seq expression compared to pseudobulk expression from single-cell/nuclei RNA-seq, with a regression line shown.
Samples with RNA-seq for both bulk and single-cell/nuclei modalities, excluding multiplexed samples, from ScPCA projects of brain and CNS tumors are shown, with sample counts in parentheses.

B. Odds ratios, which indicate overrepresentation of cell-type marker genes in bulk relative to single-cell/nuclei RNA-seq, from overrepresentation analysis for the same samples shown in panel A, colored by FDR-corrected significance.
68 cell types were evaluated for each project.

## Supplementary Figures and Tables {.page_break_before}

<!-- Table S1 -->
**Table S1. Overview of ScPCA Portal Datasets.**
This table provides descriptions and sample and library counts for projects in the ScPCA Portal.

`scpca_project_id`: ScPCA project unique identifier.
`Diagnosis group`: Diagnosis group as shown in Figure {@fig:fig1}A.
`Diagnoses`: Full set of diagnoses for all samples in the project.
`Total number of samples (S)`: Number of samples in the project.
`Total number of libraries (L)`: Number of libraries in the project.
Due to additional sequencing modalities and/or multiplexing, projects may have more libraries than samples.
All remaining columns give the number of libraries (as designated with `(L)`) with the given suspension type, 10x kit version, or additional modality.
<br><br>

<!-- Table S2 -->
**Table S2. Summary of references used for cell type annotation with `CellAssign`.**
This table summarizes the references used for assigning cell types using `CellAssign`.
References were built using all cell types from a set of organs in `PanglaoDB`'s marker gene list.

`scpca_project_id`: ScPCA project unique identifier.
`Diagnoses`: Full set of diagnoses for all samples in the project.
`ScPCA reference name`: Custom reference name.
`PanglaoDB organs included in reference`: Organs from `PanglaoDB` included in the reference.
Marker genes for all cell types in each organ were included.
<br><br>

<!-- Figure S1 -->
![**Results from benchmarking `alevin-fry` and `cellranger count` performance.**](https://raw.githubusercontent.com/AlexsLemonade/scpca-paper-figures/v0.2.2/figures/compiled_figures/pngs/figure_s1.png?sanitize=true){#fig:figS1 tag="S1" width="7in"}

Panels compare metrics for six ScPCA libraries (three single-cell and three single-nuclei), obtained from processing with `salmon alevin` and `alevin-fry` or `cellranger count`.
Results were generated with CellRanger v6.1.2 using default parameters for single-cell libraries and the `--include_introns` flag to include intronic reads for single-nuclei libraries only.
Libraries were processed with `salmon alevin` v1.5.2 and `alevin-fry` v0.4.1 using an index containing both spliced and unspliced cDNA (see Methods).
Libraries used for benchmarking were randomly chosen.

A. Runtime in minutes (top row) and peak memory in GB (bottom row) for libraries processed with both platforms.
Processing with `alevin-fry` was consistently faster and more memory-efficient than processing with `cellranger count`.

Panels B-D show only cells present in both `alevin-fry` and `cellranger count` outputs.

B. Comparison of mean gene expression values for libraries processed with both platforms, shown on a log-scale.
Each point is a gene, and only genes detected in at least 5 cells are shown.
$R^2$ values shown in the top left corner of each panel reflect broad agreement in mean gene expression values between platforms.

C. Comparison of log total UMI counts for libraries processed with both platforms.
The total UMI count per cell between platforms broadly agree, although `alevin-fry` returned slightly higher values for certain single-cell libraries.

D. Comparison of log total genes detected per cell for libraries processed with both platforms.
The total number of genes detected per cell between platforms broadly agree, although `alevin-fry` returned slightly higher values for certain single-cell libraries.
<br><br>

<!-- Figure S2 -->
![**Processing additional single-cell modalities in `scpca-nf`.**](https://raw.githubusercontent.com/AlexsLemonade/scpca-paper-figures/v0.2.2/figures/compiled_figures/pngs/figure_s2.png?sanitize=true){#fig:figS2 tag="S2" width="7in"}

A. Overview of the `scpca-nf` workflow for processing libraries with CITE-seq or antibody-derived tag (ADT) data.
The workflow mirrors that shown in Figure {@fig:fig2}A with several differences accounting for the presence of ADT data.
First, both an RNA and ADT FASTQ file are required as input to `alevin-fry`, along with a TSV file containing information about ADT barcodes.
Second, during post-processing, statistics are calculated to filter cells based on ADT counts, but the filter is not applied.
ADT counts are also normalized and included in the `Processed SCE Object`.
Third, the summary QC report will include a `CITE-seq` section with additional information about ADT-level processing.
Fourth, the workflow exports `SCE` objects containing both RNA and ADT results, while separate `AnnData` objects for RNA and ADT are exported.

Panels B-D show example figures that appear in the CITE-seq section of the summary QC report, shown here for `SCPCL000290`.

B. The percent of mitochondrial reads in each cell against the number of genes detected in each cell.
The panel labeled "Keep" displays cells that are retained based on both RNA and ADT counts.
Other panels display cells that are filtered based only on the given type of counts.

C. Density plots of the log-normalized ADT counts for the library's four most variable ADTs.

D. UMAP log-normalized RNA expression values.
Cells are colored by expression of the given highly-variable ADT.

E. Overview of the `scpca-nf` workflow for multiplexed libraries.
The workflow mirrors that shown in Figure {@fig:fig2}A with several differences accounting for the presence of multiplexed data.
First, both an RNA and HTO FASTQ file are required as input to `alevin-fry`, along with a TSV file providing information about library pools.
Second, in parallel, the RNA FASTQ file, the HTO FASTQ file, and, if available, a corresponding Bulk RNA FASTQ file for each sample present in the multiplexed library are provided to a demultiplexing subprocess.
The workflow calculates demultiplexing results based on HTO counts, as well as genetic demultiplexing results if the library has corresponding bulk RNA-seq data.
Demultiplexing results are stored in all exported `SCE` objects versions, but libraries themselves are not demultiplexed.
Third, only `SCE`, not `AnnData`, files are provided for multiplexed libraries.
<br><br>

<!-- Figure S3 -->
![**Processing other sequencing modalities and merging objects with `scpca-nf`.**](https://raw.githubusercontent.com/AlexsLemonade/scpca-paper-figures/v0.2.2/figures/compiled_figures/pngs/figure_s3.png?sanitize=true){#fig:figS3 tag="S3" width="7in"}

A. Overview of the bulk RNA-Seq workflow.
Reads are trimmed using `fastp`, and `salmon` is used to map reads and quantify counts.
Quantified expression files are grouped by project and exported as a sample-by-gene count matrix in TSV format.

B. Overview of the spatial transcriptomics workflow.
The FASTQ file and tissue and/or CytAssist image for a given library are input to `spaceranger`.
`spaceranger` results are returned without any further processing.

C. Overview of the merged workflow.
Processed `SCE` objects in a given project are merged into a single object, including ADT counts from CITE-seq data if present, and a merged summary report is generated.
Merged objects are provided in either `SCE` or `AnnData` format.

D. Example of UMAPs as shown in the merged summary report.
Cells from the library of interest are in red, and cells from other libraries are in gray.
The UMAP was constructed from the merged object with equal library weighting, but no batch correction was performed.
The libraries pictured are a subset of libraries in the ScPCA project `SCPCP000003`.
For this figure specifically, the merged UMAP was constructed from these four libraries only, but the merged object and summary report on the ScPCA Portal for `SCPCP000003` contain all of this project's libraries.
<br><br>

<!--Figure S4-->
![**Ontology-aware consensus cell type assignment provides harmonized labels for cells.**](https://raw.githubusercontent.com/AlexsLemonade/scpca-paper-figures/v0.2.2/figures/compiled_figures/pngs/figure_s4.png?sanitize=true){#fig:figS4 tag="S4" width="7in"}

A. UMAP highlighting cells annotated as types of T cells with `SingleR`, `CellAssign`, `SCimilarity` as well as the associated consensus cell types for the library `SCPCL000049`.
All other cells are shown in gray.
The top three T cell types are shown for each method, with remaining T cell types combined in "other T cells."

B. UMAP showing the top seven consensus cell types in `SCPCL0000049`.
Other consensus cell types are included in the "all remaining cell types" category.

C. UMAP showing total per-cell CNV events, calculated by summing the number of chromosome arms with a CNV event as estimated by the `i6` HMM in `InferCNV`, [@url:https://github.com/broadinstitute/inferCNV], for `SCPCL0000049`.
<br><br>


<!-- Figure S5 -->
![**Consensus cell type annotation gene expression in other diagnosis groups.**](https://raw.githubusercontent.com/AlexsLemonade/scpca-paper-figures/v0.2.2/figures/compiled_figures/pngs/figure_s5.png?sanitize=true){#fig:figS5 tag="S5" width="9in"}

Dot plots showing expression of cell-type-specific marker genes across libraries from Leukemia (A), Sarcoma (B), and Other solid tumors (C) diagnosis groups.
Expression is shown for each broad cell type annotation.
The y-axis displays broad consensus cell types.
The x-axis displays marker genes, determined by `CellMarker 2.0` [@doi:10.1093/nar/gkac947], used to validate cell types in the top annotation bar.
Dots are colored by mean gene expression across libraries and sized proportionally to the percent of libraries they are observed in, out of all cells with the same broad cell type annotation in the given diagnosis.
Up to 10 marker genes are shown per broad cell type.
Only broad cell type annotations present in at least 50 cells across samples in the given diagnosis group are shown.
Cell types without associated marker genes in `CellMarker 2.0` are excluded, including `pigment cell` for Sarcoma (B) and `pigment cell` and `kidney cell` for Other solid tumors (C).
<br><br>

<!-- Figure S6 -->
![**Consensus cell type annotation distributions in other diagnosis groups.**](https://raw.githubusercontent.com/AlexsLemonade/scpca-paper-figures/v0.2.2/figures/compiled_figures/pngs/figure_s6.png?sanitize=true){#fig:figS6 tag="S6" width="7in"}

Barplots of the percentage of cells annotated as each broad consensus cell type annotation across all libraries from Leukemia (A), Sarcoma (B), and Other solid tumors (C) diagnosis groups, specifically for non-multiplexed libraries from patient tissue samples
Libraries are grouped by diagnosis in each panel.
Each column represents the distribution of cell types within a single library.
<br><br>

<!-- Figure S7 -->
![**Comparison of bulk and pseudobulk modalities for additional projects.**](https://raw.githubusercontent.com/AlexsLemonade/scpca-paper-figures/v0.2.2/figures/compiled_figures/pngs/figure_s7.png?sanitize=true){#fig:figS7 tag="S7" width="7in"}

A. Scatter plots colored by point density of `DESeq2`-transformed and normalized bulk RNA-seq expression compared to pseudobulk expression from single-nuclei RNA-seq, with a regression line shown.
Projects with RNA-seq for both bulk and single-cell/nuclei modalities that are not displayed in Figure {@fig:fig6}A are shown, with sample counts in parentheses.
All samples shown here are single-nuclei libraries.

B. Odds ratios, which indicate overrepresentation of cell-type marker genes in bulk relative to single-cell/nuclei RNA-seq, from overrepresentation analysis for the same samples shown in panel A, colored by FDR-corrected significance.
44 cell types were evaluated for project `SCPCP000006`, and 50 cell types were evaluated for project `SCPCP000017`.


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>

