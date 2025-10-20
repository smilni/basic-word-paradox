# Basic-Word Paradox: Is Basic Vocabulary Harder to Define?

This repository contains the code and data for a computational linguistics research project investigating whether dictionary definitions of "basic" (high-frequency) words differ systematically from those of "non-basic" (low-frequency) words in terms of vocabulary frequency and definition length.

## Research Question

**Do dictionary definitions of "basic" words differ systematically from those of "non-basic" words in terms of the frequency and length of the words used to define them?**

## Hypothesis

We hypothesize that definitions of "basic" concepts should be longer and contain less frequent (i.e., less basic) words, reflecting their conceptual breadth and the limits of simple paraphrase.

## Key Findings

**Contrary to the "Basic-Word Paradox" hypothesis, our analysis reveals that:**

- Definitions of basic words systematically use **higher-frequency vocabulary** than those of non-basic words across all corpora and parts of speech
- Basic words tend to have **slightly longer definitions** in written corpora, but this effect varies by part of speech
- The pattern holds consistently across both WordNet and Wiktionary definitions

## Methodology

### Data Sources
- **Frequency corpora**: Google Web Trillion Word Corpus, OpenSubtitles2018, Google Books Ngrams
- **Definition sources**: WordNet (via NLTK) and Wiktionary (via API)
- **Sample size**: 100 basic + 100 non-basic words per corpus/part-of-speech combination

### Analysis Framework
- **Basicness definition**: Frequency-based (higher frequency = more basic)
- **Metrics**: 
  - Mean/median log-frequency of definition words
  - Definition length in content tokens
  - Statistical testing (Welch's t-test, Mann-Whitney U, Cohen's d)

## Repository Structure

```
├── basic_words_project.ipynb    # Main analysis notebook
├── data/                        # Frequency corpora
│   ├── unigram_freq_books.txt
│   ├── unigram_freq_subtitles.csv
│   └── unigram_freq_web.csv
├── results/                     # Analysis outputs
│   ├── wordnet/                 # WordNet-based results
│   └── wiktionary/              # Wiktionary-based results
├── requirements.txt             # Python dependencies
└── README.md                   # This file
```

## Installation & Usage

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd DSc4L
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the analysis**:
   ```bash
   jupyter notebook basic_words_project.ipynb
   ```

## Dependencies

- pandas==2.3.3
- nltk==3.9.2
- scipy==1.16.2
- matplotlib
- ipywidgets
- matplotlib-venn
- requests

## Results Summary

### Token Frequency Analysis
Across all corpora and parts of speech, basic words are defined using systematically more frequent vocabulary:

- **Web corpus**: 4.5× more frequent wording (p<.001, d=1.27)
- **Books corpus**: 5× more frequent wording (p<.001, d=1.36)  
- **Subtitles corpus**: 2× more frequent wording (p<.001, d=0.56)

### Definition Length Analysis
Results vary by corpus and part of speech:
- **Adjectives & Adverbs**: Consistently longer basic definitions
- **Verbs**: Modest length increases for basic words
- **Nouns**: Mixed results, sometimes favoring non-basic definitions

## Citation

If you use this work, please cite:

```bibtex
@misc{basic_word_paradox_2024,
  title={Basic-Word Paradox: Is Basic Vocabulary Harder to Define?},
  author={[Your Name]},
  year={2024},
  url={https://github.com/[username]/DSc4L}
}
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For questions or collaboration, please contact [your-email@domain.com].

## Acknowledgments

- WordNet lexical database
- Wiktionary community
- Google Books Ngrams
- OpenSubtitles2018 corpus
- NLTK development team
