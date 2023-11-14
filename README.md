# Datasets-markdown
# Multi-FireRS Dataset

## Introduction

Multi-FireRS is a multi-category dataset of fire events, featuring a diverse collection of real-world remote sensing images related to forest fires, straw burning, and volcanic eruptions. The dataset is built upon medium to high-resolution satellite images from Landsat and Sentinel sensors, widely used for fire identification, monitoring, and assessment.

## Dataset Definitions

### 1. Multispectral Satellite Images
   - **Source**: Landsat 2 and Sentinel 3 satellites.
   - **Resolution**: 30 meters (Landsat 2) and 20 meters (Sentinel 3).
   - **Characteristics**: Images cover various bands including visible light and thermal infrared, providing rich information for fire incident identification and analysis.

### 2. Land Cover Data
   - **Source**: GlobeLand30 dataset published by the National Geomatics Center of China.
   - **Resolution**: 30 meters.
   - **Details**: Describes different types of land cover such as forests, farmlands, urban areas, etc.

### 3. Elevation Data
   - **Source**: ASTER GDEMv3.
   - **Resolution**: 30 meters.
   - **Function**: Describes the surface relief with coordinates and elevation points.

### 4. Population Density Data
   - **Measure**: Recorded number of people per square kilometer or mile.

## Data Collection and Processing

- **Fire Event Data**: Sourced from California Department of Forestry and Fire Protection, SatSee-Fire platform, and Smithsonian's Global Volcanism Program.
- **Image Acquisition**: Data downloaded based on fire event locations and times from the USGS Earth Explorer platform.
- **Cloud Coverage**: Maximum cloud coverage of 5% considered for image collection.
- **Processing**: Resampled to 30m spatial resolution, with infrared and short-wave infrared bands overlaid. Images are then cropped to 512x512 pixels.
- **Annotation**: Fire event blocks are selected and labeled with the help of motivated participants, including researchers and students, and cross-referenced with high-resolution images from Google Earth for ambiguous areas.

## Multimodal Dataset for Fire Event Identification

- **Land Cover, Population Density, and Elevation Images**: Serve as a priori knowledge for fire event identification.
- **Resampling and Cropping**: Environmental data samples are resampled to 30m spatial resolution and cropped to match the size of fire event samples.

## Dataset Composition

- **Categories**: Forest fires, straw burning, volcanic eruptions.
- **Total Images**: 1151 PNG images.
- **Image Size**: 512x512 pixels.
- **Resolution**: 30 meters.
- **Multimodal Data**: Each fire event image is accompanied by corresponding environmental data.

## Access

- The Multi-FireRS Dataset is publicly available at [xxx].

## Figures

- **Spatial Distribution Statistics**: Illustrated in Figure 4.
- **Sample Images**: Examples of the three categories are shown in Figure 5.
