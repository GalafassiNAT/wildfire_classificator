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
   
   Run the following command in your terminal, at the project's root:
   
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

# About the project

This project is a **computer vision** and **machine learning** application that classifies satellite images of wildfire regions. It uses a dataset of images from the [Wildfire Dataset](https://www.kaggle.com/datasets/abhinavwalia95/wildfire-dataset) on Kaggle, which contains images of wildfires and non-wildfires.

## Technologies used

- **Python: 3.13.5**: The main programming language used in this project.
- **Jupyter Notebook**: An interactive environment for running Python code and visualizing results.
- **numpy** and **pandas**: Libraries for data manipulation and analysis.
- **Matplotlib** and **Seaborn**: Libraries for data visualization.
- **Joblib**: A library for saving and loading machine learning models. Also used to parallelize the training process and feature extraction.

## Methodology

The project follows a structured approach to classify wildfire images:
1. **Data Preparation**: Load and preprocess the dataset, such as converting them to grayscale.
2. **Feature Extraction**: Use Local Binary Patterns (LBP) and Gray Level Co-occurrence Matrix (GLCM) to extract features from the images.
4. **Hyperparameter Tuning**: Optimize the parameters of the feature extraction methods to improve model performance.
5. **Cross-Validation**: Split the dataset into training and testing sets to evaluate the model's performance.
6. **Model Training**: Train a machine learning model using the extracted features.
   - **Models Used**: 
     - **Random Forest**: A robust model for classification tasks.
     - **Support Vector Machine (SVM)**: A powerful model for high-dimensional data.
7. **Model Evaluation**: Evaluate the model's performance using accuracy, precision, recall, and F1-score metrics.
8. **Model Saving**: Save the trained model using Joblib for future use.
9. **Visualization**: Visualize the results using confusion matrices and classification reports.
10. **Plot Saving**: Save the plots generated during the analysis for future reference.

## Results

The project achieves a high accuracy in classifying wildfire images, demonstrating the effectiveness of computer vision and machine learning techniques in this domain. The results are visualized using confusion matrices and classification reports, providing insights into the model's performance. Further details on the results can be found in the Jupyter Notebook file `Wildfire Classifier.ipynb` as such with the comments made in the code and the generated plots saved in the `plots` folder.
