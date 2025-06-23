# Wildfire Classifier

This project utilizes computer vision and ML techniques to classify satellite images of wildfire regions.

---

## How to run this project

To proper configurate and run this project locally, run the following steps:



1. **Install Miniconda (if you don't have it yet)**
   
   This Project uses **Conda** to manage the environment and dependencies. I recommend installing **Miniconda**, a light version of Anaconda.
   
   - **Download**: Access the [official Miniconda download page](https://www.anaconda.com/docs/getting-started/miniconda/main) and download the installer for your operating system (Windows, macOS or Linux)
   
   - **Installing:** Run the installer and follow the steps.

2. **Clone the repository**
   
   Open your terminal, go to the folder where you wish to save your project and clone this repository.
   
   ```bash
   git clone https://github.com/GalafassiNAT/wildfire_classifier.git
   cd wildfire_classifier
   ```

3. **Create the Conda Environment**
   
   The file `environment.yml` has the necessary dependencies and libraries used to run this project. Conda will use this file to create a virtual env with everything ready.
   
   Run the following commando in your terminal, at the project's root:
   
   ```bash
   conda env create -f environment.yml
   ```
- **What it does?** This command reads `environment.yml`, creates a new env with the name specified inside the file (in this case `wildfire_env`) and installs all the dependencies automatically. \
  
  
  
  In case you install new libraries, don't forget to export the environment using the command:
  
  ```bash
  conda env export --from-history > environment.yml
  ```
  
  If you wish to update your environment, use the following command:
  
  ```bash
  conda env update --prefix ./env --file environment.yml --prune
  ```
4. **Activate the environment**
   
   After the creation, you need to "activate" the environment to start using it.
   
   ```bash
   conda activate wildfire_env
   ```

5. **Run the project**
   
   Run `Jupyter Notebook` at the project's root in your terminal, and open the file `Wildfire Classifier.ipynb`
