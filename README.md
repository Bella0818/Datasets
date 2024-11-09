# Multi-FireRS Dataset

## Tracking Fire Events with Multi-Source Satellite Data

This repository contains case study videos demonstrating the use of multi-source satellite data for wildfire tracking and analysis. These videos showcase how various satellite sources (such as Landsat, Sentinel, and MODIS) are used to monitor wildfire progression, assess burn severity, and support emergency response. 

<div style="display: flex; flex-wrap: wrap; justify-content: space-between;">
  
  <figure style="flex: 1 1 30%; text-align: center; margin: 10px;">
    <img src="https://github.com/user-attachments/assets/c661ce81-5cb2-4dcc-a7e0-38b99378d6be" width="100%" />
    <figcaption><strong>Stagecoach Fire - August 3, 2020</strong></figcaption>
  </figure>

  <figure style="flex: 1 1 30%; text-align: center; margin: 10px;">
    <img src="https://github.com/user-attachments/assets/aa67fd5d-34e1-4a44-9285-893864cd3198" width="100%" />
    <figcaption><strong>Lake Fire - August 12, 2020</strong></figcaption>
  </figure>

  <figure style="flex: 1 1 30%; text-align: center; margin: 10px;">
    <img src="https://github.com/user-attachments/assets/9e5014ac-3b20-4e42-9f3f-262ff530259d" width="100%" />
    <figcaption><strong>Mineral Fire - July 13, 2020</strong></figcaption>
  </figure>

  <figure style="flex: 1 1 30%; text-align: center; margin: 10px;">
    <img src="https://github.com/user-attachments/assets/3ca33fb8-15ba-43e0-bfb4-f07e540aa3e5" width="100%" />
    <figcaption><strong>Kīlauea Volcano Eruption - February 6, 2021</strong></figcaption>
  </figure>

  <figure style="flex: 1 1 30%; text-align: center; margin: 10px;">
    <img src="https://github.com/user-attachments/assets/8f0d36a8-11df-4fe7-893b-71e468864b71" width="100%" />
    <figcaption><strong>North Complex Fire - August 25, 2020 (Landsat/Sentinel)</strong></figcaption>
  </figure>

  <figure style="flex: 1 1 30%; text-align: center; margin: 10px;">
    <img src="https://github.com/user-attachments/assets/8f0d36a8-11df-4fe7-893b-71e468864b71" width="100%" />
    <figcaption><strong>North Complex Fire - August 25, 2020 (MODIS)</strong></figcaption>
  </figure>
  
</div>

## Introduction

Multi-FireRS is an open dataset designed specifically for instance segmentation in remote sensing images, with a focus on fire events. It comprises a diverse collection of real-world remote sensing images, facilitating the identification and analysis of various fire types, including wild fires, straw burning, and volcanic eruptions. The dataset utilizes medium to high-resolution satellite images from Landsat and Sentinel sensors.

## Data Definitions

### 1. Multispectral Satellite Images
   - **Source**: [Landsat 8](https://earthexplorer.usgs.gov/) and [Sentinel 2](https://scihub.copernicus.eu/dhus/) satellites.
   - **Resolution**: 30 meters (Landsat 8) and 20 meters (Sentinel 2).
   - **Characteristics**: Images cover various bands including visible light and thermal infrared,  providing rich information for fire event identification and analysis.
      ![image](https://github.com/Bella0818/Datasets/assets/79988921/1e7dd5aa-3571-4314-b04e-569adf688861)

### 2. Land Cover Data
| **Source**                                               | **Year(s)** | **Resolution** | **Link**                                           |
| -------------------------------------------------------- | ----------- | -------------- | -------------------------------------------------- |
| GlobeLand30 dataset (National Geomatics Center of China) | 2020        | 30 meters      | https://www.webmap.cn/commres.do?method=globeIndex |
| ESRI Land Cover dataset (Esri)                           | 2021, 2022  | 10 meters      | https://livingatlas.arcgis.com/landcoverexplorer/  |
| CLCD dataset (Annual China Land Cover Dataset)           | 2013        | 30 meters      | https://zenodo.org/records/5816591                 |

To ensure category consistency, we standardized the categories across datasets and mapped the corresponding colors, as shown in the table below.

| Category           | Value | Color (R, G, B) | GlobeLand30 | GlobeLand30 Color | Esri | Esri Color | CLCD | CLCD (R, G, B)  |
| ------------------ | ----- | --------------- | ----------- | ----------------- | ---- | ---------- | ---- | --------------- |
| Water              | 1     | (0, 0, 255)     | 60          | (0, 0, 255)       | 1    | #1A5BAB    | 5    | (30, 105, 180)  |
| Forest             | 2     | (0, 100, 0)     | 20          | (0, 100, 0)       | 2    | #358221    | 2    | (68, 111, 51)   |
| Flooded Vegetation | 3     | (0, 100, 255)   | 50          | (0, 100, 255)     | 3    | #87D19E    | 9    | (40, 155, 232)  |
| Crops              | 4     | (250, 160, 255) | 10          | (250, 160, 255)   | 4    | #FFDB5C    | 1    | (250, 227, 156) |
| Built Area         | 5     | (255, 0, 0)     | 80          | (255, 0, 0)       | 5    | #ED022A    | 8    | (226, 66, 144)  |
| Bare Ground        | 6     | (190, 190, 190) | 90          | (190, 190, 190)   | 6    | #EDE9E4    | 7    | (207, 189, 163) |
| Snow/Ice           | 7     | (200, 240, 255) | 100         | (200, 240, 255)   | 7    | #F2FAFF    | 6    | (166, 206, 227) |
| Grassland          | 8     | (100, 255, 0)   | 30          | (100, 255, 0)     | 9    | #C6AD8D    | 4    | (171, 211, 123) |
| Shrubland          | 9     | (0, 255, 120)   | 40          | (0, 255, 120)     | N/A  | N/A        | 3    | (51, 160, 44)   |
| Clouds             | 10    | (200, 200, 200) | N/A         | N/A               | 8    | #C8C8C8    | N/A  | N/A             |
| Tundra             | 11    | (100, 100, 50)  | 70          | (100, 100, 50)    | N/A  | N/A        | N/A  | N/A             |
| Sea                | 255   | (0, 200, 255)   | 255         | (0, 200, 255)     | N/A  | N/A        | N/A  | N/A             |
| No Data            | 0     | (0, 0, 0)       | 0           | (0, 0, 0)         | N/A  | N/A        | N/A  | N/A             |



### 3. Elevation Data

   - **Source**: [ASTER GDEMv3](https://www.gscloud.cn/sources/accessdata/aeab8000652a45b38afbb7ff023ddabb?pid=302).
   - **Resolution**: 30 meters.
   - **Function**: Describes the surface relief with coordinates and elevation points.

### 4. Population Density Data

| **Source**                          | **Resolution** | **Link**                                          |
| ----------------------------------- | -------------- | ------------------------------------------------- |
| WorldPop global population datasets | 1000 meters    | https://hub.worldpop.org/project/categories?id=18 |
| LandScan global population datasets | 1000 meters    | https://landscan.ornl.gov/about                   |


![fig4-v2](/Users/judy/Desktop/Judy/研究生科研制图相关/fig4-v2.png)


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
- **Data Type**: COCO Annotations Converted to YOLO Format.
- **Total Fire Event Groups**: 434.
- **Image Types per Group**: Each fire event group includes:
  - Multi-band fused fire event image.
  - Land cover image.
  - Elevation image.
  - Population density image.
  - Annotations
- **Image Size**: 512x512 pixels.
- **Resolution**: 30 meters.
- **Dataset Division**: training:testing=7:3.

## Access

- The Multi-FireRS Dataset is publicly available at this repository.
