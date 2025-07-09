# Bee Pollinator Monitoring for Coastal Endangered Plants

## Overview

This project develops a machine learning (ML) model to detect pollinator activity for two endangered coastal plant species:

- **Salt Marsh Bird's Beak** (*Chloropyron maritimum*)
- **Ventura Marsh Milkvetch** (*Astragalus pycnostachyus* var. *lanosissimus*)

Traditional pollinator monitoring is labor-intensive and limited by short bloom windows. This project uses a combination of camera trap footage, and deep learning to support scalable, non-invasive ecological monitoring and inform conservation strategies.

## Project Goals

- **Automated Detection**: Develop image-based ML classification to detect pollinator visits to target plants
- **Conservation Impact**: Identify pollinator species and quantify visitation frequency to inform conservation strategies
- **Scalable Monitoring**: Create a replicable framework for endangered plant pollinator monitoring

## Data Collection Protocol

### Study Sites
Data are collected at four sites within the North Campus Open Space (NCOS), each monitored via camera traps:

- **Monitoring Schedule**: 3 times/day, 3 days/week
- **Camera Setup**: Both high- and low-resolution cameras per site
- **Site Marking**: Yarn quadrants for spatial reference (orange at Sites 1 & 2, yellow at Sites 3 & 4)

### Metadata Collection
Each observation session logs:
- Site location and camera ID
- Date, time, and shift type (morning/midday/afternoon)
- Weather conditions (temperature, wind speed, cloud cover)
- Pollinator activity (species, count, behavior)
- Video duration and technical notes

### Data Storage Structure
```
KB_summer25_NCOS/
  └── Salt Marsh Birds Beak/
      └── Week_1/
          └── Day_1/
              └── Site_1/
                  └── morning/
                      └── camera_type/
```

## Machine Learning Pipeline

### Training Data
- **Synthetic Images**: Created by overlaying pinned bee specimens onto vegetation backgrounds
- **Real Field Data**: Camera trap footage with manual annotations
- **Metadata Integration**: Environmental conditions and temporal data

### Model Architecture
- **Framework**: CNN-based architecture using PyTorch
- **Input Features**: Image data (field + synthetic) and environmental metadata
- **Current Performance**: 80% accuracy on synthetic datasets
- **Target**: Improve accuracy by incorporating real imagery and environmental factors

## Target Species

### *Chloropyron maritimum* (Salt Marsh Bird's Beak)
- **Type**: Hemiparasitic, salt-tolerant annual herb
- **Bloom Period**: May–October
- **Primary Pollinators**: Native bees (*Melissodes*, *Lasioglossum*, *Bombus*)
- **Conservation Threats**: Invasive species, low visitation rates, habitat loss

### *Astragalus pycnostachyus* var. *lanosissimus* (Ventura Marsh Milkvetch)
- **Type**: Perennial herb (rediscovered in 1997)
- **Bloom Period**: June–October
- **Primary Pollinators**: Large bees requiring mechanical pollination (*Bombus*, *Xylocopa*)
- **Conservation Threats**: Habitat degradation, pollination failure, climate change

## Repository Structure

```
├── preliminary_research_7:9.Rmd          # Exploratory analysis of pollination dynamics
├── Collection Observations - Birds Beak-2.csv  # Field observation log
├── preliminary_research_7-9.html         # Rendered HTML analysis output
├── .gitignore                            # Git exclusions
├── birds_beak.Rproj                      # RStudio project file
└── README.md                             # Project documentation
```

## Getting Started

### Prerequisites
- R (≥ 4.0.0) with packages: `tidyverse`, `lubridate`, `plotly`, `DT`, `kableExtra`
- Python (≥ 3.8) with PyTorch for ML model development

### Data Analysis
1. Open `birds_beak.Rproj` in RStudio
2. Run `preliminary_research_7:9.Rmd` to reproduce exploratory analysis
3. View results in `preliminary_research_7-9.html`

## Current Status

- **Data Collection**: Active monitoring at 4 sites with systematic observation protocol
- **Preliminary Analysis**: Completed exploratory analysis of *Bombus* activity patterns
- **Model Development**: In progress - synthetic dataset created in the past, working toward real data integration

## Team & Contact

- **Primary Contact**: Dr. Chris Evelyn – Camera logistics and data pipeline
- **Lab Oversight**: Dr. Katja Seltmann
- **Field Support**: Wayne Chapman & Claire Wilhelm-Safian
- **Meetings**: Weekly/biweekly lab group meetings for progress updates and troubleshooting

## Contributing

This project is part of ongoing research at [Institution Name]. For questions about data collection protocols or analysis methods, please contact the project team.

## License

[Add appropriate license information]

---

*Last updated: [07/09/25]*
