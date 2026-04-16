# Bag of stories
Code and data for analysing surprisal and predictability in human and AI-generated stories. 

## Author
Florentina Armaselu  
Luxembourg Centre for Contemporary and Digital History (C2DH), University of Luxembourg

## Contributor
Cosimo Palma
ArchiveMyLegacy, University of Pisa

## Setup Instructions
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
2.1. If using the requirements file doesn't work, manually install the following libraries:
    ```
    pip install --upgrade llama-cpp-python pandas
    pip install pathlib
    pip install nltk
    pip install sentence-transformers
    pip install seaborn
    pip install ipykernel
    ```
2.2. Optionally, create a requirements.txt file for the current installations:
    ```
    pip freeze > requirements.txt
    ```
3. Add the environment as a Jupyter kernel:
    ```
    python -m ipykernel install --user --name=bag_of_stories_env
    ```

4. Open the notebooks and select the `bag_of_stories_env` kernel.
````

## Code
1. Pre-processing: subtopic detection, story segmentation using TextTiling (nltk, TextTilingTokenizer) and AI story generation.
2. Processing: Jensen-Shannon distance, Kullback-Leibler divergence (scipy: jensenshannon, entropy), and segment similarity (sentence-transformers) for adjacent segments and segment-previous context computation with: 
- equal-length story segmentation;
- TextTiling segmentation. 

## Datasets and related material
1. Popular Grimm stories
- Project Gutenberg, "Household Stories by the Brothers Grimm" (https://www.gutenberg.org/ebooks/19068).
- Selection based on "Grimms' fairy tales / The most beautiful stories of Grimm" - 21.06.2025 (https://www.grimmstories.com/).
2. Forgotten Grimm stories
- English editions (1823, 1826, 1853, vol.1 and 2) mentioned in Ashliman's list (2012-2023) "Grimms' Fairy Tales in English" (https://sites.pitt.edu/~dash/grimm-engl.html).
- Selection based on Rochon's (2016) "Les contes oubliés des frères Grimm" (https://uhearst.ca/app/uploads/2023/05/les-contes-oublies-des-freres-grimm.pdf) and Zipes' (2012) “Ihe Forgotten Tales ofthe Brothers Grimm” (https://publicdomainreview.org/essay/the-forgotten-tales-of-the-brothers-grimm/). 
3. AI-generated stories based on an opening fragment extracted from human stories, either via equal-length segmentation or TextTiling segmentation. 

## Methods
1. Jensen-Shannon Divergence (JSD).
2. Kullback-Leibler Divergence (KLD).
3. Cosine segment similarity (SGS).
4. Correlation (Pearson).

## Results
Results are saved by type of story (human, AI-generated with equal-length and TextTiling start fragment) and analysis method. Optionally, intermediate results may also be saved in a dedicated folder.

5. Citation
Armaselu, Florentina. Palma, Cosimo. (Forthcoming). “Surprisal and Predictability in Grimm’s and AI-Generated Tales: A Study in Computational Narrative Aesthetics.” Proceedings of the 9th International Workshop on Computational Models of Narrative. Madrid, Spain, June 8-10, 2026. https://sites.google.com/ucm.es/cmn26.



