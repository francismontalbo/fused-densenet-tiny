# Diagnosing Covid-19 Chest X-Rays with a Lightweight Truncated DenseNet with Partial Layer Freezing and Feature Fusion
<p> Author: Francis Jesmar P. Montalbo </p>
<p> Affiliation: Batangas State University </p>
<p> Email: francismontalbo@ieee.org </p>
<p><a href="https://francismontalbo.github.io">Personal Webpage</a></p> 
  
***:heavy_exclamation_mark:This GitHub repository serves as a support for an ACCEPTED article in Biomedical Signal Processing and Control (BSPC) ISSN: 1746-8094.*** 
***This is also a support for another article in MethodsX submission with an ISSN of 2215-0161. *** 
***This repository will be maintained and improved after all reviews are done for the use of the public. A video utorial will also be released soon for a faster and easier implementation***

# Graphical Abstract

<b>Made with <a target=_blank href="https://draw.io">draw.io</a></b>
<img src="/graphics/Montalbo_graphical_abstract_covid19.jpg" alt="Fused-DenseNet-Tiny" width="1000">

# Dataset: 
<p><a href="https://data.mendeley.com/datasets/9xkhgts2s6/1">Curated Dataset for COVID-19 Posterior-Anterior Chest Radiography Images (X-Rays).</a></p>
<h3>Citation</h3>
<p>SAIT, UNAIS; k v, Gokul Lal; Prajapati, Sunny; Bhaumik, Rahul; Kumar, Tarun; S, Sanjana; Bhalla , Kriti (2020), “Curated Dataset for COVID-19 Posterior-Anterior Chest Radiography Images (X-Rays).”, Mendeley Data, V1, doi: 10.17632/9xkhgts2s6.1 http://dx.doi.org/10.17632/9xkhgts2s6.1</p>

***:heavy_exclamation_mark:For a faster method, you may download the already prepared dataset used in the given link below.*** 

<a href="https://drive.google.com/drive/folders/1WVKRTS5Wg8FdL7GCKwebIUz9jXnKx9nH?usp=sharing">CLICK ME FOR THE PREPARED DATASET</a>

# How to use:
***:heavy_exclamation_mark:If training the model, the dependencies included a `tensorflow-gpu`. You may change the `tensorflow-gpu` to `tensorflow` if no GPU is to be used. However, the results from the paper were produced using a GPU (GTX 1070)***

Dependencies included in the `requirements.txt`: 
- jupyter==1.0.0
- keras==2.2.5
- matplotlib
- numpy==1.16.2
- opencv-python==4.4.0.42
- pandas==0.25.3
- Pillow==7.2.0
- scikit-learn
- scikit-image
- scikit-plot
- scipy
- tensorflow-gpu==1.14.0 (Note: This is optional and can train even with just a CPU or tensorflow non-gpu variant)

***:heavy_exclamation_mark: START HERE*** You may clone using git or download the repository and extract the files manually:
- Once cloned, CD into the folder and enter `pip install -r requirements.txt`. 
- After installation of the dependecies, there are two options to evaluate or use the model.

**First (easier):**
- Clone this repository or download as zip.
- Install the requirements on a newly created environment to prevent issues with other existing ones.
- Directly open the `model_evaluation.ipynb` and proceed with the evaluation. Then open the `model_tester.ipynb` to test it and you are done.
**The weight size of the model is only 10.3MB 😄 named as `fused_densenet_tiny.h5` inside the `weights/` folder.**

**Second (difficult):**
- Make sure to download the <a href="https://drive.google.com/drive/folders/1WVKRTS5Wg8FdL7GCKwebIUz9jXnKx9nH?usp=sharing">PREPARED dataset</a> and extract it to a folder within the `fused-densenet-tiny/` like `fused-densenet-tiny/dataset/`
- Clone this repository or download as zip.
- Install the requirements on a newly created environment to prevent issues with other existing ones.
- Open the `model_trainer.ipynb` and train.
- Once trained, you may now use the `model_evaluation.ipynb` and `model_tester.ipynb` and you are done.

**REMEMBER THIS IS A LONGER PROCESS (Second process) TO TEST AND SIMULATE THE MODEL**

## Performance Results

<table style="width:100%">
  <tr>
    <th>Model</th>
    <th>Accuracy</th> 
    <th>Precision</th>
    <th>Recall</th>
    <th>F1-Score</th>
  </tr>
  <tr>
    <td>Fused-DenseNet-Tiny</td>
    <td><strong>97.99%</strong></td>
    <td><strong>98.38%</strong></td>
    <td><strong>95.15%</strong></td>
    <td><strong>95.26%</strong></td>
  </tr>
</table>
