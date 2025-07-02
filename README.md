# Bag of stories
Code and data for analysing surprisal and predictability in human and AI-generated stories. 

## Contributor
Florentina Armaselu  
Luxembourg Centre for Contemporary and Digital History (C2DH), University of Luxembourg

## Setup Instructions
The code was created with Visual Studio Code (VSCode), GitHub Copilot support and Jupyter extension, under Windows 11.
To be run in the Terminal for setting up the virtual environment in the root folder of the project.
````
1. Create and activate a virtual environment (Windows):
    ```
    python -m venv bag_of_stories_env
    bag_of_stories_env\Scripts\activate
    ```

2. Install dependencies:
    ```
    pip install -r requirements.txt
    ```

3. Add the environment as a Jupyter kernel:
    ```
    python -m ipykernel install --user --name=bag_of_stories_env
    ```

4. Open the notebooks and select the `bag_of_stories_env` kernel.
````

## Code
1. Pre-processing: subtopic detection and story segmentation using TextTiling (nltk, TextTilingTokenizer)
2. Jensen-Shannon distance (scipy, jensenshannon) and divergence for adjacent segments and segment-previous context computation with: 
- fixed-size story segmentation;
- TextTiling segmentation;
- LLM narrative episode detection. 

## Datasets and related material
1. Project Gutenberg, "Household Stories by the Brothers Grimm" (https://www.gutenberg.org/ebooks/19068).
2. Selection based on "Grimms' fairy tales / The most beautiful stories of Grimm" - 21.06.2025 (https://www.grimmstories.com/).

