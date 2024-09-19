# HCC-TACE-SEG-Dataset-Overview

<div align="center"> <a href="https://www.cancerimagingarchive.net/collection/hcc-tace-seg/"><img width="700px" height="auto" src="https://www.cancerimagingarchive.net/wp-content/uploads/2021/06/TCIA-Logo-01.png"></a> </div> <p style="text-align:center;font-size:10px;"><em></em></p>

## Dataset Information

The **HCC-TACE-Seg** dataset is a comprehensive collection of CT images specifically designed for organ and tumor segmentation. It is part of the TCIA (The Cancer Imaging Archive) database and features data from 105 patients diagnosed with hepatocellular carcinoma (HCC). This dataset provides essential resources for predicting tumor response to transarterial chemoembolization (TACE) and improving the effectiveness of diagnostic and therapeutic strategies for HCC.

**Dataset Highlights:**
- **Coverage:** Pre- and post-treatment CT images
- **Patient Range:** 105 patients with HCC
- **Time Span:** 2002 to 2012
- **Segmentation:** Semi-automatically performed with manual clinical corrections
- **Format:** Data converted from NIfTI to DICOM-SEG for segmentation

**Clinical Context:**
HCC is the most common primary liver cancer, and its incidence has doubled in the past two decades due to increasing risk factors. Most cases are diagnosed late, leaving TACE or systemic treatment as the primary options. Despite its prevalence, up to 60% of TACE treatments fail, underscoring the need for advanced predictive tools. The HCC-TACE-Seg dataset supports research in radiomics to predict treatment outcomes and enhance patient management strategies.

## Dataset Meta Information

| Dimensions | Modality | Task Type    | Anatomical Structures | Anatomical Area | Number of Categories | Data Volume | File Format |
|------------|----------|--------------|-----------------------|-----------------|----------------------|-------------|-------------|
| 3D         | CT       | Segmentation | Liver, Liver Tumor    | Abdomen         | 4                    | 628         | .dcm        |

### Resolution Details

| Dataset Statistics | Spacing (mm)        | Size            |
|--------------------|---------------------|-----------------|
| min                | (0.58, 0.58, 2.50)  | (512, 512, 40)  |
| median             | (0.78, 0.78, 2.50)  | (512, 512, 87)  |
| max                | (0.98, 0.98, 5.00)  | (512, 512, 185) |

- **Number of 2D slices in the dataset:** 19,844

## Label Information Statistics

| Anatomy     | Total Cases | Coverage | Minimum Volume (cm³)  | Median Volume (cm³) | Maximum Volume (cm³) |
|-------------|-------------|----------|-----------------------|---------------------|----------------------|
| liver       | 224         | 100%     | 600.28                | 1391.05             | 2804.7               |
| liver tumor | 224         | 100%     | 3.94                  | 113.965             | 4054.63              |
| portal vein | 224         | 100%     | 3.29                  | 20.3                | 188.73               |
| aorta       | 224         | 100%     | 2.85                  | 10.71               | 126.53               |

## Visualization

<div align="center">
    <a href="https://github.com/openmedlab/"><img width="700px" height="auto" src="appendix/HCC-TACE-Seg_1.webp"></a>
</div>
<p style="text-align:center;font-size:10px;"><em>Red indicates the liver, green indicates liver tumors, small blue areas indicate the portal vein, and yellow indicates the aorta.</em></p>

## File Structure

In the repository, the `File Structures` directory contains the following files:
- `structure_level_1.txt`
- `structure_level_2.txt`
- `structure_level_3.txt`
- `structure_level_4.txt`

These files provide detailed information about the dataset structure at various levels.

## Source Information

- **Official Website:** [TCIA HCC-TACE-SEG Collection](https://www.cancerimagingarchive.net/collection/hcc-tace-seg/)
- **Download Link:** [HCC-TACE-SEG Dataset](https://www.cancerimagingarchive.net/collection/hcc-tace-seg/)
- **Publication Date:** August 2022

## Citation

Please cite the dataset using the following reference:

```
@article{moawad2021multimodality,
  title={Multimodality annotated HCC cases with and without advanced imaging segmentation [data set]},
  author={Moawad, A and Fuentes, D and Morshid, A and Khalaf, A and Elmohr, M and Abusaif, A and Hazle, JD and Kaseb, AO and Hassan, M and Mahvash, A and others},
  journal={The Cancer Imaging Archive},
  year={2021}
}
```

Original introduction article can be found [here](https://zhuanlan.zhihu.com/p/708599534).

---

For further details, contributions, or inquiries, please visit our [GitHub repository](https://github.com/openmedlab/).