## landsat-dl
*01-11-2017 - Jasper Siebring*

Tool that allows you to search and generate download URLs for LANDSAT imagery. Originally based on Olivier Hagolle' [LANDSAT-DOWNLOAD](https://github.com/olivierhagolle/LANDSAT-Download) tool but with added support for collection 1 data and overall improvements across the board (also written in Python 3 instead of 2). Uses the USGS api to get any selected imagery' storage directories on the USGS servers which is needed to generate a valid download URL. Storage directories for pre-collection datasets are still manually assessed and can sadly change at any time. Collection 1' directories however are extracted directly from their API making it much more reliable (also much faster). 

**Features**:
- Query LANDSAT MSS/TM/7/8 imagery ([pre-collection and collection 1](https://landsat.usgs.gov/download-entire-collection-metadata))
- Filter using path/row/date/cloudcover/day/night
- Preview selected imagery (using preview image url found in metadata)  
- Automatically downloads (and updates if needed) metadata required for querying
- Generates download URLs for any selected LANDSAT imagery
- Directly download from generated URLs (requires logging in to the USGS website) using urllibs
- Checks validity of given dates and generated URLs
- Written in Python 3.5

**To be implemented**:
- Download using the requests library (current download functionality is limited and unnecessarily slow)
- Metadata query via some external database (preventing local downloading of large metadata files)
 

