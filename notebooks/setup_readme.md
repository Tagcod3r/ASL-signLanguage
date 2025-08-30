# Project Setup and Running Instructions

This guide will walk you through setting up the environment and running the Jupyter notebooks for this project.

## Prerequisites

-   Windows operating system
-   Internet connection for downloading Anaconda

## Step 1: Download and Install Anaconda

1. Download Anaconda from the official website: https://www.anaconda.com/download
2. Run the installer and follow the installation wizard
3. Choose "Add Anaconda to PATH" during installation (recommended)
4. Complete the installation process

## Step 2: Open Anaconda Navigator

1. Press `Windows key` on your keyboard
2. Type "Anaconda Navigator" in the search bar
3. Click on "Anaconda Navigator" to launch the application
4. Wait for Anaconda Navigator to fully load

## Step 3: Create the Conda Environment

1. Open **Anaconda Prompt** (search for it in Windows search or find it in the Anaconda Navigator under "Environments" tab)
2. Navigate to the project directory where the `environment.yml` file is located:
    ```bash
    cd path/to/your/project
    ```
3. Create the environment using the provided environment.yml file:
    ```bash
    conda env create -f environment.yml
    ```
4. Wait for the environment creation process to complete (this may take several minutes)

## Step 4: Activate and Deactivate the Environment

### To Activate the Environment:

```bash
conda activate [environment_name]
```

_Note: Replace `[environment_name]` with the actual name specified in your environment.yml file_

### To Deactivate the Environment:

```bash
conda deactivate
```

## Step 5: Launch Jupyter Notebook

1. **Ensure your environment is activated** (see Step 4)
2. Launch Jupyter Notebook with the following command:
    ```bash
    jupyter notebook
    ```
3. Your default web browser will open automatically and display the Jupyter Notebook interface
4. Navigate to the project folder if not already there

## Step 6: Select the Correct Kernel Environment

1. Open any notebook file (`.ipynb`) in the Jupyter interface
2. In the notebook, click on **"Kernel"** in the top menu bar
3. Select **"Change Kernel"**
4. Choose the environment you created in Step 3 from the dropdown list
5. The kernel indicator (top-right corner) should now show your environment name

## Step 7: Prepare the Dataset

Before running the notebooks, ensure your dataset is properly organized:

1. Create a folder named `data` in the project root directory
2. Inside the `data` folder, create subfolders for each class/category (e.g., `A`, `B`, `C`, etc.)
3. Place the corresponding images in their respective subfolders

**Expected folder structure:**

```
project/
├── data/
│   ├── A/
│   │   ├── image1.jpg
│   │   ├── image2.jpg
│   │   └── ...
│   ├── B/
│   │   ├── image1.jpg
│   │   ├── image2.jpg
│   │   └── ...
│   ├── C/
│   │   ├── image1.jpg
│   │   ├── image2.jpg
│   │   └── ...
│   └── ...
├── environment.yml
├── notebook1.ipynb
├── notebook2.ipynb
└── README.md
```

## Step 8: Run the Notebooks

1. With the correct kernel selected, you can now run the notebook cells
2. Use `Shift + Enter` to run individual cells
3. Or use **"Cell" → "Run All"** to run all cells in the notebook
4. Follow any specific instructions within the individual notebooks

## Troubleshooting

### Common Issues:

-   **Environment not showing in Jupyter kernel list**:

    -   Make sure you activated the environment before launching Jupyter
    -   Try installing ipykernel: `conda install ipykernel`

-   **Package import errors**:

    -   Verify that the environment was created successfully
    -   Check if all dependencies in environment.yml are properly installed

-   **Jupyter Notebook won't start**:
    -   Make sure the environment is activated
    -   Try reinstalling Jupyter: `conda install jupyter`

### Getting Help:

If you encounter any issues, please check:

1. That Anaconda is properly installed
2. That the environment.yml file is in the correct location
3. That you're using the correct environment name
4. That all commands are run with the environment activated

## Additional Notes

-   Always ensure your conda environment is activated before running any project code
-   Keep your environment.yml file updated if you add new dependencies
-   You can list all available environments with: `conda env list`
-   To remove an environment: `conda env remove -n [environment_name]`

---

_Happy coding! 🚀_
