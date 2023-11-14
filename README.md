# Multi-FireRS Dataset

## Introduction

Multi-FireRS is an open dataset designed specifically for instance segmentation in remote sensing images, with a focus on fire events. It comprises a diverse collection of real-world remote sensing images, facilitating the identification and analysis of various fire types, including wild fires, straw burning, and volcanic eruptions. The dataset utilizes medium to high-resolution satellite images from Landsat and Sentinel sensors.

## Data Definitions

### 1. Multispectral Satellite Images
   - **Source**: [Landsat 8](https://earthexplorer.usgs.gov/) and [Sentinel 2](https://scihub.copernicus.eu/dhus/) satellites.
   - **Resolution**: 30 meters (Landsat 8) and 20 meters (Sentinel 2).
   - **Characteristics**: Images cover various bands including visible light and thermal infrared,  providing rich information for fire event identification and analysis.
   ![image](https://github.com/Bella0818/Datasets/assets/79988921/1e7dd5aa-3571-4314-b04e-569adf688861)

### 2. Land Cover Data
   - **Source**: [GlobeLand30](https://www.webmap.cn/commres.do?method=globeIndex) dataset published by the National Geomatics Center of China.
   - **Resolution**: 30 meters.
   - **Details**: Describes different types of land cover such as forests, croplands, urban, etc.

### 3. Elevation Data
   - **Source**: [ASTER GDEMv3](https://www.gscloud.cn/sources/accessdata/aeab8000652a45b38afbb7ff023ddabb?pid=302).
   - **Resolution**: 30 meters.
   - **Function**: Describes the surface relief with coordinates and elevation points.

### 4. Population Density Data
   - **Source**: [Unconstrained individual countries 2000-2020 population count datasets](https://hub.worldpop.org/project/categories?id=18Proc)
   - **Resolution**: 1000 meters.
   - **Measure**: Recorded number of people per square kilometer.
![image](https://github.com/Bella0818/Datasets/assets/79988921/110caba5-7c37-4bfc-b0f9-8cd9e284560a)

## Data Collection and Processing

- **Fire Event Locations and Times**: The locations and times of fire events were obtained from the California Department of Forestry and Fire Protection, SatSee-Fire platform, and the Smithsonian's Global Volcanism Program. These data were then manually cleaned and organized to ensure accuracy and relevance.
- **Image Acquisition**: Data downloaded based on fire event locations and times from the USGS Earth Explorer platform.
- **Processing**: 
  - **Band Combination**:
    - For Landsat 8 images: Band 7 (Shortwave Infrared), Band 6 (Shortwave Infrared), and Band 4 (Red) were combined.
    - For Sentinel images: Band 12 (Shortwave Infrared), Band 11 (Shortwave Infrared), and Band 8 (Near Infrared) were combined.
    - These band combinations were performed to generate false-color images, providing enriched fire event information in the remote sensing imagery.
  - **Resampling**: All types of images were uniformly resampled to a spatial resolution of 30 meters.
  - **Cropping**: After resampling, images were cropped to a size of 512x512 pixels.
- **Annotation**: Fire event blocks are selected and labeled with the help of motivated participants, including researchers and students.

## Dataset Composition

- **Categories and Ratio**: 

    | Category | Image numbers |
    |---|---|
    | Wildfire | xx |
    | StrawBurning | xx |
    | VolcanicEruption | xx |
- **Total Fire Event Groups**: 1151.
- **Image Types per Group**: Each fire event group includes:
  - Single-band fire event image.
  - RGB fire event image.
  - Multi-band fused fire event image.
  - Land cover image.
  - Elevation image.
  - Population density image.
- **Image Size**: 512x512 pixels.
- **Resolution**: 30 meters.
- **Dataset Division**: training:testing=7:3.

## Access

- The Multi-FireRS Dataset is publicly available at this repository.
