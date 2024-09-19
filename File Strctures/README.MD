# HCC-TACE-SEG Dataset Folder Structure

This README provides an overview of the folder structure for the HCC-TACE-SEG dataset, detailing its organization across multiple levels of directories and files. The dataset is structured to facilitate access to medical imaging data and associated metadata.

## Folder Structure Overview

The dataset is organized into four hierarchical levels, each providing specific details about the contents and organization of the data. Below is a summary of each level.

## Level 1: Main Patient Directories

### Overview

The Level 1 directory structure of the HCC-TACE-SEG dataset consists of directories that represent individual patient cases. Each directory is named according to a unique identifier for each patient, providing a top-level organization of the dataset.

- **File**: `strcture_level_1.txt`
- **Description**: Contains a list of directories, each representing a unique patient case.
- **Contents**: 106 directories, named `HCC_001` to `HCC_105`, where each directory corresponds to an individual patient's data.


### File

- **File Name**: `strcture_level_1.txt`
- **Purpose**: Lists all the top-level directories, each corresponding to a unique patient in the dataset.

### Directory Structure

- **Total Directories**: 106
- **Directory Naming Format**: `HCC_XXX`
  - **HCC**: Prefix indicating the dataset or project type.
  - **XXX**: A three-digit numerical identifier ranging from `001` to `105`. Each number uniquely identifies a patient case.

### Directory Details

Each directory at this level corresponds to a specific patient and contains all the data and subdirectories related to that patient’s imaging studies. Below is a brief overview of how to interpret these directories.

**Example Directory: `HCC_001`**

- **Directory Name**: `HCC_001`
  - **Description**: Represents the dataset for the first patient. It will include various subdirectories and files pertaining to the imaging studies and metadata for this patient.
  
**Example Directory: `HCC_002`**

- **Directory Name**: `HCC_002`
  - **Description**: Represents the dataset for the second patient, following the same structure as `HCC_001`.

**Example Directory: `HCC_105`**

- **Directory Name**: `HCC_105`
  - **Description**: Represents the dataset for the 105th patient, containing subdirectories and files relevant to this patient’s imaging studies.



## Level 2: Study Directories

- **File**: `strcture_level_2.txt`
- **Description**: Details the structure within each patient's directory. Each patient directory contains multiple subdirectories related to different imaging studies.
- **Contents**: 317 directories in total, including the patient directories and their respective subdirectories.
- **Subdirectory Naming Format**: `<DATE-MODALITY-DESCRIPTION-STUDYNUMBER>`
  - **Date**: The date when the scan was performed (e.g., `04-21-2000`).
  - **Modality**: Imaging modality used, such as:
    - `CT`: Computed Tomography
    - `CAP`: Chest, Abdomen, Pelvis
    - `AP`: Anteroposterior-direction
  - **Description**: Details about the imaging scan, including the region of the body and type of scan. Examples:
    - Description: The region of the body and the type of scan or protocol used. 18 unique descriptions are as per below,
    - `CT ABDPEL WC`: CT Abdomen Pelvis with Contrast
    - `ABDPEL LIVER`: Abdomen Pelvis Liver
    - `CT CHEST NON CON`: CT Chest Non-Contrast
    - `ABDPELVIS WITH CONTRAST`: Abdomen Pelvis with Contrast
    - `CHEST ORBIT FACE NECK WITHOUT CONTRAST`: Chest Orbit Face Neck without Contrast
    - `CHEST WITH CONTRAST`: Chest with Contrast
    - `LIVER MULTIPHASIC`: Liver Multiphase CT
    - `CT ABDOMEN WITH CONTRAST`: CT Abdomen with Contrast
    - `CT CHEST WITHOUT CONTRAST`: CT Chest without Contrast
    - `CT ABDOMEN NON CON`: CT Abdomen Non-Contrast
    - `CT ABDOMEN WITH MULTIPHASIC`: CT Abdomen with Multiphase Contrast
    - `CT PELVIS WITH CONTRAST`: CT Pelvis with Contrast
    - `CT CHEST WITH AND WITHOUT CONTRAST`: CT Chest with and without Contrast
    - `CT CHEST NON CONTRAST`: CT Chest Non-Contrast
    - `CT CHEST WITH IV CONTRAST`: CT Chest with Intravenous (IV) Contrast
    - `CT PELVIS NON CONTRAST`: CT Pelvis Non-Contrast
    - `LIVER 3 PHASE`: Liver Three-Phase CT
    - `CHEST WITHOUT CONTRAST`: Chest without Contrast

  - **Study Number**: Unique identifier for the specific scan (e.g., `49771`).

**Examples:**
1. `HCC_001/04-21-2000-NA-CT ABDPEL WC-49771`:
   - Patient: HCC_001
   - Date: April 21, 2000
   - Modality: CT
   - Description: Abdomen Pelvis with Contrast
   - Study Number: 49771

2. `HCC_002/03-05-1998-NA-ABDPEL LIVER-93301`:
   - Patient: HCC_002
   - Date: March 5, 1998
   - Modality: NA (not applicable)
   - Description: Abdomen Pelvis Liver
   - Study Number: 93301

## Level 3: Image/Data Segments

- **File**: `strcture_level_3.txt`
- **Description**: Contains directories and files related to specific image segments or data processing stages.
  
1. `PRE LIVER`
   - **Description**: Pre-treatment or preparatory images of the liver.
   - **Details**: Provides images before any special procedures or reconstructions are applied.
   
2. `Segmentation`
   - **Description**: Images or data related to the segmentation of liver structures.
   - **Details**: Involves separating and analyzing different parts of the liver for further examination or treatment planning.

3. `Recon 2 LIVER 3 PHASE AP`
   - **Description**: Reconstruction of liver images in a three-phase approach, focusing on the anterior-posterior (AP) plane.
   - **Details**: A second level of reconstruction that involves combining data from different imaging phases to create a detailed view of the liver.

4. `Recon 3 LIVER 3 PHASE AP`
   - **Description**: Advanced reconstruction of liver images in a three-phase approach, focusing on the anterior-posterior (AP) plane.
   - **Details**: A third level of reconstruction providing enhanced detail and clarity compared to Recon 2.

5. `3 PHASE LIVER ABD`
   - **Description**: Three-phase imaging of the liver and abdomen.
   - **Details**: Includes images captured at different phases to give a comprehensive view of the liver and surrounding abdominal structures.

6. `LIVER 3 PHASE AP`
   - **Description**: Three-phase imaging of the liver with an emphasis on the anterior-posterior (AP) plane.
   - **Details**: Similar to the "3 PHASE LIVER ABD" but focused specifically on the AP plane.

7. `LIVER 3 PHASE CAP`
   - **Description**: Three-phase imaging of the liver with a focus on the capsule.
   - **Details**: Captures detailed images of the liver capsule during different phases of imaging.

8. `NA`
   - **Description**: Not applicable or non-applicable; often used in filenames to denote a missing or non-relevant parameter.
   - **Details**: Indicates that certain details or parameters are not available or not relevant for the specific dataset.

9. `Recon 2 PRE LIVER`
   - **Description**: Reconstruction based on preparatory liver images.
   - **Details**: A second reconstruction phase applied to images taken before any further processing or treatments.

10. `Recon 3 PRE LIVER`
    - **Description**: Advanced reconstruction based on preparatory liver images.
    - **Details**: The third level of reconstruction applied to pre-treatment liver images.

11. `Recon 2 LIVER 3 PHASE CAP`
    - **Description**: Reconstruction of liver images in three phases with a focus on the liver capsule.
    - **Details**: A second level of reconstruction providing detailed views of the liver capsule.

12. `Recon 3 LIVER 3 PHASE CAP`
    - **Description**: Advanced reconstruction of liver images in three phases with a focus on the liver capsule.
    - **Details**: The third level of reconstruction offering enhanced detail of the liver capsule.

13. `CT ABDPEL LIVER`
    - **Description**: Computed tomography of the abdomen and pelvis with a focus on the liver.
    - **Details**: Provides imaging that includes both abdominal and pelvic regions with emphasis on the liver.

14. `CT ABD LIVER`
    - **Description**: Computed tomography of the abdomen with a focus on the liver.
    - **Details**: Imaging focused on the abdominal region, specifically the liver.

15. `CT CHEST ABD LIVER`
    - **Description**: Computed tomography of the chest, abdomen, and liver.
    - **Details**: Comprehensive imaging that covers the chest, abdomen, and liver areas.

16. `CT CAP LIVER`
    - **Description**: Computed tomography of the liver with emphasis on the capsule.
    - **Details**: Imaging focused on the liver capsule, often for detailed examination.

17. `CT A-P LIVER`
    - **Description**: Computed tomography of the liver with an emphasis on the anterior-posterior (A-P) plane.
    - **Details**: Provides imaging from the anterior to posterior view of the liver.

18. `CT CHESTABD LIVER`
    - **Description**: Computed tomography of the chest, abdomen, and liver together.
    - **Details**: Imaging that covers the chest and abdominal regions along with the liver.

19. `CT ABDOMEN WWO CONT`
    - **Description**: Computed tomography of the abdomen with a wide window of contrast.
    - **Details**: Includes imaging of the abdomen with extended contrast settings.

20. `CT ABDPELVIS`
    - **Description**: Computed tomography of the abdomen and pelvis.
    - **Details**: Covers both the abdominal and pelvic regions.

21. `CT CHESTABDPELVIS`
    - **Description**: Computed tomography of the chest, abdomen, and pelvis.
    - **Details**: Comprehensive imaging including chest, abdomen, and pelvis.

22. `CT CHESTABPEL LIVER`
    - **Description**: Computed tomography of the chest, abdomen, and pelvis with a focus on the liver.
    - **Details**: Imaging that includes the chest, abdomen, pelvis, and emphasizes the liver.

23. `CT ABDPEL LIVER`
    - **Description**: Computed tomography of the abdomen and pelvis with a focus on the liver.
    - **Details**: Imaging that covers the abdominal and pelvic regions with emphasis on the liver.
    
- **Contents**: 994 directories and files in total.
- **Naming Format**: `NUMBER.XXXXXX-<DESCRIPTION>-<ID>`
  - **Number**: Identifier or sequence number.
  - **Description**: Type of image processing or segmentation, such as `PRE LIVER`, `Segmentation`, or `Recon 2 LIVER 3 PHASE AP`.
  - **ID**: Additional identifier or code.

**Examples of Descriptions:**
1. `100.000000-NA-46705`:
   - **Description**: Not applicable (NA) data with an ID of 46705.

2. `2.000000-PRE LIVER-76970`:
   - **Description**: Pre-treatment liver images with an ID of 76970.

## Level 4: DICOM Files

- **File**: `strcture_level_4.txt`
- **Description**: Contains the actual imaging data files in DICOM format.
- **Contents**: 51,968 DICOM files.