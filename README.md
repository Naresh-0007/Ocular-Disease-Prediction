# 📊 Ocular Disease Prediction

## 📖 Chapter 1: Objective

This project aims to develop an automated, accurate, and reliable system for diagnosing ocular diseases using deep learning on fundus images. By leveraging advanced deep learning architectures, we address challenges in manual diagnosis—such as cost, time, and human error—that can delay treatment and worsen outcomes for patients. 

### 🎯 Key Goals
1. **Designing a High-Performance Classification System:** Implement and benchmark models like VGG19, ResNet50, and Vision Transformer to evaluate accuracy, loss, and generalization in diagnosing diseases from fundus images.
2. **Enhancing Feature Extraction Using Local Binary Pattern (LBP):** Integrate LBP to improve texture recognition in images, helping detect subtle disease indicators.
3. **Handling Class Imbalance:** Use techniques such as data augmentation and synthetic image generation to improve performance across all classes.
4. **Evaluating Model Performance with LBP Preprocessing:** Compare model metrics with and without LBP preprocessing.
5. **Scalability for Clinical Applications:** Explore fine-tuning and transfer learning for broader adaptability and clinical relevance.

## 📚 Chapter 2: Introduction

With over 2.2 billion people affected by vision impairment, early diagnosis of ocular diseases is critical. Fundus imaging captures retina details, aiding in the diagnosis of conditions like cataracts, glaucoma, and diabetic retinopathy. However, manual analysis of fundus images requires expertise and time, and resource limitations can delay diagnosis. Our deep learning-based system leverages convolutional and transformer models to automate the classification of ocular conditions, ultimately contributing to better patient outcomes and efficient healthcare resource allocation.

## ✨ Key Features of the Project
1. **Automated Diagnostic System:** Use of deep learning to reduce human error and enhance efficiency.
2. **Deep Learning Architectures:** Comparison of VGG19, ResNet50, and Vision Transformer for classifying ocular conditions.
3. **Enhanced Feature Extraction:** Integration of Local Binary Pattern (LBP) to improve model accuracy by identifying subtle indicators in images.
4. **Class Imbalance Management:** Apply augmentation techniques to improve reliability across diverse disease categories.
5. **Performance Evaluation:** Comparison of models with and without LBP preprocessing.

## 📚 Chapter 3: Literature Review

**Summary of Techniques:**
- **Traditional Methods:** Handcrafted features and machine learning techniques like SVM and KNN were once standard but lacked sufficient generalization.
- **Convolutional Neural Networks (CNNs):** VGG19 and ResNet50 improved image analysis, with VGG19 capturing spatial details and ResNet50 addressing gradient issues with residual connections.
- **Vision Transformers (ViTs):** ViTs process images as sequences of patches, allowing for long-range dependencies in visual data.
- **Local Binary Pattern (LBP):** LBP enhances texture analysis, making it effective in detecting disease markers like cataracts and glaucoma.

## ⚙️ Chapter 4: Methodology

### 📅 Dataset
- **Data Source:** Kaggle ODIR dataset with 7,000+ fundus images representing various ocular conditions.
- **Class Distribution:** The dataset has natural imbalances across disease categories.
- **Preprocessing:** Images are converted to grayscale, with backgrounds removed to focus on retinal regions.

### 🔎 Feature Extraction Using LBP
- **LBP Process:** Each pixel is compared to neighbors to create binary patterns that capture local textures, improving the model's focus on disease-relevant patterns.

### 🏛️ Model Architectures
1. **VGG19:** A 19-layer CNN with pre-trained weights, effective for complex image details.
2. **ResNet50:** A CNN with residual connections that aids in capturing subtle image features without vanishing gradients.
3. **Vision Transformer (ViT):** Utilizes self-attention on image patches, modeling long-range dependencies.

### 🧪 Training and Testing
Models are trained with and without LBP features for comparative analysis, using metrics like accuracy, precision, recall, F1-score, and loss to evaluate model generalization.

## 📊 Chapter 5: Results

### Performance Without LBP
- **VGG19:** Achieved 93.58% validation accuracy with robust results even without LBP.
- **ResNet50:** Validation accuracy of 96.79%, though with slightly higher validation loss.
- **Vision Transformer:** Lagged in performance, indicating potential need for further tuning.

### Performance With LBP
- **VGG19:** Validation accuracy increased to 97.71%, demonstrating LBP's impact.
- **ResNet50:** Achieved 100% validation accuracy with lowest validation loss, showcasing improved generalization.
- **Vision Transformer:** Performance improved with LBP, though still behind CNNs, suggesting need for larger datasets or tuning.

## 🔍 Chapter 6: Conclusion and Future Scope

This study shows that CNNs (especially ResNet50 with LBP) perform effectively in ocular disease classification, providing robust and reliable diagnostics for medical imaging.

### 🌐 Future Scope
1. **Data Augmentation with GANs:** Generate synthetic images to balance dataset classes.
2. **Optimize Vision Transformers:** Fine-tune patch sizes and augment data to improve ViT performance.
3. **Clinical Application:** With additional validation, this model could aid clinicians in resource-limited settings.
4. **Multi-Stage Models:** Combining CNNs with Transformer encoders could capture local and global image details, improving diagnostic accuracy.
