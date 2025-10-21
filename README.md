# Basic-Word Paradox: Is Basic Vocabulary Harder to Define?

This repository contains the code and data for a project investigating whether dictionary definitions of "basic" (high-frequency) words differ systematically from those of "non-basic" (low-frequency) words in terms of vocabulary frequency and definition length.

For a nicely rendered HTML version of the project, refer to the following website: https://smilni.github.io/basic-word-paradox/.

For the original executable project code, refer to the following [Jupyter Notebook](https://github.com/smilni/basic-word-paradox/blob/main/basic_words_project.ipynb).

NB: the contents of the website and the notebook are the same; use the website to read about the project and the notebook to execute the project code. The website was rendered from the notebook using [Quarto](https://quarto.org).

## Research Question

Do dictionary definitions of "basic" words differ systematically from those of "non-basic" words in terms of the frequency and length of the words used to define them?

## Hypothesis

We hypothesize that definitions of "basic" concepts should be longer and contain less frequent (i.e., less basic) words, reflecting their conceptual breadth and the limits of simple paraphrase.

## Key Findings

Contrary to the "Basic-Word Paradox" hypothesis, our analysis reveals that:

- Definitions of basic words systematically use higher-frequency vocabulary than those of non-basic words across all corpora and parts of speech
- Basic words tend to have slightly longer definitions in written corpora, but this effect varies by part of speech
- The pattern holds consistently across both WordNet and Wiktionary definitions


## Dependencies

Make sure to install dependencies to be able to run the project notebook:
   ```bash
   pip install -r requirements.txt
   ```
