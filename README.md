# 🏭 SAM2 + YOLO Industrial Product Detection

A comprehensive deep learning project for detecting industrial products using **YOLO v11** models trained on datasets annotated with **SAM 2** (Segment Anything Model 2).

## 📋 Project Overview

This project combines two powerful AI models:
- **SAM 2 (Segment Anything Model 2)**: For automated annotation and object tracking in videos
- **YOLOv11**: For real-time industrial product detection

The workflow includes:
1. **Video annotation** using SAM 2 for automatic object tracking
2. **Dataset generation** in YOLO format
3. **Model training** with YOLOv11 (Nano and Small variants)
4. **Inference** on images and videos with real-time detection capabilities


---

## 🔄 Workflow Summary

1. VIDEO ANNOTATION (SAM 2)
   video_detector.ipynb
   ↓
   → Interactive frame selection
   → Automatic object tracking
   → YOLO format export

2. DATASET PREPARATION
   industrial_product_dataset/
   ↓
   → Images (train/val split)
   → Annotations (YOLO .txt format)
   → data.yaml configuration

3. MODEL TRAINING
   train_yolo.ipynb
   ↓
   → YOLOv11n training
   → YOLOv11s training
   → Performance metrics

4. INFERENCE & DEPLOYMENT
   inference.ipynb or inference_video.ipynb
   ↓
   → Load trained weights
   → Run predictions
   → Visualize results
   → Export outputs

## 📝 License

This project uses:
- **YOLOv11**: Ultralytics (AGPL-3.0)
- **SAM 2**: Meta (Apache 2.0)

Ensure compliance with respective licenses for your use case.


---

## 🎓 References

- [YOLOv11 Documentation](https://docs.ultralytics.com/models/yolov11/)
- [SAM 2: Segment Anything Model 2](https://github.com/facebookresearch/sam2)
- [YOLO Format Specification](https://docs.ultralytics.com/datasets/detect/)
- [ONNX Format](https://onnx.ai/)

---

**Last Updated**: December 2025  
**Status**: ✅ Complete and Production Ready
