# Jupyter Notebooks

## Description

Each of these notebooks performs a task for the material classification workflow.

**The basic workflow:**
1) Run the SAM mask generation script
2) Run the ChatGPT batch classification script
3) Run the script to apply masks to the model

## Requirements

- You must make an account with Matterport and request access to their dataset that contains the original scan photos and positions. They have a separate dataset for this, which can be accessed via a python script that they provide which allows you to download individual scans. [More information](https://niessner.github.io/Matterport/).
- You will need an OpenAI API key and either a Colab instance with a GPU or your own system running Jupyter and a GPU (recommended, because otherwise the progress bars do not work). It is recommended to install Miniconda and create a conda environment within which all Python dependencies will live. You can open up the notebooks workspace in VS Code, activate the Conda environment, install juypter, then start the jupyter server and connect to it by attaching VS to the kernel at localhost. The requirements.txt file is referenced into each notebook and will automatically install any dependencies.
- A note on GPU support: CUDA is required to run the SAM script, assuming you want it to run at a reasonable speed. This being said, you can install torch without CUDA support and use the script in CPU only mode.


