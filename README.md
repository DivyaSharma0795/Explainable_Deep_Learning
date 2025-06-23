# Hypothesis Testing using Explainable Deep Learning on Adversarial Examples

## Project Overview

This project explores **explainable deep learning techniques** to test the impact of adversarial attacks on feature importance in a Convolutional Neural Network (CNN) trained for digit recognition using the MNIST dataset. Specifically, it investigates whether adversarial perturbations meaningfully alter what the model deems important when making predictions.

The study combines **hypothesis testing** with **saliency map visualizations** to determine whether a trained model’s decision-making process changes in the presence of adversarial examples.

---

## Objective

To test the hypothesis:

* **Null Hypothesis (H₀):** The CNN does not exhibit significant differences in feature importance between clean and adversarially perturbed inputs.
* **Alternative Hypothesis (H₁):** The CNN exhibits significant differences in feature importance between clean and adversarially perturbed inputs.

The aim is to verify whether adversarial images not only attempt to mislead the model’s predictions but also shift the model’s internal focus on different image features.

---

## Workflow and Explanation

### 1. Model Training

* Trained a **Convolutional Neural Network (CNN)** on the MNIST dataset for handwritten digit recognition.
* The model achieved good accuracy on the test set, indicating reliable baseline performance.

### 2. Adversarial Attack Generation

* Applied the **Fast Gradient Sign Method (FGSM)** to generate adversarial examples.
* FGSM perturbs the input image in the direction that maximizes the model’s loss, simulating a targeted adversarial scenario.
* Purpose: To introduce controlled perturbations and assess whether the model’s feature importance changes under attack.

### 3. Explainability via Saliency Maps

* Generated **saliency maps** for both clean and adversarial images.
* Saliency maps highlight the pixels the model focuses on when making predictions.
* Purpose: To visually and quantitatively compare which features (pixels) are most influential before and after perturbation.

### 4. Model Prediction Analysis

* Compared predictions on clean vs. adversarial images:

  * **Clean Image Prediction:** Correctly classified as ‘7’
  * **Adversarial Image Prediction:** Also classified as ‘7’
* Result: The adversarial example did not fool the model, indicating robustness to this specific perturbation.

### 5. Hypothesis Testing and Conclusion

* Visual inspection of the saliency maps revealed **no significant difference in feature importance** between clean and adversarial images.
* Based on the results, **the Null Hypothesis was not rejected.**
* The model remained consistent in its attention patterns and prediction outcome.

---

## Key Takeaways

* The CNN demonstrated **robustness to FGSM adversarial examples** in this instance.
* **Saliency maps** provided an interpretable window into the model’s decision-making process, showing consistent focus on relevant image regions even after adversarial perturbation.
* Explainable AI (XAI) techniques like saliency maps are valuable tools for **validating model reliability under adversarial conditions.**


---

## Future Directions

* Test additional adversarial attack methods (e.g., PGD, DeepFool) for broader validation.
* Quantify saliency map differences using pixel-level similarity metrics or structural similarity index (SSIM).
* Evaluate model robustness across a wider variety of images and perturbation strengths.
* Compare saliency-based methods with other explainability tools like SHAP or LIME in the context of adversarial analysis.

---

## Contact

For questions or collaboration, please contact **Divya Sharma** via LinkedIn or email.
