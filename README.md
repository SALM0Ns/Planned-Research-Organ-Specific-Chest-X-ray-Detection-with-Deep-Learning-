## Planned Research: Organ-Specific Chest X-ray Detection with Deep Learning  
Proposed Supervisor: Acting Sub Lt. Dr. Chaichana Kulworatit, Ph.D. Affiliation of Supervisor: King Mongkut’s Institute of Technology Ladkrabang (KMITL) 
Affiliation of Researcher: Kasetsart University, Faculty of Science, Department of Computer Science

## The researcher has completed the following ethics and research conduct certifications from the Collaborative Institutional Training Initiative (CITI Program)
demonstrating readiness to conduct research involving medical imaging and human-related data in compliance with international standards:

1.	Good Clinical Practice (GCP) – U.S. FDA Focus
CITI Program – Stage 1: Clinical Trials with Investigational Drugs and Devices

2.	Responsible Conduct of Research for Engineers (RCR)
CITI Program – Stage 1: Ethical Research Practices for Engineering Disciplines

3.	Human Subjects Research – Data or Specimens Only
CITI Program – Stage 2: Refresher Course (No direct interaction)

These certifications ensure the researcher’s competence in research ethics, human subject protection, data handling, and good clinical practices, all of which are crucial when conducting studies involving medical images such as chest X-rays.

1. Introduction and Motivation

Chest X-rays are one of the most commonly used imaging techniques for diagnosing pulmonary and cardiovascular diseases. However, accurately identifying and interpreting organ-specific structures such as the trachea, lungs, and heart in chest radiographs remains a challenge, especially in complex cases or when artifacts and overlapping tissues are present. Traditional algorithms often analyze the entire chest region, which can lead to misinterpretation or diluted focus when clinicians or AI models attempt to detect subtle anomalies in specific organs.

2. Research Objective

This research aims to develop a deep learning-based model capable of detecting and highlighting individual organs within chest X-ray images—particularly the lungs, trachea, and heart—while dimming or suppressing irrelevant anatomical structures. By enabling organ-specific visualization, the system will assist radiologists and downstream diagnostic models in improving accuracy, interpretability, and clinical decision support.

3. Methodology Overview
	•	Data Collection: Publicly available datasets such as NIH ChestX-ray14, VinDr-CXR, or JSRT will be used. Each image will be paired with segmentation masks or annotated bounding boxes when available.
	•	Preprocessing:
	•	Histogram normalization and CLAHE for contrast enhancement.
	•	Resize and standardize pixel resolution.
	•	Optional bone suppression preprocessing to reduce rib interference.
	•	Model Architecture:
	•	U-Net, DeepLabV3+, or custom encoder-decoder models will be explored for organ segmentation.
	•	Backbone networks such as ResNet or EfficientNet will be used for feature extraction.
	•	A refinement module may be added for enhancing boundary sharpness or overlapping area distinction.
	•	Training Strategy:
	•	Supervised training with Dice loss and/or focal loss for class imbalance.
	•	Data augmentation such as horizontal flipping, scaling, brightness variation, and simulated occlusion to improve generalization.
	•	Cross-validation to assess performance and prevent overfitting.
	•	Output:
	•	A visual output that highlights the selected organ while dimming or masking other regions.
	•	Optional: Heatmaps for uncertainty or anomaly highlighting in a selected organ.

4. Expected Outcomes
	•	A trained model that can isolate and enhance specific chest organs from X-ray images.
	•	Improved interpretability for AI-based diagnostic tools by focusing on a single organ at a time.
	•	Potential for use as a preprocessing step in disease classification pipelines (e.g., pneumonia in lungs, cardiomegaly in the heart).

5. Significance and Applications

By enabling organ-focused analysis, this research enhances diagnostic precision and model transparency. It supports better model explainability and aligns with clinical practice where focus is often organ-specific. The developed tool may serve as a modular plugin in existing medical imaging software or as a teaching tool for radiology students.



