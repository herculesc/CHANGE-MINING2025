# CHANGE-MINING2025

<p align="center">
  <img src="imagem/20250719_1447_Logo CHANGE-MINING2025_simple_compose_01k0hwnqxre78sp04cw5pqkehk.png" alt="CHANGE-MINING2025 Logo" width="250"/>
</p>

**CHANGE-MINING2025** is a dataset developed for **change detection tasks in mining areas**, focusing on **remote sensing** and **deep learning** applications.

> **Authors:** Hércules C. S. Pereira, Valdivino A. Santiago Júnior, Elcio H. Shiguemori

## 📦 Download

You can access and download the dataset via the link below:

🔗 [Click here to download the CHANGE-MINING2025 dataset](https://drive.google.com/drive/folders/1QcCsCtugA8Gv_HTcdKiE7ePBfu21Ko7R?usp=sharing)

## 📂 Dataset Description

The dataset consists of **bi-temporal Sentinel-2 image pairs** acquired at two distinct time points, with a **spatial resolution of 10 meters**. Each image pair is accompanied by a **binary change mask** indicating regions where mining-related changes occurred. Each sample includes:

- One image at time **T1** (year **2017**)  
- One image at time **T2** (year **2024**)  
- A **binary change mask**

## 🗂 Dataset Structure

The `CHANGE-MINING2025` dataset is organized as follows:

- 📁 **T1/**: Images from the first time point (2017)  
- 📁 **T2/**: Images from the second time point (2024)  
- 📁 **Change/**: Binary reference masks (`0` = no change, `1` = change)

Each sample contains a pair of multispectral Sentinel-2 images with **10-meter spatial resolution**, captured at two different times (**T1** and **T2**), along with a **binary mask** identifying areas with evidence of **mining activity over time**.

## 🛠️ Creation Process

The dataset was built through the following steps:

1. **Image acquisition** from Sentinel-2 via the [Copernicus Browser](https://browser.dataspace.copernicus.eu/)  
2. **Temporal selection** of the years **2017 (T1)** and **2024 (T2)**, with computation of the **SAVI spectral index** for each image  
3. **Change computation** by subtracting SAVI indices (T2 - T1), followed by **manual refinement** of the identified regions  
4. **Generation of the change mask**, with binary values:  
   - `0` = No change  
   - `1` = Change  
5. **Image cropping** into **128 × 128 pixel** patches using **QGIS**  
6. **Final organization** of the dataset into the three folders: `T1/`, `T2/`, and `Change/`

## 🚀 Applications

The CHANGE-MINING2025 dataset is ideal for:

- Training **deep learning models for change detection**  
- Land use and land cover studies focused on **mining activities**

## 📄 License

The **CHANGE-MINING2025** dataset is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/).

You are free to:

- **Share** — copy and redistribute the material in any medium or format  
- **Adapt** — remix, transform, and build upon the material  

**Under the following terms:**

- 📌 **Attribution** — You must give appropriate credit to the authors:  
  Hércules C. S. Pereira, Valdivino A. Santiago Júnior, Elcio H. Shiguemori  
  Suggested citation:  
  > *CHANGE-MINING2025: A Dataset for Change Detection in Mining Areas Using Sentinel-2 Images (2017–2024)*

- 🚫 **NonCommercial** — Use is not permitted for commercial purposes.  

Full legal text available at: [https://creativecommons.org/licenses/by-nc/4.0/legalcode](https://creativecommons.org/licenses/by-nc/4.0/legalcode)

---

📌 *For more information, please refer to the associated publication or contact the project authors.*
