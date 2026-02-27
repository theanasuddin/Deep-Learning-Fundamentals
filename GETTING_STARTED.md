# _Computer Exercises — Setup & Getting Started Guide_

All exercises are implemented in **Python 3** and provided in **Jupyter Notebook** format. The exercises use **PyTorch** as the primary deep learning framework.

The guide below explains how to set up your environment, run the notebooks, and work efficiently whether you use a **local machine**, **Conda**, or **Google Colab**.

----------

## **1. Getting Started with the Exercises**

All exercises are implemented in Python and delivered as Jupyter Notebooks.  
You will use **PyTorch** throughout the course. If you are new to PyTorch, the following tutorials are recommended:

### **PyTorch Basics**

-   [https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html](https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html)

### **Exercise‑Specific Tutorials**

-   Convolution arithmetic — [https://arxiv.org/abs/1603.07285](https://arxiv.org/abs/1603.07285)
-   Understanding LSTMs — [https://colah.github.io/posts/2015-08-Understanding-LSTMs/](https://colah.github.io/posts/2015-08-Understanding-LSTMs/)
-   Illustrated Transformer — [https://jalammar.github.io/illustrated-transformer/](https://jalammar.github.io/illustrated-transformer/)
-   Intro to GANs — [https://towardsdatascience.com/a-basic-intro-to-gans-generative-adversarial-networks-c62acbcefff3](https://towardsdatascience.com/a-basic-intro-to-gans-generative-adversarial-networks-c62acbcefff3)

### **Matrix Algebra Resources**

-   Matrix Calculus — [https://www.doc.ic.ac.uk/~ahanda/referencepdfs/MatrixCalculus.pdf](https://www.doc.ic.ac.uk/~ahanda/referencepdfs/MatrixCalculus.pdf)
-   Matrix Cookbook — [https://www.math.uwaterloo.ca/~hwolkowi/matrixcookbook.pdf](https://www.math.uwaterloo.ca/~hwolkowi/matrixcookbook.pdf)
-   Matrix Algebra for Statistics — [https://tminka.github.io/papers/matrix/minka-matrix.pdf](https://tminka.github.io/papers/matrix/minka-matrix.pdf)

Exercises can be completed on **CPU**, but **GPU is strongly recommended** for Exercises 2–6.  
If you do not have a local GPU, you may use **Google Colab**.

----------

## **2. Setup Guideline**

This section explains how to configure your environment for running the exercises.

If you plan to use **Google Colab for all exercises**, you may skip directly to **Section 4**.

----------

## **3. Setting Up a Conda Environment**

Conda allows you to create isolated environments to avoid dependency conflicts.

### **Step 1 — Install Conda**

Download and install Anaconda from the official website (platform‑specific installers available).

### **Step 2 — Create a New Environment**

```bash
conda create -n dl_course python=3.9
conda env list

```

### **Step 3 — Activate the Environment**

```bash
conda activate dl_course

```

### **Step 4 — Install PyTorch**

Installation depends on your OS and hardware.  
Use the official selector: [https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/)

Example (CPU‑only, Windows):

```bash
conda install pytorch torchvision torchaudio cpuonly -c pytorch

```

### **Step 5 — Install Required Packages**

```bash
conda install matplotlib
pip install notebook
pip install tqdm
pip install librosa
conda install seaborn
pip install pandas
pip install wordcloud
pip install transformers

```

----------

## **4. Working with Jupyter Notebook**

### **Step 1 — Launch Jupyter**

```bash
jupyter-notebook

```

A browser tab will open automatically. If not, use the URL shown in the terminal.

### **Step 2 — Running the Notebooks**

-   Navigate to the folder containing the `.ipynb` files.
-   Run cells **in order** (Shift + Enter).
-   Do not skip cells, as many define variables or helper functions.

----------

## **5. Working with Google Colab (Recommended for GPU)**

Google Colab provides free GPU access and comes with many libraries pre‑installed.

### **Steps to Use Colab**

1.  Open: `https://colab.research.google.com` [(colab.research.google.com in Bing)](https://www.bing.com/search?q=%22https%3A%2F%2Fcolab.research.google.com%2F%22)
2.  Sign in with your Google account.
3.  Upload the exercise notebook (`File → Upload notebook`).
4.  Click **Connect**, then **Change runtime type**.
5.  Select **T4 GPU** as the hardware accelerator.
6.  Run the notebook normally.
7.  After finishing, download:
    -   The updated `.ipynb` file
    -   Any trained model files

> **Important:** Colab sessions are temporary. Files stored on the VM are lost when the session ends. Always download your work before closing.

----------

## **6. Important Notes**

### **Note 1 — Only Modify Marked Sections**

Exercises include template code.  
Implement code **only** inside blocks marked:

```python
# YOUR CODE HERE

```

Do not modify:

-   Read‑only cells
-   Default value cells
-   Any other template code

If you need extra space, insert new cells, but remove them before submission.

----------

### **Note 2 — Provided Tests**

The notebooks include test cases to help you verify your implementation. 

----------

### **Note 3 — Colab Sessions Are Temporary**

Colab assigns a temporary VM.  
If you close the session:

-   Datasets
-   Saved models
-   Notebook progress

…will be lost unless downloaded manually.

Always save your work before disconnecting.
