🛳️ Ship Detection using Satellite Imagery
This project focuses on detecting ships from satellite images using advanced image segmentation techniques. It utilizes the Airbus Ship Detection Challenge dataset and implements a U-Net based segmentation model to accurately identify and segment ships in high-resolution satellite images.

🚀 Why Use U-Net for Ship Detection?
Ship detection from satellite images is a pixel-wise classification problem, where each pixel must be classified as either part of a ship or background. Here's why U-Net is particularly well-suited for this task:

🔹 1. Precise Localization
U-Net is specifically designed for semantic segmentation tasks.

Its encoder-decoder architecture enables it to learn high-level features and then recover spatial information for pixel-accurate predictions — essential for outlining ships accurately.

🔹 2. Works Well with Limited Data
U-Net performs excellently even with relatively small datasets, which is often the case in satellite imagery problems.

🔹 3. Handles Irregular Shapes
Ships in satellite images vary greatly in shape, size, and orientation.

U-Net's skip connections help it retain fine-grained details of ships during reconstruction, ensuring better shape detection.

🔹 4. Efficient & Lightweight
U-Net has fewer parameters than many other deep segmentation models, making it easier to train and deploy on resource-constrained systems.

📂 Dataset
• Source: Airbus Ship Detection Challenge

• Train Path: /kaggle/input/airbus-ship-detection/train_v2

• Test Path: /kaggle/input/airbus-ship-detection/test_v2

🧰 Libraries Used
• numpy, pandas — Data manipulation

• matplotlib, seaborn — Visualizations

• scikit-image — Image preprocessing & segmentation

• tensorflow or keras — U-Net model implementation

• gc, os, warnings — Environment & memory management

📊 Workflow
1. Setup & Imports: Import necessary libraries and configure environment.

2. Load & Visualize Images: Read images from the dataset and explore a few samples.

3. Image Preprocessing: Use morphological operations and segmentation to enhance image features.

4. Label Masks: Apply labeling to segment ship regions from the background.

5. Montage Creation: Build visual montages of ship masks and original images for analysis.

6. Model Building: Train a deep learning model for ship segmentation (e.g., U-Net, FCN).

7. Evaluation: Analyze model performance using metrics like IoU, Dice coefficient.

✅ Results
-> The U-Net model was able to detect and segment ships with high accuracy(91%).

-> Visual overlays showed precise boundary detection, even for small or partially visible ships.
• Dice Coefficient: 0.8164
• Validation Loss: 0.2260
• Estimated Accuracy: ~91%

📝 Notes
• This notebook is designed to run on Kaggle Kernels; update file paths accordingly for local execution.

• Future enhancements could include: 
      -> Use of pretrained backbones (ResNet, EfficientNet)
      -> Model ensembling
      -> Post-processing using Conditional Random Fields (CRFs)
