Bee Pollinator Monitoring for Coastal Endangered Plants

Overview

This project develops a machine learning (ML) model to detect pollinator activity for two endangered coastal plant species:

Salt Marsh Bird’s Beak (Chloropyron maritimum)
Ventura Marsh Milkvetch (Astragalus pycnostachyus var. lanosissimus)
Traditional pollinator monitoring is labor-intensive and limited by short bloom windows. This project uses a combination of camera trap footage, synthetic image generation, and deep learning to support scalable, non-invasive ecological monitoring and inform conservation strategies.

Goals

Detect pollinator visits to target plants using image-based ML classification
Use synthetic and real image datasets to train and validate the model
Contribute to conservation by identifying pollinator species and visitation frequency
Data Collection Protocol

Data are collected at four sites within the North Campus Open Space (NCOS). Each site is monitored via camera traps:

Shift structure: 3 times/day, 3 days/week, with both high- and low-res cameras
Perimeter marking: Yarn quadrants (orange at Sites 1 & 2, yellow at Sites 3 & 4)
Metadata logged: Site, date, time, weather, wind, pollinator activity, camera ID
Storage structure:
KB_summer25_NCOS/
  └── Salt Marsh Birds Beak/
      └── Week_1/
          └── Day_1/
              └── Site_1/
                  └── morning/
                      └── camera_type/
Machine Learning Pipeline

Training data: Synthetic images made by overlaying pinned bee cutouts onto vegetation backgrounds
Model: CNN-based architecture using PyTorch
Inputs: Image data (from field and synthetic), metadata
Performance goal: Improve beyond current 80% accuracy on synthetic datasets by incorporating real imagery
Species Background

Chloropyron maritimum (Salt Marsh Bird's Beak)
Hemiparasitic, salt-tolerant annual herb
Blooms May–October
Primary pollinators: native bees (Melissodes, Lasioglossum, Bombus)
Threats: invasive species, low visitation rates, habitat loss
Astragalus pycnostachyus var. lanosissimus (Ventura Marsh Milkvetch)
Perennial herb rediscovered in 1997
Blooms June–October
Relies on mechanical pollination by large bees (Bombus, Xylocopa)
Threats: habitat degradation, pollination failure, climate change
Files

preliminary_research_7:9.Rmd: Exploratory analysis of Chloropyron maritimum pollination dynamics
Collection Observations - Birds Beak-2.csv: Field observation log
preliminary_research_7-9.html: Rendered HTML output of research analysis
.gitignore: Git exclusions
birds_beak.Rproj: RStudio project file
Team & Contact

Primary contact: Dr. Chris Evelyn – Camera logistics and data pipeline
Advisors: Dr. Katja Seltmann (lab oversight), Wayne Chapman & Claire Wilhelm-Safian (field support)
Lab group meetings: Weekly or biweekly to discuss progress and troubleshoot
