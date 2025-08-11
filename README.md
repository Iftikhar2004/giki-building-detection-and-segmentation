# GIKI Campus Building Detection and Segmentation using YOLOv8

##  Project Overview
This project detects and segments GIKI campus buildings in real time using a **custom dataset** and the **YOLOv8** architecture.  
The system can identify 14 different buildings and overlay segmentation masks for visual clarity.

---

##  Problem Statement
The aim is to train two deep learning models:
1. **YOLOv8 Detection** — Predict bounding boxes around buildings with their names.
2. **YOLOv8 Segmentation** — Predict bounding boxes + masks for each detected building.

---

##  Dataset
- **Source:** Recorded videos from GIKI campus.
- **Images:** 116 total (70% train, 20% val, 10% test).
- **Classes:**  
  `HBL_bank`, `Main_gate`, `auditorium`, `central_library`, `clock_tower`,  
  `faculty_of_Basics_Science`, `faculty_of_electrical_and_computer_science`,  
  `faculty_of_material_and_chemical_eng`, `faculty_of_mechanical_eng`,  
  `hostel_11`, `hostel_12`, `laundry_shop`, `new_academic_block`, `tuck`
- Annotated in **Roboflow** for object detection, then converted to segmentation masks.

---

## Methodology
1. **Data Collection** — Campus video footage.
2. **Annotation** — Bounding boxes in Roboflow.
3. **Segmentation Conversion** — Bounding boxes → polygon masks.
4. **Training** — YOLOv8 detection and YOLOv8-segmentation models.
5. **Evaluation** — Qualitative review of outputs.


##  Insights
- YOLOv8 detection performed strongly even on small dataset.
- Segmentation masks are rectangular (box-based), but still useful for multi-object scenes.
- Real polygon masks would further improve performance.

---

##  Files in Repository
- `Task2_GIKI_Building_Detection_Segmentation.ipynb` — Full training & inference code.
- `Report_Task2.pdf` — Detailed project report with visuals.
- `best_detection.pt` — Trained YOLOv8 detection model.
- `best_segmentation.pt` — Trained YOLOv8 segmentation model.
- `outputs/` — Sample images and videos.

---

##  Example Videos
- Detection: [View](outputs/detection_video.avi)
- Segmentation: [View](outputs/segmentation_video.avi)

---

