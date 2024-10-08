# Time-paired-local-Sentinel-1-Sentinel-2-dataset

This dataset contains time-aligned data pairs from Sentinel-1 and Sentinel-2 satellites, used to train a regressive Unet-like CNN to predict NDVI maps from SAR backscatter maps in "L. Liverotti, N. Ferro, L. Soli, M. Matteucci, S. Perotto, Using SAR Data as an Effective Surrogate for Optical Data in Nitrogen Variable Rate Applications: a Winter Wheat Case Study, Remote Sensing, submitted. Specifically, we consider SAR data (SAR backscatter coefficients) and optical measurements of NDVI (Normalized Difference Vegetation Index), with a maximum acquisition gap of 3 days between the two sources and no cloud cover.

Study Area
The SAR/optical data pairs were extracted from a wide geographical area around the wheat crop of interested, in order to create a sufficiently rich training set. The specific area is described by the WKT string POLYGON(9.448694 45.492637, 9.567333 45.492637, 9.567333 45.561565, 9.448694 45.561565, 9.448694 45.492637).

Dataset Structure
For each SAR/optical data pair, nine patches of size 128 × 128 pixels were extracted, with a spatial resolution of 10 m × 10 m per pixel. One patch includes the wheat field of interest, while the remaining eight patches cover purely agricultural areas outside the target field.

Coregistered Maps
For each patch, four coregistered maps were retrieved:

NDVIo: Normalized Difference Vegetation Index derived from Sentinel-2 optical data.
LAIo: Leaf Area Index.
SAR Σ: VH+VV SAR backscatter coefficients from Sentinel-1.
The coregistered maps were created with the aim of providing a comprehensive and diverse dataset for training models based on multi-source data, useful for crop monitoring and agricultural management applications.

Acquisition Conditions
Acquisition Gap: Maximum of 3 days between Sentinel-1 and Sentinel-2 acquisitions.
Cloud Cover: No cloud cover for Sentinel-2 optical acquisitions.
