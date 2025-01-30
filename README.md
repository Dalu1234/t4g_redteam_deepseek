# Tech for Good at Pitt: Red Team DeepSeek

## Overview
The project aims to red team Deepseek to identify potential vulnerabilities. By engineering prompts, our goal is to understand the robustness of the model against a variety of real world attacks. These results will be used to build a dataset of redteaming prompts that helps understand the performance of the model 

### Key Features
- **Red Teaming**: Simulating real-world attacks to test the model’s security.
- **Modular Design**: Includes several components such as model handling, prompt engineering, metrics collection, and logs.
- **Requirements**: A list of dependencies required to run the project.

## Table of Contents
- [Overview](#overview)
- [Requirements](#requirements)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [TODO](#TODO)
- [License](#license)

## Requirements
Before using this project, ensure you have the following dependencies:

- Python
- OpenAI API
- Additional Libraries:
  - `pandas`

For helping installing the requirments please see [Installation](#install-dependencies).

## Project Structure
The directory structure of the project is as follows:

```
/red-teaming-llm
├── /main.py             # Main file to run red teaming tests
├── /Model.py            # Used to interact with different LLMs
├── /PromptBuilder.py    # Helps engineer prompts
├── /Metrics.py          # Evaluate for attack effectiveness
├── /Log.py              # Logs red teaming effects
├── /requirements.txt    # List of project dependencies
├── /README.md           # This file
```

### File Descriptions
- **main.py**: The entry point for running red teaming tests on the model. This file orchestrates the entire testing process, including model interaction and attack execution.
- **Model.py**: Contains the code to interface with the LLM model. It includes model loading ad prompting. Can be used to interact with any model. 
- **PromptBuilder.py**: Implements prompt engineering strategies to test the model’s vulnerabilities through crafted prompts.
- **Metrics.py**: Defines metrics used to evaluate the effectiveness of the red teaming attacks and the model's response.
- **Log.py**: Handles logging functionality. It records all attempts. 

## Installation
### Clone the Repository
To get started, clone the repository to your local machine and navigate to the directory:

```bash
git clone https://github.com/jal355/t4g_redteam_deepseek.git
cd t4g_redteam_deepseek
```

### Install Dependencies
**Using Conda**
```bash
conda create --name redteam_env --file requirements.txt
#OR
conda create -n readteam_env pandas openai
#then activate the env
conda activate redteam_env
```
**Using pip**
```bash
pip install pandas openai
```

## Usage
### Using the modules
**INSERT EXPLANATION OF CODE**

### Running the Red Team Test
To run the red teaming test, execute the following command:

```bash
python main.py
```

### Example Outputs

**INSERT EXAMPLE OUTPUTS**

### Configuration
Some settings can be adjusted via environment variables:

- **MODEL_NAME**: The model to be tested (e.g., OpenAI GPT-3, HuggingFace models).

You can modify these values directly in the code. 

### Logging Results
Logs of the test results will be saved in the `Results` directory. These logs contain detailed information about each attempt and overall performance values. For example:

```
/logs
├── attempt_01.csv
├── attempt_02.csv
└── summary.csv
```

## TODO
Welcome T4G Dev Team! To get started, please follow these steps:

### Using Command Line
1. Fork the repository: Go to the repository on GitHub and click the "Fork" button. This will create a copy of the repository under your own GitHub account.
2. Clone your fork to your machine: `git clone https://github.com/<YOUR USERNAME>/t4g_redteam_deepseek.git` (This creates a local copy)
3. Create a new branch: `git checkout -b <branch name>`(Branch name should describe what you are changing) (Creating a branch for each feature or update is best practice)
4. Make your changes or add new features.
5. Stage you changes: `git add .` (This adds all modified files. Optionally, you may select only specific files.) 
6. Commit your changes: `git commit -m '<DESCRIPTION>'` 
7. Push to your fork: `git push origin <BRANCH-NAME>` (This adds your changes to your own copy of the repository)
8. Open a pull request: Go to GitHub and select pull request (This pulls your changes into the main copy of the repo)

### Using Github Desktop
1. Fork the repository on the GitHub website. (This creates your own personal copy)
2. Clone your fork to GitHub desktop. Click on File -> Clone Repository (This pulls it to your machine)
3. Create a new branch. Select CurrentBranch -> New Branch (Best practice)
4. Make your changes.
5. Commit your changes. Open GitHub desktop and you will see the changes on the left hand side. Select the files to add and select Commit. 
6. Push your changes. Select Push origin (This pushes the changes to your copy)
7. Open a Pull Request. Go to the Github website and select pull requests. (This pulls them to the main copy)

### Task List
Please remove what you completed on the following list and ensure you add any new features to the README.
- Implement Log file
- Implement PromptBuilder
    - add_details
    - translate
- Implement Metrics
    - toxicity_scores
    - other metrics
- Create prompt success input for the user. This allows the user to review an output and flag it as toxic/not. Please implement using command line. 

Please reach out to Julie or Chase on discord to review the pull request!

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.