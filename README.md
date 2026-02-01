# Project Overview

This project analyses public transport accessibility across Lancashire County Council by evaluating the proportion of the population living within 400 metres of an active public transport stop.

The analysis integrates spatial accessibility modelling with socio-demographic indicators (IMD and population structure) to identify areas with good, moderate, or poor access to public transport services.

The final output is a thematic map and interactive-ready dataset designed to support transport planning, social equity assessment, and policy decision-making.

##  Use Case

This analysis can be used by:

Local authorities to identify underserved communities and prioritise transport investments

Urban and transport planners to evaluate walkable access to public transport

Social equity analysts to assess transport inequality across deprivation deciles

Policy makers to support evidence-based decisions on service expansion or optimisation

Key questions addressed include:

Which LSOAs have low population access to public transport?

How does accessibility vary across districts and deprivation levels?

Are vulnerable populations (children, working-age adults, elderly) adequately served?

## Data Sources

The project integrates multiple authoritative datasets:

Spatial Data

Lower Super Output Areas (LSOA) Boundaries
Source: Office for National Statistics (ONS)

Public Transport Stops (Bus / Rail)
Source: General Transit Feed Specification (GTFS) / Local transport datasets

Administrative Boundaries (Districts & County)
Source: ONS / Ordnance Survey Open Data

Socio-Demographic Data

Index of Multiple Deprivation (IMD 2019)
Source: Ministry of Housing, Communities & Local Government

Population Data (Age Groups)

Children (0–15)

Working Age (16–64)

Elderly (65+)
Source: ONS Census Estimates

All datasets were projected into a common coordinate reference system to ensure spatial accuracy.

## Step-by-Step Analysis
Step 1: Data Preparation

Imported all spatial and tabular datasets into ArcGIS Pro

Verified coordinate systems and re-projected where necessary
Why this step is necessary:
Ensures spatial layers align correctly and distance-based analysis is accurate.

Step 2: Cleaning and Attribute Validation

Checked attribute tables for missing values and inconsistencies

Ensured each feature had a unique numeric ID for publishing compatibility
Why this step is necessary:
Prevents errors during geoprocessing and web map publishing.

Step 3: Buffer Analysis

Created a 400-metre buffer around active public transport stops
Why this step is necessary:
400m represents a widely accepted walkable distance to public transport in urban planning.

Step 4: Spatial Overlay

Intersected LSOA boundaries with the transport buffer
Why this step is necessary:
Identifies which parts of each LSOA fall within walkable access to transport.

Step 5: Population Accessibility Calculation

Calculated the proportion of each LSOA’s population within the 400m buffer

Derived percentage accessibility values for:

Total population

Children (0–15)

Working age (16–64)

Elderly (65+)
Why this step is necessary:
Quantifies accessibility rather than relying on visual proximity alone.

Step 6: Classification and Thematic Mapping

Classified accessibility into meaningful categories:

< 25%

25–50%

50–75%

75–100%

Applied graduated colour symbology for clarity
Why this step is necessary:
Makes spatial patterns interpretable for non-technical stakeholders.

Step 7: Layout Design and Cartographic Output

Designed a professional map layout including:

Title

Legend

Scale bar

North arrow

Contextual basemap

Explanatory text
Why this step is necessary:
Transforms analysis into a communication-ready product.

## Outcome and Results
Key Findings

Most urban areas in Lancashire show moderate to high public transport accessibility

Several rural and peripheral LSOAs fall below 25% accessibility, indicating service gaps

Accessibility disparities align closely with deprivation patterns, highlighting transport inequality

Vulnerable populations, particularly the elderly, are disproportionately affected in low-access areas
