

# **Towards Robust Multimodal Sentiment Analysis with Incomplete Data**

## 🧠 Project Description

This project implements the **Language-dominated Noise-resistant Learning Network (LNLN)** for robust multimodal sentiment analysis under incomplete or noisy data conditions. The model enhances sentiment prediction by emphasizing language as the dominant modality while correcting and reconstructing missing information from other modalities.

---

## 🧩 Model Architecture

<img width="970" height="500" alt="image" src="https://github.com/user-attachments/assets/9ae6e16e-f859-45d1-8eac-c909b142576b" />

---

## 🚀 How to Run the Code

### 1. **Prepare the Dataset**

Before running the notebook, make sure the dataset is correctly placed in your Google Drive with the following folder structure:

```
MyDrive/
└── mmsa_data/
    └── MOSI/
        └── unaligned_50.pkl
```

You can download the required `.pkl` dataset files from this Google Drive link:
🔗 [https://drive.google.com/drive/folders/1A2S4pqCHryGmiqnNSPLv7rEg63WvjCSk](https://drive.google.com/drive/folders/1A2S4pqCHryGmiqnNSPLv7rEg63WvjCSk)

---

### 2. **Run the Notebook**

Open and run the **`DA241.ipynb`** file in Google Colab.

* You will be prompted to **authorize access to Google Drive** — please grant permission so the notebook can load the dataset.
* The notebook includes all necessary commands for training and evaluation.

---

### 3. **Train the Model**

Inside the notebook, training is initiated automatically via the following bash script command:

```bash
!bash train.sh
```

This will start the training process using the specified configuration.

---

### 4. **Evaluate the Model**

To evaluate the trained model on specific metrics, run the evaluation script (already included in the notebook):

```bash
!python robust_evaluation.py --config_file configs/eval_mosi.yaml --key_eval Non0_acc_2
```

This command evaluates model performance using predefined evaluation configurations for the MOSI dataset.

---

### ✅ Notes

* Ensure all dependencies are installed within the Colab environment before running training or evaluation cells.
* The notebook handles setup automatically, but you may review and adjust paths if running locally.
* You may change the `--key_eval` argument to switch between evaluation metrics defined in the config file.

---

## 📘 Reference
**Zhang et al. (2024)**, *"Towards Robust Multimodal Sentiment Analysis with Incomplete Data"*, NeurIPS 2024.
[[Paper Link]](https://openreview.net/pdf?id=mYEjc7qGRA) 

---

