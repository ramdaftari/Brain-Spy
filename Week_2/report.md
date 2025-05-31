# Task 2 Report

**Core Implementation:**
- Used nibabel for NIfTI file loading and metadata extraction
- Implemented pydicom for DICOM file handling capabilities
- Applied nilearn for neuroimaging-specific analysis functions
- Utilized numpy for numerical operations on 3D arrays
- Integrated matplotlib for data visualization

**Processing Pipeline:**
1. Loaded NIfTI files and extracted image dimensions (256 x 384 x 384 voxels)
2. Retrieved affine transformation matrices from file headers
3. Located peak activation points using argmax operations
4. Converted voxel coordinates to real-world millimeter coordinates
5. Created spherical regions of interest around peak points

## Preprocessing and Assumptions

**File Format Assumptions:**
- Input files were in NIfTI format with standard header information
- Affine transformation matrices were correctly stored in file headers
- Image orientation followed standard neuroimaging conventions

**Data Processing Assumptions:**
- Peak activation represented the brightest voxel in the dataset
- 5mm radius spheres provided appropriate region-of-interest analysis
- Coordinate system transformations used scanner-provided affine matrices

**Preprocessing Steps:**
- Extracted compressed medical image archives automatically
- Validated image dimensions and data types
- Verified affine matrix integrity before coordinate transformations

## Observations and Challenges

**Technical Findings:**
- Successfully processed 37,748,736 total voxels across the 3D volume
- Peak activation located at voxel coordinates (135, 187, 320)
- Converted to world coordinates: [-1.27, 32.27, 73.76] mm
- Mean intensity value within 5mm sphere: 2486.081

**Implementation Challenges:**
- Struggled with managing DICOM data but then uploaded it as a zip file for processing
- Encountered difficulties with stacking the DICOM files to create the 3d numpy array
- Coordinate system transformations needed careful validation



