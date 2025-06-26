# Brain Tumor Segmentation using YOLOv11 and SAM2

## 📌 Project Overview

This project aims to perform **brain tumor segmentation** using a hybrid pipeline that combines **YOLOv11** (for object detection) and **SAM2** (for mask segmentation). The goal is to accurately detect and segment various types of brain tumors in MRI images.

### 🎯 Objectives

* Detect tumors using YOLOv11
* Segment tumor regions using SAM2
* Generate labeled masks for visualization and analysis
* Save all outputs including predictions, masks, and model checkpoints

---

## 📁 Dataset

The dataset contains MRI images labeled with the following classes:

* `NO_tumor`
* `glioma`
* `meningioma`
* `pituitary`
* `space-occupying lesion-`

**Folders:**

* `/train/images`
* `/test/images`
* `/valid/images`

  ** Dataset Link:**
  * https://drive.google.com/drive/folders/1P4vuXwAPJO8oWuzrMBZ2wQALZCmzmHse?usp=drive_link

---

## ⚙️ Technologies & Tools

* Python
* Google Colab
* YOLOv11 (Ultralytics)
* SAM2 (Segment Anything Model)
* OpenCV, Matplotlib, PyTorch

---

## 🧠 Model Workflow

### 1. Mount Drive and Load Dataset

Mounted Google Drive and loaded image data for training, validation, and testing.

### 2. YOLOv11 Training

* Loaded YOLOv11 (`yolo11n.pt`)
* Trained using custom `data.yaml`
* Saved weights: `runs/detect/train3/weights/best.pt`

### 3. YOLOv11 Inference

* Performed object detection on test images
* Saved outputs and bounding boxes with class labels to JSON

### 4. SAM2 Segmentation

* Loaded YOLO-predicted bounding boxes
* Used SAM2 to generate masks for each bounding box
* Overlayed masks and labels on original images

### 5. Saved Results

* Masks saved to `/sam_segmented_results/`
* JSON results saved for analysis

---

## 🖼️ Visual Outputs

* YOLO loss and accuracy graphs
* Labeled bounding box predictions
* Masked tumor regions with class labels

---

## 📚 References

* [Ultralytics YOLOv8 Docs](https://docs.ultralytics.com)
* [SAM: Segment Anything GitHub](https://github.com/facebookresearch/segment-anything)
* YouTube tutorials on YOLO training and segmentation

---

## 👤 Author

**Name:** Saqib Hussain
**Email:** saqibhussain151214@gmail
**LINKEDIN ID:** https://www.linkedin.com/in/saqib-hussain-435b3a208/

---

> "Detection locates the tumor, segmentation defines its shape."
