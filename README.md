# Bag of stories
Code and data for analysing surprisal and predictability in human and AI-generated stories. 

## Author
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
1. Pre-processing: subtopic detection and story segmentation using TextTiling (nltk, TextTilingTokenizer).
2. Jensen-Shannon distance, Kullback-Leibler divergence (scipy: jensenshannon, entropy), and segment similarity (sentence-transformers) for adjacent segments and segment-previous context computation with: 
- fixed-size story segmentation;
- TextTiling segmentation;
- LLM narrative episode detection. 

## Datasets and related material
1. Popular Grimm stories
- Project Gutenberg, "Household Stories by the Brothers Grimm" (https://www.gutenberg.org/ebooks/19068).
- Selection based on "Grimms' fairy tales / The most beautiful stories of Grimm" - 21.06.2025 (https://www.grimmstories.com/).
2. Forgotten Grimm stories
- English editions (1823, 1826, 1853, vol.1 and 2) mentioned in Ashliman's list (2012-2023) "Grimms' Fairy Tales in English" (https://sites.pitt.edu/~dash/grimm-engl.html).
- Selection based on Rochon's (2016) "Les contes oubliés des frères Grimm" (https://uhearst.ca/app/uploads/2023/05/les-contes-oublies-des-freres-grimm.pdf) and Zipes' (2012) “Ihe Forgotten Tales ofthe Brothers Grimm” (https://publicdomainreview.org/essay/the-forgotten-tales-of-the-brothers-grimm/). 

## Methods
1. Jensen-Shannon Divergence (JSD).
2. Kullback-Leibler Divergence (KLD).
3. Cosine segment similarity (SGS).

## Results
Results are saved by analysis method. Optionally, intermediate results may also be saved in a dedicated folder.

