# 🌿 Plant Recognition Using YOLOv8

## Overview
This project focuses on classifying **10 houseplant species** using a **YOLOv8 model**, tackling challenges such as **complex pattern variations** and **subtle inter-class differences**. Through advanced dataset preparation, augmentation strategies, and hyperparameter tuning, the model achieves an **accuracy of 80%**.
The model is also **accessible via an API**, allowing users to send images and receive predictions remotely. 📌 See [API Access](#-api-access) for details.  
🌱 [Launch Demo →](https://huggingface.co/spaces/coralengel/plant-identifier-demo)

![image](https://github.com/user-attachments/assets/cfe4c5c6-a05d-49ae-9a29-a512d161e1f3) ![image](https://github.com/user-attachments/assets/0612585f-051e-4cb3-acc9-7a59858a6c6e) ![image](https://github.com/user-attachments/assets/b1ebf767-26cb-43ca-9563-a46a2fcde7a5)

### 🌿 Supported Plant Species
The model can classify the following plants:
- Aloe Vera
- Tradescantia
- Snake plant (Sanseviera)
- Peace lily
- Orchid
- Monstera Deliciosa
- Echeveria
- Ctenanthe
- Chinese Money Plant
- African Violet
  
## Project Goals
* Develop a **robust deep learning model** for plant species classification.
* Optimize dataset labeling using **Florence** and bounding box **normalization**.
* Address **underperforming classes** by analyzing classification errors and applying **oversampling** & **class weighting**.
* Apply targeted **augmentations** (color shifts, blur, contrast adjustments) to **simulate real-world conditions**.
* Fine-tune hyperparameters (IoU thresholds, learning rate, batch size) to enhance model stability.

## Technologies Used
* **Programming Language**: Python
* **Deep Learning Frameworks**: YOLOv8, OpenCV
* **Dataset Labeling**: Florence
* **Evaluation Metrics**: Precision-recall curves

## Repository Structure
* **train_set_creation.ipynb** - Dataset preparation, bounding box labeling, and normalization.
* **model_training.ipynb** - Training the YOLOv8 model with initial dataset.
* **oversampling_dataset_update.ipynb** - Handling underperforming classes with oversampling & class weighting.
* **model_inference.ipynb** - Running inference, evaluating precision-recall curves, and analyzing misclassifications.

## Project Outcomes
Upon completion of this project, you will have:

* Constructed a **high-quality dataset** using **Florence** for bounding box labeling and normalization, improving model consistency.
* Diagnosed and improved **underperforming classes** by applying **oversampling & class weighting**, enhancing class balance and model robustness.
* Applied **targeted augmentations** (color shifts, blurring, contrast adjustments) to **simulate real-world conditions** and improve generalization.
* Boosted model accuracy from **70% to 80%** through dataset refinements, augmentation strategies, and hyperparameter tuning.

## 🌍 API Access
This model is **accessible via an API**, allowing users to send images and receive predictions with a confidence level greater than 0.5.
To use the model for inference, follow the approach outlined in ```model_inference.ipynb```. The API processes uploaded images and returns predicted species along with bounding box coordinates.

## 🔧 Installation & Usage
####  1. Install Dependencies
Before running the notebooks, install all required libraries using:
```pip install -r requirements.txt```

####  2. Modify Google Drive Paths
hese notebooks use Google Drive as storage, so you'll need to update the ```base_path``` variable to your own directory.
Example:
```base_path = "/content/drive/MyDrive/YourProjectFolder/"```
