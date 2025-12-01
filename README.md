# 🏭 SAM2 + YOLO Industrial Product Detection

A comprehensive deep learning project for detecting industrial products using **YOLO v11** models. The core innovation is leveraging **SAM 2's Few-Shot Annotation capability** to eliminate tedious manual labeling. Simply click a few times on one video frame, and SAM 2 automatically generates hundreds of labeled samples by propagating masks across the entire video sequence.

## 📋 Project Overview

This project combines two powerful AI models:
- **SAM 2 (Segment Anything Model 2)**: Few-Shot video annotation with automatic object tracking
- **YOLOv11**: Real-time industrial product detection

### ⚡ The Game Changer: Few-Shot Annotation

Traditional object detection requires **thousands of manual bounding box annotations** - a tedious and expensive process. This project revolutionizes that workflow:

- **Traditional Approach**: 1,000+ images × 5-10 minutes per image = **80+ hours of manual labeling** 😫
- **SAM 2 Few-Shot Approach**: Click 2-3 times on ONE frame → SAM 2 generates 500+ labeled samples automatically ✨
- **Time Savings**: From **weeks of work** to **minutes** - up to **99% reduction in labeling time!**

### Workflow
1. **Few-Shot Video Annotation** using SAM 2 (automated propagation across frames)
2. **Dataset generation** in YOLO format (auto-export from segmentation masks)
3. **Model training** with YOLOv11 (Nano and Small variants)
4. **Inference** on images and videos with real-time detection capabilities


---

## 🔄 Workflow Summary

### 1️⃣ VIDEO ANNOTATION - FEW-SHOT WITH SAM 2 ⚡
*Notebook: `video_detector.ipynb`*

**The Magic**: Annotate once, generate hundreds of samples automatically!

↓
→ Select ONE frame + Click target objects (few-shot)
→ SAM 2 automatically tracks & segments across entire video
→ Auto-export to YOLO format

**Step 1: Original Frame**
![Original Frame](assets/frame_0.png)
*A frame from the original video showing industrial products on the assembly line.*

**Step 2: Few-Shot Interactive Segmentation**
![Annotation Step 1](assets/annotate_0.png)
![Annotation Step 2](assets/annotate_1.png)
*Just click 2-3 times to select the target object in the first frame. SAM 2 automatically detects and segments the product. No need to label any other frames!*

**Step 3: Automatic Propagation (The Heavy Lifting)**
![Segmentation Result 1](assets/segmentation_0.png)
![Segmentation Result 2](assets/segmentation_1.png)
*SAM 2 automatically tracks and propagates the mask across all video frames (potentially 500+ frames!), handling motion, occlusion, and all complexities without user intervention. Each frame = 1 labeled sample!*

**Step 4: Auto-Generated Dataset**
![Detected Objects](assets/detected_0.png)
*Final result: From a single short video clip (30 seconds), SAM 2 generates 500+ labeled samples ready for training. Bounding boxes are drawn from segmentation masks and automatically exported in YOLO format.*

**💡 Key Benefit**: Instead of manually labeling each frame, you spend just 5 minutes interacting → get a complete dataset!

---

### 2️⃣ DATASET PREPARATION (Auto-Generated)
*Folder: `industrial_product_dataset/`*

↓
→ Auto-generated images from video frames
→ Auto-generated annotations (YOLO .txt format)
→ Auto-generated data.yaml configuration

Data is automatically exported from SAM 2 segmentation masks into the standard YOLO format. **The entire process takes just minutes - no manual labeling required!**

---

### 3️⃣ MODEL TRAINING
*Notebook: `train_yolo.ipynb`*

↓
→ YOLOv11n training
→ YOLOv11s training
→ Performance metrics

Train different YOLO model variants using the auto-generated dataset.

**Training Results & Metrics:**
![Training Results](assets/results.png)
*Training performance charts - displaying mAP, precision, and recall across epochs.*

**Model Validation - Confusion Matrix:**
![Confusion Matrix](assets/confusion_matrix.png)
*Confusion matrix from validation set - detailed analysis of model classification performance.*

---

### 4️⃣ INFERENCE & DEPLOYMENT
*Notebook: `inference.ipynb` or `inference_video.ipynb`*

↓
→ Load trained weights
→ Run predictions
→ Visualize results
→ Export outputs

**Real-time Detection & Tracking Videos:**

#### 🎯 Detection - Bounding Boxes
Video displaying detection bounding boxes - YOLOv11 model detects industrial products with bounding boxes and confidence scores.

https://github.com/user-attachments/assets/fd112ef1-342d-4998-b609-31af2f5c2664

#### 📊 Counting & Tracking
Video with object counting and tracking - monitor product quantities across frames and count total detected products.

https://github.com/user-attachments/assets/c400e5e7-d652-4767-b8e3-a043d691ae5c

## 📝 License

This project uses:

Ensure compliance with respective licenses for your use case.



## 🎓 References


## 🙏 Acknowledgments



