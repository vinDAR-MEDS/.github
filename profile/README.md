# Mapping Missing Vines: Assessing the Health of Vineyards Using HD LIDAR Data (vinDAR)

<img src="https://github.com/user-attachments/assets/94ed4308-d844-4f9a-968a-bfde1b4b6e61" alt="grape vines" width="450"/>

# Table of Contents

[Project Purpose](#Project-Purpose)

[Project Description](#Project-Description)

[Data Sources](#Data-Sources)

[Abstract](#Abstract)

[Technical Documentation](#Technical-Documentation)

[Authors and Team](#Authors-and-Team)

[Client](#Client)

[Acknoledgements](#Acknoledgements)

[License](#License)

[How to Use This Organization](#How-to-Use-This-Organization)


## Project Purpose

France’s vineyards are economically and culturally significant, yet they face increasing pressures from climate change and grapevine diseases, which contribute to long-term decline (Schultz, 2016; Ashenfelter & Storchmann, 2016; Bertsch et al., 2013). This project aims to develop a quantitative, spatially explicit approach to detect and quantify missing vines within vineyard parcels using publicly available geospatial data from the French National Institute of Geographic and Forest Information (IGN). We will use high-resolution LiDAR HD data and parcel-level agricultural data, building on established airborne laser scanning techniques for vegetation analysis (Roussel et al., 2020) and existing research on vineyard disease, economic impacts, and climate adaptation (Gramaje et al., 2018; Kaplan et al., 2016; Merot et al., 2025). While the initial focus will be on the Rhône Valley region of France, the methodology is designed to be reproducible and scalable, enabling extension to other major wine-producing regions. The project will deliver three main outcomes: a validated method for estimating missing vines at the parcel level, a reproducible analytical workflow for large-scale vineyard monitoring, and spatial insights to inform long-term research and management decisions in viticulture.

# Project Description

This project develops a modeling and data‑integration framework to estimate long‑term vine mortality. The core contribution of this project is to provide a reproducible, LIDAR-based workflow for detecting missing grapevines at the parcel level. This workflow transforms raw HD LIDAR point clouds into meaningful indicators of vineyard structure, geometry and vine mortality. The analysis combines spatial preprocessing, height filtering, machine learning clustering, frequency detection and gap analyusis to produce parcel-level estimates of missing vines.

The second possible analysis may allow for the evaluations of vineyard vulnerability under climate stress, and enable the linkage of these risks to PDO/AOC regulations, grape varieties, and wine‑region characteristics. This workflow combines LiDAR data, ecological modeling models, sensitivity analysis and regulatory data extraction.

Our team is in the process in creating a reproducible workflow that detects missing vines using LiDAR point clouds, parcel boundaries, and regulatory spacing rules. The workflow integrates:

-   vegetation height filtering

-   DBSCAN clustering for vine detection

-   Fourier‑based row orientation estimation

-   gap detection and mortality estimation

-   SQL‑based data integration

-   sensitivity analysis of environmental and geometric factors

The result is a scalable methodology for quantifying vine mortality across French wine regions, beginning with the Rhône Valley.

This is a capstone project for the [Master of Environmental Data Science](https://bren.ucsb.edu/masters-programs/master-environmental-data-science) at the [Bren School of Environmental Science and Management](https://bren.ucsb.edu/), University of California, Santa Barbara.

# Data Sources

| **Data** | **Source** | **Use** |
|------------------------|------------------------|------------------------|
| LiDAR HD Point Clouds (.laz) | IGN (Institut National de l’Information Géographique et Forestière) | Vine canopy detection, clustering, gap analysis |
| Parcel Boundaries (.shp/.gpkg) | [Registre Parcellaire Graphique](data.gouv.fr) | Parcel clipping, spatial alignment |
| Wine Region / PDO Identifiers (.csv) | Public agriculture datasets | Linking parcels to regulatory regions |
| eAmbrosia Regulatory Data | [EU Commission](https://ec.europa.eu/agriculture/eambrosia/geographical-indications-register/) | Vine spacing rules, irrigation allowances |
| CVI Vine‑Age Data | Client sourced (restricted) | Validation of missing‑vine detection |
| Environmental Data (temperature, drought, slope) | Various public datasets | Sensitivity analysis inputs |

# Abstract

Climate change is reshaping vineyard viability across Europe, yet regional regulations, spacing rules, and varietal characteristics create uneven vulnerability across PDOs and wine types. vinDAR integrates climate‑stress mortality modeling, LiDAR‑based detection workflows, and PDO regulatory data to estimate long‑term vine loss and identify which regions, varieties, and wine styles are most susceptible to mortality.

Repositories in This Organization

```
vinDAR/
├── .git/
├── .gitignore
├── .Rproj.user/
├── .Rhistory
├── LICENSE
├── README.md
├── vinDAR.Rproj
├── nano.30808.save
└── src/
    ├── data_import.py
    ├── exploratory_analysis.ipynb
    ├── filename.csv
    └── lidar_improved.png
```

src:
  - data_import.py - import file 
  - exploratory_analysis.ipynb - main analysis 
  - filename.csv - data 
  - lidar_improved.png - image render

# Technical Documentation
To read more about the project and the processes, refer to the [Bren Project page and technical documentation](https://bren.ucsb.edu/projects/mapping-missing-vines-french-vineyards-using-national-lidar-hd-data-climate-and-disease)


Each repository includes its own README describing purpose, structure, and usage.

# Authors and Team

Team Members:
- Joshua Ferrer‑Lozano [Github](https://github.com/Awoo56709) | [Website](https://awoo56709.github.io/) | [LinkedIn](https://www.linkedin.com/in/joshuarflozano/)
- Stephan Kadonoff | [Github](https://github.com/SRKads1998) | [Website](https://srkads1998.github.io/) | [LinkedIn](https://www.linkedin.com/in/stephan-kadonoff-a5b1ba162/)
- Jay Kim | [GitHub](https://github.com/jwonyk) | [Website](https://jwonyk.github.io/) | [LinkedIn](https://www.linkedin.com/in/jwonyk)
- William Mullins | [Github](https://github.com/willrmull) | [Website](https://william-mullins.com/) | [LinkedIn](https://www.linkedin.com/in/william-mullins-12b430207/)

# Client:
Jean Sauveur-Ay [INRAE](https://www.inrae.fr/en)
[Andrew Plantinga](https://econ.ucsb.edu/people/faculty/andrew-plantinga)

Faculty Advisor:
[Andrew Plantinga](https://econ.ucsb.edu/people/faculty/andrew-plantinga)

# Acknowledgements 
We thank the Bren School faculty and staff for guidance, and acknowledge the organizations that provided regulatory, spatial, and grape‑quality data used in this project. Additional thanks to collaborators who supported data acquisition, domain interpretation, and methodological review.

# Key References & Data Sources EU & French PDO/AOC regulatory documents

- Grape‑quality datasets (variety‑level and region‑level attributes)

- Climate and environmental covariates used in stress modeling

- Sensitivity analysis tools and ecological modeling literature

# License 
This project is released under the MIT License unless otherwise noted in individual repositories.

# How to Use This Organization 

## Each repository includes:
- A clear README describing purpose and entry points
- A walkthrough of directory structure
- Standardized file naming conventions
- Reproducible code and documented workflows
- Appropriate licensing and contributor information
- A walkthrough of directory structure
- Standardized file naming conventions
- Reproducible code and documented workflows
- Appropriate licensing and contributor information

This organization is structured to support transparency, reproducibility, and long‑term usability for both the client and the broader community.
