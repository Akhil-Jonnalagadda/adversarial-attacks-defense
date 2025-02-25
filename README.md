
# **Adversarial Attacks and Defenses in Machine Learning**  

## **Overview**  
This project explores how deep learning models can be fooled by adversarial attacks and how to defend against them. We use the MNIST dataset to train a victim model and test different defense strategies against adversarial examples generated using the **Fast Gradient Sign Method (FGSM)**.  

## **Defense Methods Tested**  
1. **Input Preprocessing** – Normalizes inputs to reduce adversarial effects.  
2. **Adversarial Training** – Trains the model with adversarial examples for better robustness.  
3. **Randomization** – Adds randomness to make attacks less effective.  
4. **Feature Denoising** – Removes adversarial noise from inputs.  

## **Results**  
| Defense Mechanism      | Accuracy (Clean) | Accuracy (Attacked) | Attack Success Rate |
|------------------------|-----------------|----------------------|---------------------|
| No Defense            | 98.1%           | 12.3%                | 87.7%               |
| Input Preprocessing   | 97.9%           | 32.1%                | 68.4%               |
| Adversarial Training  | 95.2%           | 98.4%                | **1.53%**           |
| Randomization        | 94.9%           | 51.7%                | 48.2%               |
| Feature Denoising    | 97.7%           | 52.5%                | 47.4%               |

🔹 **Adversarial training** was the most effective defense, reducing attack success to just **1.53%**.  

## **How to Run**  
1. Clone this repo:  
   ```bash
   git clone https://github.com/Akhil-Jonnalagadda/adversarial-attacks-defense.git
   cd adversarial-defense-ml
   ```
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Train the model and generate attacks:  
   ```bash
   python main.py
   ```
4. Test defense strategies:  
   ```bash
   python evaluate_defenses.py
   ```

## **Requirements**  
- Python 3.x  
- TensorFlow  
- Keras  
- NumPy  
- Matplotlib  

