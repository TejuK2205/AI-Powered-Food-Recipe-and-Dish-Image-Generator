# AI-Powered Food Recipe and Dish Generation

This project combines **Object Detection (YOLOv3)**, **Natural Language Processing (LaMini-GPT)**, and **Generative Adversarial Networks (GANs)** to automatically:

1. Detect food ingredients from an input image  
2. Generate a complete recipe using those ingredients  
3. Generate a realistic dish image using a trained GAN  

---

## Project Motivation

Modern kitchens are full of ingredients, but home cooks often lack ideas on what to cook. This project solves that by turning an image of ingredients or a dish into:

- A **detailed recipe** (using NLP)  
- A **realistic food image** (using a GAN)  

This automation helps:
-  Home cooks looking for quick suggestions  
-  Food bloggers/chefs generating content  
-  Recipe apps improving UX with visual suggestions  

---

##  Project Components

### 1. Ingredient Detection (Object Detection)
- **Model Used**: YOLOv3  
- **Dataset**: COCO (pre-trained)  
- **Libraries**: OpenCV  
- **Output**: List of food-related ingredients detected from the input image  

### 2. Recipe Generation (Natural Language Processing)
- **Model Used**: `MBZUAI/LaMini-GPT-774M`  
- **Library**: HuggingFace Transformers  
- **Input**: Detected ingredients  
- **Output**: Recipe with:  
  - Title  
  - Preparation & Cooking Time  
  - Ingredient Quantities  
  - Instructions  
  - Serving Suggestion & Nutrition Tip  

### 3. Dish Image Generation (Generative Adversarial Network)
- **Model Type**: DCGAN  
- **Dataset**: Food-101  
- **Framework**: PyTorch  
- **Input**: Random noise vector  
- **Output**: Synthetic dish image  

---

## Installation & Setup
 Requirements
1. Python 3.8+
2. PyTorch
3. OpenCV
4. Transformers
5. torchvision
6. matplotlib

---

## Folder Structure
```plaintext

project/
├── yolov3.cfg
├── yolov3.weights
├── coco.names
├── food-101/
│   └── images/
├── cpu_generator.pth
├── generate_recipe.py
├── train_gan.py
```
---

## Sample Output

**Detected Ingredients:**
Detected Ingredients: tomato, onion, lettuce

**Generated Recipe**
Fresh Veggie Sandwich
Prep Time: 10 mins
Cook Time: 5 mins
Ingredients:
- 2 slices of bread
- 1 tomato
- 1 onion
- Lettuce leaves
Instructions:
1. Slice vegetables.
2. Toast bread.
3. Assemble and enjoy!
   
**Generated Dish Image**
(Displayed from GAN model output - sample shown in UI)

---

## Models Used

| Task                  | Model           | Dataset    |
| --------------------- | --------------- | ---------- |
| Object Detection      | YOLOv3          | COCO       |
| Recipe Generation     | LaMini-GPT-774M | Pretrained |
| Dish Image Generation | DCGAN           | Food-101   |

---

## Future Improvements
1. Real-time ingredient detection from webcam
2. Use Stable Diffusion for HD food image generation
3. Integrate voice commands using speech-to-text

---

## 👩‍💻 Author

**Tejaswini K**  
B.Tech Artificial Intelligence & Data Science  
Madras Institute of Technology, Anna University  

- 📧 [tejaswinik2205@gmail.com](mailto:tejaswinik2205@gmail.com)  
- 🌐 [GitHub](https://github.com/TejuK2205)  
- 💼 [LinkedIn](https://www.linkedin.com/in/tejaswini-k-6416b0263/)

---

## License
This project is for educational purposes only. All models used are open-source under their respective licenses.

---
