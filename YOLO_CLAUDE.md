

## Origins & History

The first version of YOLO was introduced in 2015. Over the past decade it has steadily consolidated its position within the object detection community, with the number of YOLO-related publications increasing consistently year after year. [arXiv](https://arxiv.org/html/2504.18586v1)

Before YOLO, researchers used CNN-based approaches like R-CNN and Fast R-CNN, which used a two-step process: predicting bounding boxes, then classifying objects inside them. This was slow and resource-intensive. [Viso.ai](https://viso.ai/computer-vision/yolo-explained/) YOLO's key breakthrough was reframing detection as a single regression problem — predicting bounding boxes and class probabilities in one pass. This unified architecture resulted in a significant improvement in inference speed while maintaining competitive accuracy, marking a turning point in object detection. [arXiv](https://arxiv.org/html/2504.18586v1)

The original YOLO was written by Joseph Redmon in a custom framework called Darknet — a very flexible research framework written in low-level languages. [Roboflow](https://blog.roboflow.com/guide-to-yolo-models/) It was presented at CVPR 2016 and won OpenCV's People's Choice Award.

---

## Model Release Timeline

**YOLOv1 — 2015**
Launched in 2015, YOLO gained popularity for its high speed and accuracy. [Ultralytics](https://docs.ultralytics.com/) It was the first single-shot, real-time object detector.

**YOLOv2 / YOLO9000 — 2016**
YOLOv2 improved the original model by incorporating batch normalization, anchor boxes, and dimension clusters. [Ultralytics](https://docs.ultralytics.com/) It could also detect over 9,000 object categories.

**YOLOv3 — 2018**
YOLOv3 further enhanced the model's performance using a more efficient backbone network, multiple anchors, and spatial pyramid pooling. [Ultralytics](https://docs.ultralytics.com/) It introduced the Darknet-53 architecture.

**YOLOv4 — 2020**
YOLOv4 introduced innovations like Mosaic data augmentation, a new anchor-free detection head, and a new loss function. [Ultralytics](https://docs.ultralytics.com/) It used CSPDarknet53 as its backbone.

**YOLOv5 — 2020**
Released by Ultralytics (Glenn Jocher). YOLOv5 further improved the model's performance and added new features such as hyperparameter optimization, integrated experiment tracking, and automatic export to popular formats. [Ultralytics](https://docs.ultralytics.com/) This was a pivotal release that moved YOLO into a more production-friendly, PyTorch-native framework.

**YOLOv6 — 2022**
A community release from Meituan focused on faster and more efficient real-time object detection with hardware-friendly design.

**YOLOv7 — 2022**
Introduced advanced model scaling and improved backbone design, achieving state-of-the-art results at the time of publication.

**YOLOv8 — 2023**
YOLOv8 featured a redesigned architecture with dynamic anchor-free detection. [Viso.ai](https://viso.ai/computer-vision/yolo-explained/) Released by Ultralytics, it became the dominant production model and unified detection, segmentation, pose estimation, and classification under one framework.

**YOLOv9 — February 2024**
On February 21st, 2024, Chien-Yao Wang, I-Hau Yeh, and Hong-Yuan Mark Liao released YOLOv9, which introduces Programmable Gradient Information (PGI). According to the research team, YOLOv9 achieves a higher mAP than existing popular YOLO models such as YOLOv8, YOLOv7, and YOLOv5 when benchmarked against MS COCO. [Roboflow](https://blog.roboflow.com/guide-to-yolo-models/)

**YOLO-World — February 2024**
Launched January 31st, 2024 and accepted at CVPR 2024, YOLO-World is a cutting-edge real-time open-vocabulary object detector. [GitHub](https://github.com/AILab-CVC/YOLO-World) It allows detection of arbitrary object categories via text prompts without retraining. In February 2025, a new YOLO-World-V2.1 was released, which includes new pre-trained weights and training code for image prompts. [GitHub](https://github.com/AILab-CVC/YOLO-World)

**YOLOv10 — May 2024**
Released on May 23, 2024, YOLOv10 is a real-time object detection model developed by researchers from Tsinghua University. It achieves lower latency than previous YOLO models with fewer parameters. [Roboflow](https://blog.roboflow.com/guide-to-yolo-models/) It was the first to pioneer native end-to-end NMS-free inference.

**YOLO11 — September 2024**
YOLO11 went through architectural refinements with a focus on enhancing computational efficiency without sacrificing accuracy. It introduces the C3k2 block and the C2PSA block, contributing to improved feature extraction and processing — slightly better performance with far fewer parameters. [Viso.ai](https://viso.ai/computer-vision/yolo-explained/)

**YOLOv12 — February 2025**
YOLOv12 marks a significant shift towards an attention-centric design, introducing the Area Attention (A2) module for efficient large receptive field processing, Residual Efficient Layer Aggregation Networks (R-ELAN) for enhanced feature aggregation, and architectural optimizations including FlashAttention and adjusted MLP ratios. [Springer](https://link.springer.com/article/10.1007/s10462-025-11253-3)

**YOLO26 — September 2025** *(current latest)*
On September 25th, at the annual hybrid event YOLO Vision 2025 in London, Glenn Jocher officially announced YOLO26 — the latest breakthrough in the Ultralytics YOLO series. [Ultralytics](https://www.ultralytics.com/blog/meet-ultralytics-yolo26-a-better-faster-smaller-yolo-model) Key innovations include:

- A streamlined design that removes unnecessary complexity. It is a native end-to-end model, producing predictions directly without the need for NMS. By eliminating this post-processing step, inference becomes faster, lighter, and easier to deploy. [Ultralytics](https://docs.ultralytics.com/models/yolo26/)
- The nano model now runs up to 43% faster on standard CPUs, making it especially well-suited for mobile apps, smart cameras, and other edge devices. [Ultralytics](https://www.ultralytics.com/blog/meet-ultralytics-yolo26-a-better-faster-smaller-yolo-model)
- A pioneering MuSGD optimizer combining SGD with Muon, inspired by Kimi K2 (Moonshot AI), bringing LLM-grade optimization stability to computer vision training. [GitHub](https://github.com/ultralytics/assets/releases)
- ProgLoss and STAL improve loss functions, increasing detection accuracy with notable improvements in small-object recognition — critical for IoT, robotics, and aerial imagery. [Ultralytics](https://docs.ultralytics.com/models/yolo26/)

---

## Ecosystem & Libraries Status (2026)

**Ultralytics Python Package**
The `ultralytics` package, installable via pip in a Python ≥ 3.8 / PyTorch ≥ 1.8 environment, is the primary SDK. It supports training, validation, inference, and export via both a CLI (`yolo predict model=yolo26n.pt`) and a Python API. [GitHub](https://github.com/ultralytics/ultralytics)

**Licensing**
Ultralytics offers two licensing options: AGPL-3.0 (open-source, for students/researchers) and an Enterprise License (for commercial embedding of YOLO into products and services). [GitHub](https://github.com/ultralytics/ultralytics)

**Export & Deployment**
YOLO26 supports flexible export options including ONNX, TensorRT, CoreML, and TFLite, as well as quantization for INT8/FP16. [arXiv](https://arxiv.org/abs/2509.25164) It runs on NVIDIA Jetson (Nano and Orin) and Raspberry Pi.

**Tasks Supported (across YOLO26 and YOLO11)**
YOLO26 is the first version to natively unify five key tasks: object detection, instance segmentation, classification, pose/keypoints detection, and oriented bounding box (OBB) detection. [arXiv](https://arxiv.org/html/2510.09653v2)

**Notable Integrations**
- Roboflow (dataset management + training pipelines)
- HuggingFace Spaces (YOLO-World demos)
- ComfyUI (YOLO-World integrated in July 2024) [GitHub](https://github.com/AILab-CVC/YOLO-World)
- FiftyOne computer vision toolkit
- Docker / Raspberry Pi OS

**Community & Research**
The YOLO family has fragmented into two tracks: the Ultralytics-maintained lineage (YOLOv5 → YOLOv8 → YOLO11 → YOLO26), focused on production readiness and deployment, and a community/academic track (YOLOv6, v7, v9, v10, v12, YOLO-World) that drives architectural research. Community-driven models have often prioritized experimental architectural features, while Ultralytics models consistently emphasize exportability, quantization, and production-ready APIs. [arXiv](https://arxiv.org/html/2510.09653v2)

