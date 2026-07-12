# ⭐ Week 4 Report — Azure Cloud Foundations & ADF Pipeline  
**Celebal Summer Internship 2026 · Data Engineering Track**

---

## 🔍 Weekly Focus

This week centered on assembling core Azure components—Resource Group, Storage Account, and Blob Container—and designing a functional Azure Data Factory pipeline.  
The pipeline ingests the Superstore CSV from Blob Storage, performs a metadata validation step, and then copies the file to a new output path.

---

## 📁 Contents Included

- **Week4_CEI_Subham.Singhania_CT_CSI_DE_946.pdf**  
  Detailed documentation with screenshots for Tasks 1–5 and the Mini Project.

---

## 🔧 Pipeline Structure

### `ss_pipeline`
**Get Metadata1** → **ForEach1** → *(Copy data1 inside the loop)*

Key actions:
- Reads `Superstore_raw.csv` from `superstore-container`
- Metadata step inspects file/child items before processing

---

## 🏗️ Azure Resources Used

| Component        | Identifier              |
|------------------|--------------------------|
| Resource Group   | `resogp-cei-w4`          |
| Storage Account  | `storceiw4`              |
| Blob Container   | `superstore-container`   |
| Data Factory     | `adf-cei-w4`             |
| Linked Service   | `ls_superstore_blob`     |

---

## ✅ Completion Status

All assigned tasks (1–5) and the Mini Project were completed successfully.  
The pipeline executed end‑to‑end without errors, validating metadata and copying the file as expected.

---
