This is the code for the translation experiments in the group submission to NLP Class CS 263, "Rewarding Near-Misses: The Effect of Adding an Embedding Distance Loss Term on the Training of Language Models".

To set up this code:
1. Clone the repo and navigate to its folder.
2. Set up the code environment using conda: run the following lines in your Anaconda Prompt, which should create an environment named "translation". Unfortunately this might cause some of the packages to not install due to dependency issues, but ignore those until step 5.
```conda env create -f environment.yml```
3. Activate environment:
```conda activate translation```
4. The current file should only have base torch packages without configuration for GPU usage. If you are using a GPU, download the torch package specific to your GPU driver. If you are using CPU, ignore this step.
5. In order to obtain the data from the figures in the translation task experiments, run all cells in "NLP_translation_word_aware_toggle.ipynb". If any of the packages needed are missing, refer to the version listed in environment.yml, and then manually install those versions using pip (e.g., ```pip install allennlp==2.10.1```). Data from the runs and hyperparameter lambda sweep will be saved in a folder called "logs". When running on GPU, the code should take between 2-3 hours to run.
6. In order to generate the translation figure from the writeup, run all cells in "generate_figures.ipynb" after running "NLP_translation_word_aware_toggle". They will be rendered in the jupyter notebook.