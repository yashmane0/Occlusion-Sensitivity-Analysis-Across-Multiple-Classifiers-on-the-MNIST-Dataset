# README.md

## Project Title:
**Occlusion Sensitivity Analysis Across Multiple Classifiers on the MNIST Dataset**
<video src="[occlusion_map_animation.mp4](https://github.com/Occlusion-Sensitivity-Analysis-Across-Multiple-Classifiers-on-the-MNIST-Dataset)" width="100%" controls>
  Your browser does not support the video tag.
</video>

---

## Team Members
- **Member 1:** Saurabh Kumar Singh — Reg. No: 25-27-05
- **Member 2:** Yash Mane — Reg. No: 25-27-14
- **Member 3:** Aditya Manish Shrikhande — Reg. No: 25-14-10


---

## Files Included
- `project_final.ipynb` — Main project code and analysis  
- `DSTT-final-production.pptx` — Final presentation slides  
- `README.md` — Project documentation  
- `occlusion_map_animation.mp4` — Occlusion Map Animaion 
---
## How to Run the Project

### Run directly in Google Colab (recommended)
Open the project using the link below:

👉 **Colab Link:**  
https://colab.research.google.com/drive/1-ipn3Ekg3mkCXteKmCp4izkNBMxw08Dp?usp=sharing

No installation is required.

---
## Project Overview (Brief Write-up)

This project explores **Explainable AI (XAI)** by applying **occlusion sensitivity** across multiple machine learning models trained on the MNIST handwritten digit dataset. The goal is to understand how different classifiers respond to localized perturbations, and to visualize which parts of an input image most influence a model’s decision.

The models evaluated in this study include:

- **K-Nearest Neighbors (KNN)**
- **Decision Tree**
- **Gaussian Naive Bayes**
- **Multi-Layer Perceptron (MLP)**
- **Convolutional Neural Network (CNN)**

For each model, we compute **occlusion sensitivity maps**, which measure how the predicted class probability drops when a small region of the image is masked. These heatmaps highlight influential areas in the image.

Because Naive Bayes has an analytical log-likelihood structure, we also compute **per-pixel log-probability contributions** using a custom `nb_pixel_contrib()` function. This provides a **model-faithful** explanation not dependent on perturbations. For the CNN, we additionally use **Grad-CAM** to contrast gradient-based saliency with occlusion-based explanations.

Our results show that:
- **CNNs** produce meaningful spatial saliency due to convolutional receptive fields.  
- **Non-spatial models** (KNN, NB, DecisionTree, MLP) produce *feature sensitivity* rather than true visual attention.  

This highlights both the usefulness and limitations of occlusion sensitivity in XAI.

---

## Dependencies

This project requires the following libraries:

- Python 3.9+
- TensorFlow / Keras
- NumPy
- Matplotlib
- Scikit-learn
- (Optional) SHAP, LIME for extended XAI methods
- Google Colab / Jupyter Notebook

All dependencies are preinstalled in **Google Colab**.
